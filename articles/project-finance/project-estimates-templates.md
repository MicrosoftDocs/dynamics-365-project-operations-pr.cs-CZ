---
title: Synchronizace projektových odhadů přímo z Project Service Automation do Finance and Operations
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci odhadů projektových hodin a odhadů projektových výdajů přímo z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: KimANelson
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
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750323"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="152ae-103">Synchronizace projektových odhadů přímo z Project Service Automation do Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="152ae-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="152ae-104">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci odhadů projektových hodin a odhadů projektových výdajů přímo z Dynamics 365 Project Service Automation do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="152ae-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="152ae-105">Integrace projektových úkolů, kategorie transakcí výdajů, odhady hodin, odhady výdajů a zamykání funkcí je k dispozici ve verzi 8.0.</span><span class="sxs-lookup"><span data-stu-id="152ae-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="152ae-106">Integrace skutečných hodnot je k dispozici ve verzi 8.0.1 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="152ae-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="152ae-107">Datový tok pro Project Service Automation do Finance</span><span class="sxs-lookup"><span data-stu-id="152ae-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="152ae-108">Řešení integrace aplikací Project Service Automation do Finance využívá funkci integrace dat k synchronizaci dat napříč instancemi aplikací Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="152ae-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="152ae-109">Šablony integrace, které jsou k dispozici s funkcí Integrace dat, umožňují tok dat o odhadech projektových hodin a odhadech projektových výdajů z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="152ae-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="152ae-110">Následující obrázek ukazuje, jak jsou data synchronizována mezi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="152ae-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="152ae-111">[![Datový tok pro integraci Project Service Automation s Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="152ae-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="152ae-112">Odhady projektových hodin</span><span class="sxs-lookup"><span data-stu-id="152ae-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="152ae-113">Šablona a úkoly</span><span class="sxs-lookup"><span data-stu-id="152ae-113">Template and tasks</span></span>

<span data-ttu-id="152ae-114">Pro přístup k dostupným šablonám v centru pro správu Microsoft Power Apps vyberte **Projekty** a poté v pravém horním rohu vyberte **Nový projekt**, aby se vybraly veřejné šablony.</span><span class="sxs-lookup"><span data-stu-id="152ae-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="152ae-115">Následující šablona a základní úlohy se používají k synchronizaci odhadů projektových hodin z Project Service Automation do Finance:</span><span class="sxs-lookup"><span data-stu-id="152ae-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="152ae-116">**Název šablony v integraci dat** Odhady projektových hodin (PSA do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="152ae-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="152ae-117">**Název úloh v projektu:**</span><span class="sxs-lookup"><span data-stu-id="152ae-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="152ae-118">Vztahy transakcí</span><span class="sxs-lookup"><span data-stu-id="152ae-118">Transaction relationships</span></span>
    - <span data-ttu-id="152ae-119">Odhady výdajů</span><span class="sxs-lookup"><span data-stu-id="152ae-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="152ae-120">Sada entit</span><span class="sxs-lookup"><span data-stu-id="152ae-120">Entity set</span></span>

| <span data-ttu-id="152ae-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="152ae-121">Project Service Automation</span></span> | <span data-ttu-id="152ae-122">Finance</span><span class="sxs-lookup"><span data-stu-id="152ae-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="152ae-123">Projektové úkoly</span><span class="sxs-lookup"><span data-stu-id="152ae-123">Project tasks</span></span>              | <span data-ttu-id="152ae-124">Entita integrace pro odhady projektových hodin</span><span class="sxs-lookup"><span data-stu-id="152ae-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="152ae-125">Tok entity</span><span class="sxs-lookup"><span data-stu-id="152ae-125">Entity flow</span></span>

<span data-ttu-id="152ae-126">Odhady projektových hodin jsou spravovány v aplikaci Project Service Automation a jsou synchronizovány do Finance jako předpovědi projektových hodin.</span><span class="sxs-lookup"><span data-stu-id="152ae-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="152ae-127">Požadavky</span><span class="sxs-lookup"><span data-stu-id="152ae-127">Prerequisites</span></span>

<span data-ttu-id="152ae-128">Než může dojít k synchronizaci odhadů projektových hodin, musíte synchronizovat projekty, projektové úkoly a kategorie výdajových transakcí projektu.</span><span class="sxs-lookup"><span data-stu-id="152ae-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="152ae-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="152ae-129">Power Query</span></span>

<span data-ttu-id="152ae-130">V šabloně odhadů projektových hodin musíte použít Microsoft Power Query pro Excel k dokončení těchto úkolů:</span><span class="sxs-lookup"><span data-stu-id="152ae-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="152ae-131">Nastavte ID výchozího modelu předpovědi, který se použije, když integrace vytvoří nové předpovědi hodin.</span><span class="sxs-lookup"><span data-stu-id="152ae-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="152ae-132">Odfiltrujte všechny záznamy specifické pro daný zdroj v úkolu, které selžou při integraci do předpovědí hodin.</span><span class="sxs-lookup"><span data-stu-id="152ae-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="152ae-133">Odfiltrujte všechny prázdné řádky kategorie transakcí.</span><span class="sxs-lookup"><span data-stu-id="152ae-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="152ae-134">Pokud tento úkol nedokončíte, může to mít za následek nesprávné předpovědi hodin.</span><span class="sxs-lookup"><span data-stu-id="152ae-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="152ae-135">Nastavte ID výchozího modelu předpovědi</span><span class="sxs-lookup"><span data-stu-id="152ae-135">Set the default forecast model ID</span></span>

<span data-ttu-id="152ae-136">Chcete-li aktualizovat ID výchozího modelu předpovědi v šabloně, otevřete kliknutím na ikonu **Mapovat** mapování.</span><span class="sxs-lookup"><span data-stu-id="152ae-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="152ae-137">Poté vyberte odkaz **Pokročilý dotaz a filtrování**.</span><span class="sxs-lookup"><span data-stu-id="152ae-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="152ae-138">Pokud používáte výchozí šablonu odhadů projektových hodin (PSA do Fin a Ops), vyberte hodnotu **Vložená podmínka** v seznamu **Aplikované kroky**.</span><span class="sxs-lookup"><span data-stu-id="152ae-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="152ae-139">V poli **Funkce** nahraďte **O\_předpověď** za název ID modelu předpovědi, který by měl být použit s integrací.</span><span class="sxs-lookup"><span data-stu-id="152ae-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="152ae-140">Výchozí šablona obsahuje ID modelu předpovědi z ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="152ae-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="152ae-141">Pokud vytváříte novou šablonu, musíte přidat tento sloupec.</span><span class="sxs-lookup"><span data-stu-id="152ae-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="152ae-142">V Power Query vyberte **Přidat podmíněný sloupec** a zadejte název nového sloupce, například **Model_ID**.</span><span class="sxs-lookup"><span data-stu-id="152ae-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="152ae-143">Zadejte podmínku kde pro sloupec: Pokud projektový úkol není null, Pak \<zadejte ID modelu předpovědi\> ; Jinak null.</span><span class="sxs-lookup"><span data-stu-id="152ae-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="152ae-144">Odfiltrování záznamů specifických pro určitý zdroj</span><span class="sxs-lookup"><span data-stu-id="152ae-144">Filter out resource-specific records</span></span>

<span data-ttu-id="152ae-145">Šablona Odhady projektových hodin (PSA do Fin a Ops) má výchozí filtr, který odstraní všechny záznamy specifické pro nějaký prostředek.</span><span class="sxs-lookup"><span data-stu-id="152ae-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="152ae-146">Pokud vytvoříte vlastní šablonu, musíte přidat tento filtr.</span><span class="sxs-lookup"><span data-stu-id="152ae-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="152ae-147">Vyberte odkaz **Pokročilý dotaz a filtrování** a filtrujte sloupec **msdyn\_islinetask** tak, aby byly zahrnuty pouze **Nepravdivé** záznamy.</span><span class="sxs-lookup"><span data-stu-id="152ae-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="152ae-148">Odfiltrování všech prázdných řádků kategorie transakcí</span><span class="sxs-lookup"><span data-stu-id="152ae-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="152ae-149">Chcete-li odstranit všechny řádky, které mají prázdné kategorie transakcí, musíte přidat filtr.</span><span class="sxs-lookup"><span data-stu-id="152ae-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="152ae-150">Tato úloha je vyžadována bez ohledu na to, zda používáte výchozí šablonu nebo vytváříte vlastní šablonu.</span><span class="sxs-lookup"><span data-stu-id="152ae-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="152ae-151">Tento filtr odebere všechny souhrnné řádky z Project Service Automation, které by mohly způsobit nesprávné hodinové předpovědi ve Finance.</span><span class="sxs-lookup"><span data-stu-id="152ae-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="152ae-152">Vyberte odkaz **Pokročilý dotaz a filtrování** a odfiltrujte null záznamy ve sloupci **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="152ae-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="152ae-153">Mapování šablon v integraci dat</span><span class="sxs-lookup"><span data-stu-id="152ae-153">Template mapping in Data integration</span></span>

<span data-ttu-id="152ae-154">Následující obrázek ukazuje příklad mapování úlohy šablony v Integraci dat.</span><span class="sxs-lookup"><span data-stu-id="152ae-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="152ae-155">Mapování zobrazuje informace pole, které budou synchronizovány z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="152ae-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="152ae-156">[![Mapování šablon](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="152ae-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="152ae-157">Odhady projektových výdajů</span><span class="sxs-lookup"><span data-stu-id="152ae-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="152ae-158">Šablona a úkoly</span><span class="sxs-lookup"><span data-stu-id="152ae-158">Template and tasks</span></span>

<span data-ttu-id="152ae-159">Následující šablona a základní úlohy se používají k synchronizaci odhadů projektových výdajů z Project Service Automation do Finance:</span><span class="sxs-lookup"><span data-stu-id="152ae-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="152ae-160">**Název šablony v Integraci dat** Odhady projektových výdajů (PSA do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="152ae-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="152ae-161">**Název úloh v projektu:**</span><span class="sxs-lookup"><span data-stu-id="152ae-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="152ae-162">Vztahy transakcí</span><span class="sxs-lookup"><span data-stu-id="152ae-162">Transaction relationships</span></span> 
    - <span data-ttu-id="152ae-163">Odhady výdajů</span><span class="sxs-lookup"><span data-stu-id="152ae-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="152ae-164">Sada entit</span><span class="sxs-lookup"><span data-stu-id="152ae-164">Entity set</span></span>

| <span data-ttu-id="152ae-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="152ae-165">Project Service Automation</span></span> | <span data-ttu-id="152ae-166">Finance</span><span class="sxs-lookup"><span data-stu-id="152ae-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="152ae-167">Propojení transakcí</span><span class="sxs-lookup"><span data-stu-id="152ae-167">Transaction Connections</span></span>    | <span data-ttu-id="152ae-168">Entita integrace pro vztahy projektových transakcí</span><span class="sxs-lookup"><span data-stu-id="152ae-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="152ae-169">Řádky odhadu</span><span class="sxs-lookup"><span data-stu-id="152ae-169">Estimate Lines</span></span>             | <span data-ttu-id="152ae-170">Entita integrace pro odhady projektových výdajů</span><span class="sxs-lookup"><span data-stu-id="152ae-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="152ae-171">Tok entity</span><span class="sxs-lookup"><span data-stu-id="152ae-171">Entity flow</span></span>

<span data-ttu-id="152ae-172">Odhady projektových výdajů jsou spravovány v aplikaci Project Service Automation a jsou synchronizovány do Finance jako předpovědi projektových výdajů.</span><span class="sxs-lookup"><span data-stu-id="152ae-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="152ae-173">Požadavky</span><span class="sxs-lookup"><span data-stu-id="152ae-173">Prerequisites</span></span>

<span data-ttu-id="152ae-174">Než může dojít k synchronizaci odhadů projektových výdajů, musíte synchronizovat projekty, projektové úkoly a kategorie výdajových transakcí projektu.</span><span class="sxs-lookup"><span data-stu-id="152ae-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="152ae-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="152ae-175">Power Query</span></span>

<span data-ttu-id="152ae-176">V šabloně odhadů projektových výdajů musíte použít Microsoft Power Query pro Excel k dokončení následujících úkolů:</span><span class="sxs-lookup"><span data-stu-id="152ae-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="152ae-177">Filtr, který zahrne pouze záznamy řádků odhadu výdajů.</span><span class="sxs-lookup"><span data-stu-id="152ae-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="152ae-178">Nastavte ID výchozího modelu předpovědi, který se použije, když integrace vytvoří nové předpovědi hodin.</span><span class="sxs-lookup"><span data-stu-id="152ae-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="152ae-179">Transformujte typy fakturace.</span><span class="sxs-lookup"><span data-stu-id="152ae-179">Transform the billing types.</span></span>
- <span data-ttu-id="152ae-180">Transformujte typy transakcí.</span><span class="sxs-lookup"><span data-stu-id="152ae-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="152ae-181">Filtr, který zahrne pouze řádky odhadu výdajů.</span><span class="sxs-lookup"><span data-stu-id="152ae-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="152ae-182">Šablona Odhady projektových výdajů (PSA do Fin a Ops) má výchozí filtr, který do integrace zahrne pouze řádky výdajů.</span><span class="sxs-lookup"><span data-stu-id="152ae-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="152ae-183">Pokud vytvoříte vlastní šablonu, musíte přidat tento filtr.</span><span class="sxs-lookup"><span data-stu-id="152ae-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="152ae-184">Vyberte úlohu **Vztahy transakcí** a poté kliknutím na šipku **Mapovat** otevřete mapování.</span><span class="sxs-lookup"><span data-stu-id="152ae-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="152ae-185">Vyberte odkaz **Pokročilý dotaz a filtrování**.</span><span class="sxs-lookup"><span data-stu-id="152ae-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="152ae-186">Filtrujte sloupec **msdyn\_transactiontype1** tak, aby obsahoval pouze hodnoty **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="152ae-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="152ae-187">Nastavte ID výchozího modelu předpovědi</span><span class="sxs-lookup"><span data-stu-id="152ae-187">Set the default forecast model ID</span></span>

<span data-ttu-id="152ae-188">Chcete-li aktualizovat ID výchozího modelu předpovědi v šabloně, vyberte úlohu **Odhady výdajů** a poté otevřete kliknutím na ikonu **Mapovat** mapování.</span><span class="sxs-lookup"><span data-stu-id="152ae-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="152ae-189">Vyberte odkaz **Pokročilý dotaz a filtrování**.</span><span class="sxs-lookup"><span data-stu-id="152ae-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="152ae-190">Pokud používáte výchozí šablonu odhadů projektových výdajů (PSA do Fin a Ops), vyberte v Power Query nejprve hodnotu **Vložená podmínka** v seznamu **Aplikované kroky**.</span><span class="sxs-lookup"><span data-stu-id="152ae-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="152ae-191">V poli **Funkce** nahraďte **O\_předpověď** za název ID modelu předpovědi, který by měl být použit s integrací.</span><span class="sxs-lookup"><span data-stu-id="152ae-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="152ae-192">Výchozí šablona obsahuje ID modelu předpovědi z ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="152ae-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="152ae-193">Pokud vytváříte novou šablonu, musíte přidat tento sloupec.</span><span class="sxs-lookup"><span data-stu-id="152ae-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="152ae-194">V Power Query vyberte **Přidat podmíněný sloupec** a zadejte název nového sloupce, například **Model_ID**.</span><span class="sxs-lookup"><span data-stu-id="152ae-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="152ae-195">Zadejte podmínku kde pro sloupec: Pokud ID řádku odhadu není null, Pak \<zadejte ID modelu předpovědi\> ; Jinak null.</span><span class="sxs-lookup"><span data-stu-id="152ae-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="152ae-196">Transformace typů fakturace</span><span class="sxs-lookup"><span data-stu-id="152ae-196">Transform the billing types</span></span>

<span data-ttu-id="152ae-197">Šablona Odhady projektových výdajů (PSA do Fin a Ops) obsahuje podmíněný sloupec, který se používá k transformaci typů fakturace, které jsou přijímány z Project Service Automation během integrace.</span><span class="sxs-lookup"><span data-stu-id="152ae-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="152ae-198">Pokud vytvoříte vlastní šablonu, musíte přidat tento podmíněný sloupec.</span><span class="sxs-lookup"><span data-stu-id="152ae-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="152ae-199">Vyberte odkaz **Pokročilý dotaz a filtrování** a poté vyberte možnost **Přidat podmíněný sloupec**.</span><span class="sxs-lookup"><span data-stu-id="152ae-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="152ae-200">Zadejte název nového sloupce, například **TypFakturace**.</span><span class="sxs-lookup"><span data-stu-id="152ae-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="152ae-201">Poté zadejte následující podmínku:</span><span class="sxs-lookup"><span data-stu-id="152ae-201">Then enter the following condition:</span></span>

<span data-ttu-id="152ae-202">Když **msdyn\_billingtype** = 192350000, Pak **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="152ae-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="152ae-203">Jinak Když **msdyn\_billingtype** = 192350001, Pak **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="152ae-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="152ae-204">Jinak Když **msdyn\_billingtype** = 192350002, Pak **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="152ae-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="152ae-205">Jinak **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="152ae-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="152ae-206">Transformace typů transakcí</span><span class="sxs-lookup"><span data-stu-id="152ae-206">Transform the transaction types</span></span>

<span data-ttu-id="152ae-207">Šablona Odhady projektových výdajů (PSA do Fin a Ops) obsahuje podmíněný sloupec, který se používá k transformaci typů transakcí, které jsou přijímány z Project Service Automation během integrace.</span><span class="sxs-lookup"><span data-stu-id="152ae-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="152ae-208">Pokud vytvoříte vlastní šablonu, musíte přidat tento podmíněný sloupec.</span><span class="sxs-lookup"><span data-stu-id="152ae-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="152ae-209">Vyberte odkaz **Pokročilý dotaz a filtrování** a poté vyberte možnost **Přidat podmíněný sloupec**.</span><span class="sxs-lookup"><span data-stu-id="152ae-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="152ae-210">Zadejte název nového sloupce, například **TypTransakce**.</span><span class="sxs-lookup"><span data-stu-id="152ae-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="152ae-211">Poté zadejte následující podmínku:</span><span class="sxs-lookup"><span data-stu-id="152ae-211">Then enter the following condition:</span></span>

<span data-ttu-id="152ae-212">Když **msdyn\_transactiontypecode** = 192350000, Pak **Cost**</span><span class="sxs-lookup"><span data-stu-id="152ae-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="152ae-213">Jinak Když **msdyn\_transactiontypecode** = 192350005, Pak **Sales**</span><span class="sxs-lookup"><span data-stu-id="152ae-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="152ae-214">Jinak **null**</span><span class="sxs-lookup"><span data-stu-id="152ae-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="152ae-215">Mapování šablon v integraci dat</span><span class="sxs-lookup"><span data-stu-id="152ae-215">Template mapping in Data integration</span></span>

<span data-ttu-id="152ae-216">Následující obrázky ukazují příklady mapování úlohy šablony v Integraci dat.</span><span class="sxs-lookup"><span data-stu-id="152ae-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="152ae-217">Mapování zobrazuje informace pole, které budou synchronizovány z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="152ae-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="152ae-218">[![Mapování šablon](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="152ae-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="152ae-219">[![Mapování šablon](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="152ae-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
