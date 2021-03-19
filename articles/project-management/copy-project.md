---
title: Kopiranje projekta
description: Ta tema vsebuje informacije o kopiranju projektov v aplikaciji Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479539"
---
# <a name="copy-a-project"></a><span data-ttu-id="d1492-103">Kopiranje projekta</span><span class="sxs-lookup"><span data-stu-id="d1492-103">Copy a project</span></span>

<span data-ttu-id="d1492-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="d1492-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d1492-105">V aplikaciji Dynamics 365 Project Operations lahko hitro gradite nove projekte tako, da na obrazcu **Projekti** izberete možnost **Kopiraj projekt**.</span><span class="sxs-lookup"><span data-stu-id="d1492-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="d1492-106">Če želite kopirati projekt, odprite projekt, ki ga želite kopirati, in nato izberite možnost **Kopiraj projekt**.</span><span class="sxs-lookup"><span data-stu-id="d1492-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="d1492-107">S tem dejanjem bodo kopirani naslednji elementi:</span><span class="sxs-lookup"><span data-stu-id="d1492-107">The action will copy:</span></span>

- <span data-ttu-id="d1492-108">Lastnosti projekta (predvideni datum začetka je kopiran iz izvornega projekta)</span><span class="sxs-lookup"><span data-stu-id="d1492-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="d1492-109">Strukturirana členitev dela</span><span class="sxs-lookup"><span data-stu-id="d1492-109">The Work breakdown structure</span></span>
- <span data-ttu-id="d1492-110">Člani projektne ekipe</span><span class="sxs-lookup"><span data-stu-id="d1492-110">Project team members</span></span>
- <span data-ttu-id="d1492-111">Projektne ocene</span><span class="sxs-lookup"><span data-stu-id="d1492-111">Project estimates</span></span>
- <span data-ttu-id="d1492-112">Ocene stroškov projekta</span><span class="sxs-lookup"><span data-stu-id="d1492-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="d1492-113">Lastnosti projekta</span><span class="sxs-lookup"><span data-stu-id="d1492-113">Project properties</span></span>

<span data-ttu-id="d1492-114">Pri kopiranju projekta se kopirajo vrednosti v naslednjih poljih:</span><span class="sxs-lookup"><span data-stu-id="d1492-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="d1492-115">Imenu</span><span class="sxs-lookup"><span data-stu-id="d1492-115">Name</span></span>
- <span data-ttu-id="d1492-116">Opis</span><span class="sxs-lookup"><span data-stu-id="d1492-116">Description</span></span>
- <span data-ttu-id="d1492-117">Stranki</span><span class="sxs-lookup"><span data-stu-id="d1492-117">Customer</span></span>
- <span data-ttu-id="d1492-118">Predloga koledarja</span><span class="sxs-lookup"><span data-stu-id="d1492-118">Calendar Template</span></span>
- <span data-ttu-id="d1492-119">Valuta</span><span class="sxs-lookup"><span data-stu-id="d1492-119">Currency</span></span>
- <span data-ttu-id="d1492-120">Pogodbena enota</span><span class="sxs-lookup"><span data-stu-id="d1492-120">Contracting Unit</span></span>
- <span data-ttu-id="d1492-121">Vodja projektov</span><span class="sxs-lookup"><span data-stu-id="d1492-121">Project Manager</span></span>
- <span data-ttu-id="d1492-122">Stanje</span><span class="sxs-lookup"><span data-stu-id="d1492-122">Status</span></span>
- <span data-ttu-id="d1492-123">Splošno stanje projekta</span><span class="sxs-lookup"><span data-stu-id="d1492-123">Overall Project Status</span></span>
- <span data-ttu-id="d1492-124">Pripombe</span><span class="sxs-lookup"><span data-stu-id="d1492-124">Comments</span></span>
- <span data-ttu-id="d1492-125">Ocene</span><span class="sxs-lookup"><span data-stu-id="d1492-125">Estimates</span></span>
- <span data-ttu-id="d1492-126">Predvideni začetni datum</span><span class="sxs-lookup"><span data-stu-id="d1492-126">Estimated Start Date</span></span>
- <span data-ttu-id="d1492-127">Datum zaključka</span><span class="sxs-lookup"><span data-stu-id="d1492-127">Finish Date</span></span>
- <span data-ttu-id="d1492-128">Obseg dela (ure)</span><span class="sxs-lookup"><span data-stu-id="d1492-128">Effort (Hours)</span></span>
- <span data-ttu-id="d1492-129">Predvideni stroški dela</span><span class="sxs-lookup"><span data-stu-id="d1492-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="d1492-130">Predvideni stroški</span><span class="sxs-lookup"><span data-stu-id="d1492-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="d1492-131">Strukturirana členitev dela</span><span class="sxs-lookup"><span data-stu-id="d1492-131">Work breakdown structure</span></span>

<span data-ttu-id="d1492-132">Pri kopiranju projekta se kopira celotna struktura razčlenitve dela z naloženimi viri.</span><span class="sxs-lookup"><span data-stu-id="d1492-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="d1492-133">Poimenovani vir je zamenjaj s splošnim.</span><span class="sxs-lookup"><span data-stu-id="d1492-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="d1492-134">Če imenovani viri nimajo enakega delovnega časa kot splošni vir, se urnik preračuna in trajanje opravil se lahko spremeni.</span><span class="sxs-lookup"><span data-stu-id="d1492-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="d1492-135">Člani projektne ekipe</span><span class="sxs-lookup"><span data-stu-id="d1492-135">Project team members</span></span>

<span data-ttu-id="d1492-136">Če je iz izvornega projekta kopirana projektna skupina, so kopirani splošni viri.</span><span class="sxs-lookup"><span data-stu-id="d1492-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="d1492-137">Iz izvornega projekta so ohranjene tudi dodelitve splošnega vira.</span><span class="sxs-lookup"><span data-stu-id="d1492-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="d1492-138">Poimenovani viri bodo pretvorjeni v splošne člane skupine.</span><span class="sxs-lookup"><span data-stu-id="d1492-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="d1492-139">Ocene</span><span class="sxs-lookup"><span data-stu-id="d1492-139">Estimates</span></span>

<span data-ttu-id="d1492-140">Pri kopiranju projekta so iz izvornega projekta kopirane vrstice za oceno virov in stroškov.</span><span class="sxs-lookup"><span data-stu-id="d1492-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="d1492-141">Za informacije o programskem dostopu do programa Copy Project glejte razdelek [Razvijanje predlog projektov s programom Copy Project](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="d1492-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
