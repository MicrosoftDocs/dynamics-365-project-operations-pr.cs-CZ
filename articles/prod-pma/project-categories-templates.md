---
title: Synchronizace kategorií výdajů projektu mezi aplikacemi Finance and Operations a Project Service Automation
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci kategorií výdajů projektu mezi aplikacemi Microsoft Dynamics 365 Finance a Dynamics 365 Project Service Automation.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073919"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="dfe6c-103">Synchronizace kategorií výdajů projektu mezi aplikacemi Finance and Operations a Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dfe6c-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dfe6c-104">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci kategorií výdajů projektu mezi aplikacemi Dynamics 365 Finance a Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="dfe6c-105">Integrace projektových úkolů, kategorie transakcí výdajů, odhady hodin, odhady výdajů a zamykání funkcí jsou k dispozici ve verzi 8.0.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="dfe6c-106">Integrace skutečných hodnot je k dispozici ve verzi 8.0.1 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="dfe6c-107">Pokud používáte Enterprise Edition 7.3.0, po instalaci aktualizací KB 4132657 a KB 4132660 budete moci pomocí šablon integrovat projektové úkoly, kategorie transakcí výdajů, odhady hodin, odhady výdajů a skutečné hodnoty, a také konfigurovat blokování funkcí.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="dfe6c-108">Pokud musíte resetovat rozúčtování, doporučujeme vám také nainstalovat KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="dfe6c-109">Datový tok pro aplikace Project Service Automation a Finance</span><span class="sxs-lookup"><span data-stu-id="dfe6c-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="dfe6c-110">Řešení integrace aplikací Project Service Automation a Finance využívá funkci integrace dat k synchronizaci dat napříč instancemi aplikací Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="dfe6c-111">Šablony integrace, které jsou k dispozici s funkcí Integrace dat, umožňují tok dat o kategoriích transakcí výdajů projektu mezi aplikacemi Finance a Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="dfe6c-112">Pokud jsou kategorie výdajů na projekt řízeny v aplikaci Finance, jde integrační tok nejprve z aplikace Finance do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="dfe6c-113">Identifikátory integrace kategorií výdajů na projekt se poté aktualizují prostřednictvím synchronizace z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="dfe6c-114">Pokud jsou kategorie výdajů na projekt řízeny v aplikaci Project Service Automation, jde integrační tok nejprve z aplikace Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="dfe6c-115">Před synchronizací z Project Service Automation musí být kategorie projektů již konfigurovány v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="dfe6c-116">Poté proveďte synchronizaci z Finance zpět do Project Service Automation a následně znovu z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="dfe6c-117">Tímto způsobem zaručíte propojení kategorií a zabráníte vzniku duplikátů.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="dfe6c-118">Obvykle jsou kategorie výdajů na projekty řízeny v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="dfe6c-119">Pokud však nejsou, nebo pokud již byly v Project Service Automation vytvořeny kategorie výdajů, musíte nejprve synchronizovat pomocí šablony Kategorie transakcí výdajů projektu (PSA do Fin a Ops).</span><span class="sxs-lookup"><span data-stu-id="dfe6c-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="dfe6c-120">Potom proveďte synchronizaci pomocí šablony Kategorie transakcí výdajů projektu (Fin a Ops do PSA).</span><span class="sxs-lookup"><span data-stu-id="dfe6c-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="dfe6c-121">Potom byste měli synchronizaci z Project Service Automation do Finance spustit ještě jednou.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="dfe6c-122">Pokud synchronizujete nejprve z Project Service Automation, musí být před spuštěním synchronizace v aplikaci Finance splněny následující požadavky:</span><span class="sxs-lookup"><span data-stu-id="dfe6c-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="dfe6c-123">Sdílená kategorie, která odpovídá kategorii projektu nastavené v Project Service Automation, musí existovat a musí být povolena pro možnosti **Projekt** a **Výdaje**.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="dfe6c-124">Pro každý právní subjekt Finance, který musí být integrován, musí existovat následující kategorie projektu:</span><span class="sxs-lookup"><span data-stu-id="dfe6c-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="dfe6c-125">**Kategorie projektu** existuje.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="dfe6c-126">**Použít ve výdajích** je povoleno.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="dfe6c-127">**Aktivní v deníku** je povoleno.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="dfe6c-128">**Typ transakce** je nastaven na **Výdaje**.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="dfe6c-129">Následující obrázek ukazuje, jak jsou data synchronizována mezi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="dfe6c-130">[![Datový tok pro integraci Project Service Automation s Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="dfe6c-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="dfe6c-131">Synchronizace kategorií výdajů projektu z Finance do Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dfe6c-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="dfe6c-132">Šablona a úkol</span><span class="sxs-lookup"><span data-stu-id="dfe6c-132">Template and task</span></span>

<span data-ttu-id="dfe6c-133">Pro přístup k šabloně v centru pro správu Microsoft Power Apps vyberte **Projekty** a poté v pravém horním rohu vyberte **Nový projekt** , aby se vybraly veřejné šablony.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-133">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="dfe6c-134">Následující šablona a základní úloha se používají k synchronizaci kategorií výdajů projektu z Finance do Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="dfe6c-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="dfe6c-135">**Název šablony v integraci dat** Kategorie transakcí výdajů na projekt (Fin and Ops do PSA)</span><span class="sxs-lookup"><span data-stu-id="dfe6c-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="dfe6c-136">**Název úkolu v projektu:** Synchronizace kategorií do PSA</span><span class="sxs-lookup"><span data-stu-id="dfe6c-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="dfe6c-137">Sada entit</span><span class="sxs-lookup"><span data-stu-id="dfe6c-137">Entity set</span></span>

| <span data-ttu-id="dfe6c-138">Finance</span><span class="sxs-lookup"><span data-stu-id="dfe6c-138">Finance</span></span>                           | <span data-ttu-id="dfe6c-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dfe6c-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="dfe6c-140">Integrační entita pro kategorie</span><span class="sxs-lookup"><span data-stu-id="dfe6c-140">Integration entity for categories</span></span> | <span data-ttu-id="dfe6c-141">Kategorie transakcí</span><span class="sxs-lookup"><span data-stu-id="dfe6c-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="dfe6c-142">Tok entity</span><span class="sxs-lookup"><span data-stu-id="dfe6c-142">Entity flow</span></span>

<span data-ttu-id="dfe6c-143">Kategorie výdajů na projekt jsou spravovány ve Finance a jsou synchronizovány do Project Service Automation jako kategorie transakcí.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="dfe6c-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="dfe6c-144">Power Query</span></span>

<span data-ttu-id="dfe6c-145">Když provádíte synchronizaci do Project Service Automation, musíte použít Microsoft Power Query pro Excel k nastavení typu fakturace v kategorii transakcí.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="dfe6c-146">Šablona kategorií transakcí výdajů projektu (Fin a Ops do PSA) poskytuje výchozí sloupec a mapování.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="dfe6c-147">Pokud vytvoříte vlastní šablonu, musíte přidat podmíněný sloupec v Power Query.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="dfe6c-148">Postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-148">Follow these steps.</span></span>

1. <span data-ttu-id="dfe6c-149">Kliknutím na šipku otevřete mapování úkolu kategorie výdajů projektu v šabloně Kategorie transakcí výdajů projektu (Fin a Ops do PSA).</span><span class="sxs-lookup"><span data-stu-id="dfe6c-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="dfe6c-150">Kliknutím na ikonu **Pokročilý dotaz a filtrování** otevřete Power Query.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="dfe6c-151">Vyberte **Přidat podmíněný sloupec**.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="dfe6c-152">Zadejte název nového sloupce, například **TypFakturace**.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="dfe6c-153">Zadejte následující podmínku: **Pokud CATEGORYID není rovno null, Pak 19235001, Jinak null**.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="dfe6c-154">Klikněte na možnost **OK** na sloupci.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="dfe6c-155">Nezapomeňte namapovat tento nový sloupec na stránce mapování.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="dfe6c-156">Následující obrázek ukazuje příklad mapování úlohy šablony v Integraci dat.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="dfe6c-157">Mapování zobrazuje informace pole, které budou synchronizovány z Finance do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="dfe6c-158">[![Mapování šablon kategorií výdajů projektu na šablony Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="dfe6c-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="dfe6c-159">Synchronizace kategorií výdajů projektu z Project Service Automation do Finance</span><span class="sxs-lookup"><span data-stu-id="dfe6c-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="dfe6c-160">Šablona a úkol</span><span class="sxs-lookup"><span data-stu-id="dfe6c-160">Template and task</span></span>

<span data-ttu-id="dfe6c-161">Následující šablona a základní úloha se používají k synchronizaci kategorií výdajů projektu z Project Service Automation do Finance:</span><span class="sxs-lookup"><span data-stu-id="dfe6c-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="dfe6c-162">**Název šablony v integraci dat** Kategorie transakcí výdajů na projekt (PSA do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="dfe6c-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="dfe6c-163">**Název úkolu v projektu:** Synchronizace kategorií do Fin Ops</span><span class="sxs-lookup"><span data-stu-id="dfe6c-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="dfe6c-164">Sada entit</span><span class="sxs-lookup"><span data-stu-id="dfe6c-164">Entity set</span></span>

| <span data-ttu-id="dfe6c-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dfe6c-165">Project Service Automation</span></span> | <span data-ttu-id="dfe6c-166">Finance</span><span class="sxs-lookup"><span data-stu-id="dfe6c-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="dfe6c-167">Kategorie transakcí</span><span class="sxs-lookup"><span data-stu-id="dfe6c-167">Transaction categories</span></span>     | <span data-ttu-id="dfe6c-168">Integrační entita pro kategorie</span><span class="sxs-lookup"><span data-stu-id="dfe6c-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="dfe6c-169">Tok entity</span><span class="sxs-lookup"><span data-stu-id="dfe6c-169">Entity flow</span></span>

<span data-ttu-id="dfe6c-170">Kategorie výdajů na projekt jsou spravovány ve Finance a jsou synchronizovány do Project Service Automation jako kategorie transakcí.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="dfe6c-171">Synchronizace zpět do Finance aktualizuje kategorii projektu ve Finance s ID integrace z Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="dfe6c-172">Mapování šablon v integraci dat</span><span class="sxs-lookup"><span data-stu-id="dfe6c-172">Template mapping in Data integration</span></span>

<span data-ttu-id="dfe6c-173">Následující obrázek ukazuje příklad mapování úlohy šablony v Integraci dat.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="dfe6c-174">Mapování zobrazuje informace pole, které budou synchronizovány z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="dfe6c-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="dfe6c-175">[![Mapování šablon Project Service Automation na šablony Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="dfe6c-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
