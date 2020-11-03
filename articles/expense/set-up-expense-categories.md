---
title: Nastavitev kategorij stroškov
description: Ta tema vsebuje informacije o nastavitvi kategorij stroškov in skupnih kategorij za poročila o stroških.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084646"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="70845-103">Nastavitev kategorij stroškov</span><span class="sxs-lookup"><span data-stu-id="70845-103">Set up expense categories</span></span>

<span data-ttu-id="70845-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="70845-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="70845-105">Ko zaposleni ustvarijo poročila o stroških, morajo biti vsi zabeleženi stroški povezani s kategorijo stroškov.</span><span class="sxs-lookup"><span data-stu-id="70845-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="70845-106">Kategorije stroškov izhajajo iz skupnih kategorij, ki si jih delijo vse pravne osebe v vaši organizaciji.</span><span class="sxs-lookup"><span data-stu-id="70845-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="70845-107">Če struktura vaše organizacije to omogoča, lahko te kategorije stroškov delite tudi z drugimi področji.</span><span class="sxs-lookup"><span data-stu-id="70845-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="70845-108">Na podlagi strukture vaše organizacije in navodil izvedbene ekipe morate določiti, ali se bodo kategorije, ki se uporabljajo pri upravljanju stroškov, uporabljale samo pri upravljanju stroškov ali jih boste delili z drugimi področji.</span><span class="sxs-lookup"><span data-stu-id="70845-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="70845-109">Te kategorije si lahko delita oddelka »Vodenje projekta in računovodstvo« in »Upravljanje stroškov« oz. »Vodenje projekta in računovodstvo« in »Proizvodnja«.</span><span class="sxs-lookup"><span data-stu-id="70845-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="70845-110">Ne moreta pa si jih deliti »Upravljanje stroškov« in »Proizvodnja«.</span><span class="sxs-lookup"><span data-stu-id="70845-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="70845-111">Pred začetkom postopka namestitve se morate za vsako kategorijo stroškov odločiti o naslednjem:</span><span class="sxs-lookup"><span data-stu-id="70845-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="70845-112">Katera kategorija stroška je izbrana?</span><span class="sxs-lookup"><span data-stu-id="70845-112">What is the expense category?</span></span> <span data-ttu-id="70845-113">Primeri vključujejo kategorije za lete, hotele ali kilometrino.</span><span class="sxs-lookup"><span data-stu-id="70845-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="70845-114">Ali lahko kategorijo stroškov uporabljajo tudi na oddelku »Vodenje projekta in računovodstvo«?</span><span class="sxs-lookup"><span data-stu-id="70845-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="70845-115">Če je odgovor pritrdilen, morate določiti tudi naslednje:</span><span class="sxs-lookup"><span data-stu-id="70845-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="70845-116">Kateri računi stroškov bodo uporabljeni za naslednje stroške?</span><span class="sxs-lookup"><span data-stu-id="70845-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="70845-117">Cena</span><span class="sxs-lookup"><span data-stu-id="70845-117">Cost</span></span>
        - <span data-ttu-id="70845-118">Dodelitev plače</span><span class="sxs-lookup"><span data-stu-id="70845-118">Payroll allocation</span></span>
        - <span data-ttu-id="70845-119">Vrednost cene WIP</span><span class="sxs-lookup"><span data-stu-id="70845-119">WIP-cost value</span></span>
        - <span data-ttu-id="70845-120">Element stroška</span><span class="sxs-lookup"><span data-stu-id="70845-120">Cost-item</span></span>
        - <span data-ttu-id="70845-121">Element vrednosti cene WIP</span><span class="sxs-lookup"><span data-stu-id="70845-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="70845-122">Vračunana izguba</span><span class="sxs-lookup"><span data-stu-id="70845-122">Accrued loss</span></span>
        - <span data-ttu-id="70845-123">Vračunana izguba WIP</span><span class="sxs-lookup"><span data-stu-id="70845-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="70845-124">Kateri računi prihodkov bodo uporabljeni za naslednje vire prihodkov?</span><span class="sxs-lookup"><span data-stu-id="70845-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="70845-125">Fakturirani prihodek</span><span class="sxs-lookup"><span data-stu-id="70845-125">Invoiced revenue</span></span>
        - <span data-ttu-id="70845-126">Vračunana vrednost prihodkov od prodaje</span><span class="sxs-lookup"><span data-stu-id="70845-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="70845-127">Vrednost prodaje WIP</span><span class="sxs-lookup"><span data-stu-id="70845-127">WIP-sales value</span></span>
        - <span data-ttu-id="70845-128">Vračunano razmerje med prihodkom in proizvodnjo</span><span class="sxs-lookup"><span data-stu-id="70845-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="70845-129">Proizvodnja WIP</span><span class="sxs-lookup"><span data-stu-id="70845-129">WIP-production</span></span>
        - <span data-ttu-id="70845-130">Vračunano razmerje med prihodkom in dobičkom</span><span class="sxs-lookup"><span data-stu-id="70845-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="70845-131">Dobiček WIP</span><span class="sxs-lookup"><span data-stu-id="70845-131">WIP-profit</span></span>
        - <span data-ttu-id="70845-132">Vračunano razmerje med prihodkom in naročnino</span><span class="sxs-lookup"><span data-stu-id="70845-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="70845-133">Naročnina WIP</span><span class="sxs-lookup"><span data-stu-id="70845-133">WIP-subscription</span></span>

- <span data-ttu-id="70845-134">Katera vrsta stroška je izbrana?</span><span class="sxs-lookup"><span data-stu-id="70845-134">What is the expense type?</span></span>
- <span data-ttu-id="70845-135">Kateri je privzeti način plačila za kategorijo stroškov?</span><span class="sxs-lookup"><span data-stu-id="70845-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="70845-136">Ali je treba razčleniti stroške v kategoriji stroškov?</span><span class="sxs-lookup"><span data-stu-id="70845-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="70845-137">Kateri je glavni privzeti račun za kategorijo stroškov?</span><span class="sxs-lookup"><span data-stu-id="70845-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="70845-138">Katera je privzeta davčna skupina za prodajo izdelka za kategorijo stroškov?</span><span class="sxs-lookup"><span data-stu-id="70845-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="70845-139">Ali so za kategorijo stroškov dovoljeni dodatni načini plačila?</span><span class="sxs-lookup"><span data-stu-id="70845-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="70845-140">Če je odgovor pritrdilen, kateri so to?</span><span class="sxs-lookup"><span data-stu-id="70845-140">If so, what are they?</span></span>
- <span data-ttu-id="70845-141">Ali obstajajo podkategorije v tej kategoriji stroškov?</span><span class="sxs-lookup"><span data-stu-id="70845-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="70845-142">Če obstajajo podkategorije, morate določiti tudi naslednje:</span><span class="sxs-lookup"><span data-stu-id="70845-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="70845-143">Ali je katera od podkategorij izključena iz davčne olajšave?</span><span class="sxs-lookup"><span data-stu-id="70845-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="70845-144">Katera davčna skupina za prodajo izdelka velja za podkategorije?</span><span class="sxs-lookup"><span data-stu-id="70845-144">What is the item sales tax group of the subcategories?</span></span>
