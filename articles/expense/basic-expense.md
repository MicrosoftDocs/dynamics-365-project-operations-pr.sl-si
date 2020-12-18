---
title: Vnos stroškov (poenostavljen)
description: Ta tema vsebuje informacije o tem, kako delati z vnosom stroškov v poenostavljeni uvedbi.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d87094882751f0751a8d9d539fa4cdcfc6b7b0d7
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590966"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="d29cf-103">Vnos stroškov (poenostavljen)</span><span class="sxs-lookup"><span data-stu-id="d29cf-103">Expense entry (lite)</span></span>

<span data-ttu-id="d29cf-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="d29cf-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d29cf-105">Osnovno ali poenostavljeno upravljanje stroškov pomeni zmožnost beleženja enostavnih stroškov.</span><span class="sxs-lookup"><span data-stu-id="d29cf-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="d29cf-106">Stroške lahko beležite za projekt, nato pa jih bo odobritelj projekta pregledal in odobril.</span><span class="sxs-lookup"><span data-stu-id="d29cf-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="d29cf-107">Za več informacij o stroškovnih zmožnostih v Dynamics 365 Project Operations glejte [Pregled stroškov](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d29cf-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="d29cf-108">Zajem posameznega osnovnega stroška</span><span class="sxs-lookup"><span data-stu-id="d29cf-108">Capture a basic expense</span></span>

<span data-ttu-id="d29cf-109">Podatke o stroških lahko zajamete in jih predložite odobritelju.</span><span class="sxs-lookup"><span data-stu-id="d29cf-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="d29cf-110">Odprite razdelek **Stroški** in izberite možnost **Novo**.</span><span class="sxs-lookup"><span data-stu-id="d29cf-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="d29cf-111">Na strani **Nov strošek** vnesite zahtevane podatke o stroških in nato izberite možnost **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="d29cf-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="d29cf-112">Pošiljanje posameznega osnovnega stroška</span><span class="sxs-lookup"><span data-stu-id="d29cf-112">Submit a basic expense</span></span>

<span data-ttu-id="d29cf-113">Ko končate z zajemanjem vseh stroškov in ste pripravljeni, da se jih odobri, jih morate najprej poslati v presojo.</span><span class="sxs-lookup"><span data-stu-id="d29cf-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="d29cf-114">Odprite razdelek **Stroški** in izberite posamezen strošek.</span><span class="sxs-lookup"><span data-stu-id="d29cf-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="d29cf-115">Ali pa s potrditvenim poljem v glavi izberite vse stroške.</span><span class="sxs-lookup"><span data-stu-id="d29cf-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="d29cf-116">Izberite **Pošlji**.</span><span class="sxs-lookup"><span data-stu-id="d29cf-116">Select **Submit**.</span></span> <span data-ttu-id="d29cf-117">Sistem obdela izbrane vnose in nato ustvari zahteve za odobritev stroškov.</span><span class="sxs-lookup"><span data-stu-id="d29cf-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="d29cf-118">Dodaj prilogo</span><span class="sxs-lookup"><span data-stu-id="d29cf-118">Add an attachment</span></span>

<span data-ttu-id="d29cf-119">Morda boste morali odobritelju predložiti dodatno dokumentacijo o svojih stroških.</span><span class="sxs-lookup"><span data-stu-id="d29cf-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="d29cf-120">Na časovnico z vnosom stroška lahko priložite potrdilo.</span><span class="sxs-lookup"><span data-stu-id="d29cf-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="d29cf-121">Izberite **Uredi** in v razdelku **Časovnica** izberite ikono sponke, da priložite potrdilo.</span><span class="sxs-lookup"><span data-stu-id="d29cf-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="d29cf-122">Preklic posameznega osnovnega stroška</span><span class="sxs-lookup"><span data-stu-id="d29cf-122">Recall a basic expense</span></span>

<span data-ttu-id="d29cf-123">Če v presojo pošljete strošek po pomoti, ga lahko prekličete.</span><span class="sxs-lookup"><span data-stu-id="d29cf-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="d29cf-124">Čas, ki je potreben za preklic vnosa stroškov, je odvisen od stopnje odobritve.</span><span class="sxs-lookup"><span data-stu-id="d29cf-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="d29cf-125">Če odobritelj še ni odobril vnosa, se lahko preklic izvede takoj.</span><span class="sxs-lookup"><span data-stu-id="d29cf-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="d29cf-126">Če pa je vnos že odobren, se od odobritelja zahteva odobritev preklica in razveljavitev transakcij.</span><span class="sxs-lookup"><span data-stu-id="d29cf-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="d29cf-127">V razdelku **Stroški** na seznamu stroškov izberite strošek, ki ga želite preklicati.</span><span class="sxs-lookup"><span data-stu-id="d29cf-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="d29cf-128">Izberite **Prekliči**.</span><span class="sxs-lookup"><span data-stu-id="d29cf-128">Select **Recall**.</span></span> <span data-ttu-id="d29cf-129">Če vnos stroška še ni odobren, ga sistem takoj prekliče.</span><span class="sxs-lookup"><span data-stu-id="d29cf-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="d29cf-130">Če je bil vnos stroškov že odobren, se ustvari zahteva za preklic, s katero se odobritelja obvesti, da želite stornirati stroške.</span><span class="sxs-lookup"><span data-stu-id="d29cf-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="d29cf-131">Odobritelj bo nato potrdil, ali je razveljavitev mogoča, in vnos bo vrnjen.</span><span class="sxs-lookup"><span data-stu-id="d29cf-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="d29cf-132">Izbris posameznega osnovnega stroška</span><span class="sxs-lookup"><span data-stu-id="d29cf-132">Delete a basic expense</span></span>

<span data-ttu-id="d29cf-133">Stroške, ki še niso bili poslani, je mogoče izbrisati.</span><span class="sxs-lookup"><span data-stu-id="d29cf-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="d29cf-134">Če želite izbrisati že oddani strošek, ga morate najprej preklicati.</span><span class="sxs-lookup"><span data-stu-id="d29cf-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="d29cf-135">Glejte tudi</span><span class="sxs-lookup"><span data-stu-id="d29cf-135">See also</span></span>

- [<span data-ttu-id="d29cf-136">Pregled odobritev</span><span class="sxs-lookup"><span data-stu-id="d29cf-136">Approvals overview</span></span>](../approvals/approvals-overview.md)
