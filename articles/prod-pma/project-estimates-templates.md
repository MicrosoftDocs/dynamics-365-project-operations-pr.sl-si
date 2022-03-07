---
title: Sinhronizacija ocen projektov neposredno iz rešitve Project Service Automation v Finance and Operations
description: Ta tema opisuje predloge in temeljna opravila, ki se uporabljajo za sinhronizacijo ocen delovnih ur projekta in ocen stroškov projekta neposredno iz rešitve Microsoft Dynamics 365 Project Service Automation v Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 6696449d80e0915a0c878dbe75cfdf6e268b98ad9f6453bcfc4b424db68021e4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988221"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Sinhronizacija ocen projektov neposredno iz rešitve Project Service Automation v Finance and Operations

[!include[banner](../includes/banner.md)]

Ta tema opisuje predloge in temeljna opravila, ki se uporabljajo za sinhronizacijo ocen delovnih ur projekta in ocen stroškov projekta neposredno iz rešitve Dynamics 365 Project Service Automation v Dynamics 365 Finance.

> [!NOTE]
> - V različici 8.0 so na voljo integracija projektnih opravil, kategorije transakcije stroškov, ocene delovnih ur, ocene stroškov in zaklepanje funkcionalnosti.
> - Integracija dejanskih vrednosti je na voljo v različici 8.0.1 ali novejši.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Pretok podatkov za Project Service Automation v Finance

Rešitev za integracijo rešitve Project Service Automation v rešitev Finance uporablja funkcijo za integracijo podatkov za sinhronizacijo podatkov med primerki rešitev Project Service Automation in Finance. Predloge za integracijo, ki so na voljo s funkcijo za integracijo podatkov, omogočajo pretok podatkov o ocenah delovnih ur projekta in ocenah stroškov projekta iz rešitve Project Service Automation v Finance.

Naslednja slika prikazuje, kako se podatki sinhronizirajo med rešitvama Project Service Automation in Finance.

[![Podatkovni tok za integracijo rešitve Project Service Automation z rešitvijo Finance.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Ocene delovnih ur projekta

### <a name="template-and-tasks"></a>Predloga in opravila

Za dostop do razpoložljivih predlog v skrbniškem središču Microsoft Power Apps izberite **Projekti** in nato v zgornjem desnem kotu izberite **Nov projekt**, da izberete javne predloge.

Naslednja predloga in temeljna opravila se uporabljajo za sinhronizacijo ocen delovnih ur projekta iz rešitve Project Service Automation v Finance:

- **Ime predloge v Integraciji podatkov:** Ocene delovnih ur projekta (PSA v Fin in Ops)
- **Ime opravil v projektu:**

    - Razmerje transakcij
    - Ocena stroškov

### <a name="entity-set"></a>Nabor entitet

| Project Service Automation | Finance                                       |
|----------------------------|-----------------------------------------------|
| Projektna opravila              | Integracijska entiteta za ocene delovnih ur projekta |

### <a name="entity-flow"></a>Potek entitete

Ocene delovnih ur projekta se upravljajo v rešitvi Project Service Automation in sinhronizirajo v Finance kot napovedi delovnih ur projekta.

### <a name="prerequisites"></a>Zahteve

Preden lahko pride do sinhronizacije ocen delovnih ur projekta, morate sinhronizirati projekte, projektna opravila in kategorije transakcij stroškov projekta.

### <a name="power-query"></a>Power Query

V predlogi za oceno delovnih ur projekta morate uporabiti Microsoft Power Query za Excel, če želite dokončati naslednja opravila:

- Nastavite privzeti ID modela napovedi, ki se bo uporabljal, ko bo integracija ustvarila nove napovedi delovnih ur.
- S filtriranjem izločite vse zapise, povezane z viri, v opravilu, ki bo neuspešno izvedlo integracijo napovedi delovnih ur.
- S filtriranjem izločite vse prazne vrstice za kategorije transakcij. Če tega opravila ne boste mogli izvesti, lahko pride do napačnih napovedi delovnih ur.

#### <a name="set-the-default-forecast-model-id"></a>Nastavitev privzetega ID-ja modela napovedi

Če želite v predlogi posodobiti privzeti ID modela napovedi, kliknite puščico **Zemljevid**, da odprete preslikavo. Nato izberite povezavo **Napredno pošiljanje poizvedb in filtriranje**.

- Če uporabljate privzeto predlogo Ocena delovnih ur projekta (PSA v Fin in Ops), izberite možnost **Vstavljen pogoj** na seznamu **Uporabljeni koraki**. V vnosu **Funkcija** zamenjajte **Napoved O\_** z imenom ID-ja modela napovedi, ki ga je treba uporabiti pri integraciji. Privzeta predloga vsebuje ID modela napovedi iz predstavitvenih podatkov.
- Če ustvarjate novo predlogo, morate dodati ta stolpec. V rešitvi Power Query izberite **Dodaj pogojni stolpec** in vnesite ime novega stolpca, na primer **ModelID**. Vnesite pogoj za stolpec; če vrednost projektnega opravila ni »null«, potem je \<enter the forecast model ID\>; v nasprotnem primeru ju »null«.

#### <a name="filter-out-resource-specific-records"></a>S filtriranjem izločite zapise, povezane z viri

Predloga Ocena ur projekta (PSA v Fin in Ops) ima privzeti filter, ki odstrani vse zapise, povezane z viri. Če ustvarite svojo predlogo, morate dodati ta filter. Kliknite povezavo **Napredno pošiljanje poizvedb in filtriranje**, da sprožite filtriranje stolpca **msdyn\_islinetask**, da se zajamejo le zapisi **Napačno**.

#### <a name="filter-out-empty-transaction-category-rows"></a>S filtriranjem izločite prazne vrstice za kategorije transakcij

Dodati morate filter, da odstranite vse vrstice s praznimi kategorijami transakcij. To opravilo je obvezno, ne glede na to, ali uporabljate privzeto predlogo ali ustvarjate svojo predlogo. Ta filter odstrani vse vrstice s povzetki iz rešitve Project Service Automation, ki bi lahko povzročile napačne napovedi ur v rešitvi Finance. Kliknite povezavo **Napredno pošiljanje poizvedb in filtriranje**, da s filtriranjem izločite nične zapise v stolpcu **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Preslikava predlog v Integraciji podatkov

Naslednja ilustracija prikazuje primer preslikave predloge opravila v integracijo podatkov. Preslikava prikazuje informacije o polju, ki bodo sinhronizirane iz rešitve Project Service Automation v Finance.

[![Preslikava predloge opravila pri funkciji za integracijo podatkov.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Ocene stroškov projekta

### <a name="template-and-tasks"></a>Predloga in opravila

Naslednja predloga in temeljna opravila se uporabljajo za sinhronizacijo ocen stroškov projekta iz rešitve Project Service Automation v Finance:

- **Ime predloge v Integraciji podatkov:** Ocene stroškov projekta (PSA v Fin in Ops)
- **Ime opravil v projektu:**

    - Razmerje transakcij 
    - Ocena stroškov

### <a name="entity-set"></a>Nabor entitet

| Project Service Automation | Finance                                                  |
|----------------------------|----------------------------------------------------------|
| Povezave transakcij    | Integracijska entiteta za odnose projektne transakcije |
| Vrstice ocen             | Integracijska entiteta za ocene stroškov projekta         |

### <a name="entity-flow"></a>Potek entitete

Ocene stroškov projekta se upravljajo v rešitvi Project Service Automation in sinhronizirajo v Finance kot napovedi stroškov projekta.

### <a name="prerequisites"></a>Zahteve

Preden lahko pride do sinhronizacije ocen stroškov projekta, morate sinhronizirati projekte, projektna opravila in kategorije transakcij stroškov projekta.

### <a name="power-query"></a>Power Query

V predlogi za oceno stroškov projekta morate uporabiti rešitev Power Query, če želite dokončati naslednja opravila:

- S filtriranjem poiščite izključno zapise vrstic ocene stroškov.
- Nastavite privzeti ID modela napovedi, ki se bo uporabljal, ko bo integracija ustvarila nove napovedi delovnih ur.
- Spremenite vrste obračuna.
- Spremenite vrste transakcije.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>S filtriranjem poiščite izključno vrstice ocen stroškov

Predloga Ocena stroškov projekta (PSA v Fin in Ops) ima privzeti filter, ki vključuje le vrstice stroškov v integraciji. Če ustvarite svojo predlogo, morate dodati ta filter. Izberite opravilo **Razmerje transakcij** in kliknite puščico **Zemljevid**, da odprete preslikavo. Izberite povezavo **Napredno pošiljanje poizvedb in filtriranje**. Filtrirajte stolpec **msdyn\_transactiontype1**, da bi vključeval le **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Nastavitev privzetega ID-ja modela napovedi

Če želite v predlogi posodobiti privzeti ID modela napovedi, izberite opravilo **Ocene stroškov** in kliknite puščico **Zemljevid**, da odprete preslikavo. Izberite povezavo **Napredno pošiljanje poizvedb in filtriranje**.

- Če uporabljate privzeto predlogo Ocena stroškov projekta (PSA v Fin in Ops), v rešitvi Power Query najprej izberite možnost **Vstavljen pogoj** v razdelku **Uporabljeni koraki**. V vnosu **Funkcija** zamenjajte **Napoved O\_** z imenom ID-ja modela napovedi, ki ga je treba uporabiti pri integraciji. Privzeta predloga vsebuje ID modela napovedi iz predstavitvenih podatkov.
- Če ustvarjate novo predlogo, morate dodati ta stolpec. V rešitvi Power Query izberite **Dodaj pogojni stolpec** in vnesite ime novega stolpca, na primer **ModelID**. Vnesite pogoj za stolpec; če vrednost ID-ja vrstice ocene ni »null«, potem je \<enter the forecast model ID\>; v nasprotnem primeru ju »null«.

#### <a name="transform-the-billing-types"></a>Sprememba vrst obračuna

Predloga Ocena stroškov projekta (PSA v Fin in Ops) vključuje stolpec s pogoji, ki se uporablja za pretvorbo vrst obračunavanja, ki jih med integracijo prejme rešitev Project Service Automation. Če ustvarite svojo predlogo, morate dodati ta pogojni stolpec. Kliknite povezavo **Napredno pošiljanje poizvedb in filtriranje** in izberite **Dodaj pogojni stolpec**. Vnesite ime za nov stolpec, na primer **BillingType**. Nato vnesite naslednji pogoj:

Če **msdyn\_billingtype** = 192350000, potem **NonChargeable**  
Sicer velja: če **msdyn\_billingtype** = 192350001, potem **Chargeable**  
Sicer velja: če **msdyn\_billingtype** = 192350002, potem **Complimentary**  
sicer **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Sprememba vrst transakcij

Predloga Ocena stroškov projekta (PSA v Fin in Ops) vključuje stolpec s pogoji, ki se uporablja za pretvorbo vrst transakcij, ki jih med integracijo prejme rešitev Project Service Automation. Če ustvarite svojo predlogo, morate dodati ta pogojni stolpec. Kliknite povezavo **Napredno pošiljanje poizvedb in filtriranje** in izberite **Dodaj pogojni stolpec**. Vnesite ime za nov stolpec, na primer **TransactionType**. Nato vnesite naslednji pogoj:

Če **msdyn\_transactiontypecode** = 192350000, potem **Cost**  
Sicer velja: če **msdyn\_transactiontypecode** = 192350005, potem **Sales**  
Sicer velja: **null**

### <a name="template-mapping-in-data-integration"></a>Preslikava predlog v Integraciji podatkov

Spodnje slike prikazujejo primere preslikav predlog opravil v Integracijo podatkov. Preslikava prikazuje informacije o polju, ki bodo sinhronizirane iz rešitve Project Service Automation v Finance.

[![Preslikava predloge transakcij za ocene stroškov.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Preslikava predloge za ocene stroškov.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]