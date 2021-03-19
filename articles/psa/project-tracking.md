---
title: Napredek projekta in poraba stroškov
description: Ta tema vsebuje informacije o spremljanju napredka projekta in porabi stroškov.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 73b23aad2976c8ccbb542fc2dda1d96dd9f5714b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283658"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="b9f5b-103">Napredek projekta in poraba stroškov</span><span class="sxs-lookup"><span data-stu-id="b9f5b-103">Project progress and cost consumption</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b9f5b-104">Potreba po spremljanju napredka v primerjavi z razporedom se razlikuje glede na panogo.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="b9f5b-105">V nekaterih panogah spremljanje poteka na zrnati ravni, v drugih panogah pa na višji ravni.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="b9f5b-106">V tej temi je prikazan način razporejanja, s katerim boste izpolnili zahteve vaše organizacije.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="b9f5b-107">Pogled sledenja obsegu dela</span><span class="sxs-lookup"><span data-stu-id="b9f5b-107">Effort tracking view</span></span>

<span data-ttu-id="b9f5b-108">Pogled **Sledenje obsegu dela** spremlja napredek opravila v razporedu.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="b9f5b-109">Primerja dejanske ure obsega dela, ki so bile porabljene za opravilo, z načrtovanimi urami obsega dela za opravilo.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="b9f5b-110">Project Service Automation za izračun metrike sledenja uporablja te formule:</span><span class="sxs-lookup"><span data-stu-id="b9f5b-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="b9f5b-111">Najprej pri ustvarjanju opravila: načrtovani stroški bodo nastavljeni na oceno končnih stroškov.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="b9f5b-112">Ko so za opravilo zabeležene dejanske vrednosti, se v pogledu Sledenje za obseg dela izračuna naslednje:</span><span class="sxs-lookup"><span data-stu-id="b9f5b-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="b9f5b-113">Odstotek napredka = dejanski obseg dela do danes ÷ ocena končnih stroškov (EAC)</span><span class="sxs-lookup"><span data-stu-id="b9f5b-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="b9f5b-114">Predvideni obseg dela do zaključka (ETC) = ocena končnih stroškov (EAC) – dejanski obseg dela do danes</span><span class="sxs-lookup"><span data-stu-id="b9f5b-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="b9f5b-115">Ocena končnih stroškov (EAC) = preostali obseg dela + dejanski obseg dela do danes</span><span class="sxs-lookup"><span data-stu-id="b9f5b-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="b9f5b-116">Predvideni odmik od obsega dela = načrtovan obseg dela – ocena končnih stroškov</span><span class="sxs-lookup"><span data-stu-id="b9f5b-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="b9f5b-117">Project Service Automation prikaže projekcijo odmika od obsega dela v opravilu.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="b9f5b-118">Če je EAC večji od načrtovanega obsega dela, bo opravilo predvidoma trajalo dlje časa, kot je bilo prvotno načrtovano.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="b9f5b-119">Torej je v zaostanku.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="b9f5b-120">Če je EAC manjši od načrtovanega obsega dela, bo opravilo predvidoma trajalo manj časa, kot je bilo prvotno načrtovano.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="b9f5b-121">Torej prehiteva urnik.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="b9f5b-122">Vnovična projekcija obsega dela</span><span class="sxs-lookup"><span data-stu-id="b9f5b-122">Reprojecting effort</span></span>

<span data-ttu-id="b9f5b-123">Vodja projekta pogosto popravi prvotne ocene v opravilu.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="b9f5b-124">Vnovične projekcije projekta so dojemanje ocen vodje projekta glede na trenutno stanje projekta.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="b9f5b-125">Vendar pa ne priporočamo, da vodje projektov spreminjajo osnovne številke, saj osnova projekta predstavlja zanesljiv vir ocene razporeda in stroškov za projekt, s katerim so se strinjale vse zainteresirane skupine, ki sodelujejo v projektu.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="b9f5b-126">Projektni vodja lahko znova projicira obseg dela v opravilih na dva načina:</span><span class="sxs-lookup"><span data-stu-id="b9f5b-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="b9f5b-127">Preglasi lahko privzeti ETC z novo oceno dejanskega preostalega obsega dela v opravilu.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="b9f5b-128">Preglasi lahko privzeti odstotek napredka z novo oceno dejanskega napredka v opravilu.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="b9f5b-129">Oba pristopa povzročita ponoven izračun ETC, EAC in odstotka napredka ter predvidenega odmika od obsega dela v opravilu.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="b9f5b-130">Ponovno se izračunajo tudi EAC, ETC in odstotek napredka v opravilih povzetkov, kar ustvari novo projekcijo odmika od obsega dela.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="b9f5b-131">Vnovična projekcija obsega dela v opravilih povzetka</span><span class="sxs-lookup"><span data-stu-id="b9f5b-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="b9f5b-132">Obseg dela v opravilih povzetka ali vsebnika je mogoče znova projicirati.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="b9f5b-133">Ne glede na to, ali uporabnik za ponovno projiciranje v opravilih povzetka uporabi preostali obseg dela ali odstotek napredka, se začne naslednji niz izračunov:</span><span class="sxs-lookup"><span data-stu-id="b9f5b-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="b9f5b-134">Izračunajo se EAC, ETC in odstotek napredka v opravilu.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="b9f5b-135">Novi EAC se porazdeli na podrejena opravila v enakem razmerju kot pri prvotnem EAC v opravilu.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="b9f5b-136">Izračuna se nova ocena končnih stroškov za vsako posamezno opravilo do opravil v listnem vozlišču.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="b9f5b-137">Prizadeta podrejena opravila do listnih vozlišč imajo svoj ETC in odstotek napredka, ki je znova izračunan na podlagi vrednosti EAC.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="b9f5b-138">Zato pride do nove projekcije odmika od obsega dela za opravilo.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="b9f5b-139">Znova se izračunajo vrednosti EAC opravil povzetka vse do korenskega vozlišča.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="b9f5b-140">Pogled za sledenje stroškom</span><span class="sxs-lookup"><span data-stu-id="b9f5b-140">Cost tracking view</span></span> 

<span data-ttu-id="b9f5b-141">Pogled **Sledenje stroškom** primerja dejanske stroške, ki so bili porabljeni v opravilu, z načrtovanimi stroški.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="b9f5b-142">Ta pogled prikazuje samo stroške dela in ne vključuje ocen stroškov.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="b9f5b-143">Project Service Automation za izračun metrike sledenja uporablja te formule:</span><span class="sxs-lookup"><span data-stu-id="b9f5b-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="b9f5b-144">Ko je opravilo ustvarjeno, so načrtovani stroški enaki oceni končnih stroškov.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="b9f5b-145">Ko so za opravilo zabeležene dejanske vrednosti, se v pogledu **Sledenje** za stroške izračuna naslednje:</span><span class="sxs-lookup"><span data-stu-id="b9f5b-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="b9f5b-146">Odstotek porabljenih stroškov = dejanski stroški, porabljeni do danes ÷ ocena končnih stroškov za opravilo</span><span class="sxs-lookup"><span data-stu-id="b9f5b-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="b9f5b-147">Stroški do zaključka (CTC) = ocena končnih stroškov – dejanski stroški, porabljeni do danes</span><span class="sxs-lookup"><span data-stu-id="b9f5b-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="b9f5b-148">Ocena končnih stroškov = stroški do zaključka (CTC) – dejanski stroški, porabljeni do danes</span><span class="sxs-lookup"><span data-stu-id="b9f5b-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="b9f5b-149">Predvideni odmik od stroškov = načrtovani stroški – ocena končnih stroškov</span><span class="sxs-lookup"><span data-stu-id="b9f5b-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="b9f5b-150">Projekcija odmika od stroškov je prikazana v opravilu.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="b9f5b-151">Če je ocena končnih stroškov večja od načrtovanih stroškov, bo opravilo predvidoma stalo več, kot je bilo prvotno načrtovano.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="b9f5b-152">Torej presega proračun.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="b9f5b-153">Če je ocena končnih stroškov manjša od načrtovanih stroškov, bo opravilo predvidoma stalo manj, kot je bilo prvotno načrtovano.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="b9f5b-154">Ponovna projekcija stroškov vodje projekta</span><span class="sxs-lookup"><span data-stu-id="b9f5b-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="b9f5b-155">Pri ponovni projekciji obsega dela so v pogledu **Sledenje stroškom** znova izračunani stroški do zaključka (CTC), ocena končnih stroškov, odstotek porabljenih stroškov in predvideni odmik od stroškov.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="b9f5b-156">Povzetek stanja projekta</span><span class="sxs-lookup"><span data-stu-id="b9f5b-156">Project status summary</span></span>

<span data-ttu-id="b9f5b-157">Sledenje podatkom v pogledih **Sledenje obsegu dela** in **Sledenje stroškom** prikaže napredek in porabo stroškov na ravneh korenskega vozlišča, opravil povzetka in opravil v listnem vozlišču.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="b9f5b-158">Razdelek **Stanje** na stran **Entiteta projekta** prikazuje povzetek stanja na ravni projekta.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="b9f5b-159">Polja s povzetkom stanja</span><span class="sxs-lookup"><span data-stu-id="b9f5b-159">Status summary fields</span></span>

<span data-ttu-id="b9f5b-160">Polje **Splošno stanje projekta** je polje, ki ga je mogoče urejati in ki prikazuje splošno stanje projekta.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="b9f5b-161">Uporablja barvno kodiranje, na primer zeleno, rumeno in rdečo barvo, za označevanje naraščajočega tveganja.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="b9f5b-162">Polje **Komentarji** omogoča vodji projekta, da vnese določene komentarje o stanju.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="b9f5b-163">Polja **Stanje posodobljeno dne** ni mogoče urejati, vrednost pa je časovni žig, ki označuje, kdaj je bilo stanje nazadnje posodobljeno.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="b9f5b-164">Polji **Učinkovitost razporeda** in **Stroškovna učinkovitost** sta nastavljeni iz datuma sledenja.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="b9f5b-165">Če sta vrednosti odmika od razporeda in stroškov za korensko vozlišče v pogledu **Sledenje obsegu dela** pozitivni, lahko polji nastavite na **Pred**.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="b9f5b-166">Če sta vrednosti odmika od razporeda in stroškov za korensko vozlišče negativni, ju lahko nastavite na **Za**.</span><span class="sxs-lookup"><span data-stu-id="b9f5b-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]