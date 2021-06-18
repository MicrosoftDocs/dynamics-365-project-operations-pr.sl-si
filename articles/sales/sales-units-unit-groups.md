---
title: Enote in skupine enot
description: Ta tema vsebuje informacije o tem, kako v aplikaciji Dynamics 365 Project Operations ustvariti enote in skupine enot.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 646e20189efb4aab56972f01a52b1bff19f2e79f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996091"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="7c17f-103">Enote in skupine enot</span><span class="sxs-lookup"><span data-stu-id="7c17f-103">Units and unit groups</span></span>

<span data-ttu-id="7c17f-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="7c17f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7c17f-105">Enote so količine ali meritve, v katerih prodajate svoje izdelke ali storitve.</span><span class="sxs-lookup"><span data-stu-id="7c17f-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="7c17f-106">Če na primer prodajate vrtnarske izdelke, lahko semena prodajate v enotah, kot so paketi, škatle in palete.</span><span class="sxs-lookup"><span data-stu-id="7c17f-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="7c17f-107">Skupina enot je zbirka teh različnih enot.</span><span class="sxs-lookup"><span data-stu-id="7c17f-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="7c17f-108">Za izvedbo korakov v tej temi, se prepričajte, da imate dodeljeno vlogo skrbnika sistema ali upravitelja za Sales Professional ali pa imate enakovredna dovoljenja.</span><span class="sxs-lookup"><span data-stu-id="7c17f-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="7c17f-109">Ustvarjanje skupine enot</span><span class="sxs-lookup"><span data-stu-id="7c17f-109">Create a unit group</span></span>

1. <span data-ttu-id="7c17f-110">Na zemljevidu mesta izberite **Enote**.</span><span class="sxs-lookup"><span data-stu-id="7c17f-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="7c17f-111">Izberite **Novo** in v pogovornem oknu **Ustvari skupino enot** vnesite ime enote.</span><span class="sxs-lookup"><span data-stu-id="7c17f-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="7c17f-112">V polje **Glavna enota** vnesite najmanjšo skupno mersko enoto, v kateri se bo izdelek prodajal.</span><span class="sxs-lookup"><span data-stu-id="7c17f-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="7c17f-113">Na primer, lahko vnesete »kos« ali »unča«.</span><span class="sxs-lookup"><span data-stu-id="7c17f-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="7c17f-114">Izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="7c17f-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="7c17f-115">Dodajanje enot v skupino enot</span><span class="sxs-lookup"><span data-stu-id="7c17f-115">Add units to a unit group</span></span>

1. <span data-ttu-id="7c17f-116">Odprite skupino enot in na zavihku **Sorodno** izberite **Enote**.</span><span class="sxs-lookup"><span data-stu-id="7c17f-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="7c17f-117">Videli boste, da je glavna enota že dodana.</span><span class="sxs-lookup"><span data-stu-id="7c17f-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="7c17f-118">Izberite **Dodaj novo enoto**, nato pa na strani **Hitro ustvarjanje: enota** v polje **Ime** vnesite ime enote.</span><span class="sxs-lookup"><span data-stu-id="7c17f-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="7c17f-119">V polje **Količina** vnesite količino, ki jo bo enota vsebovala.</span><span class="sxs-lookup"><span data-stu-id="7c17f-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="7c17f-120">Če sta v škatli na primer dva kosa, vnesite »2«.</span><span class="sxs-lookup"><span data-stu-id="7c17f-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="7c17f-121">V polju **Osnovna enota** izberite osnovno enoto za vzpostavitev najmanjše merske enote za enoto.</span><span class="sxs-lookup"><span data-stu-id="7c17f-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="7c17f-122">Na primer, lahko izberete »Kos«.</span><span class="sxs-lookup"><span data-stu-id="7c17f-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="7c17f-123">Izberite **Shrani**:</span><span class="sxs-lookup"><span data-stu-id="7c17f-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]