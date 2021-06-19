---
title: Načini razporejanja
description: Ta tema vsebuje informacije o načinih razporejanja.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116727"
---
# <a name="scheduling-modes"></a><span data-ttu-id="aa736-103">Načini razporejanja</span><span class="sxs-lookup"><span data-stu-id="aa736-103">Scheduling modes</span></span>

<span data-ttu-id="aa736-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="aa736-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="aa736-105">Storitev Dynamics 365 Project Operations organizacijam omogoča, da opredelijo način upravljanja sprememb ključnih spremenljivk v opravilih znotraj strukture členitve dela.</span><span class="sxs-lookup"><span data-stu-id="aa736-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="aa736-106">Na podlagi posebnih potreb organizacije lahko vodje projektov ob ustvaritvi projekta spremenijo način razporejanja.</span><span class="sxs-lookup"><span data-stu-id="aa736-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="aa736-107">V storitvi Project Operations so na voljo trije načini razporejanja:</span><span class="sxs-lookup"><span data-stu-id="aa736-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="aa736-108">Nespremenljivo trajanje (to je privzeti način)</span><span class="sxs-lookup"><span data-stu-id="aa736-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="aa736-109">Nespremenljiv obseg dela (*Delo*)</span><span class="sxs-lookup"><span data-stu-id="aa736-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="aa736-110">Nespremenljive enote</span><span class="sxs-lookup"><span data-stu-id="aa736-110">Fixed units</span></span>

<span data-ttu-id="aa736-111">Vrednosti, na katere vpliva opredelitev posameznega načina razporejanja, se določijo z naslednjo formulo:</span><span class="sxs-lookup"><span data-stu-id="aa736-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="aa736-112">Obseg dela = Trajanje x Enote</span><span class="sxs-lookup"><span data-stu-id="aa736-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="aa736-113">Ko določite način razporejanja projekta, nastavite eno od teh vrednosti, ki je nato ni mogoče spremeniti.</span><span class="sxs-lookup"><span data-stu-id="aa736-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="aa736-114">Če je ta vrednost konstanta, pridobi prednost, kar sistem obvesti, da je ne sme spremeniti, ko se spremenita drugi dve vrednosti.</span><span class="sxs-lookup"><span data-stu-id="aa736-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="aa736-115">Naslednja tabela vsebuje informacije o vplivih izbire posameznega načina.</span><span class="sxs-lookup"><span data-stu-id="aa736-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="aa736-116">**V tem opravilu**</span><span class="sxs-lookup"><span data-stu-id="aa736-116">**In this task**</span></span>             | <span data-ttu-id="aa736-117">**Če popravite enote**</span><span class="sxs-lookup"><span data-stu-id="aa736-117">**If you revise units**</span></span>   | <span data-ttu-id="aa736-118">**Če popravite trajanje**</span><span class="sxs-lookup"><span data-stu-id="aa736-118">**If you revise duration**</span></span> | <span data-ttu-id="aa736-119">**Če popravite obseg dela**</span><span class="sxs-lookup"><span data-stu-id="aa736-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="aa736-120">Opravilo z nespremenljivimi enotami</span><span class="sxs-lookup"><span data-stu-id="aa736-120">Fixed units task</span></span>     | <span data-ttu-id="aa736-121">Trajanje je znova izračunano.</span><span class="sxs-lookup"><span data-stu-id="aa736-121">Duration is recalculated.</span></span> | <span data-ttu-id="aa736-122">Obseg dela je znova izračunan.</span><span class="sxs-lookup"><span data-stu-id="aa736-122">Effort is recalculated.</span></span>    | <span data-ttu-id="aa736-123">Trajanje je znova izračunano.</span><span class="sxs-lookup"><span data-stu-id="aa736-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="aa736-124">Opravilo z nespremenljivim obsegom dela</span><span class="sxs-lookup"><span data-stu-id="aa736-124">Fixed effort task</span></span>    | <span data-ttu-id="aa736-125">Trajanje je znova izračunano.</span><span class="sxs-lookup"><span data-stu-id="aa736-125">Duration is recalculated.</span></span> | <span data-ttu-id="aa736-126">Enote so znova izračunane.</span><span class="sxs-lookup"><span data-stu-id="aa736-126">Units are recalculated.</span></span>    | <span data-ttu-id="aa736-127">Trajanje je znova izračunano.</span><span class="sxs-lookup"><span data-stu-id="aa736-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="aa736-128">Opravilo z nespremenljivim trajanjem</span><span class="sxs-lookup"><span data-stu-id="aa736-128">Fixed duration task</span></span>  | <span data-ttu-id="aa736-129">Obseg dela je znova izračunan.</span><span class="sxs-lookup"><span data-stu-id="aa736-129">Effort is recalculated.</span></span>   | <span data-ttu-id="aa736-130">Obseg dela je znova izračunan.</span><span class="sxs-lookup"><span data-stu-id="aa736-130">Effort is recalculated.</span></span>    | <span data-ttu-id="aa736-131">Enote so znova izračunane.</span><span class="sxs-lookup"><span data-stu-id="aa736-131">Units are recalculated.</span></span>   |

<span data-ttu-id="aa736-132">Za več informacij o vplivih posameznega načina si preberite razdelek [Sprememba vrste opravila za natančnejše razporejanje](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="aa736-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="aa736-133">V temi se namesto izraza **Obseg dela** uporablja izraz **Delo**.</span><span class="sxs-lookup"><span data-stu-id="aa736-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="aa736-134">Sprememba načina razporejanja organizacije</span><span class="sxs-lookup"><span data-stu-id="aa736-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="aa736-135">Upoštevajte naslednja navodila, da določite način razporejanja organizacije.</span><span class="sxs-lookup"><span data-stu-id="aa736-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="aa736-136">Odprite razdelek **Nastavitve** \> **Splošno** \> **Parametri** in nato izberite parameter projekta.</span><span class="sxs-lookup"><span data-stu-id="aa736-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="aa736-137">Na strani **Parametri projekta** izberite privzeti način razporejanja za organizacijo in nato upravitelju projekta omogočite preglasitev nastavitev pri ustvarjanju novega projekta.</span><span class="sxs-lookup"><span data-stu-id="aa736-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="aa736-138">Sprememba nastavitev načina razporejanja v projektu</span><span class="sxs-lookup"><span data-stu-id="aa736-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="aa736-139">Če organizacija upravitelju projektov dovoli, da preglasi privzeti način razporejanja, lahko vodja projekta to spremembo izvede ob ustvaritvi novega projekta.</span><span class="sxs-lookup"><span data-stu-id="aa736-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="aa736-140">Ko je projekt shranjen, pa načina razporejanja ni več mogoče spremeniti.</span><span class="sxs-lookup"><span data-stu-id="aa736-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="aa736-141">Kopirani projekti</span><span class="sxs-lookup"><span data-stu-id="aa736-141">Copied projects</span></span>

<span data-ttu-id="aa736-142">Ker je projekt ustvarjen ob izvedbi kopiranja projekta, upravitelj projekta ne more nastaviti načina razporejanja.</span><span class="sxs-lookup"><span data-stu-id="aa736-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="aa736-143">Ciljni projekt bo vedno privzeto deloval v načinu, določenem na ravni organizacije.</span><span class="sxs-lookup"><span data-stu-id="aa736-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="aa736-144">Kopirana opravila</span><span class="sxs-lookup"><span data-stu-id="aa736-144">Copied tasks</span></span>

<span data-ttu-id="aa736-145">Ko je opravilo kopirano iz enega projekta v drugega, opravilo podeduje način razporejanja ciljnega projekta.</span><span class="sxs-lookup"><span data-stu-id="aa736-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
