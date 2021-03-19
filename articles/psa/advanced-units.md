---
title: Skupiny jednotek a jednotky
description: Toto téma poskytuje informace o skupinách jednotek a jednotkách.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 45e4a95b429cd9d1f174653bd28cf567f690676d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291611"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="7de5b-103">Skupiny jednotek a jednotky</span><span class="sxs-lookup"><span data-stu-id="7de5b-103">Unit groups and units</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7de5b-104">Skupiny jednotek a jednotky jsou základními entitami v Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7de5b-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="7de5b-105">Jednotka je jedna měrná jednotka a více jednotek lze seskupit do skupin jednotek.</span><span class="sxs-lookup"><span data-stu-id="7de5b-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="7de5b-106">Skupina jednotek se v uživatelském rozhraní (UI) aplikace Dynamics 365 někdy označuje jako rozpis jednotky.</span><span class="sxs-lookup"><span data-stu-id="7de5b-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="7de5b-107">Zde je několik příkladů jednotek a skupin jednotek:</span><span class="sxs-lookup"><span data-stu-id="7de5b-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="7de5b-108">**Skupina jednotek**: Vzdálenost</span><span class="sxs-lookup"><span data-stu-id="7de5b-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="7de5b-109">**Jednotky**: míle, kilometr a tak dál.</span><span class="sxs-lookup"><span data-stu-id="7de5b-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="7de5b-110">**Skupina jednotek**: Čas</span><span class="sxs-lookup"><span data-stu-id="7de5b-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="7de5b-111">**Jednotky**: hodina, den, týden atd.</span><span class="sxs-lookup"><span data-stu-id="7de5b-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="7de5b-112">Pokud nastavíte více jednotek ve skupině jednotek, musíte také nastavit koeficient převodu tak, že určíte první jednotku, kterou nastavíte jako výchozí nebo primární jednotku pro skupinu jednotek.</span><span class="sxs-lookup"><span data-stu-id="7de5b-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="7de5b-113">Pokud například ve skupině jednotek **Čas** nastavíte jako první jednotku **Hodina**, systém označí **Hodinu** jako výchozí jednotku.</span><span class="sxs-lookup"><span data-stu-id="7de5b-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="7de5b-114">Pokud je následující jednotka, kterou nastavíte, **Den**, musíte nastavit koeficient převodu pro **Den** na **Hodinu.**</span><span class="sxs-lookup"><span data-stu-id="7de5b-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="7de5b-115">Pokud potom jako třetí jednotku přidáte **Týden**, musíte nastavit koeficient převodu pro **Týden** podle **Dnů** nebo **Hodin**.</span><span class="sxs-lookup"><span data-stu-id="7de5b-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="7de5b-116">Následující obrázek znázorňuje příklad nastavení pro jednotku **Den**, kde pole **Množství** zobrazuje počet hodin v rámci dne a **Týdne**, kde pole **Množství** zobrazí počet dnů v týdnu.</span><span class="sxs-lookup"><span data-stu-id="7de5b-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Skupina jednotek: Stránka s informacemi](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="7de5b-118">Použití jednotek a skupin jednotek</span><span class="sxs-lookup"><span data-stu-id="7de5b-118">Using units and unit groups</span></span>

<span data-ttu-id="7de5b-119">Dynamics 365 Project Service Automation používá jednotky a skupiny jednotek ke zpracování odhadů a položek pro náklady i čas.</span><span class="sxs-lookup"><span data-stu-id="7de5b-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="7de5b-120">U výdajů má každá kategorie výdajů výchozí skupinu jednotek a jednotku.</span><span class="sxs-lookup"><span data-stu-id="7de5b-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="7de5b-121">Tyto hodnoty jsou zadány jako výchozí hodnoty pro položky ceníku pro kategorie výdajů.</span><span class="sxs-lookup"><span data-stu-id="7de5b-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="7de5b-122">Máte například kategorii výdajů s názvem **Mílovné**.</span><span class="sxs-lookup"><span data-stu-id="7de5b-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="7de5b-123">Obsahuje skupinu jednotek pojmenovanou **Vzdálenost** a výchozí jednotku pojmenovanou **Míle**.</span><span class="sxs-lookup"><span data-stu-id="7de5b-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="7de5b-124">Nastavíte-li skupinu jednotek **Vzdálenost** tak, aby obsahovala dvě jednotky (**Míle** a **Kilometr**), můžete nastavit dvě ceny pro kategorii **Mílovné** v jednom ceníku: cena za míli a cena za kilometr.</span><span class="sxs-lookup"><span data-stu-id="7de5b-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="7de5b-125">Kategorie výdaje</span><span class="sxs-lookup"><span data-stu-id="7de5b-125">Expense category</span></span>  | <span data-ttu-id="7de5b-126">Skupina jednotek</span><span class="sxs-lookup"><span data-stu-id="7de5b-126">Unit group</span></span>  | <span data-ttu-id="7de5b-127">Jednotka</span><span class="sxs-lookup"><span data-stu-id="7de5b-127">Unit</span></span>      | <span data-ttu-id="7de5b-128">Způsob ocenění</span><span class="sxs-lookup"><span data-stu-id="7de5b-128">Pricing method</span></span>  | <span data-ttu-id="7de5b-129">Cena za jednotku</span><span class="sxs-lookup"><span data-stu-id="7de5b-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="7de5b-130">Mílovné</span><span class="sxs-lookup"><span data-stu-id="7de5b-130">Mileage</span></span>           | <span data-ttu-id="7de5b-131">Vzdálenost</span><span class="sxs-lookup"><span data-stu-id="7de5b-131">Distance</span></span>      | <span data-ttu-id="7de5b-132">Míle</span><span class="sxs-lookup"><span data-stu-id="7de5b-132">Mile</span></span>      | <span data-ttu-id="7de5b-133">Cena za jednotku</span><span class="sxs-lookup"><span data-stu-id="7de5b-133">Price per unit</span></span>    | <span data-ttu-id="7de5b-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="7de5b-134">10 USD</span></span>            |
| <span data-ttu-id="7de5b-135">Mílovné</span><span class="sxs-lookup"><span data-stu-id="7de5b-135">Mileage</span></span>           | <span data-ttu-id="7de5b-136">Vzdálenost</span><span class="sxs-lookup"><span data-stu-id="7de5b-136">Distance</span></span>      | <span data-ttu-id="7de5b-137">Kilometr</span><span class="sxs-lookup"><span data-stu-id="7de5b-137">Kilometer</span></span> | <span data-ttu-id="7de5b-138">Cena za jednotku</span><span class="sxs-lookup"><span data-stu-id="7de5b-138">Price per unit</span></span>    |  <span data-ttu-id="7de5b-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="7de5b-139">6 USD</span></span>            |

<span data-ttu-id="7de5b-140">Když zadáte výdaj do projektu, systém určí cenu pomocí kombinace kategorie a jednotky na náklady.</span><span class="sxs-lookup"><span data-stu-id="7de5b-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="7de5b-141">Popis výdaje</span><span class="sxs-lookup"><span data-stu-id="7de5b-141">Expense description</span></span>        | <span data-ttu-id="7de5b-142">Kategorie výdaje</span><span class="sxs-lookup"><span data-stu-id="7de5b-142">Expense category</span></span>  | <span data-ttu-id="7de5b-143">Jednotka</span><span class="sxs-lookup"><span data-stu-id="7de5b-143">Unit</span></span>  | <span data-ttu-id="7de5b-144">Množství</span><span class="sxs-lookup"><span data-stu-id="7de5b-144">Quantity</span></span>  | <span data-ttu-id="7de5b-145">Cena za jednotku</span><span class="sxs-lookup"><span data-stu-id="7de5b-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="7de5b-146">Cesta do umístění klienta</span><span class="sxs-lookup"><span data-stu-id="7de5b-146">Drive to client location</span></span> | <span data-ttu-id="7de5b-147">Mílovné</span><span class="sxs-lookup"><span data-stu-id="7de5b-147">Mileage</span></span>             | <span data-ttu-id="7de5b-148">Míle</span><span class="sxs-lookup"><span data-stu-id="7de5b-148">Mile</span></span>  | <span data-ttu-id="7de5b-149">10</span><span class="sxs-lookup"><span data-stu-id="7de5b-149">10</span></span>        | <span data-ttu-id="7de5b-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="7de5b-150">10 USD</span></span>         |

<span data-ttu-id="7de5b-151">Každá hlavička ceníku má pro čas pole **Výchozí časová jednotka**.</span><span class="sxs-lookup"><span data-stu-id="7de5b-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="7de5b-152">Tato hodnota se nastavuje při vytváření záhlaví ceníku.</span><span class="sxs-lookup"><span data-stu-id="7de5b-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="7de5b-153">Tato jednotka se pak používá k nastavení všech cen na základě rolí na tomto ceníku.</span><span class="sxs-lookup"><span data-stu-id="7de5b-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="7de5b-154">Řádky odhadu pro pole **Čas na nabídce** lze vyjádřit v libovolné časové jednotce.</span><span class="sxs-lookup"><span data-stu-id="7de5b-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="7de5b-155">Řádky odhadu v projektech a časových položkách pro projekty však mohou používat pouze jednotku času **Hodina**.</span><span class="sxs-lookup"><span data-stu-id="7de5b-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="7de5b-156">Pokud jednotka v řádku časového záznamu nebo odhadu neodpovídá jednotce na řádku ceníku pro tuto roli, převede systém cenu na jednotky definované v odhadu projektu nebo skutečné transakci projektu.</span><span class="sxs-lookup"><span data-stu-id="7de5b-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="7de5b-157">Následující příklad ukazuje, jak PSA používá skupinu jednotek, jednotky a koeficienty převodu.</span><span class="sxs-lookup"><span data-stu-id="7de5b-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="7de5b-158">Jednotky</span><span class="sxs-lookup"><span data-stu-id="7de5b-158">Units</span></span>

   - <span data-ttu-id="7de5b-159">**Skupina jednotek**: Čas</span><span class="sxs-lookup"><span data-stu-id="7de5b-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="7de5b-160">**Jednotky**: Hodina</span><span class="sxs-lookup"><span data-stu-id="7de5b-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="7de5b-161">**Den** – koeficient převodu: 8 hodin</span><span class="sxs-lookup"><span data-stu-id="7de5b-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="7de5b-162">**Týden** – koeficient převodu: 40 hodin</span><span class="sxs-lookup"><span data-stu-id="7de5b-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="7de5b-163">Nastavení ceníku na projektu A:</span><span class="sxs-lookup"><span data-stu-id="7de5b-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="7de5b-164">**Název**: prodejní ceny UK 2016</span><span class="sxs-lookup"><span data-stu-id="7de5b-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="7de5b-165">**Výchozí časová jednotka**: Den</span><span class="sxs-lookup"><span data-stu-id="7de5b-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="7de5b-166">**Měna**: GBP</span><span class="sxs-lookup"><span data-stu-id="7de5b-166">**Currency**: GBP</span></span>

| <span data-ttu-id="7de5b-167">Role</span><span class="sxs-lookup"><span data-stu-id="7de5b-167">Role</span></span>      | <span data-ttu-id="7de5b-168">Skupina jednotek</span><span class="sxs-lookup"><span data-stu-id="7de5b-168">Unit group</span></span> | <span data-ttu-id="7de5b-169">Jednotka</span><span class="sxs-lookup"><span data-stu-id="7de5b-169">Unit</span></span> | <span data-ttu-id="7de5b-170">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="7de5b-170">Organizational unit</span></span> | <span data-ttu-id="7de5b-171">Cena</span><span class="sxs-lookup"><span data-stu-id="7de5b-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="7de5b-172">Vývojář</span><span class="sxs-lookup"><span data-stu-id="7de5b-172">Developer</span></span> | <span data-ttu-id="7de5b-173">Time</span><span class="sxs-lookup"><span data-stu-id="7de5b-173">Time</span></span>       | <span data-ttu-id="7de5b-174">Day</span><span class="sxs-lookup"><span data-stu-id="7de5b-174">Day</span></span>  | <span data-ttu-id="7de5b-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="7de5b-175">Contoso UK</span></span>          | <span data-ttu-id="7de5b-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="7de5b-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="7de5b-177">Časový záznam</span><span class="sxs-lookup"><span data-stu-id="7de5b-177">Time entry</span></span>

<span data-ttu-id="7de5b-178">Následující tabulka zobrazuje výsledné transakce na straně prodeje vytvořené pomocí PSA pro tříhodinový projekt.</span><span class="sxs-lookup"><span data-stu-id="7de5b-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="7de5b-179">Projekt</span><span class="sxs-lookup"><span data-stu-id="7de5b-179">Project</span></span>   | <span data-ttu-id="7de5b-180">Task</span><span class="sxs-lookup"><span data-stu-id="7de5b-180">Task</span></span>    | <span data-ttu-id="7de5b-181">Role</span><span class="sxs-lookup"><span data-stu-id="7de5b-181">Role</span></span>      | <span data-ttu-id="7de5b-182">Množství</span><span class="sxs-lookup"><span data-stu-id="7de5b-182">Quantity</span></span> | <span data-ttu-id="7de5b-183">Jednotka</span><span class="sxs-lookup"><span data-stu-id="7de5b-183">Unit</span></span>  | <span data-ttu-id="7de5b-184">Cena za jednotku</span><span class="sxs-lookup"><span data-stu-id="7de5b-184">Unit price</span></span> | <span data-ttu-id="7de5b-185">Nefakturovaná prodejní částka</span><span class="sxs-lookup"><span data-stu-id="7de5b-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="7de5b-186">Projekt A</span><span class="sxs-lookup"><span data-stu-id="7de5b-186">Project A</span></span> | <span data-ttu-id="7de5b-187">Návrh</span><span class="sxs-lookup"><span data-stu-id="7de5b-187">Design</span></span>  | <span data-ttu-id="7de5b-188">Vývojář</span><span class="sxs-lookup"><span data-stu-id="7de5b-188">Developer</span></span> | <span data-ttu-id="7de5b-189">3</span><span class="sxs-lookup"><span data-stu-id="7de5b-189">3</span></span>        | <span data-ttu-id="7de5b-190">Hour</span><span class="sxs-lookup"><span data-stu-id="7de5b-190">Hour</span></span>  | <span data-ttu-id="7de5b-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="7de5b-191">100 GBP</span></span>    | <span data-ttu-id="7de5b-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="7de5b-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="7de5b-193">Nejčastější dotazy k časové jednotce</span><span class="sxs-lookup"><span data-stu-id="7de5b-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="7de5b-194">Převádí se PSA na různé jednotky v případě výdajů?</span><span class="sxs-lookup"><span data-stu-id="7de5b-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="7de5b-195">Č.</span><span class="sxs-lookup"><span data-stu-id="7de5b-195">No.</span></span> <span data-ttu-id="7de5b-196">Převod jednotek funguje pouze pro čas.</span><span class="sxs-lookup"><span data-stu-id="7de5b-196">Unit conversion works only for time.</span></span> <span data-ttu-id="7de5b-197">V případě výdajů, pokud systém nemůže najít cenu pro kombinaci kategorie výdajů a jednotky, je ve výchozím nastavení cena nastavena na 0,00.</span><span class="sxs-lookup"><span data-stu-id="7de5b-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="7de5b-198">Proč PSA převádí časové jednotky?</span><span class="sxs-lookup"><span data-stu-id="7de5b-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="7de5b-199">V některých zemích nebo oblastech existuje právní požadavek, aby byly fakturační sazby nastaveny ve dnech.</span><span class="sxs-lookup"><span data-stu-id="7de5b-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="7de5b-200">Sjednání ceny a slevy během cyklu nabídky se provádí pomocí denních sazeb pro každou fakturovatelnou roli.</span><span class="sxs-lookup"><span data-stu-id="7de5b-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="7de5b-201">Odhad plánu a časový záznam se provádí v hodinách.</span><span class="sxs-lookup"><span data-stu-id="7de5b-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="7de5b-202">Pro podporu tohoto rozdílu v časových jednotkách převádí PSA časové jednotky.</span><span class="sxs-lookup"><span data-stu-id="7de5b-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="7de5b-203">Lze změnit časové jednotky v odhadech projektu?</span><span class="sxs-lookup"><span data-stu-id="7de5b-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="7de5b-204">Č.</span><span class="sxs-lookup"><span data-stu-id="7de5b-204">No.</span></span> <span data-ttu-id="7de5b-205">Odhad plánu je nyní omezen na hodiny a nelze jej změnit.</span><span class="sxs-lookup"><span data-stu-id="7de5b-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="7de5b-206">Lze jednotky a skupiny jednotek upravit, odstranit a přidat?</span><span class="sxs-lookup"><span data-stu-id="7de5b-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="7de5b-207">Ano.</span><span class="sxs-lookup"><span data-stu-id="7de5b-207">Yes.</span></span> <span data-ttu-id="7de5b-208">S výjimkou skupiny jednotek **Čas** a jednotky **Hodina** lze všechny jednotky odstranit nebo upravit a přidat nové jednotky.</span><span class="sxs-lookup"><span data-stu-id="7de5b-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="7de5b-209">V PSA nelze skupinu jednotek **Čas** a jednotku **Hodina** odstranit.</span><span class="sxs-lookup"><span data-stu-id="7de5b-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="7de5b-210">Lze je však aktualizovat pomocí přeloženého textu pro pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="7de5b-210">However, they can be updated with a translated text for the **Name** field.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]