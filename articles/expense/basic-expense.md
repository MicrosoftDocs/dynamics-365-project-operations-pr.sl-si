---
title: Vnos stroškov (poenostavljen)
description: Ta tema vsebuje informacije o tem, kako delati z vnosom stroškov v poenostavljeni uvedbi.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965893"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="3daa0-103">Vnos stroškov (poenostavljen)</span><span class="sxs-lookup"><span data-stu-id="3daa0-103">Expense entry (lite)</span></span>

<span data-ttu-id="3daa0-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="3daa0-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3daa0-105">Osnovno ali poenostavljeno upravljanje stroškov pomeni zmožnost beleženja enostavnih stroškov.</span><span class="sxs-lookup"><span data-stu-id="3daa0-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="3daa0-106">Stroške lahko beležite za projekt, nato pa jih bo odobritelj projekta pregledal in odobril.</span><span class="sxs-lookup"><span data-stu-id="3daa0-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="3daa0-107">Za več informacij o stroškovnih zmožnostih v aplikaciji Dynamics 365 Project Operations glejte razdelek [Pregled stroškov](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3daa0-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="3daa0-108">Zajem posameznega osnovnega stroška</span><span class="sxs-lookup"><span data-stu-id="3daa0-108">Capture a basic expense</span></span>

<span data-ttu-id="3daa0-109">Podatke o stroških lahko zajamete in jih predložite odobritelju.</span><span class="sxs-lookup"><span data-stu-id="3daa0-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="3daa0-110">Odprite razdelek **Stroški** in izberite možnost **Novo**.</span><span class="sxs-lookup"><span data-stu-id="3daa0-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="3daa0-111">Na strani **Nov strošek** vnesite zahtevane podatke o stroških in nato izberite možnost **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="3daa0-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="3daa0-112">Pošiljanje posameznega osnovnega stroška</span><span class="sxs-lookup"><span data-stu-id="3daa0-112">Submit a basic expense</span></span>

<span data-ttu-id="3daa0-113">Ko končate z zajemanjem vseh stroškov in ste pripravljeni, da se jih odobri, jih morate najprej poslati v presojo.</span><span class="sxs-lookup"><span data-stu-id="3daa0-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="3daa0-114">Odprite razdelek **Stroški** in izberite posamezen strošek.</span><span class="sxs-lookup"><span data-stu-id="3daa0-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="3daa0-115">Ali pa s potrditvenim poljem v glavi izberite vse stroške.</span><span class="sxs-lookup"><span data-stu-id="3daa0-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="3daa0-116">Izberite **Pošlji**.</span><span class="sxs-lookup"><span data-stu-id="3daa0-116">Select **Submit**.</span></span> <span data-ttu-id="3daa0-117">Sistem obdela izbrane vnose in nato ustvari zahteve za odobritev stroškov.</span><span class="sxs-lookup"><span data-stu-id="3daa0-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="3daa0-118">Preklic posameznega osnovnega stroška</span><span class="sxs-lookup"><span data-stu-id="3daa0-118">Recall a basic expense</span></span>

<span data-ttu-id="3daa0-119">Če v presojo pošljete strošek po pomoti, ga lahko prekličete.</span><span class="sxs-lookup"><span data-stu-id="3daa0-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="3daa0-120">Čas, ki je potreben za preklic vnosa stroškov, je odvisen od stopnje odobritve.</span><span class="sxs-lookup"><span data-stu-id="3daa0-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="3daa0-121">Če odobritelj še ni odobril vnosa, se lahko preklic izvede takoj.</span><span class="sxs-lookup"><span data-stu-id="3daa0-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="3daa0-122">Če pa je vnos že odobren, se od odobritelja zahteva odobritev preklica in razveljavitev transakcij.</span><span class="sxs-lookup"><span data-stu-id="3daa0-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="3daa0-123">V razdelku **Stroški** na seznamu stroškov izberite strošek, ki ga želite preklicati.</span><span class="sxs-lookup"><span data-stu-id="3daa0-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="3daa0-124">Izberite **Prekliči**.</span><span class="sxs-lookup"><span data-stu-id="3daa0-124">Select **Recall**.</span></span> <span data-ttu-id="3daa0-125">Če vnos stroška še ni odobren, ga sistem takoj prekliče.</span><span class="sxs-lookup"><span data-stu-id="3daa0-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="3daa0-126">Če je bil vnos stroškov že odobren, se ustvari zahteva za preklic, s katero se odobritelja obvesti, da želite stornirati stroške.</span><span class="sxs-lookup"><span data-stu-id="3daa0-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="3daa0-127">Odobritelj bo nato potrdil, ali je razveljavitev mogoča, in vnos bo vrnjen.</span><span class="sxs-lookup"><span data-stu-id="3daa0-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="3daa0-128">Izbris posameznega osnovnega stroška</span><span class="sxs-lookup"><span data-stu-id="3daa0-128">Delete a basic expense</span></span>

<span data-ttu-id="3daa0-129">Stroške, ki še niso bili poslani, je mogoče izbrisati.</span><span class="sxs-lookup"><span data-stu-id="3daa0-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="3daa0-130">Če želite izbrisati že oddani strošek, ga morate najprej preklicati.</span><span class="sxs-lookup"><span data-stu-id="3daa0-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="3daa0-131">Glejte tudi</span><span class="sxs-lookup"><span data-stu-id="3daa0-131">See also</span></span>

- [<span data-ttu-id="3daa0-132">Pregled odobritev</span><span class="sxs-lookup"><span data-stu-id="3daa0-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
