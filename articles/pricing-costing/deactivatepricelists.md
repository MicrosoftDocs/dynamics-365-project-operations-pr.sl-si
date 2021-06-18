---
title: Deaktivacija cenikov
description: Ta tema pojasnjuje, kako deaktivirati ali odstraniti neuporabljene ali stare cenike.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001356"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="dc0b0-103">Deaktivacija cenikov</span><span class="sxs-lookup"><span data-stu-id="dc0b0-103">Deactivate price lists</span></span> 

<span data-ttu-id="dc0b0-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="dc0b0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dc0b0-105">Če želite odstraniti stare ali neuporabljene cenike iz storitve Dynamics 365 Project Operations, morate opraviti dva koraka.</span><span class="sxs-lookup"><span data-stu-id="dc0b0-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="dc0b0-106">Odstranite ali izbrišite cenik z določenih strani.</span><span class="sxs-lookup"><span data-stu-id="dc0b0-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="dc0b0-107">Deaktivirajte ali izbrišite cenik iz aktivnih cenikov na strani **Ceniki**.</span><span class="sxs-lookup"><span data-stu-id="dc0b0-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="dc0b0-108">Za popolno odstranitev cenika morate opraviti oba koraka.</span><span class="sxs-lookup"><span data-stu-id="dc0b0-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="dc0b0-109">Izvedba izključno 2. koraka, torej neposrednega brisanja ali deaktiviranja cenika iz pogleda »Aktivni ceniki«, ni dovolj.</span><span class="sxs-lookup"><span data-stu-id="dc0b0-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="dc0b0-110">Povezavo tega cenika morate izbrisati tudi iz vseh krajev, omenjenih v 1. koraku.</span><span class="sxs-lookup"><span data-stu-id="dc0b0-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="dc0b0-111">Izbrišite cenik z določenih strani</span><span class="sxs-lookup"><span data-stu-id="dc0b0-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="dc0b0-112">Če želite izbrisati cenik iz aplikacije Project Operations, pojdite na naslednje strani:</span><span class="sxs-lookup"><span data-stu-id="dc0b0-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="dc0b0-113">Stran **Projektni parametri** > zavihek **Ceniki**</span><span class="sxs-lookup"><span data-stu-id="dc0b0-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="dc0b0-114">Stran **Organizacijska enota** > mreža **Ceniki**</span><span class="sxs-lookup"><span data-stu-id="dc0b0-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="dc0b0-115">stran **Kupec** > mreža **Ceniki projekta**</span><span class="sxs-lookup"><span data-stu-id="dc0b0-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="dc0b0-116">Stran **Projektne ponudbe** > mreža **Ceniki projektov**: to velja za vse aktivne projektne ponudbe.</span><span class="sxs-lookup"><span data-stu-id="dc0b0-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="dc0b0-117">Stran **Projektne pogodbe** > mreža **Ceniki projektov**: to velja za vse aktivne projektne pogodbe.</span><span class="sxs-lookup"><span data-stu-id="dc0b0-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="dc0b0-118">Za vsako stran morate izbrati cenik, ki ga želite izbrisati, in nato izbrati **Izbriši**.</span><span class="sxs-lookup"><span data-stu-id="dc0b0-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="dc0b0-119">Brisanje ali deaktivacija cenika iz aktivnih cenikov na strani »Ceniki«</span><span class="sxs-lookup"><span data-stu-id="dc0b0-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="dc0b0-120">Če želite izbrisati cenik iz aktivnih cenikov, pojdite v **Prodaja** > **Stranke** > **Ceniki**.</span><span class="sxs-lookup"><span data-stu-id="dc0b0-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="dc0b0-121">Izberite cenike, ki jih želite izbrisati, in izberite **Izbriši**.</span><span class="sxs-lookup"><span data-stu-id="dc0b0-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="dc0b0-122">Če se cenik sklicuje na katero koli obstoječo transakcijo, ga ne boste mogli izbrisati.</span><span class="sxs-lookup"><span data-stu-id="dc0b0-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="dc0b0-123">Če se to zgodi, lahko deaktivirate cenik, tako da se ne prikaže v nobenem pogledu.</span><span class="sxs-lookup"><span data-stu-id="dc0b0-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="dc0b0-124">Če želite deaktivirati cenik, znova izberite cenik in nato **Deaktiviraj**.</span><span class="sxs-lookup"><span data-stu-id="dc0b0-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
