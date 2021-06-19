---
title: Potek dela upravljanja stroškov
description: Ta tema pojasnjuje, kako lahko uporabljate sistem poteka dela v aplikaciji Microsoft Dynamics 365 Finance, da vzpostavite postopek pregleda poročil o stroških v aplikaciji za upravljanje stroškov.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51ac2712f62d5c5d85b21c0ea929517ccb893bca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005226"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="42188-103">Potek dela upravljanja stroškov</span><span class="sxs-lookup"><span data-stu-id="42188-103">Expense management workflow</span></span>

<span data-ttu-id="42188-104">Sistem poteka dela lahko uporabite, da vzpostavite postopek pregleda poročil o stroških v aplikaciji za upravljanje stroškov.</span><span class="sxs-lookup"><span data-stu-id="42188-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="42188-105">Nastavite lahko potek dela, ki uporablja naslednja merila za določanje odobriteljev poročil o stroških:</span><span class="sxs-lookup"><span data-stu-id="42188-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="42188-106">Hierarhija poročanja zaposlenih in vnaprej določene omejitve odobritve</span><span class="sxs-lookup"><span data-stu-id="42188-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="42188-107">Večstopenjska odobritev, ki podpira začasne in končne odobritelje</span><span class="sxs-lookup"><span data-stu-id="42188-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="42188-108">Finančne razsežnosti in projektna odgovornost</span><span class="sxs-lookup"><span data-stu-id="42188-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="42188-109">Dodelitev določenim uporabnikom ali uporabniškim skupinam</span><span class="sxs-lookup"><span data-stu-id="42188-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="42188-110">Odobritve potekov dela je mogoče ustvariti za poročila o stroških, zahteve za pot, denarne predujme in izterjavo davka na dodano vrednost (DDV).</span><span class="sxs-lookup"><span data-stu-id="42188-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="42188-111">**Primer**</span><span class="sxs-lookup"><span data-stu-id="42188-111">**Example**</span></span>

<span data-ttu-id="42188-112">Spodnji proces prikazuje primer poteka dela upravljanja stroškov za poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="42188-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="42188-113">Zaposleni ustvari in shrani poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="42188-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="42188-114">Zaposleni pošlje poročilo o stroških v odobritev.</span><span class="sxs-lookup"><span data-stu-id="42188-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="42188-115">Odobritelj je določen na podlagi pravil, ki so bila določena ob nastavitvi poteka dela.</span><span class="sxs-lookup"><span data-stu-id="42188-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="42188-116">Odobritelj prejme obvestilo, da je poročilo o stroških pripravljeno na odobritev.</span><span class="sxs-lookup"><span data-stu-id="42188-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="42188-117">Odobritelj pregleda poročilo o stroških in preveri, ali so izpolnjeni naslednji pogoji:</span><span class="sxs-lookup"><span data-stu-id="42188-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="42188-118">Stroški ne kršijo nobenega pravilnika o stroških.</span><span class="sxs-lookup"><span data-stu-id="42188-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="42188-119">Če stroški kršijo pravilnik, odobritelj preveri, ali poročilo o stroških vključuje veljavno poslovno utemeljitev.</span><span class="sxs-lookup"><span data-stu-id="42188-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="42188-120">Elektronski računi so priloženi poročilu o stroških.</span><span class="sxs-lookup"><span data-stu-id="42188-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="42188-121">Odobritelj odobri poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="42188-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="42188-122">Poročilo o stroških je dodeljeno koordinatorju obveznosti za knjiženje.</span><span class="sxs-lookup"><span data-stu-id="42188-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="42188-123">Izvede se eden od naslednjih korakov (odvisno od tega, ali je konfigurirano samodejno knjiženje ali ne):</span><span class="sxs-lookup"><span data-stu-id="42188-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="42188-124">Če je konfigurirano samodejno knjiženje, se poročilo o stroških obdela za plačilo in posodobi stanje poročila o stroških.</span><span class="sxs-lookup"><span data-stu-id="42188-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="42188-125">Če samodejno knjiženje ni konfigurirano, koordinator obveznosti preveri, ali so bili predloženi vsi izvirni računi in ali so računi usklajeni s stroški v poročilu o stroških.</span><span class="sxs-lookup"><span data-stu-id="42188-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="42188-126">Vse davčne številke, ki so vpisane v poročilo o stroških, morajo biti preverjene.</span><span class="sxs-lookup"><span data-stu-id="42188-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="42188-127">Ko so te zahteve preverjene, se poročilo o stroških vknjiži.</span><span class="sxs-lookup"><span data-stu-id="42188-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="42188-128">Ko je poročilo o stroških vknjiženo, se zanj odobri plačilo, zaposlenemu pa povrnejo stroški.</span><span class="sxs-lookup"><span data-stu-id="42188-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]