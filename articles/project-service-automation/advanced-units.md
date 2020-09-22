---
title: Skupine enot in enote
description: V tej temi so na voljo informacije o skupinah enot in enotah.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: b5422be3-5bfc-4ee2-b19a-4eca68813ff2
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fc2dde2d9471f8585c190a65f3ad9b32de75af86
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755899"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="a6589-103">Skupine enot in enote</span><span class="sxs-lookup"><span data-stu-id="a6589-103">Unit groups and units</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a6589-104">Skupine enot in enote so osnovne entitete v Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a6589-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="a6589-105">Enota je posamezna merska enota, več enot pa je mogoče združiti v skupine enot.</span><span class="sxs-lookup"><span data-stu-id="a6589-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="a6589-106">Skupina enot se uporabniškem vmesniku Dynamics 365 včasih imenuje razpored enot.</span><span class="sxs-lookup"><span data-stu-id="a6589-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="a6589-107">Tukaj je nekaj primerov enot in skupin enot:</span><span class="sxs-lookup"><span data-stu-id="a6589-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="a6589-108">**Skupina enot**: razdalja</span><span class="sxs-lookup"><span data-stu-id="a6589-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="a6589-109">**Enote**: milja, kilometer itd.</span><span class="sxs-lookup"><span data-stu-id="a6589-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="a6589-110">**Skupina enot**: čas</span><span class="sxs-lookup"><span data-stu-id="a6589-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="a6589-111">**Enote**: ura, dan, teden itd.</span><span class="sxs-lookup"><span data-stu-id="a6589-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="a6589-112">Ko nastavite več enot v skupini enot, morate nastaviti tudi faktor pretvorbe med njimi, tako da določite prvo enoto, ki ste jo nastavili, kot privzeto ali glavno enoto za to skupino enot.</span><span class="sxs-lookup"><span data-stu-id="a6589-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="a6589-113">Če na primer v skupini enot **Čas** kot prvo enoto nastavite možnost **Ura**, sistem določi enoto **Ura** kot privzeto enoto.</span><span class="sxs-lookup"><span data-stu-id="a6589-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="a6589-114">Če kot naslednjo enoto nastavite možnost **Dan**, morate nastaviti faktor za pretvorbo **dneva** v **uro.**</span><span class="sxs-lookup"><span data-stu-id="a6589-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="a6589-115">Če nato kot tretjo enoto dodate **Teden**, morate za **Teden** nastaviti faktor za pretvorbo v enoti **Dan** ali **Ura**.</span><span class="sxs-lookup"><span data-stu-id="a6589-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="a6589-116">Naslednja slika prikazuje primer nastavitve za enoto **Dan**, kjer je v polju **Količina** prikazano število ur v dnevu, in enoto **Teden**, kjer je v polju **Količina** prikazano število dni v tednu.</span><span class="sxs-lookup"><span data-stu-id="a6589-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Skupina enot: stran z informacijami](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="a6589-118">Uporaba skupin enot in enot</span><span class="sxs-lookup"><span data-stu-id="a6589-118">Using units and unit groups</span></span>

<span data-ttu-id="a6589-119">Dynamics 365 Project Service Automation uporablja enote in skupine enot za obdelavo ocen in vnosov za stroške in čas.</span><span class="sxs-lookup"><span data-stu-id="a6589-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="a6589-120">Pri stroških ima vsaka kategorija stroškov privzeto skupino enot in enoto.</span><span class="sxs-lookup"><span data-stu-id="a6589-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="a6589-121">Te vrednosti so vnesene kot privzete vrednosti v vnosih v cenik za kategorije stroškov.</span><span class="sxs-lookup"><span data-stu-id="a6589-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="a6589-122">Tako lahko na primer imate kategorijo stroškov, ki se imenuje **Kilometrina.**</span><span class="sxs-lookup"><span data-stu-id="a6589-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="a6589-123">Ima skupino enot, ki se imenuje **Razdalja** in privzeto enoto **Milja**.</span><span class="sxs-lookup"><span data-stu-id="a6589-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="a6589-124">Če nastavite skupino enot **Razdalja** tako, da ima dve enoti (**Milja** in **Kilometer**), lahko za kategorijo **prevožene razdalje** na enem ceniku nastavite dve ceni: ceno na miljo in ceno na kilometer.</span><span class="sxs-lookup"><span data-stu-id="a6589-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="a6589-125">Kategorija stroška</span><span class="sxs-lookup"><span data-stu-id="a6589-125">Expense category</span></span>  | <span data-ttu-id="a6589-126">Skupina enot</span><span class="sxs-lookup"><span data-stu-id="a6589-126">Unit group</span></span>  | <span data-ttu-id="a6589-127">Enota</span><span class="sxs-lookup"><span data-stu-id="a6589-127">Unit</span></span>      | <span data-ttu-id="a6589-128">Način oblikovanja cen</span><span class="sxs-lookup"><span data-stu-id="a6589-128">Pricing method</span></span>  | <span data-ttu-id="a6589-129">Cena na enoto</span><span class="sxs-lookup"><span data-stu-id="a6589-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="a6589-130">Kilometrina</span><span class="sxs-lookup"><span data-stu-id="a6589-130">Mileage</span></span>           | <span data-ttu-id="a6589-131">Razdalja</span><span class="sxs-lookup"><span data-stu-id="a6589-131">Distance</span></span>      | <span data-ttu-id="a6589-132">Milja</span><span class="sxs-lookup"><span data-stu-id="a6589-132">Mile</span></span>      | <span data-ttu-id="a6589-133">Cena na enoto</span><span class="sxs-lookup"><span data-stu-id="a6589-133">Price per unit</span></span>    | <span data-ttu-id="a6589-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="a6589-134">10 USD</span></span>            |
| <span data-ttu-id="a6589-135">Kilometrina</span><span class="sxs-lookup"><span data-stu-id="a6589-135">Mileage</span></span>           | <span data-ttu-id="a6589-136">Razdalja</span><span class="sxs-lookup"><span data-stu-id="a6589-136">Distance</span></span>      | <span data-ttu-id="a6589-137">Kilometer</span><span class="sxs-lookup"><span data-stu-id="a6589-137">Kilometer</span></span> | <span data-ttu-id="a6589-138">Cena na enoto</span><span class="sxs-lookup"><span data-stu-id="a6589-138">Price per unit</span></span>    |  <span data-ttu-id="a6589-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="a6589-139">6 USD</span></span>            |

<span data-ttu-id="a6589-140">Ko za projekt vnesete strošek, sistem določi ceno na podlagi kombinacije kategorije in enote stroška.</span><span class="sxs-lookup"><span data-stu-id="a6589-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="a6589-141">Opis stroška</span><span class="sxs-lookup"><span data-stu-id="a6589-141">Expense description</span></span>        | <span data-ttu-id="a6589-142">Kategorija stroška</span><span class="sxs-lookup"><span data-stu-id="a6589-142">Expense category</span></span>  | <span data-ttu-id="a6589-143">Enota</span><span class="sxs-lookup"><span data-stu-id="a6589-143">Unit</span></span>  | <span data-ttu-id="a6589-144">Količina</span><span class="sxs-lookup"><span data-stu-id="a6589-144">Quantity</span></span>  | <span data-ttu-id="a6589-145">Cena enote</span><span class="sxs-lookup"><span data-stu-id="a6589-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="a6589-146">Prevoz k stranki</span><span class="sxs-lookup"><span data-stu-id="a6589-146">Drive to client location</span></span> | <span data-ttu-id="a6589-147">Kilometrina</span><span class="sxs-lookup"><span data-stu-id="a6589-147">Mileage</span></span>             | <span data-ttu-id="a6589-148">Milja</span><span class="sxs-lookup"><span data-stu-id="a6589-148">Mile</span></span>  | <span data-ttu-id="a6589-149">10</span><span class="sxs-lookup"><span data-stu-id="a6589-149">10</span></span>        | <span data-ttu-id="a6589-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="a6589-150">10 USD</span></span>         |

<span data-ttu-id="a6589-151">Za čas ima glava vsakega cenika polje **Privzeta časovna enota**.</span><span class="sxs-lookup"><span data-stu-id="a6589-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="a6589-152">Vrednost je nastavljena, ko ustvarite glavo cenika.</span><span class="sxs-lookup"><span data-stu-id="a6589-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="a6589-153">Ta enota se nato uporabi za nastavitev vseh cen na podlagi vlog v tem ceniku.</span><span class="sxs-lookup"><span data-stu-id="a6589-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="a6589-154">Vrstice ocen za polje **Čas v ponudbi** so lahko izražene v kateri koli časovni enoti.</span><span class="sxs-lookup"><span data-stu-id="a6589-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="a6589-155">Vendar pa lahko vrstice ocen za projekte in časovne vnose za projekte uporabljajo samo časovno enoti **Ura**.</span><span class="sxs-lookup"><span data-stu-id="a6589-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="a6589-156">Če se enota v časovnem vnosu ali vrstici ocene ujema z enoto v vrstici cenika za to vlogo, sistem pretvori ceno v enote, ki so določene v oceni projekta ali v dejanski transakciji projekta.</span><span class="sxs-lookup"><span data-stu-id="a6589-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="a6589-157">Ta primer prikazuje, kako PSA uporablja skupino enot, enote in faktorje za pretvorbo.</span><span class="sxs-lookup"><span data-stu-id="a6589-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="a6589-158">Enote</span><span class="sxs-lookup"><span data-stu-id="a6589-158">Units</span></span>

   - <span data-ttu-id="a6589-159">**Skupina enot**: čas</span><span class="sxs-lookup"><span data-stu-id="a6589-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="a6589-160">**Enote**: ura</span><span class="sxs-lookup"><span data-stu-id="a6589-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="a6589-161">**Dan** – faktor za pretvorbo: 8 ur</span><span class="sxs-lookup"><span data-stu-id="a6589-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="a6589-162">**Teden** – faktor za pretvorbo: 40 ur</span><span class="sxs-lookup"><span data-stu-id="a6589-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="a6589-163">Nastavitev cenika za projekt A:</span><span class="sxs-lookup"><span data-stu-id="a6589-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="a6589-164">**Ime**: prodajne cene v Združenem kraljestvu za 2016</span><span class="sxs-lookup"><span data-stu-id="a6589-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="a6589-165">**Privzeta časovna enota**: dan</span><span class="sxs-lookup"><span data-stu-id="a6589-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="a6589-166">**Valuta**: GBP</span><span class="sxs-lookup"><span data-stu-id="a6589-166">**Currency**: GBP</span></span>

| <span data-ttu-id="a6589-167">Vloga</span><span class="sxs-lookup"><span data-stu-id="a6589-167">Role</span></span>      | <span data-ttu-id="a6589-168">Skupina enot</span><span class="sxs-lookup"><span data-stu-id="a6589-168">Unit group</span></span> | <span data-ttu-id="a6589-169">Enota</span><span class="sxs-lookup"><span data-stu-id="a6589-169">Unit</span></span> | <span data-ttu-id="a6589-170">Organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="a6589-170">Organizational unit</span></span> | <span data-ttu-id="a6589-171">Cena</span><span class="sxs-lookup"><span data-stu-id="a6589-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="a6589-172">Developer</span><span class="sxs-lookup"><span data-stu-id="a6589-172">Developer</span></span> | <span data-ttu-id="a6589-173">Time</span><span class="sxs-lookup"><span data-stu-id="a6589-173">Time</span></span>       | <span data-ttu-id="a6589-174">Day</span><span class="sxs-lookup"><span data-stu-id="a6589-174">Day</span></span>  | <span data-ttu-id="a6589-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="a6589-175">Contoso UK</span></span>          | <span data-ttu-id="a6589-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="a6589-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="a6589-177">Časovni vnos</span><span class="sxs-lookup"><span data-stu-id="a6589-177">Time entry</span></span>

<span data-ttu-id="a6589-178">V spodnji tabeli je prikazana posledična transakcija prodaje, ki jo je aplikacija PSA ustvarila za triurni projekt.</span><span class="sxs-lookup"><span data-stu-id="a6589-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="a6589-179">Project</span><span class="sxs-lookup"><span data-stu-id="a6589-179">Project</span></span>   | <span data-ttu-id="a6589-180">Opravilo</span><span class="sxs-lookup"><span data-stu-id="a6589-180">Task</span></span>    | <span data-ttu-id="a6589-181">Vloga</span><span class="sxs-lookup"><span data-stu-id="a6589-181">Role</span></span>      | <span data-ttu-id="a6589-182">Količina</span><span class="sxs-lookup"><span data-stu-id="a6589-182">Quantity</span></span> | <span data-ttu-id="a6589-183">Enota</span><span class="sxs-lookup"><span data-stu-id="a6589-183">Unit</span></span>  | <span data-ttu-id="a6589-184">Cena enote</span><span class="sxs-lookup"><span data-stu-id="a6589-184">Unit price</span></span> | <span data-ttu-id="a6589-185">Neobračunani znesek prodaje</span><span class="sxs-lookup"><span data-stu-id="a6589-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="a6589-186">Projekt A</span><span class="sxs-lookup"><span data-stu-id="a6589-186">Project A</span></span> | <span data-ttu-id="a6589-187">Načrt</span><span class="sxs-lookup"><span data-stu-id="a6589-187">Design</span></span>  | <span data-ttu-id="a6589-188">Developer</span><span class="sxs-lookup"><span data-stu-id="a6589-188">Developer</span></span> | <span data-ttu-id="a6589-189">3</span><span class="sxs-lookup"><span data-stu-id="a6589-189">3</span></span>        | <span data-ttu-id="a6589-190">Ura</span><span class="sxs-lookup"><span data-stu-id="a6589-190">Hour</span></span>  | <span data-ttu-id="a6589-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="a6589-191">100 GBP</span></span>    | <span data-ttu-id="a6589-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="a6589-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="a6589-193">Pogosta vprašanja o časovnih enotah</span><span class="sxs-lookup"><span data-stu-id="a6589-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="a6589-194">Ali PSA v primeru stroškov izvaja pretvorbo v različne enote?</span><span class="sxs-lookup"><span data-stu-id="a6589-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="a6589-195">Ne.</span><span class="sxs-lookup"><span data-stu-id="a6589-195">No.</span></span> <span data-ttu-id="a6589-196">Pretvorba enot deluje samo za časovne enote.</span><span class="sxs-lookup"><span data-stu-id="a6589-196">Unit conversion works only for time.</span></span> <span data-ttu-id="a6589-197">Za stroške pa velja, da če sistem ne more najti ceno za kombinacijo kategorije stroška in enote, je cena privzeto nastavljena na 0,00.</span><span class="sxs-lookup"><span data-stu-id="a6589-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="a6589-198">Zakaj PSA pretvarja časovne enote?</span><span class="sxs-lookup"><span data-stu-id="a6589-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="a6589-199">V nekaterih državah ali regijah predpisi določajo, da so zneski računov določeni v dnevih.</span><span class="sxs-lookup"><span data-stu-id="a6589-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="a6589-200">Pogajanja o cenah in popustih na stopnji ponudbe se izvajajo z dnevnimi cenami za vsako posamezno vlogo za obračun.</span><span class="sxs-lookup"><span data-stu-id="a6589-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="a6589-201">Ocena razporeda in časovni vnos se opravita v urah.</span><span class="sxs-lookup"><span data-stu-id="a6589-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="a6589-202">Za podporo pri tej razliki v časovnih enotah PSA izvede pretvorbo časovnih enot.</span><span class="sxs-lookup"><span data-stu-id="a6589-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="a6589-203">Ali je v ocenah projektov mogoče spremeniti časovne enote?</span><span class="sxs-lookup"><span data-stu-id="a6589-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="a6589-204">Ne.</span><span class="sxs-lookup"><span data-stu-id="a6589-204">No.</span></span> <span data-ttu-id="a6589-205">Ocena razporeda je trenutno omejena na ure in tega ni mogoče spremeniti.</span><span class="sxs-lookup"><span data-stu-id="a6589-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="a6589-206">Ali je enote in skupine enot mogoče urediti, izbrisati in dodajati?</span><span class="sxs-lookup"><span data-stu-id="a6589-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="a6589-207">Da.</span><span class="sxs-lookup"><span data-stu-id="a6589-207">Yes.</span></span> <span data-ttu-id="a6589-208">Z izjemo skupine enot **Čas** in enote **Ura** lahko vse enote izbrišete ali uredite ter dodate nove enote.</span><span class="sxs-lookup"><span data-stu-id="a6589-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="a6589-209">V PSA skupine enot **Čas** in enote **Uda** ni mogoče izbrisati.</span><span class="sxs-lookup"><span data-stu-id="a6589-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="a6589-210">Vendar pa jih je mogoče posodobiti s prevedenim besedilo za polje **Ime**.</span><span class="sxs-lookup"><span data-stu-id="a6589-210">However, they can be updated with a translated text for the **Name** field.</span></span>
