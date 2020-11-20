---
title: Průběh projektu a spotřeba nákladů
description: Toto téma obsahuje informace o sledování průběhu projektu a spotřeby nákladů.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 0793ee0c75bcbdde0fd92a16634457f73f872b5e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120625"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="75e4c-103">Průběh projektu a spotřeba nákladů</span><span class="sxs-lookup"><span data-stu-id="75e4c-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="75e4c-104">Potřeba sledovat pokrok oproti plánu se liší podle odvětví.</span><span class="sxs-lookup"><span data-stu-id="75e4c-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="75e4c-105">Některá odvětví sledují pokrok podrobně, zatímco jiná odvětví ho sledují na vyšší úrovni.</span><span class="sxs-lookup"><span data-stu-id="75e4c-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="75e4c-106">Toto téma ukazuje, jak plánovat, abyste vyhověli požadavkům vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="75e4c-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="75e4c-107">Zobrazení sledování úsilí</span><span class="sxs-lookup"><span data-stu-id="75e4c-107">Effort tracking view</span></span>

<span data-ttu-id="75e4c-108">Zobrazení **Sledování úsilí** sleduje pokrok úkolů v plánu.</span><span class="sxs-lookup"><span data-stu-id="75e4c-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="75e4c-109">Porovnává skutečné úsilí (v hodinách) doposud vynaložené na úkol oproti úsilí (v hodinách) plánovanému pro úkol.</span><span class="sxs-lookup"><span data-stu-id="75e4c-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="75e4c-110">Project Service Automation pro výpočet metrik sledování používá následující vzorce:</span><span class="sxs-lookup"><span data-stu-id="75e4c-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="75e4c-111">Nejprve při vytváření úkolu: Plánované náklady budou nastaveny na Odhadované náklady po dokončení.</span><span class="sxs-lookup"><span data-stu-id="75e4c-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="75e4c-112">Jakmile jsou u úkolu zaznamenána skutečná data, bude v zobrazení Sledování úsilí následující výpočet</span><span class="sxs-lookup"><span data-stu-id="75e4c-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="75e4c-113">Procento pokroku = skutečné úsilí vynaložené doposud + Odhad při dokončení (EAC)</span><span class="sxs-lookup"><span data-stu-id="75e4c-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="75e4c-114">Odhad na dokončení (ETC) = Odhad na dokončení (EAC) - skutečné vynaložené úsilí k dnešnímu dni</span><span class="sxs-lookup"><span data-stu-id="75e4c-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="75e4c-115">EAC = zbývající úsilí + skutečné úsilí vynaložené doposud</span><span class="sxs-lookup"><span data-stu-id="75e4c-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="75e4c-116">Očekávaná odchylka úsilí = plánované úsilí – EAC</span><span class="sxs-lookup"><span data-stu-id="75e4c-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="75e4c-117">Project Service Automation u daného úkolu zobrazuje očekávanou odchylku úsilí.</span><span class="sxs-lookup"><span data-stu-id="75e4c-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="75e4c-118">Je-li EAC větší než plánované úsilí, předpokládá se, že úkol zabere více času, než bylo původně plánováno.</span><span class="sxs-lookup"><span data-stu-id="75e4c-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="75e4c-119">Proto je pozadu za plánem.</span><span class="sxs-lookup"><span data-stu-id="75e4c-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="75e4c-120">Je-li EAC menší než plánované úsilí, předpokládá se, že úkol zabere méně času, než bylo původně plánováno.</span><span class="sxs-lookup"><span data-stu-id="75e4c-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="75e4c-121">Proto je před plánem v předstihu.</span><span class="sxs-lookup"><span data-stu-id="75e4c-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="75e4c-122">Přeplánování úsilí</span><span class="sxs-lookup"><span data-stu-id="75e4c-122">Reprojecting effort</span></span>

<span data-ttu-id="75e4c-123">Je běžné, že projektový manažer reviduje původní odhady úkolu.</span><span class="sxs-lookup"><span data-stu-id="75e4c-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="75e4c-124">Předpovědi projektu jsou vnímání odhadů projektového manažera podle aktuálního stavu projektu.</span><span class="sxs-lookup"><span data-stu-id="75e4c-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="75e4c-125">Nedoporučujeme však, aby projektoví manažeři směrná čísla měnili, protože směrný plán projektu představuje stanovený zdroj pravdy pro odhady plánů a nákladů projektu a všichni účastníci projektu se na něm shodli.</span><span class="sxs-lookup"><span data-stu-id="75e4c-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="75e4c-126">Projektový manažer může předpovědět úsilí na úkoly dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="75e4c-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="75e4c-127">Přepsat výchozí hodnotu ETC novým odhadem skutečně zbývajícího úsilí na úkol.</span><span class="sxs-lookup"><span data-stu-id="75e4c-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="75e4c-128">Přepsat výchozí procento pokroku novým odhadem skutečného pokroku u úkolu.</span><span class="sxs-lookup"><span data-stu-id="75e4c-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="75e4c-129">Každý z těchto přístupů způsobuje přepočet hodnot ETC, EAC a procenta pokroku a očekávané odchylky úsilí daného úkolu.</span><span class="sxs-lookup"><span data-stu-id="75e4c-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="75e4c-130">Rovněž se přepočítají hodnoty EAC, ETC a procento pokroku souhrnných úkolů a vytvoří se nová projekce odchylky úsilí.</span><span class="sxs-lookup"><span data-stu-id="75e4c-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="75e4c-131">Přeplánování úsilí na souhrnné úkoly</span><span class="sxs-lookup"><span data-stu-id="75e4c-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="75e4c-132">Úsilí na souhrnné úkoly nebo úkoly kontejneru je možné přeplánovat.</span><span class="sxs-lookup"><span data-stu-id="75e4c-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="75e4c-133">Bez ohledu na to, zda uživatel provede přeplánování pomocí zbývajícího úsilí nebo procenta pokroku souhrnných úkolů, spustí se následující sada výpočtů:</span><span class="sxs-lookup"><span data-stu-id="75e4c-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="75e4c-134">Vypočítá se hodnota EAC, ETC a procento pokroku úkolu.</span><span class="sxs-lookup"><span data-stu-id="75e4c-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="75e4c-135">Nová hodnota EAC se na podřízené úkoly rozdělí ve stejném poměru jako původní EAC úkolu.</span><span class="sxs-lookup"><span data-stu-id="75e4c-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="75e4c-136">Dojde k výpočtu nové hodnoty EAC u jednotlivých úkolů, až po úkoly uzlů typu list.</span><span class="sxs-lookup"><span data-stu-id="75e4c-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="75e4c-137">Ovlivněné podřízené úkoly směrem k úkolům uzlů typu list mají hodnotu ETC a procentuální hodnotu pokroku přepočítány na základě hodnoty EAC.</span><span class="sxs-lookup"><span data-stu-id="75e4c-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="75e4c-138">Výsledkem je nový odhad odchylky úsilí na úkol.</span><span class="sxs-lookup"><span data-stu-id="75e4c-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="75e4c-139">Přepočítají se hodnoty EAC souhrnných úkolů všech cest ke kořenovému uzlu.</span><span class="sxs-lookup"><span data-stu-id="75e4c-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="75e4c-140">Zobrazení Sledování nákladů</span><span class="sxs-lookup"><span data-stu-id="75e4c-140">Cost tracking view</span></span> 

<span data-ttu-id="75e4c-141">Zobrazení **Sledování nákladů** porovnává skutečné náklady, které byly vynaloženy na úkol, s plánovanými náklady.</span><span class="sxs-lookup"><span data-stu-id="75e4c-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="75e4c-142">Toto zobrazení ukazuje pouze náklady práce a nezahrnuje náklady z odhadů výdajů.</span><span class="sxs-lookup"><span data-stu-id="75e4c-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="75e4c-143">Project Service Automation pro výpočet metrik sledování používá následující vzorce:</span><span class="sxs-lookup"><span data-stu-id="75e4c-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="75e4c-144">Po vytvoření úkolu se plánované náklady rovnají odhadovaným nákladům při dokončení.</span><span class="sxs-lookup"><span data-stu-id="75e4c-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="75e4c-145">Jakmile jsou u úkolu zaznamenána skutečná data, bude v zobrazení **Sledování** pro náklady následující výpočet:</span><span class="sxs-lookup"><span data-stu-id="75e4c-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="75e4c-146">Procento spotřebovaných nákladů = skutečné náklady vynaložené doposud ÷ odhadované náklady při dokončení na úkol</span><span class="sxs-lookup"><span data-stu-id="75e4c-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="75e4c-147">Náklady na dokončení (CTC) = odhadované náklady při dokončení – skutečné náklady vynaložené doposud</span><span class="sxs-lookup"><span data-stu-id="75e4c-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="75e4c-148">Odhadované náklady při dokončení = (CTC) + skutečné náklady vynaložené doposud</span><span class="sxs-lookup"><span data-stu-id="75e4c-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="75e4c-149">Očekávaná odchylka nákladů = plánované náklady - odhadované náklady při dokončení</span><span class="sxs-lookup"><span data-stu-id="75e4c-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="75e4c-150">U úkolu je zobrazen odhad odchylky nákladů.</span><span class="sxs-lookup"><span data-stu-id="75e4c-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="75e4c-151">Josu-li odhadované náklady při dokončení větší než plánované náklady, předpokládá se, že náklady na úkol budou vyšší, než bylo původně plánováno.</span><span class="sxs-lookup"><span data-stu-id="75e4c-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="75e4c-152">Proto vykazuje vývoj trendu nad rozpočet.</span><span class="sxs-lookup"><span data-stu-id="75e4c-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="75e4c-153">Josu-li odhadované náklady při dokončení nižší než plánované náklady, předpokládá se, že náklady na úkol budou nižší, než bylo původně plánováno a vykazují vývoj trendu pod rozpočtem.</span><span class="sxs-lookup"><span data-stu-id="75e4c-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="75e4c-154">Přeplánování nákladů projektového manažera</span><span class="sxs-lookup"><span data-stu-id="75e4c-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="75e4c-155">Při nové předpovědi úsilí se hodnoty CTC, odhadované náklady při dokončení, procento spotřebovaných nákladů a očekávaná odchylka nákladů přepočítají v zobrazení **Sledování nákladů**.</span><span class="sxs-lookup"><span data-stu-id="75e4c-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="75e4c-156">Souhrn stavu projektu</span><span class="sxs-lookup"><span data-stu-id="75e4c-156">Project status summary</span></span>

<span data-ttu-id="75e4c-157">Sledování dat v zobrazeních **Sledování úsilí** a **Sledování nákladů** znázorňuje pokrok a spotřebu nákladů na úrovni kořenového uzlu projektu, souhrnných úkolů a úkolů na úrovni uzlů typu list.</span><span class="sxs-lookup"><span data-stu-id="75e4c-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="75e4c-158">Část **Stav** na stránce **Entita projektu** zobrazuje souhrn stavu na úrovni projektu.</span><span class="sxs-lookup"><span data-stu-id="75e4c-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="75e4c-159">Souhrnná pole stavu</span><span class="sxs-lookup"><span data-stu-id="75e4c-159">Status summary fields</span></span>

<span data-ttu-id="75e4c-160">Pole **Celkový stav projektu** je upravitelné pole, které zobrazuje celkový stav projektu.</span><span class="sxs-lookup"><span data-stu-id="75e4c-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="75e4c-161">K označení zvyšujících se rizik používá barevné označení, například zelené, žluté a červené.</span><span class="sxs-lookup"><span data-stu-id="75e4c-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="75e4c-162">Pole **Komentáře** umožňuje projektovému manažerovi zadat konkrétní komentáře o stavu.</span><span class="sxs-lookup"><span data-stu-id="75e4c-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="75e4c-163">Pole **Datum aktualizace stavu** nelze upravit a tato hodnota je časové razítko, které označuje, kdy byl stav naposledy aktualizován.</span><span class="sxs-lookup"><span data-stu-id="75e4c-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="75e4c-164">Pole **Plnění plánu** a **Plnění nákladů** jsou nastavena od data sledování.</span><span class="sxs-lookup"><span data-stu-id="75e4c-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="75e4c-165">Pokud jsou odchylky plánu a nákladů kořenového uzlu v zobrazení **Sledování úsilí** kladné, můžete tato pole nastavit na **V předstihu**.</span><span class="sxs-lookup"><span data-stu-id="75e4c-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="75e4c-166">Pokud jsou odchylky plánu a nákladů kořenového uzlu záporné, můžete je nastavit na **Ve skluzu**.</span><span class="sxs-lookup"><span data-stu-id="75e4c-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
