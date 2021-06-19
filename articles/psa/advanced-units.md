---
title: Skupine enot in enote
description: V tej temi so na voljo informacije o skupinah enot in enotah.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e981f39bbb6ca4277778382a5816952df2a8a1fb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009591"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="978b5-103">Skupine enot in enote</span><span class="sxs-lookup"><span data-stu-id="978b5-103">Unit groups and units</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="978b5-104">Skupine enot in enote so osnovne entitete v Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="978b5-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="978b5-105">Enota je posamezna merska enota, več enot pa je mogoče združiti v skupine enot.</span><span class="sxs-lookup"><span data-stu-id="978b5-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="978b5-106">Skupina enot se uporabniškem vmesniku Dynamics 365 včasih imenuje razpored enot.</span><span class="sxs-lookup"><span data-stu-id="978b5-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="978b5-107">Tukaj je nekaj primerov enot in skupin enot:</span><span class="sxs-lookup"><span data-stu-id="978b5-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="978b5-108">**Skupina enot**: razdalja</span><span class="sxs-lookup"><span data-stu-id="978b5-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="978b5-109">**Enote**: milja, kilometer itd.</span><span class="sxs-lookup"><span data-stu-id="978b5-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="978b5-110">**Skupina enot**: čas</span><span class="sxs-lookup"><span data-stu-id="978b5-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="978b5-111">**Enote**: ura, dan, teden itd.</span><span class="sxs-lookup"><span data-stu-id="978b5-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="978b5-112">Ko nastavite več enot v skupini enot, morate nastaviti tudi faktor pretvorbe med njimi, tako da določite prvo enoto, ki ste jo nastavili, kot privzeto ali glavno enoto za to skupino enot.</span><span class="sxs-lookup"><span data-stu-id="978b5-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="978b5-113">Če na primer v skupini enot **Čas** kot prvo enoto nastavite možnost **Ura**, sistem določi enoto **Ura** kot privzeto enoto.</span><span class="sxs-lookup"><span data-stu-id="978b5-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="978b5-114">Če kot naslednjo enoto nastavite možnost **Dan**, morate nastaviti faktor za pretvorbo **dneva** v **uro.**</span><span class="sxs-lookup"><span data-stu-id="978b5-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="978b5-115">Če nato kot tretjo enoto dodate **Teden**, morate za **Teden** nastaviti faktor za pretvorbo v enoti **Dan** ali **Ura**.</span><span class="sxs-lookup"><span data-stu-id="978b5-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="978b5-116">Naslednja slika prikazuje primer nastavitve za enoto **Dan**, kjer je v polju **Količina** prikazano število ur v dnevu, in enoto **Teden**, kjer je v polju **Količina** prikazano število dni v tednu.</span><span class="sxs-lookup"><span data-stu-id="978b5-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Skupina enot: stran z informacijami](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="978b5-118">Uporaba skupin enot in enot</span><span class="sxs-lookup"><span data-stu-id="978b5-118">Using units and unit groups</span></span>

<span data-ttu-id="978b5-119">Dynamics 365 Project Service Automation uporablja enote in skupine enot za obdelavo ocen in vnosov za stroške in čas.</span><span class="sxs-lookup"><span data-stu-id="978b5-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="978b5-120">Pri stroških ima vsaka kategorija stroškov privzeto skupino enot in enoto.</span><span class="sxs-lookup"><span data-stu-id="978b5-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="978b5-121">Te vrednosti so vnesene kot privzete vrednosti v vnosih v cenik za kategorije stroškov.</span><span class="sxs-lookup"><span data-stu-id="978b5-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="978b5-122">Tako lahko na primer imate kategorijo stroškov, ki se imenuje **Kilometrina.**</span><span class="sxs-lookup"><span data-stu-id="978b5-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="978b5-123">Ima skupino enot, ki se imenuje **Razdalja** in privzeto enoto **Milja**.</span><span class="sxs-lookup"><span data-stu-id="978b5-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="978b5-124">Če nastavite skupino enot **Razdalja** tako, da ima dve enoti (**Milja** in **Kilometer**), lahko za kategorijo **prevožene razdalje** na enem ceniku nastavite dve ceni: ceno na miljo in ceno na kilometer.</span><span class="sxs-lookup"><span data-stu-id="978b5-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="978b5-125">Kategorija stroška</span><span class="sxs-lookup"><span data-stu-id="978b5-125">Expense category</span></span>  | <span data-ttu-id="978b5-126">Skupina enot</span><span class="sxs-lookup"><span data-stu-id="978b5-126">Unit group</span></span>  | <span data-ttu-id="978b5-127">Enota</span><span class="sxs-lookup"><span data-stu-id="978b5-127">Unit</span></span>      | <span data-ttu-id="978b5-128">Način oblikovanja cen</span><span class="sxs-lookup"><span data-stu-id="978b5-128">Pricing method</span></span>  | <span data-ttu-id="978b5-129">Cena na enoto</span><span class="sxs-lookup"><span data-stu-id="978b5-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="978b5-130">Kilometrina</span><span class="sxs-lookup"><span data-stu-id="978b5-130">Mileage</span></span>           | <span data-ttu-id="978b5-131">Razdalja</span><span class="sxs-lookup"><span data-stu-id="978b5-131">Distance</span></span>      | <span data-ttu-id="978b5-132">Milja</span><span class="sxs-lookup"><span data-stu-id="978b5-132">Mile</span></span>      | <span data-ttu-id="978b5-133">Cena na enoto</span><span class="sxs-lookup"><span data-stu-id="978b5-133">Price per unit</span></span>    | <span data-ttu-id="978b5-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="978b5-134">10 USD</span></span>            |
| <span data-ttu-id="978b5-135">Kilometrina</span><span class="sxs-lookup"><span data-stu-id="978b5-135">Mileage</span></span>           | <span data-ttu-id="978b5-136">Razdalja</span><span class="sxs-lookup"><span data-stu-id="978b5-136">Distance</span></span>      | <span data-ttu-id="978b5-137">Kilometer</span><span class="sxs-lookup"><span data-stu-id="978b5-137">Kilometer</span></span> | <span data-ttu-id="978b5-138">Cena na enoto</span><span class="sxs-lookup"><span data-stu-id="978b5-138">Price per unit</span></span>    |  <span data-ttu-id="978b5-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="978b5-139">6 USD</span></span>            |

<span data-ttu-id="978b5-140">Ko za projekt vnesete strošek, sistem določi ceno na podlagi kombinacije kategorije in enote stroška.</span><span class="sxs-lookup"><span data-stu-id="978b5-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="978b5-141">Opis stroška</span><span class="sxs-lookup"><span data-stu-id="978b5-141">Expense description</span></span>        | <span data-ttu-id="978b5-142">Kategorija stroška</span><span class="sxs-lookup"><span data-stu-id="978b5-142">Expense category</span></span>  | <span data-ttu-id="978b5-143">Enota</span><span class="sxs-lookup"><span data-stu-id="978b5-143">Unit</span></span>  | <span data-ttu-id="978b5-144">Količina</span><span class="sxs-lookup"><span data-stu-id="978b5-144">Quantity</span></span>  | <span data-ttu-id="978b5-145">Cena enote</span><span class="sxs-lookup"><span data-stu-id="978b5-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="978b5-146">Prevoz k stranki</span><span class="sxs-lookup"><span data-stu-id="978b5-146">Drive to client location</span></span> | <span data-ttu-id="978b5-147">Kilometrina</span><span class="sxs-lookup"><span data-stu-id="978b5-147">Mileage</span></span>             | <span data-ttu-id="978b5-148">Milja</span><span class="sxs-lookup"><span data-stu-id="978b5-148">Mile</span></span>  | <span data-ttu-id="978b5-149">10</span><span class="sxs-lookup"><span data-stu-id="978b5-149">10</span></span>        | <span data-ttu-id="978b5-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="978b5-150">10 USD</span></span>         |

<span data-ttu-id="978b5-151">Za čas ima glava vsakega cenika polje **Privzeta časovna enota**.</span><span class="sxs-lookup"><span data-stu-id="978b5-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="978b5-152">Vrednost je nastavljena, ko ustvarite glavo cenika.</span><span class="sxs-lookup"><span data-stu-id="978b5-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="978b5-153">Ta enota se nato uporabi za nastavitev vseh cen na podlagi vlog v tem ceniku.</span><span class="sxs-lookup"><span data-stu-id="978b5-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="978b5-154">Vrstice ocen za polje **Čas v ponudbi** so lahko izražene v kateri koli časovni enoti.</span><span class="sxs-lookup"><span data-stu-id="978b5-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="978b5-155">Vendar pa lahko vrstice ocen za projekte in časovne vnose za projekte uporabljajo samo časovno enoti **Ura**.</span><span class="sxs-lookup"><span data-stu-id="978b5-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="978b5-156">Če se enota v časovnem vnosu ali vrstici ocene ujema z enoto v vrstici cenika za to vlogo, sistem pretvori ceno v enote, ki so določene v oceni projekta ali v dejanski transakciji projekta.</span><span class="sxs-lookup"><span data-stu-id="978b5-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="978b5-157">Ta primer prikazuje, kako PSA uporablja skupino enot, enote in faktorje za pretvorbo.</span><span class="sxs-lookup"><span data-stu-id="978b5-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="978b5-158">Enote</span><span class="sxs-lookup"><span data-stu-id="978b5-158">Units</span></span>

   - <span data-ttu-id="978b5-159">**Skupina enot**: čas</span><span class="sxs-lookup"><span data-stu-id="978b5-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="978b5-160">**Enote**: ura</span><span class="sxs-lookup"><span data-stu-id="978b5-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="978b5-161">**Dan** – faktor za pretvorbo: 8 ur</span><span class="sxs-lookup"><span data-stu-id="978b5-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="978b5-162">**Teden** – faktor za pretvorbo: 40 ur</span><span class="sxs-lookup"><span data-stu-id="978b5-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="978b5-163">Nastavitev cenika za projekt A:</span><span class="sxs-lookup"><span data-stu-id="978b5-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="978b5-164">**Ime**: prodajne cene v Združenem kraljestvu za 2016</span><span class="sxs-lookup"><span data-stu-id="978b5-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="978b5-165">**Privzeta časovna enota**: dan</span><span class="sxs-lookup"><span data-stu-id="978b5-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="978b5-166">**Valuta**: GBP</span><span class="sxs-lookup"><span data-stu-id="978b5-166">**Currency**: GBP</span></span>

| <span data-ttu-id="978b5-167">Vloga</span><span class="sxs-lookup"><span data-stu-id="978b5-167">Role</span></span>      | <span data-ttu-id="978b5-168">Skupina enot</span><span class="sxs-lookup"><span data-stu-id="978b5-168">Unit group</span></span> | <span data-ttu-id="978b5-169">Enota</span><span class="sxs-lookup"><span data-stu-id="978b5-169">Unit</span></span> | <span data-ttu-id="978b5-170">Organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="978b5-170">Organizational unit</span></span> | <span data-ttu-id="978b5-171">Cena</span><span class="sxs-lookup"><span data-stu-id="978b5-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="978b5-172">Razvijalec</span><span class="sxs-lookup"><span data-stu-id="978b5-172">Developer</span></span> | <span data-ttu-id="978b5-173">Čas</span><span class="sxs-lookup"><span data-stu-id="978b5-173">Time</span></span>       | <span data-ttu-id="978b5-174">dan</span><span class="sxs-lookup"><span data-stu-id="978b5-174">Day</span></span>  | <span data-ttu-id="978b5-175">Contoso Združeno kraljestvo</span><span class="sxs-lookup"><span data-stu-id="978b5-175">Contoso UK</span></span>          | <span data-ttu-id="978b5-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="978b5-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="978b5-177">Časovni vnos</span><span class="sxs-lookup"><span data-stu-id="978b5-177">Time entry</span></span>

<span data-ttu-id="978b5-178">V spodnji tabeli je prikazana posledična transakcija prodaje, ki jo je aplikacija PSA ustvarila za triurni projekt.</span><span class="sxs-lookup"><span data-stu-id="978b5-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="978b5-179">Project</span><span class="sxs-lookup"><span data-stu-id="978b5-179">Project</span></span>   | <span data-ttu-id="978b5-180">Opravilo</span><span class="sxs-lookup"><span data-stu-id="978b5-180">Task</span></span>    | <span data-ttu-id="978b5-181">Vloga</span><span class="sxs-lookup"><span data-stu-id="978b5-181">Role</span></span>      | <span data-ttu-id="978b5-182">Količina</span><span class="sxs-lookup"><span data-stu-id="978b5-182">Quantity</span></span> | <span data-ttu-id="978b5-183">Enota</span><span class="sxs-lookup"><span data-stu-id="978b5-183">Unit</span></span>  | <span data-ttu-id="978b5-184">Cena enote</span><span class="sxs-lookup"><span data-stu-id="978b5-184">Unit price</span></span> | <span data-ttu-id="978b5-185">Neobračunani znesek prodaje</span><span class="sxs-lookup"><span data-stu-id="978b5-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="978b5-186">Projekt A</span><span class="sxs-lookup"><span data-stu-id="978b5-186">Project A</span></span> | <span data-ttu-id="978b5-187">Načrt</span><span class="sxs-lookup"><span data-stu-id="978b5-187">Design</span></span>  | <span data-ttu-id="978b5-188">Developer</span><span class="sxs-lookup"><span data-stu-id="978b5-188">Developer</span></span> | <span data-ttu-id="978b5-189">3</span><span class="sxs-lookup"><span data-stu-id="978b5-189">3</span></span>        | <span data-ttu-id="978b5-190">Ura</span><span class="sxs-lookup"><span data-stu-id="978b5-190">Hour</span></span>  | <span data-ttu-id="978b5-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="978b5-191">100 GBP</span></span>    | <span data-ttu-id="978b5-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="978b5-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="978b5-193">Pogosta vprašanja o časovnih enotah</span><span class="sxs-lookup"><span data-stu-id="978b5-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="978b5-194">Ali PSA v primeru stroškov izvaja pretvorbo v različne enote?</span><span class="sxs-lookup"><span data-stu-id="978b5-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="978b5-195">Ne.</span><span class="sxs-lookup"><span data-stu-id="978b5-195">No.</span></span> <span data-ttu-id="978b5-196">Pretvorba enot deluje samo za časovne enote.</span><span class="sxs-lookup"><span data-stu-id="978b5-196">Unit conversion works only for time.</span></span> <span data-ttu-id="978b5-197">Za stroške pa velja, da če sistem ne more najti ceno za kombinacijo kategorije stroška in enote, je cena privzeto nastavljena na 0,00.</span><span class="sxs-lookup"><span data-stu-id="978b5-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="978b5-198">Zakaj PSA pretvarja časovne enote?</span><span class="sxs-lookup"><span data-stu-id="978b5-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="978b5-199">V nekaterih državah ali regijah predpisi določajo, da so zneski računov določeni v dnevih.</span><span class="sxs-lookup"><span data-stu-id="978b5-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="978b5-200">Pogajanja o cenah in popustih na stopnji ponudbe se izvajajo z dnevnimi cenami za vsako posamezno vlogo za obračun.</span><span class="sxs-lookup"><span data-stu-id="978b5-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="978b5-201">Ocena razporeda in časovni vnos se opravita v urah.</span><span class="sxs-lookup"><span data-stu-id="978b5-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="978b5-202">Za podporo pri tej razliki v časovnih enotah PSA izvede pretvorbo časovnih enot.</span><span class="sxs-lookup"><span data-stu-id="978b5-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="978b5-203">Ali je v ocenah projektov mogoče spremeniti časovne enote?</span><span class="sxs-lookup"><span data-stu-id="978b5-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="978b5-204">Ne.</span><span class="sxs-lookup"><span data-stu-id="978b5-204">No.</span></span> <span data-ttu-id="978b5-205">Ocena razporeda je trenutno omejena na ure in tega ni mogoče spremeniti.</span><span class="sxs-lookup"><span data-stu-id="978b5-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="978b5-206">Ali je enote in skupine enot mogoče urediti, izbrisati in dodajati?</span><span class="sxs-lookup"><span data-stu-id="978b5-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="978b5-207">Da.</span><span class="sxs-lookup"><span data-stu-id="978b5-207">Yes.</span></span> <span data-ttu-id="978b5-208">Z izjemo skupine enot **Čas** in enote **Ura** lahko vse enote izbrišete ali uredite ter dodate nove enote.</span><span class="sxs-lookup"><span data-stu-id="978b5-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="978b5-209">V PSA skupine enot **Čas** in enote **Uda** ni mogoče izbrisati.</span><span class="sxs-lookup"><span data-stu-id="978b5-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="978b5-210">Vendar pa jih je mogoče posodobiti s prevedenim besedilo za polje **Ime**.</span><span class="sxs-lookup"><span data-stu-id="978b5-210">However, they can be updated with a translated text for the **Name** field.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]