---
title: Konfiguriranje zaračunavanja projektov med podjetji
description: V tej temi je prikazano, kako nastavite zaračunavanje projektov med dvema podjetjema v vaši organizaciji.
author: Yowelle
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
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
ms.openlocfilehash: ad25aba492b7902ddd8955be87f88f96f6d4508f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001221"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="781c4-103">Konfiguriranje zaračunavanja projektov med podjetji</span><span class="sxs-lookup"><span data-stu-id="781c4-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="781c4-104">V tej temi je prikazano, kako nastavite zaračunavanje projektov med dvema podjetjema v vaši organizaciji.</span><span class="sxs-lookup"><span data-stu-id="781c4-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="781c4-105">To opravilo uporablja nabor podatkov USSI.</span><span class="sxs-lookup"><span data-stu-id="781c4-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="781c4-106">V podoknu za krmarjenje pojdite na **Moduli > Obveznosti > Dobavitelji > Vsi dobavitelji**.</span><span class="sxs-lookup"><span data-stu-id="781c4-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="781c4-107">Na seznamu **Vsi dobavitelji** poiščite in izberite želeni zapis.</span><span class="sxs-lookup"><span data-stu-id="781c4-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="781c4-108">V podoknu za dejanja izberite **Splošno**.</span><span class="sxs-lookup"><span data-stu-id="781c4-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="781c4-109">Izberite **Med podjetji**.</span><span class="sxs-lookup"><span data-stu-id="781c4-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="781c4-110">Nastavite **Aktivno** na **Da**, da omogočite medpodjetniško trgovanje.</span><span class="sxs-lookup"><span data-stu-id="781c4-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="781c4-111">Vnesite ali izberite vrednost v polju **Podjetje stranke**.</span><span class="sxs-lookup"><span data-stu-id="781c4-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="781c4-112">Vnesite ali izberite vrednost v polju **Moj račun**.</span><span class="sxs-lookup"><span data-stu-id="781c4-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="781c4-113">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="781c4-113">Select **Save**.</span></span>
9. <span data-ttu-id="781c4-114">Zaprite strani, da se vrnete na domačo stran.</span><span class="sxs-lookup"><span data-stu-id="781c4-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="781c4-115">V podoknu za krmarjenje pojdite na **Moduli > Vodenje projektov in računovodstvo> Nastavitev> Vodenje projektov in računovodski parametri**.</span><span class="sxs-lookup"><span data-stu-id="781c4-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="781c4-116">Izberite zavihek **Med podjetji**.</span><span class="sxs-lookup"><span data-stu-id="781c4-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="781c4-117">Premaknite drsnik na **Da**, da omogočite razporejanje virov in časovnice med podjetji.</span><span class="sxs-lookup"><span data-stu-id="781c4-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="781c4-118">Na seznamu označite izbrano vrstico.</span><span class="sxs-lookup"><span data-stu-id="781c4-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="781c4-119">Izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="781c4-119">Select **New**.</span></span>
15. <span data-ttu-id="781c4-120">Vnesite ali izberite vrednost v polju **Pravna oseba, ki si izposoja**.</span><span class="sxs-lookup"><span data-stu-id="781c4-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="781c4-121">Potrdite potrditveno polje **Obračunaj prihodke**.</span><span class="sxs-lookup"><span data-stu-id="781c4-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="781c4-122">Vnesite ali izberite vrednost v polju **Privzeta kategorija časovnega lista**.</span><span class="sxs-lookup"><span data-stu-id="781c4-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="781c4-123">Vnesite ali izberite vrednost v polju **Privzeta kategorija stroškov**.</span><span class="sxs-lookup"><span data-stu-id="781c4-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="781c4-124">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="781c4-124">Select **Save**.</span></span>
20. <span data-ttu-id="781c4-125">Zaprite stran.</span><span class="sxs-lookup"><span data-stu-id="781c4-125">Close the page.</span></span>
21. <span data-ttu-id="781c4-126">V podoknu za krmarjenje pojdite na **Moduli > Vodenje projektov in računovodstvo> Nastavitev> Knjiženje > Nastavite knjiženja glavne knjige**.</span><span class="sxs-lookup"><span data-stu-id="781c4-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="781c4-127">Izberite možnost v polju **Vrste računov glavne knjige**.</span><span class="sxs-lookup"><span data-stu-id="781c4-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="781c4-128">Izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="781c4-128">Select **New**.</span></span>
24. <span data-ttu-id="781c4-129">V polju **Glavni račun** v novi vrstici navedite želene vrednosti.</span><span class="sxs-lookup"><span data-stu-id="781c4-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="781c4-130">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="781c4-130">Select **Save**.</span></span>
26. <span data-ttu-id="781c4-131">Zaprite stran.</span><span class="sxs-lookup"><span data-stu-id="781c4-131">Close the page.</span></span>
27. <span data-ttu-id="781c4-132">V podoknu za krmarjenje pojdite na **Moduli > Vodenje projektov in računovodstvo> Nastavitev> Cene > Cena prenosa**.</span><span class="sxs-lookup"><span data-stu-id="781c4-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="781c4-133">Izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="781c4-133">Select **New**.</span></span>
29. <span data-ttu-id="781c4-134">Vnesite datum v polje **Datum začetka veljavnosti**.</span><span class="sxs-lookup"><span data-stu-id="781c4-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="781c4-135">Vnesite ali izberite vrednost v polju **Pravna oseba, ki si izposoja**.</span><span class="sxs-lookup"><span data-stu-id="781c4-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="781c4-136">Izberite možnost v polju **Model cene prenosa**.</span><span class="sxs-lookup"><span data-stu-id="781c4-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="781c4-137">Vnesite številko v polje **Oblikovanje cen**.</span><span class="sxs-lookup"><span data-stu-id="781c4-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="781c4-138">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="781c4-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]