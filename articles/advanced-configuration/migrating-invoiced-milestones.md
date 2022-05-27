---
title: Prenesite v celoti zaračunane mejnike obračunavanja ob preseku
description: Ta tema pojasnjuje, kako preseliti mejnike obračunavanja s fiksno ceno, ki so bili zaračunani stranki za pogodbe o odprtih projektih pred datumom objave.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ccdba864a68521024b2c479c12cf5cea616c5bbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576290"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Prenesite v celoti zaračunane mejnike obračunavanja ob preseku

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

## <a name="scenario"></a>Scenarij

Contoso bo v živo z Microsoftom Dynamics 365 Project Operations za scenarije virov/brez zalog. V okviru dejavnosti preklopa mora implementacijska skupina preseliti odprte projektne pogodbe iz starega sistema. Nekatere projektne pogodbe vključujejo pogodbene linije, ki uporabljajo metodo obračunavanja s fiksno ceno in so že delno zaračunane končnemu odjemalcu. Izvedbena skupina mora te mejnike obračunavanja preseliti kot **Račun stranke objavljen**, ker jih je treba za namene pripoznanja prihodkov vključiti v skupno vrednost pogodbe. Vendar to ne sme vplivati na stanja strank v Terjatvah in Glavni knjigi.

## <a name="solution"></a>Rešitev

### <a name="prerequisites"></a>Zahteve

- Namestiti morate Dynamics 365 Finance 10.0.24 ali novejšo različico.
- Okolje, kjer bodo koraki selitve zaključeni, mora biti v načinu vzdrževanja. Med selitvijo mejnikov se ne sme izvajati nobenih drugih dejavnosti.
- Korake selitve je treba natančno upoštevati, kot je opisano tukaj, in jih je mogoče uporabiti samo za dejavnost preklopa. Microsoft ne podpira nobene druge uporabe te zmožnosti.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Ustvarite prekinjeno različico mejnikov pogodbene vrstice integracijskih operacij z dvojnim pisanjem 

1. Prepričajte se, da je ciljna preslikava za **Mejniki pogodbene linije za integracijo projektnih operacij** subjekt je posodobljen. 

    1. V Financah pojdite na **Upravljanje s podatki** \> **Podatkovne entitete** in izberite **Mejniki pogodbene linije za integracijo projektnih operacij** entiteta. 
    2. Izberite **Spremenite ciljne preslikave**. 
    3. Na **Uprizoritev zemljevida do cilja** stran, izberite **Ustvari preslikavo** in nato potrdite, da želite ustvariti preslikavo.

2. Ustavite in osvežite **Mejniki pogodbene linije za integracijo projektnih operacij** (**msdyn\_ pogodbeni razpored vrednosti**) zemljevid z dvojnim zapisom. 

    1. Pojdi do **Upravljanje s podatki** \> **Dvojno pisanje**, izberite zemljevid in odprite njegove podrobnosti. 
    2. Izberite **Ustavi se** in počakajte, da sistem ustavi zemljevid. 
    3. Izberite **Osvežite tabele**.

3. Dodajte preslikavo za status transakcije.

    1. Izberite **Dodajte preslikavo**.
    2. Na novi liniji, v **Aplikacije za finance in operacije** stolpec, izberite **TRANSSTATUS\[ TRANSSTATUS\]** polje.
    3. V **Microsoft Dataverse** stolpec, izberite **msdyn\_ stanje računa\[ Stanje računa\]**.
    4. V **Vrsta zemljevida** stolpec, izberite puščico desno (**\>**).
    5. V pogovornem oknu, ki se prikaže, v **Smer sinhronizacije** polje, izberite **Dataverse v aplikacije Finance in Operations**.
    6. Izberite **Dodaj transformacijo**.
    7. V **Vrsta preoblikovanja** polje, izberite **ValueMap**.
    8. Izberite **Dodajte preslikavo vrednosti**.
    9. V levem polju vnesite **4**. V desnem polju vnesite **192350001**. 
    10. Izberite **Shrani**, nato pa zaprite pogovorno okno.

4. Izberite **Shrani kot** da shranite različico zemljevida z dvojnim pisanjem. 
5. V **Dodaj tabelo** podokno, v **Založnik** polje, izberite **Privzeti založnik**.
6. V **Različica** vnesite različico.
7. V **Opis** vnesite opombo o tej presečni različici zemljevida. 
8. Izberite **Shrani**.
9. Zaženite zemljevid.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Prenesite fakturirane mejnike na Dataverse okolje

1. V projektnih operacijah Dataverse okolje, ustvarite mejnike, ki imajo status računa **Pripravljen za fakturiranje**. Na tej točki ne selite nobenih mejnikov, ki niso bili zaračunani.

    > [!NOTE]
    > Pred selitvijo obračunskih mejnikov se prepričajte, da so finančne razsežnosti, ki so povezane s pogodbo o projektu, nastavljene po pričakovanjih. Po končani selitvi finančnih razsežnosti ni mogoče urejati.

2. Ko so vsi mejniki preseljeni, ustavite naslednje zemljevide z dvojnim pisanjem:

    - Mejniki pogodbene linije za integracijo projektnih operacij (msdyn\_ pogodbena linija razpored vrednosti)
    - Dejanske vrednosti integracije storitve Project Operations (msdyn\_actuals)
    - Predlog za račune projekta V2 (računi)

    Če želite ustaviti zemljevide, sledite tem korakom:

    1. V Financah pojdite na **Upravljanje s podatki** \> **Dvojno pisanje**, izberite zemljevid in odprite njegove podrobnosti.
    2. Izberite **Ustavi se**, in počakajte, da sistem ustavi zemljevid.

3. V projektnih operacijah Dataverse okolju, ustvarite in potrdite predračune za obračunske mejnike. 

    1. Na zemljevidu mesta pojdite na pogodbe o projektu, izberite pogodbe in nato izberite **Ustvarite račune**.
    2. Ko so računi ustvarjeni, jih odprite v **Računi** meni na zemljevidu mesta in nato izberite **Potrdi**.

    Ta korak ustvari zahtevane zapise v Dataverse okolje. Vendar to ne vpliva na finance in terjatve, ker so bili prej navedeni preslikavi dvojnega pisanja ustavljeni.

4. Ko so vsi predračuni potrjeni, vrnite vse zemljevide z dvojnim pisanjem v prvotno stanje.

    1. Posodobite različico **Mejniki pogodbene linije za integracijo projektnih operacij** (**msdyn\_ pogodbeni razpored vrednosti**) zemljevid z dvojnim pisanjem nazaj na izvirnik. 
    2. Na seznamu zemljevidov izberite zemljevid z dvojnim zapisom, izberite **Različica tabele zemljevida**, nato pa izberite izvirno različico zemljevida tabele.
    3. Izberite **Shrani**.
    4. Znova zaženite naslednje zemljevide z dvojnim pisanjem:

        - Mejniki pogodbene linije za integracijo projektnih operacij (msdyn\_ pogodbena linija razpored vrednosti)
        - Dejanske vrednosti integracije storitve Project Operations (msdyn\_actuals)
        - Predlog za račune projekta V2 (računi)

Mejniki so zdaj preseljeni in sistem je pripravljen za naslednje korake v dejavnosti preklopa.
