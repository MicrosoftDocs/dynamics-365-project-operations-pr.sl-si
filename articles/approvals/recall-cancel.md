---
title: Odpoklic predhodno odobrenih vnosov
description: Ta članek pojasnjuje, kako lahko član projektne ekipe zahteva preklic predhodno predloženih in odobrenih zapisov o času, stroških in uporabi materiala ter kako lahko vodja projektov odobri ali zavrne zahteve za preklic.
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

Član projektne ekipe, ki predloži vnos časa, stroškov ali uporabe materiala, lahko ta vnos po odobritvi prekliče. Postopek preklica ima dva glavna koraka:

1. Pošiljatelj zahteva preklic.
2. Odobritelj odobri zahtevo za preklic.

## <a name="request-a-recall"></a>Zahteva za preklic

Če želite zahtevati preklic odobrenega vnosa časa, stroškov ali uporabe materiala, sledite tem korakom.

1. Sledite enemu od teh korakov, odvisno od vrste vnosa, ki ga želite preklicati:

    - Za časovne vnose odprite **Projekti** \> **Moje delo** \> **Časovni vnos** in izberite vse časovne vnose za določeno kombinacijo projekta in opravila. Druga možnost je, da v mreži izberete posamezne celice za čas na določen datum za določen projekt.
    - Za vnose stroškov odprite **Projekti** \> **Moje delo** \> **Stroški** izberite vrstico za vnos stroškov, ki ga želite preklicati.
    - Za vnose uporabe materiala odprite **Projekti** \> **Moje delo** \> **Dnevnik uporabe materiala** izberite vrstico za vnos uporabe materiala, ki jo želite preklicati.

2. Izberite **Prekliči**. Prikaže se potrditveno pogovorno okno. Če so bili izbrani vnosi časa, stroškov in uporabe materiala že odobreni, morate vnesti razlog za preklic.
3. Vnesite razlog za preklic in nato izberite **V redu**, da potrdite postopek. Sistem pošlje osebi, ki je odobrila vnose, zahtevo za odobritev preklica.

> [!IMPORTANT]
> Ne morete ustvariti zahteve za preklic odobrenega vnosa časa, stroškov ali uporabe materiala, ki je že bila zaračunana stranki. Če to poskusite, prejmete sporočilo, v katerem je navedeno, da vnosa časa, stroškov ali uporabe materiala ni mogoče preklicati, ker je bil vnos že fakturiran. V tem primeru lahko zahtevate preklic vnosa le, če se za izdajo celotnega dobroimetja ali vračila stranki na prvotnem računu uporabi popravljeni račun.

## <a name="approve-or-reject-a-recall-request"></a>Odobritev ali zavrnitev zahteve za preklic

Če želite odobriti ali zavrniti zahtevo za preklic, sledite spodnjim korakom.

1. Odprite **Projekti** \> **Moje delo** \> **Odobritve**.
2. Na strani s seznamom **Odobritve** spremenite pogled na **Zahteva za preklic za odobritev**. Prikaže se seznam poslanih zahtev za preklic.
3. Izberite enega ali več vnosov in nato **Odobri** ali **Zavrni**.
4. Če ste izbrali **Odobri**, prejmete opozoril, ki pojasnjuje učinek odobritve. Izberite **V redu**, da potrdite postopek. Zahteva za preklic je odobrena.

    –ali–

    Če ste izbrali **Zavrni**, je zahteva za preklic zavrnjena.

> [!IMPORTANT]
> Če je preklic odobren, tako kot če je zahtevan, sistem v vnosih časa, stroškov ali uporabe materiala poišče dejavnosti fakturiranja. Če je bil vnos že fakturiran ali če je v osnutku računa, odobritelj prejme sporočilo o napaki, v katerem je navedeno, da časa ali stroškov ni mogoče odobriti za preklic, ker je bil vnos že fakturiran. V tem primeru lahko odobritelj odobri preklic le, če se za izdajo celotnega dobroimetja ali vračila stranki na prvotnem računu uporabi popravljeni račun.

## <a name="impact-of-a-recall-request"></a>Učinek zahteve za preklic

Preklic odobritve ima operativni in finančni učinek.

### <a name="operational-impact"></a>Operativni učinek

Če je zahteva za preklic odobrena, je zapis odobritve označen kot **Zavrnjeno**. Stanje vnosa se spremeni na **Vrnjeno** ali **Zavrnjeno**, odvisno od tega, ali gre za vnos časa, stroškov ali uporabe materiala.

Član projektne ekipe si lahko ogleda vnose, jih uredi in nato znova pošlje ali pa jih v celoti izbriše.

Če je zahteva za preklic zavrnjena, stanje vnosa ostane **Odobreno**, vnosa pa član projektne ekipe ali odobritelj v projektu ne more urejati.

### <a name="financial-impact"></a>Finančni učinek

Če je zahteva za preklic odobrena, se ustrezne dejanske vrednosti za stroške in prodajne cene posodobijo tako:

- Polje **Stanje prilagoditve** je posodobljeno na **Prilagojeno**.
- Polje **Stanje obračunavanja** je posodobljeno na **Preklicano**.

Nato se v tabeli »Dejanske vrednosti« ustvarijo postavke storniranja. Če želite ustvariti postavke storniranja, sistem prekopira vrednosti polj iz prvotnih dejanskih vrednosti. Edine vrednosti, ki niso prekopirane, so vrednosti količin. Te vrednosti se stornirajo. Stornirane dejanske vrednosti se ustvarijo za dejanske vrednosti **Stroški** in **Neobračunana prodaja**. Polje **Stanje prilagoditve** za stornirane dejanske vrednosti je nastavljeno na **Ni mogoče prilagoditi**, polje **Stanje obračunavanja** pa na **Preklicano**. Zaradi teh sprememb se zabeleženi stroški in zaostali prihodki v projektu ne bodo več upoštevali pri zneskih, ki jih predstavljajo te dejanske vrednosti.

Če je zahteva za preklic zavrnjena, ni finančnega vpliva na projekt.

## <a name="changes-to-time-entry-records"></a>Spremembe zapisov časovnega vnosa

Spodnja slika prikazuje spremembe, do katerih pride pri odobrenih časovnih vnosih, in ustrezne zapise o odobritvah, ko so ti vnosi preklicani.

![Prehodi stanja vnosa stroškov.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Spremembe zapisov vnosa stroškov in uporabe materiala

Spodnja slika prikazuje spremembe, do katerih pride pri odobrenih vnosih stroškov in uporabe materiala, in ustrezne zapise o odobritvah, ko so ti vnosi preklicani.

![Prehodi stanja vnosa stroškov.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
