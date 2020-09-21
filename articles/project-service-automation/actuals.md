---
title: Skutečnost
description: Toto téma poskytuje informace o skutečných hodnotách projektu.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750397"
---
# <a name="actuals"></a><span data-ttu-id="c6279-103">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="c6279-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c6279-104">Skutečné hodnoty jsou množství práce dokončené v projektu.</span><span class="sxs-lookup"><span data-stu-id="c6279-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="c6279-105">Skutečné hodnoty projektu lze sledovat zpět do jejich zdrojových dokumentů.</span><span class="sxs-lookup"><span data-stu-id="c6279-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="c6279-106">Tyto zdrojové dokumenty obsahují čas, výdaje, položky deníku a také faktury.</span><span class="sxs-lookup"><span data-stu-id="c6279-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Způsob sledování skutečných hodnot projektu do zdrojových dokumentů](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="c6279-108">Odeslání časového záznamu.</span><span class="sxs-lookup"><span data-stu-id="c6279-108">Submitting a time entry</span></span>

<span data-ttu-id="c6279-109">V PSA se při odeslání časového záznamu pro projekt, který je namapovaný na řádek smlouvy s časem a materiálem, vytvoří dva řádky deníku.</span><span class="sxs-lookup"><span data-stu-id="c6279-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="c6279-110">Jeden řádek je pro náklady a druhý řádek je pro nefakturované prodeje.</span><span class="sxs-lookup"><span data-stu-id="c6279-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="c6279-111">Při odeslání časového záznamu pro projekt, který je namapovaný na řádek smlouvy s pevnou cenou, se vytvoří pouze řádek deníku pro náklady.</span><span class="sxs-lookup"><span data-stu-id="c6279-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="c6279-112">Logika pro zadávání výchozích cen je umístěna na řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="c6279-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="c6279-113">Všechny hodnoty polí z časového záznamu jsou zkopírovány do řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="c6279-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="c6279-114">Tato pole obsahují datum transakce, řádek smlouvy, na který je projekt namapován, a výsledek měny v příslušném ceníku.</span><span class="sxs-lookup"><span data-stu-id="c6279-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="c6279-115">Pole, která ovlivňují výchozí ceny, jako jsou **Role** a **Organizační jednotka**, způsobí, že ve výchozím nastavení bude do řádku deníku zadána odpovídající cena.</span><span class="sxs-lookup"><span data-stu-id="c6279-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="c6279-116">Přidáte-li do časového záznamu vlastní pole a chcete, aby byla hodnota pole přenesena do skutečných hodnot, vytvořte v entitě Skutečnost pole a pomocí mapování polí zkopírujte pole z časového záznamu do skutečného záznamu.</span><span class="sxs-lookup"><span data-stu-id="c6279-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="c6279-117">Odeslání výdajové položky</span><span class="sxs-lookup"><span data-stu-id="c6279-117">Submitting an expense entry</span></span>

<span data-ttu-id="c6279-118">V PSA se při odeslání výdajové položky pro projekt, který je namapovaný na řádek smlouvy s časem a materiálem, vytvoří dva řádky deníku.</span><span class="sxs-lookup"><span data-stu-id="c6279-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="c6279-119">Jeden řádek je pro náklady a druhý řádek je pro nefakturované prodeje.</span><span class="sxs-lookup"><span data-stu-id="c6279-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="c6279-120">Při odeslání výdajové položky pro projekt, který je namapovaný na řádek smlouvy s pevnou cenou, se vytvoří pouze řádek deníku pro náklady.</span><span class="sxs-lookup"><span data-stu-id="c6279-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="c6279-121">Logika pro zadávání výchozích cen pro výdaje je založena na kategorii výdajů, která je vybrána na stránce **Výdajová položka**.</span><span class="sxs-lookup"><span data-stu-id="c6279-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="c6279-122">Datum transakce, řádek smlouvy, na který je projekt namapován, a měna jsou použity k určení příslušného ceníku.</span><span class="sxs-lookup"><span data-stu-id="c6279-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="c6279-123">Avšak pro samotnou cenu je částka, kterou uživatel zadal, nastavena přímo na souvisejících výdajových řádcích deníku pro náklady a prodej ve výchozím nastavení.</span><span class="sxs-lookup"><span data-stu-id="c6279-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="c6279-124">V aktuální verzi PSA není k dispozici položka založená na kategoriích výchozích jednotkových cen na výdajových položkách.</span><span class="sxs-lookup"><span data-stu-id="c6279-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="c6279-125">Použití deníků k zaznamenání nákladů</span><span class="sxs-lookup"><span data-stu-id="c6279-125">Using journals to record costs</span></span>

<span data-ttu-id="c6279-126">V PSA vám deníky umožňují zaznamenávat náklady nebo výnosy do tříd materiálu, poplatků, času, výdajů nebo daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="c6279-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="c6279-127">Deník obsahuje hlavičku, řádky a akci **Potvrzení**.</span><span class="sxs-lookup"><span data-stu-id="c6279-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="c6279-128">Zde jsou některé scénáře, ve kterých můžete použít deník:</span><span class="sxs-lookup"><span data-stu-id="c6279-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="c6279-129">Do projektu je nutné zaznamenat skutečné náklady na materiál a prodej.</span><span class="sxs-lookup"><span data-stu-id="c6279-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="c6279-130">Skutečné hodnoty transakcí z jiného systému je nutné přesunout na PSA.</span><span class="sxs-lookup"><span data-stu-id="c6279-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="c6279-131">Je nutné zaznamenat náklady, které se vyskytly v jiném systému, například náklady na nákup nebo subdodavatele.</span><span class="sxs-lookup"><span data-stu-id="c6279-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="c6279-132">Záznam skutečných hodnot na základě událostí projektu</span><span class="sxs-lookup"><span data-stu-id="c6279-132">Recording actuals based on project events</span></span>

<span data-ttu-id="c6279-133">PSA zaznamenává finanční transakce, které nastanou během projektu.</span><span class="sxs-lookup"><span data-stu-id="c6279-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="c6279-134">Tyto transakce jsou zaznamenány jako **skutečné hodnoty**.</span><span class="sxs-lookup"><span data-stu-id="c6279-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="c6279-135">V následujících tabulkách jsou zobrazeny různé typy skutečných hodnot, které jsou vytvořeny v závislosti na tom, zda je projekt časově materiálovým projektem nebo projektem s pevnou cenou, je v předprodejní fázi nebo jde o interní projekt.</span><span class="sxs-lookup"><span data-stu-id="c6279-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="c6279-136">**Zdroj patří do stejné organizační jednotky jako smluvní jednotka projektu**</span><span class="sxs-lookup"><span data-stu-id="c6279-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="c6279-137">Událost</span><span class="sxs-lookup"><span data-stu-id="c6279-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="c6279-138">Fakturovatelný nebo prodaný projekt</span><span class="sxs-lookup"><span data-stu-id="c6279-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="c6279-139">Projekt v předprodejní fázi</span><span class="sxs-lookup"><span data-stu-id="c6279-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="c6279-140">Interní projekt</span><span class="sxs-lookup"><span data-stu-id="c6279-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="c6279-141">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="c6279-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="c6279-142">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="c6279-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c6279-143">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="c6279-143">Actuals</span></span></th>
<th><span data-ttu-id="c6279-144">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="c6279-144">Transaction currency</span></span></th>
<th><span data-ttu-id="c6279-145">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="c6279-145">Fixed price</span></span></th>
<th><span data-ttu-id="c6279-146">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="c6279-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6279-147">Je vytvořen časový záznam,</span><span class="sxs-lookup"><span data-stu-id="c6279-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="c6279-148">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="c6279-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-149">Je odeslán časový záznam.</span><span class="sxs-lookup"><span data-stu-id="c6279-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="c6279-150">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="c6279-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c6279-151">Čas je schválen a během schvalování nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="c6279-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c6279-152">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-152">Cost actual</span></span></td>
<td><span data-ttu-id="c6279-153">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="c6279-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c6279-154">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="c6279-155">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="c6279-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="c6279-156">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="c6279-157">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-158">Nefakturované skutečné prodeje – účtovatelné</span><span class="sxs-lookup"><span data-stu-id="c6279-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="c6279-159">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c6279-160">Čas je schválen a během schvalování dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="c6279-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c6279-161">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-161">Cost actual</span></span></td>
<td><span data-ttu-id="c6279-162">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="c6279-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c6279-163">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="c6279-164">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="c6279-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c6279-165">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="c6279-166">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-167">Skutečný nefakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="c6279-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c6279-168">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-169">Skutečný nefakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="c6279-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c6279-170">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c6279-171">Faktura je potvrzena a nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="c6279-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c6279-172">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="c6279-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c6279-173">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c6279-174">Fakturovaný prodej pro milník</span><span class="sxs-lookup"><span data-stu-id="c6279-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="c6279-175">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c6279-176">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="c6279-177">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-178">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="c6279-178">Billed sales</span></span></td>
<td><span data-ttu-id="c6279-179">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c6279-180">Faktura je potvrzena a dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="c6279-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c6279-181">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="c6279-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c6279-182">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c6279-183">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c6279-184">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c6279-185">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c6279-186">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-187">Fakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="c6279-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c6279-188">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-189">Fakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="c6279-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c6279-190">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c6279-191">Faktura je opravena za účelem zvýšení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="c6279-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c6279-192">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="c6279-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c6279-193">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="c6279-194">Storno fakturovaného prodeje pro milník</span><span class="sxs-lookup"><span data-stu-id="c6279-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="c6279-195">Změna stavu milníku z <strong>fakturováno</strong> na <strong>Připraveno pro fakturu</strong></span><span class="sxs-lookup"><span data-stu-id="c6279-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="c6279-196">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c6279-197">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="c6279-198">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-199">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="c6279-199">Billed sales</span></span></td>
<td><span data-ttu-id="c6279-200">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c6279-201">Faktura je opravena za účelem snížení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="c6279-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c6279-202">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="c6279-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c6279-203">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-204">Fakturovaný prodej pro nové množství</span><span class="sxs-lookup"><span data-stu-id="c6279-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="c6279-205">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-206">Nefakturovaný prodej – účtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="c6279-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="c6279-207">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c6279-208">**Zdroj patří do organizační jednotky, která se liší od smluvní jednotky projektu**</span><span class="sxs-lookup"><span data-stu-id="c6279-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="c6279-209">Událost</span><span class="sxs-lookup"><span data-stu-id="c6279-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="c6279-210">Fakturovatelný nebo prodaný projekt</span><span class="sxs-lookup"><span data-stu-id="c6279-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="c6279-211">Projekt v předprodejní fázi</span><span class="sxs-lookup"><span data-stu-id="c6279-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="c6279-212">Interní projekt</span><span class="sxs-lookup"><span data-stu-id="c6279-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="c6279-213">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="c6279-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="c6279-214">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="c6279-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c6279-215">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="c6279-215">Actuals</span></span></th>
<th><span data-ttu-id="c6279-216">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="c6279-216">Transaction currency</span></span></th>
<th><span data-ttu-id="c6279-217">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="c6279-217">Fixed price</span></span></th>
<th><span data-ttu-id="c6279-218">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="c6279-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c6279-219">Je vytvořen časový záznam,</span><span class="sxs-lookup"><span data-stu-id="c6279-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="c6279-220">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="c6279-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-221">Je odeslán časový záznam.</span><span class="sxs-lookup"><span data-stu-id="c6279-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="c6279-222">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="c6279-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="c6279-223">Čas je schválen a během schvalování nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="c6279-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c6279-224">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-224">Cost actual</span></span></td>
<td><span data-ttu-id="c6279-225">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="c6279-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="c6279-226">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="c6279-227">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="c6279-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="c6279-228">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="c6279-229">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-230">Nefakturované skutečné prodeje – účtovatelné</span><span class="sxs-lookup"><span data-stu-id="c6279-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="c6279-231">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-232">Jednotkové náklady zdroje</span><span class="sxs-lookup"><span data-stu-id="c6279-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="c6279-233">Měna jednotky zdroje</span><span class="sxs-lookup"><span data-stu-id="c6279-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-234">Vnitropodnikový prodej</span><span class="sxs-lookup"><span data-stu-id="c6279-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="c6279-235">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="c6279-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="c6279-236">Čas je schválen a během schvalování dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="c6279-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c6279-237">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-237">Cost actual</span></span></td>
<td><span data-ttu-id="c6279-238">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="c6279-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c6279-239">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="c6279-240">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="c6279-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c6279-241">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="c6279-242">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="c6279-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-243">Jednotkové náklady zdroje</span><span class="sxs-lookup"><span data-stu-id="c6279-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="c6279-244">Měna jednotky zdroje</span><span class="sxs-lookup"><span data-stu-id="c6279-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-245">Vnitropodnikový prodej</span><span class="sxs-lookup"><span data-stu-id="c6279-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="c6279-246">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="c6279-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-247">Skutečný nefakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="c6279-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c6279-248">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-249">Skutečný nefakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="c6279-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c6279-250">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c6279-251">Faktura je potvrzena a nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="c6279-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c6279-252">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="c6279-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c6279-253">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c6279-254">Fakturovaný prodej pro milník</span><span class="sxs-lookup"><span data-stu-id="c6279-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="c6279-255">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c6279-256">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="c6279-257">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-258">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="c6279-258">Billed sales</span></span></td>
<td><span data-ttu-id="c6279-259">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c6279-260">Faktura je potvrzena a dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="c6279-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c6279-261">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="c6279-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c6279-262">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c6279-263">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c6279-264">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c6279-265">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c6279-266">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-267">Fakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="c6279-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c6279-268">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-269">Fakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="c6279-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c6279-270">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c6279-271">Faktura je opravena za účelem zvýšení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="c6279-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c6279-272">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="c6279-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c6279-273">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="c6279-274">Storno fakturovaného prodeje pro milník</span><span class="sxs-lookup"><span data-stu-id="c6279-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="c6279-275">Změna stavu milníku z <strong>fakturováno</strong> na <strong>Připraveno pro fakturu</strong></span><span class="sxs-lookup"><span data-stu-id="c6279-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="c6279-276">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c6279-277">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="c6279-278">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c6279-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-279">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="c6279-279">Billed sales</span></span></td>
<td><span data-ttu-id="c6279-280">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c6279-281">Faktura je opravena za účelem snížení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="c6279-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c6279-282">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="c6279-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c6279-283">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-284">Fakturovaný prodej pro nové množství</span><span class="sxs-lookup"><span data-stu-id="c6279-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="c6279-285">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c6279-286">Nefakturovaný prodej – účtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="c6279-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="c6279-287">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="c6279-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
