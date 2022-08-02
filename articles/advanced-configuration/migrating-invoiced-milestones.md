---
title: Preselitev mejnikov zaračunavanja v celoti ob prekinitvi
description: V tem članku je razloženo, kako preseliti mejnike zaračunavanja s fiksno ceno, ki so bili stranki zaračunani za pogodbe o odprtih projektih pred datumom objave.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028722"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Preselitev mejnikov zaračunavanja v celoti ob prekinitvi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

## <a name="scenario"></a>Scenarij

Contoso je objavljen z Microsoftom Dynamics 365 Project Operations za scenarije virov/nezaloženih. Kot del prekinitvenih aktivnosti mora izvajalska ekipa preseliti odprte projektne pogodbe iz starega sistema. Nekatere projektne pogodbe vključujejo pogodbene postavke, ki uporabljajo metodo zaračunavanja po fiksni ceni in so bile delno že zaračunane končnemu kupcu. Implementacijska ekipa mora te mejnike zaračunavanja preseliti kot **Račun stranke objavljen**, ker jih je treba vključiti v skupno vrednost pogodbe za namene priznavanja prihodkov. Vendar to ne sme vplivati na stanja strank v terjatvah in glavni knjigi.

## <a name="solution"></a>Rešitev

### <a name="prerequisites"></a>Zahteve

- Dynamics 365 Finance 10.0.24 ali novejša mora biti nameščena.
- Okolje, v katerem bodo zaključeni koraki selitve, mora biti v vzdrževalnem načinu. Med selitvijo mejnikov se ne smejo izvajati nobene druge dejavnosti.
- Korake selitve je treba upoštevati natanko tako, kot je opisano tukaj, in jih je mogoče uporabiti samo za dejavnost preklopa. Microsoft ne podpira nobene druge uporabe te zmožnosti.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Ustvarite prenovljeno različico preslikave dvojnega pisanja mejnikov pogodbene vrstice integracije Project Operations 

1. Prepričajte se, da je preslikava cilja za **Mejniki pogodbene linije integracije projektnih operacij** subjekt je posodobljen. 

    1. V Financah pojdite na **Upravljanje podatkov** \> **Podatkovne entitete** in izberite **Mejniki pogodbene linije integracije projektnih operacij** entiteta. 
    2. Izberite **Spremenite ciljne preslikave**. 
    3. Na **Uprizoritev zemljevida za cilj** stran, izberite **Ustvari preslikavo** in nato potrdite, da želite ustvariti preslikavo.

2. Ustavite in osvežite **Mejniki pogodbene linije integracije projektnih operacij** (**msdyn\_ contractlinescheduleofvalues**) zemljevid dvojnega pisanja. 

    1. Pojdi do **Upravljanje podatkov** \> **Dvojno pisanje**, izberite zemljevid in odprite njegove podrobnosti. 
    2. Izberite **Stop** in počakajte, da sistem ustavi zemljevid. 
    3. Izberite **Osveži tabele**.

3. Dodajte preslikavo za stanje transakcije.

    1. Izberite **Dodajte preslikavo**.
    2. Na novi liniji, v **Aplikacije za finance in poslovanje** izberite stolpec **TRANSSTATUS\[ TRANSSTATUS\]** polje.
    3. V **Microsoft Dataverse** stolpec izberite **msdyn\_ status računa\[ Stanje računa\]**.
    4. V **Vrsta zemljevida** izberite desno puščico (**\>**).
    5. V pogovornem oknu, ki se prikaže, v **Smer sinhronizacije** polje izberite **Dataverse v aplikacije za finance in poslovanje**.
    6. Izberite **Dodaj transformacijo**.
    7. V **Vrsta preoblikovanja** polje izberite **ValueMap**.
    8. Izberite **Dodajte preslikavo vrednosti**.
    9. V levem polju vnesite **4**. V desnem polju vnesite **192350001**. 
    10. Izberite **Shrani** in zaprite pogovorno okno.

4. Izberite **Shrani kot** da shranite različico zemljevida dvojnega pisanja. 
5. V **Dodaj tabelo** podoknu, v **Založnik** polje izberite **Privzeti založnik**.
6. V **Različica** vnesite različico.
7. V **Opis** polje vnesite opombo o tej različici zemljevida. 
8. Izberite **Shrani**.
9. Zaženi zemljevid.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Preseli fakturirane mejnike v Dataverse okolju

1. V projektnih operacijah Dataverse okolje, ustvarite mejnike, ki imajo status računa **Pripravljeno za fakturiranje**. Na tej točki ne preselite nobenih mejnikov, ki še niso bili fakturirani.

    > [!NOTE]
    > Preden preselite mejnike obračunavanja, se prepričajte, da so finančne razsežnosti, ki so povezane s pogodbeno vrstico projekta, nastavljene po pričakovanjih. Po končani selitvi finančnih razsežnosti ni mogoče urejati.

2. Ko so vsi mejniki preseljeni, ustavite naslednje preslikave dvojnega pisanja:

    - Mejniki pogodbene vrstice integracije projektnih operacij (msdyn\_ contractlinescheduleofvalues)
    - Dejanske vrednosti integracije storitve Project Operations (msdyn\_actuals)
    - Predlog za račune projekta V2 (računi)

    Če želite zaustaviti zemljevide, sledite tem korakom:

    1. V Financah pojdite na **Upravljanje podatkov** \> **Dvojno pisanje**, izberite zemljevid in odprite njegove podrobnosti.
    2. Izberite **Stop** in počakajte, da sistem ustavi zemljevid.

3. V projektnih operacijah Dataverse okolje, ustvarite in potrdite predračune za obračunske mejnike. 

    1. Na zemljevidu mesta pojdite na projektne pogodbe, izberite pogodbe in nato izberite **Ustvarite račune**.
    2. Ko so računi ustvarjeni, jih odprite v **Računi** meni na zemljevidu mesta in nato izberite **Potrdi**.

    Ta korak ustvari zahtevane zapise v Dataverse okolju. Vendar pa to ne vpliva na finance in terjatve, ker so bili prej navedeni zemljevidi dvojnega pisanja ustavljeni.

4. Ko so vsi predračuni potrjeni, vrnite vse zemljevide dvojnega pisanja v začetno stanje.

    1. Posodobite različico **Mejniki pogodbene linije integracije projektnih operacij** (**msdyn\_ contractlinescheduleofvalues**) preslikava dvojnega pisanja nazaj na izvirnik. 
    2. Na seznamu zemljevidov izberite zemljevid z dvojnim pisanjem, izberite **Različica tabele zemljevida** in nato izberite izvirno različico zemljevida tabele.
    3. Izberite **Shrani**.
    4. Znova zaženite naslednje zemljevide z dvojnim pisanjem:

        - Mejniki pogodbene vrstice integracije projektnih operacij (msdyn\_ contractlinescheduleofvalues)
        - Dejanske vrednosti integracije storitve Project Operations (msdyn\_actuals)
        - Predlog za račune projekta V2 (računi)

Mejniki so zdaj preseljeni in sistem je pripravljen za naslednje korake v dejavnosti preklopa.
