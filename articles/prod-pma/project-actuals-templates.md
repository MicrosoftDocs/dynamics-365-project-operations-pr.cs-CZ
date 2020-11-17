---
title: Synchronizace skutečných hodnot projektu přímo z Project Service Automation do deníku integrace projektu k zaúčtování ve Finance and Operations
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci skutečných hodnot projektu přímo z Microsoft Dynamics 365 Project Service Automation do Finance and Operations.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: cff62e739e88dc45e7c3d1ea044875f0600f2bc1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073912"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a><span data-ttu-id="cd91b-103">Synchronizace skutečných hodnot projektu přímo z Project Service Automation do deníku integrace projektu k zaúčtování ve Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cd91b-103">Synchronize project actuals directly from Project Service Automation to the project integration journal for posting in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cd91b-104">Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci skutečných hodnot projektu přímo z Dynamics 365 Project Service Automation do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-104">This topic describes the templates and underlying tasks that are used to synchronize project actuals directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

<span data-ttu-id="cd91b-105">Šablona synchronizuje transakce z Project Service Automation do pracovní tabulky v modulu Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-105">The template synchronizes transactions from Project Service Automation into a staging table in Finance.</span></span> <span data-ttu-id="cd91b-106">Po dokončení synchronizace **musíte** importovat data z pracovní tabulky do integračního deníku.</span><span class="sxs-lookup"><span data-stu-id="cd91b-106">After synchronization is completed, you **must** import the data from the staging table into the integration journal.</span></span>

> [!NOTE]
> - <span data-ttu-id="cd91b-107">Integrace skutečných hodnot je k dispozici od verze 8.0.1.</span><span class="sxs-lookup"><span data-stu-id="cd91b-107">Project actuals integration is available starting in version 8.0.1.</span></span>
> - <span data-ttu-id="cd91b-108">Pokud používáte Enterprise Edition 7.3.0, po instalaci aktualizací KB 4132657 a KB 4132660 budete moci pomocí šablon integrovat projektové úkoly, kategorie transakcí výdajů, odhady hodin, odhady výdajů a skutečné hodnoty, a také konfigurovat blokování funkcí.</span><span class="sxs-lookup"><span data-stu-id="cd91b-108">If you're using Enterprise edition 7.3.0 after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="cd91b-109">Pokud musíte resetovat rozúčtování, doporučujeme vám také nainstalovat KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="cd91b-109">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="cd91b-110">Pokud používáte verzi 7.3.0 a přenášíte transakce poplatků z Project Service Automation, musíte nainstalovat KB 4345320, abyste mohli zahrnout tyto poplatky do faktury projektu.</span><span class="sxs-lookup"><span data-stu-id="cd91b-110">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="cd91b-111">Pokud zadáváte částky daně z obratu v časových nebo výdajových transakcích v Project Service Automation, musíte nainstalovat aktualizaci Project Service Automation Update 7.</span><span class="sxs-lookup"><span data-stu-id="cd91b-111">If you're entering sales tax amounts on time or expense transactions in Project Service Automation, you must install Project Service Automation Update 7.</span></span> <span data-ttu-id="cd91b-112">V opačném případě nebudou skutečné hodnoty daně propojeny s přidruženými skutečnými časovými nebo výdajovými údaji a nebudou synchronizovány s modulem Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-112">Otherwise, the tax actuals won't be linked to the associated time or expense actuals, and they won't be synchronized to Finance.</span></span> <span data-ttu-id="cd91b-113">Další informace vám poskytne tým podpory.</span><span class="sxs-lookup"><span data-stu-id="cd91b-113">For more information, contact Support.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="cd91b-114">Datový tok pro Project Service Automation do Finance</span><span class="sxs-lookup"><span data-stu-id="cd91b-114">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="cd91b-115">Řešení integrace aplikací Project Service Automation do Finance využívá funkci integrace dat k synchronizaci dat napříč instancemi aplikací Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-115">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="cd91b-116">Šablony integrace, které jsou k dispozici s funkcí Integrace dat, umožňují tok dat o skutečných hodnotách projektu z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-116">The integration templates that are available with the Data integration feature enable the flow of data about project actuals from Project Service Automation to Finance.</span></span>

<span data-ttu-id="cd91b-117">Následující obrázek ukazuje, jak jsou data synchronizována mezi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-117">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="cd91b-118">[![Datový tok pro integraci Project Service Automation s Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)</span><span class="sxs-lookup"><span data-stu-id="cd91b-118">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)</span></span>

## <a name="project-actuals-from-project-service-automation"></a><span data-ttu-id="cd91b-119">Skutečné hodnoty projektu z Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cd91b-119">Project actuals from Project Service Automation</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="cd91b-120">Šablona a úkoly</span><span class="sxs-lookup"><span data-stu-id="cd91b-120">Template and tasks</span></span>

<span data-ttu-id="cd91b-121">Pro přístup k dostupným šablonám v centru pro správu Microsoft Power Apps vyberte **Projekty** a poté v pravém horním rohu vyberte **Nový projekt** , aby se vybraly veřejné šablony.</span><span class="sxs-lookup"><span data-stu-id="cd91b-121">To access the available templates, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="cd91b-122">Následující šablona a základní úlohy se používají k synchronizaci skutečných hodnot projektu z Project Service Automation do Finance:</span><span class="sxs-lookup"><span data-stu-id="cd91b-122">The following template and underlying tasks are used to synchronize project actuals from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="cd91b-123">**Název šablony v integraci dat** Skutečné hodnoty projektu (PSA do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="cd91b-123">**Name of the template in Data integration:** Project actuals (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="cd91b-124">**Název úloh v projektu:**</span><span class="sxs-lookup"><span data-stu-id="cd91b-124">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="cd91b-125">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="cd91b-125">Actuals</span></span>
    - <span data-ttu-id="cd91b-126">TransactionConnections</span><span class="sxs-lookup"><span data-stu-id="cd91b-126">TransactionConnections</span></span>

### <a name="entity-set"></a><span data-ttu-id="cd91b-127">Sada entit</span><span class="sxs-lookup"><span data-stu-id="cd91b-127">Entity set</span></span>

| <span data-ttu-id="cd91b-128">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cd91b-128">Project Service Automation</span></span> | <span data-ttu-id="cd91b-129">Finance</span><span class="sxs-lookup"><span data-stu-id="cd91b-129">Finance</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="cd91b-130">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="cd91b-130">Actuals</span></span>                    | <span data-ttu-id="cd91b-131">Entita integrace pro skutečné hodnoty projektu</span><span class="sxs-lookup"><span data-stu-id="cd91b-131">Integration entity for project actuals</span></span>                   |
| <span data-ttu-id="cd91b-132">Propojení transakcí</span><span class="sxs-lookup"><span data-stu-id="cd91b-132">Transaction Connections</span></span>    | <span data-ttu-id="cd91b-133">Entita integrace pro vztahy projektových transakcí</span><span class="sxs-lookup"><span data-stu-id="cd91b-133">Integration entity for project transaction relationships</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="cd91b-134">Tok entity</span><span class="sxs-lookup"><span data-stu-id="cd91b-134">Entity flow</span></span>

<span data-ttu-id="cd91b-135">Odhady skutečných hodnot projektu hodin jsou spravovány v aplikaci Project Service Automation a jsou synchronizovány s deníkem integrace projektu v modulu Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-135">Project actuals are managed in Project Service Automation, and they are synchronized to the project integration journal in Finance.</span></span> <span data-ttu-id="cd91b-136">Účetnictví bude použito na základě výchozích finančních dimenzí a nastavení účtování.</span><span class="sxs-lookup"><span data-stu-id="cd91b-136">The accounting will be applied based on default financial dimensions and the posting setup.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="cd91b-137">Požadavky</span><span class="sxs-lookup"><span data-stu-id="cd91b-137">Prerequisites</span></span>

<span data-ttu-id="cd91b-138">Než může dojít k synchronizaci skutečných hodnot, musíte nakonfigurovat parametry integrace Project Service Automation a synchronizovat projekty, úkoly projektu a kategorie výdajových transakcí projektu.</span><span class="sxs-lookup"><span data-stu-id="cd91b-138">Before synchronization of actuals can occur, you must configure the Project Service Automation integration parameters and synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="cd91b-139">Power Query</span><span class="sxs-lookup"><span data-stu-id="cd91b-139">Power Query</span></span>

<span data-ttu-id="cd91b-140">V šabloně skutečných hodnot projektu musíte použít Microsoft Power Query pro Excel k dokončení těchto úkolů:</span><span class="sxs-lookup"><span data-stu-id="cd91b-140">In the project actuals template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="cd91b-141">Transformujte typ transakce v Project Service Automation na správný typ transakce v Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-141">Transform the transaction type in Project Service Automation to the correct transaction type in Finance.</span></span> <span data-ttu-id="cd91b-142">Tato transformace je již definována v šabloně Skutečné hodnoty projektu (PSA do Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="cd91b-142">This transformation is already defined in the Project actuals (PSA to Fin and Ops) template.</span></span>
- <span data-ttu-id="cd91b-143">Transformujte typ fakturace v Project Service Automation na správný typ fakturace v Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-143">Transform the billing type in Project Service Automation to the correct billing type in Finance.</span></span> <span data-ttu-id="cd91b-144">Tato transformace je již definována v šabloně Skutečné hodnoty projektu (PSA do Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="cd91b-144">This transformation is already defined in the Project actuals (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="cd91b-145">Typ fakturace je poté namapován na vlastnost řádku na základě konfigurace na stránce **Parametry integrace Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-145">The billing type is then mapped to the line property, based on the configuration on the **Project Service Automation integration parameters** page.</span></span>
- <span data-ttu-id="cd91b-146">Filtrujte na konkrétní organizační jednotky prostředků, které je třeba synchronizovat s touto šablonou.</span><span class="sxs-lookup"><span data-stu-id="cd91b-146">Filter to specific resource organizational units that must be synchronized with this template.</span></span>
- <span data-ttu-id="cd91b-147">Pokud budou mezipodnikový čas nebo skutečné mezipodnikové výdaje synchronizovány s modulem Finance, musíte transformovat organizační jednotku smlouvy na správnou právnickou osobu v Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-147">If intercompany time or intercompany expense actuals will be synchronized to Finance, you must transform the contract organizational unit to the correct legal entity in Finance.</span></span> <span data-ttu-id="cd91b-148">V šabloně Skutečné hodnoty projektu (PSA do Fin and Ops) je definován podmíněný sloupec založený na ukázkových datech.</span><span class="sxs-lookup"><span data-stu-id="cd91b-148">In the Project actuals (PSA to Fin and Ops) template, a conditional column is defined based on demo data.</span></span> <span data-ttu-id="cd91b-149">Poslední vložený podmíněný sloupec musíte aktualizovat na správné právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="cd91b-149">You must update the last inserted conditional column to the correct legal entities.</span></span> <span data-ttu-id="cd91b-150">V opačném případě může dojít k chybě integrace nebo k importu nesprávných skutečných transakcí do Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-150">Otherwise, either an integration error might occur, or incorrect actual transactions might be imported into Finance.</span></span>
- <span data-ttu-id="cd91b-151">Pokud se mezipodnikový čas nebo skutečné mezipodnikové výdaje nesynchronizují s Finance, musíte odstranit poslední vložený podmíněný sloupec ze své šablony.</span><span class="sxs-lookup"><span data-stu-id="cd91b-151">If intercompany time or intercompany expense actuals won't be synchronized to Finance, you must delete the last inserted conditional column from your template.</span></span> <span data-ttu-id="cd91b-152">V opačném případě může dojít k chybě integrace nebo k importu nesprávných skutečných transakcí do Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-152">Otherwise, either an integration error might occur, or incorrect actual transactions might be imported into Finance.</span></span>

#### <a name="contract-organizational-unit"></a><span data-ttu-id="cd91b-153">Smluvní organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="cd91b-153">Contract organizational unit</span></span>
<span data-ttu-id="cd91b-154">Chcete-li aktualizovat vložený podmíněný sloupec v šabloně, otevřete kliknutím na ikonu **Mapovat** mapování.</span><span class="sxs-lookup"><span data-stu-id="cd91b-154">To update the inserted conditional column in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="cd91b-155">Kliknutím na odkaz **Pokročilý dotaz a filtrování** otevřete Power Query.</span><span class="sxs-lookup"><span data-stu-id="cd91b-155">Select the **Advanced Query and Filtering** link to open Power Query.</span></span>

- <span data-ttu-id="cd91b-156">Pokud používáte výchozí šablonu skutečných hodnot projektu (PSA do Fin and Ops), vyberte v Power Query podlední hodnotu **Vložená podmínka** v seznamu **Aplikované kroky**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-156">If you're using the default Project actuals (PSA to Fin and Ops) template, in Power Query, select the last **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="cd91b-157">V poli **Funkce** nahraďte **USSI** názvem právnické osoby, která by měla být použita s integrací.</span><span class="sxs-lookup"><span data-stu-id="cd91b-157">In the **Function** entry, replace **USSI** with the name of the legal entity that should be used with the integration.</span></span> <span data-ttu-id="cd91b-158">Do záznamu **Funkce** přidejte podle potřeby další podmínky a aktualizujte podmínku **else** z **USMF** na správnou právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="cd91b-158">Add additional conditions to the **Function** entry as you require, and update the **else** condition from **USMF** to the correct legal entity.</span></span>
- <span data-ttu-id="cd91b-159">Pokud vytváříte novou šablonu, musíte přidat sloupec, abyste podpořili mezipodnikový čas a výdaje.</span><span class="sxs-lookup"><span data-stu-id="cd91b-159">If you're creating a new template, you must add the column to support intercompany time and expenses.</span></span> <span data-ttu-id="cd91b-160">Vyberte **Přidat podmíněný sloupec** a zadejte název nového sloupce, například **LegalEntity**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-160">Select **Add Conditional Column** , and enter a name for the column, such as **LegalEntity**.</span></span> <span data-ttu-id="cd91b-161">Zadejte podmínku pro sloupec, kde pokud **název msdyn\_contractorganizationalunitid.msdyn\_** je \<organizational unit\>, pak \<enter the legal entity\> ; jinak null.</span><span class="sxs-lookup"><span data-stu-id="cd91b-161">Enter a condition for the column, where, if **msdyn\_contractorganizationalunitid.msdyn\_name** is \<organizational unit\>, then \<enter the legal entity\>; else null.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cd91b-162">Mapování šablon v integraci dat</span><span class="sxs-lookup"><span data-stu-id="cd91b-162">Template mapping in Data integration</span></span>

<span data-ttu-id="cd91b-163">Následující obrázky ukazují příklady mapování úlohy šablony v Integraci dat.</span><span class="sxs-lookup"><span data-stu-id="cd91b-163">The following illustrations show an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="cd91b-164">Mapování zobrazuje informace pole, které budou synchronizovány z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-164">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="cd91b-165">[![Mapování šablon – Skutečnosti](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="cd91b-165">[![Template mapping - Actuals](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)</span></span>

<span data-ttu-id="cd91b-166">[![Mapování šablon – Propojení transakcí](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)</span><span class="sxs-lookup"><span data-stu-id="cd91b-166">[![Template mapping - Transaction connections](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)</span></span>

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a><span data-ttu-id="cd91b-167">Import z pracovní tabulky po integraci z Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cd91b-167">Import from staging table after integration from Project Service Automation</span></span>

<span data-ttu-id="cd91b-168">Periodický proces Import z pracovní tabulky musí být spuštěn po synchronizaci skutečných hodnot z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-168">The Import from staging table periodic process must be run after the synchronization of actuals from Project Service Automation to Finance.</span></span> <span data-ttu-id="cd91b-169">Tento proces naimportuje transakce projektu z pracovní tabulky do integračního deníku Project Service Automation, kde se použije účetnictví a lze zaúčtovat importované transakce.</span><span class="sxs-lookup"><span data-stu-id="cd91b-169">This process will import the project transactions from the staging table into the Project Service Automation integration journal, where the accounting is applied and the imported transactions can be posted.</span></span> <span data-ttu-id="cd91b-170">Doporučujeme spustit tento proces v dávkovém režimu; lze jej volitelně nastavit tak, aby fungoval jako opakující se dávka.</span><span class="sxs-lookup"><span data-stu-id="cd91b-170">We recommend that you run this process in batch mode; it can optionally be set up to run as a recurring batch.</span></span>

## <a name="update-actuals-from-finance"></a><span data-ttu-id="cd91b-171">Aktualizace skutečných hodnot z modulu Finance</span><span class="sxs-lookup"><span data-stu-id="cd91b-171">Update actuals from Finance</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="cd91b-172">Šablona a úkoly</span><span class="sxs-lookup"><span data-stu-id="cd91b-172">Template and tasks</span></span>

<span data-ttu-id="cd91b-173">Následující šablona a podkladové úlohy se používají k synchronizaci čísla dokladu a daně z obratu za zaúčtované transakce projektu z Finance do Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="cd91b-173">The following template and underlying tasks are used to synchronize the voucher number and sales taxes for posted project transactions from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="cd91b-174">**Název šablony v integraci dat** Aktualizace skutečných hodnot projektu (Fin Ops do PSA)</span><span class="sxs-lookup"><span data-stu-id="cd91b-174">**Name of the template in Data integration:** Project actuals update (Fin Ops to PSA)</span></span>
- <span data-ttu-id="cd91b-175">**Název úloh v projektu:**</span><span class="sxs-lookup"><span data-stu-id="cd91b-175">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="cd91b-176">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="cd91b-176">Actuals</span></span> 
    - <span data-ttu-id="cd91b-177">TransactionConnections</span><span class="sxs-lookup"><span data-stu-id="cd91b-177">TransactionConnections</span></span>

### <a name="entity-set"></a><span data-ttu-id="cd91b-178">Sada entit</span><span class="sxs-lookup"><span data-stu-id="cd91b-178">Entity set</span></span>

| <span data-ttu-id="cd91b-179">Finance</span><span class="sxs-lookup"><span data-stu-id="cd91b-179">Finance</span></span>                                                  | <span data-ttu-id="cd91b-180">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cd91b-180">Project Service Automation</span></span> |
|----------------------------------------------------------|----------------------------|
| <span data-ttu-id="cd91b-181">Entita integrace pro skutečné hodnoty projektu</span><span class="sxs-lookup"><span data-stu-id="cd91b-181">Integration entity for project actuals</span></span>                   | <span data-ttu-id="cd91b-182">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="cd91b-182">Actuals</span></span>                    |
| <span data-ttu-id="cd91b-183">Entita integrace pro vztahy projektových transakcí</span><span class="sxs-lookup"><span data-stu-id="cd91b-183">Integration entity for project transaction relationships</span></span> | <span data-ttu-id="cd91b-184">Propojení transakcí</span><span class="sxs-lookup"><span data-stu-id="cd91b-184">Transaction Connections</span></span>    |

### <a name="entity-flow"></a><span data-ttu-id="cd91b-185">Tok entity</span><span class="sxs-lookup"><span data-stu-id="cd91b-185">Entity flow</span></span>

<span data-ttu-id="cd91b-186">Odhady skutečných hodnot projektu hodin jsou spravovány v aplikaci Project Service Automation a jsou synchronizovány s deníkem integrace projektu v modulu Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-186">Project actuals are managed in Project Service Automation, and they are synchronized to the project integration journal in Finance.</span></span> <span data-ttu-id="cd91b-187">Po zveřejnění skutečných hodnot v modulu Finance se aktualizují v Project Service Automation o číslo dokladu z Finance.</span><span class="sxs-lookup"><span data-stu-id="cd91b-187">After actuals are posted in Finance, they are updated in Project Service Automation with the voucher number from Finance.</span></span> <span data-ttu-id="cd91b-188">Pokud byly ve Finance přidány daně z obratu, v Project Service Automation se vytvoří nové skutečné hodnoty daně.</span><span class="sxs-lookup"><span data-stu-id="cd91b-188">If sales taxes were added in Finance, new tax actuals are created in Project Service Automation.</span></span>

### <a name="power-query"></a><span data-ttu-id="cd91b-189">Power Query</span><span class="sxs-lookup"><span data-stu-id="cd91b-189">Power Query</span></span>

<span data-ttu-id="cd91b-190">V šabloně skutečných hodnot projektu musíte použít Power Query k dokončení těchto úkolů:</span><span class="sxs-lookup"><span data-stu-id="cd91b-190">In the project actuals update template, you must use Power Query to complete these tasks:</span></span>

- <span data-ttu-id="cd91b-191">Transformujte typ transakce ve Finance na správný typ transakce v Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="cd91b-191">Transform the transaction type in Finance to the correct transaction type in Project Service Automation.</span></span> <span data-ttu-id="cd91b-192">Tato transformace je již definována v aktualizaci šablony Skutečné hodnoty projektu (Fin Ops do PSA).</span><span class="sxs-lookup"><span data-stu-id="cd91b-192">This transformation is already defined in the Project actuals update (Fin Ops to PSA) template.</span></span>
- <span data-ttu-id="cd91b-193">Transformujte typ fakturace v modulu Finance na správný typ fakturace v Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="cd91b-193">Transform the billing type in Finance to the correct billing type in Project Service Automation.</span></span> <span data-ttu-id="cd91b-194">Tato transformace je již definována v aktualizaci šablony Skutečné hodnoty projektu (Fin Ops do PSA).</span><span class="sxs-lookup"><span data-stu-id="cd91b-194">This transformation is already defined in the Project actuals update (Fin Ops to PSA) template.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cd91b-195">Mapování šablon v integraci dat</span><span class="sxs-lookup"><span data-stu-id="cd91b-195">Template mapping in Data integration</span></span>

<span data-ttu-id="cd91b-196">Následující obrázky ukazují příklady mapování úlohy šablony v Integraci dat.</span><span class="sxs-lookup"><span data-stu-id="cd91b-196">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="cd91b-197">Mapování zobrazuje informace pole, které budou synchronizovány z Finance do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="cd91b-197">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="cd91b-198">[![Mapování šablon – Aktualizace skutečností](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="cd91b-198">[![Template mapping - Actuals update](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)</span></span>

<span data-ttu-id="cd91b-199">[![Mapování šablon – Aktualizace transakce](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)</span><span class="sxs-lookup"><span data-stu-id="cd91b-199">[![Template mapping - Transaction update](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)</span></span>