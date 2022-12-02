---
title: Izvori transakcij – povezovanje dejanskih vrednosti z njihovim virom
description: Ta članek pojasnjuje, kako se koncept izvorov transakcij uporablja za povezovanje dejanskih vrednosti z izvornimi zapisi, kot so vnos časa, vnos stroškov ali dnevniki uporabe materiala.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921322"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Izvori transakcij – povezovanje dejanskih vrednosti z njihovim virom

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Zapisi o izvoru transakcij so ustvarjeni za povezavo dejanskih vrednosti z njihovim virom, kot so časovni vnosi, vnosi stroškov, dnevniki porabe materiala in računi za projekt.

Naslednji primer prikazuje običajno obdelavo časovnih vnosov v življenjskem ciklu projekta v aplikaciji Project Operations.

> ![Obdelovanje časovnih vnosov v aplikaciji Project Operations.](media/basic-guide-17.png)
 
1. Pošiljanje časovnega vnosa povzroči ustvarjanje dveh vrstic dnevnika: eno za strošek in eno za neobračunano prodajo.
2. Morebitna odobritev časovnega vnosa povzroči ustvarjanje dveh dejanskih vrednosti: eno za strošek in eno za neobračunano prodajo.
3. Ko uporabnik ustvari račun projekta, se transakcija vrstice računa ustvari z uporabo podatka iz dejanske vrednosti neobračunane prodaje.
4. Ko je račun potrjen, sta ustvarjeni dve novi dejanski vrednosti: stornirana neobračunana prodaja in dejanska vrednost obračunane prodaje.

Vsak dogodek v tem poteku dela obdelave sproži ustvarjanje zapisov v entiteti izvora transakcije, ki pomagajo sestaviti sled odnosov med temi zapisi, ki so ustvarjeni za podrobnosti časovnega vnosa, vrstice dnevnika, dejansko vrednost in vrstice računa.

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


Naslednja slika prikazuje povezave, ki so ustvarjene med dejanskimi vrednostmi in njihovimi viri ob različnih dogodkih z uporabo primera časovnih vnosov v aplikaciji Project Operations.

> ![Kako so dejanske vrednosti povezane z izvornimi zapisi v aplikaciji Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
