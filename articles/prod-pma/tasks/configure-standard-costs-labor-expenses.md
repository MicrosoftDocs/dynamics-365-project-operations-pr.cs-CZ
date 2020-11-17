---
title: Konfigurace standardních nákladů na práci a výdaje
description: Toto téma vysvětluje, jak nastavit standardní náklady na práci a výdaje na projekt.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073837"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="16a3b-103">Konfigurace standardních nákladů na práci a výdaje</span><span class="sxs-lookup"><span data-stu-id="16a3b-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="16a3b-104">Toto téma vysvětluje, jak nastavit standardní náklady na práci a výdaje na projekt.</span><span class="sxs-lookup"><span data-stu-id="16a3b-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="16a3b-105">Tento úkol používá datovou sadu USSI.</span><span class="sxs-lookup"><span data-stu-id="16a3b-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="16a3b-106">V navigačním podokně přejděte na **Moduly> Řízení projektů a účetnictví> Nastavení> Ceny> Nákladová cena (hodina)**.</span><span class="sxs-lookup"><span data-stu-id="16a3b-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="16a3b-107">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="16a3b-107">Select **New**.</span></span>
3. <span data-ttu-id="16a3b-108">Do pole **Datum účinnosti** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="16a3b-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="16a3b-109">Do pole **Nákladová cena** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="16a3b-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="16a3b-110">Můžete nastavit standardní nákladovou cenu pro kategorii projektu nebo můžete nastavit nákladovou cenu podle čísla pracovníka, čísla projektu, kategorie, data nebo jakékoli jejich kombinace.</span><span class="sxs-lookup"><span data-stu-id="16a3b-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="16a3b-111">Nákladová cena, která se použije, je nákladová cena s nejvyšší úrovní podrobností.</span><span class="sxs-lookup"><span data-stu-id="16a3b-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="16a3b-112">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="16a3b-112">Select **Save**.</span></span>
6. <span data-ttu-id="16a3b-113">V navigačním podokně přejděte na **Moduly> Řízení projektů a účetnictví> Nastavení> Ceny> Prodejní cena (hodina)**.</span><span class="sxs-lookup"><span data-stu-id="16a3b-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="16a3b-114">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="16a3b-114">Select **New**.</span></span>
8. <span data-ttu-id="16a3b-115">Do pole **Datum účinnosti** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="16a3b-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="16a3b-116">V poli **Platné pro** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="16a3b-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="16a3b-117">Do pole **Ceny** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="16a3b-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="16a3b-118">Můžete nastavit standardní prodejní cenu pro hodinové transakce nebo pro kategorii projektu.</span><span class="sxs-lookup"><span data-stu-id="16a3b-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="16a3b-119">Můžete také nastavit prodejní ceny podle čísla pracovníka, čísla projektu, kategorie, data transakce nebo jakékoli jejich kombinace.</span><span class="sxs-lookup"><span data-stu-id="16a3b-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="16a3b-120">Skutečná prodejní cena, která se použije, když pracovník zadá transakci do deníku hodin, je prodejní cena s nejvyšší úrovní podrobností.</span><span class="sxs-lookup"><span data-stu-id="16a3b-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="16a3b-121">Například pokud je nastavena jak obecná prodejní cena, tak prodejní cena specifická pro pracovníka, použije se prodejní cena specifická pro pracovníka.</span><span class="sxs-lookup"><span data-stu-id="16a3b-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="16a3b-122">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="16a3b-122">Select **Save**.</span></span>
12. <span data-ttu-id="16a3b-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="16a3b-123">Close the page.</span></span>
13. <span data-ttu-id="16a3b-124">V navigačním podokně přejděte na **Moduly> Řízení projektů a účetnictví> Nastavení> Ceny> Nákladová cena (výdaj)**.</span><span class="sxs-lookup"><span data-stu-id="16a3b-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="16a3b-125">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="16a3b-125">Select **New**.</span></span>
15. <span data-ttu-id="16a3b-126">Do pole **Datum účinnosti** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="16a3b-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="16a3b-127">Do pole **Nákladová cena** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="16a3b-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="16a3b-128">Lze vyplnit více polí, ale toto je minimum potřebné k uložení záznamu.</span><span class="sxs-lookup"><span data-stu-id="16a3b-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="16a3b-129">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="16a3b-129">Select **Save**.</span></span>
18. <span data-ttu-id="16a3b-130">V navigačním podokně přejděte na **Moduly> Řízení projektů a účetnictví> Nastavení> Ceny> Prodejní cena (výdaj)**.</span><span class="sxs-lookup"><span data-stu-id="16a3b-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="16a3b-131">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="16a3b-131">Select **New**.</span></span>
20. <span data-ttu-id="16a3b-132">Do pole **Datum účinnosti** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="16a3b-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="16a3b-133">V poli **Platné pro** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="16a3b-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="16a3b-134">Do pole **Ceny** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="16a3b-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="16a3b-135">Skutečná prodejní cena, která se použije, když pracovník zadá transakce do deníku výdaje, je prodejní cena s nejvyšší úrovní podrobností.</span><span class="sxs-lookup"><span data-stu-id="16a3b-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="16a3b-136">Například pokud je nastavena jak obecná prodejní cena, tak prodejní cena specifická pro pracovníka, použije se prodejní cena specifická pro pracovníka.</span><span class="sxs-lookup"><span data-stu-id="16a3b-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="16a3b-137">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="16a3b-137">Select **Save**.</span></span>
