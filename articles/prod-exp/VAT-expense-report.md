---
title: Vratka DPH
description: Toto téma vysvětluje, jak získat zpět vratky u transakcí s DPH.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1be96521cdb486dd5a702cded615d3e1015b364
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073822"
---
# <a name="vat-recovery"></a><span data-ttu-id="917d7-103">Vratka DPH</span><span class="sxs-lookup"><span data-stu-id="917d7-103">VAT recovery</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="917d7-104">Aby společnost nebo organizace mohla dostávat vrácené částky za způsobilé transakce k dani z přidané hodnoty (DPH), musí identifikovat, shromažďovat, ověřovat a odesílat přesné informace.</span><span class="sxs-lookup"><span data-stu-id="917d7-104">To receive refunds on eligible value-added tax (VAT) transactions, a company or organization must identify, collect, verify, and submit accurate information.</span></span> <span data-ttu-id="917d7-105">Tento proces zahrnuje více úkolů a v závislosti na velikosti vaší společnosti může zahrnovat několik zaměstnanců nebo rolí.</span><span class="sxs-lookup"><span data-stu-id="917d7-105">This process includes multiple tasks and, depending on the size of your company, can include several employees or roles.</span></span>

<span data-ttu-id="917d7-106">Chcete-li získat zpět DPH pomocí modulu Správa výdajů, musí být splněny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="917d7-106">To recover VAT by using Expense management, the following prerequisites must be completed:</span></span>

- <span data-ttu-id="917d7-107">Kódy daně musí být vytvořeny pro země / oblasti, které jsou přiděleny do kategorií výdajů.</span><span class="sxs-lookup"><span data-stu-id="917d7-107">Tax codes must be created for countries/regions that are allocated to expense categories.</span></span>
- <span data-ttu-id="917d7-108">Pro každý daňový zákon musí být vytvořena skupina DPH.</span><span class="sxs-lookup"><span data-stu-id="917d7-108">A sales tax group must be created for each tax code.</span></span>
- <span data-ttu-id="917d7-109">Pro každou skupinu DPH musí být vytvořen kód DPH položky.</span><span class="sxs-lookup"><span data-stu-id="917d7-109">An item sales tax code must be created for each sales tax group.</span></span>

<span data-ttu-id="917d7-110">Po splnění nezbytných předpokladů zaměstnanci musejí provést následující kroky k vyžádání vratek za transakce s DPH.</span><span class="sxs-lookup"><span data-stu-id="917d7-110">After the prerequisites are completed, employees follow these steps to request refunds for VAT transactions.</span></span>

1. <span data-ttu-id="917d7-111">Ve vyúčtování výdajů zadejte daňové údaje o transakcích kreditní kartou, abyste identifikovali nároky na vrácení DPH.</span><span class="sxs-lookup"><span data-stu-id="917d7-111">On an expense report, enter tax information about credit card transactions to identify eligible VAT refunds.</span></span>
2. <span data-ttu-id="917d7-112">Ujistěte se, že jsou všechny daňové údaje úplné, a poté odešlete vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="917d7-112">Make sure that all tax information is complete, and then post the expense report.</span></span>
3. <span data-ttu-id="917d7-113">Zpracujte výdaje, které jsou způsobilé pro mezinárodní vratky DPH.</span><span class="sxs-lookup"><span data-stu-id="917d7-113">Process expenses that are eligible for international VAT recovery.</span></span>
4. <span data-ttu-id="917d7-114">Zašlete údaje o vratkách DPH prodejci třetí strany a podejte mezinárodní přiznání k vrácení.</span><span class="sxs-lookup"><span data-stu-id="917d7-114">Send VAT recovery data to the third-party vendor to file international recovery returns.</span></span>
5. <span data-ttu-id="917d7-115">Zpracujte výdaje na tuzemské vrácení DPH.</span><span class="sxs-lookup"><span data-stu-id="917d7-115">Process expenses for domestic VAT recovery.</span></span>

<span data-ttu-id="917d7-116">V následujících částech jsou uvedeny příklady, které ukazují, jak zaměstnanci společnosti Contoso dokončují jednotlivé kroky.</span><span class="sxs-lookup"><span data-stu-id="917d7-116">The following sections provide examples that show how Contoso employees complete each step.</span></span>

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a><span data-ttu-id="917d7-117">Ve vyúčtování výdajů zadejte daňové údaje o transakcích kreditní kartou, abyste identifikovali nároky na vrácení DPH</span><span class="sxs-lookup"><span data-stu-id="917d7-117">On an expense report, enter tax information about credit card transactions to identify eligible VAT refunds</span></span>

<span data-ttu-id="917d7-118">Nancy, obchodní zástupkyně společnosti Contoso se sídlem v USA, se nedávno vrátila z prodejní cesty do Velké Británie.</span><span class="sxs-lookup"><span data-stu-id="917d7-118">Nancy, a Contoso sales representative who is based in the US, recently returned from a sales trip to the United Kingdom.</span></span> <span data-ttu-id="917d7-119">Během výletu jí vznikly nějaké soukromé výdaje na kreditní kartě za jídlo.</span><span class="sxs-lookup"><span data-stu-id="917d7-119">During her trip, she incurred some personal credit card expenses for meals.</span></span> <span data-ttu-id="917d7-120">Nancy nyní musí vytvořit vyúčtování výdajů, aby sesouhlasila její výdaje.</span><span class="sxs-lookup"><span data-stu-id="917d7-120">Nancy must now create an expense report to reconcile her expenses.</span></span>

<span data-ttu-id="917d7-121">Když Nancy zadá informace ve svém vyúčtování výdajů, vybere v poli **Země/region** na stránce **Upravit vyúčtování výdajů** možnost **Spojené království**.</span><span class="sxs-lookup"><span data-stu-id="917d7-121">When Nancy enters information on her expense report, she selects **United Kingdom** in the **Country/region** field on the **Edit expense report** page.</span></span> <span data-ttu-id="917d7-122">Seznam skupin DPH je poté filtrován, takže zobrazuje pouze skupiny, které se vztahují na Spojené království.</span><span class="sxs-lookup"><span data-stu-id="917d7-122">The list of sales tax groups is then filtered so that it shows only the groups that apply to the United Kingdom.</span></span> <span data-ttu-id="917d7-123">Nancy vybere skupinu DPH **Spojené království 001** a poté vybere skupinu DPH **Jídla**.</span><span class="sxs-lookup"><span data-stu-id="917d7-123">Nancy selects the **United Kingdom 001** sales tax group and then selects the **Meals** item sales tax group.</span></span> <span data-ttu-id="917d7-124">Poté přidá novou transakci za její ubytování.</span><span class="sxs-lookup"><span data-stu-id="917d7-124">She then adds a new transaction for her lodging.</span></span> <span data-ttu-id="917d7-125">Protože pro ubytování ve Spojeném království existuje pouze jedna skupina DPH a skupina daně z prodeje zboží, tyto informace se automaticky vyplní v Nancyně vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="917d7-125">Because there is only one sales tax group and item sales tax group for lodging in the United Kingdom, this information is automatically filled in on Nancy's expense report.</span></span>

<span data-ttu-id="917d7-126">Podle zásad společnosti Contoso musí mít všechny výdaje odpovídající potvrzení.</span><span class="sxs-lookup"><span data-stu-id="917d7-126">Per Contoso policy, all expenses must have a matching receipt.</span></span> <span data-ttu-id="917d7-127">Když tedy Nancy uloží své vyúčtování výdajů, obdrží zprávu, která uvádí, že musí připojit potvrzení o každé transakci, kterou uvedla ve svém vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="917d7-127">Therefore, when Nancy saves her expense report, she receives a message that states that she must attach a receipt for each transaction that she listed on her expense report.</span></span> <span data-ttu-id="917d7-128">Nancy ověří, že ke svému vyúčtování výdajů připojila digitální snímek potvrzení každé transakce, a poté odešle vyúčtování ke schválení.</span><span class="sxs-lookup"><span data-stu-id="917d7-128">Nancy verifies that she has attached a digital image of each transaction receipt to her expense report and then submits her report for approval.</span></span> <span data-ttu-id="917d7-129">Poté odešle papírové příjemky týmu zpracování back-office.</span><span class="sxs-lookup"><span data-stu-id="917d7-129">She then sends the paper receipts to the back-office processing team.</span></span> <span data-ttu-id="917d7-130">Tento tým odešle údaje o vratce DPH dodavateli třetí strany, který pro společnost Contoso podává mezinárodní přiznání k vrácení DPH.</span><span class="sxs-lookup"><span data-stu-id="917d7-130">This team will send the VAT recovery data to the third-party vendor that files international VAT recovery returns for Contoso.</span></span>

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a><span data-ttu-id="917d7-131">Ujistěte se, že jsou všechny daňové údaje úplné, a poté odešlete vyúčtování výdajů</span><span class="sxs-lookup"><span data-stu-id="917d7-131">Make sure that all tax information is complete, and then post the expense report</span></span>

<span data-ttu-id="917d7-132">Než bude moci April, koordinátorka účtů pro společnost Contoso zaúčtovat sestavu výdajů, musí zadat všechny daňové informace, které v něm chybí.</span><span class="sxs-lookup"><span data-stu-id="917d7-132">April, the Accounts payable coordinator for Contoso, must enter any tax information that is missing from an expense report before the report can be posted.</span></span> <span data-ttu-id="917d7-133">Otevře stránku **Podrobnosti vyúčtování výdajů** a uvidí schválené vyúčtování výdajů Nancy.</span><span class="sxs-lookup"><span data-stu-id="917d7-133">She opens the **Expense report details** page and sees Nancy's approved expense report.</span></span> <span data-ttu-id="917d7-134">April poté otevře vyúčtování výdajů a zobrazí podrobnosti transakcí.</span><span class="sxs-lookup"><span data-stu-id="917d7-134">April then opens the expense report to view the details of the transactions.</span></span> <span data-ttu-id="917d7-135">Vidí, že Nancy pro jednu z transakcí nezadala skupinu DPH.</span><span class="sxs-lookup"><span data-stu-id="917d7-135">She sees that Nancy didn't enter an item sales tax group for one of the transactions.</span></span> <span data-ttu-id="917d7-136">Protože tyto informace nejsou poskytnuty, April nemůže zaúčtovat vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="917d7-136">Because this information isn't provided, April can't post the expense report.</span></span> <span data-ttu-id="917d7-137">Proto April přejde na stránku **Daňové konfigurace** v okně Správa výdajů a najde příslušnou skupinu DPH pro danou zemi / region a typ transakce.</span><span class="sxs-lookup"><span data-stu-id="917d7-137">Therefore, April looks on the **Tax configurations** page in Expense management, and finds the appropriate item sales tax group for the country/region and the transaction type.</span></span> <span data-ttu-id="917d7-138">April nyní může zaúčtovat vyúčtování výdajů do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="917d7-138">April can now post the expense report to the general ledger.</span></span>

<span data-ttu-id="917d7-139">Když April zaúčtuje vyúčtování výdajů, vytvoří se pracovní položka s možností vrácení DPH.</span><span class="sxs-lookup"><span data-stu-id="917d7-139">When April posts the expense report, a VAT recoverable work item is created.</span></span> <span data-ttu-id="917d7-140">Tato pracovní položka je přiřazena členovi týmu zpracování back-office.</span><span class="sxs-lookup"><span data-stu-id="917d7-140">This work item is assigned to a member of the back-office processing team.</span></span> <span data-ttu-id="917d7-141">April obdrží zprávu, která potvrzuje, že zaúčtování bylo úspěšné.</span><span class="sxs-lookup"><span data-stu-id="917d7-141">April receives a message that confirms that posting was successful.</span></span> <span data-ttu-id="917d7-142">Tato zpráva také uvádí počet transakcí s DPH, které byly identifikovány k vrácení.</span><span class="sxs-lookup"><span data-stu-id="917d7-142">This message also lists the number of VAT transactions that were identified for recovery.</span></span>

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a><span data-ttu-id="917d7-143">Zpracování výdajů, které jsou způsobilé pro mezinárodní vratky DPH</span><span class="sxs-lookup"><span data-stu-id="917d7-143">Process expenses that are eligible for international VAT recovery</span></span>

<span data-ttu-id="917d7-144">Arnie, člen týmu pro zpracování back-office společnosti Contoso, je odpovědný za potvrzení, že jsou ve vyúčtováních výdajů zahrnuty všechny požadované informace pro vrácení DPH.</span><span class="sxs-lookup"><span data-stu-id="917d7-144">Arnie, a member of Contoso's back-office processing team, is responsible for confirming that all the required information for VAT recovery is included on expense reports.</span></span> <span data-ttu-id="917d7-145">Otevře stránku **Vratka daně z výdajů** a vybere vyúčtování výdajů, které Nancy odeslala.</span><span class="sxs-lookup"><span data-stu-id="917d7-145">He opens the **Expense tax recovery** page and selects the expense report that Nancy submitted.</span></span> <span data-ttu-id="917d7-146">Arnie ověří, zda jsou připojeny všechny požadované příjemky a zda byly zadány správné kódy skupiny DPH a položky DPH.</span><span class="sxs-lookup"><span data-stu-id="917d7-146">Arnie verifies that all the required receipts are attached, and that the correct sales tax group and item sales tax codes were entered.</span></span>

<span data-ttu-id="917d7-147">Když Arnie obdrží papírové příjemky od Nancy, ověří papírové příjemky vůči digitálním příjemkám a poté změní stav vyúčtování výdajů na **Připraveno k vratce**.</span><span class="sxs-lookup"><span data-stu-id="917d7-147">When Arnie receives the paper receipts from Nancy, he verifies the paper receipts against the digital receipts and then changes the status of the expense report to **Ready for recovery**.</span></span>

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a><span data-ttu-id="917d7-148">Zašlete údaje o vratkách DPH prodejci třetí strany a podejte mezinárodní přiznání k vrácení</span><span class="sxs-lookup"><span data-stu-id="917d7-148">Send VAT recovery data to the third-party vendor to file international recovery returns</span></span>

<span data-ttu-id="917d7-149">Když je Arnie připraven odeslat data vyúčtování výdajů prodejci třetí strany, který bude podávat přiznání k vrácení DPH, otevře stránku **Vrácení daně z výdajů**.</span><span class="sxs-lookup"><span data-stu-id="917d7-149">When Arnie is ready to send the expense report data to the third-party vendor that will file the VAT recovery returns, he opens the **Expense tax recovery** page.</span></span> <span data-ttu-id="917d7-150">Filtruje stránku tak, aby zobrazovala pouze vyúčtování výdajů, která jsou označena jako **Připraveno k vrácení**.</span><span class="sxs-lookup"><span data-stu-id="917d7-150">He filters the page so that it shows only the expense reports that are marked as **Ready for recovery**.</span></span> <span data-ttu-id="917d7-151">Arnie pak vybere **Soubor** &gt; **Exportovat do aplikace Excel**.</span><span class="sxs-lookup"><span data-stu-id="917d7-151">Arnie then selects **File** &gt; **Export to Excel**.</span></span> <span data-ttu-id="917d7-152">Informace o DPH z vyúčtování výdajů se exportují do listu aplikace Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="917d7-152">The VAT information from the expense reports is exported to a Microsoft Excel worksheet.</span></span> <span data-ttu-id="917d7-153">Arnie odešle tento list prodejci třetí strany a přidá zprávu, která uvádí, že papírové stvrzenky byly odeslány kurýrem.</span><span class="sxs-lookup"><span data-stu-id="917d7-153">Arnie submits this worksheet to the third-party vendor and includes a message that states that the paper receipts have been sent by courier.</span></span>

## <a name="process-expenses-for-domestic-vat-recovery"></a><span data-ttu-id="917d7-154">Zpracování výdajů na tuzemské vrácení DPH</span><span class="sxs-lookup"><span data-stu-id="917d7-154">Process expenses for domestic VAT recovery</span></span>

<span data-ttu-id="917d7-155">Arnie musí ověřit, že transakce vyúčtování výdajů jsou způsobilé k vrácení DPH a že digitální příjmy jsou připojeny k vyúčtováním.</span><span class="sxs-lookup"><span data-stu-id="917d7-155">Arnie must verify that the expense report transactions are eligible for VAT recovery, and that the digital receipts are attached to the reports.</span></span> <span data-ttu-id="917d7-156">Aby mohl začít zpracovávat způsobilé výdaje k domácímu vymáhání, otevře Arnie stránku **Vrácení daně z výdajů** a vybere vyúčtování výdajů, který vyžaduje ověření.</span><span class="sxs-lookup"><span data-stu-id="917d7-156">To start to process eligible expenses for domestic recovery, Arnie opens the **Expense tax recovery** page and selects the expense report that requires verification.</span></span> <span data-ttu-id="917d7-157">Ověří, že příjmy jsou zadány jménem společnosti a nikoli zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="917d7-157">He verifies that receipts are in the name of the company instead of the employee.</span></span> <span data-ttu-id="917d7-158">Pro vrácení DPH musí být příjemky vystaveny na název společnosti.</span><span class="sxs-lookup"><span data-stu-id="917d7-158">For VAT recovery, receipts must be in the name of the company.</span></span> <span data-ttu-id="917d7-159">Arnie poté potvrdí, že byly použity správné kódy skupiny DPH a položky DPH.</span><span class="sxs-lookup"><span data-stu-id="917d7-159">Arnie then confirms that the correct sales tax group and item sales tax codes were applied.</span></span>

<span data-ttu-id="917d7-160">Když Arnie obdrží papírové stvrzenky, změní stav vyúčtování výdajů na **Připraveno k vratce**.</span><span class="sxs-lookup"><span data-stu-id="917d7-160">When Arnie receives the paper receipts, he changes the status of the expense report to **Ready for recovery**.</span></span> <span data-ttu-id="917d7-161">Poté může podat přiznání u příslušného daňového úřadu.</span><span class="sxs-lookup"><span data-stu-id="917d7-161">He can then file the return with the appropriate tax authority.</span></span> <span data-ttu-id="917d7-162">V tomto případě je příslušným daňovým úřadem v USA Internal Revenue Service (IRS).</span><span class="sxs-lookup"><span data-stu-id="917d7-162">In this case, the appropriate tax authority in the US is the Internal Revenue Service (IRS).</span></span>