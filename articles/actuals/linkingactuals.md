---
title: Izvor transakcije – povežite dejanske podatke z njihovim virom
description: Ta tema pojasnjuje, kako se koncept izvora transakcije uporablja za povezavo dejanskih dejstev z izvirnimi izvornimi zapisi, kot so vnos časa, vnos stroškov ali dnevniki porabe materiala.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 908f78f7d58ec4b18f37d03b6fa7c4e2295491fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584846"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Izvor transakcije – povežite dejanske podatke z njihovim virom

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Zapisi izvora transakcij so ustvarjeni za povezavo dejanskih dejstev z njihovim virom, kot so vnosi časa, vnosi stroškov, dnevniki porabe materiala in projektni računi.

Naslednji primer prikazuje običajno obdelavo časovnih vnosov v življenjskem ciklu projekta v aplikaciji Project Operations.

> ![Celoten čas obdelave v projektnih operacijah.](media/basic-guide-17.png)
 
1. Predložitev časovnega vnosa povzroči, da se ustvarita dve vrstici dnevnika: ena za stroške in ena za neobračunano prodajo.
2. Končna odobritev časovnega vnosa povzroči, da se ustvarita dve dejanski vrednosti: ena za stroške in ena za neobračunano prodajo.
3. Ko uporabnik ustvari račun projekta, se transakcija vrstice računa ustvari z uporabo podatka iz dejanske vrednosti neobračunane prodaje.
4. Ko je račun potrjen, sta ustvarjeni dve novi dejanski vrednosti: stornirana neobračunana prodaja in dejanska vrednost obračunane prodaje.

Vsak dogodek v tem delovnem toku obdelave sproži ustvarjanje zapisov v izvorni entiteti transakcije, da se pomaga zgraditi sled Odnosi med temi zapisi, ki so ustvarjeni med vnosom časa, vrstico dnevnika, dejanskimi podatki in podatki v vrstici računa.

Spodnja tabela prikazuje zapise v entiteti izvora transakcije izvora za predhodni potek dela.

| Dogodek                        | Izvor                   | Vrsta izvora                       | Transakcija                       | Vrsta transakcije         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Pošiljanje časovnega vnosa        | GUID zapisa časovnega vnosa   | Časovni vnos                        | GUID zapisa vrstice dnevnika (stroška)   | Vrstica dnevnika             |
| GUID zapisa časovnega vnosa       | Časovni vnos               | GUID zapisa vrstice dnevnika (prodaje)  | Vrstica dnevnika                      |                          |
| Odobritev časa                | GUID zapisa vrstice dnevnika | Vrstica dnevnika                      | GUID zapisa neobračunane prodaje        | Dejansko                   |
| GUID zapisa časovnega vnosa       | Časovni vnos               | GUID zapisa neobračunane prodaje        | Dejansko                            |                          |
| GUID zapisa vrstice dnevnika     | Vrstica dnevnika             | GUID zapisa dejanskih stroškov           | Dejansko                            |                          |
| GUID zapisa časovnega vnosa       | Časovni vnos               | GUID zapisa dejanskih stroškov           | Dejansko                            |                          |
| Ustvarjanje računa             | GUID zapisa časovnega vnosa   | Časovni vnos                        | GUID transakcije vrstice računa     | Transakcija vrstice računa |
| GUID zapisa vrstice dnevnika     | Vrstica dnevnika             | GUID transakcije vrstice računa     | Transakcija vrstice računa          |                          |
| Potrditev računa         | GUID vrstice računa        | Vrstica računa                      | GUID zapisa obračunane prodaje          | Dejansko                   |
| GUID računa                 | Račun                  | GUID zapisa obračunane prodaje          | Dejansko                            |                          |
| GUID podrobnosti vrstice računa     | Podrobnosti vrstice računa      | GUID zapisa obračunane prodaje          | Dejansko                            |                          |
| GUID zapisa časovnega vnosa       | Časovni vnos               | GUID zapisa obračunane prodaje          | Dejansko                            |                          |
| GUID zapisa vrstice dnevnika     | Vrstica dnevnika             | GUID zapisa obračunane prodaje          | Dejansko                            |                          |
| GUID zapisa časovnega vnosa       | Časovni vnos               | GUID storniranja neobračunane prodaje      | Dejansko                            |                          |
| GUID zapisa vrstice dnevnika     | Vrstica dnevnika             | GUID storniranja neobračunane prodaje      | Dejansko                            |                          |
| Popravek osnutka računa     | GUID prejšnjih podr. vr. rač.             | Transakcija vrstice računa          | GUID popravka podr. vr. rač.               | Transakcija vrstice računa |
| GUID prejšnje vrst. rač.                  | Vrstica računa             | GUID popravka podr. vr. rač.               | Transakcija vrstice računa          |                          |
| GUID prejšnjega računa             | Račun                  | GUID popravka podr. vr. rač.               | Transakcija vrstice računa          |                          |
| GUID zapisa časovnega vnosa       | Časovni vnos               | GUID popravka podr. vr. rač.               | Transakcija vrstice računa          |                          |
| GUID zapisa vrstice dnevnika     | Vrstica dnevnika             | GUID popravka podr. vr. rač.               | Transakcija vrstice računa          |                          |
| Potrjen popravek računa | GUID prejšnjih podr. vr. rač.             | Transakcija vrstice računa          | GUID storniranega dejanskega zneska obračunane prodaje | Dejansko                   |
| GUID prejšnje vrst. rač.                  | Vrstica računa             | GUID storniranega dejanskega zneska obračunane prodaje | Dejansko                            |                          |
| GUID prejšnjega računa             | Račun                  | GUID storniranega dejanskega zneska obračunane prodaje | Dejansko                            |                          |
| GUID zapisa časovnega vnosa       | Časovni vnos               | GUID storniranega dejanskega zneska obračunane prodaje | Dejansko                            |                          |
| GUID zapisa vrstice dnevnika     | Vrstica dnevnika             | GUID storniranega dejanskega zneska obračunane prodaje | Dejansko                            |                          |
| GUID prejšnjih podr. vr. rač.                 | Transakcija vrstice računa | GUID novega dejanskega zneska neobračunane prodaje    | Dejansko                            |                          |
| GUID prejšnje vrst. rač.                  | Vrstica računa             | GUID novega dejanskega zneska neobračunane prodaje    | Dejansko                            |                          |
| GUID prejšnjega računa             | Račun                  | GUID novega dejanskega zneska neobračunane prodaje    | Dejansko                            |                          |
| GUID zapisa časovnega vnosa       | Časovni vnos               | GUID novega dejanskega zneska neobračunane prodaje    | Dejansko                            |                          |
| GUID zapisa vrstice dnevnika     | Vrstica dnevnika             | GUID novega dejanskega zneska neobračunane prodaje    | Dejansko                            |                          |
| GUID popravka podr. vr. rač.          | Transakcija vrstice računa | GUID novega dejanskega zneska neobračunane prodaje    | Dejansko                            |                          |
| GUID popravka vrst. rač.           | Vrstica računa             | GUID novega dejanskega zneska neobračunane prodaje    | Dejansko                            |                          |
| GUID popravka računa      | Kupec                  | GUID novega dejanskega zneska neobračunane prodaje    | Dejansko                            |                          |


Naslednja slika prikazuje povezave, ki so ustvarjene med dejanskimi stvarmi in njihovimi viri na različnih dogodkih na primeru časovnih vnosov v Operacijah projekta.

> ![Kako so dejanski podatki povezani z izvornimi zapisi v Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
