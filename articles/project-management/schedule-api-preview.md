---
title: K provádění operací s entitami plánování použijte rozhraní API pro plánování projektu
description: Tento téma poskytuje informace a ukázky pro použití rozhraní API plánu projektu.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293219"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>K provádění operací s entitami plánování použijte rozhraní API pro plánování projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

> [!IMPORTANT] 
> Některé nebo všechny funkce uvedené v tomto tématu jsou k dispozici jako součást vydání verze Preview. Obsah a funkce se mohou změnit. 

## <a name="scheduling-entities"></a>Entity plánování

Rozhraní API plánování projektu umožňují provádět operace vytváření, aktualizace a mazání pomocí **Plánovacích entit**. Tyto entity jsou spravovány prostřednictvím modulu Plánování v aplikaci Project for the Web. Operace vytváření, aktualizace a odstraňování **entit plánování** byly ve starších verzích Dynamics 365 Project Operations omezeny.

Následující tabulka poskytuje úplný seznam entit plánu projektu.

| Název entity  | Logický název entity |
| --- | --- |
| Project | msdyn_project |
| Projektový úkol  | msdyn_projecttask  |
| Závislost projektového úkolu  | msdyn_projecttaskdependency  |
| Přiřazení zdroje | msdyn_resourceassignment |
| Kbelík projektu  | msdyn_projectbucket |
| Člen projektového týmu | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet je vzor jednotky práce, který lze použít, když musí být v rámci transakce zpracováno několik požadavků ovlivňujících plány.

## <a name="project-schedule-apis"></a>Rozhraní API plánu projektu

Následuje seznam aktuálních rozhraní API plánu projektu.

- **msdyn_CreateProjectV1** : Toto API lze použít k vytvoření projektu. Projekt a výchozí projektový kbelík se vytvoří okamžitě.
- **msdyn_CreateTeamMemberV1** : Toto API lze použít k vytvoření člena projektového týmu. Záznam člena týmu je vytvořen okamžitě.
- **msdyn_CreateOperationSetV1** : Toto API lze použít k naplánování několika požadavků, které je třeba provést v rámci transakce.
- **msdyn_PSSCreateV1** : Toto API lze použít k vytvoření entity. Entitou může být jakákoli entita plánování projektu, která podporuje operaci vytvoření.
- **msdyn_PSSUpdateV1** : Toto API lze použít k aktualizaci entity. Entitou může být jakákoli entita plánování projektu, která podporuje operaci aktualizace.
- **msdyn_PSSDeleteV1** : Toto API lze použít k odstranění entity. Entitou může být jakákoli entita plánování projektu, která podporuje operaci odstranění.
- **msdyn_ExecuteOperationSetV1** : Toto API se používá k provedení všech operací v rámci dané sady operací.

## <a name="using-project-schedule-apis-with-operationset"></a>Používání API plánu projektu s OperationSet

Protože záznamy s oběma rozhraními **CreateProjectV1** a **CreateTeamMemberV1** jsou vytvořeny okamžitě, nelze tato API použít v sadě **OperationSet** přímo. Můžete však použít API k vytvoření potřebných záznamů, vytvořit sadu **OperationSet** a poté použít tyto předem vytvořené záznamy v sadě **OperationSet**.

## <a name="supported-operations"></a>Podporované operace

| Entita plánování | Vytvoření | Aktualizace | Odstranění | Důležitá poznámka |
| --- | --- | --- | --- | --- |
Projektový úkol | Ano | Ano | Ano | Nic |
| Závislost projektového úkolu | Ano | Ano | | Záznamy závislostí projektových úkolů se neaktualizují. Místo toho lze starý záznam odstranit a vytvořit nový záznam. |
| Přiřazení zdroje | Ano | Ano | | Operace s následujícími poli nejsou podporovány: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** a **PlannedWork**. Záznamy přiřazení zdrojů se neaktualizují. Místo toho lze starý záznam odstranit a vytvořit nový záznam. |
| Kbelík projektu | Není k dispozici | Není k dispozici | Není k dispozici | Výchozí kbelík je vytvořen pomocí rozhraní API **CreateProjectV1**. |
| Člen projektového týmu | Ano | Ano | Ano | Pro operaci vytvoření použijte API **CreateTeamMemberV1**. |
| Project | Ano | Ano | Není k dispozici | Operace s následujícími poli nejsou podporovány: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** a **Duration**. |

Tato rozhraní API lze volat s objekty entit, které obsahují vlastní pole.

Vlastnost ID je volitelná. Pokud je k dispozici, systém se pokusí ji použít a vyvolá výjimku, pokud ji nelze použít. Pokud není k dispozici, systém jej vygeneruje.

## <a name="restricted-fields"></a>Omezená pole

Následující tabulky definují pole, která mají omezené funkce **Vytvořit** a **Upravit**.

### <a name="project-task"></a>Projektový úkol

| **Logický název**                       | **Je možné vytvořit** | **Může upravit**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | ne             | ne               |
| msdyn_actualcost_base                  | ne             | ne               |
| msdyn_actualend                        | ne             | ne               |
| msdyn_actualsales                      | ne             | ne               |
| msdyn_actualsales_base                 | ne             | ne               |
| msdyn_actualstart                      | ne             | ne               |
| msdyn_costatcompleteestimate           | ne             | ne               |
| msdyn_costatcompleteestimate_base      | ne             | ne               |
| msdyn_costconsumptionpercentage        | ne             | ne               |
| msdyn_effortcompleted                  | ne             | ne               |
| msdyn_effortestimateatcomplete         | ne             | ne               |
| msdyn_iscritical                       | ne             | ne               |
| msdyn_iscriticalname                   | ne             | ne               |
| msdyn_ismanual                         | ne             | ne               |
| msdyn_ismanualname                     | ne             | ne               |
| msdyn_ismilestone                      | ne             | ne               |
| msdyn_ismilestonename                  | ne             | ne               |
| msdyn_LinkStatus                       | ne             | ne               |
| msdyn_linkstatusname                   | ne             | ne               |
| msdyn_msprojectclientid                | ne             | ne               |
| msdyn_plannedcost                      | ne             | ne               |
| msdyn_plannedcost_base                 | ne             | ne               |
| msdyn_plannedsales                     | ne             | ne               |
| msdyn_plannedsales_base                | ne             | ne               |
| msdyn_pluginprocessingdata             | ne             | ne               |
| msdyn_progress                         | ne             | ne (ano pro P4W) |
| msdyn_remainingcost                    | ne             | ne               |
| msdyn_remainingcost_base               | ne             | ne               |
| msdyn_remainingsales                   | ne             | ne               |
| msdyn_remainingsales_base              | ne             | ne               |
| msdyn_requestedhours                   | ne             | ne               |
| msdyn_resourcecategory                 | ne             | ne               |
| msdyn_resourcecategoryname             | ne             | ne               |
| msdyn_resourceorganizationalunitid     | ne             | ne               |
| msdyn_resourceorganizationalunitidname | ne             | ne               |
| msdyn_salesconsumptionpercentage       | ne             | ne               |
| msdyn_salesestimateatcomplete          | ne             | ne               |
| msdyn_salesestimateatcomplete_base     | ne             | ne               |
| msdyn_salesvariance                    | ne             | ne               |
| msdyn_salesvariance_base               | ne             | ne               |
| msdyn_scheduleddurationminutes         | ne             | ne               |
| msdyn_scheduledend                     | ne             | ne               |
| msdyn_scheduledstart                   | ne             | ne               |
| msdyn_schedulevariance                 | ne             | ne               |
| msdyn_skipupdateestimateline           | ne             | ne               |
| msdyn_skipupdateestimatelinename       | ne             | ne               |
| msdyn_summary                          | ne             | ne               |
| msdyn_varianceofcost                   | ne             | ne               |
| msdyn_varianceofcost_base              | ne             | ne               |

### <a name="project-task-dependency"></a>Závislost projektového úkolu

| **Logický název**              | **Je možné vytvořit** | **Může upravit** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | ne             | ne           |
| msdyn_linktypename            | ne             | ne           |
| msdyn_predecessortask         | ano            | ne           |
| msdyn_predecessortaskname     | ano            | ne           |
| msdyn_project                 | ano            | ne           |
| msdyn_projectname             | ano            | ne           |
| msdyn_projecttaskdependencyid | ano            | ne           |
| msdyn_successortask           | ano            | ne           |
| msdyn_successortaskname       | ano            | ne           |

### <a name="resource-assignment"></a>Přiřazení zdroje

| **Logický název**             | **Je možné vytvořit** | **Může upravit** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | ano            | ne           |
| msdyn_bookableresourceidname | ano            | ne           |
| msdyn_bookingstatusid        | ne             | ne           |
| msdyn_bookingstatusidname    | ne             | ne           |
| msdyn_committype             | ne             | ne           |
| msdyn_committypename         | ne             | ne           |
| msdyn_effort                 | ne             | ne           |
| msdyn_effortcompleted        | ne             | ne           |
| msdyn_effortremaining        | ne             | ne           |
| msdyn_finish                 | ne             | ne           |
| msdyn_plannedcost            | ne             | ne           |
| msdyn_plannedcost_base       | ne             | ne           |
| msdyn_plannedcostcontour     | ne             | ne           |
| msdyn_plannedsales           | ne             | ne           |
| msdyn_plannedsales_base      | ne             | ne           |
| msdyn_plannedsalescontour    | ne             | ne           |
| msdyn_plannedwork            | ne             | ne           |
| msdyn_projectid              | ano            | ne           |
| msdyn_projectidname          | ne             | ne           |
| msdyn_projectteamid          | ne             | ne           |
| msdyn_projectteamidname      | ne             | ne           |
| msdyn_start                  | ne             | ne           |
| msdyn_taskid                 | ne             | ne           |
| msdyn_taskidname             | ne             | ne           |
| msdyn_userresourceid         | ne             | ne           |

### <a name="project-team-member"></a>Člen projektového týmu

| **Logický název**                                 | **Je možné vytvořit** | **Může upravit** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | ne             | ne           |
| msdyn_creategenericteammemberwithrequirementname | ne             | ne           |
| msdyn_deletestatus                               | ne             | ne           |
| msdyn_deletestatusname                           | ne             | ne           |
| msdyn_effort                                     | ne             | ne           |
| msdyn_effortcompleted                            | ne             | ne           |
| msdyn_effortremaining                            | ne             | ne           |
| msdyn_finish                                     | ne             | ne           |
| msdyn_hardbookedhours                            | ne             | ne           |
| msdyn_hours                                      | ne             | ne           |
| msdyn_markedfordeletiontimer                     | ne             | ne           |
| msdyn_markedfordeletiontimestamp                 | ne             | ne           |
| msdyn_msprojectclientid                          | ne             | ne           |
| msdyn_percentage                                 | ne             | ne           |
| msdyn_requiredhours                              | ne             | ne           |
| msdyn_softbookedhours                            | ne             | ne           |
| msdyn_start                                      | ne             | ne           |

### <a name="project"></a>Project

| **Logický název**                       | **Je možné vytvořit** | **Může upravit** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | ne             | ne           |
| msdyn_actualexpensecost_base           | ne             | ne           |
| msdyn_actuallaborcost                  | ne             | ne           |
| msdyn_actuallaborcost_base             | ne             | ne           |
| msdyn_actualsales                      | ne             | ne           |
| msdyn_actualsales_base                 | ne             | ne           |
| msdyn_contractlineproject              | ano            | ne           |
| msdyn_contractorganizationalunitid     | ano            | ne           |
| msdyn_contractorganizationalunitidname | ano            | ne           |
| msdyn_costconsumption                  | ne             | ne           |
| msdyn_costestimateatcomplete           | ne             | ne           |
| msdyn_costestimateatcomplete_base      | ne             | ne           |
| msdyn_costvariance                     | ne             | ne           |
| msdyn_costvariance_base                | ne             | ne           |
| msdyn_duration                         | ne             | ne           |
| msdyn_effort                           | ne             | ne           |
| msdyn_effortcompleted                  | ne             | ne           |
| msdyn_effortestimateatcompleteeac      | ne             | ne           |
| msdyn_effortremaining                  | ne             | ne           |
| msdyn_finish                           | ano            | ano          |
| msdyn_globalrevisiontoken              | ne             | ne           |
| msdyn_islinkedtomsprojectclient        | ne             | ne           |
| msdyn_islinkedtomsprojectclientname    | ne             | ne           |
| msdyn_linkeddocumenturl                | ne             | ne           |
| msdyn_msprojectdocument                | ne             | ne           |
| msdyn_msprojectdocumentname            | ne             | ne           |
| msdyn_plannedexpensecost               | ne             | ne           |
| msdyn_plannedexpensecost_base          | ne             | ne           |
| msdyn_plannedlaborcost                 | ne             | ne           |
| msdyn_plannedlaborcost_base            | ne             | ne           |
| msdyn_plannedsales                     | ne             | ne           |
| msdyn_plannedsales_base                | ne             | ne           |
| msdyn_progress                         | ne             | ne           |
| msdyn_remainingcost                    | ne             | ne           |
| msdyn_remainingcost_base               | ne             | ne           |
| msdyn_remainingsales                   | ne             | ne           |
| msdyn_remainingsales_base              | ne             | ne           |
| msdyn_replaylogheader                  | ne             | ne           |
| msdyn_salesconsumption                 | ne             | ne           |
| msdyn_salesestimateatcompleteeac       | ne             | ne           |
| msdyn_salesestimateatcompleteeac_base  | ne             | ne           |
| msdyn_salesvariance                    | ne             | ne           |
| msdyn_salesvariance_base               | ne             | ne           |
| msdyn_scheduleperformance              | ne             | ne           |
| msdyn_scheduleperformancename          | ne             | ne           |
| msdyn_schedulevariance                 | ne             | ne           |
| msdyn_taskearlieststart                | ne             | ne           |
| msdyn_teamsize                         | ne             | ne           |
| msdyn_teamsize_date                    | ne             | ne           |
| msdyn_teamsize_state                   | ne             | ne           |
| msdyn_totalactualcost                  | ne             | ne           |
| msdyn_totalactualcost_base             | ne             | ne           |
| msdyn_totalplannedcost                 | ne             | ne           |
| msdyn_totalplannedcost_base            | ne             | ne           |


## <a name="limitations-and-known-issues"></a>Omezení a známé problémy
Následuje seznam omezení a známých problémů:

- Rozhraní API plánu projektu mohou používat pouze **Uživatelé s licencí Microsoft Project.** Nemohou je používat:
    - Uživatelé aplikace
    - Systémoví uživatelé
    - Uživatelé integrace
    - Ostatní uživatelé, kteří nemají požadovanou licenci
- Každá sada **OperationSet** může mít maximálně 100 operací.
- Každý uživatel může mít maximálně 10 otevřených sad **OperationSet**.
- Project Operations v současné době podporuje maximálně 500 úkolů v jednom projektu.
- Stav selhání a protokoly selhání nejsou u sad **OperationSet** aktuálně k dispozici.
- [Meze a hranice projektů a úkolů](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Zpracování chyb

   - Chcete-li zkontrolovat chyby generované ze sad operací, přejděte na **Nastavení** \> **Naplánovat integraci** \> **Sady operací**.
   - Chcete-li zkontrolovat chyby generované službou plánování projektu, přejděte na **Nastavení** \> **Integrace plánu** \> **Protokoly chyb PSS**.

## <a name="sample-scenario"></a>Ukázkový scénář

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

## <a name="additional-samples"></a>Další ukázky

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
