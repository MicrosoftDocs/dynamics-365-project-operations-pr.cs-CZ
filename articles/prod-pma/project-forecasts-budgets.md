---
title: Projektové předpovědi a rozpočty
description: Microsoft Dynamics 365 Finance poskytuje projektové předpovědi a rozpočty pro správu a řízení vašich projektů.
author: Yowelle
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f99c00effbb0678f1f55e5068a7128cbfb86f5ce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073893"
---
# <a name="project-forecasts-and-budgets"></a><span data-ttu-id="7dd95-103">Projektové předpovědi a rozpočty</span><span class="sxs-lookup"><span data-stu-id="7dd95-103">Project forecasts and budgets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7dd95-104">Projekty můžete spravovat a řídit dvěma způsoby: pomocí projektových předpovědí nebo rozpočtů.</span><span class="sxs-lookup"><span data-stu-id="7dd95-104">There are two ways to manage and control your projects: project forecasts and project budgets.</span></span> 

<span data-ttu-id="7dd95-105">Pokud má vaše organizace provozní perspektivu a pokud se zaměřuje na výnosy a náklady odvozené z konkrétních transakcí, použijte projektové předpovědi.</span><span class="sxs-lookup"><span data-stu-id="7dd95-105">Use project forecasting if your organization has an operational perspective, and if it focuses on revenues and costs that are derived from specific transactions.</span></span> <span data-ttu-id="7dd95-106">Pokud se vaše organizace více zaměřuje na finanční částky, použijte rozpočtování projektů.</span><span class="sxs-lookup"><span data-stu-id="7dd95-106">Use project budgeting if your organization focuses more on the financial amounts.</span></span> 

<span data-ttu-id="7dd95-107">Projektové předpovědi i rozpočty používají modely předpovědí k uchovávání předpokládaných částek transakcí.</span><span class="sxs-lookup"><span data-stu-id="7dd95-107">Both project forecasts and project budgets use forecast models to hold the projected transaction amounts.</span></span> 

<span data-ttu-id="7dd95-108">Každá metoda má svoje výhody.</span><span class="sxs-lookup"><span data-stu-id="7dd95-108">Each method has its advantages.</span></span> <span data-ttu-id="7dd95-109">Než vyberete metodu pro vaši organizaci, měli byste zvážit následující body.</span><span class="sxs-lookup"><span data-stu-id="7dd95-109">You should consider the following points before you select a method for your organization.</span></span>

|   <span data-ttu-id="7dd95-110">Metoda přidělení</span><span class="sxs-lookup"><span data-stu-id="7dd95-110">Allocation method</span></span>       |           <span data-ttu-id="7dd95-111">Projektové předpovědi</span><span class="sxs-lookup"><span data-stu-id="7dd95-111">Project forecasting</span></span>            |        <span data-ttu-id="7dd95-112">Rozpočtování projektů</span><span class="sxs-lookup"><span data-stu-id="7dd95-112">Project budgeting</span></span>                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="7dd95-113">**Přidělení období**</span><span class="sxs-lookup"><span data-stu-id="7dd95-113">**Period allocation**</span></span>     | <span data-ttu-id="7dd95-114">Transakce nelze explicitně přidělit v rámci fiskálního období.</span><span class="sxs-lookup"><span data-stu-id="7dd95-114">You can't explicitly allocate transactions over a fiscal period.</span></span> <span data-ttu-id="7dd95-115">Místo toho je předpověď a její řízení založena na životnosti projektu.</span><span class="sxs-lookup"><span data-stu-id="7dd95-115">Instead, the forecast, and the control of the forecast, are based on the life of the project.</span></span> <span data-ttu-id="7dd95-116">Předpovědi jsou založeny na konkrétním datu, a proto musíte použité období odvodit od tohoto data.</span><span class="sxs-lookup"><span data-stu-id="7dd95-116">Because forecasts are based on a specific date, you must infer the period from the date.</span></span> | <span data-ttu-id="7dd95-117">Transakce můžete přidělit za celý projekt nebo fiskální období.</span><span class="sxs-lookup"><span data-stu-id="7dd95-117">You can allocate transactions over the whole project or a fiscal period.</span></span> <span data-ttu-id="7dd95-118">Pokud přidělíte za celé období, můžete nevyužité částky převést do dalšího fiskálního období.</span><span class="sxs-lookup"><span data-stu-id="7dd95-118">If you allocate over a period, you can carry unused amounts forward to the next fiscal period.</span></span> |
| <span data-ttu-id="7dd95-119">**Prohlížení transakcí**</span><span class="sxs-lookup"><span data-stu-id="7dd95-119">**Viewing transactions**</span></span>  | <span data-ttu-id="7dd95-120">Transakce můžete zobrazit ve formulářích předpovědí, kde vidíte předpovědi za celou společnost a všechny projekty bez ohledu na jejich hierarchii.</span><span class="sxs-lookup"><span data-stu-id="7dd95-120">You can view transactions in the forecast forms, where you see the forecasts for the whole company and for all projects, regardless of the hierarchy.</span></span> <span data-ttu-id="7dd95-121">Chcete-li se zaměřit na konkrétní projekt, musíte filtrovat data.</span><span class="sxs-lookup"><span data-stu-id="7dd95-121">To focus on a particular project, you must filter the data.</span></span>                                       | <span data-ttu-id="7dd95-122">Rozpočtované transakce můžete zobrazit pro jednu hierarchii projektu.</span><span class="sxs-lookup"><span data-stu-id="7dd95-122">You can view budgeted transactions for a single project hierarchy.</span></span> <span data-ttu-id="7dd95-123">Proto můžete zobrazit podrobnosti transakce u nadřazeného projektu nebo jeho dílčích projektů.</span><span class="sxs-lookup"><span data-stu-id="7dd95-123">Therefore, you can view transaction details for a parent project or its subprojects.</span></span>                 |
| <span data-ttu-id="7dd95-124">**Transakční proměnné**</span><span class="sxs-lookup"><span data-stu-id="7dd95-124">**Transaction variables**</span></span> | <span data-ttu-id="7dd95-125">Když zadáváte transakce předpovědi, můžete použít všechny atributy, které existují pro skutečnou transakci.</span><span class="sxs-lookup"><span data-stu-id="7dd95-125">When you enter forecast transactions, you can use every attribute that exists for an actual transaction.</span></span> <span data-ttu-id="7dd95-126">To umožňuje vyšší míru podrobností v předpovědi.</span><span class="sxs-lookup"><span data-stu-id="7dd95-126">This allows for greater detail in the forecast.</span></span> <span data-ttu-id="7dd95-127">Můžete například zadat podrobnosti o množství, pracovnících, položkách nebo vlastnostech výrobních linek.</span><span class="sxs-lookup"><span data-stu-id="7dd95-127">For example, you can enter details for quantities, workers, items, or line properties.</span></span>         | <span data-ttu-id="7dd95-128">Když zadáváte podrobnosti o rozpočtu, můžete použít pouze částky, kategorie a aktivity.</span><span class="sxs-lookup"><span data-stu-id="7dd95-128">When you enter budget details, you can use only amounts, categories, and activities.</span></span>                    |
| <span data-ttu-id="7dd95-129">**Zabezpečení**</span><span class="sxs-lookup"><span data-stu-id="7dd95-129">**Security**</span></span>              | <span data-ttu-id="7dd95-130">Prognózování je založeno na transakcích, které zadáte do formulářů předpovědi, a nezahrnuje žádný mechanismus řízení procesu.</span><span class="sxs-lookup"><span data-stu-id="7dd95-130">Forecasting is based on transactions that you enter in the forecast forms and involves no process control mechanism.</span></span> <span data-ttu-id="7dd95-131">Kterýkoli pracovník, který má oprávnění k formuláři předpovědi, může revidovat informace, aniž by bylo nutné schválení úprav.</span><span class="sxs-lookup"><span data-stu-id="7dd95-131">Any worker who has permissions for a forecast form can revise information without approval.</span></span>                                        | <span data-ttu-id="7dd95-132">Rozpočtování využívá systém pracovních postupů, který povoluje správu změn a umožňuje vám udržovat historii revizí.</span><span class="sxs-lookup"><span data-stu-id="7dd95-132">Budgeting uses the workflow system, which enables change management and lets you keep a history of the revisions.</span></span>         |
| <span data-ttu-id="7dd95-133">**Typy položek**</span><span class="sxs-lookup"><span data-stu-id="7dd95-133">**Entry types**</span></span>           | <span data-ttu-id="7dd95-134">Položky transakce předpovědi jsou založeny na počtu jednotek a na nákladových a prodejních jednotkových cenách.</span><span class="sxs-lookup"><span data-stu-id="7dd95-134">Forecast transaction entries are based on the number of units, and on cost and sales unit prices.</span></span>  | <span data-ttu-id="7dd95-135">Podrobnosti rozpočtu jsou založeny na částkách, které jsou rozděleny mezi náklady a výnosy.</span><span class="sxs-lookup"><span data-stu-id="7dd95-135">Budget details are based on amounts, which are split between costs and revenues.</span></span>                                          |
| <span data-ttu-id="7dd95-136">**Modely předpovědí**</span><span class="sxs-lookup"><span data-stu-id="7dd95-136">**Forecast models**</span></span>       | <span data-ttu-id="7dd95-137">Protože každá předpověď musí být přidružena k modelu, můžete vytvořit více modelů předpovědí a také nastavit dílčí modely.</span><span class="sxs-lookup"><span data-stu-id="7dd95-137">Because each forecast must be associated with a model, you can create multiple forecast models and also set up submodels.</span></span>           | <span data-ttu-id="7dd95-138">Projektové rozpočtování omezuje modely předpovědí, které se používají pro rozpočtování.</span><span class="sxs-lookup"><span data-stu-id="7dd95-138">Project budgeting limits the forecast models that are used for budgeting.</span></span> <span data-ttu-id="7dd95-139">Menší počet modelů předpovědí může pomoci zvýšit konzistenci projekcí.</span><span class="sxs-lookup"><span data-stu-id="7dd95-139">Fewer forecast models can help increase consistency in projections.</span></span>                           |
| <span data-ttu-id="7dd95-140">**Překročení nákladů**</span><span class="sxs-lookup"><span data-stu-id="7dd95-140">**Cost overruns**</span></span>         | <span data-ttu-id="7dd95-141">Zadávání transakcí, které způsobí překročení nákladů, můžete pouze povolit nebo zakázat.</span><span class="sxs-lookup"><span data-stu-id="7dd95-141">You can only allow or disallow the entry of transactions that will cause a cost overrun.</span></span>   | <span data-ttu-id="7dd95-142">Rozpočtování projektů poskytuje uživatelům další možnosti řízení.</span><span class="sxs-lookup"><span data-stu-id="7dd95-142">Project budgeting provides additional control options for users.</span></span> <span data-ttu-id="7dd95-143">Můžete povolit varování a překročení.</span><span class="sxs-lookup"><span data-stu-id="7dd95-143">You can allow warnings and overruns.</span></span>                    |
| <span data-ttu-id="7dd95-144">**Ovládací prvek**</span><span class="sxs-lookup"><span data-stu-id="7dd95-144">**Control**</span></span>               | <span data-ttu-id="7dd95-145">Řízení předpovědi se provádí pomocí redukce předpovědi.</span><span class="sxs-lookup"><span data-stu-id="7dd95-145">Forecast control is performed by using forecast reduction.</span></span> <span data-ttu-id="7dd95-146">Skutečné částky jsou odečteny od zůstatků transakcí předpovědí bez jakékoli záznamu pro audit.</span><span class="sxs-lookup"><span data-stu-id="7dd95-146">Actual amounts are subtracted from forecast transaction balances without any audit trail.</span></span> <span data-ttu-id="7dd95-147">To může ztížit dohledání, kde došlo ke skutečným transakcím.</span><span class="sxs-lookup"><span data-stu-id="7dd95-147">This can make it more difficult to trace where the actual transactions occurred.</span></span>                   | <span data-ttu-id="7dd95-148">Při řízení projektového rozpočtu se skutečné částky odečítají od částek ve zbývajícím rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="7dd95-148">In project budget control, actual amounts are subtracted from amounts in the remaining budget.</span></span> <span data-ttu-id="7dd95-149">To umožňuje vytvářet přehlednější záznam pro audit.</span><span class="sxs-lookup"><span data-stu-id="7dd95-149">This allows for a clearer audit trail.</span></span>                                   |

## <a name="project-forecasts"></a><span data-ttu-id="7dd95-150">Projektové předpovědi</span><span class="sxs-lookup"><span data-stu-id="7dd95-150">Project forecasts</span></span>
<span data-ttu-id="7dd95-151">Když používáte projektové předpovědi, můžete zadat transakce předpovědí do formulářů předpovědi pro každý typ transakce.</span><span class="sxs-lookup"><span data-stu-id="7dd95-151">When you use project forecasting, you can enter forecast transactions in forecast forms for each transaction type.</span></span> <span data-ttu-id="7dd95-152">Každý atribut, který je k dispozici pro skutečnou transakci, lze použít pro transakci předpovědi – například ziskovost linky, atributy linky, pracovníky nebo popisy.</span><span class="sxs-lookup"><span data-stu-id="7dd95-152">Every attribute that is available for an actual transaction can be used for a forecast transaction—for example, line profitability, line attributes, workers, or descriptions.</span></span> <span data-ttu-id="7dd95-153">Můžete také plánovat, jak dlouho po vzniku nákladů budete zákazníkovi fakturovat.</span><span class="sxs-lookup"><span data-stu-id="7dd95-153">You can also project how long after you incur a cost you will invoice a customer.</span></span> 

<span data-ttu-id="7dd95-154">Transakce prognózování projektů jsou založeny na jednotkách a částkách.</span><span class="sxs-lookup"><span data-stu-id="7dd95-154">Project forecasting transactions are based on units and amounts.</span></span> 

<span data-ttu-id="7dd95-155">Každou projektovou předpověď musíte spojit s modelem předpovědi.</span><span class="sxs-lookup"><span data-stu-id="7dd95-155">You must associate each project forecast with a forecast model.</span></span> <span data-ttu-id="7dd95-156">Když zadáte transakci předpovědi, automaticky se navrhne model předpovědi.</span><span class="sxs-lookup"><span data-stu-id="7dd95-156">When you enter a forecast transaction, a forecast model is automatically suggested.</span></span> <span data-ttu-id="7dd95-157">Model předpovědi funguje jako kontejner pro transakce předpovědi.</span><span class="sxs-lookup"><span data-stu-id="7dd95-157">The forecast model acts as a container for the forecast transactions.</span></span> 

<span data-ttu-id="7dd95-158">Modely předpovědi můžete označit jako dílčí modely určitého modelu.</span><span class="sxs-lookup"><span data-stu-id="7dd95-158">You can designate forecast models as submodels for a model.</span></span> <span data-ttu-id="7dd95-159">To vám umožní předpovídat podle regionu, časového období nebo oddělení.</span><span class="sxs-lookup"><span data-stu-id="7dd95-159">This lets you forecast by region, time period, or department.</span></span> <span data-ttu-id="7dd95-160">Transakce předpovědi můžete zkopírovat do modelu a vytvořit nový model. Transakce můžete také převést do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="7dd95-160">You can copy the forecast transactions in a model to create a new model, and you can also transfer the transactions to the general ledger.</span></span> <span data-ttu-id="7dd95-161">Protože mezi předpovědí a modelem existuje vztah jedna k jedné, každý model předpovědi vytváří samostatný rozpočet pro projekt.</span><span class="sxs-lookup"><span data-stu-id="7dd95-161">Because there is a one-to-one relationship between a forecast and a model, each forecast model makes up a separate budget for a project.</span></span> 

<span data-ttu-id="7dd95-162">Modely předpovědí mohou používat redukci předpovědi jako kontrolní mechanismus pro projekty.</span><span class="sxs-lookup"><span data-stu-id="7dd95-162">Forecast models can use forecast reduction as the control mechanism for projects.</span></span> <span data-ttu-id="7dd95-163">Při redukci předpovědi snižují skutečné transakce zůstatky transakcí předpovědi.</span><span class="sxs-lookup"><span data-stu-id="7dd95-163">In forecast reduction, actual transactions reduce forecast transaction balances.</span></span> <span data-ttu-id="7dd95-164">Protože se však redukce předpovědi použije na nejvyšší projekt v hierarchii, poskytuje omezený pohled na změny v předpovědi.</span><span class="sxs-lookup"><span data-stu-id="7dd95-164">However, because forecast reduction is applied to the highest project in the hierarchy, it provides a limited view of changes in the forecast.</span></span> <span data-ttu-id="7dd95-165">Například pokud je pracovník přidružen k dílčímu projektu, skutečné transakce pro pracovníka jsou zaúčtovány do nadřazeného projektu.</span><span class="sxs-lookup"><span data-stu-id="7dd95-165">For example, if a worker is associated with a subproject, the actual transactions for the worker are posted to the parent project.</span></span> <span data-ttu-id="7dd95-166">To může ztěžovat sledování změn, protože nemůžete snadno určit, která transakce ve kterém dílčím projektu způsobila snížení částky předpovědi.</span><span class="sxs-lookup"><span data-stu-id="7dd95-166">This can make it difficult to track changes, because you can't easily determine which transaction in which subproject caused a reduction to the forecast amount.</span></span> <span data-ttu-id="7dd95-167">Proto je vhodné vytvořit kopii modelu předpovědi, na kterou použijete redukci předpovědi.</span><span class="sxs-lookup"><span data-stu-id="7dd95-167">Therefore, it's a good idea to create a copy of a forecast model for forecast reduction to use.</span></span> <span data-ttu-id="7dd95-168">Poté můžete pomocí sestav zobrazit, co bylo původně předpovězeno.</span><span class="sxs-lookup"><span data-stu-id="7dd95-168">You can then use reports to view what was originally forecasted.</span></span> 

<span data-ttu-id="7dd95-169">Projektové předpovědi můžete revidovat, kopírovat, mazat nebo přenášet do rozpočtu hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="7dd95-169">You can revise, copy, delete, or transfer project forecasts to a general ledger budget.</span></span> <span data-ttu-id="7dd95-170">Neexistuje však žádné řízení procesu.</span><span class="sxs-lookup"><span data-stu-id="7dd95-170">However, there is no process control.</span></span> <span data-ttu-id="7dd95-171">Kterýkoli pracovník, který má oprávnění k formuláři předpovědi, může provádět revize bez jejich následné kontroly.</span><span class="sxs-lookup"><span data-stu-id="7dd95-171">Any worker who has permission for a forecast form can make revisions without review.</span></span>

-   <span data-ttu-id="7dd95-172">**Revidovat** – Předpověď transakce můžete revidovat ve stejných formulářích, kde byly vytvořeny původní záznamy.</span><span class="sxs-lookup"><span data-stu-id="7dd95-172">**Revise** – You can revise a forecast transaction in the same forms where the original entries were made.</span></span>
-   <span data-ttu-id="7dd95-173">**Kopírovat nebo odstranit** – Když kopírujete transakce předpovědí, kopírujete řádky transakcí jednoho modelu prognózy do jiného modelu prognózy.</span><span class="sxs-lookup"><span data-stu-id="7dd95-173">**Copy or delete** – When you copy forecast transactions, you copy the transaction lines of one forecast model to another forecast model.</span></span> <span data-ttu-id="7dd95-174">Když odstraníte předpověď, odstraníte transakce předpovědi z modelu předpovědi.</span><span class="sxs-lookup"><span data-stu-id="7dd95-174">When you delete a forecast, you delete the forecast transactions from a forecast model.</span></span> <span data-ttu-id="7dd95-175">Chcete-li omezit transakce předpovědi, které se kopírují nebo odstraňují, vyberte konkrétní typy transakcí a data.</span><span class="sxs-lookup"><span data-stu-id="7dd95-175">To limit the forecast transactions that are copied or deleted, select specific transaction types and dates.</span></span> <span data-ttu-id="7dd95-176">To vám umožní kopírovat nebo mazat pouze konkrétní části předpovědi.</span><span class="sxs-lookup"><span data-stu-id="7dd95-176">This lets you copy or delete only specific parts of a forecast.</span></span>
-   <span data-ttu-id="7dd95-177">**Převod** – Když převedete projektovou předpověď do rozpočtu hlavní knihy, převedete transakce předpovědi modelu předpovědi do rozpočtu hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="7dd95-177">**Transfer** – When you transfer a project forecast to a general ledger budget, you transfer the forecast transactions of a forecast model to a general ledger budget.</span></span> <span data-ttu-id="7dd95-178">Veškeré dříve převedené transakce můžete přepsat v rozpočtu hlavní knihy, do kterého přenesete projektovou předpověď.</span><span class="sxs-lookup"><span data-stu-id="7dd95-178">You can overwrite any previously transferred transactions in the general ledger budget that you transfer your project forecast to.</span></span>

## <a name="project-budgets"></a><span data-ttu-id="7dd95-179">Projektové rozpočty</span><span class="sxs-lookup"><span data-stu-id="7dd95-179">Project budgets</span></span>
<span data-ttu-id="7dd95-180">Projektové rozpočty jsou jednodušší metodou než předpovědi, ačkoli se integrují do modelů předpovědí.</span><span class="sxs-lookup"><span data-stu-id="7dd95-180">Project budgeting is a simpler method than forecasting, although it does integrate with forecast models.</span></span> <span data-ttu-id="7dd95-181">Rozpočet používá jediný vstupní formulář pro původní podrobnosti rozpočtu a revize, a umožňuje projekce založené pouze na částce, kategorii nebo aktivitě.</span><span class="sxs-lookup"><span data-stu-id="7dd95-181">It uses a single entry form for original budget details and revisions, and allows for projections that are based only on amount, category, or activity.</span></span> 

<span data-ttu-id="7dd95-182">V rozpočtování projektu musí být všechny původní rozpočty a revize odeslány do pracovního postupu projektu ke schválení.</span><span class="sxs-lookup"><span data-stu-id="7dd95-182">In project budgeting, all original budgets and revisions must be sent to a project workflow for approval.</span></span> <span data-ttu-id="7dd95-183">Pracovní postupy vám dávají větší kontrolu nad procesem a vytvářejí záznam historie změn.</span><span class="sxs-lookup"><span data-stu-id="7dd95-183">Workflows give you increased control over the process and create a change history record.</span></span> 

<span data-ttu-id="7dd95-184">Rozpočtování projektů se podobá rozpočtu hlavní knihy, ale jeho nastavení je rychlejší a snazší.</span><span class="sxs-lookup"><span data-stu-id="7dd95-184">Project budgeting resembles general ledger budgeting, but is faster and easier to set up.</span></span> <span data-ttu-id="7dd95-185">Mnohé možnosti v rozpočtování hlavní knihy, například číselné řady nebo měna, nemusí být pro projekty nastaveny samostatně.</span><span class="sxs-lookup"><span data-stu-id="7dd95-185">Many of the options in general ledger budgeting, such as number sequences or currency, do not have to be set up separately for projects.</span></span>

<span data-ttu-id="7dd95-186">Projektové rozpočty jsou automaticky spojeny se dvěma modely předpovědi, jedním pro původní rozpočet a druhým pro zbývající rozpočet.</span><span class="sxs-lookup"><span data-stu-id="7dd95-186">Project budgets are automatically associated with two forecast models, one for original budget and one for remaining budget.</span></span> <span data-ttu-id="7dd95-187">Proto mohou sestavy založené na modelech předpovědí využívat data rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="7dd95-187">Therefore, reports that are based on forecast models can use budget data.</span></span> <span data-ttu-id="7dd95-188">Když je projektový rozpočet přijat, systém vytvoří transakce předpovědi na základě přidružených modelů, které se používají pro účely vykazování a řízení.</span><span class="sxs-lookup"><span data-stu-id="7dd95-188">When a project budget is committed, the system creates forecast transactions based on the associated models, which are used for reporting and control purposes.</span></span>

## <a name="forecast-models"></a><span data-ttu-id="7dd95-189">Modely předpovědí</span><span class="sxs-lookup"><span data-stu-id="7dd95-189">Forecast models</span></span>
<span data-ttu-id="7dd95-190">Modely předpovědí mají jednovrstvou hierarchii.</span><span class="sxs-lookup"><span data-stu-id="7dd95-190">Forecast models have a single-layer hierarchy.</span></span> <span data-ttu-id="7dd95-191">To znamená, že jedna projektová předpověď musí být spojena s jedním modelem předpovědi.</span><span class="sxs-lookup"><span data-stu-id="7dd95-191">This means that one project forecast must be associated with one forecast model.</span></span>

<span data-ttu-id="7dd95-192">Pokud používáte projektové předpovědi, můžete modely identifikovat jako dílčí modely.</span><span class="sxs-lookup"><span data-stu-id="7dd95-192">If you use project forecasting, you can identify models as submodels.</span></span> <span data-ttu-id="7dd95-193">To vám umožní poté předpovídat podle regionu, časového období nebo oddělení.</span><span class="sxs-lookup"><span data-stu-id="7dd95-193">You can then create forecasts by department, time period, or region.</span></span> <span data-ttu-id="7dd95-194">Můžete například vytvořit model předpovědi na rok a poté vytvořit dílčí modely pro regionální předpovědi Severovýchod, Jihovýchod, Severozápad a Jihozápad, které přijímají regionální manažeři.</span><span class="sxs-lookup"><span data-stu-id="7dd95-194">For example, you can create a forecast model for a year, and then create submodels for the Northeast, Southeast, Northwest, and Southwest regional forecasts that regional heads submit.</span></span> <span data-ttu-id="7dd95-195">Výběrem různých možností v dostupných sestavách můžete zobrazit informace podle celkové předpovědi nebo podle dílčího modelu.</span><span class="sxs-lookup"><span data-stu-id="7dd95-195">By selecting different options in the available reports, you can view information by total forecast or by submodel.</span></span>


