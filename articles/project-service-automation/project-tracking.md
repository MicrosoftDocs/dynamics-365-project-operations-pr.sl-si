---
title: Napredek projekta in poraba stroškov
description: Ta tema vsebuje informacije o spremljanju napredku projekta in porabi stroškov.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755854"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="57518-103">Napredek projekta in poraba stroškov</span><span class="sxs-lookup"><span data-stu-id="57518-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="57518-104">Potreba po spremljanju napredka v primerjavi z razporedom se razlikuje glede na panogo.</span><span class="sxs-lookup"><span data-stu-id="57518-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="57518-105">V nekaterih panogah spremljanje poteka na zrnati ravni, v drugih panogah pa na višji ravni.</span><span class="sxs-lookup"><span data-stu-id="57518-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="57518-106">V tej temi je prikazan način razporejanja, s katerim boste izpolnili zahteve vaše organizacije.</span><span class="sxs-lookup"><span data-stu-id="57518-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="57518-107">Pogled sledenja obsegu dela</span><span class="sxs-lookup"><span data-stu-id="57518-107">Effort tracking view</span></span>

<span data-ttu-id="57518-108">Pogled **Sledenje obsegu dela** spremlja napredek opravila v razporedu.</span><span class="sxs-lookup"><span data-stu-id="57518-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="57518-109">Primerja dejanske ure obsega dela, ki so bile porabljene za opravilo, z načrtovanimi urami obsega dela za to opravilo.</span><span class="sxs-lookup"><span data-stu-id="57518-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="57518-110">PSA za izračun metrike sledenja uporablja te formule:</span><span class="sxs-lookup"><span data-stu-id="57518-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="57518-111">Odstotek napredka = dejanski obseg dela do danes ÷ načrtovani obseg dela za opravilo</span><span class="sxs-lookup"><span data-stu-id="57518-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="57518-112">Predvideni obseg dela do zaključka (ETC) = načrtovani obseg dela – dejanski obseg dela do danes</span><span class="sxs-lookup"><span data-stu-id="57518-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="57518-113">Ocena končnih stroškov (EAC) = preostali obseg dela + dejanski obseg dela do danes</span><span class="sxs-lookup"><span data-stu-id="57518-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="57518-114">Predvideni odmik od obsega dela = načrtovan obseg dela – EAC</span><span class="sxs-lookup"><span data-stu-id="57518-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="57518-115">PSA prikaže projekcijo odmika od obsega dela v opravilu.</span><span class="sxs-lookup"><span data-stu-id="57518-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="57518-116">Če je EAC večji od načrtovanega obsega dela, bo opravilo predvidoma trajalo dlje časa, kot je bilo prvotno načrtovano.</span><span class="sxs-lookup"><span data-stu-id="57518-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="57518-117">Torej je v zaostanku.</span><span class="sxs-lookup"><span data-stu-id="57518-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="57518-118">Če je EAC manjši od načrtovanega obsega dela, bo opravilo predvidoma trajalo manj časa, kot je bilo prvotno načrtovano.</span><span class="sxs-lookup"><span data-stu-id="57518-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="57518-119">Torej prehiteva urnik.</span><span class="sxs-lookup"><span data-stu-id="57518-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="57518-120">Vnovična projekcija obsega dela</span><span class="sxs-lookup"><span data-stu-id="57518-120">Re-projecting effort</span></span>

<span data-ttu-id="57518-121">Vodja projekta pogosto popravi prvotne ocene v opravilu.</span><span class="sxs-lookup"><span data-stu-id="57518-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="57518-122">Ponovne projekcije projekta so dojemanje ocen vodje projekta glede na trenutno stanje projekta.</span><span class="sxs-lookup"><span data-stu-id="57518-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="57518-123">Vendar pa ne priporočamo, da vodje projektov spreminjajo osnovne številke, saj osnova projekta predstavlja zanesljiv vir ocene razporeda in stroškov za projekt, s katerim so se strinjale vse zainteresirane skupine, ki sodelujejo v projektu.</span><span class="sxs-lookup"><span data-stu-id="57518-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="57518-124">Projektni vodja lahko znova projicira obseg dela v opravilih na dva načina:</span><span class="sxs-lookup"><span data-stu-id="57518-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="57518-125">Preglasi lahko privzeti ETC z novo oceno dejanskega preostalega obsega dela v opravilu.</span><span class="sxs-lookup"><span data-stu-id="57518-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="57518-126">Preglasi lahko privzeti odstotek napredka z novo oceno dejanskega napredka v opravilu.</span><span class="sxs-lookup"><span data-stu-id="57518-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="57518-127">Oba pristopa povzročita ponoven izračun ETC, EAC in odstotka napredka ter predvidenega odmika od obsega dela v opravilu.</span><span class="sxs-lookup"><span data-stu-id="57518-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="57518-128">Ponovno se izračunajo tudi EAC, ETC in odstotek napredka v opravilih povzetkov, kar ustvari novo projekcijo odmika od obsega dela.</span><span class="sxs-lookup"><span data-stu-id="57518-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="57518-129">Vnovična projekcija obsega dela v opravilih povzetka</span><span class="sxs-lookup"><span data-stu-id="57518-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="57518-130">Obseg dela v opravilih povzetka ali vsebnika je mogoče znova projicirati.</span><span class="sxs-lookup"><span data-stu-id="57518-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="57518-131">Ne glede na to, ali uporabnik za ponovno projiciranje v opravilih povzetka uporabi preostali obseg dela ali odstotek napredka, se začne naslednji niz izračunov:</span><span class="sxs-lookup"><span data-stu-id="57518-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="57518-132">Izračunajo se EAC, ETC in odstotek napredka v opravilu.</span><span class="sxs-lookup"><span data-stu-id="57518-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="57518-133">Novi EAC se porazdeli na podrejena opravila v enakem razmerju kot pri prvotnem EAC v opravilu.</span><span class="sxs-lookup"><span data-stu-id="57518-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="57518-134">Izračuna se novi EAC za vsako posamezno opravilo do opravil v listnem vozlišču.</span><span class="sxs-lookup"><span data-stu-id="57518-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="57518-135">Prizadeta podrejena opravila do listnih vozlišč imajo svoj ETC in odstotek napredka, ki je znova izračunan na podlagi vrednosti EAC.</span><span class="sxs-lookup"><span data-stu-id="57518-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="57518-136">Zato pride do nove projekcije odmika od obsega dela za opravilo.</span><span class="sxs-lookup"><span data-stu-id="57518-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="57518-137">Znova se izračunajo vrednosti EAC opravil povzetka vse do korenskega vozlišča.</span><span class="sxs-lookup"><span data-stu-id="57518-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="57518-138">Pogled za sledenje stroškom</span><span class="sxs-lookup"><span data-stu-id="57518-138">Cost tracking view</span></span> 

<span data-ttu-id="57518-139">Pogled **Sledenje stroškom** primerja dejanske stroške, ki so bili porabljeni v opravilu, z načrtovanimi stroški opravila.</span><span class="sxs-lookup"><span data-stu-id="57518-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="57518-140">Ta pogled prikazuje samo stroške dela in ne vključuje ocen stroškov.</span><span class="sxs-lookup"><span data-stu-id="57518-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="57518-141">PSA za izračun metrike sledenja uporablja te formule:</span><span class="sxs-lookup"><span data-stu-id="57518-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="57518-142">Odstotek porabljenih stroškov = dejanski stroški, porabljeni do danes ÷ načrtovani stroški za opravilo</span><span class="sxs-lookup"><span data-stu-id="57518-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="57518-143">Stroški do zaključka (CTC) = načrtovani stroški – dejanski stroški, porabljeni do danes</span><span class="sxs-lookup"><span data-stu-id="57518-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="57518-144">Ocena končnih stroškov = CTC + dejanski stroški, porabljeni do danes</span><span class="sxs-lookup"><span data-stu-id="57518-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="57518-145">Predvideni odmik od stroškov = načrtovani stroški – ocena končnih stroškov</span><span class="sxs-lookup"><span data-stu-id="57518-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="57518-146">Projekcija odmika od stroškov je prikazana v opravilu.</span><span class="sxs-lookup"><span data-stu-id="57518-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="57518-147">Če je ocena končnih stroškov večja od načrtovanih stroškov, bo opravilo predvidoma stalo več, kot je bilo prvotno načrtovano.</span><span class="sxs-lookup"><span data-stu-id="57518-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="57518-148">Torej presega proračun.</span><span class="sxs-lookup"><span data-stu-id="57518-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="57518-149">Če je ocena končnih stroškov manjša od načrtovanih stroškov, bo opravilo predvidoma stalo manj, kot je bilo prvotno načrtovano.</span><span class="sxs-lookup"><span data-stu-id="57518-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="57518-150">Torej ni preseglo proračuna.</span><span class="sxs-lookup"><span data-stu-id="57518-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="57518-151">Ponovna projekcija stroškov vodje projekta</span><span class="sxs-lookup"><span data-stu-id="57518-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="57518-152">Pri ponovni projekciji obsega dela so v pogledu **Sledenje stroškom** znova izračuni CTC, ocena končnih stroškov, odstotek porabljenih stroškov in predvideni odmik od stroškov.</span><span class="sxs-lookup"><span data-stu-id="57518-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="57518-153">Povzetek stanja projekta</span><span class="sxs-lookup"><span data-stu-id="57518-153">Project status summary</span></span>

<span data-ttu-id="57518-154">Sledenje podatkom v pogledih **Sledenje obsegu dela** in **Sledenje stroškom** prikaže napredek in porabo stroškov na ravneh korenskega vozlišča, opravil povzetka in opravil v listnem vozlišču.</span><span class="sxs-lookup"><span data-stu-id="57518-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="57518-155">Razdelek **Stanje** na stran **Entiteta projekta** prikazuje povzetek stanja na ravni projekta.</span><span class="sxs-lookup"><span data-stu-id="57518-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="57518-156">Polja s povzetkom stanja</span><span class="sxs-lookup"><span data-stu-id="57518-156">Status summary fields</span></span>

<span data-ttu-id="57518-157">Polje **Splošno stanje projekta** je polje, ki ga je mogoče urejati in ki prikazuje splošno stanje projekta.</span><span class="sxs-lookup"><span data-stu-id="57518-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="57518-158">Uporablja barvno kodiranje, na primer zeleno, rumeno in rdečo barvo, za označevanje naraščajočega tveganja.</span><span class="sxs-lookup"><span data-stu-id="57518-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="57518-159">Polje **Komentarji** omogoča vodji projekta, da vnese določene komentarje o stanju.</span><span class="sxs-lookup"><span data-stu-id="57518-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="57518-160">Polja **Stanje posodobljeno dne** ni mogoče urejati, vrednost pa je časovni žig, ki označuje, kdaj je bilo stanje nazadnje posodobljeno.</span><span class="sxs-lookup"><span data-stu-id="57518-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="57518-161">Polji **Učinkovitost razporeda** in **Stroškovna učinkovitost** sta nastavljeni iz datuma sledenja.</span><span class="sxs-lookup"><span data-stu-id="57518-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="57518-162">Če sta vrednosti odmika od razporeda in stroškov za korensko vozlišče v pogledu **Sledenje obsegu dela** pozitivni, lahko polji nastavite na **Pred**.</span><span class="sxs-lookup"><span data-stu-id="57518-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="57518-163">Če sta vrednosti odmika od razporeda in stroškov za korensko vozlišče negativni, ju lahko nastavite na **Za**.</span><span class="sxs-lookup"><span data-stu-id="57518-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
