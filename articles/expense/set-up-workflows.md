---
title: Nastavitev potekov dela za upravljanje stroškov
description: Nastavite lahko proces poteka dela, ki se uporablja za pregled in odobritev dokumentov glede poti in stroškov.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: aab6e18d1ddcffa57cf7cd4cb09eec5a4b89c0fd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001041"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="708de-103">Nastavitev potekov dela za upravljanje stroškov</span><span class="sxs-lookup"><span data-stu-id="708de-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="708de-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="708de-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="708de-105">Nastavite lahko proces poteka dela za pregled in odobritev dokumentov glede poti in stroškov.</span><span class="sxs-lookup"><span data-stu-id="708de-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="708de-106">Opredelite lahko poteke dela za poročila o stroških, zahteve za pot in zahteve za denarne predujme.</span><span class="sxs-lookup"><span data-stu-id="708de-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="708de-107">Potek dela predstavlja poslovni proces in določa, kako dokument teče skozi sistem.</span><span class="sxs-lookup"><span data-stu-id="708de-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="708de-108">Potek dela tudi označuje, kdo mora dokončati opravilo ali odobriti dokument.</span><span class="sxs-lookup"><span data-stu-id="708de-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="708de-109">Uporaba sistema poteka dela v vaši organizaciji ima več prednosti:</span><span class="sxs-lookup"><span data-stu-id="708de-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="708de-110">**Dosledni procesi**: določite lahko postopek odobritve za določene dokumente, na primer zahteve za nakup in poročila o stroških.</span><span class="sxs-lookup"><span data-stu-id="708de-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="708de-111">Uporaba sistema poteka dela pomaga zagotoviti dosledno in učinkovito obdelavo in odobritev dokumentov.</span><span class="sxs-lookup"><span data-stu-id="708de-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="708de-112">**Vidljivost procesa**: sledite lahko meritvam stanja, zgodovine in uspešnosti določenega primerka poteka dela.</span><span class="sxs-lookup"><span data-stu-id="708de-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="708de-113">To vam pomaga določiti, ali bi bilo treba potek dela spremeniti za izboljšanje učinkovitosti.</span><span class="sxs-lookup"><span data-stu-id="708de-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="708de-114">**Centraliziran delovni seznam**: uporabniki si lahko ogledajo centraliziran delovni seznam, da si ogledajo opravila poteka dela in odobritve, ki so jim dodeljene.</span><span class="sxs-lookup"><span data-stu-id="708de-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="708de-115">Vrste poteka dela</span><span class="sxs-lookup"><span data-stu-id="708de-115">Workflow types</span></span>

<span data-ttu-id="708de-116">V naslednji tabeli so navedene vrste poteka dela, ki jih lahko ustvarite v možnosti **Upravljanje stroškov**.</span><span class="sxs-lookup"><span data-stu-id="708de-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="708de-117"><strong>Vrsta</strong></span><span class="sxs-lookup"><span data-stu-id="708de-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="708de-118"><strong>Uporabite to vrsto za</strong></span><span class="sxs-lookup"><span data-stu-id="708de-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="708de-119"><strong>Samodejno odobritev poročil o stroških</strong></span><span class="sxs-lookup"><span data-stu-id="708de-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="708de-120">Ustvarite poteke dela odobritve za poročila o stroških.</span><span class="sxs-lookup"><span data-stu-id="708de-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="708de-121"><strong>Samodejno knjiženje poročil o stroških</strong></span><span class="sxs-lookup"><span data-stu-id="708de-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="708de-122">Ustvarite poteke dela samodejnega knjiženja za poročila o stroških.</span><span class="sxs-lookup"><span data-stu-id="708de-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="708de-123"><strong>Postavka vrstice stroška</strong></span><span class="sxs-lookup"><span data-stu-id="708de-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="708de-124">Ustvarite poteke dela odobritve za postavke vrstice v poročilih o stroških.</span><span class="sxs-lookup"><span data-stu-id="708de-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="708de-125"><strong>Samodejno knjiženje postavke vrstice stroška</strong></span><span class="sxs-lookup"><span data-stu-id="708de-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="708de-126">Ustvarite poteke dela samodejnih knjiženj za postavke vrstice v poročilih o stroških.</span><span class="sxs-lookup"><span data-stu-id="708de-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="708de-127"><strong>Zahteva za pot</strong></span><span class="sxs-lookup"><span data-stu-id="708de-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="708de-128">Ustvarite poteke dela odobritve za zahteve za pot.</span><span class="sxs-lookup"><span data-stu-id="708de-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="708de-129"><strong>Zahteva za denarni predujem</strong></span><span class="sxs-lookup"><span data-stu-id="708de-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="708de-130">Ustvarite poteke dela odobritve za zahteve za denarni predujem.</span><span class="sxs-lookup"><span data-stu-id="708de-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="708de-131"><strong>Izterjava davka DDV</strong></span><span class="sxs-lookup"><span data-stu-id="708de-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="708de-132">Ustvarite poteke dela odobritve za izterjavo davka na dodano vrednost (DDV).</span><span class="sxs-lookup"><span data-stu-id="708de-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]