---
title: Projektové smlouvy
description: Toto téma poskytuje příklady projektových smluv, které můžete vytvořit pro různé typy projektů a zdrojů financování, a příklady správy smluv a fakturace zákazníkům projektu.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750365"
---
# <a name="project-contracts"></a><span data-ttu-id="d1fd2-103">Projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="d1fd2-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1fd2-104">Tento článek poskytuje příklady projektových smluv, které můžete vytvořit pro různé typy projektů a zdrojů financování, a příklady správy smluv a fakturace zákazníkům projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="d1fd2-105">Typ projektu, který vytvoříte pro projektovou smlouvu, určuje metodu, která se používá k fakturaci zákazníků projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="d1fd2-106">Projektovou smlouvu a související projekt můžete změnit, ale nemůžete změnit typ projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="d1fd2-107">Pomocí projektové smlouvy můžete fakturovat jeden nebo více projektů současně.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="d1fd2-108">Projektová smlouva také pomáhá zaručit konzistentní postup fakturace pro každý dílčí projekt ve struktuře projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="d1fd2-109">Každý projekt, který bude fakturován, musí být spojen s projektovou smlouvou.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="d1fd2-110">Nastavení pro projektovou smlouvu se vztahuje na všechny projekty a dílčí projekty, které jsou spojeny s touto projektovou smlouvou.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="d1fd2-111">Projektová smlouva může stanovit jeden nebo více zdrojů financování.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="d1fd2-112">Proto můžete rozdělit fakturaci mezi více poskytovatelů financování, nastavit limity financování tak, aby ze zdrojů financování byla fakturována maximálně určená částka, a konfigurovat pravidla financování pro účtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="d1fd2-113">Financování projektových smluv</span><span class="sxs-lookup"><span data-stu-id="d1fd2-113">Funding for project contracts</span></span>
<span data-ttu-id="d1fd2-114">Některé projektové smlouvy stanoví, že odpovědnost za financování nákladů projektu sdílí více stran.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="d1fd2-115">Zde je uvedeno několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="d1fd2-115">Here are some examples:</span></span>

-   <span data-ttu-id="d1fd2-116">Velký zákazník s několika divizemi požaduje, aby bylo financování projektu rozděleno podle divizí.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="d1fd2-117">Vaše společnost sdílí náklady na velký projekt s externí organizací.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="d1fd2-118">Silniční projekt je spolufinancován dvěma obcemi.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="d1fd2-119">Projekt stavby mostu je financován z vládního grantu a soukromou společností.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="d1fd2-120">V Dynamics 365 Finance můžete rozdělit fakturaci za jednu transakci nebo celý projekt mezi více zákazníků, grantů nebo organizací.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="d1fd2-121">V projektech, které mají více poskytovatelů financování, se všechny strany, které přispívají na financování projektu s rozšířeným financováním, nazývají zdroje financování.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="d1fd2-122">Poté, co je zákazník, organizace nebo grant definován jako zdroj financování, jej lze přiřadit k jednomu nebo více pravidlům financování.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="d1fd2-123">Pravidla financování obsahují kritéria, která určují, jak jsou alokovány poplatky k různým zdrojům financování projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="d1fd2-124">Vzhledem k tomu, že položky na skladě – například ty, které se objevují na nákupních požadavcích a objednávkách – nelze rozdělit, částku nákladů nelze v době distribuce rozdělit mezi více zdrojů financování.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="d1fd2-125">Proto zůstane hodnota zdroje financování 0 (nula), dokud nebude zaúčtována emise zásob.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="d1fd2-126">Když se zaúčtuje emise zásob, částka nákladů se rozdělí podle pravidel distribuce účtu pro projekt.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="d1fd2-127">Zde je několik kroků, které můžete podniknout, abyste usnadnili rozdělení fakturace mezi více zdrojů financování:</span><span class="sxs-lookup"><span data-stu-id="d1fd2-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="d1fd2-128">Určete, že všechny transakce zadané pro projekt používají stejnou měnu prodeje jako projektová smlouva.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="d1fd2-129">Nastavte limity financování tak, aby zdroj financování nebyl fakturován více než stanovenou částkou na projekt.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="d1fd2-130">Konfigurujte pravidla financování a limity financování pro každého pracovníka, položku, kategorii, skupinu kategorií a typ transakce (nebo pro všechny typy transakcí).</span><span class="sxs-lookup"><span data-stu-id="d1fd2-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="d1fd2-131">Vyberte nepovinné počáteční a koncové datum a definujte tak období platnosti každého pravidla financování.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="d1fd2-132">Uveďte procento, za které je každý zdroj financování odpovědný.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="d1fd2-133">Určete, který zdroj financování je zodpovědný za zaokrouhlování rozdílů, které jsou způsobeny výpočty alokace financování.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="d1fd2-134">Nastavte pravidla, která určují, jak jsou náklady na projekt fakturovány externím zákazníkům a účtovány interním organizacím.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="d1fd2-135">Zaznamenávejte transakce na účtu pozastaveného financování, dokud nebude možné získat další financování nebo dokud se nerozhodnete nést náklady interně.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="d1fd2-136">V projektu se vyhledá přiřazení daňové skupiny, aby bylo možné určit, která daňová skupina se má k transakci přidružit.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="d1fd2-137">Pokud na úrovni projektu nebylo provedeno žádné přiřazení daňové skupiny, prohledá se projektová smlouva.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="d1fd2-138">Příklad: Více zdrojů financování (jednoduchý)</span><span class="sxs-lookup"><span data-stu-id="d1fd2-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="d1fd2-139">Následující tabulka poskytuje scénáře pro správu alokace financování mezi více zdroji financování.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="d1fd2-140">Tyto scénáře jsou založeny na následujících předpokladech:</span><span class="sxs-lookup"><span data-stu-id="d1fd2-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="d1fd2-141">Nastavení priorit se zohledňuje v alokaci finančních prostředků před uplatněním dalšího kritéria pravidla financování.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="d1fd2-142">Nebylo zadáno žádné časové období k definování období d, kdy je pravidlo financování platné.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d1fd2-143"><strong>Scénář</strong></span><span class="sxs-lookup"><span data-stu-id="d1fd2-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="d1fd2-144"><strong>Zdroj financování</strong></span><span class="sxs-lookup"><span data-stu-id="d1fd2-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="d1fd2-145"><strong>Procento alokace</strong></span><span class="sxs-lookup"><span data-stu-id="d1fd2-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="d1fd2-146"><strong>Priorita přidělení</strong></span><span class="sxs-lookup"><span data-stu-id="d1fd2-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1fd2-147">Chcete přidělit náklady jednomu zdroji financování, dokud nebudou vyčerpány jeho prostředky, přidělit náklady druhému zdroji financování, dokud nebudou vyčerpány jeho prostředky, a nakonec přidělit zbývající náklady třetímu zdroji financování.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="d1fd2-148">Zdroj　financování　1</span><span class="sxs-lookup"><span data-stu-id="d1fd2-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="d1fd2-149">Zdroj　financování　2</span><span class="sxs-lookup"><span data-stu-id="d1fd2-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="d1fd2-150">Zdroj　financování　3</span><span class="sxs-lookup"><span data-stu-id="d1fd2-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d1fd2-151">100%</span><span class="sxs-lookup"><span data-stu-id="d1fd2-151">100%</span></span></li>
<li><span data-ttu-id="d1fd2-152">100%</span><span class="sxs-lookup"><span data-stu-id="d1fd2-152">100%</span></span></li>
<li><span data-ttu-id="d1fd2-153">100%</span><span class="sxs-lookup"><span data-stu-id="d1fd2-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d1fd2-154">0</span><span class="sxs-lookup"><span data-stu-id="d1fd2-154">1</span></span></li>
<li><span data-ttu-id="d1fd2-155">2</span><span class="sxs-lookup"><span data-stu-id="d1fd2-155">2</span></span></li>
<li><span data-ttu-id="d1fd2-156">3</span><span class="sxs-lookup"><span data-stu-id="d1fd2-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1fd2-157">Chcete přidělit 75 procent nákladů jednomu zdroji financování a 25 procent druhému zdroji financování.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="d1fd2-158">Když je některý z těchto zdrojů financování vyčerpán, chcete uhradit zbývající náklady z třetího zdroje financování.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="d1fd2-159">Zdroj　financování　1</span><span class="sxs-lookup"><span data-stu-id="d1fd2-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="d1fd2-160">Zdroj　financování　2</span><span class="sxs-lookup"><span data-stu-id="d1fd2-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="d1fd2-161">Zdroj　financování　3</span><span class="sxs-lookup"><span data-stu-id="d1fd2-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d1fd2-162">75 %</span><span class="sxs-lookup"><span data-stu-id="d1fd2-162">75%</span></span></li>
<li><span data-ttu-id="d1fd2-163">25 %</span><span class="sxs-lookup"><span data-stu-id="d1fd2-163">25%</span></span></li>
<li><span data-ttu-id="d1fd2-164">100%</span><span class="sxs-lookup"><span data-stu-id="d1fd2-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d1fd2-165">0</span><span class="sxs-lookup"><span data-stu-id="d1fd2-165">1</span></span></li>
<li><span data-ttu-id="d1fd2-166">0</span><span class="sxs-lookup"><span data-stu-id="d1fd2-166">1</span></span></li>
<li><span data-ttu-id="d1fd2-167">2</span><span class="sxs-lookup"><span data-stu-id="d1fd2-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1fd2-168">Chcete přidělit 75 procent nákladů jednomu zdroji financování a 25 procent druhému zdroji financování.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="d1fd2-169">Když je některý z těchto zdrojů financování vyčerpán, chcete rozdělit zbývající náklady mezi třetí a čtvrtý zdroj financování.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="d1fd2-170">Zdroj　financování　1</span><span class="sxs-lookup"><span data-stu-id="d1fd2-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="d1fd2-171">Zdroj　financování　2</span><span class="sxs-lookup"><span data-stu-id="d1fd2-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="d1fd2-172">Zdroj　financování　3</span><span class="sxs-lookup"><span data-stu-id="d1fd2-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="d1fd2-173">Zdroj　financování　4</span><span class="sxs-lookup"><span data-stu-id="d1fd2-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d1fd2-174">75 %</span><span class="sxs-lookup"><span data-stu-id="d1fd2-174">75%</span></span></li>
<li><span data-ttu-id="d1fd2-175">25 %</span><span class="sxs-lookup"><span data-stu-id="d1fd2-175">25%</span></span></li>
<li><span data-ttu-id="d1fd2-176">50 %</span><span class="sxs-lookup"><span data-stu-id="d1fd2-176">50%</span></span></li>
<li><span data-ttu-id="d1fd2-177">50 %</span><span class="sxs-lookup"><span data-stu-id="d1fd2-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d1fd2-178">0</span><span class="sxs-lookup"><span data-stu-id="d1fd2-178">1</span></span></li>
<li><span data-ttu-id="d1fd2-179">0</span><span class="sxs-lookup"><span data-stu-id="d1fd2-179">1</span></span></li>
<li><span data-ttu-id="d1fd2-180">2</span><span class="sxs-lookup"><span data-stu-id="d1fd2-180">2</span></span></li>
<li><span data-ttu-id="d1fd2-181">2</span><span class="sxs-lookup"><span data-stu-id="d1fd2-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1fd2-182">Chcete přidělit prvních 25 procent nákladů jednomu zdroji financování a zbytek druhému zdroji financování.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="d1fd2-183">Zdroj　financování　1</span><span class="sxs-lookup"><span data-stu-id="d1fd2-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="d1fd2-184">Zdroj　financování　2</span><span class="sxs-lookup"><span data-stu-id="d1fd2-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d1fd2-185">25 %</span><span class="sxs-lookup"><span data-stu-id="d1fd2-185">25%</span></span></li>
<li><span data-ttu-id="d1fd2-186">100%</span><span class="sxs-lookup"><span data-stu-id="d1fd2-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d1fd2-187">0</span><span class="sxs-lookup"><span data-stu-id="d1fd2-187">1</span></span></li>
<li><span data-ttu-id="d1fd2-188">2</span><span class="sxs-lookup"><span data-stu-id="d1fd2-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="d1fd2-189">Příklad: Více zdrojů financování (složitý)</span><span class="sxs-lookup"><span data-stu-id="d1fd2-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="d1fd2-190">Máte tři zdroje financování, které chcete použít v následujícím pořadí:</span><span class="sxs-lookup"><span data-stu-id="d1fd2-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="d1fd2-191">Používejte zdroj financování 2 a zdroj financování 3 rovnoměrně, dokud nebude vyčerpán zdroj financování 2.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="d1fd2-192">Pokračujte v používání zdroje financování 3, dokud nebude vyčerpán.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="d1fd2-193">Po vyčerpání zdroje financování 3 použijte zdroj financování 1.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="d1fd2-194">K dosažení tohoto cíle musíte provést následující postup:</span><span class="sxs-lookup"><span data-stu-id="d1fd2-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="d1fd2-195">Nastavte limity financování pro zdroj financování 2 a zdroj financování 3 na jejich odpovídající částky.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="d1fd2-196">Vytvořte následující pravidla financování:</span><span class="sxs-lookup"><span data-stu-id="d1fd2-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="d1fd2-197">Pravidlo 1 (Priorita 1): Přidělte 50 procent transakcí zdroji financování 2 a 50 procent zdroji financování 3.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="d1fd2-198">Pravidlo 2 (Priorita 2): Přidělte 100 procent transakcí zdroji financování 3.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="d1fd2-199">Pravidlo 3 (Priorita 3): Přidělte 100 procent transakcí zdroji financování 1.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="d1fd2-200">Toto nastavení funguje, protože transakce jsou prověřovány na základě pravidel a limitů, aby se určilo, zda se na transakci vztahuje některé pravidlo nebo limit.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="d1fd2-201">Pokud se na transakci nevztahují žádná konkrétní pravidla nebo limity, použije se pravidlo Všechny transakce.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="d1fd2-202">Pravidlo Všechny transakce odpovídá všem transakcím.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="d1fd2-203">Pokud je nalezeno pravidlo, které odpovídá transakci, použije se nejprve procento, které bylo přiděleno v tomto pravidle, ale až poté, co jsou shody porovnány s nastavenými limity.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="d1fd2-204">Pokud byl limit splněn a prostředky zdroje financování jsou vyčerpány, pravidlo financování spojené s limitem financování bude ignorováno a program hledá další platné pravidlo.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="d1fd2-205">V některých případech lze podle pravidla přidělit pouze část transakce.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="d1fd2-206">K tomu může dojít, protože při alokaci transakce je dosaženo limitu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="d1fd2-207">V tomto případě je podle tohoto pravidla přidělena pouze určitá částka, například 50 procent na každý zdroj financování.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="d1fd2-208">To je případ pravidla 1, které je popsáno dříve v této části.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="d1fd2-209">Zbytek je přidělen podle dalšího pravidla v pořadí.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="d1fd2-210">Následující tabulka zkoumá tento scénář podrobněji.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d1fd2-211"><strong>Zaměření</strong></span><span class="sxs-lookup"><span data-stu-id="d1fd2-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="d1fd2-212"><strong>Podrobnosti</strong></span><span class="sxs-lookup"><span data-stu-id="d1fd2-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1fd2-213">Pravidla financování</span><span class="sxs-lookup"><span data-stu-id="d1fd2-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="d1fd2-214">Pravidlo 1 (Priorita 1): Všechny transakce.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="d1fd2-215">Přidělte zdroj financování 2 s 50 % a zdroj financování 3 s 50 %.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="d1fd2-216">Pravidlo 2 (Priorita 2): Všechny transakce.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="d1fd2-217">Přidělte zdroj financování 3 se 100 %.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="d1fd2-218">Pravidlo 3 (Priorita 2): Všechny transakce.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="d1fd2-219">Přidělte zdroj financování 1 se 100 %.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1fd2-220">Limity financování</span><span class="sxs-lookup"><span data-stu-id="d1fd2-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="d1fd2-221">Limit zdroje financování 1 = 10 000,00</span><span class="sxs-lookup"><span data-stu-id="d1fd2-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="d1fd2-222">Limit zdroje financování 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="d1fd2-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="d1fd2-223">Limit zdroje financování 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="d1fd2-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1fd2-224">Transakce 1</span><span class="sxs-lookup"><span data-stu-id="d1fd2-224">Transaction 1</span></span></td>
<td><span data-ttu-id="d1fd2-225"><strong>Částka transakce:</strong> 100,00<strong>Financování:</strong> Transakce se vyplácí pouze podle pravidla 1, protože transakce je plně zaplacena po uplatnění pravidla 1.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="d1fd2-226">Transakce je financována rovnoměrně mezi zdrojem financování 2 a zdrojem financování 3.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="d1fd2-227">Zdroj financování 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="d1fd2-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="d1fd2-228">Zdroj financování 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="d1fd2-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1fd2-229">Transakce 2</span><span class="sxs-lookup"><span data-stu-id="d1fd2-229">Transaction 2</span></span></td>
<td><span data-ttu-id="d1fd2-230"><strong>Částka transakce</strong> 5 000,00<strong>Financování:</strong> Transakce se vyplácí podle všech tří pravidel.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="d1fd2-231"><strong>Pravidlo 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="d1fd2-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="d1fd2-232">Zdroj financování 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="d1fd2-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="d1fd2-233">Zdroj financování 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="d1fd2-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="d1fd2-234">
<strong>Pravidlo 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="d1fd2-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="d1fd2-235">Zdroj financování 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="d1fd2-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="d1fd2-236">
<strong>Pravidlo 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="d1fd2-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="d1fd2-237">Zdroj financování 1: 3 850,00 (= 5 000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="d1fd2-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1fd2-238">Celkové prostředky, které jsou rozděleny pro každý zdroj financování</span><span class="sxs-lookup"><span data-stu-id="d1fd2-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="d1fd2-239">Zdroj financování 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="d1fd2-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="d1fd2-240">Zdroj financování 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="d1fd2-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="d1fd2-241">Zdroj financování 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="d1fd2-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="d1fd2-242">Pravidla fakturace</span><span class="sxs-lookup"><span data-stu-id="d1fd2-242">Billing rules</span></span>
<span data-ttu-id="d1fd2-243">Když sjednáváte projektovou smlouvu se zákazníkem, definujete, jak a kdy můžete zákazníkovi fakturovat práci na projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="d1fd2-244">Poté, co nastavíte projektovou smlouvu a projekt, můžete nastavit pravidla fakturace pro projekt.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="d1fd2-245">Pravidla fakturace jsou založena na smluvních podmínkách projektu, které jsou uvedeny ve smlouvě o projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="d1fd2-246">Pravidla fakturace, která můžete vytvořit, závisí na smluvních podmínkách projektové smlouvy a typu projektu, jako je Čas a materiál nebo Pevná cena, který přidružíte k pravidlu fakturace.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="d1fd2-247">Pro projektovou smlouvu můžete vytvořit více než jedno fakturační pravidlo.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="d1fd2-248">Pravidlo fakturace můžete také přiřadit několika projektům, které jsou spojeny se stejnou projektovou smlouvou a mají podobné fakturační podmínky.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="d1fd2-249">Můžete nastavit následující typy pravidel fakturace:</span><span class="sxs-lookup"><span data-stu-id="d1fd2-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="d1fd2-250">**Jednotka dodávky** – Fakturujte zákazníka, když dokončíte jednotku dodávky.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="d1fd2-251">Jednotky dodávky definujete ve smlouvě.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="d1fd2-252">**Pokrok** – Fakturujte zákazníka, když dokončíte stanovené procento projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="d1fd2-253">Můžete nastavit pravidlo fakturace, které automaticky vypočítá procento dokončené práce, nebo můžete ručně vypočítat procento dokončené práce a částku fakturovanou zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="d1fd2-254">**Milník** – Fakturujte zákazníkovi celou částku milníku projektu, když je milníku dosaženo.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="d1fd2-255">**Poplatek** – Fakturujte zákazníkovi své služby plus poplatek za správu, což je obvykle procento z ceny služeb.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="d1fd2-256">**Čas a materiál** – Fakturujte zákazníkovi hodnotu času a materiálů použitých na projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="d1fd2-257">U všech typů pravidel fakturace můžete určit retenční procento, které se odečte od faktur zákazníka, dokud projekt nedosáhne dohodnuté fáze.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="d1fd2-258">Procento zadržení platby je uvedeno v projektové smlouvě.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="d1fd2-259">Částka se vypočítá na základě celkové hodnoty řádků ve faktuře zákazníka, od které bude odečtena.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="d1fd2-260">U pravidel fakturace **Čas a materiál** a **Pokrok** můžete přiřadit zpoplatněné kategorie.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="d1fd2-261">Zpoplatněné kategorie označují transakce, které by měly být zahrnuty do faktur zákazníka.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="d1fd2-262">Když jste připraveni fakturovat zákazníkovi, vypočítá se fakturovaná částka za projekt na základě pravidel fakturace a vygeneruje se návrh faktury projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="d1fd2-263">V následujících částech jsou uvedeny příklady, které ukazují, jak nastavit a spravovat pravidla fakturace pro projekt.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="d1fd2-264">Příklad: Vytvořte fakturační pravidlo, které je založeno na počtu dodaných jednotek.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="d1fd2-265">Vaše organizace uzavře dohodu o realizaci celkem pěti školení pro zaměstnance zákazníka s cenou 10 000 za jedno školení.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="d1fd2-266">Zákazníkovi zašlete fakturu po každém školení.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="d1fd2-267">Když nastavíte pravidla fakturace pro smlouvu, použijete následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d1fd2-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="d1fd2-268">Jednotkou dodávky je jedno školení.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="d1fd2-269">Jednotková cena je 10 000 za školení.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="d1fd2-270">Celkový počet jednotek je pět školení.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="d1fd2-271">Po absolvování jednoho školení můžete vytvořit fakturu s částkou 10 000 za první dodanou jednotku a odeslat fakturu zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="d1fd2-272">Příklad: Vytvořte fakturační pravidlo založené na zadaném procentu dokončení projektu (ruční výpočet)</span><span class="sxs-lookup"><span data-stu-id="d1fd2-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="d1fd2-273">Vaše organizace – softwarová poradenská firma – uzavírá se zákazníkem dohodu o vývoji části produktu, který zákazník vyvíjí.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="d1fd2-274">Vaše organizace souhlasí s dodáním softwarového kódu během šesti měsíců.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="d1fd2-275">Zákazník se zavazuje zaplatit vaší organizaci za práci celkem 100 000.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="d1fd2-276">Vytvoříte fakturační pravidlo pro fakturaci zákazníkovi na základě procenta práce dokončené na projektu, jak je uvedeno ve smlouvě.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="d1fd2-277">Na konci prvního měsíce dojde ke schůzce se zákazníkem, abyste určili procento dokončené práce.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="d1fd2-278">Poté, co vy a zákazník zkontrolujete projekt, se rozhodnete, že je projekt dokončen na 15 procent.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="d1fd2-279">Vytvoříte fakturu s částkou 15 000 (15 procent ze 100 000) a odešlete ji zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="d1fd2-280">Příklad: Vytvořte fakturační pravidlo založené na zadaném procentu dokončení projektu (automatický výpočet)</span><span class="sxs-lookup"><span data-stu-id="d1fd2-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="d1fd2-281">Vaše organizace – zabývající se vývojem softwaru – souhlasí s vytvořením balíčku mzdového účetnictví pro zákazníka za 30 000.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="d1fd2-282">Zákazník se zavazuje zaplatit vaší organizaci na základě procenta dokončené práce.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="d1fd2-283">Odhadujete, že náklady na projekt budou 20 000.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="d1fd2-284">Projektová smlouva určuje kategorie prací, které používáte v procesu fakturace.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="d1fd2-285">Nastavíte pravidla fakturace, která automaticky vypočítají částky faktury pro procento práce dokončené v každé kategorii.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="d1fd2-286">Nastavíte rozpočet pro každou kategorii:</span><span class="sxs-lookup"><span data-stu-id="d1fd2-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="d1fd2-287">**Vývoj** - Náklady 15 000 a výnosy 20 000</span><span class="sxs-lookup"><span data-stu-id="d1fd2-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="d1fd2-288">**Instalace** - Náklady 5 000 a výnosy 10 000</span><span class="sxs-lookup"><span data-stu-id="d1fd2-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="d1fd2-289">Když vytvoříte fakturu zákazníka poprvé, částka faktury se automaticky vypočítá na základě následujících informací:</span><span class="sxs-lookup"><span data-stu-id="d1fd2-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="d1fd2-290">Po měsíci pracovník projektu odešle časový rozvrh prací na projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="d1fd2-291">Náklady na odpracované hodiny jsou 5 000 za vývoj a 1 000 za instalaci.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="d1fd2-292">Vývojové práce jsou dokončeny z 33 procent (5 000 skutečných nákladů / 15 000 rozpočtových nákladů) a instalační práce jsou dokončeny z 20 procent (1 000 skutečných nákladů / 5 000 rozpočtových nákladů).</span><span class="sxs-lookup"><span data-stu-id="d1fd2-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="d1fd2-293">Automaticky se vypočítá fakturovaná částka 8 667 (33 procent z 20 000 + 20 procent z 10 000).</span><span class="sxs-lookup"><span data-stu-id="d1fd2-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="d1fd2-294">Vytvoříte fakturu s částkou 8 667 a odešlete ji zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="d1fd2-295">Příklad: Vytvořte fakturační pravidlo založené na dohodnutých milnících</span><span class="sxs-lookup"><span data-stu-id="d1fd2-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="d1fd2-296">Vaše organizace – poradenská společnost pro management – souhlasí s provedením průzkumu trhu pro spotřební výrobek, který zákazník hodlá prodávat.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="d1fd2-297">Zákazník souhlasí s používáním vašich služeb po dobu tří měsíců, počínaje březnem, a zavazuje se zaplatit vaší organizaci 50 000.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="d1fd2-298">Projekt má tři milníky:</span><span class="sxs-lookup"><span data-stu-id="d1fd2-298">The project has three milestones:</span></span>

-   <span data-ttu-id="d1fd2-299">Milník 1: Shromažďování údajů o spotřebitelích - 31. března</span><span class="sxs-lookup"><span data-stu-id="d1fd2-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="d1fd2-300">Milník 2: Analýza spotřebitelských dat - 30. dubna</span><span class="sxs-lookup"><span data-stu-id="d1fd2-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="d1fd2-301">Milník 3: Představení návrhu životaschopnosti produktu - 31. května</span><span class="sxs-lookup"><span data-stu-id="d1fd2-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="d1fd2-302">Zákazník souhlasí, že vaší organizaci zaplatí 10 000 za první milník, 20 000 za druhý milník a 20 000 za třetí milník.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="d1fd2-303">Když nastavujete projektovou smlouvu, souhlasíte s fakturací zákazníkovi na základě milníku, který byl dokončen.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="d1fd2-304">Nastavení pravidla fakturace zahrnuje následující kroky:</span><span class="sxs-lookup"><span data-stu-id="d1fd2-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="d1fd2-305">Definujte milníky projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-305">Define the project milestones.</span></span>
-   <span data-ttu-id="d1fd2-306">Definujte částku, která bude zákazníkovi fakturována po dokončení každého milníku.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="d1fd2-307">Když je první milník dokončen 31. března, označíte milník jako dokončený a poté vytvoříte fakturu s částkou 10 000 a odešlete ji zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="d1fd2-308">Fakturu za milník nemůžete vytvořit, dokud milník neoznačíte jako dokončený.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="d1fd2-309">Příklad: Vytvořte fakturační pravidlo založené na službách plus poplatek za správu</span><span class="sxs-lookup"><span data-stu-id="d1fd2-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="d1fd2-310">Vaše organizace – poradenská firma pro management – souhlasí s provedením průzkumu trhu, jehož cílem je vyhodnocení životaschopnosti produktu, který vyvíjí maloobchodní společnost zákazníka.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="d1fd2-311">Podmínky smlouvy upřesňují, že budete poskytovat služby vašim třem nejlepším konzultantům v oblasti managementu, kteří budou provádět výzkum na základě časových a materiálových podkladů.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="d1fd2-312">Zákazník souhlasí s tím, že zaplatí 100 za hodinu plus 10% poplatek za správu za konzultační hodiny účtované projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="d1fd2-313">Když připravujete projektovou smlouvu, vytvořte fakturační pravidlo a přidejte 10% poplatek za správu ke konzultačním hodinám účtovaným projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="d1fd2-314">Když vytvoříte fakturu pro zákazníka, bude zákazníkovi účtován poplatek za správu ve výši 10 procent plus náklady na konzultační hodiny.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="d1fd2-315">Například pokud tři konzultanti na projektu pracovali celkem 200 hodin, vytvoří se faktura za 22 000 na základě následujícího výpočtu:</span><span class="sxs-lookup"><span data-stu-id="d1fd2-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="d1fd2-316">200 hodin s cenou 100 za hodinu = 20 000</span><span class="sxs-lookup"><span data-stu-id="d1fd2-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="d1fd2-317">10% poplatek za správu = 2 000</span><span class="sxs-lookup"><span data-stu-id="d1fd2-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="d1fd2-318">Celková částka faktury = 22 000</span><span class="sxs-lookup"><span data-stu-id="d1fd2-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="d1fd2-319">Pokud jsou poplatky zdanitelné zákazníkovi a v projektové smlouvě vyberete skupinu daně z obratu, zadá se skupina daně z obratu automaticky do pravidla fakturace poplatků.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="d1fd2-320">Příklad: Vytvořte fakturační pravidlo pro cenu času a materiálů</span><span class="sxs-lookup"><span data-stu-id="d1fd2-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="d1fd2-321">Vaše organizace – softwarová poradenská společnost – souhlasí s poskytnutím pěti technických konzultantů pro práci na projektu vývoje softwaru pro zákazníka na příštích šest měsíců.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="d1fd2-322">Zákazník souhlasí se zaplacením 150 za každou konzultační hodinu plus náklady na kancelářské potřeby.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="d1fd2-323">Vaše organizace pošle zákazníkovi fakturu na konci každého měsíce.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="d1fd2-324">Při uzavírání projektové smlouvy souhlasíte, že budete zákazníkovi každý měsíc fakturovat čas a materiály týkající se projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="d1fd2-325">Vytvoříte fakturační pravidlo, které obsahuje následující informace:</span><span class="sxs-lookup"><span data-stu-id="d1fd2-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="d1fd2-326">Smluvní období je šest měsíců.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-326">The contract period is six months.</span></span>
-   <span data-ttu-id="d1fd2-327">Konzultační čas se vypočítá sazbou 150 za hodinu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="d1fd2-328">Kancelářské potřeby jsou fakturovány v jejich ceně a celkové náklady na projekt nesmí překročit 10 000.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="d1fd2-329">Zákaznickou fakturu vytvoříte na konci každého kalendářního měsíce během projektu.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="d1fd2-330">Během prvního měsíce konzultanti projektu odpracovali celkem 800 hodin.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="d1fd2-331">Náklady na kancelářské potřeby účtované projektu jsou 2 000.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="d1fd2-332">Na konci měsíce tedy vytvoříte fakturu s částkou 122 000, která se počítá jako 800 hodin krát 150 za hodinu, plus 2 000 za kancelářské potřeby.</span><span class="sxs-lookup"><span data-stu-id="d1fd2-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



