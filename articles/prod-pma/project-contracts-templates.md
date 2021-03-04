---
title: Sinhronizacija projektnih pogodb in projektov neposredno iz rešitve Project Service Automation v storitev Finance
description: Ta tema opisuje predlogo in temeljna opravila, ki se uporabljajo za sinhronizacijo projektnih pogodb in projektov neposredno iz rešitve Microsoft Dynamics 365 Project Service Automation v Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 1a470fd86ceccd7b6058da6972399a6d6be2a991
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764839"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Sinhronizacija projektnih pogodb in projektov neposredno iz rešitve Project Service Automation v storitev Finance 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ta tema opisuje predlogo in temeljna opravila, ki se uporabljajo za sinhronizacijo projektnih pogodb in projektov neposredno iz rešitve Dynamics 365 Project Service Automation v Dynamics 365 Finance.

> [!NOTE] 
> Če uporabljate različico Enterprise 7.3.0, morate namestiti KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Pretok podatkov za Project Service Automation v Finance

> [!NOTE]
> Preden lahko uporabite rešitev za integracijo Project Service Automation v Finance, se morate seznaniti s funkcijo za integracijo podatkov v rešitvi Dynamics 365.

Rešitev za integracijo rešitve Project Service Automation v rešitev Finance uporablja funkcijo za integracijo podatkov za sinhronizacijo podatkov med primerki rešitev Project Service Automation in Finance. Predloga za integracijo, ki je na voljo s funkcijo za integracijo podatkov, omogoča pretok podatkov o projektnih pogodbah, projektov, podrobnosti projektnih pogodb in mejnikov podrobnosti projektnih pogodb iz rešitve Project Service Automation v Finance.

Naslednja slika prikazuje, kako se podatki sinhronizirajo med rešitvama Project Service Automation in Finance.

[![Pretok podatkov za integracijo rešitve Project Service Automation v Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Predloge in opravila

Za dostop do razpoložljivih predlog v skrbniškem središču Microsoft Power Apps izberite **Projekti** in nato v zgornjem desnem kotu izberite **Nov projekt**, da izberete javne predloge.

Naslednje predloge in temeljna opravila se uporabljajo za sinhronizacijo projektnih pogodb in projektov iz rešitve Project Service Automation v Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integracija z rešitvijo Dynamics 365 Project Service Automation v2.x
- **Ime predloge v integraciji podatkov:** projekti in pogodbe (Project Service Automation v Finance)
- **Ime opravil v projektu:**

    - Projektne pogodbe (Project Service Automation v Finance)
    - Projekti (Project Service Automation v Finance)
    - Podrobnosti projektne pogodbe (Project Service Automation v Finance)
    - Mejniki podrobnosti projektne pogodbe (Project Service Automation v Finance)
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integracija z rešitvijo Dynamics 365 Project Service Automation v3.x
V rešitvi Project Service Automation je prišlo do spremembe sheme, ki vpliva na predlogo mejnika podrobnosti projektne pogodbe, zato je za integracijo rešitve Project Service Automation v3.x z Dynamics 365 potrebna različica predloge v2.

- **Ime predloge v integraciji podatkov:** projekti in pogodbe (Project Service Automation 3.x v Finance) – v2
- **Ime opravil v projektu:**

    - Projektne pogodbe (Project Service Automation v Finance)
    - Projekti (Project Service Automation v Finance)
    - Podrobnosti projektne pogodbe (Project Service Automation v Finance)
    - Mejniki podrobnosti projektne pogodbe (Project Service Automation v Finance)

Preden lahko pride do sinhronizacije projektnih pogodb in projektov, morate sinhronizirati račune.

## <a name="entity-set"></a>Nabor entitet

| Project Service Automation       | Finance                                                |
|----------------------------------|--------------------------------------------------------|
| Naročila                           | Integracijska entiteta za projektno pogodbo                |
| Projekti                         | Integracijska entiteta za projekt                         |
| Vrstice naročila                      | Integracijska entiteta za podrobnosti projektne pogodbe           |
| Mejniki podrobnosti projektne pogodbe | Integracijska entiteta za mejnike podrobnosti projektne pogodbe |

## <a name="entity-flow"></a>Potek entitete

Projektne pogodbe se upravljajo v rešitvi Project Service Automation in sinhronizirajo v Finance kot projektne pogodbe. Kot del predloge za integracijo lahko nastavite vir integracije v rešitvi Finance za projektno pogodbo.

Projekti na podlagi porabe časa in materiala ter projekti s fiksno ceno se upravljajo v rešitvi Project Service Automation in sinhronizirajo v storitev Finance kot projekti. Kot del integracije predloge lahko v storitvi Finance nastavite vir integracije za projekt. Trenutno so podprti samo projekti na podlagi porabe časa in materiala ter projekti s fiksno ceno.


Podrobnosti projektnih pogodb se upravljajo v rešitvi Project Service Automation in sinhronizirajo v Finance kot obračunska pravila za projektne pogodbe. Če se način zaračunavanja razlikuje od privzete vrste projekta, sinhronizacija posodobi vrsto projekta za podrobnosti projektne pogodbe in projektno skupino.

Mejniki podrobnosti projektnih pogodb se upravljajo v rešitvi Project Service Automation in sinhronizirajo v Finance kot mejniki obračunskih pravil za projektne pogodbe.

## <a name="project-service-automation-to-finance-integration-solution"></a>Integracija rešitve Project Service Automation v Finance

Polje **ID projektne pogodbe** je na voljo na strani **Projektne pogodbe**. To polje je naravni in edinstveni ključ za podporo integracije.

Ko se ustvari nova projektna pogodba in vrednost **ID projektne pogodbe** še ne obstaja, se ta samodejno ustvari z uporabo zaporedja števil. Vrednost vsebuje **ORD**, sledi pa ji niz zaporednih števil in pripona šestih znakov. Primer: **ORD-01022-Z4M9Q0**.

Polje **Številka projekta** je na voljo na strani **Projekti**. To polje je naravni in edinstveni ključ za podporo integracije.

Ko se ustvari nov projekt in vrednost **Številka projekta** še ne obstaja, se ta samodejno ustvari z uporabo zaporedja števil. Vrednost vsebuje **PRJ**, sledi pa ji niz zaporednih števil in pripona šestih znakov. Primer: **PRJ-01049-CCNID0**.

Ko je uporabljena rešitev za integracijo Project Service Automation v Finance, skript za nadgradnjo nastavi polje **ID projektne pogodbe** za obstoječe projektne pogodbe in polje **Številka projekta** za obstoječe projekte v Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Predpogoji in nastavitev preslikave

- Preden lahko pride do sinhronizacije projektnih pogodb in projektov, morate sinhronizirati račune.
- V nabor povezav dodajte preslikavo polj integracijskega ključa za **msdyn\_organizationalunits** v **msdyn\_name \[Ime\]**. Morda boste morali najprej dodati projekt v nabor povezav. Za več informacij glejte [Integracija podatkov v Common Data Service za aplikacije](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- V nabor povezav dodajte preslikavo polj integracijskega ključa za **msdyn\_projects** v **msdynce\_projectnumber \[Ime projekta\]**. Morda boste morali najprej dodati projekt v nabor povezav. Za več informacij glejte [Integracija podatkov v Common Data Service za aplikacije](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** za projektne pogodbe in projekte je mogoče posodobiti na drugačno vrednost ali odstraniti iz preslikave. Privzeta vrednost predloge je **Project Service Automation**.
- Preslikavo **PaymentTerms** je treba posodobiti, da odraža veljavne plačilne pogoje v rešitvi Finance. Lahko tudi odstranite preslikavo iz projektnega opravila. Na privzetem zemljevidu vrednosti so privzete vrednosti za predstavitvene podatke. Spodnja tabela prikazuje vrednosti v rešitvi Project Service Automation.

    | Vrednost | Opis   |
    |-------|---------------|
    | 1     | 30 dni        |
    | 2     | 30 dni (2 % popust na plačilo v 10 dneh) |
    | 3     | 45 dni        |
    | 4     | 60 dni        |

## <a name="power-query"></a>Power Query

Za filtriranje podatkov uporabite Microsoft Power Query za Excel, če so izpolnjeni naslednji pogoji:

- Imate prodajne naloge v rešitvi Dynamics 365 Sales.
- Imate več organizacijskih enot v rešitvi Project Service Automation in bodo te organizacijske enote preslikane na več pravnih oseb v rešitvi Finance.

Če morate uporabiti rešitev Power Query, upoštevajte naslednja navodila:

- Predloga Projekti in pogodbe (PSA v Fin in Ops) ima privzeti filter, ki vključuje samo prodajne naloge vrste **Delovna naloga (msdyn\_ordertype = 192350001)**. Ta filter pomaga zagotoviti, da se projektne pogodbe ne ustvarijo za prodajne naloge v rešitvi Finance. Če ustvarite svojo predlogo, morate dodati ta filter.
- Ustvarite filter Power Query, ki vključuje samo pogodbene organizacije, ki jih je treba sinhronizirati s pravno osebo v naboru povezav za integracijo. Primer: projektne pogodbe, ki jih imate s pogodbeno organizacijsko enoto Contoso US, je treba sinhronizirati s pravno osebo USSI, vendar je treba projektne pogodbe, ki jih imate s pogodbeno organizacijsko enoto Contoso Global, sinhronizirati s pravno osebo USMF. Če tega filtra ne dodate v preslikavo opravil, se bodo vse projektne pogodbe sinhronizirale s pravno osebo, ki je določena za nabor povezav, ne glede na pogodbeno organizacijsko enoto.

## <a name="template-mapping-in-data-integration"></a>Preslikava predlog v Integraciji podatkov

> [!NOTE] 
> Polja **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** in **AddressZipCode** niso vključena v privzeto preslikovanje za projektne pogodbe. Preslikave lahko dodate, če želite, da se ti podatki sinhronizirajo za projektne pogodbe.
>
> Polja **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** in **ProjectType** niso vključena v privzeto preslikovanje za projekte. Preslikave lahko dodate, če želite, da se ti podatki sinhronizirajo za projekte.

Spodnje slike prikazujejo primere preslikav predlog opravil v Integracijo podatkov. Preslikava prikazuje informacije o polju, ki bodo sinhronizirane iz rešitve Project Service Automation v Finance.

[![Preslikava predloge projektne pogodbe](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Preslikava predloge projekta](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Preslikava predloge podrobnosti projektne pogodbe](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Preslikava predloge mejnika podrobnosti projektne pogodbe](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Preslikava mejnikov podrobnosti projektne pogodbe v predlogi Projekti in Pogodbe (PSA 3.x v rešitvi Dynamics) – v2:

[![Preslikava mejnika podrobnosti projektne pogodbe z drugo različico predloge](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]