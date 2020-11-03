---
title: Dodeljevanje vira opravilu
description: Ta tema vsebuje informacije o dodeljevanju virov opravilom.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084945"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="12921-103">Dodeljevanje vira opravilu</span><span class="sxs-lookup"><span data-stu-id="12921-103">Assign a resource to a task</span></span>

<span data-ttu-id="12921-104">Obstajajo trije načini dodeljevanja virov opravilu v aplikaciji Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="12921-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="12921-105">Rezervirajte vir kot član ekipe in nato dodelite vir opravilu</span><span class="sxs-lookup"><span data-stu-id="12921-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="12921-106">Vir lahko dodate projektni ekipi in ga nato dodelite opravilom v načrtu projekta.</span><span class="sxs-lookup"><span data-stu-id="12921-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="12921-107">Na zavihku **Član ekipe** dodate novega člana ekipe tako, da izberete **Novo**.</span><span class="sxs-lookup"><span data-stu-id="12921-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="12921-108">Odpre se plošča **Hitro ustvarjanje člana ekipe** , na kateri lahko izberete ime vira, ki ga je mogoče rezervirati, in nastavite vlogo.</span><span class="sxs-lookup"><span data-stu-id="12921-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="12921-109">Izberite enega od spodnjih načinov dodeljevanja za rezervacijo vira:</span><span class="sxs-lookup"><span data-stu-id="12921-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="12921-110">**Polna zmogljivost** rezervira polno zmogljivost vira za navedeni datumski obseg »Od« in »Do«.</span><span class="sxs-lookup"><span data-stu-id="12921-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="12921-111">**Odstotek zmogljivosti** rezervira vir za odstotek zmogljivosti vira za navedeni datumski obseg »Od« in »Do«.</span><span class="sxs-lookup"><span data-stu-id="12921-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="12921-112">**Enakomerna porazdelitev po urah** rezervira vir za določeno število ur, pri tem pa čas porazdeli enakomerno na dan v določenem datumskem obsegu.</span><span class="sxs-lookup"><span data-stu-id="12921-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="12921-113">**Obremenitev na začetku po urah** rezervira vir za določeno število ur, pri tem pa ure na dan porazdeli na začetek dneva v določenem časovnem obdobju »Od« in »Do«.</span><span class="sxs-lookup"><span data-stu-id="12921-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="12921-114">Način **Brez** doda vir ekipi, vendar ne ustvari rezervacij, ki bi prevzele zmogljivost vira.</span><span class="sxs-lookup"><span data-stu-id="12921-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="12921-115">V mreži za opravilo **Načrtovanje** v celici vira izberite ikono **Vir** , nato pa pod možnostjo **Člani ekipe** izberite člana ekipe, ki ste ga pravkar dodali.</span><span class="sxs-lookup"><span data-stu-id="12921-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members** , select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="12921-116">Na zavihkih **Član ekipe** in **Uskladitev** vir prikazuje rezervirane in dodeljene ure.</span><span class="sxs-lookup"><span data-stu-id="12921-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="12921-117">Ure bi morale biti enake, vendar to ni pogoj, saj rezervacije in dodelitve niso tesno povezane.</span><span class="sxs-lookup"><span data-stu-id="12921-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="12921-118">Na zavihku **Uskladitev** so navedene podrobnosti o tem, kdaj so vrednosti različne, na primer, če viru dodelite več ur, kot ste jih rezervirali.</span><span class="sxs-lookup"><span data-stu-id="12921-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="12921-119">Po potrebi lahko popravite informacije tako, da razširite rezervacije vira ali spremenite dodelitev.</span><span class="sxs-lookup"><span data-stu-id="12921-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="12921-120">Ustvarite generičnega člana ekipe z dodeljevanjem opravila</span><span class="sxs-lookup"><span data-stu-id="12921-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="12921-121">Ko z dodeljevanjem opravila ustvarite generičnega člana ekipe, ustvarite označbo mesta ali splošni vir, ki opisuje značilnosti poimenovanega vira, s katerim želite delati v opravilih.</span><span class="sxs-lookup"><span data-stu-id="12921-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="12921-122">Nato ustvarite zahtevo (ali pošljete prošnjo z uporabo zahteve), ki se uporablja za iskanje in rezervacijo poimenovanega vira.</span><span class="sxs-lookup"><span data-stu-id="12921-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="12921-123">V mreži za opravilo **Načrtovanje** v celici vira izberite ikono **Vir**.</span><span class="sxs-lookup"><span data-stu-id="12921-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="12921-124">Vnesite ime, ki bo služilo kot ime vira označbe mesta.</span><span class="sxs-lookup"><span data-stu-id="12921-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="12921-125">Na primer »Upravitelj programa«.</span><span class="sxs-lookup"><span data-stu-id="12921-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="12921-126">Izberite **Ustvari** in v polju **Hitro ustvarjanje člana projektne ekipe** nastavite vlogo za splošni vir.</span><span class="sxs-lookup"><span data-stu-id="12921-126">Select **Create** , and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="12921-127">Z dodeljevanjem opravil temu viru označbe mesta nadaljujete tako, da izberete vir v kontrolniku **Izbirnik virov** za opravilo.</span><span class="sxs-lookup"><span data-stu-id="12921-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="12921-128">Navedeni so pod možnostjo **Člani ekipe**.</span><span class="sxs-lookup"><span data-stu-id="12921-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="12921-129">Ko zaključite z dodeljevanjem splošnega vira, izberite splošni vir na zavihku **Ekipa** in nato izberite **Ustvari zahtevo** , da ustvarite zahtevo za splošni vir.</span><span class="sxs-lookup"><span data-stu-id="12921-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="12921-130">Za splošni vir izberite možnost **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="12921-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="12921-131">Nato lahko prek plošče razporeda poiščete in rezervirate pravi vir.</span><span class="sxs-lookup"><span data-stu-id="12921-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="12921-132">Prav tako lahko pošljete zahtevo za izpolnitev s strani upravitelja virov.</span><span class="sxs-lookup"><span data-stu-id="12921-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="12921-133">Ko je splošni vir izpolnjen s poimenovanim virom, se splošni vir odstrani iz ekipe, dodelitve opravil za splošni vir pa so dodeljene poimenovanemu viru, ki je izpolnil zahtevo za splošni vir.</span><span class="sxs-lookup"><span data-stu-id="12921-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="12921-134">Dodelite poimenovani vir s seznama vseh virov, ki jih je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="12921-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="12921-135">Uporabite lahko iskalno polje v kontrolniku **Izbirnik virov** , da poiščete vse vire, ki jih je mogoče rezervirati, in jih dodelite opravilu.</span><span class="sxs-lookup"><span data-stu-id="12921-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="12921-136">Viri, dodeljeni na ta način, se dodajo ekipi brez rezervacij.</span><span class="sxs-lookup"><span data-stu-id="12921-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="12921-137">To je podobno dodajanju člana ekipe in izbiri možnosti »Brez« kot načina dodeljevanja.</span><span class="sxs-lookup"><span data-stu-id="12921-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="12921-138">Vir je na zavihkih **Ekipa** in **Uskladitev** prikazan kot vir samo z dodelitvami in primanjkljajem za rezervacijo.</span><span class="sxs-lookup"><span data-stu-id="12921-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="12921-139">Če želite uporabiti njihovo razpoložljivost, jih rezervirajte.</span><span class="sxs-lookup"><span data-stu-id="12921-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="12921-140">V mreži za opravilo **Načrtovanje** v celici vira izberite ikono **Vir**.</span><span class="sxs-lookup"><span data-stu-id="12921-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="12921-141">Začnite vnašati ime.</span><span class="sxs-lookup"><span data-stu-id="12921-141">Start typing a name.</span></span> <span data-ttu-id="12921-142">Rezultati iskanja za ime so prikazani v kontrolniku **Izbirnik virov** v možnosti **Drugi viri**.</span><span class="sxs-lookup"><span data-stu-id="12921-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="12921-143">Izberite vir, ki ga želite dodeliti opravilu.</span><span class="sxs-lookup"><span data-stu-id="12921-143">Select the resource that you want to assign to the task.</span></span>

