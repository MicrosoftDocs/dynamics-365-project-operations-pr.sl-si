---
title: Nastavitev kategorij stroškov
description: Ta tema vsebuje informacije o nastavitvi kategorij stroškov in skupnih kategorij za poročila o stroških.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: d66df1ffd2be2ff884561010c46cda255a2d2189
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001829"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="66001-103">Nastavitev kategorij stroškov</span><span class="sxs-lookup"><span data-stu-id="66001-103">Set up expense categories</span></span>

<span data-ttu-id="66001-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="66001-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="66001-105">Ko zaposleni ustvarijo poročila o stroških, morajo biti vsi zabeleženi stroški povezani s kategorijo stroškov.</span><span class="sxs-lookup"><span data-stu-id="66001-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="66001-106">Kategorije stroškov izhajajo iz skupnih kategorij, ki si jih delijo vse pravne osebe v vaši organizaciji.</span><span class="sxs-lookup"><span data-stu-id="66001-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="66001-107">Če struktura vaše organizacije to omogoča, lahko te kategorije stroškov delite tudi z drugimi področji.</span><span class="sxs-lookup"><span data-stu-id="66001-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="66001-108">Na podlagi strukture vaše organizacije in navodil izvedbene ekipe morate določiti, ali se bodo kategorije, ki se uporabljajo pri upravljanju stroškov, uporabljale samo pri upravljanju stroškov ali jih boste delili z drugimi področji.</span><span class="sxs-lookup"><span data-stu-id="66001-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="66001-109">Te kategorije si lahko delita oddelka »Vodenje projekta in računovodstvo« in »Upravljanje stroškov« oz. »Vodenje projekta in računovodstvo« in »Proizvodnja«.</span><span class="sxs-lookup"><span data-stu-id="66001-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="66001-110">Ne moreta pa si jih deliti »Upravljanje stroškov« in »Proizvodnja«.</span><span class="sxs-lookup"><span data-stu-id="66001-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="66001-111">Pred začetkom postopka namestitve se morate za vsako kategorijo stroškov odločiti o naslednjem:</span><span class="sxs-lookup"><span data-stu-id="66001-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="66001-112">Katera kategorija stroška je izbrana?</span><span class="sxs-lookup"><span data-stu-id="66001-112">What is the expense category?</span></span> <span data-ttu-id="66001-113">Primeri vključujejo kategorije za lete, hotele ali kilometrino.</span><span class="sxs-lookup"><span data-stu-id="66001-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="66001-114">Ali lahko kategorijo stroškov uporabljajo tudi na oddelku »Vodenje projekta in računovodstvo«?</span><span class="sxs-lookup"><span data-stu-id="66001-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="66001-115">Če je odgovor pritrdilen, morate določiti tudi naslednje:</span><span class="sxs-lookup"><span data-stu-id="66001-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="66001-116">Kateri računi stroškov bodo uporabljeni za naslednje stroške?</span><span class="sxs-lookup"><span data-stu-id="66001-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="66001-117">Cena</span><span class="sxs-lookup"><span data-stu-id="66001-117">Cost</span></span>
        - <span data-ttu-id="66001-118">Dodelitev plače</span><span class="sxs-lookup"><span data-stu-id="66001-118">Payroll allocation</span></span>
        - <span data-ttu-id="66001-119">Vrednost cene WIP</span><span class="sxs-lookup"><span data-stu-id="66001-119">WIP-cost value</span></span>
        - <span data-ttu-id="66001-120">Element stroška</span><span class="sxs-lookup"><span data-stu-id="66001-120">Cost-item</span></span>
        - <span data-ttu-id="66001-121">Element vrednosti cene WIP</span><span class="sxs-lookup"><span data-stu-id="66001-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="66001-122">Vračunana izguba</span><span class="sxs-lookup"><span data-stu-id="66001-122">Accrued loss</span></span>
        - <span data-ttu-id="66001-123">Vračunana izguba WIP</span><span class="sxs-lookup"><span data-stu-id="66001-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="66001-124">Kateri računi prihodkov bodo uporabljeni za naslednje vire prihodkov?</span><span class="sxs-lookup"><span data-stu-id="66001-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="66001-125">Fakturirani prihodek</span><span class="sxs-lookup"><span data-stu-id="66001-125">Invoiced revenue</span></span>
        - <span data-ttu-id="66001-126">Vračunana vrednost prihodkov od prodaje</span><span class="sxs-lookup"><span data-stu-id="66001-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="66001-127">Vrednost prodaje WIP</span><span class="sxs-lookup"><span data-stu-id="66001-127">WIP-sales value</span></span>
        - <span data-ttu-id="66001-128">Vračunano razmerje med prihodkom in proizvodnjo</span><span class="sxs-lookup"><span data-stu-id="66001-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="66001-129">Proizvodnja WIP</span><span class="sxs-lookup"><span data-stu-id="66001-129">WIP-production</span></span>
        - <span data-ttu-id="66001-130">Vračunano razmerje med prihodkom in dobičkom</span><span class="sxs-lookup"><span data-stu-id="66001-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="66001-131">Dobiček WIP</span><span class="sxs-lookup"><span data-stu-id="66001-131">WIP-profit</span></span>
        - <span data-ttu-id="66001-132">Vračunano razmerje med prihodkom in naročnino</span><span class="sxs-lookup"><span data-stu-id="66001-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="66001-133">Naročnina WIP</span><span class="sxs-lookup"><span data-stu-id="66001-133">WIP-subscription</span></span>

- <span data-ttu-id="66001-134">Katera vrsta stroška je izbrana?</span><span class="sxs-lookup"><span data-stu-id="66001-134">What is the expense type?</span></span>
- <span data-ttu-id="66001-135">Kateri je privzeti način plačila za kategorijo stroškov?</span><span class="sxs-lookup"><span data-stu-id="66001-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="66001-136">Ali je treba razčleniti stroške v kategoriji stroškov?</span><span class="sxs-lookup"><span data-stu-id="66001-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="66001-137">Kateri je glavni privzeti račun za kategorijo stroškov?</span><span class="sxs-lookup"><span data-stu-id="66001-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="66001-138">Katera je privzeta davčna skupina za prodajo izdelka za kategorijo stroškov?</span><span class="sxs-lookup"><span data-stu-id="66001-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="66001-139">Ali so za kategorijo stroškov dovoljeni dodatni načini plačila?</span><span class="sxs-lookup"><span data-stu-id="66001-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="66001-140">Če je odgovor pritrdilen, kateri so to?</span><span class="sxs-lookup"><span data-stu-id="66001-140">If so, what are they?</span></span>
- <span data-ttu-id="66001-141">Ali obstajajo podkategorije v tej kategoriji stroškov?</span><span class="sxs-lookup"><span data-stu-id="66001-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="66001-142">Če obstajajo podkategorije, morate določiti tudi naslednje:</span><span class="sxs-lookup"><span data-stu-id="66001-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="66001-143">Ali je katera od podkategorij izključena iz davčne olajšave?</span><span class="sxs-lookup"><span data-stu-id="66001-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="66001-144">Katera davčna skupina za prodajo izdelka velja za podkategorije?</span><span class="sxs-lookup"><span data-stu-id="66001-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]