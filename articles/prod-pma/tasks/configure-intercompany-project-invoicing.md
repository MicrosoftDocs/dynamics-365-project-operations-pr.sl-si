---
title: Konfiguriranje zaračunavanja projektov med podjetji
description: V tej temi je prikazano, kako nastavite zaračunavanje projektov med dvema podjetjema v vaši organizaciji.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084815"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="b5e67-103">Konfiguriranje zaračunavanja projektov med podjetji</span><span class="sxs-lookup"><span data-stu-id="b5e67-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5e67-104">V tej temi je prikazano, kako nastavite zaračunavanje projektov med dvema podjetjema v vaši organizaciji.</span><span class="sxs-lookup"><span data-stu-id="b5e67-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="b5e67-105">To opravilo uporablja nabor podatkov USSI.</span><span class="sxs-lookup"><span data-stu-id="b5e67-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="b5e67-106">V podoknu za krmarjenje pojdite na **Moduli > Obveznosti > Dobavitelji > Vsi dobavitelji**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="b5e67-107">Na seznamu **Vsi dobavitelji** poiščite in izberite želeni zapis.</span><span class="sxs-lookup"><span data-stu-id="b5e67-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="b5e67-108">V podoknu za dejanja izberite **Splošno**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="b5e67-109">Izberite **Med podjetji**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="b5e67-110">Nastavite **Aktivno** na **Da** , da omogočite medpodjetniško trgovanje.</span><span class="sxs-lookup"><span data-stu-id="b5e67-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="b5e67-111">Vnesite ali izberite vrednost v polju **Podjetje stranke**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="b5e67-112">Vnesite ali izberite vrednost v polju **Moj račun**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="b5e67-113">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-113">Select **Save**.</span></span>
9. <span data-ttu-id="b5e67-114">Zaprite strani, da se vrnete na domačo stran.</span><span class="sxs-lookup"><span data-stu-id="b5e67-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="b5e67-115">V podoknu za krmarjenje pojdite na **Moduli > Vodenje projektov in računovodstvo> Nastavitev> Vodenje projektov in računovodski parametri**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="b5e67-116">Izberite zavihek **Med podjetji**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="b5e67-117">Premaknite drsnik na **Da** , da omogočite razporejanje virov in časovnice med podjetji.</span><span class="sxs-lookup"><span data-stu-id="b5e67-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="b5e67-118">Na seznamu označite izbrano vrstico.</span><span class="sxs-lookup"><span data-stu-id="b5e67-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="b5e67-119">Izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-119">Select **New**.</span></span>
15. <span data-ttu-id="b5e67-120">Vnesite ali izberite vrednost v polju **Pravna oseba, ki si izposoja**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="b5e67-121">Potrdite potrditveno polje **Obračunaj prihodke**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="b5e67-122">Vnesite ali izberite vrednost v polju **Privzeta kategorija časovnega lista**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="b5e67-123">Vnesite ali izberite vrednost v polju **Privzeta kategorija stroškov**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="b5e67-124">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-124">Select **Save**.</span></span>
20. <span data-ttu-id="b5e67-125">Zaprite stran.</span><span class="sxs-lookup"><span data-stu-id="b5e67-125">Close the page.</span></span>
21. <span data-ttu-id="b5e67-126">V podoknu za krmarjenje pojdite na **Moduli > Vodenje projektov in računovodstvo> Nastavitev> Knjiženje > Nastavite knjiženja glavne knjige**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="b5e67-127">Izberite možnost v polju **Vrste računov glavne knjige**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="b5e67-128">Izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-128">Select **New**.</span></span>
24. <span data-ttu-id="b5e67-129">V polju **Glavni račun** v novi vrstici navedite želene vrednosti.</span><span class="sxs-lookup"><span data-stu-id="b5e67-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="b5e67-130">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-130">Select **Save**.</span></span>
26. <span data-ttu-id="b5e67-131">Zaprite stran.</span><span class="sxs-lookup"><span data-stu-id="b5e67-131">Close the page.</span></span>
27. <span data-ttu-id="b5e67-132">V podoknu za krmarjenje pojdite na **Moduli > Vodenje projektov in računovodstvo> Nastavitev> Cene > Cena prenosa**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="b5e67-133">Izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-133">Select **New**.</span></span>
29. <span data-ttu-id="b5e67-134">Vnesite datum v polje **Datum začetka veljavnosti**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="b5e67-135">Vnesite ali izberite vrednost v polju **Pravna oseba, ki si izposoja**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="b5e67-136">Izberite možnost v polju **Model cene prenosa**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="b5e67-137">Vnesite številko v polje **Oblikovanje cen**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="b5e67-138">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="b5e67-138">Select **Save**.</span></span>

