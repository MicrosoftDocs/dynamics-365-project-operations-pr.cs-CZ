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
ms.openlocfilehash: 5f88d7309a5e1171629a72e749bfc01abb64c62a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284755"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="274d7-103">Změny správy zdrojů (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="274d7-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="274d7-104">Části tohoto tématu poskytují informace o změnách, které byly provedeny v oblasti správy zdrojů Dynamics 365 Project Service Automation verze 3.x.</span><span class="sxs-lookup"><span data-stu-id="274d7-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="274d7-105">Odhady projektů</span><span class="sxs-lookup"><span data-stu-id="274d7-105">Project estimates</span></span>

<span data-ttu-id="274d7-106">Místo toho, aby byly odhady projektu založeny na entitě **msdyn\_** projecttask **(Projektový úkol)**, jsou založeny na entitě **msdyn\_resourceassignment** (**Přiřazení zdroje**).</span><span class="sxs-lookup"><span data-stu-id="274d7-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="274d7-107">Přiřazení zdrojů se stala „zdrojem pravdy” pro plánování úkolů a tvorbu cen.</span><span class="sxs-lookup"><span data-stu-id="274d7-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="274d7-108">Úkoly na řádku</span><span class="sxs-lookup"><span data-stu-id="274d7-108">Line tasks</span></span>

<span data-ttu-id="274d7-109">V PSA 3.x jsou úkoly na řádku zastaralé (vyřazené).</span><span class="sxs-lookup"><span data-stu-id="274d7-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="274d7-110">Přiřazení nyní odkazují na celý úkol, nikoli na úkoly na řádku.</span><span class="sxs-lookup"><span data-stu-id="274d7-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="274d7-111">Následující příklad ukazuje, jak je úkol nazvaný „testovací úkol” přidělen členům týmu A a B v dřívějších verzích PSA a v PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="274d7-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="274d7-112">**Před PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="274d7-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="274d7-113">Testovací úkol</span><span class="sxs-lookup"><span data-stu-id="274d7-113">Test task</span></span>

        - <span data-ttu-id="274d7-114">Testovací úkol – úkol na řádku 1</span><span class="sxs-lookup"><span data-stu-id="274d7-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="274d7-115">Přiřazení k A</span><span class="sxs-lookup"><span data-stu-id="274d7-115">Assignment to A</span></span>

        - <span data-ttu-id="274d7-116">Testovací úkol – úkol na řádku 2</span><span class="sxs-lookup"><span data-stu-id="274d7-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="274d7-117">Přiřazení k B</span><span class="sxs-lookup"><span data-stu-id="274d7-117">Assignment to B</span></span>

- <span data-ttu-id="274d7-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="274d7-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="274d7-119">Testovací úkol</span><span class="sxs-lookup"><span data-stu-id="274d7-119">Test task</span></span>

        - <span data-ttu-id="274d7-120">Přiřazení k A</span><span class="sxs-lookup"><span data-stu-id="274d7-120">Assignment to A</span></span>
        - <span data-ttu-id="274d7-121">Přiřazení k B</span><span class="sxs-lookup"><span data-stu-id="274d7-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="274d7-122">Nepřiřazené přiřazení</span><span class="sxs-lookup"><span data-stu-id="274d7-122">Unassigned assignment</span></span>

<span data-ttu-id="274d7-123">V PSA 3.x je nepřiřazené přiřazení přiřazení, které je přiřazeno členu týmu **NULL** a prostředku **NULL** .</span><span class="sxs-lookup"><span data-stu-id="274d7-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="274d7-124">Nepřiřazená přiřazení se mohou vyskytnout v několika scénářích:</span><span class="sxs-lookup"><span data-stu-id="274d7-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="274d7-125">Pokud byl úkol vytvořen, ale dosud nebyl přiřazen žádné členovi týmu, je vždy vytvořeno nepřiřazené přiřazení.</span><span class="sxs-lookup"><span data-stu-id="274d7-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="274d7-126">Pokud jsou všechny přiřazené osoby v úkolu odebrány, bude pro tento úkol znovu vytvořeno nepřiřazené přiřazení.</span><span class="sxs-lookup"><span data-stu-id="274d7-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="274d7-127">Pole plánování entity Projektový úkol</span><span class="sxs-lookup"><span data-stu-id="274d7-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="274d7-128">Pole v entitě **\_msdyn projecttask** byla vyřazena nebo přesunuta do entity **msdyn\_resourceassignment** nebo je na ně nyní odkazováno z entity **msdyn\_projectteam** (**Člen projektového týmu**).</span><span class="sxs-lookup"><span data-stu-id="274d7-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="274d7-129">Vyřazené pole v msdyn\_projecttask (Projektový úkol)</span><span class="sxs-lookup"><span data-stu-id="274d7-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="274d7-130">Nové pole v msdyn\_resourceassignment (Přiřazení zdroje)</span><span class="sxs-lookup"><span data-stu-id="274d7-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="274d7-131">Komentář</span><span class="sxs-lookup"><span data-stu-id="274d7-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="274d7-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="274d7-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="274d7-133">Žádný</span><span class="sxs-lookup"><span data-stu-id="274d7-133">None</span></span> | |
| <span data-ttu-id="274d7-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="274d7-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="274d7-135">Žádný</span><span class="sxs-lookup"><span data-stu-id="274d7-135">None</span></span> | |
| <span data-ttu-id="274d7-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="274d7-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="274d7-137">Žádný</span><span class="sxs-lookup"><span data-stu-id="274d7-137">None</span></span> | |
| <span data-ttu-id="274d7-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="274d7-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="274d7-139">Žádný</span><span class="sxs-lookup"><span data-stu-id="274d7-139">None</span></span> | |
| <span data-ttu-id="274d7-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="274d7-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="274d7-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="274d7-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="274d7-142">Formát datové struktury JavaScript Object Notation (JSON), který je uložen v poli, byl změněn.</span><span class="sxs-lookup"><span data-stu-id="274d7-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="274d7-143">Průběhová křivka plánu</span><span class="sxs-lookup"><span data-stu-id="274d7-143">Schedule contour</span></span>

<span data-ttu-id="274d7-144">Průběhová křivka plánu je uložena v poli **Naplánovaná práce** (**msdyn\_plannedwork**) jednotlivých entit **Přiřazení zdroje** (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="274d7-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="274d7-145">Struktura</span><span class="sxs-lookup"><span data-stu-id="274d7-145">Structure</span></span>

<span data-ttu-id="274d7-146">Nová struktura průběhové křivky plánu se skládá z pružných časových úseků, které jsou definovány pro každý den plánu.</span><span class="sxs-lookup"><span data-stu-id="274d7-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="274d7-147">Každý časový úsek má následující vlastnosti:</span><span class="sxs-lookup"><span data-stu-id="274d7-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="274d7-148">**Začátek** – začátek pracovní doby pro daný den podle kalendáře projektu.</span><span class="sxs-lookup"><span data-stu-id="274d7-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="274d7-149">**Konec** – konec pracovní doby pro daný den podle kalendáře projektu.</span><span class="sxs-lookup"><span data-stu-id="274d7-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="274d7-150">**Hodiny** – počet hodin přiřazených k danému dnu.</span><span class="sxs-lookup"><span data-stu-id="274d7-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="274d7-151">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="274d7-151">**Example**</span></span>

<span data-ttu-id="274d7-152">V tomto příkladu je použit kalendář projektu, kde pracovní den je od 9:00 do 17:00 v časovém pásmu UTC-8.</span><span class="sxs-lookup"><span data-stu-id="274d7-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="274d7-153">Automatické plánování a ruční plánování</span><span class="sxs-lookup"><span data-stu-id="274d7-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="274d7-154">Pokud je úkol automaticky naplánován, jsou hodiny předem načteny a doba trvání úkolu může být snížena.</span><span class="sxs-lookup"><span data-stu-id="274d7-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="274d7-155">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="274d7-155">**Example**</span></span>

<span data-ttu-id="274d7-156">Následující úkol je automaticky naplánován na 18 hodin během tří dnů (od 3. prosince 2018 do 5. prosince 2018).</span><span class="sxs-lookup"><span data-stu-id="274d7-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="274d7-157">Pokud je úkol naplánován ručně, jsou hodiny rovnoměrně rozděleny do všech dat.</span><span class="sxs-lookup"><span data-stu-id="274d7-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="274d7-158">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="274d7-158">**Example**</span></span>

<span data-ttu-id="274d7-159">Následující úkol je ručně naplánován na 18 hodin během tří dnů (od 3. prosince 2018 do 5. prosince 2018).</span><span class="sxs-lookup"><span data-stu-id="274d7-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="274d7-160">Jednotka přiřazení</span><span class="sxs-lookup"><span data-stu-id="274d7-160">Assignment unit</span></span>

<span data-ttu-id="274d7-161">Jednotka přiřazení byla v PSA 3.x vyřazena.</span><span class="sxs-lookup"><span data-stu-id="274d7-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="274d7-162">Hodiny úsilí úkolu jsou nyní rovnoměrně rozděleny na každý den, mezi všechny přiřazené zdroje.</span><span class="sxs-lookup"><span data-stu-id="274d7-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="274d7-163">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="274d7-163">**Example**</span></span>

<span data-ttu-id="274d7-164">V tomto příkladu je úkol přiřazen dvěma zdrojům a je automaticky naplánován na 36 hodin během tří dnů (od 3. prosince 2018 do 5. prosince 2018).</span><span class="sxs-lookup"><span data-stu-id="274d7-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="274d7-165">Přiřazení 1:</span><span class="sxs-lookup"><span data-stu-id="274d7-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="274d7-166">Přiřazení 2:</span><span class="sxs-lookup"><span data-stu-id="274d7-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="274d7-167">Cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="274d7-167">Pricing dimensions</span></span>

<span data-ttu-id="274d7-168">V PSA 3.x byla z entity **msdyn\_projecttask** odebrána pole cenových dimenzí specifická pro konkrétní zdroj (jako např. **Role** a **Organizační jednotka**).</span><span class="sxs-lookup"><span data-stu-id="274d7-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="274d7-169">Tato pole lze nyní načíst z odpovídajícího člena projektového týmu (**msdyn\_projectteam**) přiřazení zdroje (**msdyn\_resourceassignment**) při generování odhadů projektu.</span><span class="sxs-lookup"><span data-stu-id="274d7-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="274d7-170">Nové pole **msdyn\_organizationalunit** bylo přidáno do entity **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="274d7-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="274d7-171">Vyřazené pole v msdyn\_projecttask (Projektový úkol)</span><span class="sxs-lookup"><span data-stu-id="274d7-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="274d7-172">Pole z modulu msdyn\_projectteam (Člen projektového týmu), které je použito místo</span><span class="sxs-lookup"><span data-stu-id="274d7-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="274d7-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="274d7-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="274d7-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="274d7-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="274d7-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="274d7-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="274d7-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="274d7-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="274d7-177">Průběhové křivky</span><span class="sxs-lookup"><span data-stu-id="274d7-177">Contours</span></span>

<span data-ttu-id="274d7-178">Pole průběhové křivky ocenění a odhadu byla v entitě **msdyn\_projecttask** vyřazena.</span><span class="sxs-lookup"><span data-stu-id="274d7-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="274d7-179">Byla přesunuta do entity **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="274d7-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="274d7-180">Vyřazené pole v msdyn\_projecttask (Projektový úkol)</span><span class="sxs-lookup"><span data-stu-id="274d7-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="274d7-181">Nové pole v msdyn\_resourceassignment (Přiřazení zdroje)</span><span class="sxs-lookup"><span data-stu-id="274d7-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="274d7-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="274d7-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="274d7-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="274d7-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="274d7-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="274d7-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="274d7-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="274d7-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="274d7-186">Do entity **msdyn\_resourceassignment** byla přidána následující pole.</span><span class="sxs-lookup"><span data-stu-id="274d7-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="274d7-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="274d7-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="274d7-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="274d7-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="274d7-189">Následující pole pro plánované, skutečné a zbývající náklady a prodej zůstávají v entitě **msdyn\_projecttask** beze změny:</span><span class="sxs-lookup"><span data-stu-id="274d7-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="274d7-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="274d7-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="274d7-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="274d7-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="274d7-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="274d7-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="274d7-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="274d7-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="274d7-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="274d7-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="274d7-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="274d7-195">msdyn\_remainingsales</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]