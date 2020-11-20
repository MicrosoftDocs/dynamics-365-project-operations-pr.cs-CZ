---
title: Šablony projektů
description: Toto téma poskytuje informace o tom, jak používat šablony projektů pro rychlé nastavení projektu.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 4fd618e15524c5cef5b6da9b282f449e3dfb7973
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123002"
---
# <a name="project-templates"></a><span data-ttu-id="03865-103">Šablony projektů</span><span class="sxs-lookup"><span data-stu-id="03865-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="03865-104">Šablona projektu je předdefinovaná struktura, která pomáhá rychle a snadno spustit projekt.</span><span class="sxs-lookup"><span data-stu-id="03865-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="03865-105">Pomocí předdefinované šablony můžete vytvořit nový projekt jediným klepnutím.</span><span class="sxs-lookup"><span data-stu-id="03865-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="03865-106">Pro šablony projektů musíte, stejně jako pro projekty, definovat předpoklady.</span><span class="sxs-lookup"><span data-stu-id="03865-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="03865-107">Pro každou šablonu projektu musíte definovat kalendář projektu a role a ceníky musí být v organizaci předdefinované, aby komponenty šablony obsahovaly užitečná data.</span><span class="sxs-lookup"><span data-stu-id="03865-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="03865-108">Šablona projektu sestává ze tří komponent: plánu, odhadů projektu a členů projektového týmu.</span><span class="sxs-lookup"><span data-stu-id="03865-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="03865-109">Naplánovat</span><span class="sxs-lookup"><span data-stu-id="03865-109">Schedule</span></span>

<span data-ttu-id="03865-110">Plán v šabloně projektu obsahuje stejnou sadu prvků jako plán v projektu.</span><span class="sxs-lookup"><span data-stu-id="03865-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="03865-111">Můžete vytvořit hierarchii úkolů, přiřadit role k úkolům, definovat atributy plánu a nastavit závislosti.</span><span class="sxs-lookup"><span data-stu-id="03865-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="03865-112">Plán v šabloně projektu podporuje pro jednotlivé úkoly také režimy úkolů.</span><span class="sxs-lookup"><span data-stu-id="03865-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="03865-113">Proto tedy podporuje plánovací modul.</span><span class="sxs-lookup"><span data-stu-id="03865-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="03865-114">K projektu je nutné přidružit projektový kalendář.</span><span class="sxs-lookup"><span data-stu-id="03865-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="03865-115">Při vytváření pracovního plánu není mezi šablonou projektu a projektem žádný rozdíl.</span><span class="sxs-lookup"><span data-stu-id="03865-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="03865-116">Odhady projekt</span><span class="sxs-lookup"><span data-stu-id="03865-116">Project estimates</span></span>

<span data-ttu-id="03865-117">Odhady projektu v šabloně projektu fungují stejným způsobem jako odhady projektu v projektu.</span><span class="sxs-lookup"><span data-stu-id="03865-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="03865-118">Nákladové a prodejní ceny jsou však vyžádány z výchozích nákladových a prodejních ceníků, které jsou definovány v parametrech.</span><span class="sxs-lookup"><span data-stu-id="03865-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="03865-119">Vytvoření projektu ze šablony</span><span class="sxs-lookup"><span data-stu-id="03865-119">Creating a project from a template</span></span>
 
<span data-ttu-id="03865-120">Existuje několik způsobů, jak vytvořit projekt ze šablony projektu:</span><span class="sxs-lookup"><span data-stu-id="03865-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="03865-121">Při vytváření projektu z nabídky můžete vybrat šablonu projektu v dialogovém okně **Vytvořit: Projekt**.</span><span class="sxs-lookup"><span data-stu-id="03865-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Dialogové okno Vytvořit: Projekt](media/project-11.png)

- <span data-ttu-id="03865-123">Při vytváření projektu výběrem **Nový projekt** se před uložením záznamu zobrazí stránka **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="03865-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="03865-124">V poli **Vybrat šablonu** vyberte jednu z předdefinovaných šablon projektů v organizaci.</span><span class="sxs-lookup"><span data-stu-id="03865-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="03865-125">Použijte **Vytvořit projekt ze šablony** na stránce **Entita šablona**.</span><span class="sxs-lookup"><span data-stu-id="03865-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="03865-126">Kopírování komponent šablony do projektu</span><span class="sxs-lookup"><span data-stu-id="03865-126">Copying components of template to project</span></span>

<span data-ttu-id="03865-127">Při kopírování komponent šablony projektu do projektu může dojít k několika přepsáním v závislosti na nastavení v projektu.</span><span class="sxs-lookup"><span data-stu-id="03865-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="03865-128">Kopírování plánu</span><span class="sxs-lookup"><span data-stu-id="03865-128">Copying the schedule</span></span>

<span data-ttu-id="03865-129">Pokud má projekt při kopírování plánu ze šablony projektu jiný kalendář projektu než šablona, bude v plánu úkolů použita pracovní doba z kalendáře projektu.</span><span class="sxs-lookup"><span data-stu-id="03865-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="03865-130">Tímto způsobem se plán upraví, aby odpovídal pomocnému kalendáři projektu.</span><span class="sxs-lookup"><span data-stu-id="03865-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="03865-131">A podobně první úkol v plánu bude mít datum zahájení projektu a plán zbytku hierarchie bude aktualizován na základě doby trvání a závislostí, které jsou uvedeny v šabloně.</span><span class="sxs-lookup"><span data-stu-id="03865-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="03865-132">Kopírování odhadů projektu</span><span class="sxs-lookup"><span data-stu-id="03865-132">Copying project estimates</span></span> 

<span data-ttu-id="03865-133">Při kopírování mezi řádky odhadů projektu jsou ceníky aktualizovány.</span><span class="sxs-lookup"><span data-stu-id="03865-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="03865-134">U nákladového ceníku jsou tyto aktualizace založeny na vlastnící jednotce projektu.</span><span class="sxs-lookup"><span data-stu-id="03865-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="03865-135">U prodejního ceníku jsou založeny na zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="03865-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="03865-136">U projektů, které jsou přidruženy k entitě prodeje, jsou nákladové a prodejní ceny na jednotku stanoveny na základě těchto ceníků.</span><span class="sxs-lookup"><span data-stu-id="03865-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="03865-137">Kopírování projektového týmu</span><span class="sxs-lookup"><span data-stu-id="03865-137">Copying a project team</span></span>

<span data-ttu-id="03865-138">Při kopírování projektového týmu ze šablony projektu do projektu jsou obecné zdroje zkopírovány spolu s dovednostmi a odbornými znalostmi, které jsou definovány v šabloně.</span><span class="sxs-lookup"><span data-stu-id="03865-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="03865-139">Přiřazení obecných zdrojů jsou rovněž zachována tak, jako byla v šabloně projektu.</span><span class="sxs-lookup"><span data-stu-id="03865-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="03865-140">V šablonách projektů nejsou podporovány pojmenované zdroje.</span><span class="sxs-lookup"><span data-stu-id="03865-140">Named resources aren't supported in project templates.</span></span>
