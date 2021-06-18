---
title: Zpracování příjemek výdajů
description: Toto téma poskytuje informace o zpracování optického rozpoznávání znaků (OCR) pro účtenky. Tato funkce je navržena tak, aby zlepšila uživatelské prostředí při vytváření výkazů výdajů v Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: ed9c97ba9cc505106599c2896dc2112358d0c408
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993498"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="ae763-104">Zpracování příjemek výdajů</span><span class="sxs-lookup"><span data-stu-id="ae763-104">Expense receipt processing</span></span>

<span data-ttu-id="ae763-105">Zadávání výdajů bylo vylepšeno zavedením zpracování optického rozpoznávání znaků (OCR) pro účtenky.</span><span class="sxs-lookup"><span data-stu-id="ae763-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="ae763-106">Tato funkce je navržena tak, aby zlepšila uživatelské prostředí při vytváření výkazů výdajů.</span><span class="sxs-lookup"><span data-stu-id="ae763-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="ae763-107">Klíčové funkce</span><span class="sxs-lookup"><span data-stu-id="ae763-107">Key features</span></span>

- <span data-ttu-id="ae763-108">Systém z účtenek extrahuje jméno obchodníka, datum a celkovou částku.</span><span class="sxs-lookup"><span data-stu-id="ae763-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="ae763-109">Funkce se pokusí porovnat nepřipojené účtenky s nepřipojenými výdajovými transakcemi.</span><span class="sxs-lookup"><span data-stu-id="ae763-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="ae763-110">Z účtenek může uživatel vytvořit ručně zadané výdajové transakce.</span><span class="sxs-lookup"><span data-stu-id="ae763-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="ae763-111">Příklady použití</span><span class="sxs-lookup"><span data-stu-id="ae763-111">Usage examples</span></span>

<span data-ttu-id="ae763-112">Chcete-li automaticky připojit účtenky, které zahrnují transakce kreditní kartou, když je vytvořen výkaz výdajů, proveďte následující:</span><span class="sxs-lookup"><span data-stu-id="ae763-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="ae763-113">Otevřete pracovní prostor **Správa výdajů**.</span><span class="sxs-lookup"><span data-stu-id="ae763-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="ae763-114">Na kartě **Účtenky** ověřte, zda existují nepřipojené účtenky.</span><span class="sxs-lookup"><span data-stu-id="ae763-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="ae763-115">Potvrzení můžete také odeslat na kartě **Účtenky**.</span><span class="sxs-lookup"><span data-stu-id="ae763-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="ae763-116">Na kartě **Výdaje** ověřte, zda existují nepřipojené výdaje.</span><span class="sxs-lookup"><span data-stu-id="ae763-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="ae763-117">Správce výdajů tyto náklady obvykle importuje od poskytovatele kreditní karty.</span><span class="sxs-lookup"><span data-stu-id="ae763-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="ae763-118">Vyberte **Nový výkaz výdajů**.</span><span class="sxs-lookup"><span data-stu-id="ae763-118">Select **New expense report**.</span></span> <span data-ttu-id="ae763-119">Všimněte si, že při vytváření výkazu výdajů můžete nyní zahrnout výdaje a účtenky.</span><span class="sxs-lookup"><span data-stu-id="ae763-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="ae763-120">Pokud přidáte výdaje i účtenky, spustí se automatické párování účtenek s výdaji.</span><span class="sxs-lookup"><span data-stu-id="ae763-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="ae763-121">Chcete-li vytvořit výdaj nebo spárovat výdaj z účtenky, proveďte následující:</span><span class="sxs-lookup"><span data-stu-id="ae763-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="ae763-122">Na výkazu výdajů na kartě **Účtenky** připojte účtenky volbou **Přidat účtenky**.</span><span class="sxs-lookup"><span data-stu-id="ae763-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="ae763-123">Pod nahraným obrázkem účtenky si všimněte možností **Vytvořit** a **Párovat**.</span><span class="sxs-lookup"><span data-stu-id="ae763-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="ae763-124">Vyberte **Vytvořit** k vytvoření ručně zadané výdajové transakce a vyplnění hodnot, které jsou extrahovány z účtenky.</span><span class="sxs-lookup"><span data-stu-id="ae763-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="ae763-125">Pokud vyberete **Párovat**, systém se pokusí spárovat existující výdaj s účtenkou.</span><span class="sxs-lookup"><span data-stu-id="ae763-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="ae763-126">Instalace</span><span class="sxs-lookup"><span data-stu-id="ae763-126">Installation</span></span>

<span data-ttu-id="ae763-127">Tato funkce funguje v kombinaci s funkcí **Sestavy výdajů v novém**, která pomůže zjednodušit výdaje.</span><span class="sxs-lookup"><span data-stu-id="ae763-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="ae763-128">Tato funkce je k dispozici pouze pro prostředí úrovně alespoň 2, která jsou Sandbox a provozní.</span><span class="sxs-lookup"><span data-stu-id="ae763-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="ae763-129">Chcete-li použít tyto pokročilé možnosti výdajů, nainstalujte si doplněk Služba správy výdajů pro Microsoft Dynamics 365 Finance a zapněte funkce ve vaší instanci.</span><span class="sxs-lookup"><span data-stu-id="ae763-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="ae763-130">K doplňku můžete přistupovat ze svého projektu v Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ae763-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="ae763-131">Přihlaste se do LCS a otevřete požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="ae763-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="ae763-132">Přejděte na **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="ae763-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="ae763-133">Vyberte **Udržovat**, nebo přejděte dolů záložku s náhledem **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="ae763-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="ae763-134">Vyberte **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="ae763-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="ae763-135">Zvolte **Služba správy výdajů**.</span><span class="sxs-lookup"><span data-stu-id="ae763-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="ae763-136">Postupujte podle instalačního průvodce a souhlaste s podmínkami.</span><span class="sxs-lookup"><span data-stu-id="ae763-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="ae763-137">Vyberte volbu **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="ae763-137">Select **Install**.</span></span>

<span data-ttu-id="ae763-138">V pracovním prostoru **Správa funkcí** zapněte následující funkce:</span><span class="sxs-lookup"><span data-stu-id="ae763-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="ae763-139">Nová verze výkazů výdajů</span><span class="sxs-lookup"><span data-stu-id="ae763-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="ae763-140">Automatické spárování a vytváření výdajů z účtenek</span><span class="sxs-lookup"><span data-stu-id="ae763-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="ae763-141">Po zapnutí těchto funkcí dojde k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="ae763-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="ae763-142">Existující pracovní prostor **Správa výdajů** je nahrazen novým pracovním prostorem.</span><span class="sxs-lookup"><span data-stu-id="ae763-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="ae763-143">Je přidána nová položka nabídky pro viditelnost pole výdajů.</span><span class="sxs-lookup"><span data-stu-id="ae763-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="ae763-144">Stále můžete otevřít bývalou stránku **Výkazy výdajů** přechodem na **Správa výdajů> Moje výdaje> Výkazy výdajů**.</span><span class="sxs-lookup"><span data-stu-id="ae763-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="ae763-145">Pracovní postupy a veškerá schválení vás stále budou zavádět na existujíc stránku s výkazy výdajů.</span><span class="sxs-lookup"><span data-stu-id="ae763-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="ae763-146">Účtenky budou zpracovány prostřednictvím Microsoft Azure Cognitive Services a metadata budou extrahována a přidána.</span><span class="sxs-lookup"><span data-stu-id="ae763-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="ae763-147">Přidá se možnost, která vám umožní vytvořit výkaz výdajů obsahující nespárované nepřipojené účtenky.</span><span class="sxs-lookup"><span data-stu-id="ae763-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="ae763-148">Možnost, která je přidána do výkazů výdajů, vám umožní vytvořit řádek výdajů z účtenky nebo se pokusí spárovat existující účtenku s existujícím řádkem výdajů.</span><span class="sxs-lookup"><span data-stu-id="ae763-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="ae763-149">Další informace o funkci Sestavy výdajů v novém viz [Sestavy výdajů v novém ](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="ae763-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="ae763-150">Nejčastější dotazy</span><span class="sxs-lookup"><span data-stu-id="ae763-150">Frequently asked questions</span></span>

<span data-ttu-id="ae763-151">**Používá Microsoft moje data pro své modely?**</span><span class="sxs-lookup"><span data-stu-id="ae763-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="ae763-152">Ne, společnost Microsoft vytvořila obecný model strojové učení pro svou službu zpracování účtenek.</span><span class="sxs-lookup"><span data-stu-id="ae763-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="ae763-153">Tento model není založen na účtenkách, které nahrajete.</span><span class="sxs-lookup"><span data-stu-id="ae763-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="ae763-154">**Kde je tato funkce dostupná a zpracována?**</span><span class="sxs-lookup"><span data-stu-id="ae763-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="ae763-155">V současné době jsou podporovány Spojené státy.</span><span class="sxs-lookup"><span data-stu-id="ae763-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="ae763-156">**Kam jdou moje účtenky?**</span><span class="sxs-lookup"><span data-stu-id="ae763-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="ae763-157">Finance kontaktují Cognitive Services s cílem extrahovat data pole.</span><span class="sxs-lookup"><span data-stu-id="ae763-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="ae763-158">Během zpracování bude služba Cognitive Services uchovávat kopii vašeho dokladu až 24 hodin.</span><span class="sxs-lookup"><span data-stu-id="ae763-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="ae763-159">Po dokončení zpracování odebere Cognitive Services účtenku.</span><span class="sxs-lookup"><span data-stu-id="ae763-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="ae763-160">Účtenky jsou stále uloženy v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="ae763-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="ae763-161">Další informace naleznete v tématu [Povolit porozumění účtenkám s novou funkcí rozpoznávání formulářů](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="ae763-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]