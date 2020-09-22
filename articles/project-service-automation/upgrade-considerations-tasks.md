---
title: Nadgradnja vidikov za strukturirano členitev dela
description: Ta tema vsebuje informacije o nadgradnji strukturirane členitve dela iz storitve Project Service Automation 2.x na 3.x.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755832"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="949c0-103">Nadgradnja vidikov za strukturirano členitev dela</span><span class="sxs-lookup"><span data-stu-id="949c0-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="949c0-104">Ta tema vsebuje informacije o nadgradnji strukturirane členitve dela iz storitve Project Service Automation 2.x na 3.x.</span><span class="sxs-lookup"><span data-stu-id="949c0-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="949c0-105">Ta tema opisuje zdravo stanje projekta v rešitvi Project Service Automation (PSA), ki je potrebno za uspešno nadgradnjo.</span><span class="sxs-lookup"><span data-stu-id="949c0-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="949c0-106">Vsebuje tudi informacije o pogostih razlogih za blokiranje, zaradi katerih bi bila nadgradnja neuspešna.</span><span class="sxs-lookup"><span data-stu-id="949c0-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="949c0-107">Za več informacij o določanju projektnih opravil in njihovih funkcijah v okviru projektnega razporeda glejte temo [Projektni razporedi](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="949c0-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="949c0-108">Ključne entitete</span><span class="sxs-lookup"><span data-stu-id="949c0-108">Key entities</span></span>
<span data-ttu-id="949c0-109">Za natančno strukturirano členitev dela, ki že ima naložene vire, so potrebne naslednje entitete:</span><span class="sxs-lookup"><span data-stu-id="949c0-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="949c0-110">Project</span><span class="sxs-lookup"><span data-stu-id="949c0-110">Project</span></span>](../developer/entities/msdyn_project.md)
- [<span data-ttu-id="949c0-111">Projektna ekipa</span><span class="sxs-lookup"><span data-stu-id="949c0-111">Project Team</span></span>](../developer/entities/msdyn_projectteam.md)
- [<span data-ttu-id="949c0-112">Projektno opravilo</span><span class="sxs-lookup"><span data-stu-id="949c0-112">Project Task</span></span>](../developer/entities/msdyn_projecttask.md)
- [<span data-ttu-id="949c0-113">Dodelitve virov</span><span class="sxs-lookup"><span data-stu-id="949c0-113">Resource Assignments</span></span>](../developer/entities/msdyn_resourceassignment.md)
- [<span data-ttu-id="949c0-114">Odvisnost projektnega opravila</span><span class="sxs-lookup"><span data-stu-id="949c0-114">Project Task Dependency</span></span>](../developer/entities/msdyn_projecttaskdependency.md)
- [<span data-ttu-id="949c0-115">Viri, ki jih je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="949c0-115">Bookable Resources</span></span>](../developer/entities/bookableresource.md)

<span data-ttu-id="949c0-116">Če želite določiti vir z naloženo strukturirano členitvijo dela, morate izvesti naslednje korake:</span><span class="sxs-lookup"><span data-stu-id="949c0-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="949c0-117">Ustvarite nov projekt.</span><span class="sxs-lookup"><span data-stu-id="949c0-117">Create a new project.</span></span> <span data-ttu-id="949c0-118">Za več informacij o tem, kako ustvarite nov projekt, glejte temo [msdyn_project](../developer/entities/msdyn_project.md).</span><span class="sxs-lookup"><span data-stu-id="949c0-118">For more information about how to create a new project, see [msdyn_project](../developer/entities/msdyn_project.md).</span></span>
2. <span data-ttu-id="949c0-119">Ustvarite eno ali več opravil.</span><span class="sxs-lookup"><span data-stu-id="949c0-119">Create one or more tasks.</span></span> <span data-ttu-id="949c0-120">Za več informacij o tem, kako ustvarite opravilo, glejte temo [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span><span class="sxs-lookup"><span data-stu-id="949c0-120">For more information about how to create a task, see [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span></span>
3. <span data-ttu-id="949c0-121">Določite odvisnosti opravila.</span><span class="sxs-lookup"><span data-stu-id="949c0-121">Define the task dependencies.</span></span> <span data-ttu-id="949c0-122">Za več informacij glejte [Odvisnost projektnega opravila](../developer/entities/msdyn_projecttaskdependency.md).</span><span class="sxs-lookup"><span data-stu-id="949c0-122">For more information, see [Project Task Dependency](../developer/entities/msdyn_projecttaskdependency.md).</span></span>
4. <span data-ttu-id="949c0-123">Dodelite člane projektne ekipe izbranemu projektu.</span><span class="sxs-lookup"><span data-stu-id="949c0-123">Assign project team members to the project.</span></span> <span data-ttu-id="949c0-124">Za več informacij glejte temo [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span><span class="sxs-lookup"><span data-stu-id="949c0-124">For more information, see [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span></span>
5. <span data-ttu-id="949c0-125">Dodelite člane projektne ekipe izbranim opravilom.</span><span class="sxs-lookup"><span data-stu-id="949c0-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="949c0-126">Za več informacij glejte temo [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span><span class="sxs-lookup"><span data-stu-id="949c0-126">For more information, see [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="949c0-127">Odnosi projektnih ekip</span><span class="sxs-lookup"><span data-stu-id="949c0-127">Project team relationships</span></span>

<span data-ttu-id="949c0-128">Če želite zagotoviti uspešno nadgradnjo, morate ustrezno ohraniti naslednje odnose:</span><span class="sxs-lookup"><span data-stu-id="949c0-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="949c0-129">Vsi člani projektne ekipe morajo biti povezani z virom, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="949c0-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="949c0-130">Vsi člani projektne ekipe morajo biti povezani z enakim projektom.</span><span class="sxs-lookup"><span data-stu-id="949c0-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="949c0-131">Odnosi projektnih opravil</span><span class="sxs-lookup"><span data-stu-id="949c0-131">Project task relationships</span></span>
<span data-ttu-id="949c0-132">Če želite zagotoviti uspešno nadgradnjo, morate ustrezno ohraniti naslednje odnose:</span><span class="sxs-lookup"><span data-stu-id="949c0-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="949c0-133">Vsa povezana opravila morajo biti povezana z istim projektom.</span><span class="sxs-lookup"><span data-stu-id="949c0-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="949c0-134">Vsako opravilo vrstice mora imeti nadrejeno opravilo.</span><span class="sxs-lookup"><span data-stu-id="949c0-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="949c0-135">Vsako opravilo mora imeti nadrejeni projekt.</span><span class="sxs-lookup"><span data-stu-id="949c0-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="949c0-136">Veljavni pogoji</span><span class="sxs-lookup"><span data-stu-id="949c0-136">Valid conditions</span></span>

- <span data-ttu-id="949c0-137">Vsa opravila morajo trajati točno ali dlje kot (> =) eno uro in manj kot 1.800.000 minut (1.250 dni).\*</span><span class="sxs-lookup"><span data-stu-id="949c0-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="949c0-138">Vsa opravila morajo imeti začetni datum od 1. 1. 2000.\*</span><span class="sxs-lookup"><span data-stu-id="949c0-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="949c0-139">Vsa opravila morajo imeti začetni datum najkasneje 17 let od današnjega dne.\*</span><span class="sxs-lookup"><span data-stu-id="949c0-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="949c0-140">Vsa opravila morajo imeti začetni datum pred končnim datumom ali na isti dan.</span><span class="sxs-lookup"><span data-stu-id="949c0-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="949c0-141">Vse vrste transakcij za klasifikacije (stroški, material, davek in čas) morajo imeti določene vrednosti za **Privzeta enota** in **Skupina enot**.</span><span class="sxs-lookup"><span data-stu-id="949c0-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="949c0-142">Izogibajte se črkovnem zapisu datuma.</span><span class="sxs-lookup"><span data-stu-id="949c0-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="949c0-143">Možni koraki za ublažitev</span><span class="sxs-lookup"><span data-stu-id="949c0-143">Potential mitigation steps</span></span>
- <span data-ttu-id="949c0-144">Z uporabo naprednega iskanja identificirajte projektna opravila, ki ne vsebujejo ID-ja projekta.</span><span class="sxs-lookup"><span data-stu-id="949c0-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="949c0-145">Z uporabo naprednega iskanja identificirajte projektna opravila, kjer je načrtovano trajanje večje od > 1.800.000.</span><span class="sxs-lookup"><span data-stu-id="949c0-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="949c0-146">Pred kakršnimi koli spremembami morate raziskati vse prilagoditve, povezane z entiteto, zaradi katerih bi lahko podatki prispeli v slabo stanje.</span><span class="sxs-lookup"><span data-stu-id="949c0-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="949c0-147">Te prilagoditve je treba obravnavati, preden nadaljujete s kakršnimi koli posodobitvami, povezanimi s podatki.</span><span class="sxs-lookup"><span data-stu-id="949c0-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="949c0-148">Pri identificiranih opravilih, ki so bila zapuščena, razmislite o brisanju teh opravil, če niso potrebna ali če bi morala biti povezana s pravilnim nadrejenim projektom.</span><span class="sxs-lookup"><span data-stu-id="949c0-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="949c0-149">Za vsa opravila, kjer trajanje presega 1.250 dni, razmislite o dodajanju več opravil, ki predstavljajo skupno trajanje, če je izvedljivo.</span><span class="sxs-lookup"><span data-stu-id="949c0-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="949c0-150">Elementi, označeni z zvezdico (\*), so omejeni, ker sistem za upravljanje odnosov s strankami (CRM) podpira le 7.320 ponovitev razširitev.</span><span class="sxs-lookup"><span data-stu-id="949c0-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="949c0-151">Ostati morate pod to omejitvijo.</span><span class="sxs-lookup"><span data-stu-id="949c0-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="949c0-152">Odnosi dodelitev virov</span><span class="sxs-lookup"><span data-stu-id="949c0-152">Resource Assignment relationships</span></span>
<span data-ttu-id="949c0-153">Če želite zagotoviti uspešno nadgradnjo, morate ustrezno ohraniti naslednje odnose:</span><span class="sxs-lookup"><span data-stu-id="949c0-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="949c0-154">Vse dodelitve virov v strukturirani členitvi dela morajo biti povezane z istim projektom.</span><span class="sxs-lookup"><span data-stu-id="949c0-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="949c0-155">Vse dodelitve virov v strukturirani členitvi dela morajo biti povezane s člani projektne ekipe v istem projektu.</span><span class="sxs-lookup"><span data-stu-id="949c0-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="949c0-156">Možni koraki za ublažitev</span><span class="sxs-lookup"><span data-stu-id="949c0-156">Potential mitigation steps</span></span>
- <span data-ttu-id="949c0-157">Identificirajte vsa opravila, ki so zunaj zgoraj opisanih pogojev.</span><span class="sxs-lookup"><span data-stu-id="949c0-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="949c0-158">Vse dodelitve virov, ki niso več veljavne, je treba izbrisati.</span><span class="sxs-lookup"><span data-stu-id="949c0-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="949c0-159">Odnosi pri odvisnostih projektnega opravila</span><span class="sxs-lookup"><span data-stu-id="949c0-159">Project task dependency relationships</span></span>
<span data-ttu-id="949c0-160">Če želite zagotoviti uspešno nadgradnjo, morate ustrezno ohraniti naslednje odnose:</span><span class="sxs-lookup"><span data-stu-id="949c0-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="949c0-161">Vse odvisnosti projektnih opravil morajo biti povezane z istim projektom.</span><span class="sxs-lookup"><span data-stu-id="949c0-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="949c0-162">Opravilo ne more imeti več kot enega sklica na odvisnost.</span><span class="sxs-lookup"><span data-stu-id="949c0-162">A task can't have the same dependency referenced more than once.</span></span>
