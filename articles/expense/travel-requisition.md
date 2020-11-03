---
title: Zahteve za pot
description: Ta tema vsebuje informacije o zahtevah za pot.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084625"
---
# <a name="travel-requisitions"></a><span data-ttu-id="a34ab-103">Zahteve za pot</span><span class="sxs-lookup"><span data-stu-id="a34ab-103">Travel requisitions</span></span>

<span data-ttu-id="a34ab-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="a34ab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a34ab-105">Zahteva za pot navaja stroške, ki bodo nastali zaradi potovanja.</span><span class="sxs-lookup"><span data-stu-id="a34ab-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="a34ab-106">Zahteva za pot se predloži v pregled in se lahko uporabi za odobritev stroškov.</span><span class="sxs-lookup"><span data-stu-id="a34ab-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="a34ab-107">Morda boste morali predložiti zahtevo za pot, preden boste imeli kakršne koli stroške, ki se zaračunajo organizaciji.</span><span class="sxs-lookup"><span data-stu-id="a34ab-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="a34ab-108">Ta zahteva velja ne glede na to, ali za stroške bremenite kreditno kartico podjetja, uporabite gotovino, ki ste jo prejeli kot denarni predujem, ali sami plačate stroške, ki jih bo organizacija povrnila.</span><span class="sxs-lookup"><span data-stu-id="a34ab-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="a34ab-109">Zahteve za pot in pravilniki se lahko uporabljajo za pomoč pri upravljanju izdatkov organizacije.</span><span class="sxs-lookup"><span data-stu-id="a34ab-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="a34ab-110">Če na primer vaša organizacija dela na projektu s fiksno ceno, pri katerem je potrebno potovanje, se morajo potni stroški članov projektne ekipe ujemati s proračunom projekta.</span><span class="sxs-lookup"><span data-stu-id="a34ab-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="a34ab-111">Z zahtevo po odobritvi potnih stroškov, preden nastanejo, lahko organizacija pomaga zagotoviti, da projekt ostane v okviru proračuna.</span><span class="sxs-lookup"><span data-stu-id="a34ab-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="a34ab-112">Konfiguracija</span><span class="sxs-lookup"><span data-stu-id="a34ab-112">Configuration</span></span> 

<span data-ttu-id="a34ab-113">Zahteve za pot lahko nastavite kot »obvezne«, tako da v parametrih upravljanja stroškov omogočite parameter »Predhodna odobritev potovanja je obvezna«.</span><span class="sxs-lookup"><span data-stu-id="a34ab-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="a34ab-114">Ustvarjanje in pošiljanje zahtev za pot</span><span class="sxs-lookup"><span data-stu-id="a34ab-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="a34ab-115">Odprite možnost **Moji stroški: Zahteva za pot** in izberite **Nova zahteva za pot**.</span><span class="sxs-lookup"><span data-stu-id="a34ab-115">Go to **My expenses: Travel Requisition** , and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="a34ab-116">Vnesite namen in cilj zahteve.</span><span class="sxs-lookup"><span data-stu-id="a34ab-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="a34ab-117">V polje **Opis potovanja** vnesite dodatne podatke.</span><span class="sxs-lookup"><span data-stu-id="a34ab-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="a34ab-118">Za vsakega od pričakovanih stroškov, kot so let, prehrana ali najem avtomobila, ustvarite postavko vrstice stroška.</span><span class="sxs-lookup"><span data-stu-id="a34ab-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="a34ab-119">Vključite predvideni datum, predvideni znesek in valuto za vsak strošek.</span><span class="sxs-lookup"><span data-stu-id="a34ab-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="a34ab-120">Ko končate z dodajanjem pričakovanih stroškov, izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="a34ab-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="a34ab-121">Ko ste pripravljeni na pošiljanje zahteve za pot, izberite **Potek dela** > **Pošlji**.</span><span class="sxs-lookup"><span data-stu-id="a34ab-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="a34ab-122">Odobrene zahteve za pot si lahko ogledate v možnosti **Moji stroški: Zahteva za pot**.</span><span class="sxs-lookup"><span data-stu-id="a34ab-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="a34ab-123">Oglejte si zahteve za pot, ki so na voljo</span><span class="sxs-lookup"><span data-stu-id="a34ab-123">View available travel requisitions</span></span>

<span data-ttu-id="a34ab-124">Vse svoje zahteve za pot si lahko ogledate v možnosti **Moji stroški: Zahteve za pot**.</span><span class="sxs-lookup"><span data-stu-id="a34ab-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="a34ab-125">Odobritev zahtev za pot</span><span class="sxs-lookup"><span data-stu-id="a34ab-125">Approve travel requisitions</span></span>

<span data-ttu-id="a34ab-126">Izberite zahtevo za pot, ki jo želite odobriti, in nato izberite **Potek dela** > **Odobri**.</span><span class="sxs-lookup"><span data-stu-id="a34ab-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="a34ab-127">Pošiljanje poročila o stroških z odobreno zahtevo za pot</span><span class="sxs-lookup"><span data-stu-id="a34ab-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="a34ab-128">Ustvarite novo poročilo o stroških in v glavi poročila o stroških ter na seznamu odobrenih zahtev za pot izberite **Preslikava v zahtevo za pot**.</span><span class="sxs-lookup"><span data-stu-id="a34ab-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="a34ab-129">Polje **Znesek zahteve za pot** polje se samodejno posodobi v glavi poročila o stroških.</span><span class="sxs-lookup"><span data-stu-id="a34ab-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="a34ab-130">Dodajte vse stroške, nastale na potovanju.</span><span class="sxs-lookup"><span data-stu-id="a34ab-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="a34ab-131">Če je omogočeno polje **Vnaprej odobreno** , se usklajeni znesek in odobreni znesek za določeno kategorijo stroškov posodobita.</span><span class="sxs-lookup"><span data-stu-id="a34ab-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="a34ab-132">Ko preslikate poročilo o stroških v odobreno zahtevo za pot, znesek transakcije ne sme biti večji od odobrenega zneska.</span><span class="sxs-lookup"><span data-stu-id="a34ab-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
