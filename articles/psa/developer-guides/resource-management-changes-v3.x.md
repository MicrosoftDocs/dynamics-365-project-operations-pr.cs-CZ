---
title: Změny správy zdrojů (Project Service Automation 3.x)
description: Toto téma poskytuje informace o změnách v oblasti správy zdrojů.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5176d2c6b7b00d47d4aeb12f54bdb84d4b87304c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073971"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="71fee-103">Změny správy zdrojů (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="71fee-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="71fee-104">Části tohoto tématu poskytují informace o změnách, které byly provedeny v oblasti správy zdrojů Dynamics 365 Project Service Automation verze 3.x.</span><span class="sxs-lookup"><span data-stu-id="71fee-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="71fee-105">Odhady projektů</span><span class="sxs-lookup"><span data-stu-id="71fee-105">Project estimates</span></span>

<span data-ttu-id="71fee-106">Místo toho, aby byly odhady projektu založeny na entitě **msdyn\_** projecttask **(Projektový úkol)** , jsou založeny na entitě **msdyn\_resourceassignment** ( **Přiřazení zdroje** ).</span><span class="sxs-lookup"><span data-stu-id="71fee-106">Instead of being based on the **msdyn\_projecttask** entity ( **Project Task** ), project estimates are based on the **msdyn\_resourceassignment** entity ( **Resource Assignment** ).</span></span> <span data-ttu-id="71fee-107">Přiřazení zdrojů se stala „zdrojem pravdy” pro plánování úkolů a tvorbu cen.</span><span class="sxs-lookup"><span data-stu-id="71fee-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="71fee-108">Úkoly na řádku</span><span class="sxs-lookup"><span data-stu-id="71fee-108">Line tasks</span></span>

<span data-ttu-id="71fee-109">V PSA 3.x jsou úkoly na řádku zastaralé (vyřazené).</span><span class="sxs-lookup"><span data-stu-id="71fee-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="71fee-110">Přiřazení nyní odkazují na celý úkol, nikoli na úkoly na řádku.</span><span class="sxs-lookup"><span data-stu-id="71fee-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="71fee-111">Následující příklad ukazuje, jak je úkol nazvaný „testovací úkol” přidělen členům týmu A a B v dřívějších verzích PSA a v PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="71fee-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="71fee-112">**Před PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="71fee-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="71fee-113">Testovací úkol</span><span class="sxs-lookup"><span data-stu-id="71fee-113">Test task</span></span>

        - <span data-ttu-id="71fee-114">Testovací úkol – úkol na řádku 1</span><span class="sxs-lookup"><span data-stu-id="71fee-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="71fee-115">Přiřazení k A</span><span class="sxs-lookup"><span data-stu-id="71fee-115">Assignment to A</span></span>

        - <span data-ttu-id="71fee-116">Testovací úkol – úkol na řádku 2</span><span class="sxs-lookup"><span data-stu-id="71fee-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="71fee-117">Přiřazení k B</span><span class="sxs-lookup"><span data-stu-id="71fee-117">Assignment to B</span></span>

- <span data-ttu-id="71fee-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="71fee-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="71fee-119">Testovací úkol</span><span class="sxs-lookup"><span data-stu-id="71fee-119">Test task</span></span>

        - <span data-ttu-id="71fee-120">Přiřazení k A</span><span class="sxs-lookup"><span data-stu-id="71fee-120">Assignment to A</span></span>
        - <span data-ttu-id="71fee-121">Přiřazení k B</span><span class="sxs-lookup"><span data-stu-id="71fee-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="71fee-122">Nepřiřazené přiřazení</span><span class="sxs-lookup"><span data-stu-id="71fee-122">Unassigned assignment</span></span>

<span data-ttu-id="71fee-123">V PSA 3.x je nepřiřazené přiřazení přiřazení, které je přiřazeno členu týmu **NULL** a prostředku **NULL** .</span><span class="sxs-lookup"><span data-stu-id="71fee-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="71fee-124">Nepřiřazená přiřazení se mohou vyskytnout v několika scénářích:</span><span class="sxs-lookup"><span data-stu-id="71fee-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="71fee-125">Pokud byl úkol vytvořen, ale dosud nebyl přiřazen žádné členovi týmu, je vždy vytvořeno nepřiřazené přiřazení.</span><span class="sxs-lookup"><span data-stu-id="71fee-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="71fee-126">Pokud jsou všechny přiřazené osoby v úkolu odebrány, bude pro tento úkol znovu vytvořeno nepřiřazené přiřazení.</span><span class="sxs-lookup"><span data-stu-id="71fee-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="71fee-127">Pole plánování entity Projektový úkol</span><span class="sxs-lookup"><span data-stu-id="71fee-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="71fee-128">Pole v entitě **\_msdyn projecttask** byla vyřazena nebo přesunuta do entity **msdyn\_resourceassignment** nebo je na ně nyní odkazováno z entity **msdyn\_projectteam** ( **Člen projektového týmu** ).</span><span class="sxs-lookup"><span data-stu-id="71fee-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity ( **Project Team Member** ).</span></span>

| <span data-ttu-id="71fee-129">Vyřazené pole v msdyn\_projecttask (Projektový úkol)</span><span class="sxs-lookup"><span data-stu-id="71fee-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="71fee-130">Nové pole v msdyn\_resourceassignment (Přiřazení zdroje)</span><span class="sxs-lookup"><span data-stu-id="71fee-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="71fee-131">Komentář</span><span class="sxs-lookup"><span data-stu-id="71fee-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="71fee-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="71fee-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="71fee-133">Žádný</span><span class="sxs-lookup"><span data-stu-id="71fee-133">None</span></span> | |
| <span data-ttu-id="71fee-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="71fee-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="71fee-135">Žádný</span><span class="sxs-lookup"><span data-stu-id="71fee-135">None</span></span> | |
| <span data-ttu-id="71fee-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="71fee-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="71fee-137">Žádný</span><span class="sxs-lookup"><span data-stu-id="71fee-137">None</span></span> | |
| <span data-ttu-id="71fee-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="71fee-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="71fee-139">Žádný</span><span class="sxs-lookup"><span data-stu-id="71fee-139">None</span></span> | |
| <span data-ttu-id="71fee-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="71fee-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="71fee-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="71fee-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="71fee-142">Formát datové struktury JavaScript Object Notation (JSON), který je uložen v poli, byl změněn.</span><span class="sxs-lookup"><span data-stu-id="71fee-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="71fee-143">Průběhová křivka plánu</span><span class="sxs-lookup"><span data-stu-id="71fee-143">Schedule contour</span></span>

<span data-ttu-id="71fee-144">Průběhová křivka plánu je uložena v poli **Naplánovaná práce** ( **msdyn\_plannedwork** ) jednotlivých entit **Přiřazení zdroje** ( **msdyn\_resourceassignment** ).</span><span class="sxs-lookup"><span data-stu-id="71fee-144">The schedule contour is stored in the **Planned Work** field ( **msdyn\_plannedwork** ) of each **Resource Assignment** entity ( **msdyn\_resourceassignment** ).</span></span>

### <a name="structure"></a><span data-ttu-id="71fee-145">Struktura</span><span class="sxs-lookup"><span data-stu-id="71fee-145">Structure</span></span>

<span data-ttu-id="71fee-146">Nová struktura průběhové křivky plánu se skládá z pružných časových úseků, které jsou definovány pro každý den plánu.</span><span class="sxs-lookup"><span data-stu-id="71fee-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="71fee-147">Každý časový úsek má následující vlastnosti:</span><span class="sxs-lookup"><span data-stu-id="71fee-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="71fee-148">**Začátek** – začátek pracovní doby pro daný den podle kalendáře projektu.</span><span class="sxs-lookup"><span data-stu-id="71fee-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="71fee-149">**Konec** – konec pracovní doby pro daný den podle kalendáře projektu.</span><span class="sxs-lookup"><span data-stu-id="71fee-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="71fee-150">**Hodiny** – počet hodin přiřazených k danému dnu.</span><span class="sxs-lookup"><span data-stu-id="71fee-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="71fee-151">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="71fee-151">**Example**</span></span>

<span data-ttu-id="71fee-152">V tomto příkladu je použit kalendář projektu, kde pracovní den je od 9:00 do 17:00 v časovém pásmu UTC-8.</span><span class="sxs-lookup"><span data-stu-id="71fee-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="71fee-153">Automatické plánování a ruční plánování</span><span class="sxs-lookup"><span data-stu-id="71fee-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="71fee-154">Pokud je úkol automaticky naplánován, jsou hodiny předem načteny a doba trvání úkolu může být snížena.</span><span class="sxs-lookup"><span data-stu-id="71fee-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="71fee-155">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="71fee-155">**Example**</span></span>

<span data-ttu-id="71fee-156">Následující úkol je automaticky naplánován na 18 hodin během tří dnů (od 3. prosince 2018 do 5. prosince 2018).</span><span class="sxs-lookup"><span data-stu-id="71fee-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="71fee-157">Pokud je úkol naplánován ručně, jsou hodiny rovnoměrně rozděleny do všech dat.</span><span class="sxs-lookup"><span data-stu-id="71fee-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="71fee-158">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="71fee-158">**Example**</span></span>

<span data-ttu-id="71fee-159">Následující úkol je ručně naplánován na 18 hodin během tří dnů (od 3. prosince 2018 do 5. prosince 2018).</span><span class="sxs-lookup"><span data-stu-id="71fee-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="71fee-160">Jednotka přiřazení</span><span class="sxs-lookup"><span data-stu-id="71fee-160">Assignment unit</span></span>

<span data-ttu-id="71fee-161">Jednotka přiřazení byla v PSA 3.x vyřazena.</span><span class="sxs-lookup"><span data-stu-id="71fee-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="71fee-162">Hodiny úsilí úkolu jsou nyní rovnoměrně rozděleny na každý den, mezi všechny přiřazené zdroje.</span><span class="sxs-lookup"><span data-stu-id="71fee-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="71fee-163">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="71fee-163">**Example**</span></span>

<span data-ttu-id="71fee-164">V tomto příkladu je úkol přiřazen dvěma zdrojům a je automaticky naplánován na 36 hodin během tří dnů (od 3. prosince 2018 do 5. prosince 2018).</span><span class="sxs-lookup"><span data-stu-id="71fee-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="71fee-165">Přiřazení 1:</span><span class="sxs-lookup"><span data-stu-id="71fee-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="71fee-166">Přiřazení 2:</span><span class="sxs-lookup"><span data-stu-id="71fee-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="71fee-167">Cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="71fee-167">Pricing dimensions</span></span>

<span data-ttu-id="71fee-168">V PSA 3.x byla z entity **msdyn\_projecttask** odebrána pole cenových dimenzí specifická pro konkrétní zdroj (jako např. **Role** a **Organizační jednotka** ).</span><span class="sxs-lookup"><span data-stu-id="71fee-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit** ) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="71fee-169">Tato pole lze nyní načíst z odpovídajícího člena projektového týmu ( **msdyn\_projectteam** ) přiřazení zdroje ( **msdyn\_resourceassignment** ) při generování odhadů projektu.</span><span class="sxs-lookup"><span data-stu-id="71fee-169">These fields can now be retrieved from the corresponding project team member ( **msdyn\_projectteam** ) of the resource assignment ( **msdyn\_resourceassignment** ) when project estimates are generated.</span></span> <span data-ttu-id="71fee-170">Nové pole **msdyn\_organizationalunit** bylo přidáno do entity **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="71fee-170">A new field, **msdyn\_organizationalunit** , has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="71fee-171">Vyřazené pole v msdyn\_projecttask (Projektový úkol)</span><span class="sxs-lookup"><span data-stu-id="71fee-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="71fee-172">Pole z modulu msdyn\_projectteam (Člen projektového týmu), které je použito místo</span><span class="sxs-lookup"><span data-stu-id="71fee-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="71fee-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="71fee-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="71fee-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="71fee-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="71fee-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="71fee-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="71fee-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="71fee-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="71fee-177">Průběhové křivky</span><span class="sxs-lookup"><span data-stu-id="71fee-177">Contours</span></span>

<span data-ttu-id="71fee-178">Pole průběhové křivky ocenění a odhadu byla v entitě **msdyn\_projecttask** vyřazena.</span><span class="sxs-lookup"><span data-stu-id="71fee-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="71fee-179">Byla přesunuta do entity **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="71fee-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="71fee-180">Vyřazené pole v msdyn\_projecttask (Projektový úkol)</span><span class="sxs-lookup"><span data-stu-id="71fee-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="71fee-181">Nové pole v msdyn\_resourceassignment (Přiřazení zdroje)</span><span class="sxs-lookup"><span data-stu-id="71fee-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="71fee-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="71fee-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="71fee-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="71fee-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="71fee-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="71fee-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="71fee-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="71fee-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="71fee-186">Do entity **msdyn\_resourceassignment** byla přidána následující pole.</span><span class="sxs-lookup"><span data-stu-id="71fee-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="71fee-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="71fee-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="71fee-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="71fee-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="71fee-189">Následující pole pro plánované, skutečné a zbývající náklady a prodej zůstávají v entitě **msdyn\_projecttask** beze změny:</span><span class="sxs-lookup"><span data-stu-id="71fee-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="71fee-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="71fee-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="71fee-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="71fee-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="71fee-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="71fee-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="71fee-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="71fee-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="71fee-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="71fee-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="71fee-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="71fee-195">msdyn\_remainingsales</span></span>
