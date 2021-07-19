---
title: Uporaba API-jev razporejanja projektov za izvajanje postopkov s pomočjo entitet razporejanja
description: V tej temi so na voljo informacije in vzorci za uporabo API-jev razporejanja projektov.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293247"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="f4ec9-103">Uporaba API-jev razporejanja projektov za izvajanje postopkov s pomočjo entitet razporejanja</span><span class="sxs-lookup"><span data-stu-id="f4ec9-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="f4ec9-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="f4ec9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="f4ec9-105">Nekatere ali vse funkcije, navedene v tej temi, so na voljo kot del izdaje predogledne različice.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="f4ec9-106">Vsebina in funkcionalnost se lahko spremenita.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="f4ec9-107">Entitete za razporejanje</span><span class="sxs-lookup"><span data-stu-id="f4ec9-107">Scheduling entities</span></span>

<span data-ttu-id="f4ec9-108">Uporaba API-jev razporejanja projektov ponuja možnost izvajanja postopkov ustvarjanja, posodabljanja in brisanja s pomočjo možnosti **Entitete razporejanja**.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="f4ec9-109">Te entitete upravljamo prek mehanizma za razporejanje v projektu za splet.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="f4ec9-110">Postopki ustvarjanja, posodabljanja in brisanja z **entitetami razporejanja** so bili prej omejeni v prejšnjih izdajah Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="f4ec9-111">Naslednja tabela vključuje celoten seznam entitet razporejanja projektov.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="f4ec9-112">Ime entitete</span><span class="sxs-lookup"><span data-stu-id="f4ec9-112">Entity name</span></span>  | <span data-ttu-id="f4ec9-113">Logično ime entitete</span><span class="sxs-lookup"><span data-stu-id="f4ec9-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="f4ec9-114">Project</span><span class="sxs-lookup"><span data-stu-id="f4ec9-114">Project</span></span> | <span data-ttu-id="f4ec9-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="f4ec9-115">msdyn_project</span></span> |
| <span data-ttu-id="f4ec9-116">Projektno opravilo</span><span class="sxs-lookup"><span data-stu-id="f4ec9-116">Project Task</span></span>  | <span data-ttu-id="f4ec9-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="f4ec9-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="f4ec9-118">Odvisnost projektnega opravila</span><span class="sxs-lookup"><span data-stu-id="f4ec9-118">Project Task Dependency</span></span>  | <span data-ttu-id="f4ec9-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="f4ec9-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="f4ec9-120">Dodelitev vira</span><span class="sxs-lookup"><span data-stu-id="f4ec9-120">Resource Assignment</span></span> | <span data-ttu-id="f4ec9-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="f4ec9-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="f4ec9-122">Vedro projekta</span><span class="sxs-lookup"><span data-stu-id="f4ec9-122">Project Bucket</span></span>  | <span data-ttu-id="f4ec9-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="f4ec9-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="f4ec9-124">Član projektne ekipe</span><span class="sxs-lookup"><span data-stu-id="f4ec9-124">Project Team Member</span></span> | <span data-ttu-id="f4ec9-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="f4ec9-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="f4ec9-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="f4ec9-126">OperationSet</span></span>

<span data-ttu-id="f4ec9-127">OperationSet je vzorec enote dela, ki se lahko uporablja, kadar je treba v transakciji obdelati več zahtev, ki vplivajo na urnik.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="f4ec9-128">API-ji razporejanja projektov</span><span class="sxs-lookup"><span data-stu-id="f4ec9-128">Project schedule APIs</span></span>

<span data-ttu-id="f4ec9-129">Naslednji seznam vsebuje trenutne API-je razporejanja projektov.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="f4ec9-130">**msdyn_CreateProjectV1**: ta API se lahko uporablja za ustvarjanje projekta.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="f4ec9-131">Projekt in privzeto vedro projekta se ustvarita takoj.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="f4ec9-132">**msdyn_CreateTeamMemberV1**: ta API se lahko uporablja za ustvarjanje člana projektne skupine.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="f4ec9-133">Zapis člana ekipe se ustvari takoj.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="f4ec9-134">**msdyn_CreateOperationSetV1**: ta API se lahko uporablja za razporejanje več zahtev, ki jih je treba izvesti znotraj transakcije.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="f4ec9-135">**msdyn_PSSCreateV1**: ta API se lahko uporablja za ustvarjanje entitete.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="f4ec9-136">Lahko gre za katerokoli entiteto razporejanja projektov, ki podpira postopek ustvarjanja.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="f4ec9-137">**msdyn_PSSUpdateV1**: ta API se lahko uporablja za posodabljanje entitete.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="f4ec9-138">Lahko gre za katerokoli entiteto razporejanja projektov, ki podpira postopek posodabljanja.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="f4ec9-139">**msdyn_PSSDeleteV1**: ta API se lahko uporablja za brisanje entitete.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="f4ec9-140">Lahko gre za katerokoli entiteto razporejanja projektov, ki podpira postopek brisanja.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="f4ec9-141">**msdyn_ExecuteOperationSetV1**: ta API se uporablja za izvajanje vseh postopkov znotraj danega nabora postopkov.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="f4ec9-142">Uporaba API-jev razporejanja projektov s funkcijo OperationSet</span><span class="sxs-lookup"><span data-stu-id="f4ec9-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="f4ec9-143">Ker se zapisi, ki vsebujejo **CreateProjectV1** in **CreateTeamMemberV1**, ustvarijo takoj, teh API-jev ni mogoče neposredno uporabljati pri funkciji **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="f4ec9-144">Vendar pa lahko API uporabite za ustvarjanje potrebnih zapisov, ustvarite **OperationSet** in nato uporabite te vnaprej ustvarjene zapise pri funkciji **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="f4ec9-145">Podprti postopki</span><span class="sxs-lookup"><span data-stu-id="f4ec9-145">Supported operations</span></span>

| <span data-ttu-id="f4ec9-146">Entiteta za razporejanje</span><span class="sxs-lookup"><span data-stu-id="f4ec9-146">Scheduling entity</span></span> | <span data-ttu-id="f4ec9-147">Ustvari</span><span class="sxs-lookup"><span data-stu-id="f4ec9-147">Create</span></span> | <span data-ttu-id="f4ec9-148">Posodabljanje</span><span class="sxs-lookup"><span data-stu-id="f4ec9-148">Update</span></span> | <span data-ttu-id="f4ec9-149">Delete</span><span class="sxs-lookup"><span data-stu-id="f4ec9-149">Delete</span></span> | <span data-ttu-id="f4ec9-150">Pomembni premisleki</span><span class="sxs-lookup"><span data-stu-id="f4ec9-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="f4ec9-151">Projektno opravilo</span><span class="sxs-lookup"><span data-stu-id="f4ec9-151">Project task</span></span> | <span data-ttu-id="f4ec9-152">Da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-152">Yes</span></span> | <span data-ttu-id="f4ec9-153">Da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-153">Yes</span></span> | <span data-ttu-id="f4ec9-154">Da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-154">Yes</span></span> | <span data-ttu-id="f4ec9-155">Brez</span><span class="sxs-lookup"><span data-stu-id="f4ec9-155">None</span></span> |
| <span data-ttu-id="f4ec9-156">Odvisnost projektnega opravila</span><span class="sxs-lookup"><span data-stu-id="f4ec9-156">Project task dependency</span></span> | <span data-ttu-id="f4ec9-157">Da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-157">Yes</span></span> | <span data-ttu-id="f4ec9-158">Da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-158">Yes</span></span> | | <span data-ttu-id="f4ec9-159">Zapisi odvisnosti od projektne naloge se ne posodabljajo.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="f4ec9-160">Namesto tega lahko stari zapis izbrišete in ustvarite novega.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="f4ec9-161">Dodelitev vira</span><span class="sxs-lookup"><span data-stu-id="f4ec9-161">Resource assignment</span></span> | <span data-ttu-id="f4ec9-162">Da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-162">Yes</span></span> | <span data-ttu-id="f4ec9-163">Da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-163">Yes</span></span> | | <span data-ttu-id="f4ec9-164">Postopki z naslednjimi polji niso podprti: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** in **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="f4ec9-165">Zapisi o dodeljevanju virov niso posodobljeni.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="f4ec9-166">Namesto tega lahko stari zapis izbrišete in ustvarite novega.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="f4ec9-167">Vedro projekta</span><span class="sxs-lookup"><span data-stu-id="f4ec9-167">Project bucket</span></span> | <span data-ttu-id="f4ec9-168">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f4ec9-168">N/A</span></span> | <span data-ttu-id="f4ec9-169">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f4ec9-169">N/A</span></span> | <span data-ttu-id="f4ec9-170">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f4ec9-170">N/A</span></span> | <span data-ttu-id="f4ec9-171">Privzeto vedro je ustvarjeno z API-jem **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="f4ec9-172">Član projektne ekipe</span><span class="sxs-lookup"><span data-stu-id="f4ec9-172">Project team member</span></span> | <span data-ttu-id="f4ec9-173">Da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-173">Yes</span></span> | <span data-ttu-id="f4ec9-174">Da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-174">Yes</span></span> | <span data-ttu-id="f4ec9-175">Da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-175">Yes</span></span> | <span data-ttu-id="f4ec9-176">Za postopek ustvarjanja uporabite API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="f4ec9-177">Project</span><span class="sxs-lookup"><span data-stu-id="f4ec9-177">Project</span></span> | <span data-ttu-id="f4ec9-178">Da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-178">Yes</span></span> | <span data-ttu-id="f4ec9-179">Da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-179">Yes</span></span> | <span data-ttu-id="f4ec9-180">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f4ec9-180">N/A</span></span> | <span data-ttu-id="f4ec9-181">Postopki z naslednjimi polji niso podprti: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** in **Duration**.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="f4ec9-182">Te API-je je mogoče priklicati s predmeti entitete, ki vključujejo polja po meri.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="f4ec9-183">Lastnost ID ni obvezna.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-183">The ID property is optional.</span></span> <span data-ttu-id="f4ec9-184">Če je na voljo, ga sistem poskuša uporabiti in zavrže izjemo, če je ni mogoče uporabiti.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="f4ec9-185">Če ni na voljo, ga bo sistem ustvaril.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="f4ec9-186">Omejena polja</span><span class="sxs-lookup"><span data-stu-id="f4ec9-186">Restricted fields</span></span>

<span data-ttu-id="f4ec9-187">Naslednje tabele določajo polja, za katera so omejene možnosti **Ustvari** in **Uredi.**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="f4ec9-188">Projektno opravilo</span><span class="sxs-lookup"><span data-stu-id="f4ec9-188">Project task</span></span>

| <span data-ttu-id="f4ec9-189">**Logično ime**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-189">**Logical name**</span></span>                       | <span data-ttu-id="f4ec9-190">**Možnost ustvarjanja**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-190">**Can create**</span></span> | <span data-ttu-id="f4ec9-191">**Možnost urejanja**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="f4ec9-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="f4ec9-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="f4ec9-193">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-193">no</span></span>             | <span data-ttu-id="f4ec9-194">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-194">no</span></span>               |
| <span data-ttu-id="f4ec9-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="f4ec9-196">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-196">no</span></span>             | <span data-ttu-id="f4ec9-197">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-197">no</span></span>               |
| <span data-ttu-id="f4ec9-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="f4ec9-198">msdyn_actualend</span></span>                        | <span data-ttu-id="f4ec9-199">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-199">no</span></span>             | <span data-ttu-id="f4ec9-200">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-200">no</span></span>               |
| <span data-ttu-id="f4ec9-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="f4ec9-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="f4ec9-202">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-202">no</span></span>             | <span data-ttu-id="f4ec9-203">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-203">no</span></span>               |
| <span data-ttu-id="f4ec9-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="f4ec9-205">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-205">no</span></span>             | <span data-ttu-id="f4ec9-206">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-206">no</span></span>               |
| <span data-ttu-id="f4ec9-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="f4ec9-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="f4ec9-208">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-208">no</span></span>             | <span data-ttu-id="f4ec9-209">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-209">no</span></span>               |
| <span data-ttu-id="f4ec9-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="f4ec9-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="f4ec9-211">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-211">no</span></span>             | <span data-ttu-id="f4ec9-212">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-212">no</span></span>               |
| <span data-ttu-id="f4ec9-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="f4ec9-214">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-214">no</span></span>             | <span data-ttu-id="f4ec9-215">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-215">no</span></span>               |
| <span data-ttu-id="f4ec9-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="f4ec9-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="f4ec9-217">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-217">no</span></span>             | <span data-ttu-id="f4ec9-218">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-218">no</span></span>               |
| <span data-ttu-id="f4ec9-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f4ec9-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="f4ec9-220">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-220">no</span></span>             | <span data-ttu-id="f4ec9-221">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-221">no</span></span>               |
| <span data-ttu-id="f4ec9-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="f4ec9-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="f4ec9-223">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-223">no</span></span>             | <span data-ttu-id="f4ec9-224">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-224">no</span></span>               |
| <span data-ttu-id="f4ec9-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="f4ec9-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="f4ec9-226">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-226">no</span></span>             | <span data-ttu-id="f4ec9-227">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-227">no</span></span>               |
| <span data-ttu-id="f4ec9-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="f4ec9-229">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-229">no</span></span>             | <span data-ttu-id="f4ec9-230">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-230">no</span></span>               |
| <span data-ttu-id="f4ec9-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="f4ec9-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="f4ec9-232">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-232">no</span></span>             | <span data-ttu-id="f4ec9-233">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-233">no</span></span>               |
| <span data-ttu-id="f4ec9-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="f4ec9-235">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-235">no</span></span>             | <span data-ttu-id="f4ec9-236">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-236">no</span></span>               |
| <span data-ttu-id="f4ec9-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="f4ec9-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="f4ec9-238">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-238">no</span></span>             | <span data-ttu-id="f4ec9-239">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-239">no</span></span>               |
| <span data-ttu-id="f4ec9-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="f4ec9-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="f4ec9-241">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-241">no</span></span>             | <span data-ttu-id="f4ec9-242">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-242">no</span></span>               |
| <span data-ttu-id="f4ec9-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="f4ec9-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="f4ec9-244">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-244">no</span></span>             | <span data-ttu-id="f4ec9-245">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-245">no</span></span>               |
| <span data-ttu-id="f4ec9-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="f4ec9-247">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-247">no</span></span>             | <span data-ttu-id="f4ec9-248">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-248">no</span></span>               |
| <span data-ttu-id="f4ec9-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="f4ec9-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="f4ec9-250">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-250">no</span></span>             | <span data-ttu-id="f4ec9-251">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-251">no</span></span>               |
| <span data-ttu-id="f4ec9-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="f4ec9-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="f4ec9-253">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-253">no</span></span>             | <span data-ttu-id="f4ec9-254">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-254">no</span></span>               |
| <span data-ttu-id="f4ec9-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="f4ec9-256">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-256">no</span></span>             | <span data-ttu-id="f4ec9-257">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-257">no</span></span>               |
| <span data-ttu-id="f4ec9-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="f4ec9-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="f4ec9-259">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-259">no</span></span>             | <span data-ttu-id="f4ec9-260">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-260">no</span></span>               |
| <span data-ttu-id="f4ec9-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="f4ec9-262">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-262">no</span></span>             | <span data-ttu-id="f4ec9-263">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-263">no</span></span>               |
| <span data-ttu-id="f4ec9-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="f4ec9-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="f4ec9-265">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-265">no</span></span>             | <span data-ttu-id="f4ec9-266">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-266">no</span></span>               |
| <span data-ttu-id="f4ec9-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="f4ec9-267">msdyn_progress</span></span>                         | <span data-ttu-id="f4ec9-268">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-268">no</span></span>             | <span data-ttu-id="f4ec9-269">ne (da za P4W)</span><span class="sxs-lookup"><span data-stu-id="f4ec9-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="f4ec9-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="f4ec9-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="f4ec9-271">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-271">no</span></span>             | <span data-ttu-id="f4ec9-272">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-272">no</span></span>               |
| <span data-ttu-id="f4ec9-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="f4ec9-274">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-274">no</span></span>             | <span data-ttu-id="f4ec9-275">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-275">no</span></span>               |
| <span data-ttu-id="f4ec9-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="f4ec9-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="f4ec9-277">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-277">no</span></span>             | <span data-ttu-id="f4ec9-278">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-278">no</span></span>               |
| <span data-ttu-id="f4ec9-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="f4ec9-280">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-280">no</span></span>             | <span data-ttu-id="f4ec9-281">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-281">no</span></span>               |
| <span data-ttu-id="f4ec9-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="f4ec9-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="f4ec9-283">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-283">no</span></span>             | <span data-ttu-id="f4ec9-284">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-284">no</span></span>               |
| <span data-ttu-id="f4ec9-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="f4ec9-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="f4ec9-286">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-286">no</span></span>             | <span data-ttu-id="f4ec9-287">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-287">no</span></span>               |
| <span data-ttu-id="f4ec9-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="f4ec9-289">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-289">no</span></span>             | <span data-ttu-id="f4ec9-290">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-290">no</span></span>               |
| <span data-ttu-id="f4ec9-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="f4ec9-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="f4ec9-292">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-292">no</span></span>             | <span data-ttu-id="f4ec9-293">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-293">no</span></span>               |
| <span data-ttu-id="f4ec9-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="f4ec9-295">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-295">no</span></span>             | <span data-ttu-id="f4ec9-296">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-296">no</span></span>               |
| <span data-ttu-id="f4ec9-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="f4ec9-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="f4ec9-298">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-298">no</span></span>             | <span data-ttu-id="f4ec9-299">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-299">no</span></span>               |
| <span data-ttu-id="f4ec9-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="f4ec9-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="f4ec9-301">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-301">no</span></span>             | <span data-ttu-id="f4ec9-302">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-302">no</span></span>               |
| <span data-ttu-id="f4ec9-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="f4ec9-304">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-304">no</span></span>             | <span data-ttu-id="f4ec9-305">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-305">no</span></span>               |
| <span data-ttu-id="f4ec9-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="f4ec9-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="f4ec9-307">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-307">no</span></span>             | <span data-ttu-id="f4ec9-308">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-308">no</span></span>               |
| <span data-ttu-id="f4ec9-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="f4ec9-310">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-310">no</span></span>             | <span data-ttu-id="f4ec9-311">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-311">no</span></span>               |
| <span data-ttu-id="f4ec9-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="f4ec9-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="f4ec9-313">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-313">no</span></span>             | <span data-ttu-id="f4ec9-314">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-314">no</span></span>               |
| <span data-ttu-id="f4ec9-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="f4ec9-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="f4ec9-316">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-316">no</span></span>             | <span data-ttu-id="f4ec9-317">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-317">no</span></span>               |
| <span data-ttu-id="f4ec9-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="f4ec9-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="f4ec9-319">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-319">no</span></span>             | <span data-ttu-id="f4ec9-320">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-320">no</span></span>               |
| <span data-ttu-id="f4ec9-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="f4ec9-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="f4ec9-322">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-322">no</span></span>             | <span data-ttu-id="f4ec9-323">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-323">no</span></span>               |
| <span data-ttu-id="f4ec9-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="f4ec9-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="f4ec9-325">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-325">no</span></span>             | <span data-ttu-id="f4ec9-326">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-326">no</span></span>               |
| <span data-ttu-id="f4ec9-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="f4ec9-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="f4ec9-328">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-328">no</span></span>             | <span data-ttu-id="f4ec9-329">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-329">no</span></span>               |
| <span data-ttu-id="f4ec9-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="f4ec9-330">msdyn_summary</span></span>                          | <span data-ttu-id="f4ec9-331">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-331">no</span></span>             | <span data-ttu-id="f4ec9-332">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-332">no</span></span>               |
| <span data-ttu-id="f4ec9-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="f4ec9-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="f4ec9-334">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-334">no</span></span>             | <span data-ttu-id="f4ec9-335">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-335">no</span></span>               |
| <span data-ttu-id="f4ec9-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="f4ec9-337">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-337">no</span></span>             | <span data-ttu-id="f4ec9-338">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="f4ec9-339">Odvisnost projektnega opravila</span><span class="sxs-lookup"><span data-stu-id="f4ec9-339">Project task dependency</span></span>

| <span data-ttu-id="f4ec9-340">**Logično ime**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-340">**Logical name**</span></span>              | <span data-ttu-id="f4ec9-341">**Možnost ustvarjanja**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-341">**Can create**</span></span> | <span data-ttu-id="f4ec9-342">**Možnost urejanja**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="f4ec9-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="f4ec9-343">msdyn_linktype</span></span>                | <span data-ttu-id="f4ec9-344">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-344">no</span></span>             | <span data-ttu-id="f4ec9-345">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-345">no</span></span>           |
| <span data-ttu-id="f4ec9-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="f4ec9-346">msdyn_linktypename</span></span>            | <span data-ttu-id="f4ec9-347">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-347">no</span></span>             | <span data-ttu-id="f4ec9-348">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-348">no</span></span>           |
| <span data-ttu-id="f4ec9-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="f4ec9-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="f4ec9-350">da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-350">yes</span></span>            | <span data-ttu-id="f4ec9-351">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-351">no</span></span>           |
| <span data-ttu-id="f4ec9-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="f4ec9-353">da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-353">yes</span></span>            | <span data-ttu-id="f4ec9-354">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-354">no</span></span>           |
| <span data-ttu-id="f4ec9-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="f4ec9-355">msdyn_project</span></span>                 | <span data-ttu-id="f4ec9-356">da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-356">yes</span></span>            | <span data-ttu-id="f4ec9-357">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-357">no</span></span>           |
| <span data-ttu-id="f4ec9-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-358">msdyn_projectname</span></span>             | <span data-ttu-id="f4ec9-359">da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-359">yes</span></span>            | <span data-ttu-id="f4ec9-360">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-360">no</span></span>           |
| <span data-ttu-id="f4ec9-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="f4ec9-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="f4ec9-362">da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-362">yes</span></span>            | <span data-ttu-id="f4ec9-363">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-363">no</span></span>           |
| <span data-ttu-id="f4ec9-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="f4ec9-364">msdyn_successortask</span></span>           | <span data-ttu-id="f4ec9-365">da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-365">yes</span></span>            | <span data-ttu-id="f4ec9-366">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-366">no</span></span>           |
| <span data-ttu-id="f4ec9-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="f4ec9-368">da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-368">yes</span></span>            | <span data-ttu-id="f4ec9-369">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="f4ec9-370">Dodelitev vira</span><span class="sxs-lookup"><span data-stu-id="f4ec9-370">Resource assignment</span></span>

| <span data-ttu-id="f4ec9-371">**Logično ime**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-371">**Logical name**</span></span>             | <span data-ttu-id="f4ec9-372">**Možnost ustvarjanja**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-372">**Can create**</span></span> | <span data-ttu-id="f4ec9-373">**Možnost urejanja**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="f4ec9-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="f4ec9-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="f4ec9-375">da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-375">yes</span></span>            | <span data-ttu-id="f4ec9-376">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-376">no</span></span>           |
| <span data-ttu-id="f4ec9-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="f4ec9-378">da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-378">yes</span></span>            | <span data-ttu-id="f4ec9-379">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-379">no</span></span>           |
| <span data-ttu-id="f4ec9-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="f4ec9-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="f4ec9-381">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-381">no</span></span>             | <span data-ttu-id="f4ec9-382">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-382">no</span></span>           |
| <span data-ttu-id="f4ec9-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="f4ec9-384">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-384">no</span></span>             | <span data-ttu-id="f4ec9-385">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-385">no</span></span>           |
| <span data-ttu-id="f4ec9-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="f4ec9-386">msdyn_committype</span></span>             | <span data-ttu-id="f4ec9-387">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-387">no</span></span>             | <span data-ttu-id="f4ec9-388">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-388">no</span></span>           |
| <span data-ttu-id="f4ec9-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="f4ec9-389">msdyn_committypename</span></span>         | <span data-ttu-id="f4ec9-390">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-390">no</span></span>             | <span data-ttu-id="f4ec9-391">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-391">no</span></span>           |
| <span data-ttu-id="f4ec9-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="f4ec9-392">msdyn_effort</span></span>                 | <span data-ttu-id="f4ec9-393">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-393">no</span></span>             | <span data-ttu-id="f4ec9-394">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-394">no</span></span>           |
| <span data-ttu-id="f4ec9-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f4ec9-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="f4ec9-396">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-396">no</span></span>             | <span data-ttu-id="f4ec9-397">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-397">no</span></span>           |
| <span data-ttu-id="f4ec9-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="f4ec9-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="f4ec9-399">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-399">no</span></span>             | <span data-ttu-id="f4ec9-400">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-400">no</span></span>           |
| <span data-ttu-id="f4ec9-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="f4ec9-401">msdyn_finish</span></span>                 | <span data-ttu-id="f4ec9-402">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-402">no</span></span>             | <span data-ttu-id="f4ec9-403">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-403">no</span></span>           |
| <span data-ttu-id="f4ec9-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="f4ec9-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="f4ec9-405">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-405">no</span></span>             | <span data-ttu-id="f4ec9-406">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-406">no</span></span>           |
| <span data-ttu-id="f4ec9-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="f4ec9-408">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-408">no</span></span>             | <span data-ttu-id="f4ec9-409">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-409">no</span></span>           |
| <span data-ttu-id="f4ec9-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="f4ec9-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="f4ec9-411">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-411">no</span></span>             | <span data-ttu-id="f4ec9-412">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-412">no</span></span>           |
| <span data-ttu-id="f4ec9-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="f4ec9-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="f4ec9-414">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-414">no</span></span>             | <span data-ttu-id="f4ec9-415">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-415">no</span></span>           |
| <span data-ttu-id="f4ec9-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="f4ec9-417">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-417">no</span></span>             | <span data-ttu-id="f4ec9-418">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-418">no</span></span>           |
| <span data-ttu-id="f4ec9-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="f4ec9-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="f4ec9-420">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-420">no</span></span>             | <span data-ttu-id="f4ec9-421">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-421">no</span></span>           |
| <span data-ttu-id="f4ec9-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="f4ec9-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="f4ec9-423">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-423">no</span></span>             | <span data-ttu-id="f4ec9-424">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-424">no</span></span>           |
| <span data-ttu-id="f4ec9-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="f4ec9-425">msdyn_projectid</span></span>              | <span data-ttu-id="f4ec9-426">da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-426">yes</span></span>            | <span data-ttu-id="f4ec9-427">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-427">no</span></span>           |
| <span data-ttu-id="f4ec9-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-428">msdyn_projectidname</span></span>          | <span data-ttu-id="f4ec9-429">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-429">no</span></span>             | <span data-ttu-id="f4ec9-430">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-430">no</span></span>           |
| <span data-ttu-id="f4ec9-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="f4ec9-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="f4ec9-432">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-432">no</span></span>             | <span data-ttu-id="f4ec9-433">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-433">no</span></span>           |
| <span data-ttu-id="f4ec9-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="f4ec9-435">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-435">no</span></span>             | <span data-ttu-id="f4ec9-436">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-436">no</span></span>           |
| <span data-ttu-id="f4ec9-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="f4ec9-437">msdyn_start</span></span>                  | <span data-ttu-id="f4ec9-438">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-438">no</span></span>             | <span data-ttu-id="f4ec9-439">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-439">no</span></span>           |
| <span data-ttu-id="f4ec9-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="f4ec9-440">msdyn_taskid</span></span>                 | <span data-ttu-id="f4ec9-441">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-441">no</span></span>             | <span data-ttu-id="f4ec9-442">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-442">no</span></span>           |
| <span data-ttu-id="f4ec9-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-443">msdyn_taskidname</span></span>             | <span data-ttu-id="f4ec9-444">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-444">no</span></span>             | <span data-ttu-id="f4ec9-445">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-445">no</span></span>           |
| <span data-ttu-id="f4ec9-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="f4ec9-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="f4ec9-447">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-447">no</span></span>             | <span data-ttu-id="f4ec9-448">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="f4ec9-449">Član projektne ekipe</span><span class="sxs-lookup"><span data-stu-id="f4ec9-449">Project team member</span></span>

| <span data-ttu-id="f4ec9-450">**Logično ime**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-450">**Logical name**</span></span>                                 | <span data-ttu-id="f4ec9-451">**Možnost ustvarjanja**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-451">**Can create**</span></span> | <span data-ttu-id="f4ec9-452">**Možnost urejanja**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="f4ec9-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="f4ec9-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="f4ec9-454">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-454">no</span></span>             | <span data-ttu-id="f4ec9-455">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-455">no</span></span>           |
| <span data-ttu-id="f4ec9-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="f4ec9-457">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-457">no</span></span>             | <span data-ttu-id="f4ec9-458">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-458">no</span></span>           |
| <span data-ttu-id="f4ec9-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="f4ec9-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="f4ec9-460">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-460">no</span></span>             | <span data-ttu-id="f4ec9-461">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-461">no</span></span>           |
| <span data-ttu-id="f4ec9-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="f4ec9-463">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-463">no</span></span>             | <span data-ttu-id="f4ec9-464">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-464">no</span></span>           |
| <span data-ttu-id="f4ec9-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="f4ec9-465">msdyn_effort</span></span>                                     | <span data-ttu-id="f4ec9-466">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-466">no</span></span>             | <span data-ttu-id="f4ec9-467">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-467">no</span></span>           |
| <span data-ttu-id="f4ec9-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f4ec9-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="f4ec9-469">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-469">no</span></span>             | <span data-ttu-id="f4ec9-470">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-470">no</span></span>           |
| <span data-ttu-id="f4ec9-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="f4ec9-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="f4ec9-472">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-472">no</span></span>             | <span data-ttu-id="f4ec9-473">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-473">no</span></span>           |
| <span data-ttu-id="f4ec9-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="f4ec9-474">msdyn_finish</span></span>                                     | <span data-ttu-id="f4ec9-475">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-475">no</span></span>             | <span data-ttu-id="f4ec9-476">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-476">no</span></span>           |
| <span data-ttu-id="f4ec9-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="f4ec9-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="f4ec9-478">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-478">no</span></span>             | <span data-ttu-id="f4ec9-479">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-479">no</span></span>           |
| <span data-ttu-id="f4ec9-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="f4ec9-480">msdyn_hours</span></span>                                      | <span data-ttu-id="f4ec9-481">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-481">no</span></span>             | <span data-ttu-id="f4ec9-482">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-482">no</span></span>           |
| <span data-ttu-id="f4ec9-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="f4ec9-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="f4ec9-484">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-484">no</span></span>             | <span data-ttu-id="f4ec9-485">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-485">no</span></span>           |
| <span data-ttu-id="f4ec9-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="f4ec9-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="f4ec9-487">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-487">no</span></span>             | <span data-ttu-id="f4ec9-488">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-488">no</span></span>           |
| <span data-ttu-id="f4ec9-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="f4ec9-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="f4ec9-490">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-490">no</span></span>             | <span data-ttu-id="f4ec9-491">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-491">no</span></span>           |
| <span data-ttu-id="f4ec9-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="f4ec9-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="f4ec9-493">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-493">no</span></span>             | <span data-ttu-id="f4ec9-494">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-494">no</span></span>           |
| <span data-ttu-id="f4ec9-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="f4ec9-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="f4ec9-496">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-496">no</span></span>             | <span data-ttu-id="f4ec9-497">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-497">no</span></span>           |
| <span data-ttu-id="f4ec9-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="f4ec9-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="f4ec9-499">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-499">no</span></span>             | <span data-ttu-id="f4ec9-500">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-500">no</span></span>           |
| <span data-ttu-id="f4ec9-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="f4ec9-501">msdyn_start</span></span>                                      | <span data-ttu-id="f4ec9-502">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-502">no</span></span>             | <span data-ttu-id="f4ec9-503">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="f4ec9-504">Project</span><span class="sxs-lookup"><span data-stu-id="f4ec9-504">Project</span></span>

| <span data-ttu-id="f4ec9-505">**Logično ime**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-505">**Logical name**</span></span>                       | <span data-ttu-id="f4ec9-506">**Možnost ustvarjanja**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-506">**Can create**</span></span> | <span data-ttu-id="f4ec9-507">**Možnost urejanja**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="f4ec9-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="f4ec9-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="f4ec9-509">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-509">no</span></span>             | <span data-ttu-id="f4ec9-510">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-510">no</span></span>           |
| <span data-ttu-id="f4ec9-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="f4ec9-512">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-512">no</span></span>             | <span data-ttu-id="f4ec9-513">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-513">no</span></span>           |
| <span data-ttu-id="f4ec9-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="f4ec9-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="f4ec9-515">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-515">no</span></span>             | <span data-ttu-id="f4ec9-516">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-516">no</span></span>           |
| <span data-ttu-id="f4ec9-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="f4ec9-518">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-518">no</span></span>             | <span data-ttu-id="f4ec9-519">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-519">no</span></span>           |
| <span data-ttu-id="f4ec9-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="f4ec9-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="f4ec9-521">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-521">no</span></span>             | <span data-ttu-id="f4ec9-522">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-522">no</span></span>           |
| <span data-ttu-id="f4ec9-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="f4ec9-524">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-524">no</span></span>             | <span data-ttu-id="f4ec9-525">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-525">no</span></span>           |
| <span data-ttu-id="f4ec9-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="f4ec9-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="f4ec9-527">da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-527">yes</span></span>            | <span data-ttu-id="f4ec9-528">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-528">no</span></span>           |
| <span data-ttu-id="f4ec9-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="f4ec9-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="f4ec9-530">da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-530">yes</span></span>            | <span data-ttu-id="f4ec9-531">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-531">no</span></span>           |
| <span data-ttu-id="f4ec9-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="f4ec9-533">da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-533">yes</span></span>            | <span data-ttu-id="f4ec9-534">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-534">no</span></span>           |
| <span data-ttu-id="f4ec9-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="f4ec9-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="f4ec9-536">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-536">no</span></span>             | <span data-ttu-id="f4ec9-537">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-537">no</span></span>           |
| <span data-ttu-id="f4ec9-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="f4ec9-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="f4ec9-539">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-539">no</span></span>             | <span data-ttu-id="f4ec9-540">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-540">no</span></span>           |
| <span data-ttu-id="f4ec9-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="f4ec9-542">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-542">no</span></span>             | <span data-ttu-id="f4ec9-543">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-543">no</span></span>           |
| <span data-ttu-id="f4ec9-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="f4ec9-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="f4ec9-545">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-545">no</span></span>             | <span data-ttu-id="f4ec9-546">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-546">no</span></span>           |
| <span data-ttu-id="f4ec9-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="f4ec9-548">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-548">no</span></span>             | <span data-ttu-id="f4ec9-549">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-549">no</span></span>           |
| <span data-ttu-id="f4ec9-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="f4ec9-550">msdyn_duration</span></span>                         | <span data-ttu-id="f4ec9-551">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-551">no</span></span>             | <span data-ttu-id="f4ec9-552">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-552">no</span></span>           |
| <span data-ttu-id="f4ec9-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="f4ec9-553">msdyn_effort</span></span>                           | <span data-ttu-id="f4ec9-554">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-554">no</span></span>             | <span data-ttu-id="f4ec9-555">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-555">no</span></span>           |
| <span data-ttu-id="f4ec9-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f4ec9-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="f4ec9-557">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-557">no</span></span>             | <span data-ttu-id="f4ec9-558">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-558">no</span></span>           |
| <span data-ttu-id="f4ec9-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="f4ec9-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="f4ec9-560">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-560">no</span></span>             | <span data-ttu-id="f4ec9-561">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-561">no</span></span>           |
| <span data-ttu-id="f4ec9-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="f4ec9-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="f4ec9-563">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-563">no</span></span>             | <span data-ttu-id="f4ec9-564">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-564">no</span></span>           |
| <span data-ttu-id="f4ec9-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="f4ec9-565">msdyn_finish</span></span>                           | <span data-ttu-id="f4ec9-566">da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-566">yes</span></span>            | <span data-ttu-id="f4ec9-567">da</span><span class="sxs-lookup"><span data-stu-id="f4ec9-567">yes</span></span>          |
| <span data-ttu-id="f4ec9-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="f4ec9-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="f4ec9-569">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-569">no</span></span>             | <span data-ttu-id="f4ec9-570">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-570">no</span></span>           |
| <span data-ttu-id="f4ec9-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="f4ec9-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="f4ec9-572">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-572">no</span></span>             | <span data-ttu-id="f4ec9-573">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-573">no</span></span>           |
| <span data-ttu-id="f4ec9-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="f4ec9-575">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-575">no</span></span>             | <span data-ttu-id="f4ec9-576">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-576">no</span></span>           |
| <span data-ttu-id="f4ec9-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="f4ec9-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="f4ec9-578">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-578">no</span></span>             | <span data-ttu-id="f4ec9-579">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-579">no</span></span>           |
| <span data-ttu-id="f4ec9-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="f4ec9-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="f4ec9-581">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-581">no</span></span>             | <span data-ttu-id="f4ec9-582">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-582">no</span></span>           |
| <span data-ttu-id="f4ec9-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="f4ec9-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="f4ec9-584">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-584">no</span></span>             | <span data-ttu-id="f4ec9-585">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-585">no</span></span>           |
| <span data-ttu-id="f4ec9-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="f4ec9-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="f4ec9-587">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-587">no</span></span>             | <span data-ttu-id="f4ec9-588">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-588">no</span></span>           |
| <span data-ttu-id="f4ec9-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="f4ec9-590">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-590">no</span></span>             | <span data-ttu-id="f4ec9-591">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-591">no</span></span>           |
| <span data-ttu-id="f4ec9-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="f4ec9-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="f4ec9-593">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-593">no</span></span>             | <span data-ttu-id="f4ec9-594">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-594">no</span></span>           |
| <span data-ttu-id="f4ec9-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="f4ec9-596">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-596">no</span></span>             | <span data-ttu-id="f4ec9-597">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-597">no</span></span>           |
| <span data-ttu-id="f4ec9-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="f4ec9-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="f4ec9-599">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-599">no</span></span>             | <span data-ttu-id="f4ec9-600">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-600">no</span></span>           |
| <span data-ttu-id="f4ec9-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="f4ec9-602">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-602">no</span></span>             | <span data-ttu-id="f4ec9-603">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-603">no</span></span>           |
| <span data-ttu-id="f4ec9-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="f4ec9-604">msdyn_progress</span></span>                         | <span data-ttu-id="f4ec9-605">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-605">no</span></span>             | <span data-ttu-id="f4ec9-606">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-606">no</span></span>           |
| <span data-ttu-id="f4ec9-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="f4ec9-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="f4ec9-608">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-608">no</span></span>             | <span data-ttu-id="f4ec9-609">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-609">no</span></span>           |
| <span data-ttu-id="f4ec9-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="f4ec9-611">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-611">no</span></span>             | <span data-ttu-id="f4ec9-612">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-612">no</span></span>           |
| <span data-ttu-id="f4ec9-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="f4ec9-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="f4ec9-614">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-614">no</span></span>             | <span data-ttu-id="f4ec9-615">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-615">no</span></span>           |
| <span data-ttu-id="f4ec9-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="f4ec9-617">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-617">no</span></span>             | <span data-ttu-id="f4ec9-618">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-618">no</span></span>           |
| <span data-ttu-id="f4ec9-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="f4ec9-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="f4ec9-620">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-620">no</span></span>             | <span data-ttu-id="f4ec9-621">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-621">no</span></span>           |
| <span data-ttu-id="f4ec9-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="f4ec9-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="f4ec9-623">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-623">no</span></span>             | <span data-ttu-id="f4ec9-624">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-624">no</span></span>           |
| <span data-ttu-id="f4ec9-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="f4ec9-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="f4ec9-626">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-626">no</span></span>             | <span data-ttu-id="f4ec9-627">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-627">no</span></span>           |
| <span data-ttu-id="f4ec9-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="f4ec9-629">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-629">no</span></span>             | <span data-ttu-id="f4ec9-630">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-630">no</span></span>           |
| <span data-ttu-id="f4ec9-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="f4ec9-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="f4ec9-632">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-632">no</span></span>             | <span data-ttu-id="f4ec9-633">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-633">no</span></span>           |
| <span data-ttu-id="f4ec9-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="f4ec9-635">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-635">no</span></span>             | <span data-ttu-id="f4ec9-636">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-636">no</span></span>           |
| <span data-ttu-id="f4ec9-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="f4ec9-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="f4ec9-638">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-638">no</span></span>             | <span data-ttu-id="f4ec9-639">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-639">no</span></span>           |
| <span data-ttu-id="f4ec9-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="f4ec9-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="f4ec9-641">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-641">no</span></span>             | <span data-ttu-id="f4ec9-642">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-642">no</span></span>           |
| <span data-ttu-id="f4ec9-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="f4ec9-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="f4ec9-644">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-644">no</span></span>             | <span data-ttu-id="f4ec9-645">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-645">no</span></span>           |
| <span data-ttu-id="f4ec9-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="f4ec9-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="f4ec9-647">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-647">no</span></span>             | <span data-ttu-id="f4ec9-648">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-648">no</span></span>           |
| <span data-ttu-id="f4ec9-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="f4ec9-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="f4ec9-650">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-650">no</span></span>             | <span data-ttu-id="f4ec9-651">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-651">no</span></span>           |
| <span data-ttu-id="f4ec9-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="f4ec9-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="f4ec9-653">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-653">no</span></span>             | <span data-ttu-id="f4ec9-654">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-654">no</span></span>           |
| <span data-ttu-id="f4ec9-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="f4ec9-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="f4ec9-656">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-656">no</span></span>             | <span data-ttu-id="f4ec9-657">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-657">no</span></span>           |
| <span data-ttu-id="f4ec9-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="f4ec9-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="f4ec9-659">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-659">no</span></span>             | <span data-ttu-id="f4ec9-660">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-660">no</span></span>           |
| <span data-ttu-id="f4ec9-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="f4ec9-662">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-662">no</span></span>             | <span data-ttu-id="f4ec9-663">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-663">no</span></span>           |
| <span data-ttu-id="f4ec9-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="f4ec9-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="f4ec9-665">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-665">no</span></span>             | <span data-ttu-id="f4ec9-666">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-666">no</span></span>           |
| <span data-ttu-id="f4ec9-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="f4ec9-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="f4ec9-668">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-668">no</span></span>             | <span data-ttu-id="f4ec9-669">ne</span><span class="sxs-lookup"><span data-stu-id="f4ec9-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="f4ec9-670">Omejitve in znane težave</span><span class="sxs-lookup"><span data-stu-id="f4ec9-670">Limitations and known issues</span></span>
<span data-ttu-id="f4ec9-671">Sledi seznam omejitev in znanih težav:</span><span class="sxs-lookup"><span data-stu-id="f4ec9-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="f4ec9-672">API-je razporejanja projektov lahko uporabljajo samo **Uporabniki z licenco za storitev Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="f4ec9-673">Ne morejo jih uporabljati:</span><span class="sxs-lookup"><span data-stu-id="f4ec9-673">They can't be used by:</span></span>
    - <span data-ttu-id="f4ec9-674">Uporabniki aplikacij</span><span class="sxs-lookup"><span data-stu-id="f4ec9-674">Application users</span></span>
    - <span data-ttu-id="f4ec9-675">Uporabniki sistema</span><span class="sxs-lookup"><span data-stu-id="f4ec9-675">System users</span></span>
    - <span data-ttu-id="f4ec9-676">Uporabniki integracije</span><span class="sxs-lookup"><span data-stu-id="f4ec9-676">Integration users</span></span>
    - <span data-ttu-id="f4ec9-677">Drugi uporabniki, ki nimajo zahtevane licence</span><span class="sxs-lookup"><span data-stu-id="f4ec9-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="f4ec9-678">Vsak **OperationSet** ima lahko največ 100 postopkov.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="f4ec9-679">Vsak uporabnik ima lahko odprtih največ 10 postopkov **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="f4ec9-680">Project Operations trenutno podpira največ 500 skupnih opravil na projektu.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="f4ec9-681">Stanje napake in dnevniki napak **OperationSet** trenutno niso na voljo.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="f4ec9-682">Omejitve in meje projektov ter opravil</span><span class="sxs-lookup"><span data-stu-id="f4ec9-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="f4ec9-683">Obravnava napak</span><span class="sxs-lookup"><span data-stu-id="f4ec9-683">Error handling</span></span>

   - <span data-ttu-id="f4ec9-684">Če želite pregledati napake, ustvarjene iz naborov postopkov, odprite razdelek **Nastavitve** \> **Načrtovanje integracije** \> **Nabori postopkov**.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="f4ec9-685">Za ogled napak iz storitve razporejanja projektov pojdite v **Nastavitve** \> **Integracija načrtovanja** \> **Dnevniki napak za PSS**.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="f4ec9-686">Vzorčni scenarij</span><span class="sxs-lookup"><span data-stu-id="f4ec9-686">Sample scenario</span></span>

<span data-ttu-id="f4ec9-687">V tem primeru boste ustvarili projekt, člana ekipe, štiri opravila in dve dodelitvi virov.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="f4ec9-688">Nato boste posodobili eno opravilo, posodobili projekt, izbrisali eno opravilo, izbrisali eno dodelitev vira in ustvarili odvisnost od opravila.</span><span class="sxs-lookup"><span data-stu-id="f4ec9-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="f4ec9-689">Dodatni vzorci</span><span class="sxs-lookup"><span data-stu-id="f4ec9-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
