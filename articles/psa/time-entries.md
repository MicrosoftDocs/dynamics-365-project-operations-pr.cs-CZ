---
title: Vytvoření časových záznamů
description: Toto téma obsahuje informace o způsobu vytvoření časových záznamů.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 878413a24baa340b745a045a6991a63a00851c8b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073871"
---
# <a name="create-time-entries"></a><span data-ttu-id="ce0d8-103">Vytvoření časových záznamů</span><span class="sxs-lookup"><span data-stu-id="ce0d8-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ce0d8-104">V předchozích verzích Dynamics 365 Project Service Automation byly časové záznamy zadány týdně.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="ce0d8-105">Ve verzi 3 Project Service Automation se časové záznamy zadávají denně.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="ce0d8-106">Po vytvoření několika časových záznamů však tyto položky můžete hromadně vytvořit nebo zkopírovat.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="ce0d8-107">Vytvoření časového záznamu</span><span class="sxs-lookup"><span data-stu-id="ce0d8-107">Create a time entry</span></span>

<span data-ttu-id="ce0d8-108">Chcete-li vytvořit časový záznam, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="ce0d8-109">Na stránce **Časové záznamy** vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="ce0d8-110">V dialogovém okně **Vytvořit: Časový záznam** zadejte dobu trvání časového záznamu v minutách, hodinách nebo dnech.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="ce0d8-111">Doba trvání musí být zadána v následujícím formátu: *x* minut, *x* hodin nebo *x* dnů.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="ce0d8-112">Hodiny a dny lze také zadávat jako desetinná čísla, například *x.x* hodin nebo *x.x* dnů.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="ce0d8-113">Vyberte typ časového záznamu a projekt, pro který tento časový záznam zadáváte.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="ce0d8-114">V poli **Projektový úkol** najděte úkol pro tento časový záznam.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ce0d8-115">Pokud vytváříte časový záznam pro úkol, který není přiřazen uživateli, vyberte v poli **Projektový úkol** tlačítko **Hledat** , vyberte **Změnit zobrazení** a pak vyberte **Všechny aktivní projektové úkoly** pro zobrazení seznamu všech úkolů.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View** , and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="ce0d8-116">Zadejte popis, pokud je vyžadován popis, a pak vyberte **Uložit a zavřít**.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="ce0d8-117">Jakmile je časový záznam vytvořen a uložen, můžete ho upravit v mřížce časového záznamu.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="ce0d8-118">Mřížka časového záznamu podporuje dva formáty:</span><span class="sxs-lookup"><span data-stu-id="ce0d8-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="ce0d8-119">Časové záznamy lze zadat ve formátu **hh: mm**.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="ce0d8-120">Tento formát je pak převeden na hodiny a zlomky.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="ce0d8-121">Hodiny a zlomky můžete zadat přímo.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="ce0d8-122">Všimněte si, že zlomky hodiny nejsou minuty.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="ce0d8-123">Proto 1,5 hodiny představuje 1 hodinu a 30 minut.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="ce0d8-124">Stejné pravidlo platí pro zlomky dne.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="ce0d8-125">Jeden den je 24 hodin a 0,5 dne představuje 12 hodin.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="ce0d8-126">Hromadné vytvoření časových záznamů</span><span class="sxs-lookup"><span data-stu-id="ce0d8-126">Bulk create time entries</span></span>

<span data-ttu-id="ce0d8-127">Po vytvoření několika časových záznamů je můžete pomocí funkce kopírování kopírovat za účelem hromadného vytvoření dalších záznamů.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="ce0d8-128">Na stránce **Časové záznamy** vyberte **Kopírovat týden**.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="ce0d8-129">Ve skupině polí **Od období** definujte v polích **Počáteční datum** a  **Koncové datum** rozsah dat, ze kterého se má zkopírovat časový záznam.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="ce0d8-130">Ve skupině polí **Do období** v poli **Počáteční datum** zadejte datum, pro které chcete vytvořit časové záznamy.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="ce0d8-131">Chcete-li vytvořit kopii časových záznamů, které odpovídají dnu v týdnu určenému ve skupině polí **Do období** , klikněte na **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="ce0d8-132">Například pondělní časový záznam z minulého týdne bude zkopírován do pondělí týdne, který je zadán ve skupině polí jako **Do období**.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="ce0d8-133">Importovat data pro časové záznamy</span><span class="sxs-lookup"><span data-stu-id="ce0d8-133">Import data for time entries</span></span>

<span data-ttu-id="ce0d8-134">Můžete importovat data z rezervací projektů a přiřazení.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="ce0d8-135">Při importu dat můžete určit rozsah kalendářních dat rezervací, které chcete importovat, a pak explicitně vybrat rezervace, které mají být vytvořeny jako **Koncept** časových záznamů.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="ce0d8-136">Funkce seskupit podle, třídit, hledat a filtrovat</span><span class="sxs-lookup"><span data-stu-id="ce0d8-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="ce0d8-137">Časové záznamy lze seskupit a filtrovat podle dimenzí zadaných ve sloupcích.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="ce0d8-138">V poli **Seskupit podle** vyberte dimenzi, kterou chcete použít k filtrování časových záznamů.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="ce0d8-139">Záznamy s položkami času lze také řadit vzestupně nebo sestupně pomocí šipky řazení v záhlavích sloupců.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="ce0d8-140">Tyto záznamy lze zobrazit nebo skrýt výběrem tlačítka **Filtrovat** v záhlavích sloupců a potom do políčka **Hledat** zadáním textu, který má být použit k hledání časových položek podle názvu projektu, úkolu projektu, času položku nebo zdroj.</span><span class="sxs-lookup"><span data-stu-id="ce0d8-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>