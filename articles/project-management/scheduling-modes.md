---
title: Režimy plánování
description: Toto téma poskytuje informace o režimech plánování.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116699"
---
# <a name="scheduling-modes"></a><span data-ttu-id="7bb65-103">Režimy plánování</span><span class="sxs-lookup"><span data-stu-id="7bb65-103">Scheduling modes</span></span>

<span data-ttu-id="7bb65-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="7bb65-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7bb65-105">Dynamics 365 Project Operations poskytuje organizacím možnost definovat, jak řídí změny klíčových proměnných v úkolech ve strukturovaném rozpisu prací.</span><span class="sxs-lookup"><span data-stu-id="7bb65-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="7bb65-106">Na základě konkrétních potřeb organizace mohou projektoví manažeři při vytváření projektu provádět změny v režimu plánování.</span><span class="sxs-lookup"><span data-stu-id="7bb65-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="7bb65-107">V Project Operations jsou k dispozici tři režimy plánování:</span><span class="sxs-lookup"><span data-stu-id="7bb65-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="7bb65-108">Pevná doba trvání (toto je výchozí režim)</span><span class="sxs-lookup"><span data-stu-id="7bb65-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="7bb65-109">Opravené úsilí (*Práce*)</span><span class="sxs-lookup"><span data-stu-id="7bb65-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="7bb65-110">Pevné jednotky</span><span class="sxs-lookup"><span data-stu-id="7bb65-110">Fixed units</span></span>

<span data-ttu-id="7bb65-111">Hodnoty ovlivněné definicí konkrétního režimu plánování jsou určeny následujícím vzorcem:</span><span class="sxs-lookup"><span data-stu-id="7bb65-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="7bb65-112">Úsilí = trvání × jednotky</span><span class="sxs-lookup"><span data-stu-id="7bb65-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="7bb65-113">Když definujete režim plánování projektu, nastavujete jednu z těchto hodnot, kterou pak nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="7bb65-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="7bb65-114">Udržování této hodnoty jako konstanty klade prioritu na tuto hodnotu, která upozorní systém, aby ji nezměnil, když se změní další dvě hodnoty.</span><span class="sxs-lookup"><span data-stu-id="7bb65-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="7bb65-115">Následující tabulka poskytuje informace o dopadech výběru konkrétního režimu.</span><span class="sxs-lookup"><span data-stu-id="7bb65-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="7bb65-116">**V tomto úkolu**</span><span class="sxs-lookup"><span data-stu-id="7bb65-116">**In this task**</span></span>             | <span data-ttu-id="7bb65-117">**Pokud revidujete jednotky**</span><span class="sxs-lookup"><span data-stu-id="7bb65-117">**If you revise units**</span></span>   | <span data-ttu-id="7bb65-118">**Pokud revidujete dobu trvání**</span><span class="sxs-lookup"><span data-stu-id="7bb65-118">**If you revise duration**</span></span> | <span data-ttu-id="7bb65-119">**Pokud revidujete úsilí**</span><span class="sxs-lookup"><span data-stu-id="7bb65-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="7bb65-120">Úkoly s pevnými jednotkami</span><span class="sxs-lookup"><span data-stu-id="7bb65-120">Fixed units task</span></span>     | <span data-ttu-id="7bb65-121">Doba trvání se přepočítá.</span><span class="sxs-lookup"><span data-stu-id="7bb65-121">Duration is recalculated.</span></span> | <span data-ttu-id="7bb65-122">Úsilí se přepočítá.</span><span class="sxs-lookup"><span data-stu-id="7bb65-122">Effort is recalculated.</span></span>    | <span data-ttu-id="7bb65-123">Doba trvání se přepočítá.</span><span class="sxs-lookup"><span data-stu-id="7bb65-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="7bb65-124">Úkol s pevným úsilím</span><span class="sxs-lookup"><span data-stu-id="7bb65-124">Fixed effort task</span></span>    | <span data-ttu-id="7bb65-125">Doba trvání se přepočítá.</span><span class="sxs-lookup"><span data-stu-id="7bb65-125">Duration is recalculated.</span></span> | <span data-ttu-id="7bb65-126">Jednotky jsou přepočítány.</span><span class="sxs-lookup"><span data-stu-id="7bb65-126">Units are recalculated.</span></span>    | <span data-ttu-id="7bb65-127">Doba trvání se přepočítá.</span><span class="sxs-lookup"><span data-stu-id="7bb65-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="7bb65-128">Úkol s pevnou dobou trvání</span><span class="sxs-lookup"><span data-stu-id="7bb65-128">Fixed duration task</span></span>  | <span data-ttu-id="7bb65-129">Úsilí se přepočítá.</span><span class="sxs-lookup"><span data-stu-id="7bb65-129">Effort is recalculated.</span></span>   | <span data-ttu-id="7bb65-130">Úsilí se přepočítá.</span><span class="sxs-lookup"><span data-stu-id="7bb65-130">Effort is recalculated.</span></span>    | <span data-ttu-id="7bb65-131">Jednotky jsou přepočítány.</span><span class="sxs-lookup"><span data-stu-id="7bb65-131">Units are recalculated.</span></span>   |

<span data-ttu-id="7bb65-132">Další informace o implikacích daného režimu najdete v části [Změna typu úkolu pro přesnější plánování](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="7bb65-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="7bb65-133">V téma se výraz **Práce** se používá místo **Úsilí**.</span><span class="sxs-lookup"><span data-stu-id="7bb65-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="7bb65-134">Změna režimu plánování organizace</span><span class="sxs-lookup"><span data-stu-id="7bb65-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="7bb65-135">Chcete-li definovat režim plánování organizace, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="7bb65-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="7bb65-136">Přejděte na **Nastavení** \> **Obecné** \> **Parametry** a potom vyberte parametr projektu.</span><span class="sxs-lookup"><span data-stu-id="7bb65-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="7bb65-137">Na stránce **Parametry projektu** vyberte výchozí režim plánování pro organizaci a poté definujte možnost projektového manažera přepsat toto nastavení při vytváření nového projektu.</span><span class="sxs-lookup"><span data-stu-id="7bb65-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="7bb65-138">Změna nastavení režimu plánování na projektu</span><span class="sxs-lookup"><span data-stu-id="7bb65-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="7bb65-139">Pokud organizace umožňuje manažerovi projektu přepsat výchozí režim plánování, může projektový manažer tuto změnu provést, když vytvoří nový projekt.</span><span class="sxs-lookup"><span data-stu-id="7bb65-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="7bb65-140">Po uložení projektu však nelze režim plánování změnit.</span><span class="sxs-lookup"><span data-stu-id="7bb65-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="7bb65-141">Zkopírované projekty</span><span class="sxs-lookup"><span data-stu-id="7bb65-141">Copied projects</span></span>

<span data-ttu-id="7bb65-142">Protože je projekt vytvořen, když je provedena akce kopírování projektu, manažer projektu nemůže nastavit režim plánování.</span><span class="sxs-lookup"><span data-stu-id="7bb65-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="7bb65-143">Cílový projekt bude vždy výchozí do režimu definovaného na úrovni organizace.</span><span class="sxs-lookup"><span data-stu-id="7bb65-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="7bb65-144">Zkopírované úkoly</span><span class="sxs-lookup"><span data-stu-id="7bb65-144">Copied tasks</span></span>

<span data-ttu-id="7bb65-145">Když je úkol zkopírován z jednoho projektu do druhého, zdědí úkol režim plánování cílového projektu.</span><span class="sxs-lookup"><span data-stu-id="7bb65-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
