---
title: Uporaba API-jev razporejanja projektov za izvajanje postopkov s pomočjo entitet razporejanja
description: Ta članek ponuja informacije in vzorce za uporabo API-jev za načrtovanje projekta.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541145"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Uporaba API-jev razporejanja projektov za izvajanje postopkov s pomočjo entitet razporejanja

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_


**Entitete za razporejanje**

Uporaba API-jev razporejanja projektov ponuja možnost izvajanja postopkov ustvarjanja, posodabljanja in brisanja s pomočjo možnosti **Entitete razporejanja**. Te entitete upravljamo prek mehanizma za razporejanje v projektu za splet. Postopki ustvarjanja, posodabljanja in brisanja z **entitetami razporejanja** so bili prej omejeni v prejšnjih izdajah Dynamics 365 Project Operations.

Naslednja tabela vključuje celoten seznam entitet razporejanja projektov.

| **Ime entitete**         | **Logično ime entitete**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektno opravilo            | msdyn_projecttask           |
| Odvisnost projektnega opravila | msdyn_projecttaskdependency |
| Dodelitev vira     | msdyn_resourceassignment    |
| Vedro projekta          | msdyn_projectbucket         |
| Član projektne ekipe     | msdyn_projectteam           |
| Kontrolni seznami projekta      | msdyn_projectchecklist      |
| Oznaka projekta           | msdyn_projectlabel          |
| Projektna naloga za oznako   | msdyn_projecttasktolabel    |
| Projektni sprint          | msdyn_projectsprint         |

**OperationSet**

OperationSet je vzorec enote dela, ki se lahko uporablja, kadar je treba v transakciji obdelati več zahtev, ki vplivajo na urnik.

**API-ji razporejanja projektov**

Naslednji seznam vsebuje trenutne API-je razporejanja projektov.

| **API**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Ta API se uporablja za ustvarjanje projekta. Projekt in privzeto projektno vedro sta ustvarjena takoj.                         |
| **msdyn_CreateTeamMemberV1**            | Ta API se uporablja za ustvarjanje člana projektne skupine. Zapis člana ekipe se ustvari takoj.                                  |
| **msdyn_CreateOperationSetV1**          | Ta API se uporablja za načrtovanje več zahtev, ki jih je treba izvesti znotraj transakcije.                                        |
| **msdyn_PssCreateV1**                   | Ta API se uporablja za ustvarjanje entitete. Lahko gre za katerokoli entiteto razporejanja projektov, ki podpira postopek ustvarjanja. |
| **msdyn_PssUpdateV1**                   | Ta API se uporablja za posodobitev entitete. Entiteta je lahko katera koli entiteta za načrtovanje projekta, ki podpira operacijo posodabljanja  |
| **msdyn_PssDeleteV1**                   | Ta API se uporablja za brisanje entitete. Lahko gre za katerokoli entiteto razporejanja projektov, ki podpira postopek brisanja. |
| **msdyn_ExecuteOperationSetV1**         | Ta API se uporablja za izvajanje vseh operacij v danem nizu operacij.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Ta API se uporablja za posodobitev konture načrtovanega dela Dodelitve virov.                                                        |



**Uporaba API-jev razporejanja projektov s funkcijo OperationSet**

Ker se zapisi, ki vsebujejo **CreateProjectV1** in **CreateTeamMemberV1**, ustvarijo takoj, teh API-jev ni mogoče neposredno uporabljati pri funkciji **OperationSet**. Vendar pa lahko API uporabite za ustvarjanje potrebnih zapisov, ustvarite **OperationSet** in nato uporabite te vnaprej ustvarjene zapise pri funkciji **OperationSet**.

**Podprti postopki**

| **Entiteta za razporejanje**   | **Ustvari** | **Posodabljanje** | **Delete** | **Pomembni premisleki**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektno opravilo            | Da        | Da        | Da        | The **Napredek**, **je končan**, in **Preostali trud** polja je mogoče urejati v programu Project za splet, ni pa jih mogoče urejati v programu Project Operations.                                                                                                                                                                                             |
| Odvisnost projektnega opravila | Da        | No         | Da        | Zapisi odvisnosti od projektne naloge se ne posodabljajo. Namesto tega lahko stari zapis izbrišete in ustvarite nov zapis.                                                                                                                                                                                                                                 |
| Dodelitev vira     | Da        | Da\*      | Da        | Postopki z naslednjimi polji niso podprti: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** in **PlannedWork**. Zapisi o dodeljevanju virov niso posodobljeni. Namesto tega lahko stari zapis izbrišete in ustvarite nov zapis. Na voljo je bil ločen API za posodobitev kontur dodelitve virov. |
| Vedro projekta          | Da        | Da        | Da        | Privzeto vedro je ustvarjeno z uporabo **CreateProjectV1** API. Podpora za ustvarjanje in brisanje projektnih veder je bila dodana v posodobitvi izdaje 16.                                                                                                                                                                                                   |
| Član projektne ekipe     | Da        | Da        | Da        | Za postopek ustvarjanja uporabite API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Projekt                 | Da        | Da        |            | Postopki z naslednjimi polji niso podprti: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** in **Duration**.                                                                                       |
| Kontrolni seznami projekta      | Da        | Da        | Da        |                                                                                                                                                                                                                                                                                                                                                         |
| Oznaka projekta           | No         | Da        | No         | Imena oznak je mogoče spremeniti. Ta funkcija je na voljo samo za Project za splet                                                                                                                                                                                                                                                                      |
| Projektna naloga za oznako   | Da        | No         | Da        | Ta funkcija je na voljo samo za Project za splet                                                                                                                                                                                                                                                                                                  |
| Projektni sprint          | Da        | Da        | Da        | The **Začetek** polje mora imeti datum pred **Končaj** polje. Šprinti za isti projekt se med seboj ne morejo prekrivati. Ta funkcija je na voljo samo za Project za splet                                                                                                                                                                    |




Lastnost ID ni obvezna. Če je na voljo, ga sistem poskuša uporabiti in zavrže izjemo, če je ni mogoče uporabiti. Če ni na voljo, ga bo sistem ustvaril.

**Omejitve in znane težave**

Sledi seznam omejitev in znanih težav:

-   API-je za urnik projekta lahko uporablja samo **Uporabniki z licenco Microsoft Project**. Ne morejo jih uporabljati:
    -   Uporabniki aplikacij
    -   Uporabniki sistema
    -   Uporabniki integracije
    -   Drugi uporabniki, ki nimajo zahtevane licence
-   Vsak **OperationSet** ima lahko največ 100 postopkov.
-   Vsak uporabnik ima lahko odprtih največ 10 postopkov **OperationSet**.
-   Project Operations trenutno podpira največ 500 skupnih opravil na projektu.
-   Vsaka operacija Update Resource Assignment Contour se šteje kot ena sama operacija.
-   Vsak seznam posodobljenih kontur lahko vsebuje največ 100 časovnih rezin.
-   Stanje napake in dnevniki napak **OperationSet** trenutno niso na voljo.
-   Na projekt je na voljo največ 400 sprintov.
-   [Omejitve in meje projektov in nalog](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Oznake so trenutno na voljo samo za Project za splet.

**Obravnava napak**

-   Če želite pregledati napake, ustvarjene iz naborov postopkov, odprite razdelek **Nastavitve** \> **Načrtovanje integracije** \> **Nabori postopkov**.
-   Za ogled napak iz storitve razporejanja projektov pojdite v **Nastavitve** \> **Integracija načrtovanja** \> **Dnevniki napak za PSS**.

**Urejanje obrisov dodelitve virov**

Za razliko od vseh drugih API-jev za razporejanje projektov, ki posodabljajo entiteto, je API konture dodelitve virov izključno odgovoren za posodobitve posameznega polja, msdyn_plannedwork, v eni entiteti, msydn_resourceassignment.

Podani način urnika je:

-   **fiksne enote**
-   Koledar projekta je 9-5p je 9-5pst, pon, torek, četrtek, petek (OB SREDAH NI DELA)
-   In koledar virov je 9-13p PST od ponedeljka do petka

Ta naloga traja en teden, štiri ure na dan. To je zato, ker je koledar virov od 9. do 1. PST ali štiri ure na dan.

| &nbsp;     | opravilo, | Datum začetka | Datum konca  | Količina | 6. 2022 | 6. 2022 | 6. 2022 | 6. 2022 | 6. 2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 delavec |  T1  | 6. 2022  | 6. 2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Na primer, če želite, da delavec ta teden vsak dan dela samo tri ure in da ima eno uro za druge naloge.

#### <a name="updatedcontours-sample-payload"></a>Posodobljeni vzorčni tovor Contours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

To je dodelitev po zagonu API-ja Update Contour Schedule.

| &nbsp;     | opravilo, | Datum začetka | Datum konca  | Količina | 6. 2022 | 6. 2022 | 6. 2022 | 6. 2022 | 6. 2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 delavec | T1   | 6. 2022  | 6. 2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Vzorčni scenarij**

V tem primeru boste ustvarili projekt, člana ekipe, štiri opravila in dve dodelitvi virov. Nato boste posodobili eno opravilo, posodobili projekt, izbrisali eno opravilo, izbrisali eno dodelitev vira in ustvarili odvisnost od opravila.

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

** Dodatni vzorci

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
