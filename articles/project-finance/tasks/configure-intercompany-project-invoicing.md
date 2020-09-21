---
title: Konfigurace fakturace mezipodnikového projektu
description: Tento téma ukazuje, jak nastavit fakturaci projektu mezi dvěma společnostmi ve vaší organizaci.
author: KimANelson
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
ms.assetid: 72d6c257-f2d3-483b-8ff2-445263796963
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b199c85736f6268bc5914fddaa10e4cabd44ef1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750293"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="af2f4-103">Konfigurace fakturace mezipodnikového projektu</span><span class="sxs-lookup"><span data-stu-id="af2f4-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af2f4-104">Tento téma ukazuje, jak nastavit fakturaci projektu mezi dvěma společnostmi ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="af2f4-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="af2f4-105">Tento úkol používá datovou sadu USSI.</span><span class="sxs-lookup"><span data-stu-id="af2f4-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="af2f4-106">V navigačním podokně přejděte na **Moduly > Závazky > Dodavatelé > Všichni dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="af2f4-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="af2f4-107">V seznamu **Všichni dodavatelé** vyhledejte a vyberte požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="af2f4-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="af2f4-108">V podokně akcí vyberte **Obecné**.</span><span class="sxs-lookup"><span data-stu-id="af2f4-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="af2f4-109">Vyberte **Mezipodnikové**.</span><span class="sxs-lookup"><span data-stu-id="af2f4-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="af2f4-110">Nastavte **Aktivní** na **Ano** k povolení vnitropodnikového obchodování.</span><span class="sxs-lookup"><span data-stu-id="af2f4-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="af2f4-111">V poli **Společnost zákazníka** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="af2f4-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="af2f4-112">V poli **Můj obchodní vztah** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="af2f4-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="af2f4-113">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="af2f4-113">Select **Save**.</span></span>
9. <span data-ttu-id="af2f4-114">Zavřete stránky a vraťte se na domovskou stránku.</span><span class="sxs-lookup"><span data-stu-id="af2f4-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="af2f4-115">V navigačním podokně přejděte na **Moduly> Řízení projektů a účetnictví> Nastavení > Ceny> Parametry řízení projektu a účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="af2f4-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="af2f4-116">Vyberte kartu **Mezipodnikové**.</span><span class="sxs-lookup"><span data-stu-id="af2f4-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="af2f4-117">Přesuňte posuvník na **Ano** pro povolení mezipodnikového plánování zdrojů a časových rozvrhů.</span><span class="sxs-lookup"><span data-stu-id="af2f4-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="af2f4-118">V seznamu označte vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="af2f4-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="af2f4-119">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="af2f4-119">Select **New**.</span></span>
15. <span data-ttu-id="af2f4-120">V poli **Půjčující si subjekt** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="af2f4-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="af2f4-121">Zaškrtněte políčko **Poměrně rozložit zisk**.</span><span class="sxs-lookup"><span data-stu-id="af2f4-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="af2f4-122">V poli **Výchozí kategorie časového plánu** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="af2f4-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="af2f4-123">V poli **Výchozí kategorie výdajů** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="af2f4-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="af2f4-124">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="af2f4-124">Select **Save**.</span></span>
20. <span data-ttu-id="af2f4-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="af2f4-125">Close the page.</span></span>
21. <span data-ttu-id="af2f4-126">V navigačním podokně přejděte na **Moduly> Řízení projektů a účetnictví> Nastavení > Zaúčtování > Nastavení zaúčtování v hlavní knize**.</span><span class="sxs-lookup"><span data-stu-id="af2f4-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="af2f4-127">V poli **Typy účtů hlavní knihy** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="af2f4-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="af2f4-128">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="af2f4-128">Select **New**.</span></span>
24. <span data-ttu-id="af2f4-129">V poli **Hlavní účet** nového řádku zadejte požadované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="af2f4-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="af2f4-130">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="af2f4-130">Select **Save**.</span></span>
26. <span data-ttu-id="af2f4-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="af2f4-131">Close the page.</span></span>
27. <span data-ttu-id="af2f4-132">V navigačním podokně přejděte na **Moduly> Řízení projektů a účetnictví> Nastavení> Ceny> Cena za převod**.</span><span class="sxs-lookup"><span data-stu-id="af2f4-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="af2f4-133">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="af2f4-133">Select **New**.</span></span>
29. <span data-ttu-id="af2f4-134">Do pole **Datum účinnosti** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="af2f4-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="af2f4-135">V poli **Půjčující si subjekt** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="af2f4-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="af2f4-136">V poli **Převést cenový model** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="af2f4-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="af2f4-137">Do pole **Ceny** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="af2f4-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="af2f4-138">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="af2f4-138">Select **Save**.</span></span>

