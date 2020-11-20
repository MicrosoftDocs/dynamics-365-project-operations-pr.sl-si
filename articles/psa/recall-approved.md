---
title: Preklic odobrenih časovnih vnosov ali vnosov stroškov
description: V tej temi najdete informacije o tem, kako prekličete predhodno potrjen čas ali transakcijo stroškov.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 102da39d5940874a8e1f4220437ecdf386a7187b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120563"
---
# <a name="recall-approved-time-or-expense-entries"></a>Preklic odobrenih časovnih vnosov ali vnosov stroškov

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Član projektne ekipe ali druga oseba, ki predloži vnos časa ali stroškov, lahko ta vnos po odobritvi prekliče. Postopek za preklic odobrenega vnosa časa ali stroškov ima dva koraka:

1. Pošiljatelj zahteva preklic.
2. Odobritelj odobri preklic.

## <a name="request-a-recall"></a>Zahteva za preklic

Če želite zahtevati preklic odobrenega vnosa časa ali stroškov, sledite spodnjim korakom.

1. Za časovne vnose odprite **Projekti** \> **Moje delo** \> **Časovni vnos**.

    –ali–

    Za vnose stroškov odprite **Projekti** \> **Moje delo** \> **Stroški**.

2. Pri časovnih vnosih izberite vse časovne vnose za določeno kombinacijo projekta in opravila. Druga možnost je, da v mreži izberete posamezne celice za čas na določen datum za določen projekt.

    –ali–

    Pri vnosih stroškov izberite vrstico za vnos stroškov, ki ga želite preklicati.

3. Izberite **Prekliči**. Prikaže se potrditveno pogovorno okno. Če so bili izbrani vnosi časa in stroškov že odobreni, morate vnesti razlog za preklic.
4. Vnesite razlog za preklic in nato izberite **V redu**, da potrdite postopek. Sistem pošlje osebi, ki je odobrila vnose, zahtevo za odobritev preklica.

> [!NOTE]
> Čeprav je odobrene vnose časa in stroškov mogoče preklicati, pa zahteve za preklic ni mogoče ustvariti, če je kupcu že zaračunan odobren čas ali strošek. Uporabnik, ki poskuša ustvariti zahtevo za preklic, prejme sporočilo, v katerem je navedeno, da časa ali stroškov ni mogoče preklicati, ker je bil vnos že fakturiran.

## <a name="approve-or-reject-a-recall-request"></a>Odobritev ali zavrnitev zahteve za preklic

Če želite odobriti ali zavrniti zahtevo za preklic, sledite spodnjim korakom.

1. Odprite **Projekti** \> **Moje delo** \> **Odobritve**.
2. Na strani s seznamom **Odobritve** spremenite pogled na **Zahteva za preklic za odobritev**. Prikaže se seznam poslanih zahtev za preklic.
3. Izberite enega ali več vnosov in nato **Odobri** ali **Zavrni**.
4. Če ste izbrali **Odobri**, prejmete opozoril, ki pojasnjuje učinek odobritve. Izberite **V redu**, da potrdite postopek. Zahteva za preklic je odobrena.

    –ali–

    Če ste izbrali **Zavrni**, je zahteva za preklic zavrnjena.

> [!NOTE]
> Tako kot pri zahtevi preklica tudi pri odobritvi preklica sistem v vnosih časa ali stroškov poišče dejavnosti fakturiranja. Če je bil vnos že fakturiran ali če je v osnutku računa, bo odobritelj prejel sporočilo o napaki, v katerem je navedeno, da časa ali stroškov ni mogoče odobriti za preklic, ker je bil vnos že fakturiran.

## <a name="impact-of-a-recall-request"></a>Učinek zahteve za preklic

Preklic odobritve ima operativni in finančni učinek.

### <a name="operational-impact"></a>Operativni učinek

Če je zahteva za preklic odobrena, je zapis odobritve označen kot **Zavrnjeno**. Stanje vnosa se spremeni na **Vrnjeno** ali **Zavrnjeno**, odvisno od tega, ali gre za časovni vnos ali vnos stroškov.

Član projektne ekipe si lahko ogleda vnose, jih uredi in nato znova pošlje ali pa jih v celoti izbriše.

Če je zahteva za preklic zavrnjena, stanje vnosa ostane **Odobreno**, vnosa pa član projektne ekipe ali odobritelj v projektu ne more urejati.

### <a name="financial-impact"></a>Finančni učinek

Če je zahteva za preklic odobrena, se ustrezne dejanske vrednosti za stroške in prodajne cene posodobijo tako:

- Polje **Stanje prilagoditve** je posodobljeno na **Prilagojeno**.
- Polje **Stanje obračunavanja** je posodobljeno na **Preklicano**.

Nato se v tabeli »Dejanske vrednosti« ustvarijo postavke storniranja. Če želite ustvariti postavke storniranja, sistem prekopira vrednosti polj iz prvotnih dejanskih vrednosti. Edine vrednosti, ki niso prekopirane, so vrednosti količin. Te vrednosti se stornirajo. Stornirane dejanske vrednosti se ustvarijo za dejanske vrednosti **Stroški** in **Neobračunana prodaja**. Polje **Stanje prilagoditve** za stornirane dejanske vrednosti je nastavljeno na **Ni mogoče prilagoditi**, polje **Stanje obračunavanja** pa na **Preklicano**. Zaradi teh sprememb se zabeleženi stroški in zaostali prihodki v projektu ne bodo več upoštevali pri zneskih, ki jih predstavljajo te dejanske vrednosti.

Če je zahteva za preklic zavrnjena, ni finančnega vpliva na projekt.

## <a name="changes-to-time-entry-records"></a>Spremembe zapisov časovnega vnosa

Spodnja slika prikazuje spremembe, do katerih pride pri odobrenih časovnih vnosih, ko so ti preklicani.

![Prehodi stanja časovnega vnosa](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Spremembe zapisov vnosa stroškov

Spodnja slika prikazuje spremembe, do katerih pride pri odobrenih vnosih stroškov, ko so ti preklicani.

![Prehodi stanja vnosa stroškov](media/ExpenseEntryStateTransitions.png)
