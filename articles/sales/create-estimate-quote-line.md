---
title: Vytvoření odhadů na řádku nabídky
description: Toto téma poskytuje informace o tom, jak vytvořit odhad na řádku nabídky pro projekt.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e841ab7c37e0b348a4d1570123a5aea00ede0047
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898479"
---
# <a name="create-estimates-on-a-quote-line"></a><span data-ttu-id="18388-103">Vytvoření odhadů na řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="18388-103">Create estimates on a quote line</span></span>

<span data-ttu-id="18388-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="18388-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="18388-105">U nabídky založené na projektu můžete pomocí entity Podrobnosti řádku nabídky odhadnout práci, která je požadována pro dodání projektu.</span><span class="sxs-lookup"><span data-stu-id="18388-105">On a project-based quote, you can use the Quote line detail entity to estimate the work that is required to deliver a project.</span></span> <span data-ttu-id="18388-106">Tento odhad pak můžete sdílet se zákazníkem.</span><span class="sxs-lookup"><span data-stu-id="18388-106">You can then share that estimate with the customer.</span></span>

<span data-ttu-id="18388-107">Řádky nabídky založené na projektu nebudou muset obsahovat žádné podrobnosti řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="18388-107">Project-based quote lines don't have to have any quote line details.</span></span> <span data-ttu-id="18388-108">Alternativně mohou obsahovat mnoho podrobností řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="18388-108">Alternatively, they can have many quote line details.</span></span> <span data-ttu-id="18388-109">Podrobnosti řádku nabídky se používají k odhadu času, výdajů nebo poplatků.</span><span class="sxs-lookup"><span data-stu-id="18388-109">Quote line details are used to estimate time, expenses, or fees.</span></span> <span data-ttu-id="18388-110">Dynamics 365 Project Operations neumožňuje u podrobností řádku nabídky materiálové odhady.</span><span class="sxs-lookup"><span data-stu-id="18388-110">Dynamics 365 Project Operations doesn't allow for material estimates on quote line details.</span></span> <span data-ttu-id="18388-111">Ty se nazývají třídy transakcí.</span><span class="sxs-lookup"><span data-stu-id="18388-111">These are called transaction classes.</span></span> <span data-ttu-id="18388-112">Odhadované částky daně lze zadat také do třídy transakcí.</span><span class="sxs-lookup"><span data-stu-id="18388-112">Estimated tax amounts can also be entered on a transaction class.</span></span>

<span data-ttu-id="18388-113">Kromě tříd transakcí, obsahují podrobnosti řádku nabídky mají typ transakce.</span><span class="sxs-lookup"><span data-stu-id="18388-113">In addition to transaction classes, quote line details have a transaction type.</span></span> <span data-ttu-id="18388-114">Existují dva typy transakcí pro podrobnosti řádku nabídky, **Náklady** a **Projektová smlouva**.</span><span class="sxs-lookup"><span data-stu-id="18388-114">There are two transaction types for quote line details, **Cost** and **Project Contract**.</span></span>

## <a name="estimate-by-using-a-contract"></a><span data-ttu-id="18388-115">Odhad pomocí smlouvy</span><span class="sxs-lookup"><span data-stu-id="18388-115">Estimate by using a contract</span></span>

<span data-ttu-id="18388-116">Pokud jste při vytváření smlouvy založené na projektu použili nabídku Project Operations, bude odhad, který jste udělali pro každý řádek nabídky v nabídce, zkopírován do projektové smlouvy.</span><span class="sxs-lookup"><span data-stu-id="18388-116">If you used a Project Operations quote when you created a project-based contract, the estimate that you did for each quote line on the quote is copied to the project contract.</span></span> <span data-ttu-id="18388-117">Struktura projektové smlouvy se podobá struktuře projektové nabídky, která obsahuje řádky, podrobnosti řádků a rozpisy faktur.</span><span class="sxs-lookup"><span data-stu-id="18388-117">The structure of a project contract is like the structure of project quote that has lines, line details, and invoice schedules.</span></span>

<span data-ttu-id="18388-118">Odhady lze provádět přímo v projektové smlouvě, jako v projektové nabídce.</span><span class="sxs-lookup"><span data-stu-id="18388-118">Estimates can be done directly in a project contract, as in a project quote.</span></span> <span data-ttu-id="18388-119">U projektové nabídky se odhad provádí pomocí řádků smlouvy a podrobností řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="18388-119">For a project quotation, the estimate is done by using contract lines and contract line details.</span></span> <span data-ttu-id="18388-120">Podrobnosti řádku smlouvy lze také vygenerovat z projektového plánu, který byl vytvořen pomocí metody odhadu zdola nahoru.</span><span class="sxs-lookup"><span data-stu-id="18388-120">Contract line details can also be generated from a project plan that was created by using the bottom-up estimate approach.</span></span>

<span data-ttu-id="18388-121">Podrobnosti řádku smlouvy lze použít k odhadu času, výdajů nebo poplatků.</span><span class="sxs-lookup"><span data-stu-id="18388-121">Contract line details can be used to estimate time, expenses, or fees.</span></span> <span data-ttu-id="18388-122">Odhadované částky daně lze zadat také do podrobností řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="18388-122">Estimated tax amounts can also be entered on a contract line detail.</span></span>

<span data-ttu-id="18388-123">Na podrobnostech řádku smlouvy nejsou materiálové odhady povoleny.</span><span class="sxs-lookup"><span data-stu-id="18388-123">Material estimates are not allowed on contract line details.</span></span>

<span data-ttu-id="18388-124">Procesy, které jsou podporovány ve smlouvě o projektu, jsou vytvoření a potvrzení faktury.</span><span class="sxs-lookup"><span data-stu-id="18388-124">The processes that are supported on a project contract are invoice creation and confirmation.</span></span> <span data-ttu-id="18388-125">Vytvoření faktury vytvoří koncept faktury založené na projektu, který zahrnuje všechny skutečné hodnoty nefakturovaného prodeje do aktuálního data.</span><span class="sxs-lookup"><span data-stu-id="18388-125">Invoice creation creates a draft of a project-based invoice that includes all unbilled sales actuals until the current date.</span></span>

<span data-ttu-id="18388-126">Po potvrzení je smlouva jen pro čtení a její stav se změní z **Koncept** na **Potvrzeno**.</span><span class="sxs-lookup"><span data-stu-id="18388-126">Confirmation makes the contract read-only and changes its status from **Draft** to **Confirmed**.</span></span> <span data-ttu-id="18388-127">Jakmile tuto akci provedete, nelze ji vrátit zpět.</span><span class="sxs-lookup"><span data-stu-id="18388-127">After you take this action, you can't undo it.</span></span> <span data-ttu-id="18388-128">Vzhledem k tomu, že tato akce je trvalá, je vhodné udržovat smlouvu ve stavu **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="18388-128">Because this action is permanent, it's a best practice to keep the contract in a **Draft** status.</span></span>

<span data-ttu-id="18388-129">Jedinými rozdíly mezi koncepty smluv a potvrzenými smlouvami je jejich stav a skutečnost, že koncept smluv lze upravit, zatímco potvrzené smlouvy nelze.</span><span class="sxs-lookup"><span data-stu-id="18388-129">The only differences between draft contracts and confirmed contracts are their status and the fact that draft contracts can be edited whereas confirmed contracts can't.</span></span> <span data-ttu-id="18388-130">Vytváření faktur a sledování skutečných hodnot lze provádět u konceptů smluv i u potvrzených smluv.</span><span class="sxs-lookup"><span data-stu-id="18388-130">Invoice creation and tracking actuals can be done on both draft contracts and confirmed contracts.</span></span>

<span data-ttu-id="18388-131">U smluv nebo projektů nejsou změnové příkazy podporovány.</span><span class="sxs-lookup"><span data-stu-id="18388-131">Change orders are not supported on contracts or projects.</span></span>

## <a name="estimating-projects"></a><span data-ttu-id="18388-132">Odhady projektů</span><span class="sxs-lookup"><span data-stu-id="18388-132">Estimating projects</span></span>

<span data-ttu-id="18388-133">Můžete odhadnout čas a výdaje na projekty, ale nikoliv materiály nebo poplatky.</span><span class="sxs-lookup"><span data-stu-id="18388-133">You can estimate time and expenses on projects but not materials or fees.</span></span>

<span data-ttu-id="18388-134">Odhady času se generují při vytvoření úkolu a určení atributů obecného zdroje, který je vyžadován k provedení úkolu.</span><span class="sxs-lookup"><span data-stu-id="18388-134">Time estimates are generated when you create a task and identify the attributes of a generic resource that is required to perform the task.</span></span> <span data-ttu-id="18388-135">Odhady času jsou generovány z plánování úkolů.</span><span class="sxs-lookup"><span data-stu-id="18388-135">Time estimates are generated from schedule tasks.</span></span> <span data-ttu-id="18388-136">Odhady času nejsou vytvářeny, pokud vytváříte obecné členy týmu mimo kontext plánu.</span><span class="sxs-lookup"><span data-stu-id="18388-136">Time estimates aren't created if you create generic team members outside the context of the schedule.</span></span>

<span data-ttu-id="18388-137">Odhady výdajů se zapisují do mřížky na stránce **Odhady**.</span><span class="sxs-lookup"><span data-stu-id="18388-137">Expense estimates are entered in the grid on the **Estimates** page.</span></span>

## <a name="understand-estimation"></a><span data-ttu-id="18388-138">Porozumění odhadům</span><span class="sxs-lookup"><span data-stu-id="18388-138">Understand estimation</span></span>

<span data-ttu-id="18388-139">Následující tabulku použijte jako vodítko pro pochopení obchodní logiky ve fázi odhadu.</span><span class="sxs-lookup"><span data-stu-id="18388-139">Use the following table as a guide for understanding the business logic in the estimation phase.</span></span>

| <span data-ttu-id="18388-140">Situace</span><span class="sxs-lookup"><span data-stu-id="18388-140">Scenario</span></span>                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="18388-141">Záznam entity</span><span class="sxs-lookup"><span data-stu-id="18388-141">Entity record</span></span>                                                                                                                                                                                                       | <span data-ttu-id="18388-142">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="18388-142">Transaction Type</span></span> | <span data-ttu-id="18388-143">Třída transakce</span><span class="sxs-lookup"><span data-stu-id="18388-143">Transaction Class</span></span> | <span data-ttu-id="18388-144">Další informace</span><span class="sxs-lookup"><span data-stu-id="18388-144">Additional information</span></span>                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="18388-145">Potřebujete-li odhadnout prodejní hodnotu času v nabídce</span><span class="sxs-lookup"><span data-stu-id="18388-145">When you need to estimate the sales value of time on a quote</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="18388-146">Je vytvořen záznam Podrobnosti řádku nabídky (PŘN).</span><span class="sxs-lookup"><span data-stu-id="18388-146">Quote line detail (QLD) record is created</span></span>                                                                                                                                                                               | <span data-ttu-id="18388-147">Projektová smlouva</span><span class="sxs-lookup"><span data-stu-id="18388-147">Project contract</span></span> | <span data-ttu-id="18388-148">Time</span><span class="sxs-lookup"><span data-stu-id="18388-148">Time</span></span>        | <span data-ttu-id="18388-149">Pole Původ transakce na řádku PŘN strany prodeje odkazuje na PŘN strany nákladů</span><span class="sxs-lookup"><span data-stu-id="18388-149">Transaction origin field on the sales side QLD row references the Cost side QLD</span></span> |
|                                                                                                                                                                                                                                                                                     | <span data-ttu-id="18388-150">Systém vytvoří druhý záznam PŘN, který bude uchovávat odpovídající hodnoty nákladů.</span><span class="sxs-lookup"><span data-stu-id="18388-150">A second QLD record is created by the system to store the corresponding cost values.</span></span> <span data-ttu-id="18388-151">Systém zkopíruje všechna nepeněžní pole z PŘN prodeje do PŘN nákladů.</span><span class="sxs-lookup"><span data-stu-id="18388-151">All non-money fields are copied from the sales QLD to the Cost QLD by the system.</span></span>                                                                                                                                                                               | <span data-ttu-id="18388-152">Náklady</span><span class="sxs-lookup"><span data-stu-id="18388-152">Cost</span></span> | <span data-ttu-id="18388-153">Time</span><span class="sxs-lookup"><span data-stu-id="18388-153">Time</span></span>        | <span data-ttu-id="18388-154">Pole Původ transakce na řádku PŘN strany prodeje odkazuje na PŘN strany nákladů</span><span class="sxs-lookup"><span data-stu-id="18388-154">Transaction origin field on the sales side quote line detail (QLD) row references the Cost side QLD</span></span> |
| <span data-ttu-id="18388-155">Potřebujete-li odhadnout prodejní hodnotu času ve smlouvě</span><span class="sxs-lookup"><span data-stu-id="18388-155">When you need to estimate the sales value of time on a contract</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="18388-156">Je vytvořen záznam Podrobnosti řádku projektové smlouvy (PŘS).</span><span class="sxs-lookup"><span data-stu-id="18388-156">Project contract line detail (CLD) record is created</span></span>                                                                                                                                                                    | <span data-ttu-id="18388-157">Projektová smlouva</span><span class="sxs-lookup"><span data-stu-id="18388-157">Project Contract</span></span> | <span data-ttu-id="18388-158">Time</span><span class="sxs-lookup"><span data-stu-id="18388-158">Time</span></span>        | <span data-ttu-id="18388-159">Pole Původ transakce na řádku PŘS strany prodeje odkazuje na PŘS nákladů</span><span class="sxs-lookup"><span data-stu-id="18388-159">Transaction origin field on the sales side CLD row references the cost CLD</span></span>      |
|                                                                                                                                                                                                                                                                                  | <span data-ttu-id="18388-160">Systém vytvoří druhý záznam PŘS, který bude uchovávat odpovídající hodnoty nákladů.</span><span class="sxs-lookup"><span data-stu-id="18388-160">A second CLD record is created by the system to store the corresponding cost values.</span></span> <span data-ttu-id="18388-161">Systém zkopíruje všechna nepeněžní pole z PŘS prodeje do PŘS nákladů.</span><span class="sxs-lookup"><span data-stu-id="18388-161">All non-money fields are copied from the sales CLD to the cost CLD by the system.</span></span>                                                                                                                                                                    | <span data-ttu-id="18388-162">Náklady</span><span class="sxs-lookup"><span data-stu-id="18388-162">Cost</span></span> | <span data-ttu-id="18388-163">Time</span><span class="sxs-lookup"><span data-stu-id="18388-163">Time</span></span>        | <span data-ttu-id="18388-164">Pole Původ transakce na řádku PŘS strany prodeje odkazuje na PŘS nákladů</span><span class="sxs-lookup"><span data-stu-id="18388-164">Transaction origin field on the sales side CLD row references the cost CLD</span></span>      |
| <span data-ttu-id="18388-165">Pokud uživatel popisuje zdroj v úkolu projektu</span><span class="sxs-lookup"><span data-stu-id="18388-165">When the user describes a resource on a project task</span></span>                                                                                                                                                                                                                                                                                            | <span data-ttu-id="18388-166">Záznam řádku odhadu pro zobrazení hodnoty prodeje úkolu je vytvořen při vytvoření úkolu se všemi požadovanými cenovými dimenzemi.</span><span class="sxs-lookup"><span data-stu-id="18388-166">Estimate line record to show the sales value of the task is created when a task is created with all required pricing dimensions.</span></span> <span data-ttu-id="18388-167">Role a organizační jednotky jsou cenovými dimenzemi</span><span class="sxs-lookup"><span data-stu-id="18388-167">Role and organizational units are the pricing dimensions</span></span> | <span data-ttu-id="18388-168">Projektová smlouva</span><span class="sxs-lookup"><span data-stu-id="18388-168">Project Contract</span></span> | <span data-ttu-id="18388-169">Čas</span><span class="sxs-lookup"><span data-stu-id="18388-169">Time</span></span>        |                                                                                   |
|     | <span data-ttu-id="18388-170">Záznam řádku odhadu pro zobrazení hodnoty nákladů úkolu je vytvořen při vytvoření úkolu se všemi požadovanými cenovými dimenzemi.</span><span class="sxs-lookup"><span data-stu-id="18388-170">The estimate line record to show the cost value of the task is created when a task is created with all required pricing dimensions.</span></span> <span data-ttu-id="18388-171">Systém zkopíruje všechna nepeněžní pole z řádku odhadu prodeje do řádku odhadu nákladů.</span><span class="sxs-lookup"><span data-stu-id="18388-171">All non-money fields are copied from the sales estimate line to the cost estimate line by the system.</span></span> <span data-ttu-id="18388-172">Role a organizační jednotka jsou cenovými dimenzemi pro nákladové a fakturační sazby.</span><span class="sxs-lookup"><span data-stu-id="18388-172">Role and organizational unit are the pricing dimensions for both cost and bill rates.</span></span>                                                                                                                                                                                                                | <span data-ttu-id="18388-173">Náklady</span><span class="sxs-lookup"><span data-stu-id="18388-173">Cost</span></span>             | <span data-ttu-id="18388-174">Čas</span><span class="sxs-lookup"><span data-stu-id="18388-174">Time</span></span>           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a><span data-ttu-id="18388-175">Přizpůsobení entit Podrobnosti řádku nabídky a Podrobnosti řádku smlouvy</span><span class="sxs-lookup"><span data-stu-id="18388-175">Customize the Quote line detail and Contract line detail entities</span></span>

<span data-ttu-id="18388-176">Pokud jste na řádku podrobností nabídky přidali vlastní pole a chcete, aby systém zadal hodnotu pole jako výchozí hodnotu na souvisejícím řádku nákladů, který vytvoří, použijte nástroje pro registraci modulů plug-in PreOperationContractLineDetailUpdate a PreOperationQuoteLineDetailUpdate.</span><span class="sxs-lookup"><span data-stu-id="18388-176">If you added a custom field on the quote line detail and want the system to enter the value of the field as a default value on the related cost line that it creates, use the PreOperationContractLineDetailUpdate and PreOperationQuoteLineDetailUpdate plug-in registration tools.</span></span> <span data-ttu-id="18388-177">Tyto moduly plug-in je nutné znovu zaregistrovat po změně podrobností řádku nabídky nebo řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="18388-177">These plug-ins must be re-registered after the quote line detail or the contract line detail is changed.</span></span> <span data-ttu-id="18388-178">Postup pro dokončení tohoto procesu:</span><span class="sxs-lookup"><span data-stu-id="18388-178">Follow these steps to complete the process.</span></span>

1. <span data-ttu-id="18388-179">Otevřete PluginRegistrationTool a připojte se k vaší online instanci.</span><span class="sxs-lookup"><span data-stu-id="18388-179">Open PluginRegistrationTool, and connect to your online instance.</span></span>
2. <span data-ttu-id="18388-180">Vyberte **Hledat** a vyhledejte modul plug-in, který chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="18388-180">Select **Search**, and search for the plug-in to update.</span></span>
3. <span data-ttu-id="18388-181">Vyberte modul plug-in a poté na hlavní stránce vyberte **Vybrat**.</span><span class="sxs-lookup"><span data-stu-id="18388-181">Select the plug-in, and then, on the main page, select **Select**.</span></span>
4. <span data-ttu-id="18388-182">Vyberte krok modulu plug-in, který chcete aktualizovat, klikněte pravým tlačítkem myši a vyberte **Aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="18388-182">Select the step of the plug-in to update, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="18388-183">V dialogovém okně **Aktualizovat existující krok** vyberte v poli **Atributy filtrování** tlačítko se třemi tečkami (**…**):</span><span class="sxs-lookup"><span data-stu-id="18388-183">In the **Update Existing Step** dialog box, in the **Filtering Attributes** field, select the ellipsis button (**...**):</span></span>
6. <span data-ttu-id="18388-184">V dialogovém **Vybrat atributy** zaškrtněte zaškrtávací políčka u vlastních atributů.</span><span class="sxs-lookup"><span data-stu-id="18388-184">In the **Select Attributes** dialog box, select check boxes for custom attributes.</span></span>
7. <span data-ttu-id="18388-185">Klepnutím na **OK** zavřete dialogové okno a pak vyberte **Aktualizovat krok**.</span><span class="sxs-lookup"><span data-stu-id="18388-185">Select **OK** to close the dialog box, and then select **Update Step**.</span></span>
8. <span data-ttu-id="18388-186">Opakujte kroky 1 až 7 pro druhý modul plug-in.</span><span class="sxs-lookup"><span data-stu-id="18388-186">Repeat steps 1 through 7 for the second plug-in.</span></span>
9. <span data-ttu-id="18388-187">Zavřete PluginRegistrationTool.</span><span class="sxs-lookup"><span data-stu-id="18388-187">Close the PluginRegistrationTool.</span></span>