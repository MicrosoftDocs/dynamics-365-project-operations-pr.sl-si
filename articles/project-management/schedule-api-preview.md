---
title: Uporaba API-jev razporeda za izvajanje opravil z entitetami razporejanja
description: Ta tema vsebuje informacije in vzorce za uporabo API-jev razporeda.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868149"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="be161-103">Uporaba API-jev razporeda za izvajanje opravil z entitetami razporejanja</span><span class="sxs-lookup"><span data-stu-id="be161-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="be161-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="be161-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="be161-105">Nekatere ali vse funkcije, navedene v tej temi, so na voljo kot del izdaje predogledne različice.</span><span class="sxs-lookup"><span data-stu-id="be161-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="be161-106">Vsebina in funkcionalnost se lahko spremenita.</span><span class="sxs-lookup"><span data-stu-id="be161-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="be161-107">Entitete za razporejanje</span><span class="sxs-lookup"><span data-stu-id="be161-107">Scheduling entities</span></span>

<span data-ttu-id="be161-108">API-ji razporeda omogočajo izvajanje postopkov ustvarjanja, posodabljanja in brisanja z **entitetami razporeda**.</span><span class="sxs-lookup"><span data-stu-id="be161-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="be161-109">Te entitete upravljamo prek mehanizma za razporejanje v projektu za splet.</span><span class="sxs-lookup"><span data-stu-id="be161-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="be161-110">Postopki ustvarjanja, posodabljanja in brisanja z **entitetami razporejanja** so bili prej omejeni v prejšnjih izdajah Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="be161-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="be161-111">Naslednja tabela vsebuje celoten seznam **entitet razporejanja**.</span><span class="sxs-lookup"><span data-stu-id="be161-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="be161-112">Ime entitete</span><span class="sxs-lookup"><span data-stu-id="be161-112">Entity name</span></span>  | <span data-ttu-id="be161-113">Logično ime entitete</span><span class="sxs-lookup"><span data-stu-id="be161-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="be161-114">Project</span><span class="sxs-lookup"><span data-stu-id="be161-114">Project</span></span> | <span data-ttu-id="be161-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="be161-115">msdyn_project</span></span> |
| <span data-ttu-id="be161-116">Projektno opravilo</span><span class="sxs-lookup"><span data-stu-id="be161-116">Project Task</span></span>  | <span data-ttu-id="be161-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="be161-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="be161-118">Odvisnost projektnega opravila</span><span class="sxs-lookup"><span data-stu-id="be161-118">Project Task Dependency</span></span>  | <span data-ttu-id="be161-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="be161-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="be161-120">Dodelitev vira</span><span class="sxs-lookup"><span data-stu-id="be161-120">Resource Assignment</span></span> | <span data-ttu-id="be161-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="be161-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="be161-122">Vedro projekta</span><span class="sxs-lookup"><span data-stu-id="be161-122">Project Bucket</span></span>  | <span data-ttu-id="be161-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="be161-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="be161-124">Član projektne ekipe</span><span class="sxs-lookup"><span data-stu-id="be161-124">Project Team Member</span></span> | <span data-ttu-id="be161-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="be161-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="be161-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="be161-126">OperationSet</span></span>

<span data-ttu-id="be161-127">OperationSet je vzorec enote dela, ki se lahko uporablja, kadar je treba v transakciji obdelati več zahtev, ki vplivajo na urnik.</span><span class="sxs-lookup"><span data-stu-id="be161-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="be161-128">Načrtovanje API-jev</span><span class="sxs-lookup"><span data-stu-id="be161-128">Schedule APIs</span></span>

<span data-ttu-id="be161-129">Sledi seznam trenutnih API-jev razporeda.</span><span class="sxs-lookup"><span data-stu-id="be161-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="be161-130">**msdyn_CreateProjectV1**: ta API se lahko uporablja za ustvarjanje projekta.</span><span class="sxs-lookup"><span data-stu-id="be161-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="be161-131">Projekt in privzeto vedro projekta se ustvarita takoj.</span><span class="sxs-lookup"><span data-stu-id="be161-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="be161-132">**msdyn_CreateTeamMemberV1**: ta API se lahko uporablja za ustvarjanje člana projektne skupine.</span><span class="sxs-lookup"><span data-stu-id="be161-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="be161-133">Zapis člana ekipe se ustvari takoj.</span><span class="sxs-lookup"><span data-stu-id="be161-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="be161-134">**msdyn_CreateOperationSetV1**: ta API se lahko uporablja za razporejanje več zahtev, ki jih je treba izvesti znotraj transakcije.</span><span class="sxs-lookup"><span data-stu-id="be161-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="be161-135">**msdyn_PSSCreateV1**: ta API se lahko uporablja za ustvarjanje entitete.</span><span class="sxs-lookup"><span data-stu-id="be161-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="be161-136">Entiteta je lahko katera koli entiteta razporejanja, ki podpira postopek ustvarjanja.</span><span class="sxs-lookup"><span data-stu-id="be161-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="be161-137">**msdyn_PSSUpdateV1**: ta API se lahko uporablja za posodabljanje entitete.</span><span class="sxs-lookup"><span data-stu-id="be161-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="be161-138">Entiteta je lahko katera koli entiteta razporejanja, ki podpira postopek posodabljanja.</span><span class="sxs-lookup"><span data-stu-id="be161-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="be161-139">**msdyn_PSSDeleteV1**: ta API se lahko uporablja za brisanje entitete.</span><span class="sxs-lookup"><span data-stu-id="be161-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="be161-140">Entiteta je lahko katera koli entiteta razporejanja, ki podpira postopek brisanja.</span><span class="sxs-lookup"><span data-stu-id="be161-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="be161-141">**msdyn_ExecuteOperationSetV1**: ta API se uporablja za izvajanje vseh postopkov znotraj danega nabora postopkov.</span><span class="sxs-lookup"><span data-stu-id="be161-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="be161-142">Uporaba API-jev razporeda s funkcijo OperationSet</span><span class="sxs-lookup"><span data-stu-id="be161-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="be161-143">Ker se zapisi, ki vsebujejo **CreateProjectV1** in **CreateTeamMemberV1**, ustvarijo takoj, teh API-jev ni mogoče neposredno uporabljati pri funkciji **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="be161-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="be161-144">Vendar pa lahko API uporabite za ustvarjanje potrebnih zapisov, ustvarite **OperationSet** in nato uporabite te vnaprej ustvarjene zapise pri funkciji **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="be161-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="be161-145">Podprti postopki</span><span class="sxs-lookup"><span data-stu-id="be161-145">Supported operations</span></span>

| <span data-ttu-id="be161-146">Entiteta za razporejanje</span><span class="sxs-lookup"><span data-stu-id="be161-146">Scheduling entity</span></span> | <span data-ttu-id="be161-147">Ustvari</span><span class="sxs-lookup"><span data-stu-id="be161-147">Create</span></span> | <span data-ttu-id="be161-148">Posodabljanje</span><span class="sxs-lookup"><span data-stu-id="be161-148">Update</span></span> | <span data-ttu-id="be161-149">Delete</span><span class="sxs-lookup"><span data-stu-id="be161-149">Delete</span></span> | <span data-ttu-id="be161-150">Pomembni premisleki</span><span class="sxs-lookup"><span data-stu-id="be161-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="be161-151">Projektno opravilo</span><span class="sxs-lookup"><span data-stu-id="be161-151">Project task</span></span> | <span data-ttu-id="be161-152">Da</span><span class="sxs-lookup"><span data-stu-id="be161-152">Yes</span></span> | <span data-ttu-id="be161-153">Da</span><span class="sxs-lookup"><span data-stu-id="be161-153">Yes</span></span> | <span data-ttu-id="be161-154">Da</span><span class="sxs-lookup"><span data-stu-id="be161-154">Yes</span></span> | <span data-ttu-id="be161-155">Brez</span><span class="sxs-lookup"><span data-stu-id="be161-155">None</span></span> |
| <span data-ttu-id="be161-156">Odvisnost projektnega opravila</span><span class="sxs-lookup"><span data-stu-id="be161-156">Project task dependency</span></span> | <span data-ttu-id="be161-157">Da</span><span class="sxs-lookup"><span data-stu-id="be161-157">Yes</span></span> | <span data-ttu-id="be161-158">Da</span><span class="sxs-lookup"><span data-stu-id="be161-158">Yes</span></span> | | <span data-ttu-id="be161-159">Zapisi odvisnosti od projektne naloge se ne posodabljajo.</span><span class="sxs-lookup"><span data-stu-id="be161-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="be161-160">Namesto tega lahko stari zapis izbrišete in ustvarite novega.</span><span class="sxs-lookup"><span data-stu-id="be161-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="be161-161">Dodelitev vira</span><span class="sxs-lookup"><span data-stu-id="be161-161">Resource assignment</span></span> | <span data-ttu-id="be161-162">Da</span><span class="sxs-lookup"><span data-stu-id="be161-162">Yes</span></span> | <span data-ttu-id="be161-163">Da</span><span class="sxs-lookup"><span data-stu-id="be161-163">Yes</span></span> | | <span data-ttu-id="be161-164">Postopki z naslednjimi polji niso podprti: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** in **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="be161-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="be161-165">Zapisi o dodeljevanju virov niso posodobljeni.</span><span class="sxs-lookup"><span data-stu-id="be161-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="be161-166">Namesto tega lahko stari zapis izbrišete in ustvarite novega.</span><span class="sxs-lookup"><span data-stu-id="be161-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="be161-167">Vedro projekta</span><span class="sxs-lookup"><span data-stu-id="be161-167">Project bucket</span></span> | <span data-ttu-id="be161-168">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="be161-168">N/A</span></span> | <span data-ttu-id="be161-169">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="be161-169">N/A</span></span> | <span data-ttu-id="be161-170">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="be161-170">N/A</span></span> | <span data-ttu-id="be161-171">Privzeto vedro je ustvarjeno z API-jem **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="be161-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="be161-172">Član projektne ekipe</span><span class="sxs-lookup"><span data-stu-id="be161-172">Project team member</span></span> | <span data-ttu-id="be161-173">Da</span><span class="sxs-lookup"><span data-stu-id="be161-173">Yes</span></span> | <span data-ttu-id="be161-174">Da</span><span class="sxs-lookup"><span data-stu-id="be161-174">Yes</span></span> | <span data-ttu-id="be161-175">Da</span><span class="sxs-lookup"><span data-stu-id="be161-175">Yes</span></span> | <span data-ttu-id="be161-176">Za postopek ustvarjanja uporabite API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="be161-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="be161-177">Project</span><span class="sxs-lookup"><span data-stu-id="be161-177">Project</span></span> | <span data-ttu-id="be161-178">Da</span><span class="sxs-lookup"><span data-stu-id="be161-178">Yes</span></span> | <span data-ttu-id="be161-179">Da</span><span class="sxs-lookup"><span data-stu-id="be161-179">Yes</span></span> | <span data-ttu-id="be161-180">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="be161-180">N/A</span></span> | <span data-ttu-id="be161-181">Postopki z naslednjimi polji niso podprti: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** in **Duration**.</span><span class="sxs-lookup"><span data-stu-id="be161-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="be161-182">Te API-je je mogoče priklicati s predmeti entitete, ki vključujejo polja po meri.</span><span class="sxs-lookup"><span data-stu-id="be161-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="be161-183">Lastnost ID ni obvezna.</span><span class="sxs-lookup"><span data-stu-id="be161-183">The ID property is optional.</span></span> <span data-ttu-id="be161-184">Če je na voljo, ga sistem poskuša uporabiti in zavrže izjemo, če je ni mogoče uporabiti.</span><span class="sxs-lookup"><span data-stu-id="be161-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="be161-185">Če ni na voljo, ga bo sistem ustvaril.</span><span class="sxs-lookup"><span data-stu-id="be161-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="be161-186">Omejitve in znane težave</span><span class="sxs-lookup"><span data-stu-id="be161-186">Limitations and known issues</span></span>
<span data-ttu-id="be161-187">Sledi seznam omejitev in znanih težav:</span><span class="sxs-lookup"><span data-stu-id="be161-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="be161-188">API-je razporeda lahko uporabljajo samo **uporabniki z licenco Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="be161-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="be161-189">Ne morejo jih uporabljati:</span><span class="sxs-lookup"><span data-stu-id="be161-189">They can't be used by:</span></span>
    - <span data-ttu-id="be161-190">Uporabniki aplikacij</span><span class="sxs-lookup"><span data-stu-id="be161-190">Application users</span></span>
    - <span data-ttu-id="be161-191">Uporabniki sistema</span><span class="sxs-lookup"><span data-stu-id="be161-191">System users</span></span>
    - <span data-ttu-id="be161-192">Uporabniki integracije</span><span class="sxs-lookup"><span data-stu-id="be161-192">Integration users</span></span>
    - <span data-ttu-id="be161-193">Drugi uporabniki, ki nimajo zahtevane licence</span><span class="sxs-lookup"><span data-stu-id="be161-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="be161-194">Vsak **OperationSet** ima lahko največ 100 postopkov.</span><span class="sxs-lookup"><span data-stu-id="be161-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="be161-195">Vsak uporabnik ima lahko odprtih največ 10 postopkov **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="be161-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="be161-196">Project Operations trenutno podpira največ 500 skupnih opravil na projektu.</span><span class="sxs-lookup"><span data-stu-id="be161-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="be161-197">Stanje napake in dnevniki napak **OperationSet** trenutno niso na voljo.</span><span class="sxs-lookup"><span data-stu-id="be161-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="be161-198">API-ji razporeda so na voljo pri predogledni različici za javnost.</span><span class="sxs-lookup"><span data-stu-id="be161-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="be161-199">Microsoft ne podpira uporabe teh API-jev v produkcijskem okolju.</span><span class="sxs-lookup"><span data-stu-id="be161-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="be161-200">Vzorčni scenarij</span><span class="sxs-lookup"><span data-stu-id="be161-200">Sample scenario</span></span>

<span data-ttu-id="be161-201">V tem primeru boste ustvarili projekt, člana ekipe, štiri opravila in dve dodelitvi virov.</span><span class="sxs-lookup"><span data-stu-id="be161-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="be161-202">Nato boste posodobili eno opravilo, posodobili projekt, izbrisali eno opravilo, izbrisali eno dodelitev vira in ustvarili odvisnost od opravila.</span><span class="sxs-lookup"><span data-stu-id="be161-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="be161-203">Dodatni vzorci</span><span class="sxs-lookup"><span data-stu-id="be161-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
