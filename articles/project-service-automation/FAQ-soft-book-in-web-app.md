---
title: Kako začasno rezerviram vire v aplikaciji različice 2.x?
description: V tem članku je opisano, kako začasno rezervirate člane projektne ekipe v storitvi Project Service.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Applies to Project Service version 2.x
ms.technology: ''
ms.assetid: 27063de4-cb0c-436f-970e-c87ebcab92db
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: aad119c0907cdd31220a0d73e6e7d99ee63e2e13
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755806"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="25d86-103">Kako začasno rezerviram vire v spletni aplikaciji (aplikacija Project Service različice 2.x)?</span><span class="sxs-lookup"><span data-stu-id="25d86-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="25d86-104">Za vir lahko okvirno načrtujete ali začasno rezervirate projektno ekipo in tako nakažete, da boste temu viru dodelili projekt.</span><span class="sxs-lookup"><span data-stu-id="25d86-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="25d86-105">Začasne rezervacije ne porabijo razpoložljive zmogljivosti vira.</span><span class="sxs-lookup"><span data-stu-id="25d86-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="25d86-106">Začasno rezerviranih članov ekipe ni mogoče dodeliti projektnim nalogam.</span><span class="sxs-lookup"><span data-stu-id="25d86-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="25d86-107">Nalogam je mogoče dodeliti samo vire s stanjem veljavne rezervacije in vrsto obveznosti Potrjeno (ob upoštevanju, da imajo dovolj ur veljavnih rezervacij, ki jih potrebujejo za dodelitev).</span><span class="sxs-lookup"><span data-stu-id="25d86-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="25d86-108">Člani projektne ekipe, ki so začasno rezervirani, so prikazani na mreži članov ekipe, pri čemer so začasno rezervirane ure prikazane v stolpcu Začasno rezervirano.</span><span class="sxs-lookup"><span data-stu-id="25d86-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="25d86-109">Prikazani so tudi na plošči razporeda.</span><span class="sxs-lookup"><span data-stu-id="25d86-109">They also show up on the schedule board.</span></span> <span data-ttu-id="25d86-110">Vseeno pa porabljena zmogljivost ni navedena, ker začasne rezervacije ne vplivajo na zmogljivost vira.</span><span class="sxs-lookup"><span data-stu-id="25d86-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="25d86-111">Obstajajo trije načini za začasno rezervacijo člana skupine v projektu prek aplikacije Project Service različice 2.x.</span><span class="sxs-lookup"><span data-stu-id="25d86-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="25d86-112">Začasno lahko rezervirate prek plošče razporeda, uporabite funkcijo Upravljanje rezervacij ali ustvarite splošen vir.</span><span class="sxs-lookup"><span data-stu-id="25d86-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="25d86-113">Ti načini so opisani spodaj.</span><span class="sxs-lookup"><span data-stu-id="25d86-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="25d86-114">Začasna rezervacija prek plošče razporeda</span><span class="sxs-lookup"><span data-stu-id="25d86-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="25d86-115">Za začasno rezervacijo prek plošče razporeda upoštevajte ta postopek:</span><span class="sxs-lookup"><span data-stu-id="25d86-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="25d86-116">Odpiranje plošče razporeda.</span><span class="sxs-lookup"><span data-stu-id="25d86-116">Open the schedule board.</span></span>
2. <span data-ttu-id="25d86-117">Na dnu plošče Zahteve za rezervacije na plošči razporeda izberite zavihek Projekt.</span><span class="sxs-lookup"><span data-stu-id="25d86-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="25d86-118">Poiščite projekt, za katerega želite začasno rezervirati vir.</span><span class="sxs-lookup"><span data-stu-id="25d86-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="25d86-119">Če imate več projektov, kliknite glavo stolpca Projekt in prek filtrov poiščite svoj projekt.</span><span class="sxs-lookup"><span data-stu-id="25d86-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="25d86-120">Kliknite projekt, nato ga povlecite in spustite na časovno mrežo vira.</span><span class="sxs-lookup"><span data-stu-id="25d86-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="25d86-121">Na desni se odpre plošča Ustvarjanje rezervacije vira.</span><span class="sxs-lookup"><span data-stu-id="25d86-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="25d86-122">Nastavite začetni in končni datum, izberite stanje rezervacije Začasno in določite ure.</span><span class="sxs-lookup"><span data-stu-id="25d86-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="25d86-123">Kliknite Rezerviraj.</span><span class="sxs-lookup"><span data-stu-id="25d86-123">Click Book.</span></span>
7. <span data-ttu-id="25d86-124">V projektu bo vir zdaj prikazan kot član ekipe, začasno rezervirane ure pa bodo prikazane v stolpcu Začasno rezervirano.</span><span class="sxs-lookup"><span data-stu-id="25d86-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="25d86-125">Upoštevajte, da virov v strukturirani členitvi dela (SČD) ne morete dodeliti opravilom, ker morajo biti veljavno rezervirani v ekipi, da jih lahko dodelite.</span><span class="sxs-lookup"><span data-stu-id="25d86-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="25d86-126">Začasna rezervacija prek funkcije Upravljanje rezervacij</span><span class="sxs-lookup"><span data-stu-id="25d86-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="25d86-127">Za začasno rezervacijo prek funkcije Upravljanje rezervacij upoštevajte ta postopek:</span><span class="sxs-lookup"><span data-stu-id="25d86-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="25d86-128">Na mreži člana ekipe kliknite Novo.</span><span class="sxs-lookup"><span data-stu-id="25d86-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="25d86-129">Izberite vire, ki jih je mogoče rezervirati, vloge ter časovno obdobje.</span><span class="sxs-lookup"><span data-stu-id="25d86-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="25d86-130">Izberite način dodelitve, ki je različen od Brez:</span><span class="sxs-lookup"><span data-stu-id="25d86-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="25d86-131">Polna zmogljivost</span><span class="sxs-lookup"><span data-stu-id="25d86-131">Full Capacity</span></span>
- <span data-ttu-id="25d86-132">Odstotek zmogljivosti</span><span class="sxs-lookup"><span data-stu-id="25d86-132">Percentage Capacity</span></span>
- <span data-ttu-id="25d86-133">Po urah, enakomerno</span><span class="sxs-lookup"><span data-stu-id="25d86-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="25d86-134">Po urah, obremenitev na začetku</span><span class="sxs-lookup"><span data-stu-id="25d86-134">By Hours Front Load</span></span>
4. <span data-ttu-id="25d86-135">Kliknite Shrani.</span><span class="sxs-lookup"><span data-stu-id="25d86-135">Click Save.</span></span> <span data-ttu-id="25d86-136">Vir bo prikazan na mreži ekipe, ure pa kot Veljavno rezervirane ure.</span><span class="sxs-lookup"><span data-stu-id="25d86-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="25d86-137">Ohranjanje rezervacije vira s klikom na Upravljanje rezervacij.</span><span class="sxs-lookup"><span data-stu-id="25d86-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="25d86-138">Ko se odpre plošča razporeda, razširite vir, da prikažete rezervacije.</span><span class="sxs-lookup"><span data-stu-id="25d86-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="25d86-139">Rezervacija bo navedena kot Veljavna.</span><span class="sxs-lookup"><span data-stu-id="25d86-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="25d86-140">Z desno tipko miške kliknite rezervacijo, pod možnostjo Sprememba stanja izberite Začasna rezervacija in nato Začasna.</span><span class="sxs-lookup"><span data-stu-id="25d86-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="25d86-141">Stanje rezervacije je Začasna.</span><span class="sxs-lookup"><span data-stu-id="25d86-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="25d86-142">Ko zaprete ploščo razporeda boste videli, da so se ure za vir na mreži ekipe spremenile iz Veljavno v Začasno.</span><span class="sxs-lookup"><span data-stu-id="25d86-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="25d86-143">Upoštevajte, da če veljavno rezervirate vir v ekipi in nato viru dodelite opravila v SČD, bodo, ko prek upravljanja rezervacij stanje spremenite iz veljavnega v začasno, dodelitve odstranjene iz opravil za ta vir, saj je samo veljavno rezerviranim virom mogoče dodeliti opravila.</span><span class="sxs-lookup"><span data-stu-id="25d86-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="25d86-144">Začasna rezervacija prek ustvarjanja splošnega vira</span><span class="sxs-lookup"><span data-stu-id="25d86-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="25d86-145">Začasno rezervacijo lahko ustvarite tudi tako, da ustvarite splošen vir v skupini članov, izpolnite ploščo razporeda ali zahtevo za vir in med postopkom rezervacije spremenite vrsto.</span><span class="sxs-lookup"><span data-stu-id="25d86-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="25d86-146">Upoštevajte spodnji postopek:</span><span class="sxs-lookup"><span data-stu-id="25d86-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="25d86-147">V SČD projekta dodelite vloge opravilom, za katera želite ustvariti splošnega člana ekipe.</span><span class="sxs-lookup"><span data-stu-id="25d86-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="25d86-148">Kliknite Ustvari projektno ekipo.</span><span class="sxs-lookup"><span data-stu-id="25d86-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="25d86-149">Na mreži člana ekipe izberite splošen vir in kliknite Rezerviraj.</span><span class="sxs-lookup"><span data-stu-id="25d86-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="25d86-150">Na plošči razporeda izberite vir, ki ga želite rezervirati.</span><span class="sxs-lookup"><span data-stu-id="25d86-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="25d86-151">Na plošči razporeda, v razdelku Ustvarjanje rezervacije vira, spremenite stanje rezervacije v Začasno.</span><span class="sxs-lookup"><span data-stu-id="25d86-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="25d86-152">Kliknite Rezerviraj ali Rezerviraj in zapri.</span><span class="sxs-lookup"><span data-stu-id="25d86-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="25d86-153">Ko zaprete ploščo razporeda boste izbrani vir videli v skupini, pri čemer so prikazane začasno rezervirane ure in dodeljene ure.</span><span class="sxs-lookup"><span data-stu-id="25d86-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="25d86-154">Prav tako bo splošni vir ostal v ekipi kot indikator, da so opravila dodeljena začasno dodeljenemu članu ekipe.</span><span class="sxs-lookup"><span data-stu-id="25d86-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="25d86-155">Ko ste pripravljeni na spremembo začasne rezervacije člana ekipe v veljavno rezervacijo, da mu lahko dodelite opravila, naredite naslednje:</span><span class="sxs-lookup"><span data-stu-id="25d86-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="25d86-156">Izberite vir in kliknite Upravljanje rezervacij.</span><span class="sxs-lookup"><span data-stu-id="25d86-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="25d86-157">Ko se odpre plošča razporeda, razširite vir, da prikažete rezervacije.</span><span class="sxs-lookup"><span data-stu-id="25d86-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="25d86-158">Rezervacija bo označena kot Začasna.</span><span class="sxs-lookup"><span data-stu-id="25d86-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="25d86-159">Z desno tipko miške kliknite rezervacijo, pod možnostjo Sprememba stanja izberite Veljavna rezervacija in nato Veljavna.</span><span class="sxs-lookup"><span data-stu-id="25d86-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="25d86-160">Stanje rezervacije je Veljavna.</span><span class="sxs-lookup"><span data-stu-id="25d86-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="25d86-161">Ko zaprete ploščo razporeda boste videli, da so se ure za vir na mreži ekipe spremenile iz Začasno v Veljavno.</span><span class="sxs-lookup"><span data-stu-id="25d86-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="25d86-162">Zdaj lahko viru dodelite opravila (ob upoštevanju, da so veljavno rezervirane ure usklajene s predvidenimi urami za opravilo).</span><span class="sxs-lookup"><span data-stu-id="25d86-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="25d86-163">Če ste upoštevali korake za izpolnitev splošnega vira iz točke 3 zgoraj, bo, ko stanje začasno rezerviranega vira spremenite v veljavno rezerviranega, splošni član ekipe odstranjen iz ekipe.</span><span class="sxs-lookup"><span data-stu-id="25d86-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>
