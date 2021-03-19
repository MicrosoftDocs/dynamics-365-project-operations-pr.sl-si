---
title: Nastavitev potekov dela za upravljanje stroškov
description: Nastavite lahko proces poteka dela za pregled in odobritev dokumentov glede poti in stroškov.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36ab1edc4769013684fa9248e6c5eac025637bbd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271643"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="19586-103">Nastavitev potekov dela za upravljanje stroškov</span><span class="sxs-lookup"><span data-stu-id="19586-103">Set up Expense management workflows</span></span>

<span data-ttu-id="19586-104">Nastavite lahko proces poteka dela, ki se uporablja za pregled in odobritev dokumentov glede poti in stroškov.</span><span class="sxs-lookup"><span data-stu-id="19586-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="19586-105">Dokumenti, za katere lahko opredelite poteke dela, vključujejo poročila o stroških, zahteve za pot in zahteve za denarne predujme.</span><span class="sxs-lookup"><span data-stu-id="19586-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="19586-106">Potek dela predstavlja poslovni proces.</span><span class="sxs-lookup"><span data-stu-id="19586-106">A workflow represents a business process.</span></span> <span data-ttu-id="19586-107">V njem je določeno, kako dokument teče skozi sistem in kdo mora dokončati opravilo ali odobriti dokument.</span><span class="sxs-lookup"><span data-stu-id="19586-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="19586-108">Uporaba sistema poteka dela v vaši organizaciji ima več prednosti:</span><span class="sxs-lookup"><span data-stu-id="19586-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="19586-109">**Dosledni procesi** – določite lahko postopek odobritve za določene dokumente, na primer zahteve za nakup in poročila o stroških.</span><span class="sxs-lookup"><span data-stu-id="19586-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="19586-110">Uporaba sistema poteka dela pomaga zagotoviti dosledno in učinkovito obdelavo in odobritev dokumentov.</span><span class="sxs-lookup"><span data-stu-id="19586-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="19586-111">Vidljivost procesa – sledite lahko meritvam stanja, zgodovine in uspešnosti določenega primerka poteka dela.</span><span class="sxs-lookup"><span data-stu-id="19586-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="19586-112">To vam pomaga določiti, ali bi bilo treba potek dela spremeniti za izboljšanje učinkovitosti.</span><span class="sxs-lookup"><span data-stu-id="19586-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="19586-113">Centraliziran delovni seznam – uporabniki si lahko ogledajo centraliziran delovni seznam, da si ogledajo opravila poteka dela in odobritve, ki so jim dodeljene.</span><span class="sxs-lookup"><span data-stu-id="19586-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="19586-114">**Vrste potekov dela, ki jih lahko ustvarite**</span><span class="sxs-lookup"><span data-stu-id="19586-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="19586-115">V naslednji tabeli so navedene vrste poteka dela, ki jih lahko ustvarite v možnosti **Stroški**.</span><span class="sxs-lookup"><span data-stu-id="19586-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="19586-116"><strong>Vrsta </strong></span><span class="sxs-lookup"><span data-stu-id="19586-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="19586-117"><strong>Uporabite to vrsto za</strong></span><span class="sxs-lookup"><span data-stu-id="19586-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="19586-118"><strong>Poročilo o stroških</strong></span><span class="sxs-lookup"><span data-stu-id="19586-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="19586-119">Ustvarite poteke dela odobritve za poročila o stroških.</span><span class="sxs-lookup"><span data-stu-id="19586-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="19586-120"><strong>Samodejno knjiženje poročil o stroških</strong></span><span class="sxs-lookup"><span data-stu-id="19586-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="19586-121">Ustvarite poteke dela samodejnega knjiženja za poročila o stroških.</span><span class="sxs-lookup"><span data-stu-id="19586-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="19586-122"><strong>Postavka vrstice stroška</strong></span><span class="sxs-lookup"><span data-stu-id="19586-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="19586-123">Ustvarite poteke dela odobritve za postavke vrstice v poročilih o stroških.</span><span class="sxs-lookup"><span data-stu-id="19586-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="19586-124"><strong>Samodejno knjiženje postavke vrstice stroška</strong></span><span class="sxs-lookup"><span data-stu-id="19586-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="19586-125">Ustvarite poteke dela samodejnih knjiženj za postavke vrstice v poročilih o stroških.</span><span class="sxs-lookup"><span data-stu-id="19586-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="19586-126"><strong>Zahteva za pot</strong></span><span class="sxs-lookup"><span data-stu-id="19586-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="19586-127">Ustvarite poteke dela odobritve za zahteve za pot.</span><span class="sxs-lookup"><span data-stu-id="19586-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="19586-128"><strong>Zahteva za denarni predujem</strong></span><span class="sxs-lookup"><span data-stu-id="19586-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="19586-129">Ustvarite poteke dela odobritve za zahteve za denarni predujem.</span><span class="sxs-lookup"><span data-stu-id="19586-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="19586-130"><strong>Izterjava davka DDV</strong></span><span class="sxs-lookup"><span data-stu-id="19586-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="19586-131">Ustvarite poteke dela odobritve za izterjavo davka na dodano vrednost (DDV).</span><span class="sxs-lookup"><span data-stu-id="19586-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]