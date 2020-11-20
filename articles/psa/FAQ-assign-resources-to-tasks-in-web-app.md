---
title: Kako dodelim vir, ki ga je mogoče rezervirati, opravilu v spletni aplikaciji?
description: Pregled načinov dodeljevanja virov, ki jih je mogoče rezervirati.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: cc1859540ede064c4ab3e2ac128573972912a207
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125198"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="ae1d8-103">Kako dodelim vir, ki ga je mogoče rezervirati, opravilu v spletni aplikaciji (aplikacija Project Service različice 2.x)?</span><span class="sxs-lookup"><span data-stu-id="ae1d8-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ae1d8-104">Obstajata dva načina dodeljevanja virov opravilu v aplikaciji Project Service.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="ae1d8-105">Vir lahko rezervirate kot član ekipe in ga nato dodelite opravilu.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="ae1d8-106">Lahko pa ustvarite generičnega člana ekipe z dodeljevanjem vlog opravilom, ustvarite ekipo in nato s poimenovanim virom izpolnite zahteve za varnostno kopiranje.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="ae1d8-107">Če želite vir, ki ga je mogoče rezervirati, dodeliti opravilu, mora imeti član ekipe vira, ki ga je mogoče rezervirati, na voljo dovolj rezervacij.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="ae1d8-108">Stanje rezervacije mora biti »Potrdi vrsto veljavne rezervacije« in »Stanje potrjeno«.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="ae1d8-109">Če ni dovolj rezervacij za vir, aplikacija Project Service odstrani dodelitev in prikaže naslednje sporočilo o napaki:</span><span class="sxs-lookup"><span data-stu-id="ae1d8-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="ae1d8-110">*Ni mogoče dodeliti vira opravilu – naslednji viri za ta projekt nimajo rezerviranega zadostnega števila ur*</span><span class="sxs-lookup"><span data-stu-id="ae1d8-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="ae1d8-111">Rezervacija vira, pri čemer vir rezervirate kot član ekipe, in dodelitev vira opravilu</span><span class="sxs-lookup"><span data-stu-id="ae1d8-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="ae1d8-112">S tem načinom dodate vir projektni ekipi in nato opravila dodelite viru v načrtu projekta.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="ae1d8-113">To naredite tako:</span><span class="sxs-lookup"><span data-stu-id="ae1d8-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="ae1d8-114">V mreži člana ekipe dodajte novega člana ekipe tako, da izberete **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="ae1d8-115">V oknu »Hitro ustvarjanje člana ekipe« izberite ime vira, ki ga je mogoče rezervirati, in nastavite vlogo.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="ae1d8-116">Izberite datum **Od** in **Do**.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="ae1d8-117">![Posnetek zaslona dodajanja člana ekipe](media/FAQ-Resources-to-Tasks2-1.png "Posnetek zaslona dodajanja člana ekipe")</span><span class="sxs-lookup"><span data-stu-id="ae1d8-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="ae1d8-118">Izberite enega od naslednjih načinov dodeljevanja za rezervacijo vira:</span><span class="sxs-lookup"><span data-stu-id="ae1d8-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="ae1d8-119">**Polna zmogljivost** rezervira polno zmogljivost vira za navedeni datumski obseg »Od« in »Do«.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="ae1d8-120">**Odstotek zmogljivosti** rezervira vir za odstotek zmogljivosti vira za navedeni datumski obseg »Od« in »Do«.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="ae1d8-121">**Enakomerna porazdelitev po urah** rezervira vir za določeno število ur, pri tem pa čas porazdeli enakomerno na dan v določenem časovnem obdobju »Od« in »Do«.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="ae1d8-122">**Obremenitev na začetku po urah** rezervira vir za določeno število ur, pri tem pa ure na dan porazdeli na začetek dneva v določenem časovnem obdobju »Od« in »Do«.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="ae1d8-123">Ne izberite načina **Brez**, saj doda vir ekipi, vendar ne ustvari rezervacij, ki bi prevzele zmogljivost vira.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="ae1d8-124">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-124">Select **Save**.</span></span>

    <span data-ttu-id="ae1d8-125">Upoštevajte, da morajo ure rezervacije zadostovati za pokritje ur dela in datumskih obsegov opravil, katerim dodelite ta vir.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="ae1d8-126">Če ure niso usklajene, vira ne morete dodeliti opravilu.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="ae1d8-127">Na strukturirani členitvi dela (SČD) za opravilo kliknite spustni seznam s celicami vira.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="ae1d8-128">Nato:</span><span class="sxs-lookup"><span data-stu-id="ae1d8-128">Then:</span></span> 

    1. <span data-ttu-id="ae1d8-129">Izberite **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-129">Select **Add**.</span></span>
    2. <span data-ttu-id="ae1d8-130">Izberite spustni seznam pod možnostjo **Viri** in izberite člana ekipe, ki ste ga dodali zgoraj.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="ae1d8-131">izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-131">Select **OK**.</span></span> <span data-ttu-id="ae1d8-132">Član ekipe je zdaj dodeljen opravilu.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="ae1d8-133">![Posnetek zaslona dodajanja virov s SČD](media/FAQ-Resources-to-Tasks2-2.png "Posnetek zaslona dodajanja virov s SČD")</span><span class="sxs-lookup"><span data-stu-id="ae1d8-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="ae1d8-134">V mreži člana ekipe boste pod možnostjo »Dodeljene ure« videli združeno število ur, dodeljenih viru.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="ae1d8-135">To število je manjše ali enako številu rezerviranih ur za vir.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="ae1d8-136">![Posnetek zaslona dodeljenih ur za vir](media/FAQ-Resources-to-Tasks2-3.png "Posnetek zaslona dodeljenih ur za vir")</span><span class="sxs-lookup"><span data-stu-id="ae1d8-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="ae1d8-137">Če se opravilo, ki ga skušate dodeliti viru, začne po končnem datumu rezervacij virov, vir ne bo prikazan na spustnem seznamu.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="ae1d8-138">Upoštevajte, da lahko vir dodelite več uram, kot je rezerviranih ur vira, če ima vir še kaj preostale nedodeljene zmogljivosti.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="ae1d8-139">V tem primeru bo vir le delno dodeljen do števila rezervacij.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="ae1d8-140">Te preostale nedodeljene ure za opravila lahko vidite tako, da stolpec »Osebju nedodeljene ure« dodate v strukturirano členitev dela.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="ae1d8-141">Če so viri dodeljeni svojim rezerviranim uram (rezervirane ure virov so enake njihovim dodeljenim uram), boste videli naslednje sporočilo o napaki, če jim boste skušali dodeliti dodatna opravila:</span><span class="sxs-lookup"><span data-stu-id="ae1d8-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="ae1d8-142">*Ni mogoče dodeliti vira opravilu – naslednji viri za ta projekt nimajo rezerviranega zadostnega števila ur.*</span><span class="sxs-lookup"><span data-stu-id="ae1d8-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="ae1d8-143">Poleg tega je privzeti vodja projekta kot član ekipe, ki je dodan ekipi, ko ustvarite projekt, dodan brez rezervacij in ga ni mogoče dodeliti nobenemu opravilu.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="ae1d8-144">Ne bo prikazan na spustnem seznamu virov za opravila.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="ae1d8-145">Če želite dodeliti ta vir, ga morate odstraniti iz ekipe in ga nato ponovno dodati na kateri koli način dodeljevanja, ki ni »Brez«.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="ae1d8-146">Ko ustvarite projekt, se vir ekipi doda z namenom, da ima projekt vsaj enega privzetega odobritelja.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="ae1d8-147">Ustvarjanje generičnega člana ekipe z dodeljevanjem vlog opravilom</span><span class="sxs-lookup"><span data-stu-id="ae1d8-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="ae1d8-148">Ta način zagotavlja, da imajo viri dovolj rezervacij za opravila.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="ae1d8-149">Najprej ustvarite ogrado ali splošni vir, ki opisuje značilnosti poimenovanega vira, ki ga želite dodeliti opravilom, tako, da opravilom najprej dodelite vloge, nato pa ustvarite ekipo.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="ae1d8-150">To naredite tako:</span><span class="sxs-lookup"><span data-stu-id="ae1d8-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="ae1d8-151">V strukturirani členitvi dela izberite opravilo.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="ae1d8-152">V celici vira izberite ikono spustnega seznama **Dodeljena vloga**.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="ae1d8-153">Izberite spustni seznam **Vloga** in izberite vlogo za splošni vir.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="ae1d8-154">Izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="ae1d8-155">![Posnetek zaslona uporabe SČD za dodajanje vira](media/FAQ-Resources-to-Tasks2-4.png "Posnetek zaslona uporabe SČD za dodajanje vira")</span><span class="sxs-lookup"><span data-stu-id="ae1d8-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="ae1d8-156">Ko končate z dodeljevanjem vlog opravilom v SČD, izberite **Ustvari projektno ekipo**.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="ae1d8-157">Storitev Project Service ustvari najmanjše število generičnih članov ekipe na podlagi njihovih vlog, organizacijskih enot vira in koledarja projekta z združevanjem dodelitev opravil.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="ae1d8-158">![Posnetek zaslona ustvarjanja projektne ekipe](media/FAQ-Resources-to-Tasks2-5.png "Posnetek zaslona ustvarjanja projektne ekipe")</span><span class="sxs-lookup"><span data-stu-id="ae1d8-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="ae1d8-159">V mreži člana ekipe boste videli vire vrste »Splošni vir« z vlogo in imenom položaja.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="ae1d8-160">Če sta potrebna dva vira za vlogo za dokončanje dela, funkcija »Ustvari ekipo« ustvari dva člana ekipe in uporabi ime položaja, da ju loči.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="ae1d8-161">![Posnetek zaslona dodajanja dveh splošnih virov](media/FAQ-Resources-to-Tasks2-6.png "Posnetek zaslona dodajanja dveh splošnih virov")</span><span class="sxs-lookup"><span data-stu-id="ae1d8-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="ae1d8-162">Zahtevo za rezervni vir za generičnega člana ekipe lahko odprete tako, da izberete povezavo pod možnostjo »Zahteva za vir«.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="ae1d8-163">![Posnetek zaslona odpiranja zahteve za rezervni vir](media/FAQ-Resources-to-Tasks2-7.png "Posnetek zaslona odpiranja zahteve za rezervni vir")</span><span class="sxs-lookup"><span data-stu-id="ae1d8-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="ae1d8-164">Za splošni vir izberite možnost **Rezerviraj**, nato pa prek plošče razporeda poiščite in rezervirajte pravi vir.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="ae1d8-165">Prav tako lahko pošljete zahtevo za izpolnitev s strani upravitelja virov tako, da izberete **Pošlji zahtevo**.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="ae1d8-166">Ko je splošni vir izpolnjen s poimenovanim virom, se splošni vir odstrani iz ekipe, dodelitve opravil za splošni vir pa so dodeljene poimenovanemu viru, ki je izpolnil zahtevo za splošni vir.</span><span class="sxs-lookup"><span data-stu-id="ae1d8-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

