---
title: Spremembe upravljanja virov (Project Service Automation 3.x)
description: Ta tema vsebuje informacije o spremembah Območja za upravljanje virov.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5f88d7309a5e1171629a72e749bfc01abb64c62a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284783"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="599c6-103">Spremembe upravljanja virov (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="599c6-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="599c6-104">Posamezni razdelki te teme vsebujejo informacije o spremembah Območja za upravljanje virov aplikacije Dynamics 365 Project Service Automation, različica 3.x.</span><span class="sxs-lookup"><span data-stu-id="599c6-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="599c6-105">Projektne ocene</span><span class="sxs-lookup"><span data-stu-id="599c6-105">Project estimates</span></span>

<span data-ttu-id="599c6-106">Namesto da bi bile projektne ocene narejene na podlagi entitete **msdyn\_projecttask** (**Projektno opravilo**), so narejene na podlagi entitete **msdyn\_resourceassignment** (**Dodelitev vira**).</span><span class="sxs-lookup"><span data-stu-id="599c6-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="599c6-107">Dodelitve virov so postale »vir resničnosti« za razporejanje opravil in določanje cen.</span><span class="sxs-lookup"><span data-stu-id="599c6-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="599c6-108">Opravila vrstic</span><span class="sxs-lookup"><span data-stu-id="599c6-108">Line tasks</span></span>

<span data-ttu-id="599c6-109">V PSA 3.x so opravila vrstic zastarela.</span><span class="sxs-lookup"><span data-stu-id="599c6-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="599c6-110">Dodelitve zdaj kažejo na celotno opravilo in ne le na opravila vrstic.</span><span class="sxs-lookup"><span data-stu-id="599c6-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="599c6-111">Spodnji primer prikazuje, kako je opravilo, imenovano »Opravilo preizkusa«, dodeljeno članom skupine A in B v starejših različicah PSA in PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="599c6-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="599c6-112">**Pred PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="599c6-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="599c6-113">Opravilo preizkusa</span><span class="sxs-lookup"><span data-stu-id="599c6-113">Test task</span></span>

        - <span data-ttu-id="599c6-114">Opravilo preizkusa – opravilo vrstice 1</span><span class="sxs-lookup"><span data-stu-id="599c6-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="599c6-115">Dodelitev skupini A</span><span class="sxs-lookup"><span data-stu-id="599c6-115">Assignment to A</span></span>

        - <span data-ttu-id="599c6-116">Opravilo preizkusa – opravilo vrstice 2</span><span class="sxs-lookup"><span data-stu-id="599c6-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="599c6-117">Dodelitev skupini B</span><span class="sxs-lookup"><span data-stu-id="599c6-117">Assignment to B</span></span>

- <span data-ttu-id="599c6-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="599c6-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="599c6-119">Opravilo preizkusa</span><span class="sxs-lookup"><span data-stu-id="599c6-119">Test task</span></span>

        - <span data-ttu-id="599c6-120">Dodelitev skupini A</span><span class="sxs-lookup"><span data-stu-id="599c6-120">Assignment to A</span></span>
        - <span data-ttu-id="599c6-121">Dodelitev skupini B</span><span class="sxs-lookup"><span data-stu-id="599c6-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="599c6-122">Nedodeljena dodelitev</span><span class="sxs-lookup"><span data-stu-id="599c6-122">Unassigned assignment</span></span>

<span data-ttu-id="599c6-123">V različici PSA 3.x je nedodeljena dodelitev tista, ki je dodeljena članu ekipe z vrednostjo **NULL** in viru z vrednostjo **NULL**.</span><span class="sxs-lookup"><span data-stu-id="599c6-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="599c6-124">Nedodeljene dodelitve se lahko pojavijo v spodaj naštetih primerih:</span><span class="sxs-lookup"><span data-stu-id="599c6-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="599c6-125">Nedodeljena dodelitev se vedno ustvari, če je bilo opravilo ustvarjeno, vendar še ni bilo dodeljeno nobenemu članu ekipe.</span><span class="sxs-lookup"><span data-stu-id="599c6-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="599c6-126">Nedodeljena dodelitev se ponovno ustvari, če so odstranjeni vsi pooblaščenci posameznega opravila.</span><span class="sxs-lookup"><span data-stu-id="599c6-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="599c6-127">Polja za načrtovanje v entiteti »Projektno opravilo«</span><span class="sxs-lookup"><span data-stu-id="599c6-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="599c6-128">Polja v entiteti **msdyn\_projecttask** so zastarela ali premaknjena v entiteto **msdyn\_resourceassignment** oziroma se nanje sklicuje entiteta **msdyn\_projectteam** (**Član projektne ekipe**).</span><span class="sxs-lookup"><span data-stu-id="599c6-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="599c6-129">Zastarelo polje v msdyn\_projecttask (projektno opravilo)</span><span class="sxs-lookup"><span data-stu-id="599c6-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="599c6-130">Novo polje v msdyn\_resourcedodelitve (dodelitev vira)</span><span class="sxs-lookup"><span data-stu-id="599c6-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="599c6-131">Pripomba</span><span class="sxs-lookup"><span data-stu-id="599c6-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="599c6-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="599c6-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="599c6-133">Ni priprav ali omejitev</span><span class="sxs-lookup"><span data-stu-id="599c6-133">None</span></span> | |
| <span data-ttu-id="599c6-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="599c6-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="599c6-135">Ni priprav ali omejitev</span><span class="sxs-lookup"><span data-stu-id="599c6-135">None</span></span> | |
| <span data-ttu-id="599c6-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="599c6-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="599c6-137">Ni priprav ali omejitev</span><span class="sxs-lookup"><span data-stu-id="599c6-137">None</span></span> | |
| <span data-ttu-id="599c6-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="599c6-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="599c6-139">Ni priprav ali omejitev</span><span class="sxs-lookup"><span data-stu-id="599c6-139">None</span></span> | |
| <span data-ttu-id="599c6-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="599c6-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="599c6-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="599c6-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="599c6-142">Oblika podatkovne strukture JavaScript Object Notation (JSON), ki je shranjena v polju, je bila spremenjena.</span><span class="sxs-lookup"><span data-stu-id="599c6-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="599c6-143">Krivulja razporeda</span><span class="sxs-lookup"><span data-stu-id="599c6-143">Schedule contour</span></span>

<span data-ttu-id="599c6-144">Krivulja razporeda je shranjena v polju **Načrtovano delo** (**msdyn\_plannedwork**) za vsako entiteto **Dodelitev vira** posebej (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="599c6-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="599c6-145">Struktura</span><span class="sxs-lookup"><span data-stu-id="599c6-145">Structure</span></span>

<span data-ttu-id="599c6-146">Nova struktura krivulje razporeda je sestavljena iz prilagodljivih časovnih rezin, ki so definirane za vsak dan razporeda.</span><span class="sxs-lookup"><span data-stu-id="599c6-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="599c6-147">Vsaka časovna rezina ima naslednje lastnosti:</span><span class="sxs-lookup"><span data-stu-id="599c6-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="599c6-148">**Začetek** – začetek delovnega časa za posamezni dan glede na projektni koledar.</span><span class="sxs-lookup"><span data-stu-id="599c6-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="599c6-149">**Konec** – konec delovnega časa za posamezni dan glede na projektni koledar.</span><span class="sxs-lookup"><span data-stu-id="599c6-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="599c6-150">**Ure** – število dodeljenih ur za posamezni dan.</span><span class="sxs-lookup"><span data-stu-id="599c6-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="599c6-151">**Primer**</span><span class="sxs-lookup"><span data-stu-id="599c6-151">**Example**</span></span>

<span data-ttu-id="599c6-152">Ta primer uporablja projektni koledar, kjer delovni dan traja od 9.00 do 17.00 v časovnem pasu UTC-8.</span><span class="sxs-lookup"><span data-stu-id="599c6-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="599c6-153">Samodejno in ročno razporejanje</span><span class="sxs-lookup"><span data-stu-id="599c6-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="599c6-154">Če je opravilo samodejno razporejeno, se ure naložijo vnaprej, trajanje opravila pa se lahko zmanjša.</span><span class="sxs-lookup"><span data-stu-id="599c6-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="599c6-155">**Primer**</span><span class="sxs-lookup"><span data-stu-id="599c6-155">**Example**</span></span>

<span data-ttu-id="599c6-156">Spodnji primer prikazuje opravilo, ki je bilo samodejno razporejeno za 18 ur v treh dneh (od 3. decembra 2018 do 5. decembra 2018).</span><span class="sxs-lookup"><span data-stu-id="599c6-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="599c6-157">Če je opravilo ročno razporejeno, se ure enakomerno porazdelijo na vse datume.</span><span class="sxs-lookup"><span data-stu-id="599c6-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="599c6-158">**Primer**</span><span class="sxs-lookup"><span data-stu-id="599c6-158">**Example**</span></span>

<span data-ttu-id="599c6-159">Spodnji primer prikazuje opravilo, ki je bilo ročno razporejeno za 18 ur v treh dneh (od 3. decembra 2018 do 5. decembra 2018).</span><span class="sxs-lookup"><span data-stu-id="599c6-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="599c6-160">Enota dodelitve</span><span class="sxs-lookup"><span data-stu-id="599c6-160">Assignment unit</span></span>

<span data-ttu-id="599c6-161">Enota dodelitve je bila v PSA 3.x opuščena.</span><span class="sxs-lookup"><span data-stu-id="599c6-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="599c6-162">Ure potrebnega dela za opravilo se zdaj enakomerno porazdelijo po dneh za vse dodeljene vire.</span><span class="sxs-lookup"><span data-stu-id="599c6-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="599c6-163">**Primer**</span><span class="sxs-lookup"><span data-stu-id="599c6-163">**Example**</span></span>

<span data-ttu-id="599c6-164">V tem primeru je opravilo dodeljeno dvema viroma in samodejno razporejeno za 36 ur v treh dneh (od 3. decembra 2018 do 5. decembra 2018).</span><span class="sxs-lookup"><span data-stu-id="599c6-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="599c6-165">Dodelitev 1:</span><span class="sxs-lookup"><span data-stu-id="599c6-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="599c6-166">Dodelitev 2:</span><span class="sxs-lookup"><span data-stu-id="599c6-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="599c6-167">Cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="599c6-167">Pricing dimensions</span></span>

<span data-ttu-id="599c6-168">V PSA 3.x so bila polja cenovnih razsežnosti za posamezne vire (kot sta **Vloga** in **Organizacijska enota**) odstranjena iz entitete **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="599c6-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="599c6-169">Ta polja je zdaj mogoče pridobiti od posameznega člana projektne skupine (**msdyn\_projectteam**) dodelitve vira (**msdyn\_resourceassignment**), ko so ustvarjene ocene projekta.</span><span class="sxs-lookup"><span data-stu-id="599c6-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="599c6-170">Novo polje **msdyn\_organizationalunit** je bilo dodano entiteti **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="599c6-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="599c6-171">Zastarelo polje v msdyn\_projecttask (projektno opravilo)</span><span class="sxs-lookup"><span data-stu-id="599c6-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="599c6-172">Polje iz msdyn\_projectteam (Član projektne skupine), ki se uporablja v zameno</span><span class="sxs-lookup"><span data-stu-id="599c6-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="599c6-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="599c6-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="599c6-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="599c6-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="599c6-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="599c6-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="599c6-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="599c6-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="599c6-177">Krivulje</span><span class="sxs-lookup"><span data-stu-id="599c6-177">Contours</span></span>

<span data-ttu-id="599c6-178">Polja s krivuljami cen in ocen so bila opuščena v entiteti **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="599c6-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="599c6-179">Premaknjena so bila v entiteto **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="599c6-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="599c6-180">Zastarelo polje v msdyn\_projecttask (projektno opravilo)</span><span class="sxs-lookup"><span data-stu-id="599c6-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="599c6-181">Novo polje v msdyn\_resourcedodelitve (dodelitev vira)</span><span class="sxs-lookup"><span data-stu-id="599c6-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="599c6-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="599c6-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="599c6-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="599c6-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="599c6-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="599c6-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="599c6-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="599c6-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="599c6-186">Entiteti **msdyn\_resourceassignment** so bila dodana naslednja polja:</span><span class="sxs-lookup"><span data-stu-id="599c6-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="599c6-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="599c6-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="599c6-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="599c6-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="599c6-189">Entiteta **msdyn\_projecttask** ima nespremenjena spodaj našteta polja za načrtovane, dejanske in preostale stroške ter prodajo:</span><span class="sxs-lookup"><span data-stu-id="599c6-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="599c6-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="599c6-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="599c6-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="599c6-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="599c6-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="599c6-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="599c6-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="599c6-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="599c6-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="599c6-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="599c6-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="599c6-195">msdyn\_remainingsales</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]