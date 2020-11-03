---
title: Prikaz zaračunane uporabe virov
description: V tej temi so na voljo informacije o prikazu uporabe virov.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 6daa6cfa1c6a237d8a1685123f7c1a6926418bfe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084778"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="63362-103">Prikaz zaračunane uporabe virov</span><span class="sxs-lookup"><span data-stu-id="63362-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="63362-104">**Pogled »Uporaba«** na strani **Project Service – uporaba virov** prikazuje zaračunano uporabo za vsak vir, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="63362-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="63362-105">Ker pogled temelji na plošči razporeda, ima veliko podobnih funkcij.</span><span class="sxs-lookup"><span data-stu-id="63362-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Posnetek zaslona pogleda Uporaba](media/FAQ-utilization-1.png)
 

<span data-ttu-id="63362-107">Izračun zaračunane uporabe se izvaja kot sledi:</span><span class="sxs-lookup"><span data-stu-id="63362-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="63362-108">Zaračunana uporaba = (dejanske zaračunane ure) / (zmogljivost vira)</span><span class="sxs-lookup"><span data-stu-id="63362-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="63362-109">Celice predstavljajo izračunano zaračunano uporabo za izbrano obdobje (dnevi, tedni ali meseci).</span><span class="sxs-lookup"><span data-stu-id="63362-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="63362-110">Barve v vsaki celici prikazujejo zaračunano uporabo za vir, primerjano s ciljno zaračunano uporabo.</span><span class="sxs-lookup"><span data-stu-id="63362-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="63362-111">Ciljna uporaba se lahko določi glede na privzeto vlogo vira ali glede na posamezni vir.</span><span class="sxs-lookup"><span data-stu-id="63362-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="63362-112">Izračun najprej poišče posamezni vir in njegov cilj, šele nato privzeto vlogo vira.</span><span class="sxs-lookup"><span data-stu-id="63362-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="63362-113">Nastavljanje cilja v viru</span><span class="sxs-lookup"><span data-stu-id="63362-113">Set target on a resource</span></span>

1. <span data-ttu-id="63362-114">Odprite možnost **Viri** \> **Viri**.</span><span class="sxs-lookup"><span data-stu-id="63362-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="63362-115">Izberite vir, da odprete zapis.</span><span class="sxs-lookup"><span data-stu-id="63362-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="63362-116">Na zavihku **Project Service** lahko nastavite ciljno uporabo za vir.</span><span class="sxs-lookup"><span data-stu-id="63362-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Posnetek zaslona z zavihkom Project Service za nastavitev ciljne uporabe](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="63362-118">Nastavljanje ciljne uporabe v vlogi</span><span class="sxs-lookup"><span data-stu-id="63362-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="63362-119">Odprite **Viri** \> **Vloge virov**.</span><span class="sxs-lookup"><span data-stu-id="63362-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="63362-120">Izberite vlogo in odprite zapis.</span><span class="sxs-lookup"><span data-stu-id="63362-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="63362-121">Nastavite ciljno uporabo za to vlogo.</span><span class="sxs-lookup"><span data-stu-id="63362-121">Set the target utilization for the role.</span></span>

> ![Posnetek zaslona z možnostjo Vloge virov za nastavitev ciljne uporabe](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="63362-123">Izračun zaračunane uporabe za vir</span><span class="sxs-lookup"><span data-stu-id="63362-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="63362-124">Za izračun zaračunane uporabe vira morate izpolniti nekaj pogojev.</span><span class="sxs-lookup"><span data-stu-id="63362-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="63362-125">Nastavljanje privzete vloge za posamezni vir</span><span class="sxs-lookup"><span data-stu-id="63362-125">Set default role for individual resource</span></span>

<span data-ttu-id="63362-126">Ciljna uporaba se določi glede na posamezni vir ali vloge vira.</span><span class="sxs-lookup"><span data-stu-id="63362-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="63362-127">Če za cilje uporabljate vloge vira, mora imeti vsak posamezni vir privzeto vlogo.</span><span class="sxs-lookup"><span data-stu-id="63362-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="63362-128">To nastavite v možnosti **Viri** \> **Viri**.</span><span class="sxs-lookup"><span data-stu-id="63362-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="63362-129">Izberite vir, odprite zapis in nato izberite zavihek **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="63362-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="63362-130">V mreži **Vloga vira** preverite, ali vir ima vlogo in ali je možnost **Je privzeta** nastavljena na **Da**.</span><span class="sxs-lookup"><span data-stu-id="63362-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="63362-131">Spreminjanje vrste obračunavanja za vlogo vira</span><span class="sxs-lookup"><span data-stu-id="63362-131">Change billing type for resource role</span></span>

<span data-ttu-id="63362-132">Vloge virov morajo biti nastavljene tako, da je za vrsto obračunavanja izbrana možnost **Se zaračuna**.</span><span class="sxs-lookup"><span data-stu-id="63362-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="63362-133">Odprite **Viri** \> **Vloge virov**.</span><span class="sxs-lookup"><span data-stu-id="63362-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="63362-134">Odprite zapis, ki ga želite posodobiti, in nato privzeto vrsto obračunavanja nastavite na **Se zaračuna**.</span><span class="sxs-lookup"><span data-stu-id="63362-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="63362-135">Nastavitev delovnega časa za vlogo vira</span><span class="sxs-lookup"><span data-stu-id="63362-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="63362-136">Vir mora imeti delovnik, ki ustreza izračunani zmogljivosti.</span><span class="sxs-lookup"><span data-stu-id="63362-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="63362-137">Odprite možnost **Viri** \> **Viri**.</span><span class="sxs-lookup"><span data-stu-id="63362-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="63362-138">Izberite vir, da odprete zapis, in nato izberite **Prikaži delovne ure**.</span><span class="sxs-lookup"><span data-stu-id="63362-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="63362-139">Seznam virov lahko množično posodobite tako, da v pogledu **Seznam virov** uporabite **predlogo za delovne ure**.</span><span class="sxs-lookup"><span data-stu-id="63362-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="63362-140">Odpravljanje težav z dejanskimi zaračunanimi urami</span><span class="sxs-lookup"><span data-stu-id="63362-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="63362-141">Dejanske zaračunane ure so pridobljene iz entitete **Opravljeno delo**.</span><span class="sxs-lookup"><span data-stu-id="63362-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="63362-142">Opravljeno delo z vrsto obračunavanja **Se zaračuna** je vključeno v izračun, zato potrebujete projekte, v katerih je opravljeno delo mogoče zaračunati.</span><span class="sxs-lookup"><span data-stu-id="63362-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="63362-143">Če ne vidite zaračunane uporabe, lahko preverite naslednje:</span><span class="sxs-lookup"><span data-stu-id="63362-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="63362-144">Delovne ure vira so določene za zmogljivost.</span><span class="sxs-lookup"><span data-stu-id="63362-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="63362-145">Vir ima individualno določen ciljno uporabo ali mu je dodeljena vloga.</span><span class="sxs-lookup"><span data-stu-id="63362-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="63362-146">Vloga ima opredeljeno ciljno uporabo.</span><span class="sxs-lookup"><span data-stu-id="63362-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="63362-147">Vrsta obračunavanja za opravljeno delo je **Se zaračuna** in velja za obdobje, za katerega pričakujete izračun uporabe.</span><span class="sxs-lookup"><span data-stu-id="63362-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="63362-148">Če je opravljeno delo prikazano z drugimi vrstami obračunavanja, kot je »Se zaračuna«, preverite naslednje:</span><span class="sxs-lookup"><span data-stu-id="63362-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="63362-149">Vloga, ki se uporablja za opravljeno delo, ima privzeto vrsto obračunavanja drugačno od Se zaračuna.</span><span class="sxs-lookup"><span data-stu-id="63362-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="63362-150">Vloga v podrobnostih pogodbe za projekt je nastavljena na Se ne zaračuna.</span><span class="sxs-lookup"><span data-stu-id="63362-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="63362-151">Projekt nima povezanih podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="63362-151">The project does not have an associated contract line.</span></span>

