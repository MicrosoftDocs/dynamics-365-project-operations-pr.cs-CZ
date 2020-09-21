---
title: Skupiny jednotek a jednotky
description: Toto téma poskytuje informace o skupinách jednotek a jednotkách.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: b5422be3-5bfc-4ee2-b19a-4eca68813ff2
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fc2dde2d9471f8585c190a65f3ad9b32de75af86
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750438"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="f8854-103">Skupiny jednotek a jednotky</span><span class="sxs-lookup"><span data-stu-id="f8854-103">Unit groups and units</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f8854-104">Skupiny jednotek a jednotky jsou základními entitami v Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f8854-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="f8854-105">Jednotka je jedna měrná jednotka a více jednotek lze seskupit do skupin jednotek.</span><span class="sxs-lookup"><span data-stu-id="f8854-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="f8854-106">Skupina jednotek se v uživatelském rozhraní (UI) aplikace Dynamics 365 někdy označuje jako rozpis jednotky.</span><span class="sxs-lookup"><span data-stu-id="f8854-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="f8854-107">Zde je několik příkladů jednotek a skupin jednotek:</span><span class="sxs-lookup"><span data-stu-id="f8854-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="f8854-108">**Skupina jednotek**: Vzdálenost</span><span class="sxs-lookup"><span data-stu-id="f8854-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="f8854-109">**Jednotky**: míle, kilometr a tak dál.</span><span class="sxs-lookup"><span data-stu-id="f8854-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="f8854-110">**Skupina jednotek**: Čas</span><span class="sxs-lookup"><span data-stu-id="f8854-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="f8854-111">**Jednotky**: hodina, den, týden atd.</span><span class="sxs-lookup"><span data-stu-id="f8854-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="f8854-112">Pokud nastavíte více jednotek ve skupině jednotek, musíte také nastavit koeficient převodu tak, že určíte první jednotku, kterou nastavíte jako výchozí nebo primární jednotku pro skupinu jednotek.</span><span class="sxs-lookup"><span data-stu-id="f8854-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="f8854-113">Pokud například ve skupině jednotek **Čas** nastavíte jako první jednotku **Hodina**, systém označí **Hodinu** jako výchozí jednotku.</span><span class="sxs-lookup"><span data-stu-id="f8854-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="f8854-114">Pokud je následující jednotka, kterou nastavíte, **Den**, musíte nastavit koeficient převodu pro **Den** na **Hodinu.**</span><span class="sxs-lookup"><span data-stu-id="f8854-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="f8854-115">Pokud potom jako třetí jednotku přidáte **Týden**, musíte nastavit koeficient převodu pro **Týden** podle **Dnů** nebo **Hodin**.</span><span class="sxs-lookup"><span data-stu-id="f8854-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="f8854-116">Následující obrázek znázorňuje příklad nastavení pro jednotku **Den**, kde pole **Množství** zobrazuje počet hodin v rámci dne a **Týdne**, kde pole **Množství** zobrazí počet dnů v týdnu.</span><span class="sxs-lookup"><span data-stu-id="f8854-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Skupina jednotek: Stránka s informacemi](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="f8854-118">Použití jednotek a skupin jednotek</span><span class="sxs-lookup"><span data-stu-id="f8854-118">Using units and unit groups</span></span>

<span data-ttu-id="f8854-119">Dynamics 365 Project Service Automation používá jednotky a skupiny jednotek ke zpracování odhadů a položek pro náklady i čas.</span><span class="sxs-lookup"><span data-stu-id="f8854-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="f8854-120">U výdajů má každá kategorie výdajů výchozí skupinu jednotek a jednotku.</span><span class="sxs-lookup"><span data-stu-id="f8854-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="f8854-121">Tyto hodnoty jsou zadány jako výchozí hodnoty pro položky ceníku pro kategorie výdajů.</span><span class="sxs-lookup"><span data-stu-id="f8854-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="f8854-122">Máte například kategorii výdajů s názvem **Mílovné**.</span><span class="sxs-lookup"><span data-stu-id="f8854-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="f8854-123">Obsahuje skupinu jednotek pojmenovanou **Vzdálenost** a výchozí jednotku pojmenovanou **Míle**.</span><span class="sxs-lookup"><span data-stu-id="f8854-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="f8854-124">Nastavíte-li skupinu jednotek **Vzdálenost** tak, aby obsahovala dvě jednotky (**Míle** a **Kilometr**), můžete nastavit dvě ceny pro kategorii **Mílovné** v jednom ceníku: cena za míli a cena za kilometr.</span><span class="sxs-lookup"><span data-stu-id="f8854-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="f8854-125">Kategorie výdaje</span><span class="sxs-lookup"><span data-stu-id="f8854-125">Expense category</span></span>  | <span data-ttu-id="f8854-126">Skupina jednotek</span><span class="sxs-lookup"><span data-stu-id="f8854-126">Unit group</span></span>  | <span data-ttu-id="f8854-127">Jednotka</span><span class="sxs-lookup"><span data-stu-id="f8854-127">Unit</span></span>      | <span data-ttu-id="f8854-128">Způsob ocenění</span><span class="sxs-lookup"><span data-stu-id="f8854-128">Pricing method</span></span>  | <span data-ttu-id="f8854-129">Cena za jednotku</span><span class="sxs-lookup"><span data-stu-id="f8854-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="f8854-130">Mílovné</span><span class="sxs-lookup"><span data-stu-id="f8854-130">Mileage</span></span>           | <span data-ttu-id="f8854-131">Vzdálenost</span><span class="sxs-lookup"><span data-stu-id="f8854-131">Distance</span></span>      | <span data-ttu-id="f8854-132">Míle</span><span class="sxs-lookup"><span data-stu-id="f8854-132">Mile</span></span>      | <span data-ttu-id="f8854-133">Cena za jednotku</span><span class="sxs-lookup"><span data-stu-id="f8854-133">Price per unit</span></span>    | <span data-ttu-id="f8854-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="f8854-134">10 USD</span></span>            |
| <span data-ttu-id="f8854-135">Mílovné</span><span class="sxs-lookup"><span data-stu-id="f8854-135">Mileage</span></span>           | <span data-ttu-id="f8854-136">Vzdálenost</span><span class="sxs-lookup"><span data-stu-id="f8854-136">Distance</span></span>      | <span data-ttu-id="f8854-137">Kilometr</span><span class="sxs-lookup"><span data-stu-id="f8854-137">Kilometer</span></span> | <span data-ttu-id="f8854-138">Cena za jednotku</span><span class="sxs-lookup"><span data-stu-id="f8854-138">Price per unit</span></span>    |  <span data-ttu-id="f8854-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="f8854-139">6 USD</span></span>            |

<span data-ttu-id="f8854-140">Když zadáte výdaj do projektu, systém určí cenu pomocí kombinace kategorie a jednotky na náklady.</span><span class="sxs-lookup"><span data-stu-id="f8854-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="f8854-141">Popis výdaje</span><span class="sxs-lookup"><span data-stu-id="f8854-141">Expense description</span></span>        | <span data-ttu-id="f8854-142">Kategorie výdaje</span><span class="sxs-lookup"><span data-stu-id="f8854-142">Expense category</span></span>  | <span data-ttu-id="f8854-143">Jednotka</span><span class="sxs-lookup"><span data-stu-id="f8854-143">Unit</span></span>  | <span data-ttu-id="f8854-144">Množství</span><span class="sxs-lookup"><span data-stu-id="f8854-144">Quantity</span></span>  | <span data-ttu-id="f8854-145">Cena za jednotku</span><span class="sxs-lookup"><span data-stu-id="f8854-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="f8854-146">Cesta do umístění klienta</span><span class="sxs-lookup"><span data-stu-id="f8854-146">Drive to client location</span></span> | <span data-ttu-id="f8854-147">Mílovné</span><span class="sxs-lookup"><span data-stu-id="f8854-147">Mileage</span></span>             | <span data-ttu-id="f8854-148">Míle</span><span class="sxs-lookup"><span data-stu-id="f8854-148">Mile</span></span>  | <span data-ttu-id="f8854-149">10</span><span class="sxs-lookup"><span data-stu-id="f8854-149">10</span></span>        | <span data-ttu-id="f8854-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="f8854-150">10 USD</span></span>         |

<span data-ttu-id="f8854-151">Každá hlavička ceníku má pro čas pole **Výchozí časová jednotka**.</span><span class="sxs-lookup"><span data-stu-id="f8854-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="f8854-152">Tato hodnota se nastavuje při vytváření záhlaví ceníku.</span><span class="sxs-lookup"><span data-stu-id="f8854-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="f8854-153">Tato jednotka se pak používá k nastavení všech cen na základě rolí na tomto ceníku.</span><span class="sxs-lookup"><span data-stu-id="f8854-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="f8854-154">Řádky odhadu pro pole **Čas na nabídce** lze vyjádřit v libovolné časové jednotce.</span><span class="sxs-lookup"><span data-stu-id="f8854-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="f8854-155">Řádky odhadu v projektech a časových položkách pro projekty však mohou používat pouze jednotku času **Hodina**.</span><span class="sxs-lookup"><span data-stu-id="f8854-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="f8854-156">Pokud jednotka v řádku časového záznamu nebo odhadu neodpovídá jednotce na řádku ceníku pro tuto roli, převede systém cenu na jednotky definované v odhadu projektu nebo skutečné transakci projektu.</span><span class="sxs-lookup"><span data-stu-id="f8854-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="f8854-157">Následující příklad ukazuje, jak PSA používá skupinu jednotek, jednotky a koeficienty převodu.</span><span class="sxs-lookup"><span data-stu-id="f8854-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="f8854-158">Jednotky</span><span class="sxs-lookup"><span data-stu-id="f8854-158">Units</span></span>

   - <span data-ttu-id="f8854-159">**Skupina jednotek**: Čas</span><span class="sxs-lookup"><span data-stu-id="f8854-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="f8854-160">**Jednotky**: Hodina</span><span class="sxs-lookup"><span data-stu-id="f8854-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="f8854-161">**Den** – koeficient převodu: 8 hodin</span><span class="sxs-lookup"><span data-stu-id="f8854-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="f8854-162">**Týden** – koeficient převodu: 40 hodin</span><span class="sxs-lookup"><span data-stu-id="f8854-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="f8854-163">Nastavení ceníku na projektu A:</span><span class="sxs-lookup"><span data-stu-id="f8854-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="f8854-164">**Název**: prodejní ceny UK 2016</span><span class="sxs-lookup"><span data-stu-id="f8854-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="f8854-165">**Výchozí časová jednotka**: Den</span><span class="sxs-lookup"><span data-stu-id="f8854-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="f8854-166">**Měna**: GBP</span><span class="sxs-lookup"><span data-stu-id="f8854-166">**Currency**: GBP</span></span>

| <span data-ttu-id="f8854-167">Role</span><span class="sxs-lookup"><span data-stu-id="f8854-167">Role</span></span>      | <span data-ttu-id="f8854-168">Skupina jednotek</span><span class="sxs-lookup"><span data-stu-id="f8854-168">Unit group</span></span> | <span data-ttu-id="f8854-169">Jednotka</span><span class="sxs-lookup"><span data-stu-id="f8854-169">Unit</span></span> | <span data-ttu-id="f8854-170">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="f8854-170">Organizational unit</span></span> | <span data-ttu-id="f8854-171">Cena</span><span class="sxs-lookup"><span data-stu-id="f8854-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="f8854-172">Vývojář</span><span class="sxs-lookup"><span data-stu-id="f8854-172">Developer</span></span> | <span data-ttu-id="f8854-173">Time</span><span class="sxs-lookup"><span data-stu-id="f8854-173">Time</span></span>       | <span data-ttu-id="f8854-174">Day</span><span class="sxs-lookup"><span data-stu-id="f8854-174">Day</span></span>  | <span data-ttu-id="f8854-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="f8854-175">Contoso UK</span></span>          | <span data-ttu-id="f8854-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="f8854-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="f8854-177">Časový záznam</span><span class="sxs-lookup"><span data-stu-id="f8854-177">Time entry</span></span>

<span data-ttu-id="f8854-178">Následující tabulka zobrazuje výsledné transakce na straně prodeje vytvořené pomocí PSA pro tříhodinový projekt.</span><span class="sxs-lookup"><span data-stu-id="f8854-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="f8854-179">Projekt</span><span class="sxs-lookup"><span data-stu-id="f8854-179">Project</span></span>   | <span data-ttu-id="f8854-180">Task</span><span class="sxs-lookup"><span data-stu-id="f8854-180">Task</span></span>    | <span data-ttu-id="f8854-181">Role</span><span class="sxs-lookup"><span data-stu-id="f8854-181">Role</span></span>      | <span data-ttu-id="f8854-182">Množství</span><span class="sxs-lookup"><span data-stu-id="f8854-182">Quantity</span></span> | <span data-ttu-id="f8854-183">Jednotka</span><span class="sxs-lookup"><span data-stu-id="f8854-183">Unit</span></span>  | <span data-ttu-id="f8854-184">Cena za jednotku</span><span class="sxs-lookup"><span data-stu-id="f8854-184">Unit price</span></span> | <span data-ttu-id="f8854-185">Nefakturovaná prodejní částka</span><span class="sxs-lookup"><span data-stu-id="f8854-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="f8854-186">Projekt A</span><span class="sxs-lookup"><span data-stu-id="f8854-186">Project A</span></span> | <span data-ttu-id="f8854-187">Návrh</span><span class="sxs-lookup"><span data-stu-id="f8854-187">Design</span></span>  | <span data-ttu-id="f8854-188">Vývojář</span><span class="sxs-lookup"><span data-stu-id="f8854-188">Developer</span></span> | <span data-ttu-id="f8854-189">3</span><span class="sxs-lookup"><span data-stu-id="f8854-189">3</span></span>        | <span data-ttu-id="f8854-190">Hour</span><span class="sxs-lookup"><span data-stu-id="f8854-190">Hour</span></span>  | <span data-ttu-id="f8854-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="f8854-191">100 GBP</span></span>    | <span data-ttu-id="f8854-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="f8854-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="f8854-193">Nejčastější dotazy k časové jednotce</span><span class="sxs-lookup"><span data-stu-id="f8854-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="f8854-194">Převádí se PSA na různé jednotky v případě výdajů?</span><span class="sxs-lookup"><span data-stu-id="f8854-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="f8854-195">Č.</span><span class="sxs-lookup"><span data-stu-id="f8854-195">No.</span></span> <span data-ttu-id="f8854-196">Převod jednotek funguje pouze pro čas.</span><span class="sxs-lookup"><span data-stu-id="f8854-196">Unit conversion works only for time.</span></span> <span data-ttu-id="f8854-197">V případě výdajů, pokud systém nemůže najít cenu pro kombinaci kategorie výdajů a jednotky, je ve výchozím nastavení cena nastavena na 0,00.</span><span class="sxs-lookup"><span data-stu-id="f8854-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="f8854-198">Proč PSA převádí časové jednotky?</span><span class="sxs-lookup"><span data-stu-id="f8854-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="f8854-199">V některých zemích nebo oblastech existuje právní požadavek, aby byly fakturační sazby nastaveny ve dnech.</span><span class="sxs-lookup"><span data-stu-id="f8854-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="f8854-200">Sjednání ceny a slevy během cyklu nabídky se provádí pomocí denních sazeb pro každou fakturovatelnou roli.</span><span class="sxs-lookup"><span data-stu-id="f8854-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="f8854-201">Odhad plánu a časový záznam se provádí v hodinách.</span><span class="sxs-lookup"><span data-stu-id="f8854-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="f8854-202">Pro podporu tohoto rozdílu v časových jednotkách převádí PSA časové jednotky.</span><span class="sxs-lookup"><span data-stu-id="f8854-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="f8854-203">Lze změnit časové jednotky v odhadech projektu?</span><span class="sxs-lookup"><span data-stu-id="f8854-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="f8854-204">Č.</span><span class="sxs-lookup"><span data-stu-id="f8854-204">No.</span></span> <span data-ttu-id="f8854-205">Odhad plánu je nyní omezen na hodiny a nelze jej změnit.</span><span class="sxs-lookup"><span data-stu-id="f8854-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="f8854-206">Lze jednotky a skupiny jednotek upravit, odstranit a přidat?</span><span class="sxs-lookup"><span data-stu-id="f8854-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="f8854-207">Ano.</span><span class="sxs-lookup"><span data-stu-id="f8854-207">Yes.</span></span> <span data-ttu-id="f8854-208">S výjimkou skupiny jednotek **Čas** a jednotky **Hodina** lze všechny jednotky odstranit nebo upravit a přidat nové jednotky.</span><span class="sxs-lookup"><span data-stu-id="f8854-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="f8854-209">V PSA nelze skupinu jednotek **Čas** a jednotku **Hodina** odstranit.</span><span class="sxs-lookup"><span data-stu-id="f8854-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="f8854-210">Lze je však aktualizovat pomocí přeloženého textu pro pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="f8854-210">However, they can be updated with a translated text for the **Name** field.</span></span>
