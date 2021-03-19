---
title: Nastavení kategorií výdajů
description: Toto téma poskytuje informace o tom, jak nastavit kategorie výdajů a sdílené kategorie pro sestavy výdajů.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1589cf82626e744d35f31fef8e8437a5ad71360d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276115"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="bd9a6-103">Nastavení kategorií výdajů</span><span class="sxs-lookup"><span data-stu-id="bd9a6-103">Set up expense categories</span></span>

<span data-ttu-id="bd9a6-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="bd9a6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="bd9a6-105">Když zaměstnanci vytvářejí sestavy výdajů, musí být každý zaznamenaný výdaj přidružen ke kategorii výdajů.</span><span class="sxs-lookup"><span data-stu-id="bd9a6-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="bd9a6-106">Kategorie výdajů jsou odvozeny ze sdílených kategorií, které lze sdílet mezi právnickými osobami ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="bd9a6-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="bd9a6-107">V závislosti na tom, jak je vaše organizace definována, lze tyto kategorie výdajů sdílet také v jiných oblastech.</span><span class="sxs-lookup"><span data-stu-id="bd9a6-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="bd9a6-108">Na základě definice vaší organizace a pokynů od implementačního týmu musíte určit, zda kategorie, které se používají ve správě výdajů, budou použity pouze ve správě výdajů, nebo zda by měly být sdíleny v jiných oblastech.</span><span class="sxs-lookup"><span data-stu-id="bd9a6-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="bd9a6-109">Tyto kategorie lze sdílet mezi moduly Řízení a účetnictví projektů a Správa výdajů, nebo mezi moduly Řízení a účetnictví projektů a Výroba.</span><span class="sxs-lookup"><span data-stu-id="bd9a6-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="bd9a6-110">Nelze je však sdílet mezi moduly Správa výdajů a Výroba.</span><span class="sxs-lookup"><span data-stu-id="bd9a6-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="bd9a6-111">Než budete moci zahájit proces instalace, je třeba učinit následující rozhodnutí pro každou kategorii výdajů:</span><span class="sxs-lookup"><span data-stu-id="bd9a6-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="bd9a6-112">Jaká je kategorie výdajů?</span><span class="sxs-lookup"><span data-stu-id="bd9a6-112">What is the expense category?</span></span> <span data-ttu-id="bd9a6-113">Mezi příklady patří kategorie letů, hotelů nebo najetých kilometrů.</span><span class="sxs-lookup"><span data-stu-id="bd9a6-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="bd9a6-114">Lze kategorii výdajů použít také v modulu Řízení a účetnictví projektů?</span><span class="sxs-lookup"><span data-stu-id="bd9a6-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="bd9a6-115">Když to jde, musíte rovněž učinit následující rozhodnutí:</span><span class="sxs-lookup"><span data-stu-id="bd9a6-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="bd9a6-116">Které nákladové účty budou použity pro následující výdaje?</span><span class="sxs-lookup"><span data-stu-id="bd9a6-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="bd9a6-117">Náklady</span><span class="sxs-lookup"><span data-stu-id="bd9a6-117">Cost</span></span>
        - <span data-ttu-id="bd9a6-118">Přidělení mezd</span><span class="sxs-lookup"><span data-stu-id="bd9a6-118">Payroll allocation</span></span>
        - <span data-ttu-id="bd9a6-119">Hodnota nákladů nedokončené práce</span><span class="sxs-lookup"><span data-stu-id="bd9a6-119">WIP-cost value</span></span>
        - <span data-ttu-id="bd9a6-120">Náklady – položka</span><span class="sxs-lookup"><span data-stu-id="bd9a6-120">Cost-item</span></span>
        - <span data-ttu-id="bd9a6-121">Nedokončená výroba – hodnota nákladů – položka</span><span class="sxs-lookup"><span data-stu-id="bd9a6-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="bd9a6-122">Časově rozlišená ztráta</span><span class="sxs-lookup"><span data-stu-id="bd9a6-122">Accrued loss</span></span>
        - <span data-ttu-id="bd9a6-123">NV – časově rozlišená ztráta</span><span class="sxs-lookup"><span data-stu-id="bd9a6-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="bd9a6-124">Které účty výnosů budou použity pro následující zdroje výnosů?</span><span class="sxs-lookup"><span data-stu-id="bd9a6-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="bd9a6-125">Fakturované výnosy</span><span class="sxs-lookup"><span data-stu-id="bd9a6-125">Invoiced revenue</span></span>
        - <span data-ttu-id="bd9a6-126">Časově rozlišené výnosy – hodnota prodeje</span><span class="sxs-lookup"><span data-stu-id="bd9a6-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="bd9a6-127">NV – prodej</span><span class="sxs-lookup"><span data-stu-id="bd9a6-127">WIP-sales value</span></span>
        - <span data-ttu-id="bd9a6-128">Časově rozlišené výnosy – výroba</span><span class="sxs-lookup"><span data-stu-id="bd9a6-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="bd9a6-129">NV – výroba</span><span class="sxs-lookup"><span data-stu-id="bd9a6-129">WIP-production</span></span>
        - <span data-ttu-id="bd9a6-130">Časově rozlišené výnosy – zisk</span><span class="sxs-lookup"><span data-stu-id="bd9a6-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="bd9a6-131">NV – zisk</span><span class="sxs-lookup"><span data-stu-id="bd9a6-131">WIP-profit</span></span>
        - <span data-ttu-id="bd9a6-132">Časově rozlišené výnosy – předplatné</span><span class="sxs-lookup"><span data-stu-id="bd9a6-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="bd9a6-133">NV – předplatné</span><span class="sxs-lookup"><span data-stu-id="bd9a6-133">WIP-subscription</span></span>

- <span data-ttu-id="bd9a6-134">Jaký je typ výdajů?</span><span class="sxs-lookup"><span data-stu-id="bd9a6-134">What is the expense type?</span></span>
- <span data-ttu-id="bd9a6-135">Jaký je výchozí způsob platby pro kategorii výdajů?</span><span class="sxs-lookup"><span data-stu-id="bd9a6-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="bd9a6-136">Musí být výdaje v kategorii výdajů rozepsány?</span><span class="sxs-lookup"><span data-stu-id="bd9a6-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="bd9a6-137">Jaký je hlavní výchozí účet pro kategorii výdajů?</span><span class="sxs-lookup"><span data-stu-id="bd9a6-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="bd9a6-138">Jaká je výchozí skupina daně z prodeje zboží pro kategorii výdajů?</span><span class="sxs-lookup"><span data-stu-id="bd9a6-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="bd9a6-139">Jsou pro kategorii výdajů povoleny další způsoby platby?</span><span class="sxs-lookup"><span data-stu-id="bd9a6-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="bd9a6-140">Pokud ano, které to jsou?</span><span class="sxs-lookup"><span data-stu-id="bd9a6-140">If so, what are they?</span></span>
- <span data-ttu-id="bd9a6-141">Existují v této kategorii výdajů podkategorie?</span><span class="sxs-lookup"><span data-stu-id="bd9a6-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="bd9a6-142">Když existují podkategorie, musíte rovněž učinit následující rozhodnutí:</span><span class="sxs-lookup"><span data-stu-id="bd9a6-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="bd9a6-143">Jsou některé z podkategorií vyloučeny z vymáhání daní?</span><span class="sxs-lookup"><span data-stu-id="bd9a6-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="bd9a6-144">Jaká je skupina daně z prodeje zboží u podkategorií?</span><span class="sxs-lookup"><span data-stu-id="bd9a6-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]