---
title: Vývoj šablon projektů pomocí kopírování projektu
description: Tento téma poskytuje informace o tom, jak vytvořit šablony projektu pomocí vlastní akce Kopírovat projekt.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073720"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="00644-103">Vývoj šablon projektů pomocí kopírování projektu</span><span class="sxs-lookup"><span data-stu-id="00644-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="00644-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="00644-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="00644-105">Dynamics 365 Project Operations podporuje schopnost kopírovat projekt a vrátit všechna přiřazení zpět k obecným prostředkům, které představují roli.</span><span class="sxs-lookup"><span data-stu-id="00644-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="00644-106">Zákazníci mohou pomocí této funkce vytvářet základní šablony projektů.</span><span class="sxs-lookup"><span data-stu-id="00644-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="00644-107">Když vyberete **Kopírovat projekt** , je aktualizován stav cílového projektu.</span><span class="sxs-lookup"><span data-stu-id="00644-107">When you select **Copy Project** , the status of the target project is updated.</span></span> <span data-ttu-id="00644-108">Použijte **Důvod stavu** k určení, kdy je akce kopírování dokončena.</span><span class="sxs-lookup"><span data-stu-id="00644-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="00644-109">Výběr možnosti **Kopírovat projekt** také aktualizuje počáteční datum projektu na aktuální počáteční datum, pokud v entitě cílového projektu není zjištěno žádné cílové datum.</span><span class="sxs-lookup"><span data-stu-id="00644-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="00644-110">Vlastní akce Kopírovat projekt</span><span class="sxs-lookup"><span data-stu-id="00644-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="00644-111">Jméno</span><span class="sxs-lookup"><span data-stu-id="00644-111">Name</span></span> 

<span data-ttu-id="00644-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="00644-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="00644-113">Vstupní parametry</span><span class="sxs-lookup"><span data-stu-id="00644-113">Input parameters</span></span>
<span data-ttu-id="00644-114">Jsou tři vstupní parametry:</span><span class="sxs-lookup"><span data-stu-id="00644-114">There are three input parameters:</span></span>

| <span data-ttu-id="00644-115">Parametr</span><span class="sxs-lookup"><span data-stu-id="00644-115">Parameter</span></span>          | <span data-ttu-id="00644-116">Typ</span><span class="sxs-lookup"><span data-stu-id="00644-116">Type</span></span>   | <span data-ttu-id="00644-117">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="00644-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="00644-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="00644-118">ProjectCopyOption</span></span>  | <span data-ttu-id="00644-119">String</span><span class="sxs-lookup"><span data-stu-id="00644-119">String</span></span> | <span data-ttu-id="00644-120">**{"removeNamedResources":true}** nebo **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="00644-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="00644-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="00644-121">SourceProject</span></span>      | <span data-ttu-id="00644-122">Odkaz na entitu</span><span class="sxs-lookup"><span data-stu-id="00644-122">Entity Reference</span></span> | <span data-ttu-id="00644-123">Zdrojový projekt</span><span class="sxs-lookup"><span data-stu-id="00644-123">Source Project</span></span> |
| <span data-ttu-id="00644-124">Cíl</span><span class="sxs-lookup"><span data-stu-id="00644-124">Target</span></span>             | <span data-ttu-id="00644-125">Odkaz na entitu</span><span class="sxs-lookup"><span data-stu-id="00644-125">Entity Reference</span></span> | <span data-ttu-id="00644-126">Cílový projekt</span><span class="sxs-lookup"><span data-stu-id="00644-126">Target Project</span></span> |


- <span data-ttu-id="00644-127">**{"clearTeamsAndAssignments":true}** : Výchozí chování pro Project for the Web a odstraní všechna přiřazení a členy týmu.</span><span class="sxs-lookup"><span data-stu-id="00644-127">**{"clearTeamsAndAssignments":true}** : Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="00644-128">**{"removeNamedResources":true}** Výchozí chování pro Project Operations a vrátí přiřazení na obecné prostředky.</span><span class="sxs-lookup"><span data-stu-id="00644-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="00644-129">Další informace o akcích naleznete v části [Použití akcí Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="00644-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="00644-130">Zadejte pole ke kopírování</span><span class="sxs-lookup"><span data-stu-id="00644-130">Specify fields to copy</span></span> 
<span data-ttu-id="00644-131">Po zavolání se akce **Kopírovat projekt** podívá na pohled projektu **Kopírovat sloupce projektu** k určení, která pole se mají kopírovat při kopírování projektu.</span><span class="sxs-lookup"><span data-stu-id="00644-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
