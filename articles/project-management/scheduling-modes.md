---
title: Režimy plánování
description: Toto téma poskytuje informace o režimech plánování.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981427"
---
# <a name="scheduling-modes"></a><span data-ttu-id="6760f-103">Režimy plánování</span><span class="sxs-lookup"><span data-stu-id="6760f-103">Scheduling modes</span></span>

<span data-ttu-id="6760f-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="6760f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="6760f-105">Dynamics 365 Project Operations poskytuje organizacím možnost definovat, jak řídí změny klíčových proměnných v úkolech ve strukturovaném rozpisu prací.</span><span class="sxs-lookup"><span data-stu-id="6760f-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="6760f-106">Na základě konkrétních potřeb organizace mohou projektoví manažeři při vytváření projektu provádět změny v režimu plánování.</span><span class="sxs-lookup"><span data-stu-id="6760f-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="6760f-107">V Project Operations jsou k dispozici tři režimy plánování:</span><span class="sxs-lookup"><span data-stu-id="6760f-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="6760f-108">Pevná doba trvání (toto je výchozí režim)</span><span class="sxs-lookup"><span data-stu-id="6760f-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="6760f-109">Pevná práce</span><span class="sxs-lookup"><span data-stu-id="6760f-109">Fixed work</span></span>
  - <span data-ttu-id="6760f-110">Pevné jednotky</span><span class="sxs-lookup"><span data-stu-id="6760f-110">Fixed units</span></span>

<span data-ttu-id="6760f-111">Hodnoty ovlivněné definicí konkrétního režimu plánování jsou určeny následujícím vzorcem:</span><span class="sxs-lookup"><span data-stu-id="6760f-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="6760f-112">Úsilí (*Práce*) = Doba trvání × Jednotky</span><span class="sxs-lookup"><span data-stu-id="6760f-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="6760f-113">Když definujete režim plánování projektu, nastavujete jednu z těchto hodnot, kterou pak nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="6760f-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="6760f-114">Udržování této hodnoty jako konstanty klade prioritu na tuto hodnotu, která upozorní systém, aby ji nezměnil, když se změní další dvě hodnoty.</span><span class="sxs-lookup"><span data-stu-id="6760f-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="6760f-115">Následující tabulka poskytuje informace o dopadech výběru konkrétního režimu.</span><span class="sxs-lookup"><span data-stu-id="6760f-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="6760f-116">**V tomto úkolu**</span><span class="sxs-lookup"><span data-stu-id="6760f-116">**In this task**</span></span>             | <span data-ttu-id="6760f-117">**Pokud revidujete jednotky**</span><span class="sxs-lookup"><span data-stu-id="6760f-117">**If you revise units**</span></span>   | <span data-ttu-id="6760f-118">**Pokud revidujete dobu trvání**</span><span class="sxs-lookup"><span data-stu-id="6760f-118">**If you revise duration**</span></span> | <span data-ttu-id="6760f-119">**Pokud revidujete úsilí**</span><span class="sxs-lookup"><span data-stu-id="6760f-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="6760f-120">Úkoly s pevnými jednotkami</span><span class="sxs-lookup"><span data-stu-id="6760f-120">Fixed units task</span></span>     | <span data-ttu-id="6760f-121">Doba trvání se přepočítá.</span><span class="sxs-lookup"><span data-stu-id="6760f-121">Duration is recalculated.</span></span> | <span data-ttu-id="6760f-122">Úsilí se přepočítá.</span><span class="sxs-lookup"><span data-stu-id="6760f-122">Effort is recalculated.</span></span>    | <span data-ttu-id="6760f-123">Doba trvání se přepočítá.</span><span class="sxs-lookup"><span data-stu-id="6760f-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="6760f-124">Úkol s pevným úsilím</span><span class="sxs-lookup"><span data-stu-id="6760f-124">Fixed effort task</span></span>    | <span data-ttu-id="6760f-125">Doba trvání se přepočítá.</span><span class="sxs-lookup"><span data-stu-id="6760f-125">Duration is recalculated.</span></span> | <span data-ttu-id="6760f-126">Jednotky jsou přepočítány.</span><span class="sxs-lookup"><span data-stu-id="6760f-126">Units are recalculated.</span></span>    | <span data-ttu-id="6760f-127">Doba trvání se přepočítá.</span><span class="sxs-lookup"><span data-stu-id="6760f-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="6760f-128">Úkol s pevnou dobou trvání</span><span class="sxs-lookup"><span data-stu-id="6760f-128">Fixed duration task</span></span>  | <span data-ttu-id="6760f-129">Úsilí se přepočítá.</span><span class="sxs-lookup"><span data-stu-id="6760f-129">Effort is recalculated.</span></span>   | <span data-ttu-id="6760f-130">Úsilí se přepočítá.</span><span class="sxs-lookup"><span data-stu-id="6760f-130">Effort is recalculated.</span></span>    | <span data-ttu-id="6760f-131">Jednotky jsou přepočítány.</span><span class="sxs-lookup"><span data-stu-id="6760f-131">Units are recalculated.</span></span>   |

<span data-ttu-id="6760f-132">Další informace o implikacích daného režimu najdete v části [Změna typu úkolu pro přesnější plánování](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="6760f-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="6760f-133">V téma se výraz **Práce** se používá místo **Úsilí**.</span><span class="sxs-lookup"><span data-stu-id="6760f-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="6760f-134">Změna režimu plánování organizace</span><span class="sxs-lookup"><span data-stu-id="6760f-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="6760f-135">Chcete-li definovat režim plánování organizace, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="6760f-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="6760f-136">Přejděte na **Nastavení** \> **Obecné** \> **Parametry** a potom vyberte parametr projektu.</span><span class="sxs-lookup"><span data-stu-id="6760f-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="6760f-137">Na stránce **Parametry projektu** vyberte výchozí režim plánování pro organizaci a poté definujte možnost projektového manažera přepsat toto nastavení při vytváření nového projektu.</span><span class="sxs-lookup"><span data-stu-id="6760f-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="6760f-138">Změna nastavení režimu plánování na projektu</span><span class="sxs-lookup"><span data-stu-id="6760f-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="6760f-139">Pokud organizace umožňuje manažerovi projektu přepsat výchozí režim plánování, může projektový manažer tuto změnu provést, když vytvoří nový projekt.</span><span class="sxs-lookup"><span data-stu-id="6760f-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="6760f-140">Po uložení projektu však nelze režim plánování změnit.</span><span class="sxs-lookup"><span data-stu-id="6760f-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="6760f-141">Zkopírované projekty</span><span class="sxs-lookup"><span data-stu-id="6760f-141">Copied projects</span></span>

<span data-ttu-id="6760f-142">Protože je projekt vytvořen, když je provedena akce kopírování projektu, manažer projektu nemůže nastavit režim plánování.</span><span class="sxs-lookup"><span data-stu-id="6760f-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="6760f-143">Cílový projekt bude vždy výchozí do režimu definovaného na úrovni organizace.</span><span class="sxs-lookup"><span data-stu-id="6760f-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="6760f-144">Zkopírované úkoly</span><span class="sxs-lookup"><span data-stu-id="6760f-144">Copied tasks</span></span>

<span data-ttu-id="6760f-145">Když je úkol zkopírován z jednoho projektu do druhého, zdědí úkol režim plánování cílového projektu.</span><span class="sxs-lookup"><span data-stu-id="6760f-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
