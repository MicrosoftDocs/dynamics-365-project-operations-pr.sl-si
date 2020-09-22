---
title: Konfiguriranje standardnih stroškov dela in drugih stroškov
description: V tej temi je pojasnjeno, kako nastavite standardne stroške dela in stroške projekta.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755887"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="e62c5-103">Konfiguriranje standardnih stroškov dela in drugih stroškov</span><span class="sxs-lookup"><span data-stu-id="e62c5-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e62c5-104">V tej temi je pojasnjeno, kako nastavite standardne stroške dela in stroške projekta.</span><span class="sxs-lookup"><span data-stu-id="e62c5-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="e62c5-105">To opravilo uporablja nabor podatkov USSI.</span><span class="sxs-lookup"><span data-stu-id="e62c5-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="e62c5-106">V podoknu za krmarjenje pojdite na **Moduli > Vodenje projektov in računovodstvo> Nastavitev> Cene > Lastna cena (ura)**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="e62c5-107">Izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-107">Select **New**.</span></span>
3. <span data-ttu-id="e62c5-108">Vnesite datum v polje **Datum začetka veljavnosti**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="e62c5-109">Vnesite številko v polje **Lastna cena**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="e62c5-110">Nastavite lahko standardno lastno ceno za kategorijo projekta ali pa lastno ceno glede na številko delavca, številko projekta, kategorijo, datum ali katerokoli kombinacijo teh.</span><span class="sxs-lookup"><span data-stu-id="e62c5-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="e62c5-111">Lastna cena, ki se uporabi, je lastna cena z najvišjo ravnjo podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="e62c5-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="e62c5-112">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-112">Select **Save**.</span></span>
6. <span data-ttu-id="e62c5-113">V podoknu za krmarjenje pojdite na **Moduli > Vodenje projektov in računovodstvo> Nastavitev> Cene > Prodajna cena (ura)**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="e62c5-114">Izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-114">Select **New**.</span></span>
8. <span data-ttu-id="e62c5-115">Vnesite datum v polje **Datum začetka veljavnosti**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="e62c5-116">Izberite možnost v polju **Veljavno za**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="e62c5-117">Vnesite številko v polje **Oblikovanje cen**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="e62c5-118">Nastavite lahko standardno prodajno ceno za urne transakcije ali za kategorijo projekta.</span><span class="sxs-lookup"><span data-stu-id="e62c5-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="e62c5-119">Prodajne cene lahko nastavite tudi glede na številko delavca, številko projekta, kategorijo, datum transakcije ali katerokoli kombinacijo teh.</span><span class="sxs-lookup"><span data-stu-id="e62c5-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="e62c5-120">Dejanska prodajna cena, ki se uporabi, ko delavec vnese transakcijo v dnevnik ur, je prodajna cena z najvišjo stopnjo podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="e62c5-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="e62c5-121">Če sta na primer nastavljeni splošna prodajna cena in prodajna cena za določenega delavca, se uporabi prodajna cena za določenega delavca.</span><span class="sxs-lookup"><span data-stu-id="e62c5-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="e62c5-122">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-122">Select **Save**.</span></span>
12. <span data-ttu-id="e62c5-123">Zaprite stran.</span><span class="sxs-lookup"><span data-stu-id="e62c5-123">Close the page.</span></span>
13. <span data-ttu-id="e62c5-124">V podoknu za krmarjenje pojdite na **Moduli > Vodenje projektov in računovodstvo> Nastavitev> Cene > Lastna cena (strošek)**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="e62c5-125">Izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-125">Select **New**.</span></span>
15. <span data-ttu-id="e62c5-126">Vnesite datum v polje **Datum začetka veljavnosti**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="e62c5-127">Vnesite številko v polje **Lastna cena**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="e62c5-128">Če želite shraniti zapis, morate izpolniti vsaj ta polja, lahko pa jih izpolnite več.</span><span class="sxs-lookup"><span data-stu-id="e62c5-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="e62c5-129">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-129">Select **Save**.</span></span>
18. <span data-ttu-id="e62c5-130">V podoknu za krmarjenje pojdite na **Moduli > Vodenje projektov in računovodstvo> Nastavitev> Cene > Prodajna cena (strošek)**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="e62c5-131">Izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-131">Select **New**.</span></span>
20. <span data-ttu-id="e62c5-132">Vnesite datum v polje **Datum začetka veljavnosti**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="e62c5-133">Izberite možnost v polju **Veljavno za**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="e62c5-134">Vnesite številko v polje **Oblikovanje cen**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="e62c5-135">Dejanska prodajna cena, ki se uporabi, ko delavec vnese transakcije v dnevnik stroškov, je prodajna cena z najvišjo stopnjo podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="e62c5-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="e62c5-136">Če sta na primer nastavljeni splošna prodajna cena in prodajna cena za določenega delavca, se uporabi prodajna cena za določenega delavca.</span><span class="sxs-lookup"><span data-stu-id="e62c5-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="e62c5-137">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="e62c5-137">Select **Save**.</span></span>

