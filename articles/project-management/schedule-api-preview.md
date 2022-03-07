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
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Uporaba API-jev razporeda za izvajanje opravil z entitetami razporejanja

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

> [!IMPORTANT] 
> Nekatere ali vse funkcije, navedene v tej temi, so na voljo kot del izdaje predogledne različice. Vsebina in funkcionalnost se lahko spremenita. 

## <a name="scheduling-entities"></a>Entitete za razporejanje

API-ji razporeda omogočajo izvajanje postopkov ustvarjanja, posodabljanja in brisanja z **entitetami razporeda**. Te entitete upravljamo prek mehanizma za razporejanje v projektu za splet. Postopki ustvarjanja, posodabljanja in brisanja z **entitetami razporejanja** so bili prej omejeni v prejšnjih izdajah Dynamics 365 Project Operations.

Naslednja tabela vsebuje celoten seznam **entitet razporejanja**.

| Ime entitete  | Logično ime entitete |
| --- | --- |
| Project | msdyn_project |
| Projektno opravilo  | msdyn_projecttask  |
| Odvisnost projektnega opravila  | msdyn_projecttaskdependency  |
| Dodelitev vira | msdyn_resourceassignment |
| Vedro projekta  | msdyn_projectbucket |
| Član projektne ekipe | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet je vzorec enote dela, ki se lahko uporablja, kadar je treba v transakciji obdelati več zahtev, ki vplivajo na urnik.

## <a name="schedule-apis"></a>Načrtovanje API-jev

Sledi seznam trenutnih API-jev razporeda.

- **msdyn_CreateProjectV1**: ta API se lahko uporablja za ustvarjanje projekta. Projekt in privzeto vedro projekta se ustvarita takoj.
- **msdyn_CreateTeamMemberV1**: ta API se lahko uporablja za ustvarjanje člana projektne skupine. Zapis člana ekipe se ustvari takoj.
- **msdyn_CreateOperationSetV1**: ta API se lahko uporablja za razporejanje več zahtev, ki jih je treba izvesti znotraj transakcije.
- **msdyn_PSSCreateV1**: ta API se lahko uporablja za ustvarjanje entitete. Entiteta je lahko katera koli entiteta razporejanja, ki podpira postopek ustvarjanja.
- **msdyn_PSSUpdateV1**: ta API se lahko uporablja za posodabljanje entitete. Entiteta je lahko katera koli entiteta razporejanja, ki podpira postopek posodabljanja.
- **msdyn_PSSDeleteV1**: ta API se lahko uporablja za brisanje entitete. Entiteta je lahko katera koli entiteta razporejanja, ki podpira postopek brisanja.
- **msdyn_ExecuteOperationSetV1**: ta API se uporablja za izvajanje vseh postopkov znotraj danega nabora postopkov.

## <a name="using-schedule-apis-with-operationset"></a>Uporaba API-jev razporeda s funkcijo OperationSet

Ker se zapisi, ki vsebujejo **CreateProjectV1** in **CreateTeamMemberV1**, ustvarijo takoj, teh API-jev ni mogoče neposredno uporabljati pri funkciji **OperationSet**. Vendar pa lahko API uporabite za ustvarjanje potrebnih zapisov, ustvarite **OperationSet** in nato uporabite te vnaprej ustvarjene zapise pri funkciji **OperationSet**.

## <a name="supported-operations"></a>Podprti postopki

| Entiteta za razporejanje | Ustvari | Posodabljanje | Delete | Pomembni premisleki |
| --- | --- | --- | --- | --- |
Projektno opravilo | Da | Da | Da | Brez |
| Odvisnost projektnega opravila | Da | Da | | Zapisi odvisnosti od projektne naloge se ne posodabljajo. Namesto tega lahko stari zapis izbrišete in ustvarite novega. |
| Dodelitev vira | Da | Da | | Postopki z naslednjimi polji niso podprti: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** in **PlannedWork**. Zapisi o dodeljevanju virov niso posodobljeni. Namesto tega lahko stari zapis izbrišete in ustvarite novega. |
| Vedro projekta | Ni na voljo | Ni na voljo | Ni na voljo | Privzeto vedro je ustvarjeno z API-jem **CreateProjectV1**. |
| Član projektne ekipe | Da | Da | Da | Za postopek ustvarjanja uporabite API **CreateTeamMemberV1**. |
| Project | Da | Da | Ni na voljo | Postopki z naslednjimi polji niso podprti: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** in **Duration**. |

Te API-je je mogoče priklicati s predmeti entitete, ki vključujejo polja po meri.

Lastnost ID ni obvezna. Če je na voljo, ga sistem poskuša uporabiti in zavrže izjemo, če je ni mogoče uporabiti. Če ni na voljo, ga bo sistem ustvaril.

## <a name="limitations-and-known-issues"></a>Omejitve in znane težave
Sledi seznam omejitev in znanih težav:

- API-je razporeda lahko uporabljajo samo **uporabniki z licenco Microsoft Project.** Ne morejo jih uporabljati:
    - Uporabniki aplikacij
    - Uporabniki sistema
    - Uporabniki integracije
    - Drugi uporabniki, ki nimajo zahtevane licence
- Vsak **OperationSet** ima lahko največ 100 postopkov.
- Vsak uporabnik ima lahko odprtih največ 10 postopkov **OperationSet**.
- Project Operations trenutno podpira največ 500 skupnih opravil na projektu.
- Stanje napake in dnevniki napak **OperationSet** trenutno niso na voljo.
- API-ji razporeda so na voljo pri predogledni različici za javnost. Microsoft ne podpira uporabe teh API-jev v produkcijskem okolju.

## <a name="sample-scenario"></a>Vzorčni scenarij

V tem primeru boste ustvarili projekt, člana ekipe, štiri opravila in dve dodelitvi virov. Nato boste posodobili eno opravilo, posodobili projekt, izbrisali eno opravilo, izbrisali eno dodelitev vira in ustvarili odvisnost od opravila.

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

## <a name="additional-samples"></a>Dodatni vzorci

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
