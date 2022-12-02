---
title: Selitev v celoti zaračunanih mejnikov obračunavanja med prehodom
description: V tem članku je razloženo, kako preseliti mejnike obračunavanja s fiksno ceno, ki so bili stranki zaračunani za odprte projekte pogodbe pred datumom začetka.
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
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Selitev v celoti zaračunanih mejnikov obračunavanja med prehodom

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

## <a name="scenario"></a>Scenarij

Družba Contoso bo začela izvajati storitev Microsoft Dynamics 365 Project Operations za scenarije z viri/brez zalog. Kot del prehodnih dejavnosti mora izvedbena ekipa preseliti odprte projektne pogodbe iz starega sistema. Nekatere projektne pogodbe vključujejo podrobnosti pogodbe, ki uporabljajo način obračunavanja po fiksni ceni in so bile delno že obračunane končni stranki. Izvedbena ekipa mora te mejnike obračunavanja preseliti kot **Račun za stranko je objavljen**, ker jih je treba vključiti v skupno vrednost pogodbe za namene priznavanja prihodkov. Vendar pa to ne sme vplivati na stanja strank v terjatvah in glavni knjigi.

## <a name="solution"></a>Rešitev

### <a name="prerequisites"></a>Zahteve

- Nameščena mora biti storitev Dynamics 365 Finance 10.0.24 ali novejša različica.
- Okolje, v katerem bodo zaključeni koraki selitve, mora biti v načinu vzdrževanja. Med selitvijo mejnikov se ne smejo izvajati nobene druge dejavnosti.
- Korake selitve je treba upoštevati natanko tako, kot je opisano tukaj, in jih je mogoče uporabiti samo za dejavnost prehoda. Microsoft ne podpira nobene druge uporabe te zmožnosti.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Ustvarjanje prehodne različice preslikave dvojnega zapisovanja mejnikov podrobnosti pogodbe o integraciji aplikacije Project Operations 

1. Prepričajte se, da je preslikava cilja za entiteto **Mejniki podrobnosti pogodbe o integraciji aplikacije Project Operations** posodobljena. 

    1. V aplikaciji Finance odprite **Upravljanje podatkov** \> **Podatkovne entitete** in izberite entiteto **Mejniki podrobnosti pogodbe o integraciji aplikacije Project Operations**. 
    2. Izberite **Spremeni preslikave cilja**. 
    3. Na strani **Priprava preslikave za cilj** izberite **Ustvari preslikavo** in nato potrdite, da želite ustvariti preslikavo.

2. Zaustavite in osvežite preslikavo dvojnega zapisovanja **Mejniki podrobnosti pogodbe o integraciji aplikacije Project Operations** (**msdyn\_contractlinescheduleofvalues**). 

    1. Odprite **Upravljanje podatkov** \> **Dvojno zapisovanje**, izberite preslikavo in odprite njene podrobnosti. 
    2. Izberite možnost **Zaustavi** in počakajte, da sistem zaustavi preslikavo. 
    3. Izberite možnost **Osveži tabele**.

3. Dodajte preslikavo za stanje transakcije.

    1. Izberite možnost **Dodaj preslikavo**.
    2. V novi vrstici v stolpcu **Aplikacije za finance in postopke** izberite polje **TRANSSTATUS \[TRANSSTATUS\]**.
    3. V stolpcu **Microsoft Dataverse** izberite **msdyn\_invoicestatus \[Stanje računa\]**.
    4. V stolpcu **Vrsta preslikave** izberite desno puščico (**\>**).
    5. V pogovornem oknu, ki se prikaže, v polju **Smer sinhronizacije** izberite **Dataverse v aplikacije za finance in postopke**.
    6. Izberite možnost **Dodaj pretvorbo**.
    7. V polju **Vrsta pretvorbe** izberite možnost **ValueMap**.
    8. Izberite možnost **Dodaj preslikavo vrednosti**.
    9. V levo polje vnesite **4**. V desno polje vnesite **192350001**. 
    10. Izberite **Shrani** in nato zaprite pogovorno okno.

4. Izberite **Shrani kot**, da shranite različico preslikave dvojnega zapisovanja. 
5. V podoknu **Dodaj tabelo** v polju **Izdajatelj** izberite **Privzeti izdajatelj**.
6. V polje **Različica** vnesite različico.
7. V polje **Opis** vnesite opombo o tej prehodni različici preslikave. 
8. Izberite **Shrani**.
9. Zaženi preslikavo.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Selitev obračunanih mejnikov v okolje Dataverse

1. V okolju Project Operations Dataverse ustvarite mejnike, ki imajo stanje računa **Pripravljeno za izdajo računa**. Ne preselite nobenih mejnikov, ki še niso bili izdani.

    > [!NOTE]
    > Preden preselite mejnike obračunavanja, se prepričajte, da so finančne razsežnosti, ki so povezane s podrobnostmi projektne pogodbe, nastavljene po pričakovanjih. Po končani selitvi finančnih razsežnosti ni mogoče urejati.

2. Ko so vsi mejniki preseljeni, ustavite naslednje preslikave dvojnega zapisovanja:

    - Mejniki podrobnosti pogodbe o integraciji aplikacije Project Operations (msdyn\_contractlinescheduleofvalues)
    - Dejanske vrednosti integracije storitve Project Operations (msdyn\_actuals)
    - Predlog za račune projekta V2 (računi)

    Če želite zaustaviti preslikave, sledite tem korakom:

    1. V aplikaciji Finance odprite **Upravljanje podatkov** \> **Dvojno zapisovanje**, izberite preslikavo in odprite njene podrobnosti.
    2. Izberite možnost **Zaustavi** in počakajte, da sistem zaustavi preslikavo.

3. V okolju Project Operations Dataverse ustvarite in potrdite predračune za mejnike obračunavanja. 

    1. Na zemljevidu mesta odprite projektne pogodbe, izberite pogodbe in nato izberite **Ustvari račune**.
    2. Ko so računi ustvarjeni, jih odprite v meniju **Računi** na zemljevidu mesta in nato izberite **Potrdi**.

    Ta korak ustvari zahtevane zapise v okolju Dataverse. Vendar pa to ne vpliva na finančne podatke in terjatve, ker so bili prej navedene preslikave dvojnega zapisovanja zaustavljene.

4. Ko so vsi predračuni potrjeni, vrnite vse preslikave dvojnega zapisovanja v začetno stanje.

    1. Različico preslikave dvojnega zapisovanja **Mejniki podrobnosti pogodbe o integraciji aplikacije Project Operations** (**msdyn\_contractlinescheduleofvalues**) posodobite na izvorno. 
    2. Na seznamu preslikav izberite preslikavo dvojnega zapisovanja, izberite **Različica preslikave tabele** in nato izberite izvirno različico preslikave tabele.
    3. Izberite **Shrani**.
    4. Znova zaženite naslednje preslikave dvojnega zapisovanja:

        - Mejniki podrobnosti pogodbe o integraciji aplikacije Project Operations (msdyn\_contractlinescheduleofvalues)
        - Dejanske vrednosti integracije storitve Project Operations (msdyn\_actuals)
        - Predlog za račune projekta V2 (računi)

Mejniki so zdaj preseljeni in sistem je pripravljen za naslednje korake v dejavnosti prehoda.
