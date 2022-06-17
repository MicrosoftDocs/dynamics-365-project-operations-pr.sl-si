---
title: Odpoklic predhodno odobrenih vnosov
description: Ta članek pojasnjuje, kako lahko član projektne skupine zahteva odpoklic predhodno predloženih in odobrenih evidenc o času, stroških in porabi materiala ter kako lahko vodja projekta odobri ali zavrne zahteve za odpoklic.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930384"
---
# <a name="recall-previously-approved-entries"></a>Odpoklic predhodno odobrenih vnosov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Član projektne skupine, ki predloži vnos časa, stroškov ali porabe materiala, lahko ta vnos prikliče, potem ko je bil odobren. Postopek odpoklica ima dva glavna koraka:

1. Pošiljatelj zahteva preklic.
2. Odobrnik odobri zahtevo za odpoklic.

## <a name="request-a-recall"></a>Zahteva za preklic

Sledite tem korakom, da zahtevate odpoklic odobrenih vnosov časa, stroškov ali porabe materiala.

1. Sledite enemu od teh korakov, odvisno od vrste vnosa, ki ga želite priklicati:

    - Za vnose časa pojdite na **Projekti** \> **Moje delo** \> **Vnos časa** in izberite vse časovne vnose za določeno kombinacijo projekta in opravila. Druga možnost je, da v mreži izberete posamezne celice za čas na določen datum za določen projekt.
    - Za vnose stroškov pojdite na **Projekti** \> **Moje delo** \> **Stroški** in izberite vrstico za vnos stroškov, ki ga želite priklicati.
    - Za vnose o porabi materiala pojdite na **Projekti** \> **Moje delo** \> **Dnevnik porabe materiala** in izberite vrstico za vnos porabe materiala, ki ga želite priklicati.

2. Izberite **Prekliči**. Prikaže se potrditveno pogovorno okno. Če so bili izbrani vnosi časa, stroškov ali porabe materiala že odobreni, boste pozvani, da vnesete razlog za odpoklic.
3. Vnesite razlog za preklic in nato izberite **V redu**, da potrdite postopek. Sistem pošlje osebi, ki je odobrila vnose, zahtevo za odobritev preklica.

> [!IMPORTANT]
> Ne morete ustvariti zahteve za odpoklic za odobreni vnos časa, stroškov ali porabe materiala, ki je že bil zaračunan stranki. Če poskusite, prejmete sporočilo, ki navaja, da vnosa časa, stroškov ali porabe materiala ni mogoče priklicati, ker je bil že zaračunan. V tem primeru lahko zahtevate odpoklic vnosa le, če se za izdajo celotnega dobropisa ali vračila kupcu na izvirnem računu uporabi popravni račun.

## <a name="approve-or-reject-a-recall-request"></a>Odobritev ali zavrnitev zahteve za preklic

Če želite odobriti ali zavrniti zahtevo za preklic, sledite spodnjim korakom.

1. Odprite **Projekti** \> **Moje delo** \> **Odobritve**.
2. Na strani s seznamom **Odobritve** spremenite pogled na **Zahteva za preklic za odobritev**. Prikaže se seznam poslanih zahtev za preklic.
3. Izberite enega ali več vnosov in nato **Odobri** ali **Zavrni**.
4. Če ste izbrali **Odobri**, prejmete opozoril, ki pojasnjuje učinek odobritve. Izberite **V redu**, da potrdite postopek. Zahteva za preklic je odobrena.

    –ali–

    Če ste izbrali **Zavrni**, je zahteva za preklic zavrnjena.

> [!IMPORTANT]
> Ko je odpoklic odobren, tako kot takrat, ko je zahtevan, sistem preveri kakršno koli dejavnost izdajanja računov za vnose časa, stroškov ali porabe materiala. Če je bil vnos že zaračunan ali če je na osnutku računa, odobritelj prejme sporočilo o napaki, ki navaja, da časa ali stroškov ni mogoče odobriti za odpoklic, ker je bil že zaračunan. V tem primeru lahko odobritelj odobri odpoklic le, če se za izdajo celotnega dobropisa ali vračila kupcu na izvirnem računu uporabi korektivni račun.

## <a name="impact-of-a-recall-request"></a>Učinek zahteve za preklic

Preklic odobritve ima operativni in finančni učinek.

### <a name="operational-impact"></a>Operativni učinek

Če je zahteva za preklic odobrena, je zapis odobritve označen kot **Zavrnjeno**. Status vnosa se spremeni v eno ali drugo **Vrnjeno** oz **Zavrnjeno**, odvisno od tega, ali gre za vnos časa ali vnos stroškov ali porabe materiala.

Član projektne skupine si lahko ogleda vnose, jih ureja in nato znova odda ali popolnoma izbriše vnose.

Če je zahteva za preklic zavrnjena, stanje vnosa ostane **Odobreno**, vnosa pa član projektne ekipe ali odobritelj v projektu ne more urejati.

### <a name="financial-impact"></a>Finančni učinek

Če je zahteva za preklic odobrena, se ustrezne dejanske vrednosti za stroške in prodajne cene posodobijo tako:

- Polje **Stanje prilagoditve** je posodobljeno na **Prilagojeno**.
- Polje **Stanje obračunavanja** je posodobljeno na **Preklicano**.

Nato se v tabeli »Dejanske vrednosti« ustvarijo postavke storniranja. Če želite ustvariti postavke storniranja, sistem prekopira vrednosti polj iz prvotnih dejanskih vrednosti. Edine vrednosti, ki niso prekopirane, so vrednosti količin. Te vrednosti se stornirajo. Stornirane dejanske vrednosti se ustvarijo za dejanske vrednosti **Stroški** in **Neobračunana prodaja**. Polje **Stanje prilagoditve** za stornirane dejanske vrednosti je nastavljeno na **Ni mogoče prilagoditi**, polje **Stanje obračunavanja** pa na **Preklicano**. Zaradi teh sprememb se zabeleženi stroški in zaostali prihodki v projektu ne bodo več upoštevali pri zneskih, ki jih predstavljajo te dejanske vrednosti.

Če je zahteva za preklic zavrnjena, ni finančnega vpliva na projekt.

## <a name="changes-to-time-entry-records"></a>Spremembe zapisov časovnega vnosa

Naslednja slika prikazuje spremembe, ki se pojavijo za odobrene vnose časa in ustrezne zapise o odobritvi, ko so odpoklicani.

![Prehodi med stanjem vnosa časa.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Spremembe evidenc o stroških in porabi materiala

Naslednja slika prikazuje spremembe, ki se pojavijo za odobrene vnose stroškov in porabe materiala ter ustrezne zapise o odobritvah, ko so odpoklicani.

![Prehodi med stanjem vnosa odhodkov.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
