---
title: Rezervacija v projekt
description: Ta tema vsebuje informacije o tem, kako rezervirati vir v projekt.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908613"
---
# <a name="book-to-a-project"></a><span data-ttu-id="d49cb-103">Rezervacija v projekt</span><span class="sxs-lookup"><span data-stu-id="d49cb-103">Book to a project</span></span>

<span data-ttu-id="d49cb-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="d49cb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d49cb-105">Včasih mora vodja projektov ali upravitelj virov dodeliti vir projektu, ne da bi bila določena posebna zahteva splošnega člana ekipe.</span><span class="sxs-lookup"><span data-stu-id="d49cb-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="d49cb-106">To lahko dosežete na enega od treh načinov.</span><span class="sxs-lookup"><span data-stu-id="d49cb-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="d49cb-107">Dodajanje rezervacij na mreži člana ekipe</span><span class="sxs-lookup"><span data-stu-id="d49cb-107">Book from the team member grid</span></span>
- <span data-ttu-id="d49cb-108">Dodajanje rezervacij na plošči razporeda</span><span class="sxs-lookup"><span data-stu-id="d49cb-108">Book from the schedule board</span></span>
- <span data-ttu-id="d49cb-109">Dodajanje rezervacij iz obrazca **projekta**</span><span class="sxs-lookup"><span data-stu-id="d49cb-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="d49cb-110">Dodajanje rezervacij na mreži člana ekipe</span><span class="sxs-lookup"><span data-stu-id="d49cb-110">Book from the team member grid</span></span>

<span data-ttu-id="d49cb-111">Če vaša organizacija deluje v hibridnem načinu dodeljevanja virov, lahko upravitelj projekta vir rezervira neposredno v projekt tako, da izvede naslednje korake.</span><span class="sxs-lookup"><span data-stu-id="d49cb-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="d49cb-112">V projektu pojdite na mrežo članov ekipe in izberite možnost **Novo**.</span><span class="sxs-lookup"><span data-stu-id="d49cb-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="d49cb-113">Določite ime položaja in vlogo vira.</span><span class="sxs-lookup"><span data-stu-id="d49cb-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="d49cb-114">S seznama izberite vir, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="d49cb-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="d49cb-115">Ko izberete vir, določite vrednosti za naslednja polja, da ga rezervirate:</span><span class="sxs-lookup"><span data-stu-id="d49cb-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="d49cb-116">Začetni datum</span><span class="sxs-lookup"><span data-stu-id="d49cb-116">Start date</span></span>
    - <span data-ttu-id="d49cb-117">Datum zaključka</span><span class="sxs-lookup"><span data-stu-id="d49cb-117">Finish date</span></span>
    - <span data-ttu-id="d49cb-118">Način dodelitve</span><span class="sxs-lookup"><span data-stu-id="d49cb-118">Allocation method</span></span>
    - <span data-ttu-id="d49cb-119">Ure, če je primerno</span><span class="sxs-lookup"><span data-stu-id="d49cb-119">Hours, if applicable</span></span>
    - <span data-ttu-id="d49cb-120">Odobritelj projekta</span><span class="sxs-lookup"><span data-stu-id="d49cb-120">Project approver</span></span>

6. <span data-ttu-id="d49cb-121">Izberite možnost **Shrani in zapri**.</span><span class="sxs-lookup"><span data-stu-id="d49cb-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="d49cb-122">Dodajanje rezervacij na plošči razporeda</span><span class="sxs-lookup"><span data-stu-id="d49cb-122">Book from the schedule board</span></span>

<span data-ttu-id="d49cb-123">Kadar mora upravitelj virov vir rezervirati neposredno v projekt, lahko uporabi ploščo razporeda in zahtevo za projekt.</span><span class="sxs-lookup"><span data-stu-id="d49cb-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="d49cb-124">Zahteva projekta je zahteva za vire, katero je vedno mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="d49cb-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="d49cb-125">Za rezervacijo vira neposredno v obrazec projekta na plošči razporeda dokončajte spodnje korake.</span><span class="sxs-lookup"><span data-stu-id="d49cb-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="d49cb-126">Pomaknite se do plošče razporeda in na levi strani filtrirajte vire, ki so primerni za zahtevo.</span><span class="sxs-lookup"><span data-stu-id="d49cb-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="d49cb-127">V spodnjem podoknu izberite zavihek **Projekt** za ogled seznama projektnih zahtev.</span><span class="sxs-lookup"><span data-stu-id="d49cb-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="d49cb-128">Povlecite zahtevo na vir in določite vrednost naslednjih podatkov:</span><span class="sxs-lookup"><span data-stu-id="d49cb-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="d49cb-129">Začetni datum</span><span class="sxs-lookup"><span data-stu-id="d49cb-129">Start date</span></span>
    - <span data-ttu-id="d49cb-130">Datum zaključka</span><span class="sxs-lookup"><span data-stu-id="d49cb-130">Finish date</span></span>
    - <span data-ttu-id="d49cb-131">Stanje rezervacije</span><span class="sxs-lookup"><span data-stu-id="d49cb-131">Booking status</span></span>
    - <span data-ttu-id="d49cb-132">Način rezervacije</span><span class="sxs-lookup"><span data-stu-id="d49cb-132">Booking method</span></span>
    - <span data-ttu-id="d49cb-133">Trajanje</span><span class="sxs-lookup"><span data-stu-id="d49cb-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="d49cb-134">Dodajanje rezervacij iz obrazca projekta</span><span class="sxs-lookup"><span data-stu-id="d49cb-134">Book from the Project form</span></span>

<span data-ttu-id="d49cb-135">Kot vodja projekta boste morda morali rezervirati vir za projekt, za katerega poznate le merila, ne pa tudi imena.</span><span class="sxs-lookup"><span data-stu-id="d49cb-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="d49cb-136">Dokončajte naslednje korake, če želite s pomočjo pomočnika za razporejanje poiskati vir na podlagi katerih koli razpoložljivih atributov vira.</span><span class="sxs-lookup"><span data-stu-id="d49cb-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="d49cb-137">Pomaknite se do projekta in izberite možnost **Rezerviraj**, da odprete pomočnika za razporejanje.</span><span class="sxs-lookup"><span data-stu-id="d49cb-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="d49cb-138">S filtri na levi strani pomočnika za razporejanje zožite merila in izberite možnost **Išči.**</span><span class="sxs-lookup"><span data-stu-id="d49cb-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="d49cb-139">Na podlagi virov, vrnjenih v rezultatih iskanja, lahko rezervirate vir.</span><span class="sxs-lookup"><span data-stu-id="d49cb-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="d49cb-140">Ta način ne ustvari nobenih rezervacij za vir.</span><span class="sxs-lookup"><span data-stu-id="d49cb-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="d49cb-141">Namesto tega je vir dodan v ekipo.</span><span class="sxs-lookup"><span data-stu-id="d49cb-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="d49cb-142">Potem ko je član ekipe dodan v projekt, lahko vodja projekta z vzdrževanjem rezervacij ali podaljšanjem rezervacij doda zahtevane rezervacije v vir.</span><span class="sxs-lookup"><span data-stu-id="d49cb-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
