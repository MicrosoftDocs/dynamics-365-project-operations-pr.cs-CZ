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
ms.openlocfilehash: cea8ce7f61fbc0f0c8c8deb522bc332be102238d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149535"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="2d685-103">Důležité informace o upgradu pro strukturovaný rozpis prací</span><span class="sxs-lookup"><span data-stu-id="2d685-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2d685-104">Toto téma obsahuje informace o upgradu strukturovaného rozpisu prací z verze Project Service Automation 2.x na 3.x.</span><span class="sxs-lookup"><span data-stu-id="2d685-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="2d685-105">Toto téma definuje zdravý stav projektu v aplikaci Project Service Automation (PSA), který je nutný pro úspěšný upgrade.</span><span class="sxs-lookup"><span data-stu-id="2d685-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="2d685-106">Obsahuje také informace o běžných blokovacích podmínkách, které způsobí selhání upgradu.</span><span class="sxs-lookup"><span data-stu-id="2d685-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="2d685-107">Další informace o definování úkolů projektu a jejich funkcích v rámci plánu projektu naleznete v tématu [Projektové plány](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="2d685-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="2d685-108">Klíčové entity</span><span class="sxs-lookup"><span data-stu-id="2d685-108">Key entities</span></span>
<span data-ttu-id="2d685-109">Pro přesný strukturovaný rozpis prací, ve kterém jsou již načteny zdroje, jsou vyžadovány následující entity:</span><span class="sxs-lookup"><span data-stu-id="2d685-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="2d685-110">Projekt</span><span class="sxs-lookup"><span data-stu-id="2d685-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="2d685-111">Projektový tým</span><span class="sxs-lookup"><span data-stu-id="2d685-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="2d685-112">Projektový úkol</span><span class="sxs-lookup"><span data-stu-id="2d685-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="2d685-113">Přiřazení zdrojů</span><span class="sxs-lookup"><span data-stu-id="2d685-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="2d685-114">Závislost projektového úkolu</span><span class="sxs-lookup"><span data-stu-id="2d685-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="2d685-115">Rezervovatelné zdroje</span><span class="sxs-lookup"><span data-stu-id="2d685-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="2d685-116">Chcete-li definovat strukturovaný rozpis prací s načtenými zdroji, je třeba provést následující kroky:</span><span class="sxs-lookup"><span data-stu-id="2d685-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="2d685-117">Vytvořte nový projekt.</span><span class="sxs-lookup"><span data-stu-id="2d685-117">Create a new project.</span></span> <span data-ttu-id="2d685-118">Další informace o vytvoření nového projektu naleznete v tématu [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="2d685-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="2d685-119">Vytvořte jeden nebo více úkolů.</span><span class="sxs-lookup"><span data-stu-id="2d685-119">Create one or more tasks.</span></span> <span data-ttu-id="2d685-120">Další informace o vytvoření nového úkolu naleznete v tématu [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="2d685-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="2d685-121">Definujte závislosti mezi úkoly.</span><span class="sxs-lookup"><span data-stu-id="2d685-121">Define the task dependencies.</span></span> <span data-ttu-id="2d685-122">Další informace viz [Závislost projektového úkolu](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="2d685-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="2d685-123">Přiřaďte členy projektového týmu k projektu.</span><span class="sxs-lookup"><span data-stu-id="2d685-123">Assign project team members to the project.</span></span> <span data-ttu-id="2d685-124">Další informace naleznete v tématu [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="2d685-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="2d685-125">Přiřaďte členy projektového týmu k úkolům.</span><span class="sxs-lookup"><span data-stu-id="2d685-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="2d685-126">Další informace naleznete v tématu [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="2d685-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="2d685-127">Vztahy v projektovém týmu</span><span class="sxs-lookup"><span data-stu-id="2d685-127">Project team relationships</span></span>

<span data-ttu-id="2d685-128">Aby bylo možné zajistit úspěšný upgrade, je nutné správně udržovat následující vztahy:</span><span class="sxs-lookup"><span data-stu-id="2d685-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="2d685-129">Všem členům projektového týmu musí být přiřazen rezervovatelný zdroj.</span><span class="sxs-lookup"><span data-stu-id="2d685-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="2d685-130">Všichni členové projektového týmu musí být přiřazeni ke stejnému projektu.</span><span class="sxs-lookup"><span data-stu-id="2d685-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="2d685-131">Vztahy úkolu projektu</span><span class="sxs-lookup"><span data-stu-id="2d685-131">Project task relationships</span></span>
<span data-ttu-id="2d685-132">Aby bylo možné zajistit úspěšný upgrade, je nutné správně udržovat následující vztahy:</span><span class="sxs-lookup"><span data-stu-id="2d685-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="2d685-133">Všechny související úkoly musí být přiřazeny ke stejnému projektu.</span><span class="sxs-lookup"><span data-stu-id="2d685-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="2d685-134">Každý úkol na řádku musí mít nadřazený úkol.</span><span class="sxs-lookup"><span data-stu-id="2d685-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="2d685-135">Každý úkol musí mít nadřazený projekt.</span><span class="sxs-lookup"><span data-stu-id="2d685-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="2d685-136">Platné podmínky</span><span class="sxs-lookup"><span data-stu-id="2d685-136">Valid conditions</span></span>

- <span data-ttu-id="2d685-137">Všechny doby trvání úkolů musí být větší nebo rovny (>=) jedné hodině a menší než 1 800 000 minut (1 250 dní).\*</span><span class="sxs-lookup"><span data-stu-id="2d685-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="2d685-138">Všechny úkoly musí mít počáteční datum nejdříve 1. 1. 2000.\*</span><span class="sxs-lookup"><span data-stu-id="2d685-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="2d685-139">Všechny úkoly musí mít počáteční datum nejpozději 17 let od dnešního dne.\*</span><span class="sxs-lookup"><span data-stu-id="2d685-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="2d685-140">Všechny úkoly musí mít počáteční datum dřívější nebo shodné s datem dokončení.</span><span class="sxs-lookup"><span data-stu-id="2d685-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="2d685-141">Všechny typy transakcí v klasifikacích (výdaje, materiál, daň a čas) musí mít hodnoty pro **Výchozí jednotku** a **Skupinu jednotek**.</span><span class="sxs-lookup"><span data-stu-id="2d685-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="2d685-142">Je třeba se vyhnout formátům data s písmeny.</span><span class="sxs-lookup"><span data-stu-id="2d685-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="2d685-143">Potenciální postup zmírnění</span><span class="sxs-lookup"><span data-stu-id="2d685-143">Potential mitigation steps</span></span>
- <span data-ttu-id="2d685-144">Pomocí rozšířeného hledání lze identifikovat projektové úkoly, které neobsahují ID projektu.</span><span class="sxs-lookup"><span data-stu-id="2d685-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="2d685-145">Pomocí rozšířeného hledání lze identifikovat projektové úkoly, u nichž je plánované trvání delší než> 1 800 000.</span><span class="sxs-lookup"><span data-stu-id="2d685-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="2d685-146">Před provedením jakýchkoli změn dat byste měli prozkoumat všechna vlastní nastavení spojená s entitou, která mohla vést k tomu, že se data dostanou do špatného stavu.</span><span class="sxs-lookup"><span data-stu-id="2d685-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="2d685-147">Tato vlastní nastavení by měla být vyřešena před provedením jakékoli aktualizace týkající se dat.</span><span class="sxs-lookup"><span data-stu-id="2d685-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="2d685-148">U identifikovaných úkolů, které jsou osiřelé, zvažte odstranění těchto úkolů, pokud nejsou potřeba nebo pokud by měly být přidruženy ke správnému nadřazenému projektu.</span><span class="sxs-lookup"><span data-stu-id="2d685-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="2d685-149">U všech úkolů, jejichž trvání je delší než 1 250 dní, zvažte přidání více úkolů, které představují celkové trvání, pokud je to možné.</span><span class="sxs-lookup"><span data-stu-id="2d685-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="2d685-150">Položky označené hvězdičkou (\*) mají limity, které jsou způsobeny skutečností, že správa vztahů se zákazníky (CRM) podporuje pouze 7 320 rozšíření opakování.</span><span class="sxs-lookup"><span data-stu-id="2d685-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="2d685-151">Musíte zůstat pod tímto limitem.</span><span class="sxs-lookup"><span data-stu-id="2d685-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="2d685-152">Vztahy přiřazení zdroje</span><span class="sxs-lookup"><span data-stu-id="2d685-152">Resource Assignment relationships</span></span>
<span data-ttu-id="2d685-153">Aby bylo možné zajistit úspěšný upgrade, je nutné správně udržovat následující vztahy:</span><span class="sxs-lookup"><span data-stu-id="2d685-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="2d685-154">Všechna přiřazení zdrojů ve strukturovaném rozpisu prací musí souviset se stejným projektem.</span><span class="sxs-lookup"><span data-stu-id="2d685-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="2d685-155">Všechna přiřazení zdrojů ve strukturovaném rozpisu prací musí být přiřazeny členům projektového týmu ve stejném projektu.</span><span class="sxs-lookup"><span data-stu-id="2d685-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="2d685-156">Potenciální postup zmírnění</span><span class="sxs-lookup"><span data-stu-id="2d685-156">Potential mitigation steps</span></span>
- <span data-ttu-id="2d685-157">Určete všechny úkoly, které nespadají do výše popsaných podmínek.</span><span class="sxs-lookup"><span data-stu-id="2d685-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="2d685-158">Všechna přiřazení zdrojů, která již nejsou platná, by měla být odstraněna.</span><span class="sxs-lookup"><span data-stu-id="2d685-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="2d685-159">Vztahy závislosti úkolů projektu</span><span class="sxs-lookup"><span data-stu-id="2d685-159">Project task dependency relationships</span></span>
<span data-ttu-id="2d685-160">Aby bylo možné zajistit úspěšný upgrade, je nutné správně udržovat následující vztahy:</span><span class="sxs-lookup"><span data-stu-id="2d685-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="2d685-161">Všechny závislosti úkolů projektu musí souviset se stejným projektem.</span><span class="sxs-lookup"><span data-stu-id="2d685-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="2d685-162">Úkol nesmí mít stejnou závislost odkazovanou více než jednou.</span><span class="sxs-lookup"><span data-stu-id="2d685-162">A task can't have the same dependency referenced more than once.</span></span>
