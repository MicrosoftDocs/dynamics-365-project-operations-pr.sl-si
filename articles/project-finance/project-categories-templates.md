---
title: Sinhronizacija kategorij stroškov projekta med Finance and Operations in Project Service Automation
description: Ta tema opisuje predloge in temeljna opravila, ki se uporabljajo za sinhronizacijo kategorij stroškov projekta med rešitvama Microsoft Dynamics 365 Finance in Dynamics 365 Project Service Automation.
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
ms.assetid: 7dd914dc-1913-45eb-8a67-e897b00089fa
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 757fe1dbc804b986fc3334ebae7254a3f0491f59
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755824"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="ff066-103">Sinhronizacija kategorij stroškov projekta med Finance and Operations in Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ff066-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ff066-104">Ta tema opisuje predloge in temeljna opravila, ki se uporabljajo za sinhronizacijo kategorij stroškov projekta med rešitvama Dynamics 365 Finance in Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ff066-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="ff066-105">V različici 8.0 so na voljo integracija projektnih opravil, kategorije transakcije stroškov, ocene delovnih ur, ocene stroškov in zaklepanje funkcionalnosti.</span><span class="sxs-lookup"><span data-stu-id="ff066-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="ff066-106">Integracija dejanskih vrednosti je na voljo v različici 8.0.1 ali novejši.</span><span class="sxs-lookup"><span data-stu-id="ff066-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="ff066-107">Če uporabljate različico Enterprise 7.3.0, boste po namestitvi KB 4132657 in KB 4132660 lahko predloge uporabili za integracijo projektnih opravil, kategorij stroškov transakcij, ocen delovnih ur, ocen stroškov in dejanskih vrednosti ter konfiguriranje zaklepanja funkcionalnosti.</span><span class="sxs-lookup"><span data-stu-id="ff066-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="ff066-108">Če morate ponastaviti računovodsko porazdeljevanje, priporočamo, da namestite tudi KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="ff066-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="ff066-109">Pretok podatkov za rešitvi Project Service Automation in Finance</span><span class="sxs-lookup"><span data-stu-id="ff066-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="ff066-110">Rešitev za integracijo rešitve Project Service Automation in Finance uporablja funkcijo za integracijo podatkov za sinhronizacijo podatkov med primerki rešitev Project Service Automation in Finance.</span><span class="sxs-lookup"><span data-stu-id="ff066-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="ff066-111">Predloge za integracijo, ki so na voljo s funkcijo za integracijo podatkov, omogočajo pretok podatkov o kategorijah transakcij stroškov projekta med rešitvama Finance in Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ff066-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="ff066-112">Če so kategorije stroškov projekta upravljane v rešitvi Finance, gre potek integracije od rešitve Finance do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ff066-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="ff066-113">ID-ji integracije kategorij stroškov projekta se nato posodobijo s sinhronizacijo od rešitve Project Service Automation do rešitve Finance.</span><span class="sxs-lookup"><span data-stu-id="ff066-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ff066-114">Če so kategorije stroškov projekta upravljane v rešitvi Project Service Automation, gre potek integracije od rešitve Project Service Automation do rešitve Finance.</span><span class="sxs-lookup"><span data-stu-id="ff066-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="ff066-115">Kategorije projektov morajo biti konfigurirane v rešitvi Finance, preden se izvede sinhronizacija s programom Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ff066-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="ff066-116">Nato sinhronizirajte še enkrat iz rešitve Finance v Project Service Automation in nato še iz Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="ff066-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="ff066-117">Na ta način boste zagotovili, da bodo kategorije povezane in ne bodo obstajali dvojniki.</span><span class="sxs-lookup"><span data-stu-id="ff066-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="ff066-118">Kategorije stroškov projekta se običajno upravljajo v rešitvi Finance.</span><span class="sxs-lookup"><span data-stu-id="ff066-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="ff066-119">Če pa niso ali če so kategorije stroškov že bile ustvarjene v rešitvi Project Service Automation, morate najprej izvesti sinhronizacijo s predlogo Kategorije transakcij stroškov projekta (PSA v Fin in Ops).</span><span class="sxs-lookup"><span data-stu-id="ff066-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="ff066-120">Nato sinhronizirajte s predlogo Kategorije transakcij stroškov projekta (Fin in Ops v PSA).</span><span class="sxs-lookup"><span data-stu-id="ff066-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="ff066-121">Nato morate še enkrat zagnati sinhronizacijo iz rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="ff066-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="ff066-122">Če sinhronizirate najprej iz rešitve Project Service Automation, morajo biti pred začetkom sinhronizacije v programu Finance izpolnjene naslednje zahteve:</span><span class="sxs-lookup"><span data-stu-id="ff066-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="ff066-123">Kategorija v skupni rabi, ki se ujema s kategorijo projekta, ki je nastavljena v rešitvi Project Service Automation, mora obstajati in biti omogočena tako za **Projekt** kot za **Stroški**.</span><span class="sxs-lookup"><span data-stu-id="ff066-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="ff066-124">Za vsako pravno osebo v rešitvi Finance, za katero je treba izvesti integracijo, morajo obstajati naslednje kategorije projektov:</span><span class="sxs-lookup"><span data-stu-id="ff066-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="ff066-125">**Kategorija projekta** obstaja.</span><span class="sxs-lookup"><span data-stu-id="ff066-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="ff066-126">**Uporaba v stroških** je omogočena.</span><span class="sxs-lookup"><span data-stu-id="ff066-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="ff066-127">**Dejavnost v dnevniku** je omogočena.</span><span class="sxs-lookup"><span data-stu-id="ff066-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="ff066-128">**Vrsta transakcije** je nastavljena na **Stroški**.</span><span class="sxs-lookup"><span data-stu-id="ff066-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="ff066-129">Naslednja slika prikazuje, kako se podatki sinhronizirajo med rešitvama Project Service Automation in Finance.</span><span class="sxs-lookup"><span data-stu-id="ff066-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="ff066-130">[![Pretok podatkov za integracijo rešitve Project Service Automation v Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="ff066-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="ff066-131">Sinhronizacija kategorije stroškov projekta iz rešitve Finance v Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ff066-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="ff066-132">Predloga in opravilo</span><span class="sxs-lookup"><span data-stu-id="ff066-132">Template and task</span></span>

<span data-ttu-id="ff066-133">Za dostop do predloge v skrbniškem središču Microsoft Power Apps izberite **Projekti** in nato v zgornjem desnem kotu izberite **Nov projekt**, da izberete javne predloge.</span><span class="sxs-lookup"><span data-stu-id="ff066-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="ff066-134">Spodnja predloga in temeljno opravilo se uporabljata za sinhronizacijo kategorij stroškov projekta iz rešitve Finance v Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="ff066-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="ff066-135">**Ime predloge v Integraciji podatkov:** Kategorije transakcij stroškov projekta (Fin in Ops v PSA)</span><span class="sxs-lookup"><span data-stu-id="ff066-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="ff066-136">**Ime opravila v projektu:** Sinhronizacija kategorij s PSA</span><span class="sxs-lookup"><span data-stu-id="ff066-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="ff066-137">Nabor entitet</span><span class="sxs-lookup"><span data-stu-id="ff066-137">Entity set</span></span>

| <span data-ttu-id="ff066-138">Finance</span><span class="sxs-lookup"><span data-stu-id="ff066-138">Finance</span></span>                           | <span data-ttu-id="ff066-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ff066-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="ff066-140">Integracijska entiteta za kategorije</span><span class="sxs-lookup"><span data-stu-id="ff066-140">Integration entity for categories</span></span> | <span data-ttu-id="ff066-141">Kategorije transakcij</span><span class="sxs-lookup"><span data-stu-id="ff066-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="ff066-142">Potek entitete</span><span class="sxs-lookup"><span data-stu-id="ff066-142">Entity flow</span></span>

<span data-ttu-id="ff066-143">Kategorije stroškov projekta se upravljajo v rešitvi Finance in sinhronizirajo v rešitev Project Service Automation kot kategorije transakcij.</span><span class="sxs-lookup"><span data-stu-id="ff066-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="ff066-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="ff066-144">Power Query</span></span>

<span data-ttu-id="ff066-145">Ko izvajate sinhronizacijo z rešitvijo Project Service Automation, morate uporabiti Microsoft Power Query za Excel, da nastavite vrsto obračunavanja za kategorijo transakcij.</span><span class="sxs-lookup"><span data-stu-id="ff066-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="ff066-146">Predloga kategorij transakcij stroškov projekta (Fin in Ops v PSA) vsebuje privzeti stolpec in preslikavo.</span><span class="sxs-lookup"><span data-stu-id="ff066-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="ff066-147">Če ustvarite svojo predlogo, morate dodati pogojni stolpec v Power Query.</span><span class="sxs-lookup"><span data-stu-id="ff066-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="ff066-148">Upoštevajte ta navodila.</span><span class="sxs-lookup"><span data-stu-id="ff066-148">Follow these steps.</span></span>

1. <span data-ttu-id="ff066-149">Kliknite puščico, da odprete preslikavo opravila kategorij stroškov projekta v predlogi Kategorije transakcij stroškov projekta (Fin in Ops v PSA).</span><span class="sxs-lookup"><span data-stu-id="ff066-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="ff066-150">Kliknite povezavo **Napredno pošiljanje poizvedb in filtriranje**, da odprete Power Query.</span><span class="sxs-lookup"><span data-stu-id="ff066-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="ff066-151">Izberite **Dodaj pogojni stolpec**.</span><span class="sxs-lookup"><span data-stu-id="ff066-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="ff066-152">Vnesite ime za nov stolpec, na primer **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="ff066-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="ff066-153">Vnesite naslednji pogoj: **če CATEGORYID ni enak nič, potem je 19235001, sicer pa nič**.</span><span class="sxs-lookup"><span data-stu-id="ff066-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="ff066-154">Kliknite **V redu** za stolpec.</span><span class="sxs-lookup"><span data-stu-id="ff066-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="ff066-155">Novi stolpec preslikajte na stran za preslikavo.</span><span class="sxs-lookup"><span data-stu-id="ff066-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="ff066-156">Naslednja ilustracija prikazuje primer preslikave predloge opravila v integracijo podatkov.</span><span class="sxs-lookup"><span data-stu-id="ff066-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="ff066-157">Preslikava prikazuje informacije o polju, ki bodo sinhronizirane iz rešitve Finance v Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ff066-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="ff066-158">[![Preslikava predloge](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ff066-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="ff066-159">Sinhronizacija kategorije stroškov projekta iz rešitve Project Service Automation v Finance</span><span class="sxs-lookup"><span data-stu-id="ff066-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="ff066-160">Predloga in opravilo</span><span class="sxs-lookup"><span data-stu-id="ff066-160">Template and task</span></span>

<span data-ttu-id="ff066-161">Spodnja predloga in temeljno opravilo se uporabljata za sinhronizacijo kategorij stroškov projekta iz rešitve Project Service Automation v Finance:</span><span class="sxs-lookup"><span data-stu-id="ff066-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="ff066-162">**Ime predloge v Integraciji podatkov:** Kategorije transakcij stroškov projekta (PSA v Fin in Ops)</span><span class="sxs-lookup"><span data-stu-id="ff066-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="ff066-163">**Ime opravila v projektu:** Sinhronizacija kategorij s Fin Ops</span><span class="sxs-lookup"><span data-stu-id="ff066-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="ff066-164">Nabor entitet</span><span class="sxs-lookup"><span data-stu-id="ff066-164">Entity set</span></span>

| <span data-ttu-id="ff066-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ff066-165">Project Service Automation</span></span> | <span data-ttu-id="ff066-166">Finance</span><span class="sxs-lookup"><span data-stu-id="ff066-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="ff066-167">Kategorije transakcij</span><span class="sxs-lookup"><span data-stu-id="ff066-167">Transaction categories</span></span>     | <span data-ttu-id="ff066-168">Integracijska entiteta za kategorije</span><span class="sxs-lookup"><span data-stu-id="ff066-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="ff066-169">Potek entitete</span><span class="sxs-lookup"><span data-stu-id="ff066-169">Entity flow</span></span>

<span data-ttu-id="ff066-170">Kategorije stroškov projekta se upravljajo v rešitvi Finance in sinhronizirajo v rešitev Project Service Automation kot kategorije transakcij.</span><span class="sxs-lookup"><span data-stu-id="ff066-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="ff066-171">S povratno sinhronizacijo v rešitev Finance se posodobi kategorija projekta v rešitvi Finance z ID-jem integracije iz rešitve Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ff066-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ff066-172">Preslikava predlog v Integraciji podatkov</span><span class="sxs-lookup"><span data-stu-id="ff066-172">Template mapping in Data integration</span></span>

<span data-ttu-id="ff066-173">Naslednja ilustracija prikazuje primer preslikave predloge opravila v integracijo podatkov.</span><span class="sxs-lookup"><span data-stu-id="ff066-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="ff066-174">Preslikava prikazuje informacije o polju, ki bodo sinhronizirane iz rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="ff066-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ff066-175">[![Preslikava predloge](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ff066-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
