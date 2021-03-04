---
title: Odhad tržeb a nákladů projektu, když rezervovatelný zdroj plní více rolí v projektu
description: Tento téma obsahuje informace, jak používat cenové dimenze k podpoře vytváření cen a nákladů pro zdroj, který v projektu plní více rolí.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 67e24156e960b9b09cf92f7f0cd77f6c74a982b8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145035"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="bb318-103">Odhad tržeb a nákladů projektu, když rezervovatelný zdroj plní více rolí v projektu</span><span class="sxs-lookup"><span data-stu-id="bb318-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bb318-104">Projektové společnosti často potřebují, aby jeden zdroj prováděl více rolí v projektu.</span><span class="sxs-lookup"><span data-stu-id="bb318-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="bb318-105">Každá z těchto rolí by mohla jinou cenu a náklady, což znamená, že čas stejného zdroje na projektu by mohl získat jiný finanční odhad v závislosti na sazbách fakturace a nákladových sazbách pro každou z rolí.</span><span class="sxs-lookup"><span data-stu-id="bb318-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="bb318-106">Project Service Automation umožňuje nastavení hodnot v záznamu člena týmu pro pojmenovaný zdroj a umožňuje různé přepsání každého z úkolů, ke kterým je člen týmu přiřazen.</span><span class="sxs-lookup"><span data-stu-id="bb318-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="bb318-107">Následující příklad vysvětluje, jak jednoduché přepsání této hodnoty umožňuje, aby měl prostředek v projektu více rolí s různými sazbami fakturace a nákladovými sazbami.</span><span class="sxs-lookup"><span data-stu-id="bb318-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="bb318-108">Vytvoření úkolů</span><span class="sxs-lookup"><span data-stu-id="bb318-108">Create tasks</span></span>
<span data-ttu-id="bb318-109">Vytvořte dva projektové úkoly na 40 hodin, úkol A a úkol B. Vyberte úkol A jako předchůdce úlohy B.</span><span class="sxs-lookup"><span data-stu-id="bb318-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="bb318-110">Nastavte roli a organizační jednotku pro člena obecného projektového týmu</span><span class="sxs-lookup"><span data-stu-id="bb318-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="bb318-111">Na stránce **Plán** vyberte řádek **Úkol** pro úkol A.</span><span class="sxs-lookup"><span data-stu-id="bb318-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="bb318-112">V poli **Zdroje** vyberte **Vytvořit** v rozevíracím seznamu.</span><span class="sxs-lookup"><span data-stu-id="bb318-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="bb318-113">Na stránce **Rychlé vytvoření člena týmu** zadejte atributy obecného člena týmu, který může tento úkol provádět.</span><span class="sxs-lookup"><span data-stu-id="bb318-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="bb318-114">Vyberte příslušnou roli a organizační jednotku a poté vyberte **Uložit a zavřít**.</span><span class="sxs-lookup"><span data-stu-id="bb318-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="bb318-115">Je vytvořen obecný člen týmu a přiřazen k tomuto úkolu.</span><span class="sxs-lookup"><span data-stu-id="bb318-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="bb318-116">Opakujte tyto kroky pro úkol B a ujistěte se, že role a organizační jednotka člena obecného týmu vytvořeného pro úkol B se liší od úlohy A.</span><span class="sxs-lookup"><span data-stu-id="bb318-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="bb318-117">Nastavte roli a organizační jednotku pro projektový úkol</span><span class="sxs-lookup"><span data-stu-id="bb318-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="bb318-118">Po vytvoření úlohy A vyberte úkol a poté vyberte **Upravit úkol**.</span><span class="sxs-lookup"><span data-stu-id="bb318-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="bb318-119">Na stránce **Podrobnosti úkolu** najděte pole **Role** a **Organizační jednotka**, přidejte hodnoty požadované u zdroje, který by tuto úlohu provedl.</span><span class="sxs-lookup"><span data-stu-id="bb318-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="bb318-120">Pokud dokončujete tyto scénáře pomocí ukázkových dat Project Service Automation, vyberte **Poradenský vedoucí** jako roli a **Fabrikam USA** jako organizační jednotku.</span><span class="sxs-lookup"><span data-stu-id="bb318-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="bb318-121">Vyberte úkol B a potom vyberte položku **Upravit úkol**.</span><span class="sxs-lookup"><span data-stu-id="bb318-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="bb318-122">Na stránce **Podrobnosti úkolu** najděte pole **Role** a **Organizační jednotka**, přidejte hodnoty požadované u zdroje, který by tuto úlohu provedl.</span><span class="sxs-lookup"><span data-stu-id="bb318-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="bb318-123">Ujistěte se, že hodnoty v polích **Role** a **Organizační jednotka** se liší pro úkol B od hodnot pro úkol A.</span><span class="sxs-lookup"><span data-stu-id="bb318-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="bb318-124">Pokud dokončujete tyto scénáře pomocí ukázkových dat Project Service Automation, vyberte **Síťový technik** jako roli a **Fabrikam USA** jako organizační jednotku.</span><span class="sxs-lookup"><span data-stu-id="bb318-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="bb318-125">Uložte a zavřete stránku **Podrobnosti úkolu**.</span><span class="sxs-lookup"><span data-stu-id="bb318-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="bb318-126">Člen týmu a odhady chování</span><span class="sxs-lookup"><span data-stu-id="bb318-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="bb318-127">Na stránce **Podrobnosti úkolu** u **Člena týmu** vyberte dva obecné členy týmu a poté vyberte **Generovat požadavky**.</span><span class="sxs-lookup"><span data-stu-id="bb318-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="bb318-128">Vyberte řádek člena týmu pro **Poradenský vedoucí** a poté vyberte **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="bb318-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="bb318-129">Otevře se plánovací vývěska a rezervuje zdroj k tomuto požadavku.</span><span class="sxs-lookup"><span data-stu-id="bb318-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="bb318-130">Vyberte řádek člena týmu pro **Síťového technika** a poté vyberte **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="bb318-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="bb318-131">Otevře se plánovací vývěska a rezervuje stejný zdroj k tomuto požadavku.</span><span class="sxs-lookup"><span data-stu-id="bb318-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="bb318-132">Mřížka členů týmu</span><span class="sxs-lookup"><span data-stu-id="bb318-132">Team Member grid</span></span> 
<span data-ttu-id="bb318-133">V mřížce **Člen týmu** si všimněte, že dva obecné záznamy členů týmu jsou odstraněny a byly nahrazeny jedním prostředkem.</span><span class="sxs-lookup"><span data-stu-id="bb318-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="bb318-134">Pro tento zdroj existuje jedna sada hodnot, která zobrazuje výchozí sadu hodnot pro **Roli** a **Organizační jednotku**.</span><span class="sxs-lookup"><span data-stu-id="bb318-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="bb318-135">Když rozbalíte řádek daného záznamu člena týmu, uvidíte v záznamu člena týmu odlišná přiřazení pro obě tyto úlohy.</span><span class="sxs-lookup"><span data-stu-id="bb318-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="bb318-136">Každý řádek přiřazení má specifické hodnoty úkolu pro **Roli** a **Organizační jednotku**.</span><span class="sxs-lookup"><span data-stu-id="bb318-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="bb318-137">Mřížka odhadů</span><span class="sxs-lookup"><span data-stu-id="bb318-137">Estimates grid</span></span> 
<span data-ttu-id="bb318-138">Když přejdete na mřížku **Odhady**, všimnete si, že obě přiřazení stejného zdroje jsou oceněny odlišně.</span><span class="sxs-lookup"><span data-stu-id="bb318-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="bb318-139">Cena za přiřazení zdroje na úkolu A je stanovena pomocí hodnoty atributu **Role** položky **Poradenský vedoucí**.</span><span class="sxs-lookup"><span data-stu-id="bb318-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="bb318-140">Cena za přiřazení stejného zdroje na úkolu B je stanovena pomocí hodnoty atributu **Role** položky **Síťový technik**.</span><span class="sxs-lookup"><span data-stu-id="bb318-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>

