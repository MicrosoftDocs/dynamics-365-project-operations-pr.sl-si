---
title: Ustvarjanje rezervacije projekta na plošči razporeda
description: V tej temi so na voljo informacije o tem, kako ustvarite rezervacijo projekta na plošči razporeda.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: ccbfedec82b2d9035b51cf1b283ae5c441f1cbcc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122318"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="09554-103">Ustvarjanje rezervacije projekta na plošči razporeda</span><span class="sxs-lookup"><span data-stu-id="09554-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="09554-104">Vir lahko rezervirate za projekt neposredno na zavihku **Ekipa** projekta ali tako, da v dodelitvi generičnega člana ekipe ustvarite zahtevo za vir in nato ustvarjeno zahtevo izpolnite s članom projektne ekipe.</span><span class="sxs-lookup"><span data-stu-id="09554-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="09554-105">Prav tako lahko vir rezervirate za projekt neposredno na plošči razporeda.</span><span class="sxs-lookup"><span data-stu-id="09554-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="09554-106">To lahko naredite na tri načine:</span><span class="sxs-lookup"><span data-stu-id="09554-106">There are three ways to do this:</span></span>

- <span data-ttu-id="09554-107">**Rezervacija v ustvarjeni zahtevi za vir:** zahtevo za vir lahko ustvarite po tem, ko ustvarite splošni vir in dodelite opravila znotraj projekta.</span><span class="sxs-lookup"><span data-stu-id="09554-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="09554-108">**Rezervacija v primarni zahtevi:** primarne zahteve se prikažejo na plošči razporeda na zavihku **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="09554-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="09554-109">**Rezervacija v novi zahtevi za vir:** ustvarite lahko povsem novo zahtevo za vir in jo povežete s projektom.</span><span class="sxs-lookup"><span data-stu-id="09554-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="09554-110">Na plošči razporeda se zahteva za vir prikaže na zavihku **Odprte zahteve**.</span><span class="sxs-lookup"><span data-stu-id="09554-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="09554-111">Rezervacije v ustvarjeni zahtevi za vir</span><span class="sxs-lookup"><span data-stu-id="09554-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="09554-112">Ustvarite lahko splošni vir in mu dodelite eno ali več opravil znotraj projekta.</span><span class="sxs-lookup"><span data-stu-id="09554-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="09554-113">Nato lahko pri generičnem članu ekipe ustvarite zahtevo za vir.</span><span class="sxs-lookup"><span data-stu-id="09554-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="09554-114">Na plošči razporeda se bo ta vir prikazal na zavihku **Odprte zahteve**. Če imate veliko odprtih zahtev, boste morda morali uporabiti filtre stolpcev v mreži.</span><span class="sxs-lookup"><span data-stu-id="09554-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="09554-115">![Zavihek »Odprte zahteve na plošči razporeda](media/FAQ-Project-Booking-Schedule-Board-1.png "Posnetek zaslona tabele rezervacij in dodelitev")</span><span class="sxs-lookup"><span data-stu-id="09554-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="09554-116">Izberite zahtevo.</span><span class="sxs-lookup"><span data-stu-id="09554-116">Select the requirement.</span></span> <span data-ttu-id="09554-117">Na vrhu izbrane vrstice se prikaže zavihek **Poišči razpoložljivost**.</span><span class="sxs-lookup"><span data-stu-id="09554-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="09554-118">Ko izberete zavihek, se na plošči razporeda odpre način pomočnika za razporejanje, ki nato filtrira razpoložljive vire, ki izpolnjujejo zahtevo za vir.</span><span class="sxs-lookup"><span data-stu-id="09554-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="09554-119">Nato lahko rezervirate vir.</span><span class="sxs-lookup"><span data-stu-id="09554-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="09554-120">Prav tako lahko izbrano vrstico povlečete z dna plošče razporeda in jo spustite v celico vira v mreži zgoraj.</span><span class="sxs-lookup"><span data-stu-id="09554-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="09554-121">Ko jo spustite, se na desni strani odpre plošča **Ustvarjanje rezervacije vira**.</span><span class="sxs-lookup"><span data-stu-id="09554-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="09554-122">Če izberete možnost **Rezerviraj**, rezervirate vir za projektno ekipo.</span><span class="sxs-lookup"><span data-stu-id="09554-122">Selecting **Book** books the resource onto the project team.</span></span>

![Plošča »Ustvarjanje rezervacije vira«](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="09554-124">Rezervacija v primarni zahtevi</span><span class="sxs-lookup"><span data-stu-id="09554-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="09554-125">Če v storitvi Project Service ustvarite projekt, se samodejno ustvari zahteva za vir, imenovana primarna zahteva.</span><span class="sxs-lookup"><span data-stu-id="09554-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="09554-126">To je prazna zahteva, ki se uporablja za hitro rezervacijo vira na plošči razporeda, pri čemer ni treba ustvariti (povsem nove) zahteve.</span><span class="sxs-lookup"><span data-stu-id="09554-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="09554-127">Ker je zahteva prazna, boste morali določiti datume in način dodelitve ter ure, če so na voljo.</span><span class="sxs-lookup"><span data-stu-id="09554-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="09554-128">Če želite rezervirati vir s primarno zahtevo, na plošči razporeda izberite zavihek **Projekt**. Če imate veliko projektov, boste morda morali uporabiti filter stolpca v stolpcu **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="09554-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="09554-129">![Filtri stolpca na plošči razporeda](media/FAQ-Project-Booking-Schedule-Board-2.png "Posnetek zaslona tabele rezervacij in dodelitev")</span><span class="sxs-lookup"><span data-stu-id="09554-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="09554-130">Izberite zahtevo, ki ima v svojem imenu samo ime projekta, vrednost njenega trajanja pa je nič (0).</span><span class="sxs-lookup"><span data-stu-id="09554-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="09554-131">Izberite zavihek **Poišči razpoložljivost**, ki se prikaže v vrstici.</span><span class="sxs-lookup"><span data-stu-id="09554-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="09554-132">Plošča razporeda preide v način pomočnika za razporejanje in prikaže razpoložljive vire, ki jih je mogoče rezervirati za projekt.</span><span class="sxs-lookup"><span data-stu-id="09554-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="09554-133">Ker je **Primarna zahteva** prazna zahteva z vrednostjo trajanja nič (0), boste morali pri izbiri in rezervaciji vira na plošči **Ustvarjanje rezervacije vira** določiti trajanje.</span><span class="sxs-lookup"><span data-stu-id="09554-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="09554-134">Lahko izberete tudi možnost **Primarna zahteva projekta** na dnu plošče razporeda ter jo povlečete in spustite v vir, da ga rezervirate.</span><span class="sxs-lookup"><span data-stu-id="09554-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="09554-135">Ker je **Primarna zahteva** prazna zahteva z vrednostjo trajanja nič (0), boste morali pri izbiri in rezervaciji vira na plošči **Ustvarjanje rezervacije vira** določiti trajanje.</span><span class="sxs-lookup"><span data-stu-id="09554-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="09554-136">Če vir rezervirate prek možnosti **Primarna zahteva** na plošči razporeda, ga dodate projektni ekipi brez kakršnih koli dodelitev.</span><span class="sxs-lookup"><span data-stu-id="09554-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="09554-137">Rezervacije v novi zahtevi za vir</span><span class="sxs-lookup"><span data-stu-id="09554-137">Book from a new resource requirement</span></span>
<span data-ttu-id="09554-138">Za rezervacijo iz nove zahteve za vir dokončajte spodnje korake.</span><span class="sxs-lookup"><span data-stu-id="09554-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="09554-139">Odprite **Zahteve za vir** in nato izberite **Novo**, da ustvarite novo zahtevo za vir.</span><span class="sxs-lookup"><span data-stu-id="09554-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="09554-140">Na zavihku **Projekt** izberite projekt, da povežete zahtevo s projektom.</span><span class="sxs-lookup"><span data-stu-id="09554-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="09554-141">Ta novo ustvarjena zahteva se na plošči razporeda prikaže kot **Odprta zahteva**, ki jo lahko izpolnite.</span><span class="sxs-lookup"><span data-stu-id="09554-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="09554-142">Rezervirajte vir, da ga dodate projektni ekipi.</span><span class="sxs-lookup"><span data-stu-id="09554-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="09554-143">Zdaj, ko je vir rezerviran, morate ročno dodeliti opravila.</span><span class="sxs-lookup"><span data-stu-id="09554-143">Now that the resource is booked, you must assign tasks manually.</span></span>

