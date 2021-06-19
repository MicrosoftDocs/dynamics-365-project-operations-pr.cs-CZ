---
title: Přehled skutečných hodnot
description: Toto téma poskytuje informace o skutečných hodnotách projektu.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
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
ms.openlocfilehash: 73f1b14bbb4cc53111a1b3a93756a86db04475ab
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014648"
---
# <a name="actuals-overview"></a><span data-ttu-id="79ee7-103">Přehled skutečných hodnot</span><span class="sxs-lookup"><span data-stu-id="79ee7-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="79ee7-104">Skutečné hodnoty jsou množství práce dokončené v projektu.</span><span class="sxs-lookup"><span data-stu-id="79ee7-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="79ee7-105">Skutečné hodnoty projektu lze sledovat zpět do jejich zdrojových dokumentů.</span><span class="sxs-lookup"><span data-stu-id="79ee7-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="79ee7-106">Tyto zdrojové dokumenty obsahují čas, výdaje, položky deníku a také faktury.</span><span class="sxs-lookup"><span data-stu-id="79ee7-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Způsob sledování skutečných hodnot projektu do zdrojových dokumentů](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="79ee7-108">Odeslání časového záznamu.</span><span class="sxs-lookup"><span data-stu-id="79ee7-108">Submitting a time entry</span></span>

<span data-ttu-id="79ee7-109">V PSA se při odeslání časového záznamu pro projekt, který je namapovaný na řádek smlouvy s časem a materiálem, vytvoří dva řádky deníku.</span><span class="sxs-lookup"><span data-stu-id="79ee7-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="79ee7-110">Jeden řádek je pro náklady a druhý řádek je pro nefakturované prodeje.</span><span class="sxs-lookup"><span data-stu-id="79ee7-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="79ee7-111">Při odeslání časového záznamu pro projekt, který je namapovaný na řádek smlouvy s pevnou cenou, se vytvoří pouze řádek deníku pro náklady.</span><span class="sxs-lookup"><span data-stu-id="79ee7-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="79ee7-112">Logika pro zadávání výchozích cen je umístěna na řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="79ee7-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="79ee7-113">Všechny hodnoty polí z časového záznamu jsou zkopírovány do řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="79ee7-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="79ee7-114">Tato pole obsahují datum transakce, řádek smlouvy, na který je projekt namapován, a výsledek měny v příslušném ceníku.</span><span class="sxs-lookup"><span data-stu-id="79ee7-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="79ee7-115">Pole, která ovlivňují výchozí ceny, jako jsou **Role** a **Organizační jednotka**, způsobí, že ve výchozím nastavení bude do řádku deníku zadána odpovídající cena.</span><span class="sxs-lookup"><span data-stu-id="79ee7-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="79ee7-116">Přidáte-li do časového záznamu vlastní pole a chcete, aby byla hodnota pole přenesena do skutečných hodnot, vytvořte v entitě Skutečnost pole a pomocí mapování polí zkopírujte pole z časového záznamu do skutečného záznamu.</span><span class="sxs-lookup"><span data-stu-id="79ee7-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="79ee7-117">Odeslání výdajové položky</span><span class="sxs-lookup"><span data-stu-id="79ee7-117">Submitting an expense entry</span></span>

<span data-ttu-id="79ee7-118">V PSA se při odeslání výdajové položky pro projekt, který je namapovaný na řádek smlouvy s časem a materiálem, vytvoří dva řádky deníku.</span><span class="sxs-lookup"><span data-stu-id="79ee7-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="79ee7-119">Jeden řádek je pro náklady a druhý řádek je pro nefakturované prodeje.</span><span class="sxs-lookup"><span data-stu-id="79ee7-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="79ee7-120">Při odeslání výdajové položky pro projekt, který je namapovaný na řádek smlouvy s pevnou cenou, se vytvoří pouze řádek deníku pro náklady.</span><span class="sxs-lookup"><span data-stu-id="79ee7-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="79ee7-121">Logika pro zadávání výchozích cen pro výdaje je založena na kategorii výdajů, která je vybrána na stránce **Výdajová položka**.</span><span class="sxs-lookup"><span data-stu-id="79ee7-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="79ee7-122">Datum transakce, řádek smlouvy, na který je projekt namapován, a měna jsou použity k určení příslušného ceníku.</span><span class="sxs-lookup"><span data-stu-id="79ee7-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="79ee7-123">Avšak pro samotnou cenu je částka, kterou uživatel zadal, nastavena přímo na souvisejících výdajových řádcích deníku pro náklady a prodej ve výchozím nastavení.</span><span class="sxs-lookup"><span data-stu-id="79ee7-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="79ee7-124">V aktuální verzi PSA není k dispozici položka založená na kategoriích výchozích jednotkových cen na výdajových položkách.</span><span class="sxs-lookup"><span data-stu-id="79ee7-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="79ee7-125">Použití deníků položek k zaznamenání nákladů</span><span class="sxs-lookup"><span data-stu-id="79ee7-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="79ee7-126">V PSA vám deníky položek umožňují zaznamenávat náklady nebo výnosy do tříd materiálu, poplatků, času, výdajů nebo daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="79ee7-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="79ee7-127">Deník obsahuje hlavičku, řádky a akci **Potvrzení**.</span><span class="sxs-lookup"><span data-stu-id="79ee7-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="79ee7-128">Zde jsou některé scénáře, ve kterých můžete použít deník:</span><span class="sxs-lookup"><span data-stu-id="79ee7-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="79ee7-129">Do projektu je nutné zaznamenat skutečné náklady na materiál a prodej.</span><span class="sxs-lookup"><span data-stu-id="79ee7-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="79ee7-130">Skutečné hodnoty transakcí z jiného systému je nutné přesunout na PSA.</span><span class="sxs-lookup"><span data-stu-id="79ee7-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="79ee7-131">Je nutné zaznamenat náklady, které se vyskytly v jiném systému, například náklady na nákup nebo subdodavatele.</span><span class="sxs-lookup"><span data-stu-id="79ee7-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="79ee7-132">Používání deníků položek k vytváření skutečných hodnot by měl provádět pouze uživatel, který si je plně vědom účetního dopadu skutečných hodnot na projekt.</span><span class="sxs-lookup"><span data-stu-id="79ee7-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="79ee7-133">Důvodem je, že aplikace neověřuje typ řádku deníku nebo související ceny, které jsou zadány na řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="79ee7-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="79ee7-134">Vzhledem k dopadům tohoto typu deníku věnujte dostatečnou pozornost tomu, komu je povolen přístup k tvorbě vstupních časopisů.</span><span class="sxs-lookup"><span data-stu-id="79ee7-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="79ee7-135">Záznam skutečných hodnot na základě událostí projektu</span><span class="sxs-lookup"><span data-stu-id="79ee7-135">Recording actuals based on project events</span></span>

<span data-ttu-id="79ee7-136">PSA zaznamenává finanční transakce, které nastanou během projektu.</span><span class="sxs-lookup"><span data-stu-id="79ee7-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="79ee7-137">Tyto transakce jsou zaznamenány jako **skutečné hodnoty**.</span><span class="sxs-lookup"><span data-stu-id="79ee7-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="79ee7-138">V následujících tabulkách jsou zobrazeny různé typy skutečných hodnot, které jsou vytvořeny v závislosti na tom, zda je projekt časově materiálovým projektem nebo projektem s pevnou cenou, je v předprodejní fázi nebo jde o interní projekt.</span><span class="sxs-lookup"><span data-stu-id="79ee7-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="79ee7-139">**Zdroj patří do stejné organizační jednotky jako smluvní jednotka projektu**</span><span class="sxs-lookup"><span data-stu-id="79ee7-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="79ee7-140">Událost</span><span class="sxs-lookup"><span data-stu-id="79ee7-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="79ee7-141">Fakturovatelný nebo prodaný projekt</span><span class="sxs-lookup"><span data-stu-id="79ee7-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="79ee7-142">Projekt v předprodejní fázi</span><span class="sxs-lookup"><span data-stu-id="79ee7-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="79ee7-143">Interní projekt</span><span class="sxs-lookup"><span data-stu-id="79ee7-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="79ee7-144">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="79ee7-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="79ee7-145">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="79ee7-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="79ee7-146">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="79ee7-146">Actuals</span></span></th>
<th><span data-ttu-id="79ee7-147">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="79ee7-147">Transaction currency</span></span></th>
<th><span data-ttu-id="79ee7-148">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="79ee7-148">Fixed price</span></span></th>
<th><span data-ttu-id="79ee7-149">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="79ee7-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79ee7-150">Je vytvořen časový záznam,</span><span class="sxs-lookup"><span data-stu-id="79ee7-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="79ee7-151">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="79ee7-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-152">Je odeslán časový záznam.</span><span class="sxs-lookup"><span data-stu-id="79ee7-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="79ee7-153">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="79ee7-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="79ee7-154">Čas je schválen a během schvalování nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="79ee7-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="79ee7-155">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-155">Cost actual</span></span></td>
<td><span data-ttu-id="79ee7-156">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="79ee7-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="79ee7-157">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="79ee7-158">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="79ee7-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="79ee7-159">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="79ee7-160">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-161">Nefakturované skutečné prodeje – účtovatelné</span><span class="sxs-lookup"><span data-stu-id="79ee7-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="79ee7-162">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="79ee7-163">Čas je schválen a během schvalování dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="79ee7-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="79ee7-164">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-164">Cost actual</span></span></td>
<td><span data-ttu-id="79ee7-165">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="79ee7-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="79ee7-166">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="79ee7-167">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="79ee7-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="79ee7-168">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="79ee7-169">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-170">Skutečný nefakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="79ee7-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="79ee7-171">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-172">Skutečný nefakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="79ee7-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="79ee7-173">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="79ee7-174">Faktura je potvrzena a nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="79ee7-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="79ee7-175">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="79ee7-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="79ee7-176">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="79ee7-177">Fakturovaný prodej pro milník</span><span class="sxs-lookup"><span data-stu-id="79ee7-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="79ee7-178">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="79ee7-179">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="79ee7-180">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-181">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="79ee7-181">Billed sales</span></span></td>
<td><span data-ttu-id="79ee7-182">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="79ee7-183">Faktura je potvrzena a dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="79ee7-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="79ee7-184">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="79ee7-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="79ee7-185">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="79ee7-186">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="79ee7-187">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="79ee7-188">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="79ee7-189">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-190">Fakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="79ee7-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="79ee7-191">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-192">Fakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="79ee7-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="79ee7-193">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="79ee7-194">Faktura je opravena za účelem zvýšení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="79ee7-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="79ee7-195">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="79ee7-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="79ee7-196">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="79ee7-197">Storno fakturovaného prodeje pro milník</span><span class="sxs-lookup"><span data-stu-id="79ee7-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="79ee7-198">Změna stavu milníku z <strong>fakturováno</strong> na <strong>Připraveno pro fakturu</strong></span><span class="sxs-lookup"><span data-stu-id="79ee7-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="79ee7-199">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="79ee7-200">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="79ee7-201">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-202">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="79ee7-202">Billed sales</span></span></td>
<td><span data-ttu-id="79ee7-203">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="79ee7-204">Faktura je opravena za účelem snížení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="79ee7-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="79ee7-205">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="79ee7-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="79ee7-206">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-207">Fakturovaný prodej pro nové množství</span><span class="sxs-lookup"><span data-stu-id="79ee7-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="79ee7-208">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-209">Nefakturovaný prodej – účtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="79ee7-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="79ee7-210">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79ee7-211">**Zdroj patří do organizační jednotky, která se liší od smluvní jednotky projektu**</span><span class="sxs-lookup"><span data-stu-id="79ee7-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="79ee7-212">Událost</span><span class="sxs-lookup"><span data-stu-id="79ee7-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="79ee7-213">Fakturovatelný nebo prodaný projekt</span><span class="sxs-lookup"><span data-stu-id="79ee7-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="79ee7-214">Projekt v předprodejní fázi</span><span class="sxs-lookup"><span data-stu-id="79ee7-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="79ee7-215">Interní projekt</span><span class="sxs-lookup"><span data-stu-id="79ee7-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="79ee7-216">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="79ee7-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="79ee7-217">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="79ee7-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="79ee7-218">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="79ee7-218">Actuals</span></span></th>
<th><span data-ttu-id="79ee7-219">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="79ee7-219">Transaction currency</span></span></th>
<th><span data-ttu-id="79ee7-220">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="79ee7-220">Fixed price</span></span></th>
<th><span data-ttu-id="79ee7-221">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="79ee7-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79ee7-222">Je vytvořen časový záznam,</span><span class="sxs-lookup"><span data-stu-id="79ee7-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="79ee7-223">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="79ee7-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-224">Je odeslán časový záznam.</span><span class="sxs-lookup"><span data-stu-id="79ee7-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="79ee7-225">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="79ee7-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="79ee7-226">Čas je schválen a během schvalování nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="79ee7-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="79ee7-227">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-227">Cost actual</span></span></td>
<td><span data-ttu-id="79ee7-228">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="79ee7-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="79ee7-229">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="79ee7-230">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="79ee7-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="79ee7-231">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="79ee7-232">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-233">Nefakturované skutečné prodeje – účtovatelné</span><span class="sxs-lookup"><span data-stu-id="79ee7-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="79ee7-234">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-235">Jednotkové náklady zdroje</span><span class="sxs-lookup"><span data-stu-id="79ee7-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="79ee7-236">Měna jednotky zdroje</span><span class="sxs-lookup"><span data-stu-id="79ee7-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-237">Vnitropodnikový prodej</span><span class="sxs-lookup"><span data-stu-id="79ee7-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="79ee7-238">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="79ee7-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="79ee7-239">Čas je schválen a během schvalování dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="79ee7-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="79ee7-240">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-240">Cost actual</span></span></td>
<td><span data-ttu-id="79ee7-241">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="79ee7-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="79ee7-242">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="79ee7-243">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="79ee7-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="79ee7-244">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="79ee7-245">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="79ee7-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-246">Jednotkové náklady zdroje</span><span class="sxs-lookup"><span data-stu-id="79ee7-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="79ee7-247">Měna jednotky zdroje</span><span class="sxs-lookup"><span data-stu-id="79ee7-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-248">Vnitropodnikový prodej</span><span class="sxs-lookup"><span data-stu-id="79ee7-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="79ee7-249">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="79ee7-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-250">Skutečný nefakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="79ee7-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="79ee7-251">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-252">Skutečný nefakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="79ee7-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="79ee7-253">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="79ee7-254">Faktura je potvrzena a nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="79ee7-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="79ee7-255">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="79ee7-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="79ee7-256">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="79ee7-257">Fakturovaný prodej pro milník</span><span class="sxs-lookup"><span data-stu-id="79ee7-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="79ee7-258">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="79ee7-259">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="79ee7-260">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-261">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="79ee7-261">Billed sales</span></span></td>
<td><span data-ttu-id="79ee7-262">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="79ee7-263">Faktura je potvrzena a dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="79ee7-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="79ee7-264">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="79ee7-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="79ee7-265">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="79ee7-266">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="79ee7-267">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="79ee7-268">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="79ee7-269">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-270">Fakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="79ee7-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="79ee7-271">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-272">Fakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="79ee7-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="79ee7-273">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="79ee7-274">Faktura je opravena za účelem zvýšení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="79ee7-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="79ee7-275">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="79ee7-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="79ee7-276">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="79ee7-277">Storno fakturovaného prodeje pro milník</span><span class="sxs-lookup"><span data-stu-id="79ee7-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="79ee7-278">Změna stavu milníku z <strong>fakturováno</strong> na <strong>Připraveno pro fakturu</strong></span><span class="sxs-lookup"><span data-stu-id="79ee7-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="79ee7-279">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="79ee7-280">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="79ee7-281">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="79ee7-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-282">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="79ee7-282">Billed sales</span></span></td>
<td><span data-ttu-id="79ee7-283">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="79ee7-284">Faktura je opravena za účelem snížení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="79ee7-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="79ee7-285">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="79ee7-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="79ee7-286">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-287">Fakturovaný prodej pro nové množství</span><span class="sxs-lookup"><span data-stu-id="79ee7-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="79ee7-288">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79ee7-289">Nefakturovaný prodej – účtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="79ee7-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="79ee7-290">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="79ee7-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]