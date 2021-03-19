---
title: Navigace v uživatelském rozhraní
description: Toto téma poskytuje informace o správě projektů v Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 02dda534dcab4e8fee0a96a7e09759c32a669be5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286735"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="bd316-103">Navigace v uživatelském rozhraní</span><span class="sxs-lookup"><span data-stu-id="bd316-103">Navigating the user interface</span></span>

<span data-ttu-id="bd316-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="bd316-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="bd316-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="bd316-105">Overview</span></span>

<span data-ttu-id="bd316-106">Hlavní formulář projektu je rozdělen do několika karet.</span><span class="sxs-lookup"><span data-stu-id="bd316-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="bd316-107">Každá karta představuje jinou úroveň podrobností v rámci projektu.</span><span class="sxs-lookup"><span data-stu-id="bd316-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="bd316-108">**Souhrn** : Poskytuje popis projektu a agreguje plánovaný i skutečný výkon projektu.</span><span class="sxs-lookup"><span data-stu-id="bd316-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Karta Souhrn a pole](media/navigation7.png)

- <span data-ttu-id="bd316-110">**Úkoly** : Poskytuje podrobnosti týkající se strukturovaného rozpisu prací vyjádřeného jako zobrazení mřížky, plánovací vývěska nebo Ganttův diagram.</span><span class="sxs-lookup"><span data-stu-id="bd316-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Karta Úkol a pole](media/navigation8.png)

- <span data-ttu-id="bd316-112">**Tým** : Poskytuje podrobnosti o účastnících projektu.</span><span class="sxs-lookup"><span data-stu-id="bd316-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="bd316-113">V tomto zobrazení je také shrnuto přidělené úsilí každého člena týmu.</span><span class="sxs-lookup"><span data-stu-id="bd316-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Karta Tým a pole](media/navigation9.png)

- <span data-ttu-id="bd316-115">**Přiřazení zdrojů** : Poskytuje časově odstupňovaný pohled na úsilí každého zdroje v projektu.</span><span class="sxs-lookup"><span data-stu-id="bd316-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Karta Přiřazení zdrojů a pole](media/navigation10.png)

- <span data-ttu-id="bd316-117">**Vyrovnání zdrojů**: Poskytuje časově odstupňovaný pohled na rozdíly mezi přiřazením každého pojmenovaného zdroje a jejich rezervacemi.</span><span class="sxs-lookup"><span data-stu-id="bd316-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Karta Vyrovnání zdrojů a pole](media/navigation11.png)

- <span data-ttu-id="bd316-119">**Odhady** : Poskytuje časově odstupňovaný pohled na odhady nákladů a prodejů projektu.</span><span class="sxs-lookup"><span data-stu-id="bd316-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Karta Odhady a pole](media/navigation12.png)

- <span data-ttu-id="bd316-121">**Sledování** : Poskytuje pohled zobrazující průběh úkolů ve strukturovaném rozpisu prací pro úsilí, náklady a prodej.</span><span class="sxs-lookup"><span data-stu-id="bd316-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Karta Sledování a pole](media/navigation13.png)

- <span data-ttu-id="bd316-123">**Prodej** : Poskytuje přímé odkazy na nabídky a smlouvy přidružené k projektu.</span><span class="sxs-lookup"><span data-stu-id="bd316-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="bd316-124">**Odhady výdajů** : Poskytuje mřížku definující výdaje projektu na základě kategorií výdajů organizace.</span><span class="sxs-lookup"><span data-stu-id="bd316-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Karta Odhady výdajů a pole](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="bd316-126">Ovládací prvky mřížky</span><span class="sxs-lookup"><span data-stu-id="bd316-126">Grid controls</span></span>

<span data-ttu-id="bd316-127">Následuje stručný přehled typických ovládacích prvků na různých kartách plánování projektu.</span><span class="sxs-lookup"><span data-stu-id="bd316-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="bd316-128">Obnovit</span><span class="sxs-lookup"><span data-stu-id="bd316-128">Refresh</span></span>

<span data-ttu-id="bd316-129">**Obnovit** : Načte nejnovější data ze serveru, pokud po načtení mřížky došlo k jakýmkoli změnám.</span><span class="sxs-lookup"><span data-stu-id="bd316-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Tlačítko Aktualizovat](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="bd316-131">Seskupit podle</span><span class="sxs-lookup"><span data-stu-id="bd316-131">Group by</span></span>

<span data-ttu-id="bd316-132">**Seskupit podle** : Aktualizuje seskupení řádků v mřížce tak, aby odrážely buď zdroje, role nebo kategorie na základě potřeb uživatele.</span><span class="sxs-lookup"><span data-stu-id="bd316-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Tlačítko Seskupit podle](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="bd316-134">Předchozí/Další</span><span class="sxs-lookup"><span data-stu-id="bd316-134">Previous/Next</span></span>

<span data-ttu-id="bd316-135">**Předchozí**/**Další** : Aktualizujte viditelná časová období na časově rozložených mřížkách.</span><span class="sxs-lookup"><span data-stu-id="bd316-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Tlačítka Předchozí a Další](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="bd316-137">Časové měřítko</span><span class="sxs-lookup"><span data-stu-id="bd316-137">Timescale</span></span>

<span data-ttu-id="bd316-138">**Časové měřítko** : Změní agregaci časově rozložených dat mezi dny, týdny, měsíci a roky.</span><span class="sxs-lookup"><span data-stu-id="bd316-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Tlačítko Časové měřítko](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="bd316-140">Rozšířit</span><span class="sxs-lookup"><span data-stu-id="bd316-140">Expand</span></span>

<span data-ttu-id="bd316-141">**Rozšířit** : Vykreslí viditelnou mřížku na celou obrazovku a nabídne tak zobrazení dalších rolí.</span><span class="sxs-lookup"><span data-stu-id="bd316-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Tlačítko Rozbalit](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="bd316-143">Časově uspořádat podle</span><span class="sxs-lookup"><span data-stu-id="bd316-143">Time-phase by</span></span>

<span data-ttu-id="bd316-144">**Časově uspořádat podle** : Aktualizujte seskupení řádků v mřížce tak, aby odráželo odhady nákladů pro odhady prodejů.</span><span class="sxs-lookup"><span data-stu-id="bd316-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="bd316-145">Tento ovládací prvek se vztahuje také na skript odhadu a sledovací mřížku.</span><span class="sxs-lookup"><span data-stu-id="bd316-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Tlačítko Časově uspořádat podle](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="bd316-147">Přidat sloupec</span><span class="sxs-lookup"><span data-stu-id="bd316-147">Add column</span></span>

<span data-ttu-id="bd316-148">**Přidat sloupec** : Umožňuje uživateli definovat viditelné sloupce v mřížce.</span><span class="sxs-lookup"><span data-stu-id="bd316-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="bd316-149">Do mřížek ve formuláři **Plánování projektu** lze přidat pouze předem připravené sloupce.</span><span class="sxs-lookup"><span data-stu-id="bd316-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Tlačítko Přidat sloupec](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]