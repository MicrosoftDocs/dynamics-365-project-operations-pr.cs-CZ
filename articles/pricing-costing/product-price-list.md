---
title: Produktové ceníky
description: Tento téma poskytuje informace o cenících v katalogových cenách používaných pro projektové nabídky a smlouvy.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 02d274725983e50adc35a4cae1ac60c35be346a4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004928"
---
# <a name="product-price-lists"></a><span data-ttu-id="35d62-103">Produktové ceníky</span><span class="sxs-lookup"><span data-stu-id="35d62-103">Product price lists</span></span>

<span data-ttu-id="35d62-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="35d62-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="35d62-105">V Project Operations podporují **Ceníky produktů** a související entity položek ceníku funkčnost pro oceňování produktů na základě řádků nabídek a smluv založených na produktu.</span><span class="sxs-lookup"><span data-stu-id="35d62-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="35d62-106">U produktů použitých na projektech se používají záznamy položek ceníku pro projektové ceníky.</span><span class="sxs-lookup"><span data-stu-id="35d62-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="35d62-107">Produkty by měly být nastaveny tak, aby měly v katalogu produktů výchozí nákladové ceníky a ceníky.</span><span class="sxs-lookup"><span data-stu-id="35d62-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="35d62-108">Ke konfiguraci výchozích nákladových cen a ceníků použijte ceníkovou cenu, standardní cenu a aktuální cenu.</span><span class="sxs-lookup"><span data-stu-id="35d62-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="35d62-109">Výchozí ceníky se používají na řádku nabídky nebo řádku projektové smlouvy pouze v případě, že systém nemůže pro tento produkt najít řádek ceníku v produktovém ceníku pro nabídku nebo projektovou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="35d62-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="35d62-110">Nákladová cena řádků katalogu produktů může být změněna mezi nabídkami.</span><span class="sxs-lookup"><span data-stu-id="35d62-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="35d62-111">Tato možnost je důležitá, protože pokud přesně nesledujete náklady, nemůžete u učastí na projektu určit provozní zisky.</span><span class="sxs-lookup"><span data-stu-id="35d62-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="35d62-112">Ve výchozím nastavení se standardní cena produktu používá jako nákladová cena.</span><span class="sxs-lookup"><span data-stu-id="35d62-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="35d62-113">Výchozí nákladovou cenu je však možné na řádku nabídky aktualizovat, pokud pro tuto nabídku existuje jiná nákladová cena.</span><span class="sxs-lookup"><span data-stu-id="35d62-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="35d62-114">Položky ceníku</span><span class="sxs-lookup"><span data-stu-id="35d62-114">Price list items</span></span>

<span data-ttu-id="35d62-115">Produkty z katalogu produktů můžete přidat do různých ceníků.</span><span class="sxs-lookup"><span data-stu-id="35d62-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="35d62-116">Řádky ceníku pro produkty vždy odkazují na určitou jednotku.</span><span class="sxs-lookup"><span data-stu-id="35d62-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="35d62-117">Ocenění produktu v položkách ceníku lze konfigurovat jako částku v měně.</span><span class="sxs-lookup"><span data-stu-id="35d62-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="35d62-118">Alternativně může být nakonfigurována jako funkce ceníku, aktuální ceny nebo standardní ceny.</span><span class="sxs-lookup"><span data-stu-id="35d62-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="35d62-119">Funkčnost ocenění podporuje různé možnosti zaokrouhlení, pokud jsou ceny produktů konfigurovány jako funkce ceníku, standardní ceny nebo aktuální ceny.</span><span class="sxs-lookup"><span data-stu-id="35d62-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="35d62-120">Kromě využití více způsobů ocenění a možností zaokrouhlení můžete k položkám ceníku přidružit seznamy slev.</span><span class="sxs-lookup"><span data-stu-id="35d62-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="35d62-121">Výchozí ceník produktu</span><span class="sxs-lookup"><span data-stu-id="35d62-121">Default product price list</span></span>
<span data-ttu-id="35d62-122">Každý záznam zákazníka obsahuje pole **Výchozí ceník**, ve kterém můžete určit ceník, který odpovídá měně zákazníka.</span><span class="sxs-lookup"><span data-stu-id="35d62-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="35d62-123">Do tohoto pole nevloží automaticky výchozí hodnota.</span><span class="sxs-lookup"><span data-stu-id="35d62-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="35d62-124">Pokud existuje vlastní cenová dohoda s určitým zákazníkem, můžete toto pole použít k přidružení ceníku k tomuto zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="35d62-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="35d62-125">Entity Příležitost, Nabídka a Projektová smlouva používají k zadávání výchozích ceníků produktů následující pořadí.</span><span class="sxs-lookup"><span data-stu-id="35d62-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="35d62-126">Stejné pořadí se používá pro projektové ceníky.</span><span class="sxs-lookup"><span data-stu-id="35d62-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="35d62-127">Nabídka</span><span class="sxs-lookup"><span data-stu-id="35d62-127">Quote</span></span>
2.  <span data-ttu-id="35d62-128">Příležitost</span><span class="sxs-lookup"><span data-stu-id="35d62-128">Opportunity</span></span>
3.  <span data-ttu-id="35d62-129">Zákazník</span><span class="sxs-lookup"><span data-stu-id="35d62-129">Customer</span></span>
4.  <span data-ttu-id="35d62-130">Globální nastavení</span><span class="sxs-lookup"><span data-stu-id="35d62-130">Global settings</span></span> 

<span data-ttu-id="35d62-131">Ve výchozím nastavení uvádí pole **Produkt** na řádku nabídky všechny aktivní produkty v ceníku produktu nabídky.</span><span class="sxs-lookup"><span data-stu-id="35d62-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="35d62-132">Pokud byl produkt inaktivován nebo pokud se jedná o koncept produktu, není v seznamu uveden, i když je v ceníku.</span><span class="sxs-lookup"><span data-stu-id="35d62-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="35d62-133">Řádky katalogu produktů jsou přidány jako řádky faktury v první faktuře, která je vytvořena pro projektovou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="35d62-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="35d62-134">Tyto řádky faktury lze v konceptu faktury odstranit.</span><span class="sxs-lookup"><span data-stu-id="35d62-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="35d62-135">V takovém případě se řádky objeví na následující faktuře, dokud nebudou fakturovány nebo dokud nebude faktura odeslána zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="35d62-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="35d62-136">Nelze fakturovat částečné množství z řádku faktury za produkt.</span><span class="sxs-lookup"><span data-stu-id="35d62-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="35d62-137">Při fakturaci řádků produktu z projektové smlouvy se vytvoří skutečné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="35d62-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="35d62-138">Tyto skutečné hodnoty však nejsou propojeny se související entitou projektu.</span><span class="sxs-lookup"><span data-stu-id="35d62-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="35d62-139">Jinými slovy, řádky projektové smlouvy založené na produktu jsou nezávislé na jakémkoli použití založeném na projektu.</span><span class="sxs-lookup"><span data-stu-id="35d62-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
