---
title: Pokrok projektu a spotřeba nákladů
description: Toto téma obsahuje informace o způsobu sledování pokroku projektu a spotřeby nákladů.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750393"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="695b7-103">Pokrok projektu a spotřeba nákladů</span><span class="sxs-lookup"><span data-stu-id="695b7-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="695b7-104">Potřeba sledovat pokrok oproti plánu se liší podle odvětví.</span><span class="sxs-lookup"><span data-stu-id="695b7-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="695b7-105">Některá odvětví sledují pokrok podrobně, zatímco jiná odvětví ho sledují na vyšší úrovni.</span><span class="sxs-lookup"><span data-stu-id="695b7-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="695b7-106">Toto téma ukazuje, jak plánovat, abyste vyhověli požadavkům vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="695b7-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="695b7-107">Zobrazení sledování úsilí</span><span class="sxs-lookup"><span data-stu-id="695b7-107">Effort tracking view</span></span>

<span data-ttu-id="695b7-108">Zobrazení **Sledování úsilí** sleduje pokrok úkolů v plánu.</span><span class="sxs-lookup"><span data-stu-id="695b7-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="695b7-109">Porovnává skutečné úsilí (v hodinách) doposud vynaložené na úkol oproti úsilí (v hodinách) plánovanému pro úkol.</span><span class="sxs-lookup"><span data-stu-id="695b7-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="695b7-110">PSA pro výpočet metrik sledování používá následující vzorce:</span><span class="sxs-lookup"><span data-stu-id="695b7-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="695b7-111">Procento pokroku = skutečné úsilí vynaložené doposud ÷ plánované úsilí na úkol</span><span class="sxs-lookup"><span data-stu-id="695b7-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="695b7-112">Odhad dokončení (ETC) = plánované úsilí – skutečné úsilí vynaložené doposud</span><span class="sxs-lookup"><span data-stu-id="695b7-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="695b7-113">Odhad při dokončení (EAC) = zbývající úsilí + skutečné úsilí vynaložené doposud</span><span class="sxs-lookup"><span data-stu-id="695b7-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="695b7-114">Očekávaná odchylka úsilí = plánované úsilí – EAC</span><span class="sxs-lookup"><span data-stu-id="695b7-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="695b7-115">PSA u daného úkolu zobrazuje očekávanou odchylku úsilí.</span><span class="sxs-lookup"><span data-stu-id="695b7-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="695b7-116">Je-li EAC větší než plánované úsilí, předpokládá se, že úkol zabere více času, než bylo původně plánováno.</span><span class="sxs-lookup"><span data-stu-id="695b7-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="695b7-117">Proto je pozadu za plánem.</span><span class="sxs-lookup"><span data-stu-id="695b7-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="695b7-118">Je-li EAC menší než plánované úsilí, předpokládá se, že úkol zabere méně času, než bylo původně plánováno.</span><span class="sxs-lookup"><span data-stu-id="695b7-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="695b7-119">Proto je před plánem v předstihu.</span><span class="sxs-lookup"><span data-stu-id="695b7-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="695b7-120">Přeplánování úsilí</span><span class="sxs-lookup"><span data-stu-id="695b7-120">Re-projecting effort</span></span>

<span data-ttu-id="695b7-121">Je běžné, že projektový manažer reviduje původní odhady úkolu.</span><span class="sxs-lookup"><span data-stu-id="695b7-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="695b7-122">Předpovědi projektu jsou vnímání odhadů projektového manažera podle aktuálního stavu projektu.</span><span class="sxs-lookup"><span data-stu-id="695b7-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="695b7-123">Nedoporučujeme však, aby projektoví manažeři směrná čísla měnili, protože směrný plán projektu představuje stanovený zdroj pravdy pro odhady plánů a nákladů projektu a všichni účastníci projektu se na něm shodli.</span><span class="sxs-lookup"><span data-stu-id="695b7-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="695b7-124">Projektový manažer může předpovědět úsilí na úkoly dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="695b7-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="695b7-125">Přepsat výchozí hodnotu ETC novým odhadem skutečně zbývajícího úsilí na úkol.</span><span class="sxs-lookup"><span data-stu-id="695b7-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="695b7-126">Přepsat výchozí procento pokroku novým odhadem skutečného pokroku u úkolu.</span><span class="sxs-lookup"><span data-stu-id="695b7-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="695b7-127">Každý z těchto přístupů způsobuje přepočet hodnot ETC, EAC a procenta pokroku a očekávané odchylky úsilí daného úkolu.</span><span class="sxs-lookup"><span data-stu-id="695b7-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="695b7-128">Rovněž se přepočítají hodnoty EAC, ETC a procento pokroku souhrnných úkolů a vytvoří se nová projekce odchylky úsilí.</span><span class="sxs-lookup"><span data-stu-id="695b7-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="695b7-129">Nový odhad úsilí na souhrnné úkoly</span><span class="sxs-lookup"><span data-stu-id="695b7-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="695b7-130">Úsilí na souhrnné úkoly nebo úkoly kontejneru je možné znovu odhadnout.</span><span class="sxs-lookup"><span data-stu-id="695b7-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="695b7-131">Bez ohledu na to, zda uživatel provede nový odhad pomocí zbývajícího úsilí nebo procenta pokroku souhrnných úkolů, spustí se následující sada výpočtů:</span><span class="sxs-lookup"><span data-stu-id="695b7-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="695b7-132">Vypočítá se hodnota EAC, ETC a procento pokroku úkolu.</span><span class="sxs-lookup"><span data-stu-id="695b7-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="695b7-133">Nová hodnota EAC se na podřízené úkoly rozdělí ve stejném poměru jako původní EAC úkolu.</span><span class="sxs-lookup"><span data-stu-id="695b7-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="695b7-134">Dojde k výpočtu nové hodnoty EAC u jednotlivých úkolů, až po úkoly uzlů typu list.</span><span class="sxs-lookup"><span data-stu-id="695b7-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="695b7-135">Ovlivněné podřízené úkoly směrem k úkolům uzlů typu list mají hodnotu ETC a procentuální hodnotu pokroku přepočítány na základě hodnoty EAC.</span><span class="sxs-lookup"><span data-stu-id="695b7-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="695b7-136">Výsledkem je nový odhad odchylky úsilí na úkol.</span><span class="sxs-lookup"><span data-stu-id="695b7-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="695b7-137">Přepočítají se hodnoty EAC souhrnných úkolů všech cest ke kořenovému uzlu.</span><span class="sxs-lookup"><span data-stu-id="695b7-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="695b7-138">Zobrazení Sledování nákladů</span><span class="sxs-lookup"><span data-stu-id="695b7-138">Cost tracking view</span></span> 

<span data-ttu-id="695b7-139">Zobrazení **Sledování nákladů** porovnává skutečné náklady, které byly vynaloženy na úkol, s plánovanými náklady na úkol.</span><span class="sxs-lookup"><span data-stu-id="695b7-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="695b7-140">Toto zobrazení ukazuje pouze náklady práce a nezahrnuje náklady z odhadů výdajů.</span><span class="sxs-lookup"><span data-stu-id="695b7-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="695b7-141">PSA pro výpočet metrik sledování používá následující vzorce:</span><span class="sxs-lookup"><span data-stu-id="695b7-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="695b7-142">Procento spotřebovaných nákladů = skutečné náklady vynaložené doposud ÷ plánované náklady na úkol</span><span class="sxs-lookup"><span data-stu-id="695b7-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="695b7-143">Náklady na dokončení (CTC) = plánované náklady – skutečné náklady vynaložené doposud</span><span class="sxs-lookup"><span data-stu-id="695b7-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="695b7-144">EAC = CTC + skutečné náklady vynaložené doposud</span><span class="sxs-lookup"><span data-stu-id="695b7-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="695b7-145">Očekávaná odchylka nákladů = plánované náklady – EAC</span><span class="sxs-lookup"><span data-stu-id="695b7-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="695b7-146">U úkolu je zobrazen odhad odchylky nákladů.</span><span class="sxs-lookup"><span data-stu-id="695b7-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="695b7-147">Je-li EAC větší než plánované náklady, předpokládá se, že náklady na úkol budou vyšší, než bylo původně plánováno.</span><span class="sxs-lookup"><span data-stu-id="695b7-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="695b7-148">Proto vykazuje vývoj trendu nad rozpočet.</span><span class="sxs-lookup"><span data-stu-id="695b7-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="695b7-149">Je-li EAC menší než plánované náklady, předpokládá se, že náklady na úkol budou nižší, než bylo původně plánováno.</span><span class="sxs-lookup"><span data-stu-id="695b7-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="695b7-150">Proto vykazuje vývoj trendu pod rozpočtem.</span><span class="sxs-lookup"><span data-stu-id="695b7-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="695b7-151">Nová předpověď nákladů projektového manažera</span><span class="sxs-lookup"><span data-stu-id="695b7-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="695b7-152">Při nové předpovědi úsilí se hodnoty CTC, EAC, procento spotřebovaných nákladů a očekávaná odchylka nákladů přepočítají v zobrazení **Sledování nákladů**.</span><span class="sxs-lookup"><span data-stu-id="695b7-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="695b7-153">Souhrn stavu projektu</span><span class="sxs-lookup"><span data-stu-id="695b7-153">Project status summary</span></span>

<span data-ttu-id="695b7-154">Sledování dat v zobrazeních **Sledování úsilí** a **Sledování nákladů** znázorňuje pokrok a spotřebu nákladů na úrovni kořenového uzlu projektu, souhrnných úkolů a úkolů na úrovni uzlů typu list.</span><span class="sxs-lookup"><span data-stu-id="695b7-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="695b7-155">Část **Stav** na stránce **Entita projektu** zobrazuje souhrn stavu na úrovni projektu.</span><span class="sxs-lookup"><span data-stu-id="695b7-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="695b7-156">Souhrnná pole stavu</span><span class="sxs-lookup"><span data-stu-id="695b7-156">Status summary fields</span></span>

<span data-ttu-id="695b7-157">Pole **Celkový stav projektu** je upravitelné pole, které zobrazuje celkový stav projektu.</span><span class="sxs-lookup"><span data-stu-id="695b7-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="695b7-158">K označení zvyšujících se rizik používá barevné označení, například zelené, žluté a červené.</span><span class="sxs-lookup"><span data-stu-id="695b7-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="695b7-159">Pole **Komentáře** umožňuje projektovému manažerovi zadat konkrétní komentáře o stavu.</span><span class="sxs-lookup"><span data-stu-id="695b7-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="695b7-160">Pole **Datum aktualizace stavu** nelze upravit a tato hodnota je časové razítko, které označuje, kdy byl stav naposledy aktualizován.</span><span class="sxs-lookup"><span data-stu-id="695b7-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="695b7-161">Pole **Plnění plánu** a **Plnění nákladů** jsou nastavena od data sledování.</span><span class="sxs-lookup"><span data-stu-id="695b7-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="695b7-162">Pokud jsou odchylky plánu a nákladů kořenového uzlu v zobrazení **Sledování úsilí** kladné, můžete tato pole nastavit na **V předstihu**.</span><span class="sxs-lookup"><span data-stu-id="695b7-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="695b7-163">Pokud jsou odchylky plánu a nákladů kořenového uzlu záporné, můžete je nastavit na **Ve skluzu**.</span><span class="sxs-lookup"><span data-stu-id="695b7-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
