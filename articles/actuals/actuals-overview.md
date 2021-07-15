---
title: Skutečné hodnoty
description: Tento téma poskytuje informace o tom, jak pracovat s aktuálními údaji v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9e046602a3005930c41ab8c50472d5b1a72303c6
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368603"
---
# <a name="actuals"></a><span data-ttu-id="68c9d-103">Skutečné hodnoty</span><span class="sxs-lookup"><span data-stu-id="68c9d-103">Actuals</span></span> 

<span data-ttu-id="68c9d-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="68c9d-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="68c9d-105">Skutečné hodnoty představují zkontrolovaný a schválený finanční a časový plán postupu v projektu.</span><span class="sxs-lookup"><span data-stu-id="68c9d-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="68c9d-106">Jsou vytvářeny na základě schválení času, výdajů, záznamů o použití materiálu a záznamů faktur a deníku.</span><span class="sxs-lookup"><span data-stu-id="68c9d-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="68c9d-107">Řádky deníku a časové záznamy</span><span class="sxs-lookup"><span data-stu-id="68c9d-107">Journal lines and time submission</span></span>

<span data-ttu-id="68c9d-108">Další informace o časových záznamech najdete v části [Přehled časových záznamů](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="68c9d-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="68c9d-109">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="68c9d-109">Time and materials</span></span>

<span data-ttu-id="68c9d-110">Když je zadaný časový údaj propojen s projektem, který je namapován na řádek kontraktu času a materiálů, systém vytvoří dva řádky deníku, jeden pro náklady a druhý pro nevyfakturované prodeje.</span><span class="sxs-lookup"><span data-stu-id="68c9d-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="68c9d-111">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="68c9d-111">Fixed price</span></span>

<span data-ttu-id="68c9d-112">Při odeslání časového záznamu propojeného s projektem, který je namapovaný na řádek smlouvy s pevnou cenou, systém vytvoří jeden řádek deníku pro náklady.</span><span class="sxs-lookup"><span data-stu-id="68c9d-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="68c9d-113">Výchozí cena</span><span class="sxs-lookup"><span data-stu-id="68c9d-113">Default pricing</span></span>

<span data-ttu-id="68c9d-114">Logika pro vytváření výchozích cen je umístěna na řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="68c9d-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="68c9d-115">Hodnoty polí z časového záznamu jsou zkopírovány do řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="68c9d-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="68c9d-116">Tyto hodnoty obsahují datum transakce, řádek smlouvy, na který je projekt namapován, a výsledek měny v příslušném ceníku.</span><span class="sxs-lookup"><span data-stu-id="68c9d-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="68c9d-117">Pole, která ovlivňují výchozí ceny, jako jsou **Role** a **Jednotka prostředků** se používají k určení odpovídající ceny na řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="68c9d-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="68c9d-118">K časovému záznamu můžete přidat vlastní pole.</span><span class="sxs-lookup"><span data-stu-id="68c9d-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="68c9d-119">Pokud chcete, aby se hodnota pole rozšířila na skutečné hodnoty, vytvořte pole v tabulkách **Skutečné hodnoty** a **Řádek deníku**.</span><span class="sxs-lookup"><span data-stu-id="68c9d-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="68c9d-120">Pomocí vlastního kódu můžete šířit vybranou hodnotu pole z položky Zadání na Skutečné hodnoty prostřednictvím řádku deníku pomocí původů transakcí.</span><span class="sxs-lookup"><span data-stu-id="68c9d-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="68c9d-121">Další informace o původu transakcí a propojení najdete v tématu [Propojení skutečných hodnot s původními záznamy](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="68c9d-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="68c9d-122">Řádky deníku a zadávání základních výdajů</span><span class="sxs-lookup"><span data-stu-id="68c9d-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="68c9d-123">Další informace o záznamech o výdajích najdete v části [Přehled výdajů](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="68c9d-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="68c9d-124">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="68c9d-124">Time and materials</span></span>

<span data-ttu-id="68c9d-125">Když je zadaný záznam základního výdaje propojen s projektem, který je namapován na řádek kontraktu času a materiálů, systém vytvoří dva řádky deníku, jeden pro náklady a druhý pro nevyfakturované prodeje.</span><span class="sxs-lookup"><span data-stu-id="68c9d-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="68c9d-126">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="68c9d-126">Fixed price</span></span>

<span data-ttu-id="68c9d-127">Když je odeslaný záznam základního výdaje spojen s projektem, který je namapovaný na řádek smlouvy s pevnou cenou, systém vytvoří jeden řádek deníku na náklad.</span><span class="sxs-lookup"><span data-stu-id="68c9d-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="68c9d-128">Výchozí cena</span><span class="sxs-lookup"><span data-stu-id="68c9d-128">Default pricing</span></span>

<span data-ttu-id="68c9d-129">Logika pro zadávání výchozích cen výdajů je založena na kategorii výdajů.</span><span class="sxs-lookup"><span data-stu-id="68c9d-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="68c9d-130">Datum transakce, řádek smlouvy, na který je projekt namapován, a měna jsou použity k určení příslušného ceníku.</span><span class="sxs-lookup"><span data-stu-id="68c9d-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="68c9d-131">Pole, která ovlivňují výchozí ceny, jako jsou **Kategorie transakce** a **Jednotka prostředků** se používají k určení odpovídající ceny na řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="68c9d-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="68c9d-132">To však funguje pouze v případě, že cenová metoda v ceníku je **Cena za jednotku**.</span><span class="sxs-lookup"><span data-stu-id="68c9d-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="68c9d-133">Pokud je způsob stanovení cen **Za cenu** nebo **Přirážka nad náklady**, pro náklady se použije cena zadaná při vytvoření položky výdajů a cena na řádku prodejního deníku se vypočítá na základě metody stanovení cen.</span><span class="sxs-lookup"><span data-stu-id="68c9d-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="68c9d-134">K záznamu výdajů můžete přidat vlastní pole.</span><span class="sxs-lookup"><span data-stu-id="68c9d-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="68c9d-135">Pokud chcete, aby se hodnota pole rozšířila na skutečné hodnoty, vytvořte pole v tabulkách **Skutečné hodnoty** a **Řádek deníku**.</span><span class="sxs-lookup"><span data-stu-id="68c9d-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="68c9d-136">Pomocí vlastního kódu můžete šířit vybranou hodnotu pole z položky Zadání na Skutečné hodnoty prostřednictvím řádku deníku pomocí původů transakcí.</span><span class="sxs-lookup"><span data-stu-id="68c9d-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="68c9d-137">Další informace o původu transakcí a propojení najdete v tématu [Propojení skutečných hodnot s původními záznamy](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="68c9d-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="68c9d-138">Řádky deníku a odeslání protokolu o použití materiálu</span><span class="sxs-lookup"><span data-stu-id="68c9d-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="68c9d-139">Další informace o zadávání výdajů najdete v části [Protokol použití materiálu](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="68c9d-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="68c9d-140">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="68c9d-140">Time and materials</span></span>

<span data-ttu-id="68c9d-141">Když je zadaná položka protokolu o použití materiálu propojena s projektem, který je mapován na řádek smlouvy o čase a materiálech, systém vytvoří dva řádky deníku, jeden pro náklady a druhý pro nevyfakturované prodeje.</span><span class="sxs-lookup"><span data-stu-id="68c9d-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="68c9d-142">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="68c9d-142">Fixed price</span></span>

<span data-ttu-id="68c9d-143">Když je odeslaný záznam protokolu využití materiálu spojen s projektem, který je namapovaný na řádek smlouvy s pevnou cenou, systém vytvoří jeden řádek deníku na náklad.</span><span class="sxs-lookup"><span data-stu-id="68c9d-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="68c9d-144">Výchozí cena</span><span class="sxs-lookup"><span data-stu-id="68c9d-144">Default pricing</span></span>

<span data-ttu-id="68c9d-145">Logika pro zadání výchozích cen materiálu je založena na kombinaci produktu a jednotky.</span><span class="sxs-lookup"><span data-stu-id="68c9d-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="68c9d-146">Datum transakce, řádek smlouvy, na který je projekt namapován, a měna jsou použity k určení příslušného ceníku.</span><span class="sxs-lookup"><span data-stu-id="68c9d-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="68c9d-147">Pole, která ovlivňují výchozí ceny, jako jsou **ID produktu** a **Jednotka prostředků** se používají k určení odpovídající ceny na řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="68c9d-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="68c9d-148">To však funguje pouze u katalogových produktů.</span><span class="sxs-lookup"><span data-stu-id="68c9d-148">However, this only works for catalog products.</span></span> <span data-ttu-id="68c9d-149">U produktů, které nejsou v katalogu, se pro náklady a prodejní cenu na řádcích deníku použije cena zadaná při vytvoření položky protokolu o použití materiálu.</span><span class="sxs-lookup"><span data-stu-id="68c9d-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="68c9d-150">K záznamu **Protokol využití materiálu** můžete přidat vlastní pole.</span><span class="sxs-lookup"><span data-stu-id="68c9d-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="68c9d-151">Pokud chcete, aby se hodnota pole rozšířila na skutečné hodnoty, vytvořte pole v tabulkách **Skutečné hodnoty** a **Řádek deníku**.</span><span class="sxs-lookup"><span data-stu-id="68c9d-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="68c9d-152">Pomocí vlastního kódu můžete šířit vybranou hodnotu pole z položky Zadání na Skutečné hodnoty prostřednictvím řádku deníku pomocí původů transakcí.</span><span class="sxs-lookup"><span data-stu-id="68c9d-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="68c9d-153">Další informace o původu transakcí a propojení najdete v tématu [Propojení skutečných hodnot s původními záznamy](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="68c9d-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="68c9d-154">Použití deníků k zaznamenání nákladů</span><span class="sxs-lookup"><span data-stu-id="68c9d-154">Use entry journals to record costs</span></span>

<span data-ttu-id="68c9d-155">Deníky záznamů můžete použít a zaznamenávat náklady nebo výnosy do tříd materiálu, poplatků, času, výdajů nebo daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="68c9d-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="68c9d-156">Deníky lze použít k následujícím účelům:</span><span class="sxs-lookup"><span data-stu-id="68c9d-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="68c9d-157">Skutečné hodnoty transakcí z jiného systému je nutné přesunout do Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="68c9d-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="68c9d-158">Zaznamenejte náklady, ke kterým došlo v jiném systému.</span><span class="sxs-lookup"><span data-stu-id="68c9d-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="68c9d-159">Tyto náklady mohou zahrnovat náklady na pořízení nebo subdodávky.</span><span class="sxs-lookup"><span data-stu-id="68c9d-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68c9d-160">Aplikace neověřuje typ řádku deníku ani související ceny, které jsou zadány na řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="68c9d-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="68c9d-161">Proto by měl k vytváření skutečných hodnot používat deníky pouze uživatel, který si je plně vědom účetního dopadu skutečných hodnot na projekt.</span><span class="sxs-lookup"><span data-stu-id="68c9d-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="68c9d-162">Z důvodu dopadu tohoto typu deníku byste měli pečlivě zvolit, kdo má přístup k vytváření deníků záznamů.</span><span class="sxs-lookup"><span data-stu-id="68c9d-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="68c9d-163">Záznam skutečných hodnot na základě událostí projektu</span><span class="sxs-lookup"><span data-stu-id="68c9d-163">Record actuals based on project events</span></span>

<span data-ttu-id="68c9d-164">Project Operations zaznamenává finanční transakce, které nastanou během projektu.</span><span class="sxs-lookup"><span data-stu-id="68c9d-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="68c9d-165">Tyto transakce jsou zaznamenány jako skutečné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="68c9d-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="68c9d-166">V následujících tabulkách jsou zobrazeny různé typy skutečných hodnot, které jsou vytvořeny v závislosti na tom, zda je projekt časově materiálovým projektem nebo projektem s pevnou cenou, je v předprodejní fázi nebo jde o interní projekt.</span><span class="sxs-lookup"><span data-stu-id="68c9d-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="68c9d-167">Zdroj patří do stejné organizační jednotky jako smluvní jednotka projektu</span><span class="sxs-lookup"><span data-stu-id="68c9d-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="68c9d-168">Událost</span><span class="sxs-lookup"><span data-stu-id="68c9d-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="68c9d-169">Fakturovatelný nebo prodaný projekt</span><span class="sxs-lookup"><span data-stu-id="68c9d-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="68c9d-170">Projekt v předprodejní fázi</span><span class="sxs-lookup"><span data-stu-id="68c9d-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="68c9d-171">Interní projekt</span><span class="sxs-lookup"><span data-stu-id="68c9d-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="68c9d-172">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="68c9d-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="68c9d-173">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="68c9d-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="68c9d-174">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="68c9d-174">Actuals</span></span></th>
<th><span data-ttu-id="68c9d-175">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="68c9d-175">Transaction currency</span></span></th>
<th><span data-ttu-id="68c9d-176">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="68c9d-176">Fixed price</span></span></th>
<th><span data-ttu-id="68c9d-177">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="68c9d-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="68c9d-178">Je vytvořen časový záznam,</span><span class="sxs-lookup"><span data-stu-id="68c9d-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="68c9d-179">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="68c9d-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-180">Je odeslán časový záznam.</span><span class="sxs-lookup"><span data-stu-id="68c9d-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="68c9d-181">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="68c9d-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="68c9d-182">Čas je schválen a během schvalování nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="68c9d-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="68c9d-183">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-183">Cost actual</span></span></td>
<td><span data-ttu-id="68c9d-184">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="68c9d-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="68c9d-185">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="68c9d-186">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="68c9d-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="68c9d-187">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="68c9d-188">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-189">Nefakturované skutečné prodeje – účtovatelné</span><span class="sxs-lookup"><span data-stu-id="68c9d-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="68c9d-190">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="68c9d-191">Čas je schválen a během schvalování dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="68c9d-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="68c9d-192">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-192">Cost actual</span></span></td>
<td><span data-ttu-id="68c9d-193">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="68c9d-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="68c9d-194">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="68c9d-195">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="68c9d-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="68c9d-196">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="68c9d-197">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-198">Skutečný nefakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="68c9d-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="68c9d-199">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-200">Skutečný nefakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="68c9d-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="68c9d-201">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="68c9d-202">Faktura je potvrzena a nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="68c9d-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="68c9d-203">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="68c9d-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="68c9d-204">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="68c9d-205">Fakturovaný prodej pro milník</span><span class="sxs-lookup"><span data-stu-id="68c9d-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="68c9d-206">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="68c9d-207">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="68c9d-208">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-209">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="68c9d-209">Billed sales</span></span></td>
<td><span data-ttu-id="68c9d-210">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="68c9d-211">Faktura je potvrzena a dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="68c9d-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="68c9d-212">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="68c9d-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="68c9d-213">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="68c9d-214">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="68c9d-215">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="68c9d-216">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="68c9d-217">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-218">Fakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="68c9d-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="68c9d-219">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-220">Fakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="68c9d-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="68c9d-221">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="68c9d-222">Faktura je opravena za účelem zvýšení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="68c9d-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="68c9d-223">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="68c9d-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="68c9d-224">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="68c9d-225">Storno fakturovaného prodeje pro milník</span><span class="sxs-lookup"><span data-stu-id="68c9d-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="68c9d-226">Změna stavu milníku z <strong>fakturováno</strong> na <strong>Připraveno pro fakturu</strong></span><span class="sxs-lookup"><span data-stu-id="68c9d-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="68c9d-227">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="68c9d-228">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="68c9d-229">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-230">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="68c9d-230">Billed sales</span></span></td>
<td><span data-ttu-id="68c9d-231">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="68c9d-232">Faktura je opravena za účelem snížení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="68c9d-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="68c9d-233">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="68c9d-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="68c9d-234">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-235">Fakturovaný prodej pro nové množství</span><span class="sxs-lookup"><span data-stu-id="68c9d-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="68c9d-236">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-237">Nefakturovaný prodej – účtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="68c9d-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="68c9d-238">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="68c9d-239">Zdroj patří do organizační jednotky, která se liší od smluvní jednotky projektu</span><span class="sxs-lookup"><span data-stu-id="68c9d-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="68c9d-240">Událost</span><span class="sxs-lookup"><span data-stu-id="68c9d-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="68c9d-241">Fakturovatelný nebo prodaný projekt</span><span class="sxs-lookup"><span data-stu-id="68c9d-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="68c9d-242">Projekt v předprodejní fázi</span><span class="sxs-lookup"><span data-stu-id="68c9d-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="68c9d-243">Interní projekt</span><span class="sxs-lookup"><span data-stu-id="68c9d-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="68c9d-244">Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="68c9d-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="68c9d-245">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="68c9d-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="68c9d-246">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="68c9d-246">Actuals</span></span></th>
<th><span data-ttu-id="68c9d-247">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="68c9d-247">Transaction currency</span></span></th>
<th><span data-ttu-id="68c9d-248">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="68c9d-248">Fixed price</span></span></th>
<th><span data-ttu-id="68c9d-249">Měna transakce</span><span class="sxs-lookup"><span data-stu-id="68c9d-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="68c9d-250">Je vytvořen časový záznam,</span><span class="sxs-lookup"><span data-stu-id="68c9d-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="68c9d-251">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="68c9d-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-252">Je odeslán časový záznam.</span><span class="sxs-lookup"><span data-stu-id="68c9d-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="68c9d-253">V entitě Skutečné hodnoty není žádná aktivita</span><span class="sxs-lookup"><span data-stu-id="68c9d-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="68c9d-254">Čas je schválen a během schvalování nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="68c9d-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="68c9d-255">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-255">Cost actual</span></span></td>
<td><span data-ttu-id="68c9d-256">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="68c9d-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="68c9d-257">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="68c9d-258">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="68c9d-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="68c9d-259">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="68c9d-260">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-261">Nefakturované skutečné prodeje – účtovatelné</span><span class="sxs-lookup"><span data-stu-id="68c9d-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="68c9d-262">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-263">Jednotkové náklady zdroje</span><span class="sxs-lookup"><span data-stu-id="68c9d-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="68c9d-264">Měna jednotky zdroje</span><span class="sxs-lookup"><span data-stu-id="68c9d-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-265">Vnitropodnikový prodej</span><span class="sxs-lookup"><span data-stu-id="68c9d-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="68c9d-266">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="68c9d-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="68c9d-267">Čas je schválen a během schvalování dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="68c9d-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="68c9d-268">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-268">Cost actual</span></span></td>
<td><span data-ttu-id="68c9d-269">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="68c9d-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="68c9d-270">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="68c9d-271">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="68c9d-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="68c9d-272">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="68c9d-273">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="68c9d-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-274">Jednotkové náklady zdroje</span><span class="sxs-lookup"><span data-stu-id="68c9d-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="68c9d-275">Měna jednotky zdroje</span><span class="sxs-lookup"><span data-stu-id="68c9d-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-276">Vnitropodnikový prodej</span><span class="sxs-lookup"><span data-stu-id="68c9d-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="68c9d-277">Měna smluvní jednotky</span><span class="sxs-lookup"><span data-stu-id="68c9d-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-278">Skutečný nefakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="68c9d-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="68c9d-279">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-280">Skutečný nefakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="68c9d-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="68c9d-281">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="68c9d-282">Faktura je potvrzena a nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="68c9d-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="68c9d-283">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="68c9d-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="68c9d-284">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="68c9d-285">Fakturovaný prodej pro milník</span><span class="sxs-lookup"><span data-stu-id="68c9d-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="68c9d-286">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="68c9d-287">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="68c9d-288">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-289">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="68c9d-289">Billed sales</span></span></td>
<td><span data-ttu-id="68c9d-290">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="68c9d-291">Faktura je potvrzena a dojde ke snížení fakturovatelných hodin.</span><span class="sxs-lookup"><span data-stu-id="68c9d-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="68c9d-292">Storno nefakturovaného prodeje</span><span class="sxs-lookup"><span data-stu-id="68c9d-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="68c9d-293">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="68c9d-294">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="68c9d-295">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="68c9d-296">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="68c9d-297">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-298">Fakturovaný prodej – účtovatelný pro nové množství</span><span class="sxs-lookup"><span data-stu-id="68c9d-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="68c9d-299">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-300">Fakturovaný prodej – neúčtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="68c9d-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="68c9d-301">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="68c9d-302">Faktura je opravena za účelem zvýšení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="68c9d-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="68c9d-303">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="68c9d-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="68c9d-304">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="68c9d-305">Storno fakturovaného prodeje pro milník</span><span class="sxs-lookup"><span data-stu-id="68c9d-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="68c9d-306">Změna stavu milníku z <strong>fakturováno</strong> na <strong>Připraveno pro fakturu</strong></span><span class="sxs-lookup"><span data-stu-id="68c9d-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="68c9d-307">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="68c9d-308">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="68c9d-309">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="68c9d-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-310">Fakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="68c9d-310">Billed sales</span></span></td>
<td><span data-ttu-id="68c9d-311">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="68c9d-312">Faktura je opravena za účelem snížení účtovatelného množství.</span><span class="sxs-lookup"><span data-stu-id="68c9d-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="68c9d-313">Fakturovaný prodej – storno</span><span class="sxs-lookup"><span data-stu-id="68c9d-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="68c9d-314">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-315">Fakturovaný prodej pro nové množství</span><span class="sxs-lookup"><span data-stu-id="68c9d-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="68c9d-316">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="68c9d-317">Nefakturovaný prodej – účtovatelný pro rozdíl</span><span class="sxs-lookup"><span data-stu-id="68c9d-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="68c9d-318">Měna projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="68c9d-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
