---
title: Nabori odobritev
description: Ta tema zagotavlja informacije o naboru odobritev, zahtevah in podmnožicah teh postopkov.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116891"
---
# <a name="approval-sets"></a><span data-ttu-id="8ed1d-103">Nabori odobritev</span><span class="sxs-lookup"><span data-stu-id="8ed1d-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8ed1d-104">Nabori odobritev združujejo zahtev za odobritev v manjše podskupine postopkov.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="8ed1d-105">To združevanje omogoča obdelavo odobritev po vrstnem redu po projektu ter vnovični poskus in upoštevanje vrstnega reda.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="8ed1d-106">Združevanj izboljšuje zanesljivost in sledljivost obdelave odobritev za velike količine odobritev.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="8ed1d-107">Nabori odobritev kažejo splošno stanje obdelave njihovih povezanih zapisov.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="8ed1d-108">Ko je zapis odobritve obdelan z naborom odobritve, se zapis premakne iz **Oddano** v **Odobreno** in je ločen od nabora odobritev.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="8ed1d-109">Če zapis ne uspe, ko je predložen v odobritev, ostane v stanju **Oddano**, nabor odobritev pa je označen kot neuspešen.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="8ed1d-110">Nabor odobritev zabeleži sporočilo o napaki.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="8ed1d-111">Obdelava odobritev in naborov odobritev</span><span class="sxs-lookup"><span data-stu-id="8ed1d-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="8ed1d-112">Odobritve, ki so v čakalni vrsti za obdelavo, so vidne v pogledu **Obdelava odobritev**.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="8ed1d-113">Sistem poskuša večkrat asinhrono obdelati vse vnose, vključno z vnovičnim poskusom odobritve, če prejšnji poskusi niso uspeli.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="8ed1d-114">Polke **Življenjska doba nabora odobritev** beleži število poskusov obdelave niza, preden je označen kot neuspešen.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="8ed1d-115">Neuspešne odobritve in nabori odobritev</span><span class="sxs-lookup"><span data-stu-id="8ed1d-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="8ed1d-116">Pogled **Neuspešne odobritve** navaja vse odobritve, ki zahtevajo posredovanje uporabnika.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="8ed1d-117">Odprite povezane dnevnike nabora odobritev, da ugotovite vzrok napake.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="8ed1d-118">Z izbiro možnosti **Poskusi znova** se doda številu življenjske dobe nabora odobritev, premakne nabor odobritev nazaj v stanje **Obdelava** in poskuša obdelati preostale zapise.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="8ed1d-119">Konfiguracija naborov odobritev</span><span class="sxs-lookup"><span data-stu-id="8ed1d-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="8ed1d-120">Omogočite funkcijo Nabori odobritev</span><span class="sxs-lookup"><span data-stu-id="8ed1d-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="8ed1d-121">Preden omogočite funkcijo Nabori odobritev, preverite, ali se trenutno ne obdeluje nobena odobritev.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="8ed1d-122">Pojdite na stran **Projektni parametri** in izberite možnost **Nadzor funkcij** > **Omogoči sodobne odobritve**.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="8ed1d-123">Izklop funkcije Nabori odobritev</span><span class="sxs-lookup"><span data-stu-id="8ed1d-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="8ed1d-124">Preden izklopite funkcijo Nabori odobritev, preverite, ali se trenutno ne obdeluje nobena odobritev.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="8ed1d-125">Pojdite na stran **Projektni parametri** in izberite možnost **Nadzor funkcij** > **Onemogoči sodobne odobritve**.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="8ed1d-126">Konfiguriranje asinhronega praga</span><span class="sxs-lookup"><span data-stu-id="8ed1d-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="8ed1d-127">Ko se nabori odobritev ustvarijo, se obdelava premakne v ozadje, ko izbrano število zapisov za odobritev preseže navedeni prag.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="8ed1d-128">Uporabite polje **Asinhroni prag** za konfiguracijo, kdaj naj se obdelava odobritve izvaja sinhrono ali asinhrono.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="8ed1d-129">Veljavne vrednosti so:</span><span class="sxs-lookup"><span data-stu-id="8ed1d-129">Valid values are:</span></span>

  - <span data-ttu-id="8ed1d-130">Nič: vse zahteve naj se obdelajo asinhrono.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="8ed1d-131">Številke, večje od nič: odobritve se obdelujejo asinhrono le, če predloženo število odobritev preseže to vrednost.</span><span class="sxs-lookup"><span data-stu-id="8ed1d-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
