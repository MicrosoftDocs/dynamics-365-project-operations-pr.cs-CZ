---
title: Skutečné hodnoty
description: Tento téma poskytuje informace o práci se skutečnými hodnotami v Microsoft Dynamics 365 Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073770"
---
# <a name="actuals"></a><span data-ttu-id="04ca9-103">Skutečné hodnoty</span><span class="sxs-lookup"><span data-stu-id="04ca9-103">Actuals</span></span> 

<span data-ttu-id="04ca9-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="04ca9-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="04ca9-105">Skutečné hodnoty jsou množství práce dokončené v projektu.</span><span class="sxs-lookup"><span data-stu-id="04ca9-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="04ca9-106">Jsou vytvářeny jako výsledek časových a výdajových záznamů, záznamů deníku a faktur.</span><span class="sxs-lookup"><span data-stu-id="04ca9-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="04ca9-107">Řádky deníku a časové záznamy</span><span class="sxs-lookup"><span data-stu-id="04ca9-107">Journal lines and time submission</span></span>

<span data-ttu-id="04ca9-108">Další informace o časových záznamech najdete v části [Přehled časových záznamů](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="04ca9-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="04ca9-109">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="04ca9-109">Time and materials</span></span>

<span data-ttu-id="04ca9-110">Když je zadaný časový údaj propojen s projektem, který je namapován na řádek kontraktu času a materiálů, systém vytvoří dva řádky deníku, jeden pro náklady a druhý pro nevyfakturované prodeje.</span><span class="sxs-lookup"><span data-stu-id="04ca9-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="04ca9-111">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="04ca9-111">Fixed price</span></span>

<span data-ttu-id="04ca9-112">Při odeslání časového záznamu propojeného s projektem, který je namapovaný na řádek smlouvy s pevnou cenou, systém vytvoří jeden řádek deníku pro náklady.</span><span class="sxs-lookup"><span data-stu-id="04ca9-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="04ca9-113">Výchozí cena</span><span class="sxs-lookup"><span data-stu-id="04ca9-113">Default pricing</span></span>

<span data-ttu-id="04ca9-114">Logika pro vytváření výchozích cen je umístěna na řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="04ca9-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="04ca9-115">Hodnoty polí z časového záznamu jsou zkopírovány do řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="04ca9-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="04ca9-116">Tyto hodnoty obsahují datum transakce, řádek smlouvy, na který je projekt namapován, a výsledek měny v příslušném ceníku.</span><span class="sxs-lookup"><span data-stu-id="04ca9-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="04ca9-117">Pole, která ovlivňují výchozí ceny, jako jsou **Role** a **Organizační jednotka** se používají k tomu, aby byla do řádku deníku zadána odpovídající cena.</span><span class="sxs-lookup"><span data-stu-id="04ca9-117">The fields that affect default pricing, such as **Role** and **Org Unit** , are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="04ca9-118">K časovému záznamu můžete přidat vlastní pole.</span><span class="sxs-lookup"><span data-stu-id="04ca9-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="04ca9-119">Pokud chcete, aby byla hodnota pole přenesena do skutečných hodnot, vytvořte v entitě Skutečnost pole a pomocí mapování polí zkopírujte pole z časového záznamu do skutečného záznamu.</span><span class="sxs-lookup"><span data-stu-id="04ca9-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="04ca9-120">Řádky deníku a zadávání základních výdajů</span><span class="sxs-lookup"><span data-stu-id="04ca9-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="04ca9-121">Další informace o záznamech o výdajích najdete v části [Přehled výdajů](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="04ca9-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="04ca9-122">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="04ca9-122">Time and materials</span></span>

<span data-ttu-id="04ca9-123">Když je zadaný záznam základního výdaje propojen s projektem, který je namapován na řádek kontraktu času a materiálů, systém vytvoří dva řádky deníku, jeden pro náklady a druhý pro nevyfakturované prodeje.</span><span class="sxs-lookup"><span data-stu-id="04ca9-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="04ca9-124">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="04ca9-124">Fixed price</span></span>

<span data-ttu-id="04ca9-125">Při odeslání základního záznamu o výdajích propojeného s projektem, který je namapovaný na řádek smlouvy s pevnou cenou, systém vytvoří jeden řádek deníku pro náklady.</span><span class="sxs-lookup"><span data-stu-id="04ca9-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="04ca9-126">Výchozí cena</span><span class="sxs-lookup"><span data-stu-id="04ca9-126">Default pricing</span></span>

<span data-ttu-id="04ca9-127">Logika pro zadávání výchozích cen výdajů je založena na kategorii výdajů.</span><span class="sxs-lookup"><span data-stu-id="04ca9-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="04ca9-128">Datum transakce, řádek smlouvy, na který je projekt namapován, a měna jsou použity k určení příslušného ceníku.</span><span class="sxs-lookup"><span data-stu-id="04ca9-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="04ca9-129">Avšak ve výchozím nastavení je zadaná částka pro samotnou cenu nastavena přímo na souvisejících výdajových řádcích deníku pro náklady a prodej ve výchozím nastavení.</span><span class="sxs-lookup"><span data-stu-id="04ca9-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="04ca9-130">Položka založená na kategoriích výchozích jednotkových cen na výdajových položkách.</span><span class="sxs-lookup"><span data-stu-id="04ca9-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="04ca9-131">Použití deníků k zaznamenání nákladů</span><span class="sxs-lookup"><span data-stu-id="04ca9-131">Use entry journals to record costs</span></span>

<span data-ttu-id="04ca9-132">Deníky záznamů můžete použít a zaznamenávat náklady nebo výnosy do tříd materiálu, poplatků, času, výdajů nebo daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="04ca9-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="04ca9-133">Deníky lze použít k následujícím účelům:</span><span class="sxs-lookup"><span data-stu-id="04ca9-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="04ca9-134">Záznam skutečných nákladů na materiál a prodej projektu.</span><span class="sxs-lookup"><span data-stu-id="04ca9-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="04ca9-135">Přesunout dkutečné hodnoty transakcí z jiného systému do Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="04ca9-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="04ca9-136">Zaznamenejte náklady, ke kterým došlo v jiném systému.</span><span class="sxs-lookup"><span data-stu-id="04ca9-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="04ca9-137">Tyto náklady mohou zahrnovat náklady na pořízení nebo subdodávky.</span><span class="sxs-lookup"><span data-stu-id="04ca9-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04ca9-138">Aplikace neověřuje typ řádku deníku ani související ceny, které jsou zadány na řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="04ca9-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="04ca9-139">Proto by měl k vytváření skutečných hodnot používat deníky pouze uživatel, který si je plně vědom účetního dopadu skutečných hodnot na projekt.</span><span class="sxs-lookup"><span data-stu-id="04ca9-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="04ca9-140">Z důvodu dopadu tohoto typu deníku byste měli pečlivě zvolit, kdo má přístup k vytváření deníků záznamů.</span><span class="sxs-lookup"><span data-stu-id="04ca9-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="04ca9-141">Záznam skutečných hodnot na základě událostí projektu</span><span class="sxs-lookup"><span data-stu-id="04ca9-141">Record actuals based on project events</span></span>

<span data-ttu-id="04ca9-142">Project Operations zaznamenává finanční transakce, které nastanou během projektu.</span><span class="sxs-lookup"><span data-stu-id="04ca9-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="04ca9-143">Tyto transakce jsou zaznamenány jako skutečné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="04ca9-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="04ca9-144">V následujících tabulkách jsou zobrazeny různé typy skutečných hodnot, které jsou vytvořeny v závislosti na tom, zda je projekt časově materiálovým projektem nebo projektem s pevnou cenou, je v předprodejní fázi nebo jde o interní projekt.</span><span class="sxs-lookup"><span data-stu-id="04ca9-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="04ca9-145">Zdroj patří do stejné organizační jednotky jako smluvní jednotka projektu</span><span class="sxs-lookup"><span data-stu-id="04ca9-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="04ca9-146">Událost</span><span class="sxs-lookup"><span data-stu-id="04ca9-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="04ca9-147">Fakturovatelný nebo prodaný projekt</span><span class="sxs-lookup"><span data-stu-id="04ca9-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="04ca9-148">Projekt v předprodejní fázi</span><span class="sxs-lookup"><span data-stu-id="04ca9-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="04ca9-149">Interní projekt</span><span class="sxs-lookup"><span data-stu-id="04ca9-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="04ca9-150">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="04ca9-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="04ca9-151">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="04ca9-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="04ca9-152">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="04ca9-152">Actuals</span></span></th>
<th><span data-ttu-id="04ca9-153">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="04ca9-153">Transaction currency</span></span></th>
<th><span data-ttu-id="04ca9-154">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="04ca9-154">Fixed price</span></span></th>
<th><span data-ttu-id="04ca9-155">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="04ca9-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04ca9-156">Je vytvořen časový záznam,</span><span class="sxs-lookup"><span data-stu-id="04ca9-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="04ca9-157">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="04ca9-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-158">Je odeslán časový záznam.</span><span class="sxs-lookup"><span data-stu-id="04ca9-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="04ca9-159">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="04ca9-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="04ca9-160">Čas je schválen a během schvalování nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="04ca9-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="04ca9-161">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-161">Cost actual</span></span></td>
<td><span data-ttu-id="04ca9-162">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="04ca9-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="04ca9-163">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="04ca9-164">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="04ca9-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="04ca9-165">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="04ca9-166">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-167">Nefakturované skutečné prodeje – účtovatelné</span><span class="sxs-lookup"><span data-stu-id="04ca9-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="04ca9-168">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="04ca9-169">Čas je schválen a během schvalování dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="04ca9-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="04ca9-170">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-170">Cost actual</span></span></td>
<td><span data-ttu-id="04ca9-171">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="04ca9-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="04ca9-172">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="04ca9-173">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="04ca9-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="04ca9-174">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="04ca9-175">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-176">Skutečný nefakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="04ca9-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="04ca9-177">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-178">Skutečný nefakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="04ca9-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="04ca9-179">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="04ca9-180">Faktura je potvrzena a nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="04ca9-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="04ca9-181">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="04ca9-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="04ca9-182">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="04ca9-183">Fakturovaný prodej pro milník</span><span class="sxs-lookup"><span data-stu-id="04ca9-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="04ca9-184">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="04ca9-185">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="04ca9-186">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-187">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="04ca9-187">Billed sales</span></span></td>
<td><span data-ttu-id="04ca9-188">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="04ca9-189">Faktura je potvrzena a dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="04ca9-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="04ca9-190">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="04ca9-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="04ca9-191">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="04ca9-192">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="04ca9-193">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="04ca9-194">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="04ca9-195">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-196">Fakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="04ca9-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="04ca9-197">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-198">Fakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="04ca9-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="04ca9-199">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="04ca9-200">Faktura je opravena za účelem zvýšení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="04ca9-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="04ca9-201">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="04ca9-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="04ca9-202">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="04ca9-203">Storno fakturovaného prodeje pro milník</span><span class="sxs-lookup"><span data-stu-id="04ca9-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="04ca9-204">Změna stavu milníku z <strong>fakturováno</strong> na <strong>Připraveno pro fakturu</strong></span><span class="sxs-lookup"><span data-stu-id="04ca9-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="04ca9-205">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="04ca9-206">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="04ca9-207">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-208">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="04ca9-208">Billed sales</span></span></td>
<td><span data-ttu-id="04ca9-209">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="04ca9-210">Faktura je opravena za účelem snížení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="04ca9-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="04ca9-211">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="04ca9-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="04ca9-212">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-213">Fakturovaný prodej pro nové množství</span><span class="sxs-lookup"><span data-stu-id="04ca9-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="04ca9-214">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-215">Nefakturovaný prodej – účtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="04ca9-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="04ca9-216">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="04ca9-217">Zdroj patří do organizační jednotky, která se liší od smluvní jednotky projektu</span><span class="sxs-lookup"><span data-stu-id="04ca9-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="04ca9-218">Událost</span><span class="sxs-lookup"><span data-stu-id="04ca9-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="04ca9-219">Fakturovatelný nebo prodaný projekt</span><span class="sxs-lookup"><span data-stu-id="04ca9-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="04ca9-220">Projekt v předprodejní fázi</span><span class="sxs-lookup"><span data-stu-id="04ca9-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="04ca9-221">Interní projekt</span><span class="sxs-lookup"><span data-stu-id="04ca9-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="04ca9-222">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="04ca9-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="04ca9-223">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="04ca9-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="04ca9-224">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="04ca9-224">Actuals</span></span></th>
<th><span data-ttu-id="04ca9-225">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="04ca9-225">Transaction currency</span></span></th>
<th><span data-ttu-id="04ca9-226">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="04ca9-226">Fixed price</span></span></th>
<th><span data-ttu-id="04ca9-227">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="04ca9-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04ca9-228">Je vytvořen časový záznam,</span><span class="sxs-lookup"><span data-stu-id="04ca9-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="04ca9-229">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="04ca9-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-230">Je odeslán časový záznam.</span><span class="sxs-lookup"><span data-stu-id="04ca9-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="04ca9-231">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="04ca9-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="04ca9-232">Čas je schválen a během schvalování nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="04ca9-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="04ca9-233">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-233">Cost actual</span></span></td>
<td><span data-ttu-id="04ca9-234">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="04ca9-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="04ca9-235">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="04ca9-236">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="04ca9-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="04ca9-237">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="04ca9-238">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-239">Nefakturované skutečné prodeje – účtovatelné</span><span class="sxs-lookup"><span data-stu-id="04ca9-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="04ca9-240">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-241">Jednotkové náklady zdroje</span><span class="sxs-lookup"><span data-stu-id="04ca9-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="04ca9-242">Měna jednotky zdroje</span><span class="sxs-lookup"><span data-stu-id="04ca9-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-243">Vnitropodnikový prodej</span><span class="sxs-lookup"><span data-stu-id="04ca9-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="04ca9-244">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="04ca9-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="04ca9-245">Čas je schválen a během schvalování dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="04ca9-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="04ca9-246">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-246">Cost actual</span></span></td>
<td><span data-ttu-id="04ca9-247">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="04ca9-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="04ca9-248">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="04ca9-249">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="04ca9-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="04ca9-250">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="04ca9-251">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="04ca9-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-252">Jednotkové náklady zdroje</span><span class="sxs-lookup"><span data-stu-id="04ca9-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="04ca9-253">Měna jednotky zdroje</span><span class="sxs-lookup"><span data-stu-id="04ca9-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-254">Vnitropodnikový prodej</span><span class="sxs-lookup"><span data-stu-id="04ca9-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="04ca9-255">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="04ca9-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-256">Skutečný nefakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="04ca9-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="04ca9-257">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-258">Skutečný nefakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="04ca9-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="04ca9-259">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="04ca9-260">Faktura je potvrzena a nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="04ca9-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="04ca9-261">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="04ca9-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="04ca9-262">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="04ca9-263">Fakturovaný prodej pro milník</span><span class="sxs-lookup"><span data-stu-id="04ca9-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="04ca9-264">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="04ca9-265">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="04ca9-266">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-267">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="04ca9-267">Billed sales</span></span></td>
<td><span data-ttu-id="04ca9-268">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="04ca9-269">Faktura je potvrzena a dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="04ca9-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="04ca9-270">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="04ca9-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="04ca9-271">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="04ca9-272">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="04ca9-273">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="04ca9-274">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="04ca9-275">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-276">Fakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="04ca9-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="04ca9-277">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-278">Fakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="04ca9-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="04ca9-279">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="04ca9-280">Faktura je opravena za účelem zvýšení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="04ca9-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="04ca9-281">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="04ca9-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="04ca9-282">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="04ca9-283">Storno fakturovaného prodeje pro milník</span><span class="sxs-lookup"><span data-stu-id="04ca9-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="04ca9-284">Změna stavu milníku z <strong>fakturováno</strong> na <strong>Připraveno pro fakturu</strong></span><span class="sxs-lookup"><span data-stu-id="04ca9-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="04ca9-285">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="04ca9-286">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="04ca9-287">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="04ca9-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-288">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="04ca9-288">Billed sales</span></span></td>
<td><span data-ttu-id="04ca9-289">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="04ca9-290">Faktura je opravena za účelem snížení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="04ca9-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="04ca9-291">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="04ca9-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="04ca9-292">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-293">Fakturovaný prodej pro nové množství</span><span class="sxs-lookup"><span data-stu-id="04ca9-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="04ca9-294">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ca9-295">Nefakturovaný prodej – účtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="04ca9-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="04ca9-296">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="04ca9-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
