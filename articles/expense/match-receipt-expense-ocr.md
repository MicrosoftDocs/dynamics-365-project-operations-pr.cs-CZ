---
title: Pořízení účtenky pomocí OCR
description: Toto téma poskytuje informace o zpracování optického rozpoznávání znaků (OCR) pro účtenky.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fd0cb0fb094260fa3e82d7a2f200f328a39dd7a1
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499843"
---
# <a name="capture-a-receipt-using-ocr"></a><span data-ttu-id="6e39e-103">Pořízení účtenky pomocí OCR</span><span class="sxs-lookup"><span data-stu-id="6e39e-103">Capture a receipt using OCR</span></span>

<span data-ttu-id="6e39e-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="6e39e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6e39e-105">Zadávání výdajů bylo vylepšeno zavedením zpracování optického rozpoznávání znaků (OCR) pro účtenky.</span><span class="sxs-lookup"><span data-stu-id="6e39e-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="6e39e-106">Tato funkce je navržena tak, aby zlepšila uživatelské prostředí při vytváření výkazů výdajů.</span><span class="sxs-lookup"><span data-stu-id="6e39e-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="6e39e-107">Klíčové funkce</span><span class="sxs-lookup"><span data-stu-id="6e39e-107">Key features</span></span>

- <span data-ttu-id="6e39e-108">Systém z účtenek extrahuje jméno obchodníka, datum a celkovou částku.</span><span class="sxs-lookup"><span data-stu-id="6e39e-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="6e39e-109">Systém se pokusí porovnat nepřipojené účtenky s nepřipojenými výdajovými transakcemi.</span><span class="sxs-lookup"><span data-stu-id="6e39e-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="6e39e-110">Z účtenek můžete vytvořit ručně zadané výdajové transakce.</span><span class="sxs-lookup"><span data-stu-id="6e39e-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="6e39e-111">Připojení účtenek k výkazu výdajů</span><span class="sxs-lookup"><span data-stu-id="6e39e-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="6e39e-112">Chcete-li automaticky připojit účtenky, které zahrnují transakce kreditní kartou, když je vytvořen výkaz výdajů, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="6e39e-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="6e39e-113">Otevřete pracovní prostor **Správa výdajů**.</span><span class="sxs-lookup"><span data-stu-id="6e39e-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="6e39e-114">Na kartě **Účtenky** ověřte, zda existují nepřipojené účtenky.</span><span class="sxs-lookup"><span data-stu-id="6e39e-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="6e39e-115">Potvrzení můžete také odeslat na kartě **Účtenky**.</span><span class="sxs-lookup"><span data-stu-id="6e39e-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="6e39e-116">Na kartě **Výdaje** ověřte, zda existují nepřipojené výdaje.</span><span class="sxs-lookup"><span data-stu-id="6e39e-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="6e39e-117">Správce výdajů tyto náklady obvykle importuje od poskytovatele kreditní karty.</span><span class="sxs-lookup"><span data-stu-id="6e39e-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="6e39e-118">Vyberte **Nový výkaz výdajů**.</span><span class="sxs-lookup"><span data-stu-id="6e39e-118">Select **New expense report**.</span></span> <span data-ttu-id="6e39e-119">Všimněte si, že při vytváření výkazu výdajů můžete nyní zahrnout výdaje a účtenky.</span><span class="sxs-lookup"><span data-stu-id="6e39e-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="6e39e-120">Pokud přidáte výdaje i účtenky, spustí se automatické párování účtenek s výdaji.</span><span class="sxs-lookup"><span data-stu-id="6e39e-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="6e39e-121">Vytvoření nebo párování účtenek s výkazy výdajů</span><span class="sxs-lookup"><span data-stu-id="6e39e-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="6e39e-122">Chcete-li vytvořit výdaj nebo spárovat výdaj z účtenky, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="6e39e-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="6e39e-123">Na výkazu výdajů na kartě **Účtenky** připojte účtenky volbou **Přidat účtenky**.</span><span class="sxs-lookup"><span data-stu-id="6e39e-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="6e39e-124">Pod nahraným obrázkem účtenky si všimněte možností **Vytvořit** a **Párovat**.</span><span class="sxs-lookup"><span data-stu-id="6e39e-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="6e39e-125">Vyberte **Vytvořit** k vytvoření ručně zadané výdajové transakce a vyplnění hodnot, které jsou extrahovány z účtenky.</span><span class="sxs-lookup"><span data-stu-id="6e39e-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="6e39e-126">Pokud vyberete **Párovat**, systém se pokusí spárovat existující výdaj s účtenkou.</span><span class="sxs-lookup"><span data-stu-id="6e39e-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="6e39e-127">Instalace</span><span class="sxs-lookup"><span data-stu-id="6e39e-127">Installation</span></span>

<span data-ttu-id="6e39e-128">Chcete-li použít tyto pokročilé možnosti výdajů, nainstalujte si doplněk Služba správy výdajů pro Microsoft Dynamics 365 Finance a zapněte funkce ve vaší instanci.</span><span class="sxs-lookup"><span data-stu-id="6e39e-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="6e39e-129">K doplňku můžete přistupovat ze svého projektu v Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6e39e-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="6e39e-130">Přihlaste se do LCS a otevřete požadované prostředí.</span><span class="sxs-lookup"><span data-stu-id="6e39e-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="6e39e-131">Přejděte na **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="6e39e-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="6e39e-132">Vyberte **Udržovat**, nebo přejděte dolů záložku s náhledem **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="6e39e-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="6e39e-133">Vyberte **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="6e39e-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="6e39e-134">Zvolte **Služba správy výdajů**.</span><span class="sxs-lookup"><span data-stu-id="6e39e-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="6e39e-135">Postupujte podle instalačního průvodce a souhlaste s podmínkami.</span><span class="sxs-lookup"><span data-stu-id="6e39e-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="6e39e-136">Vyberte volbu **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="6e39e-136">Select **Install**.</span></span>

<span data-ttu-id="6e39e-137">V pracovním prostoru **Správa funkcí** zapněte následující funkce:</span><span class="sxs-lookup"><span data-stu-id="6e39e-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="6e39e-138">Nová verze výkazů výdajů</span><span class="sxs-lookup"><span data-stu-id="6e39e-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="6e39e-139">Automatické spárování a vytváření výdajů z účtenek</span><span class="sxs-lookup"><span data-stu-id="6e39e-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="6e39e-140">Po zapnutí těchto funkcí dojde k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="6e39e-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="6e39e-141">Existující pracovní prostor **Správa výdajů** je nahrazen novým pracovním prostorem.</span><span class="sxs-lookup"><span data-stu-id="6e39e-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="6e39e-142">Je přidána nová položka nabídky pro viditelnost pole výdajů.</span><span class="sxs-lookup"><span data-stu-id="6e39e-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="6e39e-143">Stále můžete otevřít bývalou stránku **Výkazy výdajů** přechodem na **Správa výdajů> Moje výdaje> Výkazy výdajů**.</span><span class="sxs-lookup"><span data-stu-id="6e39e-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="6e39e-144">Pracovní postupy a veškerá schválení vás stále budou zavádět na existujíc stránku s výkazy výdajů.</span><span class="sxs-lookup"><span data-stu-id="6e39e-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="6e39e-145">Účtenky budou zpracovány prostřednictvím Microsoft Azure Cognitive Services a metadata budou extrahována a přidána.</span><span class="sxs-lookup"><span data-stu-id="6e39e-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="6e39e-146">Přidá se možnost, která vám umožní vytvořit výkaz výdajů obsahující nespárované nepřipojené účtenky.</span><span class="sxs-lookup"><span data-stu-id="6e39e-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="6e39e-147">Možnost, která je přidána do výkazů výdajů, vám umožní vytvořit řádek výdajů z účtenky nebo se pokusí spárovat existující účtenku s existujícím řádkem výdajů.</span><span class="sxs-lookup"><span data-stu-id="6e39e-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="6e39e-148">Nejčastější dotazy</span><span class="sxs-lookup"><span data-stu-id="6e39e-148">Frequently asked questions</span></span>

<span data-ttu-id="6e39e-149">**Používá Microsoft moje data pro své modely?**</span><span class="sxs-lookup"><span data-stu-id="6e39e-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="6e39e-150">Ne, společnost Microsoft vytvořila obecný model strojové učení pro svou službu zpracování účtenek.</span><span class="sxs-lookup"><span data-stu-id="6e39e-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="6e39e-151">Tento model není založen na účtenkách, které nahrajete.</span><span class="sxs-lookup"><span data-stu-id="6e39e-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="6e39e-152">**Kde je tato funkce dostupná a zpracována?**</span><span class="sxs-lookup"><span data-stu-id="6e39e-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="6e39e-153">V současné době jsou podporovány Spojené státy.</span><span class="sxs-lookup"><span data-stu-id="6e39e-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="6e39e-154">**Kam jdou moje účtenky?**</span><span class="sxs-lookup"><span data-stu-id="6e39e-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="6e39e-155">Finance kontaktují Cognitive Services s cílem extrahovat data pole.</span><span class="sxs-lookup"><span data-stu-id="6e39e-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="6e39e-156">Během zpracování bude služba Cognitive Services uchovávat kopii vašeho dokladu až 24 hodin.</span><span class="sxs-lookup"><span data-stu-id="6e39e-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="6e39e-157">Po dokončení zpracování odebere Cognitive Services účtenku.</span><span class="sxs-lookup"><span data-stu-id="6e39e-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="6e39e-158">Účtenky jsou stále uloženy v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="6e39e-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="6e39e-159">Další informace naleznete v tématu [Povolit porozumění účtenkám s novou funkcí rozpoznávání formulářů](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="6e39e-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
