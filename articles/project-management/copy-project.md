---
title: Kopiranje projekta
description: Ta tema vsebuje informacije o kopiranju projektov v aplikaciji Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091274"
---
# <a name="copy-a-project"></a><span data-ttu-id="1e838-103">Kopiranje projekta</span><span class="sxs-lookup"><span data-stu-id="1e838-103">Copy a project</span></span>

<span data-ttu-id="1e838-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="1e838-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1e838-105">V aplikaciji Dynamics 365 Project Operations lahko hitro gradite nove projekte tako, da na obrazcu **Projekti** izberete možnost **Kopiraj projekt**.</span><span class="sxs-lookup"><span data-stu-id="1e838-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="1e838-106">Če želite kopirati projekt, odprite projekt, ki ga želite kopirati, in nato izberite možnost **Kopiraj projekt**.</span><span class="sxs-lookup"><span data-stu-id="1e838-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="1e838-107">Dejanje bo kopiralo naslednje:</span><span class="sxs-lookup"><span data-stu-id="1e838-107">The action will copy the following:</span></span>

- <span data-ttu-id="1e838-108">Lastnosti projekta</span><span class="sxs-lookup"><span data-stu-id="1e838-108">Project properties</span></span> 
- <span data-ttu-id="1e838-109">Strukturirana členitev dela</span><span class="sxs-lookup"><span data-stu-id="1e838-109">Work breakdown structure</span></span>
- <span data-ttu-id="1e838-110">Člani projektne ekipe</span><span class="sxs-lookup"><span data-stu-id="1e838-110">Project team members</span></span>
- <span data-ttu-id="1e838-111">Projektne ocene</span><span class="sxs-lookup"><span data-stu-id="1e838-111">Project estimates</span></span>
- <span data-ttu-id="1e838-112">Ocene stroškov projekta</span><span class="sxs-lookup"><span data-stu-id="1e838-112">Project expense estimates</span></span>
- <span data-ttu-id="1e838-113">Ocene materiala za projekt</span><span class="sxs-lookup"><span data-stu-id="1e838-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="1e838-114">Lastnosti projekta</span><span class="sxs-lookup"><span data-stu-id="1e838-114">Project properties</span></span>

<span data-ttu-id="1e838-115">Pri kopiranju projekta se kopirajo vrednosti v naslednjih poljih:</span><span class="sxs-lookup"><span data-stu-id="1e838-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="1e838-116">Imenu</span><span class="sxs-lookup"><span data-stu-id="1e838-116">Name</span></span>
- <span data-ttu-id="1e838-117">Opis</span><span class="sxs-lookup"><span data-stu-id="1e838-117">Description</span></span>
- <span data-ttu-id="1e838-118">Stranki</span><span class="sxs-lookup"><span data-stu-id="1e838-118">Customer</span></span>
- <span data-ttu-id="1e838-119">Predloga koledarja</span><span class="sxs-lookup"><span data-stu-id="1e838-119">Calendar Template</span></span>
- <span data-ttu-id="1e838-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="1e838-120">Currency</span></span>
- <span data-ttu-id="1e838-121">Pogodbena enota</span><span class="sxs-lookup"><span data-stu-id="1e838-121">Contracting Unit</span></span>
- <span data-ttu-id="1e838-122">Vodja projektov</span><span class="sxs-lookup"><span data-stu-id="1e838-122">Project Manager</span></span>
- <span data-ttu-id="1e838-123">Stanje</span><span class="sxs-lookup"><span data-stu-id="1e838-123">Status</span></span>
- <span data-ttu-id="1e838-124">Splošno stanje projekta</span><span class="sxs-lookup"><span data-stu-id="1e838-124">Overall Project Status</span></span>
- <span data-ttu-id="1e838-125">Pripombe</span><span class="sxs-lookup"><span data-stu-id="1e838-125">Comments</span></span>
- <span data-ttu-id="1e838-126">Ocene</span><span class="sxs-lookup"><span data-stu-id="1e838-126">Estimates</span></span>
- <span data-ttu-id="1e838-127">Predvideni začetni datum: to je datum, ko je projekt ustvarjen iz kopije.</span><span class="sxs-lookup"><span data-stu-id="1e838-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="1e838-128">Predvideni končni datum: ta datum se prilagodi glede na začetni datum novega projekta, ki je bil narejen iz kopije.</span><span class="sxs-lookup"><span data-stu-id="1e838-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="1e838-129">Obseg dela (ure)</span><span class="sxs-lookup"><span data-stu-id="1e838-129">Effort (Hours)</span></span>
- <span data-ttu-id="1e838-130">Ocenjena cena dela</span><span class="sxs-lookup"><span data-stu-id="1e838-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="1e838-131">Ocenjena cena stroškov</span><span class="sxs-lookup"><span data-stu-id="1e838-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="1e838-132">Ocenjena vrednost »material – cena«</span><span class="sxs-lookup"><span data-stu-id="1e838-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="1e838-133">Kopiranje projekta je dolgotrajen postopek.</span><span class="sxs-lookup"><span data-stu-id="1e838-133">Copy project is a long running operation.</span></span> <span data-ttu-id="1e838-134">Kopirajo se tudi projektni zapisi, njihovi ustrezni atributi in številne povezane entitete.</span><span class="sxs-lookup"><span data-stu-id="1e838-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="1e838-135">Zaradi dolgotrajne narave postopka je po začetku kopiranja stran ciljnega projekta zaklenjena za urejanje, dokler postopek kopiranja ni končan.</span><span class="sxs-lookup"><span data-stu-id="1e838-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="1e838-136">Strukturirana členitev dela</span><span class="sxs-lookup"><span data-stu-id="1e838-136">Work breakdown structure</span></span>

<span data-ttu-id="1e838-137">Pri kopiranju projekta se kopira celotna struktura razčlenitve dela z naloženimi viri.</span><span class="sxs-lookup"><span data-stu-id="1e838-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="1e838-138">Poimenovani vir je zamenjaj s splošnim.</span><span class="sxs-lookup"><span data-stu-id="1e838-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="1e838-139">Če imenovani viri nimajo enakega delovnega časa kot splošni vir, se urnik preračuna in trajanje opravil se lahko spremeni.</span><span class="sxs-lookup"><span data-stu-id="1e838-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="1e838-140">Člani projektne ekipe</span><span class="sxs-lookup"><span data-stu-id="1e838-140">Project team members</span></span>

<span data-ttu-id="1e838-141">Če je iz izvornega projekta kopirana projektna skupina, so kopirani splošni viri.</span><span class="sxs-lookup"><span data-stu-id="1e838-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="1e838-142">Iz izvornega projekta so ohranjene tudi dodelitve splošnega vira.</span><span class="sxs-lookup"><span data-stu-id="1e838-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="1e838-143">Poimenovani viri bodo pretvorjeni v splošne člane skupine.</span><span class="sxs-lookup"><span data-stu-id="1e838-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="1e838-144">Ocene</span><span class="sxs-lookup"><span data-stu-id="1e838-144">Estimates</span></span>

<span data-ttu-id="1e838-145">Ko je projekt kopiran, se iz izvornega projekta kopirajo vrstice virov, stroškov in ocene materiala.</span><span class="sxs-lookup"><span data-stu-id="1e838-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="1e838-146">Za informacije o programskem dostopu do programa Copy Project glejte razdelek [Razvijanje predlog projektov s programom Copy Project](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="1e838-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
