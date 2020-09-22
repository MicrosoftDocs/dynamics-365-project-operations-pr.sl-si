---
title: Prejemanje izdelkov, ki so navedeni v naročilu, v okviru zahteve po izdelku
description: Ta tema pojasnjuje, kako sprejeti izdelke, navedene v naročilu, v okviru zahteve po izdelku.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755731"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="0d39e-103">Prejemanje izdelkov, ki so navedeni v naročilu, v okviru zahteve po izdelku</span><span class="sxs-lookup"><span data-stu-id="0d39e-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0d39e-104">Ta tema pojasnjuje, kako sprejeti izdelke, navedene v naročilu, v okviru zahteve po izdelku.</span><span class="sxs-lookup"><span data-stu-id="0d39e-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="0d39e-105">S tem ko namesto transakcije izdelka uporabite zahtevo po izdelku, lahko načrtujete dostavo tik pred dejansko uporabo izdelka, ustvarite naročilo, vključite izdelek v ogrodje trgovinskega sporazuma in zahtevo po izdelku vključite v načrtovanje proizvodnje.</span><span class="sxs-lookup"><span data-stu-id="0d39e-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="0d39e-106">To opravilo uporablja nabor podatkov USSI.</span><span class="sxs-lookup"><span data-stu-id="0d39e-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="0d39e-107">V podoknu za krmarjenje pojdite na **Moduli > Vodenje projekta in računovodstvo > Projekti > Vsi projekti**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="0d39e-108">Na seznamu izberite povezavo v želeni vrstici.</span><span class="sxs-lookup"><span data-stu-id="0d39e-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="0d39e-109">V podoknu za dejanja izberite **Načrtovanje**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="0d39e-110">Izberite **Zahteve po izdelku**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="0d39e-111">Izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-111">Select **New**.</span></span>
6. <span data-ttu-id="0d39e-112">V novo vrstico vnesite ali izberite vrednost v polje **Številka izdelka**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="0d39e-113">Vnesite številko v polje **Količina**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="0d39e-114">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-114">Select **Save**.</span></span>
9. <span data-ttu-id="0d39e-115">V podoknu za dejanja izberite **Upravljanje**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="0d39e-116">Izberite **Funkcije**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-116">Select **Functions**.</span></span>
11. <span data-ttu-id="0d39e-117">Izberite **Ustvarjanje naročila**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="0d39e-118">Izberite potrditveno polje **Vključi vse**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="0d39e-119">V polje **Račun prodajalca** vnesite ali izberite vrednost.</span><span class="sxs-lookup"><span data-stu-id="0d39e-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="0d39e-120">Izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-120">Select **OK**.</span></span>
15. <span data-ttu-id="0d39e-121">V podoknu za krmarjenje pojdite na **Moduli > Obveznosti > Naročila > Vsa naročila**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="0d39e-122">Na seznamu izberite povezavo v želeni vrstici.</span><span class="sxs-lookup"><span data-stu-id="0d39e-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="0d39e-123">V podoknu za dejanja izberite **Nakup**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="0d39e-124">Izberite **Potrdi**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="0d39e-125">V podoknu za dejanja izberite **Prejem**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="0d39e-126">Izberite **Potrdilo izdelka**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="0d39e-127">Vnesite vrednost v polje **Potrdilo izdelka**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="0d39e-128">Izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="0d39e-128">Select **OK**.</span></span>

