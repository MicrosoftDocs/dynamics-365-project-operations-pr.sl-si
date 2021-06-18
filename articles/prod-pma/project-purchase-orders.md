---
title: Naročilnice za projekt
description: V tem članku so opisane različne metode, s katerimi lahko ustvarite naročilnice za projekt. Uporabljena metoda je odvisna od namena naročilnice in od tega, kdaj se kupljeni artikli uporabijo in zaračunajo za projekt.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c3ce2d0c0fb3cecf22157db5cb37eb744027d0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999376"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="3013b-104">Naročilnice za projekt</span><span class="sxs-lookup"><span data-stu-id="3013b-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3013b-105">V tem članku so opisane različne metode, s katerimi lahko ustvarite naročilnice za projekt.</span><span class="sxs-lookup"><span data-stu-id="3013b-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="3013b-106">Uporabljena metoda je odvisna od namena naročilnice in od tega, kdaj se kupljeni artikli uporabijo in zaračunajo za projekt.</span><span class="sxs-lookup"><span data-stu-id="3013b-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="3013b-107">Metode za ustvarjanje naročilnice</span><span class="sxs-lookup"><span data-stu-id="3013b-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="3013b-108">Za ustvarjanje naročilnice v območju »Vodenje projektov in računovodstvo« lahko uporabite eno od spodnjih metod.</span><span class="sxs-lookup"><span data-stu-id="3013b-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="3013b-109">Namen naročilnice določa, kdaj je naročilnica uporabljena in kdaj se zaračunajo artikli za projekt.</span><span class="sxs-lookup"><span data-stu-id="3013b-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3013b-110">Način</span><span class="sxs-lookup"><span data-stu-id="3013b-110">Method</span></span></th>
<th><span data-ttu-id="3013b-111">Namen</span><span class="sxs-lookup"><span data-stu-id="3013b-111">Purpose</span></span></th>
<th><span data-ttu-id="3013b-112">Poraba izdelkov</span><span class="sxs-lookup"><span data-stu-id="3013b-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3013b-113">Ustvarite naročilnico neposredno iz projekta.</span><span class="sxs-lookup"><span data-stu-id="3013b-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="3013b-114">To metodo uporabite za nakup artiklov od zunanjega dobavitelja za uporabo v projektu.</span><span class="sxs-lookup"><span data-stu-id="3013b-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="3013b-115">Naročilnico lahko ustvarite na dva načina:</span><span class="sxs-lookup"><span data-stu-id="3013b-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="3013b-116">V samem projektu.</span><span class="sxs-lookup"><span data-stu-id="3013b-116">From the project itself.</span></span> <span data-ttu-id="3013b-117">V tem primeru je projekt že opredeljen za naročilnico.</span><span class="sxs-lookup"><span data-stu-id="3013b-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="3013b-118">Tako da poiščete in odprete naročilnico projekta.</span><span class="sxs-lookup"><span data-stu-id="3013b-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="3013b-119">Za izdelavo naročilnice morate izbrati dobavitelja in projekt, za katerega jo želite ustvariti.</span><span class="sxs-lookup"><span data-stu-id="3013b-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="3013b-120">Izdelki se porabijo, ko se posodobi račun dobavitelja.</span><span class="sxs-lookup"><span data-stu-id="3013b-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3013b-121">Ustvarite naročilnico iz prodajnega naloga.</span><span class="sxs-lookup"><span data-stu-id="3013b-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="3013b-122">To metodo uporabite za nakup artiklov, ko ustvarite prodajni nalog iz projekta.</span><span class="sxs-lookup"><span data-stu-id="3013b-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="3013b-123">Izdelki se porabijo, ko je stranki zaračunan prodajni nalog.</span><span class="sxs-lookup"><span data-stu-id="3013b-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3013b-124">Ustvarite naročilnico iz zahteve za izdelek.</span><span class="sxs-lookup"><span data-stu-id="3013b-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="3013b-125">To metodo uporabite za nakup artiklov, ko ustvarite zahtevo za artikel iz projekta.</span><span class="sxs-lookup"><span data-stu-id="3013b-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="3013b-126">Izdelki se porabijo s posodobitvijo odpremnice za zahtevo za izdelek.</span><span class="sxs-lookup"><span data-stu-id="3013b-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="3013b-127">Ko posodobite račun dobavitelja ali odpremnico, morate posodobiti tudi odpremnico v zahtevi za artikel.</span><span class="sxs-lookup"><span data-stu-id="3013b-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="3013b-128">Za več informacij glejte [Prejemanje izdelkov, ki so navedeni v naročilu, v okviru zahteve po izdelku](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="3013b-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]