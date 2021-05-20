---
title: Vývoj šablon projektů pomocí kopírování projektu
description: Tento téma poskytuje informace o tom, jak vytvořit šablony projektu pomocí vlastní akce Kopírovat projekt.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cc17df0c73b276048f7c4b04bd9dc6644e828dc0
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949806"
---
# <a name="develop-project-templates-with-copy-project"></a>Vývoj šablon projektů pomocí kopírování projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations podporuje schopnost kopírovat projekt a vrátit jakékoli přiřazení zpět k obecným prostředkům, které představují roli. Zákazníci mohou pomocí této funkce vytvářet základní šablony projektů.

Když vyberete **Kopírovat projekt**, je aktualizován stav cílového projektu. Použijte **Důvod stavu** k určení, kdy je akce kopírování dokončena. Výběr možnosti **Kopírovat projekt** také aktualizuje počáteční datum projektu na aktuální počáteční datum, pokud v entitě cílového projektu není zjištěno žádné cílové datum.

## <a name="copy-project-custom-action"></a>Vlastní akce Kopírovat projekt 

### <a name="name"></a>Jméno 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Vstupní parametry
Jsou tři vstupní parametry:

| Parametr          | Typ   | Hodnoty                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** nebo **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Odkaz na entitu | Zdrojový projekt |
| Cíl             | Odkaz na entitu | Cílový projekt |


- **{"clearTeamsAndAssignments":true}**: Výchozí chování pro Project for the Web a odstraní všechna přiřazení a členy týmu.
- **{"removeNamedResources":true}** Výchozí chování pro Project Operations a vrátí přiřazení na obecné prostředky.

Další informace o akcích naleznete v části [Použití akcí Web API](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Zadejte pole ke kopírování 
Po zavolání se akce **Kopírovat projekt** podívá na pohled projektu **Kopírovat sloupce projektu** k určení, která pole se mají kopírovat při kopírování projektu.


### <a name="example"></a>Příklad
Následující příklad ukazuje, jak volat vlastní akci **CopyProject** vlastní akce se sadou parametrů **removeNamedResources**.
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]