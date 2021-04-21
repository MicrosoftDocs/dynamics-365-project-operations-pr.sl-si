---
title: Povezava dejanskih vrednosti z izvirnimi zapisi
description: Ta tema pojasnjuje, kako povezati dejanske vrednosti z izvirnimi zapisi, kot so vnos časa, vnos stroškov ali dnevniki uporabe materiala.
author: rumant
manager: tfehr
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 545775c4eae6c3dc689f264e7f662471c17b2340
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852609"
---
# <a name="link-actuals-to-original-records"></a>Povezava dejanskih vrednosti z izvirnimi zapisi

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_


V aplikaciji Dynamics 365 Project Operations je *poslovna transakcija* abstrakten koncept, ki ga ne predstavlja entiteta. Vendar so nekatera skupna področja in procesi za entitete zasnovani tako, da uporabljajo koncept poslovnih transakcij. Ta koncept uporabljajo naslednje entitete:

- Podrobnosti vrstice ponudb
- Podrobnosti vrstice pogodb
- Vrstice ocen
- Vrstice dnevnikov
- Opravljeno delo

Od teh entitet so **podrobnosti vrstice ponudb**, **podrobnosti vrstice pogodb** in **vrstice ocen** preslikane na stopnjo ocenjevanja v življenjskem ciklu projekta. Entiteti **Vrstice dnevnikov** in **Dejanske vrednosti** so preslikane na stopnjo izvedbe v življenjskem ciklu projekta.

Project Operations prepozna zapise v teh petih entitetah obravnava kot poslovne transakcije. Edina razlika je, da se zapisi v entitetah, ki so preslikane na stopnjo ocenjevanja, upoštevajo kot finančne napovedi, medtem ko se zapisi v entitetah, ki so preslikane na stopnjo izvedbe, upoštevajo kot finančna dejstva, ki so se že zgodila.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepti, ki so značilni za poslovne transakcije
Naslednji koncepti so značilni za koncept poslovnih transakcij:

- Vrsta transakcije
- Razred transakcije
- Izvor transakcije
- Povezava transakcije

### <a name="transaction-type"></a>Vrsta transakcije

Vrsta transakcije predstavlja čas in kontekst finančnega učinka na projekt. Predstavlja jo nabor možnosti, ki ima v aplikaciji Project Operations naslednje podprte vrednosti:

  - Cena
  - Projektna pogodba
  - Neobračunana prodaja
  - Obračunana prodaja
  - Prodaja znotraj organizacije
  - Cena enote vira

### <a name="transaction-class"></a>Razred transakcije

Razred transakcije predstavlja različne vrste stroškov, ki nastanejo pri projektih. Predstavlja jo nabor možnosti, ki ima v aplikaciji Project Operations naslednje podprte vrednosti:

  - Čas
  - Stroški
  - Material
  - Dajatev
  - Mejnik
  - Davek

Vrednost **Mejnik** se v aplikaciji Project Operations običajno uporablja v poslovni logiki za obračunavanje fiksnih cen.

### <a name="transaction-origin"></a>Izvor transakcije

**Izvor transakcije** je entiteta, ki shranjuje izvor vsake poslovne transakcije. Ko se projekt začne izvajati, bo vsaka poslovna transakcija privedla do druge poslovne transakcije, ki pa bo ustvarila novo in tako naprej. Entiteta izvora transakcije je zasnovana za shranjevanje podatkov o izvoru vsake transakcije za pomoč pri poročanju in sledljivosti. 

### <a name="transaction-connection"></a>Povezava transakcije

**Povezava transakcije** je entiteta, ki shranjuje odnos med dvema podobnima poslovnima transakcijama, kot so stroški in povezani dejanski podatki o prodaji ali stornirane transakcije, ki jih sprožijo obračunske dejavnosti, kot sta potrditev računa ali popravki računa.

Skupaj vam **izvor transakcije** in **povezava transakcije** pomagata spremljati odnose med poslovnimi transakcijami in dejanji, ki povzročijo ustvarjanje določene poslovne transakcije.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Primer: delovanje izvora transakcije s povezavo transakcije

Naslednji primer prikazuje običajno obdelavo časovnih vnosov v življenjskem ciklu projekta v aplikaciji Project Operations.

> ![Obdelovanje časovnih vnosov v življenjskem ciklu projekta v aplikaciji Project Service](media/basic-guide-17.png)
 
1. Pošiljanje časovnega vnosa ustvari dve vrstici dnevnika: eno za strošek in eno za neobračunano prodajo.
2. Morebitna odobritev časovnega vnosa ustvari dve dejanski vrednosti: eno za strošek in eno za neobračunano prodajo.
3. Ko je ustvarjen nov račun projekta, se transakcija vrstice računa ustvari z uporabo podatka iz dejanske vrednosti neobračunane prodaje. 
4. Ko je račun potrjen, sta ustvarjeni dve novi dejanski vrednosti: dejanska vrednost stornirane neobračunane prodaje in obračunane prodaje.

Vsak od teh dogodkov ustvari zapis v entitetah **izvor transakcije** in **povezava transakcije**. Ti novi zapisi pomagajo ustvariti zgodovino odnosov med zapisi, ki so ustvarjeni v časovnem vnosu, vrstici dnevnika, dejanskih podatkih in podrobnostih vrstice računa.

Spodnja tabela prikazuje zapise v entiteti **izvora transakcije** za predhodni potek dela.

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
| GUID popravka računa      | Račun                  | GUID novega dejanskega zneska neobračunane prodaje    | Dejansko                            |                          |

Spodnja tabela prikazuje zapise v entiteti **povezave transakcije** za predhodni potek dela.

| Dogodek                          | Transakcija 1                 | Vloga transakcije 1 | Vrsta transakcije 1           | Transakcija 2                | Vloga transakcije 2 | Vrsta transakcije 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Pošiljanje časovnega vnosa          | GUID vrstice dnevnika (prodaje)     | Neobračunana prodaja     | msdyn_journalline            | GUID vrstice dnevnika (stroška)     | Stroški               | msdyn_journalline  |
| Odobritev časa                  | GUID dejanskega neobračunanega zneska (prodaje)  | Neobračunana prodaja     | msdyn_actual                 | GUID dejanske vrednosti stroška (strošek)       | Stroški               | msdyn_actual       |
| Ustvarjanje računa               | GUID podrobnosti vrstice računa      | Obračunana prodaja       | msdyn_invoicelinetransaction | GUID dejanskega neobračunanega zneska prodaje   | Neobračunana prodaja     | msdyn_actual       |
| Potrditev računa           | GUID storniranega dejanskega zneska         | Storniranje          | msdyn_actual                 | GUID izvorne neobračunane prodaje | Izvirnik           | msdyn_actual       |
| GUID obračunane prodaje              | Obračunana prodaja                  | msdyn_actual       | GUID dejanskega neobračunanega zneska prodaje   | Neobračunana prodaja               | msdyn_actual       |                    |
| Popravek osnutka računa       | GUID transakcije vrstice računa | Nadomeščanje          | msdyn_invoicelinetransaction | GUID obračunane prodaje            | Izvirnik           | msdyn_actual       |
| Potrditev popravka računa     | GUID storniranja obračunane prodaje    | Storniranje          | msdyn_actual                 | GUID obračunane prodaje            | Izvirnik           | msdyn_actual       |
| GUID novega dejanskega zneska neobračunane prodaje | Nadomeščanje                     | msdyn_actual       | GUID obračunane prodaje            | Izvirnik                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
