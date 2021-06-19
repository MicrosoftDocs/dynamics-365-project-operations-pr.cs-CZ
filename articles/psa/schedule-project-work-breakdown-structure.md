---
title: Plánování projektu pomocí strukturovaného rozpisu prací
description: Postup plánování projektu pomocí strukturovaného rozpisu prací v Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
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
ms.openlocfilehash: 027bcbc8995ed39af78c7ff9b1028f401c3b0d4d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008573"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="e3813-103">Plánování projektu se strukturou rozpisu práce (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e3813-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e3813-104">Plán projektu uvádí, co je třeba udělat, které zdroje práci vykonají a časový rámec, ve kterém je třeba práci dokončit.</span><span class="sxs-lookup"><span data-stu-id="e3813-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="e3813-105">Plán projektu odráží všechny práce související s dodáním projektu včas.</span><span class="sxs-lookup"><span data-stu-id="e3813-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="e3813-106">Jedním z prvních kroků v počáteční fázi projektu je přijít s plánem projektu.</span><span class="sxs-lookup"><span data-stu-id="e3813-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="e3813-107">K vytvoření plánu projektu je nutné vytvořit strukturovaný rozpis prací.</span><span class="sxs-lookup"><span data-stu-id="e3813-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="e3813-108">Vytvořte strukturu projektu pomocí strukturovaného rozpisu prací, což vám pomůže:</span><span class="sxs-lookup"><span data-stu-id="e3813-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="e3813-109">Rozdělit práci na zvládnutelné úkoly</span><span class="sxs-lookup"><span data-stu-id="e3813-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="e3813-110">Odhadnout čas potřebný k dokončení úkolu</span><span class="sxs-lookup"><span data-stu-id="e3813-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="e3813-111">Nastavit závislostí a dobu trvání úkolu</span><span class="sxs-lookup"><span data-stu-id="e3813-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="e3813-112">Určit role potřebné k dokončení každého úkolu</span><span class="sxs-lookup"><span data-stu-id="e3813-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="e3813-113">Plán projektu ve strukturovaném rozpisu prací má známý vzhled a chování, včetně interaktivního Ganttova diagramu.</span><span class="sxs-lookup"><span data-stu-id="e3813-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="e3813-114">Vytvoření strukturovaného rozpisu prací pro projekt</span><span class="sxs-lookup"><span data-stu-id="e3813-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="e3813-115">Vytvořte strukturovaný rozpis prací pro znázornění posloupnosti úkolů v projektu.</span><span class="sxs-lookup"><span data-stu-id="e3813-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="e3813-116">Strukturovaný rozpis prací zahrnuje úkoly, požadavky na jednotlivé úkoly a informace o výnosech a nákladech.</span><span class="sxs-lookup"><span data-stu-id="e3813-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="e3813-117">Ve strukturovaném rozpisu prací můžete přidat:</span><span class="sxs-lookup"><span data-stu-id="e3813-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="e3813-118">Řadu úkolů v hierarchii</span><span class="sxs-lookup"><span data-stu-id="e3813-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="e3813-119">Další úkoly, které je nutno dokončit před zahájením úkolu</span><span class="sxs-lookup"><span data-stu-id="e3813-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="e3813-120">Počáteční datum, koncové datum a dobu trvání úkolu</span><span class="sxs-lookup"><span data-stu-id="e3813-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="e3813-121">Počet hodin, které jsou potřebné pro daný úkol</span><span class="sxs-lookup"><span data-stu-id="e3813-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="e3813-122">Jakékoli požadované dovednosti pracovníků a vzdělávání</span><span class="sxs-lookup"><span data-stu-id="e3813-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="e3813-123">Pracovníci, kteří jsou přiřazeni k úkolu</span><span class="sxs-lookup"><span data-stu-id="e3813-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="e3813-124">Odhadované výnosy a náklady</span><span class="sxs-lookup"><span data-stu-id="e3813-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="e3813-125">Typy úkolů</span><span class="sxs-lookup"><span data-stu-id="e3813-125">Task types</span></span>  
<span data-ttu-id="e3813-126">Při vytváření strukturovaného rozpisu prací budete používat následující typy úkolů:</span><span class="sxs-lookup"><span data-stu-id="e3813-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="e3813-127">**Kořenový uzel projektu**.</span><span class="sxs-lookup"><span data-stu-id="e3813-127">**Project root node**</span></span> | <span data-ttu-id="e3813-128">Souhrnný úkol nejvyšší úrovně pro projekt.</span><span class="sxs-lookup"><span data-stu-id="e3813-128">The top-level summary task for the project.</span></span> <span data-ttu-id="e3813-129">Všechny ostatní úkoly projektu jsou vytvořeny pod ním.</span><span class="sxs-lookup"><span data-stu-id="e3813-129">All other project tasks are created under it.</span></span> <span data-ttu-id="e3813-130">Název kořenového úkolu je název projektu.</span><span class="sxs-lookup"><span data-stu-id="e3813-130">The name of the root task is the project name.</span></span> <span data-ttu-id="e3813-131">Úsilí, data a doba trvání kořenového uzlu se zakládají na hodnotách v hierarchii pod ním.</span><span class="sxs-lookup"><span data-stu-id="e3813-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="e3813-132">Nelze upravit vlastnosti kořenového uzlu ani odstranit kořenový uzel.</span><span class="sxs-lookup"><span data-stu-id="e3813-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="e3813-133">**Souhrnné úkoly nebo úkoly kontejneru**</span><span class="sxs-lookup"><span data-stu-id="e3813-133">**Summary or container tasks**</span></span> | <span data-ttu-id="e3813-134">Souhrnný úkol je úkol, který má pod sebou dílčí úkoly.</span><span class="sxs-lookup"><span data-stu-id="e3813-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="e3813-135">Souhrnný úkol nemá žádné vlastní úsilí nebo své vlastní náklady.</span><span class="sxs-lookup"><span data-stu-id="e3813-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="e3813-136">Jeho pracovní úsilí a náklady jsou součtem jeho dílčích úkolů.</span><span class="sxs-lookup"><span data-stu-id="e3813-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="e3813-137">Můžete změnit název souhrnného úkolu, ale nelze změnit úsilí, data a dobu trvání, protože ty jsou vypočteny automaticky.</span><span class="sxs-lookup"><span data-stu-id="e3813-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="e3813-138">Odstraněním souhrnného úkolu odstraníte úkol a všechny jeho dílčí úkoly.</span><span class="sxs-lookup"><span data-stu-id="e3813-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="e3813-139">**Úkoly uzlu typu list**</span><span class="sxs-lookup"><span data-stu-id="e3813-139">**Leaf node tasks**</span></span> | <span data-ttu-id="e3813-140">Úkol uzlu typu list představuje nejpodrobnější práci na projektu.</span><span class="sxs-lookup"><span data-stu-id="e3813-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="e3813-141">Má odhadnuté úsilí, plánovaný počet prostředků, plánované datum zahájení a ukončení a dobu trvání.</span><span class="sxs-lookup"><span data-stu-id="e3813-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="e3813-142">Hierarchie úkolů</span><span class="sxs-lookup"><span data-stu-id="e3813-142">Task hierarchy</span></span>  
 <span data-ttu-id="e3813-143">Při vytváření hierarchie úkolů máte následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="e3813-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="e3813-144">**Přidat úkol**.</span><span class="sxs-lookup"><span data-stu-id="e3813-144">**Add task**.</span></span>   <span data-ttu-id="e3813-145">Můžete přidat úkol do zvoleného umístění v hierarchii úkolů.</span><span class="sxs-lookup"><span data-stu-id="e3813-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="e3813-146">Pokud nevyberete umístění, zobrazí se nový úkol na konci.</span><span class="sxs-lookup"><span data-stu-id="e3813-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="e3813-147">**Zvětšit odsazení úkolu**.</span><span class="sxs-lookup"><span data-stu-id="e3813-147">**Indent task**.</span></span>   <span data-ttu-id="e3813-148">Zvětšením odsazení úkolu jej můžete nastavit jako podřízený úkol úkolu přímo nad ním.</span><span class="sxs-lookup"><span data-stu-id="e3813-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="e3813-149">**Zmenšit odsazení úkolu**.</span><span class="sxs-lookup"><span data-stu-id="e3813-149">**Outdent task**.</span></span>   <span data-ttu-id="e3813-150">Zmenšením odsazení úkolu již nebude dílčím úkolem jeho původního nadřazeného úkolu.</span><span class="sxs-lookup"><span data-stu-id="e3813-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="e3813-151">**Posunout nahoru a Posunout dolů**.</span><span class="sxs-lookup"><span data-stu-id="e3813-151">**Move up and Move down**.</span></span>   <span data-ttu-id="e3813-152">Přesune úkoly nahoru nebo dolů v hierarchii jejich nadřazeného úkolu.</span><span class="sxs-lookup"><span data-stu-id="e3813-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="e3813-153">Přesunutí úkolu směrem nahoru nebo dolů nemá žádný vliv na jeho úsilí, náklady, data nebo dobu trvání.</span><span class="sxs-lookup"><span data-stu-id="e3813-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="e3813-154">Atributy úkolu</span><span class="sxs-lookup"><span data-stu-id="e3813-154">Task attributes</span></span>  
 <span data-ttu-id="e3813-155">Název úkolu popisuje práci, kterou je třeba vykonat.</span><span class="sxs-lookup"><span data-stu-id="e3813-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="e3813-156">K popisu plánu a požadavků na pracovníky využijte různé atributy úkolu.</span><span class="sxs-lookup"><span data-stu-id="e3813-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="e3813-157">Plánování atributů</span><span class="sxs-lookup"><span data-stu-id="e3813-157">Schedule attributes</span></span>

 - <span data-ttu-id="e3813-158">Přiřaďte hodnoty k možnostem **Hodiny úsilí**, **Počet zdrojů**, **Datum zahájení**, **Datum ukončení** a **Doba trvání** a stanovte plán úkolu.</span><span class="sxs-lookup"><span data-stu-id="e3813-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="e3813-159">**Úsilí** je odhadovaný počet hodin nutných k dokončení úkolu.</span><span class="sxs-lookup"><span data-stu-id="e3813-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="e3813-160">**Počet zdrojů** je odhad vedoucího projektu ohledně počtu osob, které jsou třeba pro nejlepší možný plán.</span><span class="sxs-lookup"><span data-stu-id="e3813-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="e3813-161">**Doba trvání** (ve dnech) označuje počet pracovních dnů, které budou třeba k dokončení úkolu.</span><span class="sxs-lookup"><span data-stu-id="e3813-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="e3813-162">Personální atributy</span><span class="sxs-lookup"><span data-stu-id="e3813-162">Staffing attributes</span></span>

 - <span data-ttu-id="e3813-163">**Role**, **Organizační jednotka zdroje**, **Počet zdrojů**, a **Zdroje** popisují požadavky na personální obsazení úkolu.</span><span class="sxs-lookup"><span data-stu-id="e3813-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="e3813-164">**Role** popisuje typ zdroje potřebný k provedení úkolu.</span><span class="sxs-lookup"><span data-stu-id="e3813-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="e3813-165">**Organizační jednotka zdroje** označuje organizační jednotku, ze které je pro tento úkol třeba zajistit zdroje. To ovlivní také nákladové a prodejní odhady úkolu, protože je třeba vzít tyto hodnoty v úvahu při určování jednotkové prodejní ceny zdroje.</span><span class="sxs-lookup"><span data-stu-id="e3813-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="e3813-166">**Zdroje** zahrnují obecné zdroje nebo pojmenované zdroje, pokud existují.</span><span class="sxs-lookup"><span data-stu-id="e3813-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="e3813-167">Závislosti úkolu</span><span class="sxs-lookup"><span data-stu-id="e3813-167">Task dependencies</span></span>  
 <span data-ttu-id="e3813-168">Můžete vytvořit vztahy mezi předchůdci pro jeden nebo více úkolů ve strukturovaném rozpisu prací.</span><span class="sxs-lookup"><span data-stu-id="e3813-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="e3813-169">Můžete nastavit jednu nebo více hodnot pro pole předchůdce úkolů, čímž označíte úkoly, na kterých bude záviset.</span><span class="sxs-lookup"><span data-stu-id="e3813-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="e3813-170">Když přiadíte hodnotu předchůdce k úkolu, můžete se úkol spustit pouze v případě, že byly dokončeny všechny úkoly typu předchůdce.</span><span class="sxs-lookup"><span data-stu-id="e3813-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="e3813-171">Výsledkem nastavení této závislosti na úkolu bude přepočet plánovaného data zahájení úkolu až po ukončení všech jeho předchůdců.</span><span class="sxs-lookup"><span data-stu-id="e3813-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="e3813-172">Vliv předchůdce na plán není omezen režimem úkolu definovaným v úkolu.</span><span class="sxs-lookup"><span data-stu-id="e3813-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="e3813-173">Režim úkolu</span><span class="sxs-lookup"><span data-stu-id="e3813-173">Task mode</span></span>  
 <span data-ttu-id="e3813-174">Režim úkolu je jedním z důležitých faktorů, které určují plánování úkolů uzlu typu list.</span><span class="sxs-lookup"><span data-stu-id="e3813-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="e3813-175">Existují dva režimy úkolů pro každý úkol: režim automatického plánování a režim ručního plánování.</span><span class="sxs-lookup"><span data-stu-id="e3813-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="e3813-176">**Automatické plánování**.</span><span class="sxs-lookup"><span data-stu-id="e3813-176">**Auto scheduling**.</span></span>   <span data-ttu-id="e3813-177">Při nastavení režimu úkolu na automatické plánování modul plánování úkolu používá pravidla plánování na následující atributy úkolu k určení plánu úkolu:</span><span class="sxs-lookup"><span data-stu-id="e3813-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="e3813-178">Předchůdci</span><span class="sxs-lookup"><span data-stu-id="e3813-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="e3813-179">Úsilí</span><span class="sxs-lookup"><span data-stu-id="e3813-179">Effort</span></span>  
  
    -   <span data-ttu-id="e3813-180">Počet zdrojů</span><span class="sxs-lookup"><span data-stu-id="e3813-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="e3813-181">Počáteční a koncová data</span><span class="sxs-lookup"><span data-stu-id="e3813-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="e3813-182">**Pravidla plánování**.</span><span class="sxs-lookup"><span data-stu-id="e3813-182">**Scheduling rules**.</span></span>   <span data-ttu-id="e3813-183">Počáteční datum úkolu uzlu typu list, který nemá předchůdce, bude nastaven na výchozí datum zahájení plánování projektu.</span><span class="sxs-lookup"><span data-stu-id="e3813-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="e3813-184">Doba trvání úkolu uzlu typu list se vždy počítá jako počet pracovních dnů mezi jeho počátečním a koncovým datem.</span><span class="sxs-lookup"><span data-stu-id="e3813-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="e3813-185">Když je úkol naplánován automaticky, plánovací modul postupujte podle následujících pravidel:</span><span class="sxs-lookup"><span data-stu-id="e3813-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="e3813-186">Datum zahájení a dokončení úkolu musí být vždy pracovní dny podle plánovacího kalendáře projektu</span><span class="sxs-lookup"><span data-stu-id="e3813-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="e3813-187">Datum zahájení úkolu, který má předchůdce, bude nastaveno na poslední koncové datum jeho předchůdců</span><span class="sxs-lookup"><span data-stu-id="e3813-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="e3813-188">Úsilí = počet osob \* doba trvání \* hodiny ve standardní pracovní den kalendáře projektu</span><span class="sxs-lookup"><span data-stu-id="e3813-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="e3813-189">**Ruční plánování**.</span><span class="sxs-lookup"><span data-stu-id="e3813-189">**Manual scheduling**.</span></span>   <span data-ttu-id="e3813-190">V některých případech se můžete chtít od těchto pravidel odchýlit.</span><span class="sxs-lookup"><span data-stu-id="e3813-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="e3813-191">V těchto případech můžete nastavit režim úkolu pro úkol na ruční plánování.</span><span class="sxs-lookup"><span data-stu-id="e3813-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="e3813-192">Tím zabráníte plánovacímu modulu ve výpočtu hodnot z jiných atributů plánování.</span><span class="sxs-lookup"><span data-stu-id="e3813-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="e3813-193">Nastavení předchůdců úkolů vždy ovlivňuje datum zahájení závislého úkolu.</span><span class="sxs-lookup"><span data-stu-id="e3813-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="e3813-194">Vytvoření strukturovaného rozpisu prací</span><span class="sxs-lookup"><span data-stu-id="e3813-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="e3813-195">Přejděte do nabídky **Project Service > Projekty**.</span><span class="sxs-lookup"><span data-stu-id="e3813-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="e3813-196">Klepněte na projekt, na kterém chcete pracovat.</span><span class="sxs-lookup"><span data-stu-id="e3813-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="e3813-197">Na panelu v horní části obrazovky vyberte šipku dolů vedle názvu projektu a potom klikněte na možnost Strukturovaný rozpis prací.</span><span class="sxs-lookup"><span data-stu-id="e3813-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="e3813-198">Chcete-li přidat úkol, klikněte na tlačítko **Přidat úkol**.</span><span class="sxs-lookup"><span data-stu-id="e3813-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="e3813-199">Vyplňte pole úkolu a klikněte na tlačítko **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e3813-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="e3813-200">Pokračujte v přidávání úkolů, dokud nebude strukturovaný rozpis prací dokončen.</span><span class="sxs-lookup"><span data-stu-id="e3813-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="e3813-201">Při vytváření strukturovaného rozpisu prací můžete provést následující, chcete-li uspořádat úkoly:</span><span class="sxs-lookup"><span data-stu-id="e3813-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="e3813-202">Vyberte úkol a klikněte na tlačítko **Zvětšit odsazení**, chcete-li jej posunout pod jiný úkol, nebo na tlačítko Zmenšit odsazení, chcete-li jej přesunout na vyšší úroveň.</span><span class="sxs-lookup"><span data-stu-id="e3813-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="e3813-203">Vyberte úkol a klikněte na tlačítko **Posunout nahoru** nebo **Posunout dolů** , chcete-li úkol přesunout nahoru nebo dolů v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e3813-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="e3813-204">Klikněte na tlačítko **Skrýt Ganttův diagram**, chcete-li skrýt Ganttům diagram, a na tlačítko **Zobrazit Ganttův diagram**, chcete-li jej znovu zobrazit.</span><span class="sxs-lookup"><span data-stu-id="e3813-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="e3813-205">Vyberte jinou dobu pro Ganttův diagram v poli **Časové měřítko**.</span><span class="sxs-lookup"><span data-stu-id="e3813-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="e3813-206">Chcete-li přidat role uvedené ve strukturovaném rozpisu prací ke členům týmu projektu, klikněte na tlačítko **Generovat projektový tým**.</span><span class="sxs-lookup"><span data-stu-id="e3813-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="e3813-207">Když jste s prováděním změn hotovi, klikněte na tlačítko **Uložit** v pravém dolním rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="e3813-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e3813-208">Viz také</span><span class="sxs-lookup"><span data-stu-id="e3813-208">See Also</span></span>  
 [<span data-ttu-id="e3813-209">Příručka pro projektového manažera</span><span class="sxs-lookup"><span data-stu-id="e3813-209">Project manager guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]