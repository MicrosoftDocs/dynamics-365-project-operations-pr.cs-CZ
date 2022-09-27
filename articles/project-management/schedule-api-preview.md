---
title: K provádění operací s entitami plánování použijte rozhraní API pro plánování projektu
description: Tento článek poskytuje informace a ukázky pro použití rozhraní API plánování projektu.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541116"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>K provádění operací s entitami plánování použijte rozhraní API pro plánování projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_


**Entity plánování**

Rozhraní API plánování projektu umožňují provádět operace vytváření, aktualizace a mazání pomocí **Plánovacích entit**. Tyto entity jsou spravovány prostřednictvím modulu Plánování v aplikaci Project for the Web. Operace vytváření, aktualizace a odstraňování **entit plánování** byly ve starších verzích Dynamics 365 Project Operations omezeny.

Následující tabulka poskytuje úplný seznam entit plánu projektu.

| **Název entity**         | **Logický název entity**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektový úkol            | msdyn_projecttask           |
| Závislost projektového úkolu | msdyn_projecttaskdependency |
| Přiřazení zdroje     | msdyn_resourceassignment    |
| Kbelík projektu          | msdyn_projectbucket         |
| Člen projektového týmu     | msdyn_projectteam           |
| Kontrolní seznamy projektu      | msdyn_projectchecklist      |
| Popisek projektu           | msdyn_projectlabel          |
| Projektový úkol k popisku   | msdyn_projecttasktolabel    |
| Sprint projektu          | msdyn_projectsprint         |

**OperationSet**

OperationSet je vzor jednotky práce, který lze použít, když musí být v rámci transakce zpracováno několik požadavků ovlivňujících plány.

**Rozhraní API plánu projektu**

Následuje seznam aktuálních rozhraní API plánu projektu.

| **API**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Toto rozhraní API slouží k vytvoření projektu. Projekt a výchozí skupina projektů se vytvoří okamžitě.                         |
| **msdyn_CreateTeamMemberV1**            | Toto rozhraní API slouží k vytvoření člena projektového týmu. Záznam člena týmu je vytvořen okamžitě.                                  |
| **msdyn_CreateOperationSetV1**          | Toto rozhraní API slouží k naplánování několika požadavků, které je třeba provést v rámci transakce.                                        |
| **msdyn_PssCreateV1**                   | Toto rozhraní API slouží k vytvoření entity. Entitou může být jakákoli entita plánování projektu, která podporuje operaci vytvoření. |
| **msdyn_PssUpdateV1**                   | Toto rozhraní API slouží k aktualizaci entity. Entitou může být jakákoli entita plánování projektu, která podporuje operaci aktualizace  |
| **msdyn_PssDeleteV1**                   | Toto rozhraní API slouží k odstranění entity. Entitou může být jakákoli entita plánování projektu, která podporuje operaci odstranění. |
| **msdyn_ExecuteOperationSetV1**         | Toto rozhraní API slouží k provedení všech operací v rámci dané sady operací.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Toto rozhraní API slouží k aktualizaci průběhové křivky plánované práce v rámci přiřazení zdrojů.                                                        |



**Používání API plánu projektu s OperationSet**

Protože záznamy s oběma rozhraními **CreateProjectV1** a **CreateTeamMemberV1** jsou vytvořeny okamžitě, nelze tato API použít v sadě **OperationSet** přímo. Můžete však použít API k vytvoření potřebných záznamů, vytvořit sadu **OperationSet** a poté použít tyto předem vytvořené záznamy v sadě **OperationSet**.

**Podporované operace**

| **Entita plánování**   | **Vytvoření** | **Update** | **Odstranění** | **Důležitá poznámka**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektový úkol            | Ano        | Ano        | Ano        | Pole **Pokrok**, **EffortCompleted** a **EffortRemaining** lze upravovat v Project for the Web, ale nelze je upravovat v Project Operations.                                                                                                                                                                                             |
| Závislost projektového úkolu | Ano        | No         | Ano        | Záznamy závislostí projektových úkolů se neaktualizují. Místo toho lze starý záznam odstranit a vytvořit nový záznam.                                                                                                                                                                                                                                 |
| Přiřazení zdroje     | Ano        | Ano\*      | Ano        | Operace s následujícími poli nejsou podporovány: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** a **PlannedWork**. Záznamy přiřazení zdrojů se neaktualizují. Místo toho lze starý záznam odstranit a vytvořit nový záznam. Pro aktualizaci průběhové křivky přiřazení zdrojů slouží samostatné rozhraní API. |
| Kbelík projektu          | Ano        | Ano        | Ano        | Výchozí segment je vytvořen pomocí API **CreateProjectV1**. V aktualizaci 16 byla přidána podpora pro vytváření a odstraňování skupin projektů.                                                                                                                                                                                                   |
| Člen projektového týmu     | Ano        | Ano        | Ano        | Pro operaci vytvoření použijte API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Ano        | Ano        |            | Operace s následujícími poli nejsou podporovány: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** a **Duration**.                                                                                       |
| Kontrolní seznamy projektu      | Ano        | Ano        | Ano        |                                                                                                                                                                                                                                                                                                                                                         |
| Popisek projektu           | No         | Ano        | No         | Názvy popisků lze změnit. Tato funkce je k dispozici pouze pro Project for the Web                                                                                                                                                                                                                                                                      |
| Projektový úkol k popisku   | Ano        | No         | Ano        | Tato funkce je k dispozici pouze pro Project for the Web                                                                                                                                                                                                                                                                                                  |
| Sprint projektu          | Ano        | Ano        | Ano        | Pole **Zahájení** musí mít dřívější datum než pole **Dokončení**. Sprinty pro stejný projekt se nemohou navzájem překrývat. Tato funkce je k dispozici pouze pro Project for the Web                                                                                                                                                                    |




Vlastnost ID je volitelná. Pokud je k dispozici, systém se pokusí ji použít a vyvolá výjimku, pokud ji nelze použít. Pokud není k dispozici, systém jej vygeneruje.

**Omezení a známé problémy**

Následuje seznam omezení a známých problémů:

-   Rozhraní API plánu projektu mohou používat pouze **Uživatelé s licencí Microsoft Project**. Nemohou je používat:
    -   Uživatelé aplikace
    -   Systémoví uživatelé
    -   Uživatelé integrace
    -   Ostatní uživatelé, kteří nemají požadovanou licenci
-   Každá sada **OperationSet** může mít maximálně 100 operací.
-   Každý uživatel může mít maximálně 10 otevřených sad **OperationSet**.
-   Project Operations v současné době podporuje maximálně 500 úkolů v jednom projektu.
-   Každá operace Aktualizovat průběhovou křivku přiřazení zdrojů se počítá jako jedna operace.
-   Každý seznam aktualizovaných průběhových křivek může obsahovat maximálně 100 časových řezů.
-   Stav selhání a protokoly selhání nejsou u sad **OperationSet** aktuálně k dispozici.
-   Na jeden projekt lze použít maximálně 400 sprintů.
-   [Omezení a hranice projektů a úkolů](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Popisky jsou momentálně k dispozici pouze pro Project for the Web.

**Zpracování chyb**

-   Chcete-li zkontrolovat chyby generované ze sad operací, přejděte na **Nastavení** \> **Naplánovat integraci** \> **Sady operací**.
-   Chcete-li zkontrolovat chyby generované službou plánování projektu, přejděte na **Nastavení** \> **Integrace plánu** \> **Protokoly chyb PSS**.

**Úprava průběhových křivek přiřazení zdrojů**

Na rozdíl od všech ostatních rozhraní API, která aktualizují entity, je rozhraní API průběhové křivky přiřazení zdrojů zodpovědné výhradně za aktualizace jediného pole msdyn_plannedwork v jedné entitě msydn_resourceassignment.

Daný režim plánu je:

-   **pevné jednotky**
-   kalendář projektu je 9–17 hod je 9–17 hod PST, pondělí, út, čtvrtek, pátek (ŽÁDNÉ PRACOVNÍ STŘEDY)
-   a kalendář zdrojů je 9–13 hod PST od pondělí do pátku

Toto přiřazení platí na jeden týden, čtyři hodiny denně. Důvodem je, že kalendář zdrojů je od 9–13 hod PST nebo čtyři hodiny denně.

| &nbsp;     | Úloha | Počáteční datum | Datum ukončení  | Množství | 13. 6. 2022 | 14. 6. 2022 | 15. 6. 2022 | 16. 6. 2022 | 17. 6. 2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9–13 pracovník |  T1  | 13. 6. 2022  | 17. 6. 2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Pokud například chcete, aby pracovník tento týden pracoval pouze tři hodiny denně a jednu hodinu si ponechal na jiné úkoly.

#### <a name="updatedcontours-sample-payload"></a>Ukázková datová část pro UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Toto je přiřazení po spuštění rozhraní API Aktualizovat plán průběhové křivky.

| &nbsp;     | Úloha | Počáteční datum | Datum ukončení  | Množství | 13. 6. 2022 | 14. 6. 2022 | 15. 6. 2022 | 16. 6. 2022 | 17. 6. 2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9–13 pracovník | T1   | 13. 6. 2022  | 17. 6. 2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Ukázkový scénář**

V tomto scénáři vytvoříte projekt, člena týmu, čtyři úkoly a dvě přiřazení prostředků. Dále aktualizujete jeden úkol, aktualizujete projekt, odstraníte jeden úkol, odstraníte jedno přiřazení prostředku a vytvoříte závislost úkolu.

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

** Další ukázky

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
