---
title: Konfigurace správy výdajů
description: Tento článek popisuje úvahy a rozhodnutí, která musíte udělat během procesu plánování, než nakonfigurujete správu výdajů v Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a8435464c8573ca831b7886f00c2695fd29827
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271345"
---
# <a name="configure-expense-management"></a><span data-ttu-id="b7293-103">Konfigurace správy výdajů</span><span class="sxs-lookup"><span data-stu-id="b7293-103">Configure expense management</span></span>

<span data-ttu-id="b7293-104">Toto téma popisuje úvahy a rozhodnutí, která musíte udělat během procesu plánování, než nakonfigurujete správu výdajů.</span><span class="sxs-lookup"><span data-stu-id="b7293-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="b7293-105">Ve správě výdajů můžete ukládat informace o platebních metodách, cestovních požadavcích, sestavách výdajů, zásadách atd.</span><span class="sxs-lookup"><span data-stu-id="b7293-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="b7293-106">Protože mnohá rozhodnutí, která uděláte při plánování konfigurace správy výdajů, jsou založena na hierarchii a finanční struktuře vaší organizace, musíte si přečíst plánovací dokumenty pro tyto oblasti.</span><span class="sxs-lookup"><span data-stu-id="b7293-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="b7293-107">Mezipodnikové výdaje</span><span class="sxs-lookup"><span data-stu-id="b7293-107">Intercompany expenses</span></span>

<span data-ttu-id="b7293-108">Když povolíte mezipodnikové výdaje, umožníte právním subjektům a zaměstnancům nést náklady jménem jiné právnické osoby a inkasovat platby od právnické osoby zaměstnávající ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="b7293-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="b7293-109">Například zaměstnanec v právnické osobě A dokončí projekt pro právnickou osobu B a v projektu vzniknou cestovní výdaje.</span><span class="sxs-lookup"><span data-stu-id="b7293-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="b7293-110">Pokud jsou povoleny mezipodnikové výdaje, může zaměstnanec následně předložit sestavu výdajů, které zaúčtuje výdaj právnické osobě B, a výdaj musí poté uhradit právnická osoba A. Pokud vaše organizace nemá více právnických osob, nemusíte povolit mezipodnikové výdaje.</span><span class="sxs-lookup"><span data-stu-id="b7293-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="b7293-111">**Rozhodnutí:** Chcete povolit mezipodnikové výdaje?</span><span class="sxs-lookup"><span data-stu-id="b7293-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="b7293-112">Finanční správa</span><span class="sxs-lookup"><span data-stu-id="b7293-112">Financial management</span></span>

<span data-ttu-id="b7293-113">Správa výdajů je úzce integrována do finančního řízení vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="b7293-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="b7293-114">Spousta vaší konfigurace pro správu výdajů bude založena na rozhodnutích, které jste přijali v oblasti financování vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="b7293-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="b7293-115">V následujících částech jsou popsány různé oblasti, které vyžadují plánování a rozhodování na základě finančních rozhodnutí vaší organizace a pokynů vašeho vedoucího týmu.</span><span class="sxs-lookup"><span data-stu-id="b7293-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="b7293-116">Denní diety</span><span class="sxs-lookup"><span data-stu-id="b7293-116">Per diems</span></span>

<span data-ttu-id="b7293-117">Musíte definovat denní diety zaměstnanců, které vaše organizace poskytuje.</span><span class="sxs-lookup"><span data-stu-id="b7293-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="b7293-118">Protože se denní diety obvykle používají k pokrytí výdajů, jako jsou stravování, ubytování a další vedlejší výdaje, můžete vytvořit pravidla pro denní diety, které vaše organizace nabízí.</span><span class="sxs-lookup"><span data-stu-id="b7293-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="b7293-119">sazby denních diet mohou být založeny na ročním období, místě cesty nebo na obou kritériích.</span><span class="sxs-lookup"><span data-stu-id="b7293-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="b7293-120">Když definujete pravidlo denní diety, můžete určit, že určité procento sazby diety bude zadrženo, pokud pracovník obdrží bezplatné jídlo nebo služby.</span><span class="sxs-lookup"><span data-stu-id="b7293-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="b7293-121">Můžete také definovat úrovně denních diet a nastavit pomocí nich minimální a maximální počet hodin, které musí cesta pracovníka trvat, aby byla sazba denní diety použita.</span><span class="sxs-lookup"><span data-stu-id="b7293-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="b7293-122">**Rozhodnutí:**</span><span class="sxs-lookup"><span data-stu-id="b7293-122">**Decisions:**</span></span>

- <span data-ttu-id="b7293-123">Výchozí pravidla denních diet pro první a poslední den:</span><span class="sxs-lookup"><span data-stu-id="b7293-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="b7293-124">Jaký je minimální počet hodin, který může zaměstnanec za den vykázat a přesto dostat denní dietu?</span><span class="sxs-lookup"><span data-stu-id="b7293-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="b7293-125">Dochází ke snížení částky nabízené za jídlo za první a poslední den?</span><span class="sxs-lookup"><span data-stu-id="b7293-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="b7293-126">Pokud dojde ke snížení, jaké je jeho procento?</span><span class="sxs-lookup"><span data-stu-id="b7293-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="b7293-127">Dochází ke snížení částky nabízené za ubytování v hotelu za první a poslední den?</span><span class="sxs-lookup"><span data-stu-id="b7293-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="b7293-128">Pokud dojde ke snížení, jaké je jeho procento?</span><span class="sxs-lookup"><span data-stu-id="b7293-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="b7293-129">Dochází ke snížení částky nabízené za jiné výdaje, ke kterým dojde v prvním a posledním dnu?</span><span class="sxs-lookup"><span data-stu-id="b7293-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="b7293-130">Pokud dojde ke snížení, jaké je jeho procento?</span><span class="sxs-lookup"><span data-stu-id="b7293-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="b7293-131">Výchozí pravidla denních diet:</span><span class="sxs-lookup"><span data-stu-id="b7293-131">Default per diem rules:</span></span>

    - <span data-ttu-id="b7293-132">Dochází k procentnímu snížení denní diety za každé jídlo, pokud je například jídlo bezplatné?</span><span class="sxs-lookup"><span data-stu-id="b7293-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="b7293-133">Pokud dojde ke snížení, jaké je jeho procento za každé jídlo?</span><span class="sxs-lookup"><span data-stu-id="b7293-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="b7293-134">Je snížení za jídlo počítáno za den, za celou cestu nebo podle počtu jídel za den?</span><span class="sxs-lookup"><span data-stu-id="b7293-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="b7293-135">Mají být částky za diety zaokrouhleny běžným způsobem nebo zaokrouhleny nahoru?</span><span class="sxs-lookup"><span data-stu-id="b7293-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="b7293-136">Počítají se diety za 24 hodin nebo za kalendářní den?</span><span class="sxs-lookup"><span data-stu-id="b7293-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="b7293-137">Pravidla denních diet, která jsou založena na umístění:</span><span class="sxs-lookup"><span data-stu-id="b7293-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="b7293-138">Liší se sazby denních diet podle umístění?</span><span class="sxs-lookup"><span data-stu-id="b7293-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="b7293-139">Jaká umístění jsou zahrnuta?</span><span class="sxs-lookup"><span data-stu-id="b7293-139">What locations are included?</span></span>
    - <span data-ttu-id="b7293-140">Pokud se sazby denních diet liší podle umístění, jaká procentní částka pro každou lokalitu je poskytována pro následující typy výdajů:</span><span class="sxs-lookup"><span data-stu-id="b7293-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="b7293-141">Stravování</span><span class="sxs-lookup"><span data-stu-id="b7293-141">Meals</span></span>
        - <span data-ttu-id="b7293-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="b7293-142">Hotel</span></span>
        - <span data-ttu-id="b7293-143">Jiné výdaje</span><span class="sxs-lookup"><span data-stu-id="b7293-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="b7293-144">Deníky a účty pro správu výdajů</span><span class="sxs-lookup"><span data-stu-id="b7293-144">Expense management journals and accounts</span></span>

<span data-ttu-id="b7293-145">Správa výdajů vyžaduje, abyste používali více deníků a účtů.</span><span class="sxs-lookup"><span data-stu-id="b7293-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="b7293-146">Musíte se například rozhodnout, zda se stejný účet používá pro hotovostní zálohy a spory o kreditní karty.</span><span class="sxs-lookup"><span data-stu-id="b7293-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="b7293-147">**Rozhodnutí:**</span><span class="sxs-lookup"><span data-stu-id="b7293-147">**Decisions:**</span></span>

- <span data-ttu-id="b7293-148">Do kterého deníku hlavní knihy jsou schválené sestavy výdajů zaúčtovány?</span><span class="sxs-lookup"><span data-stu-id="b7293-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="b7293-149">Který účet se používá pro hotovostní zálohy?</span><span class="sxs-lookup"><span data-stu-id="b7293-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="b7293-150">Měly by být peněžní zálohy zaúčtovány okamžitě?</span><span class="sxs-lookup"><span data-stu-id="b7293-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="b7293-151">Způsoby platby</span><span class="sxs-lookup"><span data-stu-id="b7293-151">Payment methods</span></span>

<span data-ttu-id="b7293-152">Pokud zaměstnancům umožníte, aby vytvářeli výdaje jménem vašeho podniku, musíte definovat způsoby platby, které mohou zaměstnanci používat.</span><span class="sxs-lookup"><span data-stu-id="b7293-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="b7293-153">Například můžete zaměstnancům umožnit používat hotovost nebo firemní kreditní kartu.</span><span class="sxs-lookup"><span data-stu-id="b7293-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="b7293-154">Můžete také umožnit zaměstnancům používat osobní kreditní karty a poté zaměstnancům vrátit peníze.</span><span class="sxs-lookup"><span data-stu-id="b7293-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="b7293-155">U každého povoleného způsobu platby musíte učinit následující rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="b7293-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="b7293-156">**Rozhodnutí:**</span><span class="sxs-lookup"><span data-stu-id="b7293-156">**Decisions:**</span></span>

- <span data-ttu-id="b7293-157">Jaké způsoby platby jsou povoleny?</span><span class="sxs-lookup"><span data-stu-id="b7293-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="b7293-158">Kdo vlastní výdaje na způsob platby?</span><span class="sxs-lookup"><span data-stu-id="b7293-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="b7293-159">Existuje typ offsetového účtu?</span><span class="sxs-lookup"><span data-stu-id="b7293-159">Is there an offset account type?</span></span> <span data-ttu-id="b7293-160">Pokud existuje typ offsetového účtu, který to je?</span><span class="sxs-lookup"><span data-stu-id="b7293-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="b7293-161">Pokud existuje typ offsetového účtu, který účet to je?</span><span class="sxs-lookup"><span data-stu-id="b7293-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="b7293-162">Pokud je způsobem platby kreditní karta, měl by se tento způsob použít pouze u importovaných transakcí?</span><span class="sxs-lookup"><span data-stu-id="b7293-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="b7293-163">Kategorie výdajů a sdílené kategorie</span><span class="sxs-lookup"><span data-stu-id="b7293-163">Expense categories and shared categories</span></span>

<span data-ttu-id="b7293-164">Když zaměstnanci vytvářejí sestavu výdajů, musí být každý zaznamenaný výdaj přidružen ke kategorii výdajů.</span><span class="sxs-lookup"><span data-stu-id="b7293-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="b7293-165">Kategorie výdajů jsou odvozeny ze sdílených kategorií, které lze sdílet mezi právnickými osobami ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="b7293-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="b7293-166">Tyto kategorie lze také sdílet v Řízení projektů a účetnictví, v závislosti na způsobu, jakým je vaše organizace definována.</span><span class="sxs-lookup"><span data-stu-id="b7293-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="b7293-167">Na základě definice vaší organizace a pokynů od implementačního týmu určete, zda kategorie, které se používají ve správě výdajů, budou použity pouze ve správě výdajů, nebo zda by měly být sdíleny mezi moduly Řízení projektů a účetnictví a Správa výdajů.</span><span class="sxs-lookup"><span data-stu-id="b7293-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="b7293-168">Poznámka: tyto kategorie lze sdílet mezi moduly Projekty a Výdaje nebo mezi moduly Projekt a Výroba, ale ne mezi moduly Výdaje a Výroba.</span><span class="sxs-lookup"><span data-stu-id="b7293-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="b7293-169">Pro každou kategorii výdajů musíte učinit následující rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="b7293-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="b7293-170">**Rozhodnutí:**</span><span class="sxs-lookup"><span data-stu-id="b7293-170">**Decisions:**</span></span>

- <span data-ttu-id="b7293-171">Jaká je kategorie výdajů?</span><span class="sxs-lookup"><span data-stu-id="b7293-171">What is the expense category?</span></span> <span data-ttu-id="b7293-172">Mezi příklady patří kategorie letů, hotelů nebo najetých kilometrů.</span><span class="sxs-lookup"><span data-stu-id="b7293-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="b7293-173">Lze kategorii výdajů použít také v modulu Řízení a účetnictví projektů?</span><span class="sxs-lookup"><span data-stu-id="b7293-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="b7293-174">Jaký je typ výdajů?</span><span class="sxs-lookup"><span data-stu-id="b7293-174">What is the expense type?</span></span>
- <span data-ttu-id="b7293-175">Jaký je výchozí způsob platby pro kategorii výdajů?</span><span class="sxs-lookup"><span data-stu-id="b7293-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="b7293-176">Musí být výdaje v kategorii výdajů rozepsány?</span><span class="sxs-lookup"><span data-stu-id="b7293-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="b7293-177">Jaký je hlavní výchozí účet pro kategorii výdajů?</span><span class="sxs-lookup"><span data-stu-id="b7293-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="b7293-178">Jaká je výchozí skupina daně z prodeje zboží pro kategorii výdajů?</span><span class="sxs-lookup"><span data-stu-id="b7293-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="b7293-179">Jsou pro kategorii výdajů povoleny další způsoby platby?</span><span class="sxs-lookup"><span data-stu-id="b7293-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="b7293-180">Jsou-li povoleny další způsoby platby, které to jsou?</span><span class="sxs-lookup"><span data-stu-id="b7293-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="b7293-181">Existují v této kategorii výdajů podkategorie?</span><span class="sxs-lookup"><span data-stu-id="b7293-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="b7293-182">Když existují podkategorie, musíte rovněž učinit následující rozhodnutí:</span><span class="sxs-lookup"><span data-stu-id="b7293-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="b7293-183">Jsou některé z podkategorií vyloučeny z vymáhání daní?</span><span class="sxs-lookup"><span data-stu-id="b7293-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="b7293-184">Jaká je skupina daně z prodeje zboží u podkategorií?</span><span class="sxs-lookup"><span data-stu-id="b7293-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="b7293-185">Pokud se kategorie výdajů používá také v Řízení projektů a účetnictví, odpovězte na zbývající otázky.</span><span class="sxs-lookup"><span data-stu-id="b7293-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="b7293-186">V opačném případě přejděte k další části.</span><span class="sxs-lookup"><span data-stu-id="b7293-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="b7293-187">Které nákladové účty budou použity pro následující výdaje?</span><span class="sxs-lookup"><span data-stu-id="b7293-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="b7293-188">Náklady</span><span class="sxs-lookup"><span data-stu-id="b7293-188">Cost</span></span>
    - <span data-ttu-id="b7293-189">Přidělení mezd</span><span class="sxs-lookup"><span data-stu-id="b7293-189">Payroll allocation</span></span>
    - <span data-ttu-id="b7293-190">Hodnota nákladů nedokončené práce</span><span class="sxs-lookup"><span data-stu-id="b7293-190">WIP-cost value</span></span>
    - <span data-ttu-id="b7293-191">Náklady – položka</span><span class="sxs-lookup"><span data-stu-id="b7293-191">Cost-item</span></span>
    - <span data-ttu-id="b7293-192">Nedokončená výroba – hodnota nákladů – položka</span><span class="sxs-lookup"><span data-stu-id="b7293-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="b7293-193">Časově rozlišená ztráta</span><span class="sxs-lookup"><span data-stu-id="b7293-193">Accrued loss</span></span>
    - <span data-ttu-id="b7293-194">NV – časově rozlišená ztráta</span><span class="sxs-lookup"><span data-stu-id="b7293-194">WIP-accrued loss</span></span>

- <span data-ttu-id="b7293-195">Které účty výnosů budou použity pro následující položky?</span><span class="sxs-lookup"><span data-stu-id="b7293-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="b7293-196">Fakturované výnosy</span><span class="sxs-lookup"><span data-stu-id="b7293-196">Invoiced revenue</span></span>
    - <span data-ttu-id="b7293-197">Časově rozlišené výnosy – hodnota prodeje</span><span class="sxs-lookup"><span data-stu-id="b7293-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="b7293-198">NV – prodej</span><span class="sxs-lookup"><span data-stu-id="b7293-198">WIP-sales value</span></span>
    - <span data-ttu-id="b7293-199">Časově rozlišené výnosy – výroba</span><span class="sxs-lookup"><span data-stu-id="b7293-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="b7293-200">NV – výroba</span><span class="sxs-lookup"><span data-stu-id="b7293-200">WIP-production</span></span>
    - <span data-ttu-id="b7293-201">Časově rozlišené výnosy – zisk</span><span class="sxs-lookup"><span data-stu-id="b7293-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="b7293-202">NV – zisk</span><span class="sxs-lookup"><span data-stu-id="b7293-202">WIP-profit</span></span>
    - <span data-ttu-id="b7293-203">Časově rozlišené výnosy – předplatné</span><span class="sxs-lookup"><span data-stu-id="b7293-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="b7293-204">NV – předplatné</span><span class="sxs-lookup"><span data-stu-id="b7293-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="b7293-205">Daně</span><span class="sxs-lookup"><span data-stu-id="b7293-205">Taxes</span></span>

<span data-ttu-id="b7293-206">U daní souvisejících s výdaji musíte určit, co je zahrnuto nebo povoleno v sestavách výdajů.</span><span class="sxs-lookup"><span data-stu-id="b7293-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="b7293-207">**Rozhodnutí:**</span><span class="sxs-lookup"><span data-stu-id="b7293-207">**Decisions:**</span></span>

- <span data-ttu-id="b7293-208">Je prodejní daň zahrnuta do částky výdajů?</span><span class="sxs-lookup"><span data-stu-id="b7293-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="b7293-209">Mají být povoleny vratky daní u výdajů?</span><span class="sxs-lookup"><span data-stu-id="b7293-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="b7293-210">Pokud jste se při plánování hlavní knihy rozhodli použít prodejní daň v USA a použít daňová pravidla, nemůžete povolit vratky daní u výdajů.</span><span class="sxs-lookup"><span data-stu-id="b7293-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="b7293-211">(Chcete-li použít prodejní daň v USA a použít daňová pravidla, nastavte možnost **Použít pravidla zdanění prodejní daně** na **Ano** .)</span><span class="sxs-lookup"><span data-stu-id="b7293-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="b7293-212">Zásady</span><span class="sxs-lookup"><span data-stu-id="b7293-212">Policies</span></span>

<span data-ttu-id="b7293-213">Vytvořením zásad sestav výdajů můžete pomoci vaší organizaci ušetřit čas a peníze, když zaměstnancům vzniknou náklady jejím jménem.</span><span class="sxs-lookup"><span data-stu-id="b7293-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="b7293-214">Zásady pomáhají zaručit, že zaměstnanci nepřekročí rozpočet, dostanou všechny požadované informace a utratí peníze, pouze pokud je potřebují.</span><span class="sxs-lookup"><span data-stu-id="b7293-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="b7293-215">Pro každou vytvořenou zásadu sestavy výdajů a každou zásadu schvalování sestavy výdajů musíte učinit následující rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="b7293-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="b7293-216">**Rozhodnutí:**</span><span class="sxs-lookup"><span data-stu-id="b7293-216">**Decisions:**</span></span>

- <span data-ttu-id="b7293-217">Jaký je název zásady?</span><span class="sxs-lookup"><span data-stu-id="b7293-217">What is the name of the policy?</span></span>
- <span data-ttu-id="b7293-218">K čemu zásada výdajů slouží?</span><span class="sxs-lookup"><span data-stu-id="b7293-218">What is the expense policy for?</span></span>
- <span data-ttu-id="b7293-219">Pokud jste se dříve rozhodli povolit mezipodnikové výdaje, na které společnosti ve vaší organizaci se tato zásada bude vztahovat?</span><span class="sxs-lookup"><span data-stu-id="b7293-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="b7293-220">Kdy začne zásada platit?</span><span class="sxs-lookup"><span data-stu-id="b7293-220">When does the policy become effective?</span></span>
- <span data-ttu-id="b7293-221">Kdy platnost zásady skončí?</span><span class="sxs-lookup"><span data-stu-id="b7293-221">When does the policy expire?</span></span>
- <span data-ttu-id="b7293-222">Jaké je pravidlo zásady?</span><span class="sxs-lookup"><span data-stu-id="b7293-222">What is the policy rule?</span></span>
- <span data-ttu-id="b7293-223">Jaký je výstup pravidla zásady?</span><span class="sxs-lookup"><span data-stu-id="b7293-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]