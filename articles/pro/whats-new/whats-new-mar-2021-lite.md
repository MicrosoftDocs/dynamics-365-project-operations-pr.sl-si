---
title: Novosti v marcu 2021 – poenostavljeno uvajanje storitve Project Operations
description: Ta tema vsebuje informacije o posodobitvah kakovosti, ki so na voljo v marčevski izdaji (2021) poenostavljenega uvajanja storitve Project Operations.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd1518ef8f5645bace63a222b92cfd16d9c19a21
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500042"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="a0658-103">Novosti v marcu 2021 – poenostavljeno uvajanje storitve Project Operations</span><span class="sxs-lookup"><span data-stu-id="a0658-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="a0658-104">_Velja za: poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="a0658-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a0658-105">Ta tema velja za naslednje komponente in različice aplikacije Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="a0658-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="a0658-106">Project Operations v okolju Dataverse različice 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="a0658-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="a0658-107">Posodobitve kakovosti</span><span class="sxs-lookup"><span data-stu-id="a0658-107">Quality updates</span></span>

| <span data-ttu-id="a0658-108">**Območje funkcij**</span><span class="sxs-lookup"><span data-stu-id="a0658-108">**Feature area**</span></span> | <span data-ttu-id="a0658-109">**Številka sklica**</span><span class="sxs-lookup"><span data-stu-id="a0658-109">**Reference number**</span></span> | <span data-ttu-id="a0658-110">**Posodobitev kakovosti**</span><span class="sxs-lookup"><span data-stu-id="a0658-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a0658-111">Zaračunavanje in cene</span><span class="sxs-lookup"><span data-stu-id="a0658-111">Billing and pricing</span></span> | <span data-ttu-id="a0658-112">2133873</span><span class="sxs-lookup"><span data-stu-id="a0658-112">2133873</span></span> | <span data-ttu-id="a0658-113">Popravljen je prikaz simbola valute za **prodajno ceno na enoto** v mreži **ocen stroškov**.</span><span class="sxs-lookup"><span data-stu-id="a0658-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="a0658-114">Zaračunavanje in cene</span><span class="sxs-lookup"><span data-stu-id="a0658-114">Billing and pricing</span></span> | <span data-ttu-id="a0658-115">2174616</span><span class="sxs-lookup"><span data-stu-id="a0658-115">2174616</span></span> | <span data-ttu-id="a0658-116">Ko je ponudba pridobljena, je v podrobnostih pogodbe, ki se kopirajo iz ponudbe, sklic na pogodbi prilagojen cenik.</span><span class="sxs-lookup"><span data-stu-id="a0658-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="a0658-117">Upravljanje priložnosti</span><span class="sxs-lookup"><span data-stu-id="a0658-117">Opportunity Management</span></span> | <span data-ttu-id="a0658-118">2167475</span><span class="sxs-lookup"><span data-stu-id="a0658-118">2167475</span></span> | <span data-ttu-id="a0658-119">Popravljen je znesek davka na popravljenem računu, iz katerega izvira neobračunan dejanski vnos.</span><span class="sxs-lookup"><span data-stu-id="a0658-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="a0658-120">Upravljanje priložnosti</span><span class="sxs-lookup"><span data-stu-id="a0658-120">Opportunity Management</span></span> | <span data-ttu-id="a0658-121">2176285</span><span class="sxs-lookup"><span data-stu-id="a0658-121">2176285</span></span> | <span data-ttu-id="a0658-122">Zneska davka ni dovoljeno kopirati iz podrobnosti prodajne pogodbe/ponudbe v stroškovne podrobnosti  pogodbe/ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a0658-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="a0658-123">Upravljanje priložnosti</span><span class="sxs-lookup"><span data-stu-id="a0658-123">Opportunity Management</span></span> | <span data-ttu-id="a0658-124">2188079</span><span class="sxs-lookup"><span data-stu-id="a0658-124">2188079</span></span> | <span data-ttu-id="a0658-125">Pravilo za izstavitev deljenega računa ne sme biti ustvarjeno za pogodbe, ki ne temeljijo na delu.</span><span class="sxs-lookup"><span data-stu-id="a0658-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="a0658-126">Načrtovanje in sledenje</span><span class="sxs-lookup"><span data-stu-id="a0658-126">Planning and Tracking</span></span> | <span data-ttu-id="a0658-127">2138853</span><span class="sxs-lookup"><span data-stu-id="a0658-127">2138853</span></span> | <span data-ttu-id="a0658-128">Funkcija kopiranja projekta je posodobljena za zagotavljanje kopiranja vrstic za oceno stroškov, ki se sklicujejo na opravila, v ciljni projekt.</span><span class="sxs-lookup"><span data-stu-id="a0658-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="a0658-129">Načrtovanje in sledenje</span><span class="sxs-lookup"><span data-stu-id="a0658-129">Planning and Tracking</span></span> | <span data-ttu-id="a0658-130">2173259</span><span class="sxs-lookup"><span data-stu-id="a0658-130">2173259</span></span> | <span data-ttu-id="a0658-131">Funkcija kopiranja projekta je posodobljena, da se v nekaterih primerih ne prikaže sporočilo o napaki **kopiranja WBS**.</span><span class="sxs-lookup"><span data-stu-id="a0658-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="a0658-132">Čas in strošek</span><span class="sxs-lookup"><span data-stu-id="a0658-132">Time and Expense</span></span> | <span data-ttu-id="a0658-133">2148910</span><span class="sxs-lookup"><span data-stu-id="a0658-133">2148910</span></span> | <span data-ttu-id="a0658-134">V mreži **časovnih vnosov** je odpravljena težava s stranjo za **urejanje vnosov**.</span><span class="sxs-lookup"><span data-stu-id="a0658-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="a0658-135">Čas in strošek</span><span class="sxs-lookup"><span data-stu-id="a0658-135">Time and Expense</span></span> | <span data-ttu-id="a0658-136">2159798</span><span class="sxs-lookup"><span data-stu-id="a0658-136">2159798</span></span> | <span data-ttu-id="a0658-137">Poostren je nadzor za preprečevanje urejanja odobrenih vnosov stroškov.</span><span class="sxs-lookup"><span data-stu-id="a0658-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


