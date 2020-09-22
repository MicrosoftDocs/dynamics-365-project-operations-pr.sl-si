---
title: Sinhronizacija ocen projektov neposredno iz rešitve Project Service Automation v Finance and Operations
description: Ta tema opisuje predloge in temeljna opravila, ki se uporabljajo za sinhronizacijo ocen delovnih ur projekta in ocen stroškov projekta neposredno iz rešitve Microsoft Dynamics 365 Project Service Automation v Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755784"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="361b0-103">Sinhronizacija ocen projektov neposredno iz rešitve Project Service Automation v Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="361b0-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="361b0-104">Ta tema opisuje predloge in temeljna opravila, ki se uporabljajo za sinhronizacijo ocen delovnih ur projekta in ocen stroškov projekta neposredno iz rešitve Dynamics 365 Project Service Automation v Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="361b0-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="361b0-105">V različici 8.0 so na voljo integracija projektnih opravil, kategorije transakcije stroškov, ocene delovnih ur, ocene stroškov in zaklepanje funkcionalnosti.</span><span class="sxs-lookup"><span data-stu-id="361b0-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="361b0-106">Integracija dejanskih vrednosti je na voljo v različici 8.0.1 ali novejši.</span><span class="sxs-lookup"><span data-stu-id="361b0-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="361b0-107">Pretok podatkov za Project Service Automation v Finance</span><span class="sxs-lookup"><span data-stu-id="361b0-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="361b0-108">Rešitev za integracijo rešitve Project Service Automation v rešitev Finance uporablja funkcijo za integracijo podatkov za sinhronizacijo podatkov med primerki rešitev Project Service Automation in Finance.</span><span class="sxs-lookup"><span data-stu-id="361b0-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="361b0-109">Predloge za integracijo, ki so na voljo s funkcijo za integracijo podatkov, omogočajo pretok podatkov o ocenah delovnih ur projekta in ocenah stroškov projekta iz rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="361b0-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="361b0-110">Naslednja slika prikazuje, kako se podatki sinhronizirajo med rešitvama Project Service Automation in Finance.</span><span class="sxs-lookup"><span data-stu-id="361b0-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="361b0-111">[![Pretok podatkov za integracijo rešitve Project Service Automation s Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="361b0-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="361b0-112">Ocene delovnih ur projekta</span><span class="sxs-lookup"><span data-stu-id="361b0-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="361b0-113">Predloga in opravila</span><span class="sxs-lookup"><span data-stu-id="361b0-113">Template and tasks</span></span>

<span data-ttu-id="361b0-114">Za dostop do razpoložljivih predlog v skrbniškem središču Microsoft Power Apps izberite **Projekti** in nato v zgornjem desnem kotu izberite **Nov projekt**, da izberete javne predloge.</span><span class="sxs-lookup"><span data-stu-id="361b0-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="361b0-115">Naslednja predloga in temeljna opravila se uporabljajo za sinhronizacijo ocen delovnih ur projekta iz rešitve Project Service Automation v Finance:</span><span class="sxs-lookup"><span data-stu-id="361b0-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="361b0-116">**Ime predloge v Integraciji podatkov:** Ocene delovnih ur projekta (PSA v Fin in Ops)</span><span class="sxs-lookup"><span data-stu-id="361b0-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="361b0-117">**Ime opravil v projektu:**</span><span class="sxs-lookup"><span data-stu-id="361b0-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="361b0-118">Razmerje transakcij</span><span class="sxs-lookup"><span data-stu-id="361b0-118">Transaction relationships</span></span>
    - <span data-ttu-id="361b0-119">Ocena stroškov</span><span class="sxs-lookup"><span data-stu-id="361b0-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="361b0-120">Nabor entitet</span><span class="sxs-lookup"><span data-stu-id="361b0-120">Entity set</span></span>

| <span data-ttu-id="361b0-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="361b0-121">Project Service Automation</span></span> | <span data-ttu-id="361b0-122">Finance</span><span class="sxs-lookup"><span data-stu-id="361b0-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="361b0-123">Projektna opravila</span><span class="sxs-lookup"><span data-stu-id="361b0-123">Project tasks</span></span>              | <span data-ttu-id="361b0-124">Integracijska entiteta za ocene delovnih ur projekta</span><span class="sxs-lookup"><span data-stu-id="361b0-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="361b0-125">Potek entitete</span><span class="sxs-lookup"><span data-stu-id="361b0-125">Entity flow</span></span>

<span data-ttu-id="361b0-126">Ocene delovnih ur projekta se upravljajo v rešitvi Project Service Automation in sinhronizirajo v Finance kot napovedi delovnih ur projekta.</span><span class="sxs-lookup"><span data-stu-id="361b0-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="361b0-127">Zahteve</span><span class="sxs-lookup"><span data-stu-id="361b0-127">Prerequisites</span></span>

<span data-ttu-id="361b0-128">Preden lahko pride do sinhronizacije ocen delovnih ur projekta, morate sinhronizirati projekte, projektna opravila in kategorije transakcij stroškov projekta.</span><span class="sxs-lookup"><span data-stu-id="361b0-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="361b0-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="361b0-129">Power Query</span></span>

<span data-ttu-id="361b0-130">V predlogi za oceno delovnih ur projekta morate uporabiti Microsoft Power Query za Excel, če želite dokončati naslednja opravila:</span><span class="sxs-lookup"><span data-stu-id="361b0-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="361b0-131">Nastavite privzeti ID modela napovedi, ki se bo uporabljal, ko bo integracija ustvarila nove napovedi delovnih ur.</span><span class="sxs-lookup"><span data-stu-id="361b0-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="361b0-132">S filtriranjem izločite vse zapise, povezane z viri, v opravilu, ki bo neuspešno izvedlo integracijo napovedi delovnih ur.</span><span class="sxs-lookup"><span data-stu-id="361b0-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="361b0-133">S filtriranjem izločite vse prazne vrstice za kategorije transakcij.</span><span class="sxs-lookup"><span data-stu-id="361b0-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="361b0-134">Če tega opravila ne boste mogli izvesti, lahko pride do napačnih napovedi delovnih ur.</span><span class="sxs-lookup"><span data-stu-id="361b0-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="361b0-135">Nastavitev privzetega ID-ja modela napovedi</span><span class="sxs-lookup"><span data-stu-id="361b0-135">Set the default forecast model ID</span></span>

<span data-ttu-id="361b0-136">Če želite v predlogi posodobiti privzeti ID modela napovedi, kliknite puščico **Zemljevid**, da odprete preslikavo.</span><span class="sxs-lookup"><span data-stu-id="361b0-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="361b0-137">Nato izberite povezavo **Napredno pošiljanje poizvedb in filtriranje**.</span><span class="sxs-lookup"><span data-stu-id="361b0-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="361b0-138">Če uporabljate privzeto predlogo Ocena delovnih ur projekta (PSA v Fin in Ops), izberite možnost **Vstavljen pogoj** na seznamu **Uporabljeni koraki**.</span><span class="sxs-lookup"><span data-stu-id="361b0-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="361b0-139">V vnosu **Funkcija** zamenjajte **Napoved O\_** z imenom ID-ja modela napovedi, ki ga je treba uporabiti pri integraciji.</span><span class="sxs-lookup"><span data-stu-id="361b0-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="361b0-140">Privzeta predloga vsebuje ID modela napovedi iz predstavitvenih podatkov.</span><span class="sxs-lookup"><span data-stu-id="361b0-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="361b0-141">Če ustvarjate novo predlogo, morate dodati ta stolpec.</span><span class="sxs-lookup"><span data-stu-id="361b0-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="361b0-142">V rešitvi Power Query izberite **Dodaj pogojni stolpec** in vnesite ime novega stolpca, na primer **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="361b0-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="361b0-143">Vnesite pogoj za stolpec, kjer velja: če projektno opravilo nima prazne vrednosti (»null«), potem \<vnesite ID modela napovedi\>; sicer »null«.</span><span class="sxs-lookup"><span data-stu-id="361b0-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="361b0-144">S filtriranjem izločite zapise, povezane z viri</span><span class="sxs-lookup"><span data-stu-id="361b0-144">Filter out resource-specific records</span></span>

<span data-ttu-id="361b0-145">Predloga Ocena ur projekta (PSA v Fin in Ops) ima privzeti filter, ki odstrani vse zapise, povezane z viri.</span><span class="sxs-lookup"><span data-stu-id="361b0-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="361b0-146">Če ustvarite svojo predlogo, morate dodati ta filter.</span><span class="sxs-lookup"><span data-stu-id="361b0-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="361b0-147">Kliknite povezavo **Napredno pošiljanje poizvedb in filtriranje**, da sprožite filtriranje stolpca **msdyn\_islinetask**, da se zajamejo le zapisi **Napačno**.</span><span class="sxs-lookup"><span data-stu-id="361b0-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="361b0-148">S filtriranjem izločite prazne vrstice za kategorije transakcij</span><span class="sxs-lookup"><span data-stu-id="361b0-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="361b0-149">Dodati morate filter, da odstranite vse vrstice s praznimi kategorijami transakcij.</span><span class="sxs-lookup"><span data-stu-id="361b0-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="361b0-150">To opravilo je obvezno, ne glede na to, ali uporabljate privzeto predlogo ali ustvarjate svojo predlogo.</span><span class="sxs-lookup"><span data-stu-id="361b0-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="361b0-151">Ta filter odstrani vse vrstice s povzetki iz rešitve Project Service Automation, ki bi lahko povzročile napačne napovedi ur v rešitvi Finance.</span><span class="sxs-lookup"><span data-stu-id="361b0-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="361b0-152">Kliknite povezavo **Napredno pošiljanje poizvedb in filtriranje**, da s filtriranjem izločite nične zapise v stolpcu **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="361b0-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="361b0-153">Preslikava predlog v Integraciji podatkov</span><span class="sxs-lookup"><span data-stu-id="361b0-153">Template mapping in Data integration</span></span>

<span data-ttu-id="361b0-154">Naslednja ilustracija prikazuje primer preslikave predloge opravila v integracijo podatkov.</span><span class="sxs-lookup"><span data-stu-id="361b0-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="361b0-155">Preslikava prikazuje informacije o polju, ki bodo sinhronizirane iz rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="361b0-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="361b0-156">[![Preslikava predloge](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="361b0-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="361b0-157">Ocene stroškov projekta</span><span class="sxs-lookup"><span data-stu-id="361b0-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="361b0-158">Predloga in opravila</span><span class="sxs-lookup"><span data-stu-id="361b0-158">Template and tasks</span></span>

<span data-ttu-id="361b0-159">Naslednja predloga in temeljna opravila se uporabljajo za sinhronizacijo ocen stroškov projekta iz rešitve Project Service Automation v Finance:</span><span class="sxs-lookup"><span data-stu-id="361b0-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="361b0-160">**Ime predloge v Integraciji podatkov:** Ocene stroškov projekta (PSA v Fin in Ops)</span><span class="sxs-lookup"><span data-stu-id="361b0-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="361b0-161">**Ime opravil v projektu:**</span><span class="sxs-lookup"><span data-stu-id="361b0-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="361b0-162">Razmerje transakcij</span><span class="sxs-lookup"><span data-stu-id="361b0-162">Transaction relationships</span></span> 
    - <span data-ttu-id="361b0-163">Ocena stroškov</span><span class="sxs-lookup"><span data-stu-id="361b0-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="361b0-164">Nabor entitet</span><span class="sxs-lookup"><span data-stu-id="361b0-164">Entity set</span></span>

| <span data-ttu-id="361b0-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="361b0-165">Project Service Automation</span></span> | <span data-ttu-id="361b0-166">Finance</span><span class="sxs-lookup"><span data-stu-id="361b0-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="361b0-167">Povezave transakcij</span><span class="sxs-lookup"><span data-stu-id="361b0-167">Transaction Connections</span></span>    | <span data-ttu-id="361b0-168">Integracijska entiteta za odnose projektne transakcije</span><span class="sxs-lookup"><span data-stu-id="361b0-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="361b0-169">Vrstice ocen</span><span class="sxs-lookup"><span data-stu-id="361b0-169">Estimate Lines</span></span>             | <span data-ttu-id="361b0-170">Integracijska entiteta za ocene stroškov projekta</span><span class="sxs-lookup"><span data-stu-id="361b0-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="361b0-171">Potek entitete</span><span class="sxs-lookup"><span data-stu-id="361b0-171">Entity flow</span></span>

<span data-ttu-id="361b0-172">Ocene stroškov projekta se upravljajo v rešitvi Project Service Automation in sinhronizirajo v Finance kot napovedi stroškov projekta.</span><span class="sxs-lookup"><span data-stu-id="361b0-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="361b0-173">Zahteve</span><span class="sxs-lookup"><span data-stu-id="361b0-173">Prerequisites</span></span>

<span data-ttu-id="361b0-174">Preden lahko pride do sinhronizacije ocen stroškov projekta, morate sinhronizirati projekte, projektna opravila in kategorije transakcij stroškov projekta.</span><span class="sxs-lookup"><span data-stu-id="361b0-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="361b0-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="361b0-175">Power Query</span></span>

<span data-ttu-id="361b0-176">V predlogi za oceno stroškov projekta morate uporabiti rešitev Power Query, če želite dokončati naslednja opravila:</span><span class="sxs-lookup"><span data-stu-id="361b0-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="361b0-177">S filtriranjem poiščite izključno zapise vrstic ocene stroškov.</span><span class="sxs-lookup"><span data-stu-id="361b0-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="361b0-178">Nastavite privzeti ID modela napovedi, ki se bo uporabljal, ko bo integracija ustvarila nove napovedi delovnih ur.</span><span class="sxs-lookup"><span data-stu-id="361b0-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="361b0-179">Spremenite vrste obračuna.</span><span class="sxs-lookup"><span data-stu-id="361b0-179">Transform the billing types.</span></span>
- <span data-ttu-id="361b0-180">Spremenite vrste transakcije.</span><span class="sxs-lookup"><span data-stu-id="361b0-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="361b0-181">S filtriranjem poiščite izključno vrstice ocen stroškov</span><span class="sxs-lookup"><span data-stu-id="361b0-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="361b0-182">Predloga Ocena stroškov projekta (PSA v Fin in Ops) ima privzeti filter, ki vključuje le vrstice stroškov v integraciji.</span><span class="sxs-lookup"><span data-stu-id="361b0-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="361b0-183">Če ustvarite svojo predlogo, morate dodati ta filter.</span><span class="sxs-lookup"><span data-stu-id="361b0-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="361b0-184">Izberite opravilo **Razmerje transakcij** in kliknite puščico **Zemljevid**, da odprete preslikavo.</span><span class="sxs-lookup"><span data-stu-id="361b0-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="361b0-185">Izberite povezavo **Napredno pošiljanje poizvedb in filtriranje**.</span><span class="sxs-lookup"><span data-stu-id="361b0-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="361b0-186">Filtrirajte stolpec **msdyn\_transactiontype1**, da bi vključeval le **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="361b0-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="361b0-187">Nastavitev privzetega ID-ja modela napovedi</span><span class="sxs-lookup"><span data-stu-id="361b0-187">Set the default forecast model ID</span></span>

<span data-ttu-id="361b0-188">Če želite v predlogi posodobiti privzeti ID modela napovedi, izberite opravilo **Ocene stroškov** in kliknite puščico **Zemljevid**, da odprete preslikavo.</span><span class="sxs-lookup"><span data-stu-id="361b0-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="361b0-189">Izberite povezavo **Napredno pošiljanje poizvedb in filtriranje**.</span><span class="sxs-lookup"><span data-stu-id="361b0-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="361b0-190">Če uporabljate privzeto predlogo Ocena stroškov projekta (PSA v Fin in Ops), v rešitvi Power Query najprej izberite možnost **Vstavljen pogoj** v razdelku **Uporabljeni koraki**.</span><span class="sxs-lookup"><span data-stu-id="361b0-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="361b0-191">V vnosu **Funkcija** zamenjajte **Napoved O\_** z imenom ID-ja modela napovedi, ki ga je treba uporabiti pri integraciji.</span><span class="sxs-lookup"><span data-stu-id="361b0-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="361b0-192">Privzeta predloga vsebuje ID modela napovedi iz predstavitvenih podatkov.</span><span class="sxs-lookup"><span data-stu-id="361b0-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="361b0-193">Če ustvarjate novo predlogo, morate dodati ta stolpec.</span><span class="sxs-lookup"><span data-stu-id="361b0-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="361b0-194">V rešitvi Power Query izberite **Dodaj pogojni stolpec** in vnesite ime novega stolpca, na primer **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="361b0-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="361b0-195">Vnesite pogoj za stolpec, kjer velja: če ID vrstice ocene nima prazne vrednosti (»null«), potem \<vnesite ID modela napovedi\>; sicer »null«.</span><span class="sxs-lookup"><span data-stu-id="361b0-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="361b0-196">Sprememba vrst obračuna</span><span class="sxs-lookup"><span data-stu-id="361b0-196">Transform the billing types</span></span>

<span data-ttu-id="361b0-197">Predloga Ocena stroškov projekta (PSA v Fin in Ops) vključuje stolpec s pogoji, ki se uporablja za pretvorbo vrst obračunavanja, ki jih med integracijo prejme rešitev Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="361b0-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="361b0-198">Če ustvarite svojo predlogo, morate dodati ta pogojni stolpec.</span><span class="sxs-lookup"><span data-stu-id="361b0-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="361b0-199">Kliknite povezavo **Napredno pošiljanje poizvedb in filtriranje** in izberite **Dodaj pogojni stolpec**.</span><span class="sxs-lookup"><span data-stu-id="361b0-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="361b0-200">Vnesite ime za nov stolpec, na primer **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="361b0-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="361b0-201">Nato vnesite naslednji pogoj:</span><span class="sxs-lookup"><span data-stu-id="361b0-201">Then enter the following condition:</span></span>

<span data-ttu-id="361b0-202">Če **msdyn\_billingtype** = 192350000, potem **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="361b0-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="361b0-203">Sicer velja: če **msdyn\_billingtype** = 192350001, potem **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="361b0-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="361b0-204">Sicer velja: če **msdyn\_billingtype** = 192350002, potem **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="361b0-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="361b0-205">sicer **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="361b0-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="361b0-206">Sprememba vrst transakcij</span><span class="sxs-lookup"><span data-stu-id="361b0-206">Transform the transaction types</span></span>

<span data-ttu-id="361b0-207">Predloga Ocena stroškov projekta (PSA v Fin in Ops) vključuje stolpec s pogoji, ki se uporablja za pretvorbo vrst transakcij, ki jih med integracijo prejme rešitev Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="361b0-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="361b0-208">Če ustvarite svojo predlogo, morate dodati ta pogojni stolpec.</span><span class="sxs-lookup"><span data-stu-id="361b0-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="361b0-209">Kliknite povezavo **Napredno pošiljanje poizvedb in filtriranje** in izberite **Dodaj pogojni stolpec**.</span><span class="sxs-lookup"><span data-stu-id="361b0-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="361b0-210">Vnesite ime za nov stolpec, na primer **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="361b0-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="361b0-211">Nato vnesite naslednji pogoj:</span><span class="sxs-lookup"><span data-stu-id="361b0-211">Then enter the following condition:</span></span>

<span data-ttu-id="361b0-212">Če **msdyn\_transactiontypecode** = 192350000, potem **Cost**</span><span class="sxs-lookup"><span data-stu-id="361b0-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="361b0-213">Sicer velja: če **msdyn\_transactiontypecode** = 192350005, potem **Sales**</span><span class="sxs-lookup"><span data-stu-id="361b0-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="361b0-214">Sicer velja: **null**</span><span class="sxs-lookup"><span data-stu-id="361b0-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="361b0-215">Preslikava predlog v Integraciji podatkov</span><span class="sxs-lookup"><span data-stu-id="361b0-215">Template mapping in Data integration</span></span>

<span data-ttu-id="361b0-216">Spodnje slike prikazujejo primere preslikav predlog opravil v Integracijo podatkov.</span><span class="sxs-lookup"><span data-stu-id="361b0-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="361b0-217">Preslikava prikazuje informacije o polju, ki bodo sinhronizirane iz rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="361b0-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="361b0-218">[![Preslikava predloge](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="361b0-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="361b0-219">[![Preslikava predloge](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="361b0-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
