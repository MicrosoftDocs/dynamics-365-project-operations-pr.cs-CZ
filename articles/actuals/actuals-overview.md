---
title: Skutečné hodnoty
description: Tento téma poskytuje informace o tom, jak pracovat s aktuálními údaji v Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291791"
---
# <a name="actuals"></a><span data-ttu-id="496b1-103">Skutečné hodnoty</span><span class="sxs-lookup"><span data-stu-id="496b1-103">Actuals</span></span> 

<span data-ttu-id="496b1-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="496b1-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="496b1-105">Skutečné hodnoty jsou množství práce dokončené v projektu.</span><span class="sxs-lookup"><span data-stu-id="496b1-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="496b1-106">Jsou vytvářeny jako výsledek časových a výdajových záznamů, záznamů deníku a faktur.</span><span class="sxs-lookup"><span data-stu-id="496b1-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="496b1-107">Řádky deníku a časové záznamy</span><span class="sxs-lookup"><span data-stu-id="496b1-107">Journal lines and time submission</span></span>

<span data-ttu-id="496b1-108">Další informace o časových záznamech najdete v části [Přehled časových záznamů](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="496b1-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="496b1-109">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="496b1-109">Time and materials</span></span>

<span data-ttu-id="496b1-110">Když je zadaný časový údaj propojen s projektem, který je namapován na řádek kontraktu času a materiálů, systém vytvoří dva řádky deníku, jeden pro náklady a druhý pro nevyfakturované prodeje.</span><span class="sxs-lookup"><span data-stu-id="496b1-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="496b1-111">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="496b1-111">Fixed price</span></span>

<span data-ttu-id="496b1-112">Při odeslání časového záznamu propojeného s projektem, který je namapovaný na řádek smlouvy s pevnou cenou, systém vytvoří jeden řádek deníku pro náklady.</span><span class="sxs-lookup"><span data-stu-id="496b1-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="496b1-113">Výchozí cena</span><span class="sxs-lookup"><span data-stu-id="496b1-113">Default pricing</span></span>

<span data-ttu-id="496b1-114">Logika pro vytváření výchozích cen je umístěna na řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="496b1-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="496b1-115">Hodnoty polí z časového záznamu jsou zkopírovány do řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="496b1-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="496b1-116">Tyto hodnoty obsahují datum transakce, řádek smlouvy, na který je projekt namapován, a výsledek měny v příslušném ceníku.</span><span class="sxs-lookup"><span data-stu-id="496b1-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="496b1-117">Pole, která ovlivňují výchozí ceny, jako jsou **Role** a **Organizační jednotka** se používají k tomu, aby byla do řádku deníku zadána odpovídající cena.</span><span class="sxs-lookup"><span data-stu-id="496b1-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="496b1-118">K časovému záznamu můžete přidat vlastní pole.</span><span class="sxs-lookup"><span data-stu-id="496b1-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="496b1-119">Pokud chcete, aby byla hodnota pole přenesena do skutečných hodnot, vytvořte v entitě Skutečnost pole a pomocí mapování polí zkopírujte pole z časového záznamu do skutečného záznamu.</span><span class="sxs-lookup"><span data-stu-id="496b1-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="496b1-120">Řádky deníku a zadávání základních výdajů</span><span class="sxs-lookup"><span data-stu-id="496b1-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="496b1-121">Další informace o záznamech o výdajích najdete v části [Přehled výdajů](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="496b1-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="496b1-122">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="496b1-122">Time and materials</span></span>

<span data-ttu-id="496b1-123">Když je zadaný záznam základního výdaje propojen s projektem, který je namapován na řádek kontraktu času a materiálů, systém vytvoří dva řádky deníku, jeden pro náklady a druhý pro nevyfakturované prodeje.</span><span class="sxs-lookup"><span data-stu-id="496b1-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="496b1-124">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="496b1-124">Fixed price</span></span>

<span data-ttu-id="496b1-125">Při odeslání základního záznamu o výdajích propojeného s projektem, který je namapovaný na řádek smlouvy s pevnou cenou, systém vytvoří jeden řádek deníku pro náklady.</span><span class="sxs-lookup"><span data-stu-id="496b1-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="496b1-126">Výchozí cena</span><span class="sxs-lookup"><span data-stu-id="496b1-126">Default pricing</span></span>

<span data-ttu-id="496b1-127">Logika pro zadávání výchozích cen výdajů je založena na kategorii výdajů.</span><span class="sxs-lookup"><span data-stu-id="496b1-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="496b1-128">Datum transakce, řádek smlouvy, na který je projekt namapován, a měna jsou použity k určení příslušného ceníku.</span><span class="sxs-lookup"><span data-stu-id="496b1-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="496b1-129">Avšak ve výchozím nastavení je zadaná částka pro samotnou cenu nastavena přímo na souvisejících výdajových řádcích deníku pro náklady a prodej ve výchozím nastavení.</span><span class="sxs-lookup"><span data-stu-id="496b1-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="496b1-130">Položka založená na kategoriích výchozích jednotkových cen na výdajových položkách.</span><span class="sxs-lookup"><span data-stu-id="496b1-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="496b1-131">Použití deníků k zaznamenání nákladů</span><span class="sxs-lookup"><span data-stu-id="496b1-131">Use entry journals to record costs</span></span>

<span data-ttu-id="496b1-132">Deníky záznamů můžete použít a zaznamenávat náklady nebo výnosy do tříd materiálu, poplatků, času, výdajů nebo daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="496b1-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="496b1-133">Deníky lze použít k následujícím účelům:</span><span class="sxs-lookup"><span data-stu-id="496b1-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="496b1-134">Záznam skutečných nákladů na materiál a prodej projektu.</span><span class="sxs-lookup"><span data-stu-id="496b1-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="496b1-135">Skutečné hodnoty transakcí z jiného systému je nutné přesunout do Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="496b1-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="496b1-136">Zaznamenejte náklady, ke kterým došlo v jiném systému.</span><span class="sxs-lookup"><span data-stu-id="496b1-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="496b1-137">Tyto náklady mohou zahrnovat náklady na pořízení nebo subdodávky.</span><span class="sxs-lookup"><span data-stu-id="496b1-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="496b1-138">Aplikace neověřuje typ řádku deníku ani související ceny, které jsou zadány na řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="496b1-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="496b1-139">Proto by měl k vytváření skutečných hodnot používat deníky pouze uživatel, který si je plně vědom účetního dopadu skutečných hodnot na projekt.</span><span class="sxs-lookup"><span data-stu-id="496b1-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="496b1-140">Z důvodu dopadu tohoto typu deníku byste měli pečlivě zvolit, kdo má přístup k vytváření deníků záznamů.</span><span class="sxs-lookup"><span data-stu-id="496b1-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="496b1-141">Záznam skutečných hodnot na základě událostí projektu</span><span class="sxs-lookup"><span data-stu-id="496b1-141">Record actuals based on project events</span></span>

<span data-ttu-id="496b1-142">Project Operations zaznamenává finanční transakce, které nastanou během projektu.</span><span class="sxs-lookup"><span data-stu-id="496b1-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="496b1-143">Tyto transakce jsou zaznamenány jako skutečné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="496b1-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="496b1-144">V následujících tabulkách jsou zobrazeny různé typy skutečných hodnot, které jsou vytvořeny v závislosti na tom, zda je projekt časově materiálovým projektem nebo projektem s pevnou cenou, je v předprodejní fázi nebo jde o interní projekt.</span><span class="sxs-lookup"><span data-stu-id="496b1-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="496b1-145">Zdroj patří do stejné organizační jednotky jako smluvní jednotka projektu</span><span class="sxs-lookup"><span data-stu-id="496b1-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="496b1-146">Událost</span><span class="sxs-lookup"><span data-stu-id="496b1-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="496b1-147">Fakturovatelný nebo prodaný projekt</span><span class="sxs-lookup"><span data-stu-id="496b1-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="496b1-148">Projekt v předprodejní fázi</span><span class="sxs-lookup"><span data-stu-id="496b1-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="496b1-149">Interní projekt</span><span class="sxs-lookup"><span data-stu-id="496b1-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="496b1-150">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="496b1-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="496b1-151">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="496b1-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="496b1-152">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="496b1-152">Actuals</span></span></th>
<th><span data-ttu-id="496b1-153">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="496b1-153">Transaction currency</span></span></th>
<th><span data-ttu-id="496b1-154">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="496b1-154">Fixed price</span></span></th>
<th><span data-ttu-id="496b1-155">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="496b1-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="496b1-156">Je vytvořen časový záznam,</span><span class="sxs-lookup"><span data-stu-id="496b1-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="496b1-157">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="496b1-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-158">Je odeslán časový záznam.</span><span class="sxs-lookup"><span data-stu-id="496b1-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="496b1-159">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="496b1-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="496b1-160">Čas je schválen a během schvalování nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="496b1-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="496b1-161">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-161">Cost actual</span></span></td>
<td><span data-ttu-id="496b1-162">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="496b1-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="496b1-163">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="496b1-164">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="496b1-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="496b1-165">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="496b1-166">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-167">Nefakturované skutečné prodeje – účtovatelné</span><span class="sxs-lookup"><span data-stu-id="496b1-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="496b1-168">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="496b1-169">Čas je schválen a během schvalování dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="496b1-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="496b1-170">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-170">Cost actual</span></span></td>
<td><span data-ttu-id="496b1-171">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="496b1-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="496b1-172">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="496b1-173">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="496b1-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="496b1-174">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="496b1-175">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-176">Skutečný nefakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="496b1-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="496b1-177">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-178">Skutečný nefakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="496b1-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="496b1-179">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="496b1-180">Faktura je potvrzena a nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="496b1-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="496b1-181">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="496b1-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="496b1-182">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="496b1-183">Fakturovaný prodej pro milník</span><span class="sxs-lookup"><span data-stu-id="496b1-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="496b1-184">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="496b1-185">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="496b1-186">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-187">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="496b1-187">Billed sales</span></span></td>
<td><span data-ttu-id="496b1-188">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="496b1-189">Faktura je potvrzena a dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="496b1-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="496b1-190">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="496b1-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="496b1-191">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="496b1-192">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="496b1-193">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="496b1-194">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="496b1-195">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-196">Fakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="496b1-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="496b1-197">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-198">Fakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="496b1-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="496b1-199">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="496b1-200">Faktura je opravena za účelem zvýšení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="496b1-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="496b1-201">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="496b1-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="496b1-202">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="496b1-203">Storno fakturovaného prodeje pro milník</span><span class="sxs-lookup"><span data-stu-id="496b1-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="496b1-204">Změna stavu milníku z <strong>fakturováno</strong> na <strong>Připraveno pro fakturu</strong></span><span class="sxs-lookup"><span data-stu-id="496b1-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="496b1-205">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="496b1-206">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="496b1-207">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-208">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="496b1-208">Billed sales</span></span></td>
<td><span data-ttu-id="496b1-209">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="496b1-210">Faktura je opravena za účelem snížení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="496b1-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="496b1-211">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="496b1-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="496b1-212">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-213">Fakturovaný prodej pro nové množství</span><span class="sxs-lookup"><span data-stu-id="496b1-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="496b1-214">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-215">Nefakturovaný prodej – účtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="496b1-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="496b1-216">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="496b1-217">Zdroj patří do organizační jednotky, která se liší od smluvní jednotky projektu</span><span class="sxs-lookup"><span data-stu-id="496b1-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="496b1-218">Událost</span><span class="sxs-lookup"><span data-stu-id="496b1-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="496b1-219">Fakturovatelný nebo prodaný projekt</span><span class="sxs-lookup"><span data-stu-id="496b1-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="496b1-220">Projekt v předprodejní fázi</span><span class="sxs-lookup"><span data-stu-id="496b1-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="496b1-221">Interní projekt</span><span class="sxs-lookup"><span data-stu-id="496b1-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="496b1-222">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="496b1-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="496b1-223">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="496b1-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="496b1-224">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="496b1-224">Actuals</span></span></th>
<th><span data-ttu-id="496b1-225">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="496b1-225">Transaction currency</span></span></th>
<th><span data-ttu-id="496b1-226">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="496b1-226">Fixed price</span></span></th>
<th><span data-ttu-id="496b1-227">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="496b1-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="496b1-228">Je vytvořen časový záznam,</span><span class="sxs-lookup"><span data-stu-id="496b1-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="496b1-229">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="496b1-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-230">Je odeslán časový záznam.</span><span class="sxs-lookup"><span data-stu-id="496b1-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="496b1-231">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="496b1-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="496b1-232">Čas je schválen a během schvalování nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="496b1-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="496b1-233">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-233">Cost actual</span></span></td>
<td><span data-ttu-id="496b1-234">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="496b1-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="496b1-235">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="496b1-236">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="496b1-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="496b1-237">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="496b1-238">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-239">Nefakturované skutečné prodeje – účtovatelné</span><span class="sxs-lookup"><span data-stu-id="496b1-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="496b1-240">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-241">Jednotkové náklady zdroje</span><span class="sxs-lookup"><span data-stu-id="496b1-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="496b1-242">Měna jednotky zdroje</span><span class="sxs-lookup"><span data-stu-id="496b1-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-243">Vnitropodnikový prodej</span><span class="sxs-lookup"><span data-stu-id="496b1-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="496b1-244">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="496b1-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="496b1-245">Čas je schválen a během schvalování dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="496b1-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="496b1-246">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-246">Cost actual</span></span></td>
<td><span data-ttu-id="496b1-247">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="496b1-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="496b1-248">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="496b1-249">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="496b1-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="496b1-250">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="496b1-251">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="496b1-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-252">Jednotkové náklady zdroje</span><span class="sxs-lookup"><span data-stu-id="496b1-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="496b1-253">Měna jednotky zdroje</span><span class="sxs-lookup"><span data-stu-id="496b1-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-254">Vnitropodnikový prodej</span><span class="sxs-lookup"><span data-stu-id="496b1-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="496b1-255">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="496b1-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-256">Skutečný nefakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="496b1-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="496b1-257">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-258">Skutečný nefakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="496b1-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="496b1-259">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="496b1-260">Faktura je potvrzena a nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="496b1-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="496b1-261">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="496b1-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="496b1-262">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="496b1-263">Fakturovaný prodej pro milník</span><span class="sxs-lookup"><span data-stu-id="496b1-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="496b1-264">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="496b1-265">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="496b1-266">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-267">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="496b1-267">Billed sales</span></span></td>
<td><span data-ttu-id="496b1-268">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="496b1-269">Faktura je potvrzena a dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="496b1-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="496b1-270">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="496b1-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="496b1-271">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="496b1-272">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="496b1-273">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="496b1-274">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="496b1-275">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-276">Fakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="496b1-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="496b1-277">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-278">Fakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="496b1-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="496b1-279">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="496b1-280">Faktura je opravena za účelem zvýšení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="496b1-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="496b1-281">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="496b1-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="496b1-282">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="496b1-283">Storno fakturovaného prodeje pro milník</span><span class="sxs-lookup"><span data-stu-id="496b1-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="496b1-284">Změna stavu milníku z <strong>fakturováno</strong> na <strong>Připraveno pro fakturu</strong></span><span class="sxs-lookup"><span data-stu-id="496b1-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="496b1-285">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="496b1-286">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="496b1-287">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="496b1-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-288">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="496b1-288">Billed sales</span></span></td>
<td><span data-ttu-id="496b1-289">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="496b1-290">Faktura je opravena za účelem snížení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="496b1-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="496b1-291">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="496b1-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="496b1-292">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-293">Fakturovaný prodej pro nové množství</span><span class="sxs-lookup"><span data-stu-id="496b1-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="496b1-294">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="496b1-295">Nefakturovaný prodej – účtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="496b1-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="496b1-296">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="496b1-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]