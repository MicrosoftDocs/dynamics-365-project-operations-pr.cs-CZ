---
title: Konfigurace fakturace mezipodnikového projektu
description: Tento téma ukazuje, jak nastavit fakturaci projektu mezi dvěma společnostmi ve vaší organizaci.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073839"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="e008e-103">Konfigurace fakturace mezipodnikového projektu</span><span class="sxs-lookup"><span data-stu-id="e008e-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e008e-104">Tento téma ukazuje, jak nastavit fakturaci projektu mezi dvěma společnostmi ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="e008e-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="e008e-105">Tento úkol používá datovou sadu USSI.</span><span class="sxs-lookup"><span data-stu-id="e008e-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="e008e-106">V navigačním podokně přejděte na **Moduly > Závazky > Dodavatelé > Všichni dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="e008e-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="e008e-107">V seznamu **Všichni dodavatelé** vyhledejte a vyberte požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="e008e-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="e008e-108">V podokně akcí vyberte **Obecné**.</span><span class="sxs-lookup"><span data-stu-id="e008e-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="e008e-109">Vyberte **Mezipodnikové**.</span><span class="sxs-lookup"><span data-stu-id="e008e-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="e008e-110">Nastavte **Aktivní** na **Ano** k povolení vnitropodnikového obchodování.</span><span class="sxs-lookup"><span data-stu-id="e008e-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="e008e-111">V poli **Společnost zákazníka** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e008e-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="e008e-112">V poli **Můj obchodní vztah** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e008e-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="e008e-113">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e008e-113">Select **Save**.</span></span>
9. <span data-ttu-id="e008e-114">Zavřete stránky a vraťte se na domovskou stránku.</span><span class="sxs-lookup"><span data-stu-id="e008e-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="e008e-115">V navigačním podokně přejděte na **Moduly> Řízení projektů a účetnictví> Nastavení > Ceny> Parametry řízení projektu a účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="e008e-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="e008e-116">Vyberte kartu **Mezipodnikové**.</span><span class="sxs-lookup"><span data-stu-id="e008e-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="e008e-117">Přesuňte posuvník na **Ano** pro povolení mezipodnikového plánování zdrojů a časových rozvrhů.</span><span class="sxs-lookup"><span data-stu-id="e008e-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="e008e-118">V seznamu označte vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="e008e-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="e008e-119">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="e008e-119">Select **New**.</span></span>
15. <span data-ttu-id="e008e-120">V poli **Půjčující si subjekt** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e008e-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="e008e-121">Zaškrtněte políčko **Poměrně rozložit zisk**.</span><span class="sxs-lookup"><span data-stu-id="e008e-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="e008e-122">V poli **Výchozí kategorie časového plánu** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e008e-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="e008e-123">V poli **Výchozí kategorie výdajů** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e008e-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="e008e-124">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e008e-124">Select **Save**.</span></span>
20. <span data-ttu-id="e008e-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e008e-125">Close the page.</span></span>
21. <span data-ttu-id="e008e-126">V navigačním podokně přejděte na **Moduly> Řízení projektů a účetnictví> Nastavení > Zaúčtování > Nastavení zaúčtování v hlavní knize**.</span><span class="sxs-lookup"><span data-stu-id="e008e-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="e008e-127">V poli **Typy účtů hlavní knihy** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="e008e-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="e008e-128">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="e008e-128">Select **New**.</span></span>
24. <span data-ttu-id="e008e-129">V poli **Hlavní účet** nového řádku zadejte požadované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="e008e-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="e008e-130">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e008e-130">Select **Save**.</span></span>
26. <span data-ttu-id="e008e-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e008e-131">Close the page.</span></span>
27. <span data-ttu-id="e008e-132">V navigačním podokně přejděte na **Moduly> Řízení projektů a účetnictví> Nastavení> Ceny> Cena za převod**.</span><span class="sxs-lookup"><span data-stu-id="e008e-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="e008e-133">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="e008e-133">Select **New**.</span></span>
29. <span data-ttu-id="e008e-134">Do pole **Datum účinnosti** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="e008e-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="e008e-135">V poli **Půjčující si subjekt** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e008e-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="e008e-136">V poli **Převést cenový model** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="e008e-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="e008e-137">Do pole **Ceny** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="e008e-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="e008e-138">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e008e-138">Select **Save**.</span></span>

