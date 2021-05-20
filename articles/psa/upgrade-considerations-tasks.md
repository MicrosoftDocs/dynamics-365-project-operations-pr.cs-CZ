---
title: Důležité informace o upgradu pro strukturovaný rozpis prací
description: Toto téma obsahuje informace o upgradu strukturovaného rozpisu prací z verze Project Service Automation 2.x na 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d31ca60b267063e9cadf544468ece501353950fa
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951336"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="de447-103">Důležité informace o upgradu pro strukturovaný rozpis prací</span><span class="sxs-lookup"><span data-stu-id="de447-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="de447-104">Toto téma obsahuje informace o upgradu strukturovaného rozpisu prací z verze Project Service Automation 2.x na 3.x.</span><span class="sxs-lookup"><span data-stu-id="de447-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="de447-105">Toto téma definuje zdravý stav projektu v aplikaci Project Service Automation (PSA), který je nutný pro úspěšný upgrade.</span><span class="sxs-lookup"><span data-stu-id="de447-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="de447-106">Obsahuje také informace o běžných blokovacích podmínkách, které způsobí selhání upgradu.</span><span class="sxs-lookup"><span data-stu-id="de447-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="de447-107">Další informace o definování úkolů projektu a jejich funkcích v rámci plánu projektu naleznete v tématu [Projektové plány](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="de447-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="de447-108">Klíčové entity</span><span class="sxs-lookup"><span data-stu-id="de447-108">Key entities</span></span>
<span data-ttu-id="de447-109">Pro přesný strukturovaný rozpis prací, ve kterém jsou již načteny zdroje, jsou vyžadovány následující entity:</span><span class="sxs-lookup"><span data-stu-id="de447-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="de447-110">Projekt</span><span class="sxs-lookup"><span data-stu-id="de447-110">Project</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="de447-111">Projektový tým</span><span class="sxs-lookup"><span data-stu-id="de447-111">Project Team</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="de447-112">Projektový úkol</span><span class="sxs-lookup"><span data-stu-id="de447-112">Project Task</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="de447-113">Přiřazení zdrojů</span><span class="sxs-lookup"><span data-stu-id="de447-113">Resource Assignments</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="de447-114">Závislost projektového úkolu</span><span class="sxs-lookup"><span data-stu-id="de447-114">Project Task Dependency</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="de447-115">Rezervovatelné zdroje</span><span class="sxs-lookup"><span data-stu-id="de447-115">Bookable Resources</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="de447-116">Chcete-li definovat strukturovaný rozpis prací s načtenými zdroji, je třeba provést následující kroky:</span><span class="sxs-lookup"><span data-stu-id="de447-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="de447-117">Vytvořte nový projekt.</span><span class="sxs-lookup"><span data-stu-id="de447-117">Create a new project.</span></span> <span data-ttu-id="de447-118">Další informace o vytvoření nového projektu naleznete v tématu [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="de447-118">For more information about how to create a new project, see [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="de447-119">Vytvořte jeden nebo více úkolů.</span><span class="sxs-lookup"><span data-stu-id="de447-119">Create one or more tasks.</span></span> <span data-ttu-id="de447-120">Další informace o vytvoření nového úkolu naleznete v tématu [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="de447-120">For more information about how to create a task, see [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="de447-121">Definujte závislosti mezi úkoly.</span><span class="sxs-lookup"><span data-stu-id="de447-121">Define the task dependencies.</span></span> <span data-ttu-id="de447-122">Další informace viz [Závislost projektového úkolu](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="de447-122">For more information, see [Project Task Dependency](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="de447-123">Přiřaďte členy projektového týmu k projektu.</span><span class="sxs-lookup"><span data-stu-id="de447-123">Assign project team members to the project.</span></span> <span data-ttu-id="de447-124">Další informace naleznete v tématu [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="de447-124">For more information, see [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="de447-125">Přiřaďte členy projektového týmu k úkolům.</span><span class="sxs-lookup"><span data-stu-id="de447-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="de447-126">Další informace naleznete v tématu [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="de447-126">For more information, see [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="de447-127">Vztahy v projektovém týmu</span><span class="sxs-lookup"><span data-stu-id="de447-127">Project team relationships</span></span>

<span data-ttu-id="de447-128">Aby bylo možné zajistit úspěšný upgrade, je nutné správně udržovat následující vztahy:</span><span class="sxs-lookup"><span data-stu-id="de447-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="de447-129">Všem členům projektového týmu musí být přiřazen rezervovatelný zdroj.</span><span class="sxs-lookup"><span data-stu-id="de447-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="de447-130">Všichni členové projektového týmu musí být přiřazeni ke stejnému projektu.</span><span class="sxs-lookup"><span data-stu-id="de447-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="de447-131">Vztahy úkolu projektu</span><span class="sxs-lookup"><span data-stu-id="de447-131">Project task relationships</span></span>
<span data-ttu-id="de447-132">Aby bylo možné zajistit úspěšný upgrade, je nutné správně udržovat následující vztahy:</span><span class="sxs-lookup"><span data-stu-id="de447-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="de447-133">Všechny související úkoly musí být přiřazeny ke stejnému projektu.</span><span class="sxs-lookup"><span data-stu-id="de447-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="de447-134">Každý úkol na řádku musí mít nadřazený úkol.</span><span class="sxs-lookup"><span data-stu-id="de447-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="de447-135">Každý úkol musí mít nadřazený projekt.</span><span class="sxs-lookup"><span data-stu-id="de447-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="de447-136">Platné podmínky</span><span class="sxs-lookup"><span data-stu-id="de447-136">Valid conditions</span></span>

- <span data-ttu-id="de447-137">Všechny doby trvání úkolů musí být větší nebo rovny (>=) jedné hodině a menší než 1 800 000 minut (1 250 dní).\*</span><span class="sxs-lookup"><span data-stu-id="de447-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="de447-138">Všechny úkoly musí mít počáteční datum nejdříve 1. 1. 2000.\*</span><span class="sxs-lookup"><span data-stu-id="de447-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="de447-139">Všechny úkoly musí mít počáteční datum nejpozději 17 let od dnešního dne.\*</span><span class="sxs-lookup"><span data-stu-id="de447-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="de447-140">Všechny úkoly musí mít počáteční datum dřívější nebo shodné s datem dokončení.</span><span class="sxs-lookup"><span data-stu-id="de447-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="de447-141">Všechny typy transakcí v klasifikacích (výdaje, materiál, daň a čas) musí mít hodnoty pro **Výchozí jednotku** a **Skupinu jednotek**.</span><span class="sxs-lookup"><span data-stu-id="de447-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="de447-142">Je třeba se vyhnout formátům data s písmeny.</span><span class="sxs-lookup"><span data-stu-id="de447-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="de447-143">Potenciální postup zmírnění</span><span class="sxs-lookup"><span data-stu-id="de447-143">Potential mitigation steps</span></span>
- <span data-ttu-id="de447-144">Pomocí rozšířeného hledání lze identifikovat projektové úkoly, které neobsahují ID projektu.</span><span class="sxs-lookup"><span data-stu-id="de447-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="de447-145">Pomocí rozšířeného hledání lze identifikovat projektové úkoly, u nichž je plánované trvání delší než> 1 800 000.</span><span class="sxs-lookup"><span data-stu-id="de447-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="de447-146">Před provedením jakýchkoli změn dat byste měli prozkoumat všechna vlastní nastavení spojená s entitou, která mohla vést k tomu, že se data dostanou do špatného stavu.</span><span class="sxs-lookup"><span data-stu-id="de447-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="de447-147">Tato vlastní nastavení by měla být vyřešena před provedením jakékoli aktualizace týkající se dat.</span><span class="sxs-lookup"><span data-stu-id="de447-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="de447-148">U identifikovaných úkolů, které jsou osiřelé, zvažte odstranění těchto úkolů, pokud nejsou potřeba nebo pokud by měly být přidruženy ke správnému nadřazenému projektu.</span><span class="sxs-lookup"><span data-stu-id="de447-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="de447-149">U všech úkolů, jejichž trvání je delší než 1 250 dní, zvažte přidání více úkolů, které představují celkové trvání, pokud je to možné.</span><span class="sxs-lookup"><span data-stu-id="de447-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="de447-150">Položky označené hvězdičkou (\*) mají limity, které jsou způsobeny skutečností, že správa vztahů se zákazníky (CRM) podporuje pouze 7 320 rozšíření opakování.</span><span class="sxs-lookup"><span data-stu-id="de447-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="de447-151">Musíte zůstat pod tímto limitem.</span><span class="sxs-lookup"><span data-stu-id="de447-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="de447-152">Vztahy přiřazení zdroje</span><span class="sxs-lookup"><span data-stu-id="de447-152">Resource Assignment relationships</span></span>
<span data-ttu-id="de447-153">Aby bylo možné zajistit úspěšný upgrade, je nutné správně udržovat následující vztahy:</span><span class="sxs-lookup"><span data-stu-id="de447-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="de447-154">Všechna přiřazení zdrojů ve strukturovaném rozpisu prací musí souviset se stejným projektem.</span><span class="sxs-lookup"><span data-stu-id="de447-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="de447-155">Všechna přiřazení zdrojů ve strukturovaném rozpisu prací musí být přiřazeny členům projektového týmu ve stejném projektu.</span><span class="sxs-lookup"><span data-stu-id="de447-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="de447-156">Potenciální postup zmírnění</span><span class="sxs-lookup"><span data-stu-id="de447-156">Potential mitigation steps</span></span>
- <span data-ttu-id="de447-157">Určete všechny úkoly, které nespadají do výše popsaných podmínek.</span><span class="sxs-lookup"><span data-stu-id="de447-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="de447-158">Všechna přiřazení zdrojů, která již nejsou platná, by měla být odstraněna.</span><span class="sxs-lookup"><span data-stu-id="de447-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="de447-159">Vztahy závislosti úkolů projektu</span><span class="sxs-lookup"><span data-stu-id="de447-159">Project task dependency relationships</span></span>
<span data-ttu-id="de447-160">Aby bylo možné zajistit úspěšný upgrade, je nutné správně udržovat následující vztahy:</span><span class="sxs-lookup"><span data-stu-id="de447-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="de447-161">Všechny závislosti úkolů projektu musí souviset se stejným projektem.</span><span class="sxs-lookup"><span data-stu-id="de447-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="de447-162">Úkol nesmí mít stejnou závislost odkazovanou více než jednou.</span><span class="sxs-lookup"><span data-stu-id="de447-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]