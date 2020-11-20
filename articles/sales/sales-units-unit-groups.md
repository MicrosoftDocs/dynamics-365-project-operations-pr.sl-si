---
title: Enote in skupine enot
description: Ta tema vsebuje informacije o tem, kako ustvariti enote in skupine enot v storitvi Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 3f588e41d001befeac87bb6a4e28a83cf5cfa865
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131048"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="18680-103">Enote in skupine enot</span><span class="sxs-lookup"><span data-stu-id="18680-103">Units and unit groups</span></span>

<span data-ttu-id="18680-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="18680-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="18680-105">Enote so količine ali meritve, v katerih prodajate svoje izdelke ali storitve.</span><span class="sxs-lookup"><span data-stu-id="18680-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="18680-106">Če na primer prodajate vrtnarske izdelke, lahko semena prodajate v enotah, kot so paketi, škatle in palete.</span><span class="sxs-lookup"><span data-stu-id="18680-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="18680-107">Skupina enot je zbirka teh različnih enot.</span><span class="sxs-lookup"><span data-stu-id="18680-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="18680-108">Za izvedbo korakov v tej temi, se prepričajte, da imate dodeljeno vlogo skrbnika sistema ali upravitelja za Sales Professional ali pa imate enakovredna dovoljenja.</span><span class="sxs-lookup"><span data-stu-id="18680-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="18680-109">Ustvarjanje skupine enot</span><span class="sxs-lookup"><span data-stu-id="18680-109">Create a unit group</span></span>

1. <span data-ttu-id="18680-110">Na zemljevidu mesta izberite **Enote**.</span><span class="sxs-lookup"><span data-stu-id="18680-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="18680-111">Izberite **Novo** in v pogovornem oknu **Ustvari skupino enot** vnesite ime enote.</span><span class="sxs-lookup"><span data-stu-id="18680-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="18680-112">V polje **Glavna enota** vnesite najmanjšo skupno mersko enoto, v kateri se bo izdelek prodajal.</span><span class="sxs-lookup"><span data-stu-id="18680-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="18680-113">Na primer, lahko vnesete »kos« ali »unča«.</span><span class="sxs-lookup"><span data-stu-id="18680-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="18680-114">Izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="18680-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="18680-115">Dodajanje enot v skupino enot</span><span class="sxs-lookup"><span data-stu-id="18680-115">Add units to a unit group</span></span>

1. <span data-ttu-id="18680-116">Odprite skupino enot in na zavihku **Sorodno** izberite **Enote**.</span><span class="sxs-lookup"><span data-stu-id="18680-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="18680-117">Videli boste, da je glavna enota že dodana.</span><span class="sxs-lookup"><span data-stu-id="18680-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="18680-118">Izberite **Dodaj novo enoto**, nato pa na strani **Hitro ustvarjanje: enota** v polje **Ime** vnesite ime enote.</span><span class="sxs-lookup"><span data-stu-id="18680-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="18680-119">V polje **Količina** vnesite količino, ki jo bo enota vsebovala.</span><span class="sxs-lookup"><span data-stu-id="18680-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="18680-120">Če sta v škatli na primer dva kosa, vnesite »2«.</span><span class="sxs-lookup"><span data-stu-id="18680-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="18680-121">V polju **Osnovna enota** izberite osnovno enoto za vzpostavitev najmanjše merske enote za enoto.</span><span class="sxs-lookup"><span data-stu-id="18680-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="18680-122">Na primer, lahko izberete »Kos«.</span><span class="sxs-lookup"><span data-stu-id="18680-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="18680-123">Izberite **Shrani**:</span><span class="sxs-lookup"><span data-stu-id="18680-123">Select **Save**:</span></span>
