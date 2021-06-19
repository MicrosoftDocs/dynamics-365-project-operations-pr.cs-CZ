---
title: Vývoj šablon projektů pomocí kopírování projektu
description: Tento téma poskytuje informace o tom, jak vytvořit šablony projektu pomocí vlastní akce Kopírovat projekt.
author: stsporen
ms.date: 01/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 7a1f602e789e07014fd6c742940f52341ce6c672
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005648"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="cfe88-103">Vývoj šablon projektů pomocí kopírování projektu</span><span class="sxs-lookup"><span data-stu-id="cfe88-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="cfe88-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="cfe88-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="cfe88-105">Dynamics 365 Project Operations podporuje schopnost kopírovat projekt a vrátit jakékoli přiřazení zpět k obecným prostředkům, které představují roli.</span><span class="sxs-lookup"><span data-stu-id="cfe88-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="cfe88-106">Zákazníci mohou pomocí této funkce vytvářet základní šablony projektů.</span><span class="sxs-lookup"><span data-stu-id="cfe88-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="cfe88-107">Když vyberete **Kopírovat projekt**, je aktualizován stav cílového projektu.</span><span class="sxs-lookup"><span data-stu-id="cfe88-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="cfe88-108">Použijte **Důvod stavu** k určení, kdy je akce kopírování dokončena.</span><span class="sxs-lookup"><span data-stu-id="cfe88-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="cfe88-109">Výběr možnosti **Kopírovat projekt** také aktualizuje počáteční datum projektu na aktuální počáteční datum, pokud v entitě cílového projektu není zjištěno žádné cílové datum.</span><span class="sxs-lookup"><span data-stu-id="cfe88-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="cfe88-110">Vlastní akce Kopírovat projekt</span><span class="sxs-lookup"><span data-stu-id="cfe88-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="cfe88-111">Jméno</span><span class="sxs-lookup"><span data-stu-id="cfe88-111">Name</span></span> 

<span data-ttu-id="cfe88-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="cfe88-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="cfe88-113">Vstupní parametry</span><span class="sxs-lookup"><span data-stu-id="cfe88-113">Input parameters</span></span>
<span data-ttu-id="cfe88-114">Jsou tři vstupní parametry:</span><span class="sxs-lookup"><span data-stu-id="cfe88-114">There are three input parameters:</span></span>

| <span data-ttu-id="cfe88-115">Parametr</span><span class="sxs-lookup"><span data-stu-id="cfe88-115">Parameter</span></span>          | <span data-ttu-id="cfe88-116">Typ</span><span class="sxs-lookup"><span data-stu-id="cfe88-116">Type</span></span>   | <span data-ttu-id="cfe88-117">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="cfe88-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="cfe88-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="cfe88-118">ProjectCopyOption</span></span>  | <span data-ttu-id="cfe88-119">String</span><span class="sxs-lookup"><span data-stu-id="cfe88-119">String</span></span> | <span data-ttu-id="cfe88-120">**{"removeNamedResources":true}** nebo **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="cfe88-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="cfe88-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="cfe88-121">SourceProject</span></span>      | <span data-ttu-id="cfe88-122">Odkaz na entitu</span><span class="sxs-lookup"><span data-stu-id="cfe88-122">Entity Reference</span></span> | <span data-ttu-id="cfe88-123">Zdrojový projekt</span><span class="sxs-lookup"><span data-stu-id="cfe88-123">Source Project</span></span> |
| <span data-ttu-id="cfe88-124">Cíl</span><span class="sxs-lookup"><span data-stu-id="cfe88-124">Target</span></span>             | <span data-ttu-id="cfe88-125">Odkaz na entitu</span><span class="sxs-lookup"><span data-stu-id="cfe88-125">Entity Reference</span></span> | <span data-ttu-id="cfe88-126">Cílový projekt</span><span class="sxs-lookup"><span data-stu-id="cfe88-126">Target Project</span></span> |


- <span data-ttu-id="cfe88-127">**{"clearTeamsAndAssignments":true}**: Výchozí chování pro Project for the Web a odstraní všechna přiřazení a členy týmu.</span><span class="sxs-lookup"><span data-stu-id="cfe88-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="cfe88-128">**{"removeNamedResources":true}** Výchozí chování pro Project Operations a vrátí přiřazení na obecné prostředky.</span><span class="sxs-lookup"><span data-stu-id="cfe88-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="cfe88-129">Další informace o akcích naleznete v části [Použití akcí Web API](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="cfe88-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="cfe88-130">Zadejte pole ke kopírování</span><span class="sxs-lookup"><span data-stu-id="cfe88-130">Specify fields to copy</span></span> 
<span data-ttu-id="cfe88-131">Po zavolání se akce **Kopírovat projekt** podívá na pohled projektu **Kopírovat sloupce projektu** k určení, která pole se mají kopírovat při kopírování projektu.</span><span class="sxs-lookup"><span data-stu-id="cfe88-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="cfe88-132">Příklad</span><span class="sxs-lookup"><span data-stu-id="cfe88-132">Example</span></span>
<span data-ttu-id="cfe88-133">Následující příklad ukazuje, jak volat vlastní akci **CopyProject** vlastní akce se sadou parametrů **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="cfe88-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
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