---
title: Synchronizace projektových úkolů přímo z Project Service Automation do Finance and Operations
description: Toto téma popisuje šablonu a základní úkol, které se používají k synchronizaci projektových úkolů přímo z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073762"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="738ac-103">Synchronizace projektových úkolů přímo z Project Service Automation do Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="738ac-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="738ac-104">Toto téma popisuje šablonu a základní úkol, který se používají k synchronizaci projektových úkolů přímo z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="738ac-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="738ac-105">Integrace projektových úkolů, kategorie transakcí výdajů, odhady hodin, odhady výdajů a zamykání funkcí jsou k dispozici ve verzi 8.0.</span><span class="sxs-lookup"><span data-stu-id="738ac-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="738ac-106">Pokud používáte Enterprise Edition 7.3.0, po instalaci aktualizací KB 4132657 a KB 4132660 budete moci pomocí šablon integrovat projektové úkoly, kategorie transakcí výdajů, odhady hodin, odhady výdajů a skutečné hodnoty, a také konfigurovat blokování funkcí.</span><span class="sxs-lookup"><span data-stu-id="738ac-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="738ac-107">Pokud musíte resetovat rozúčtování, doporučujeme vám také nainstalovat KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="738ac-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="738ac-108">Integrace skutečných hodnot je k dispozici ve verzi 8.0.1 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="738ac-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="738ac-109">Datový tok pro Project Service Automation do Finance</span><span class="sxs-lookup"><span data-stu-id="738ac-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="738ac-110">Řešení integrace aplikací Project Service Automation do Finance využívá funkci integrace dat k synchronizaci dat napříč instancemi aplikací Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="738ac-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="738ac-111">Šablona integrace, která je k dispozici s funkcí Integrace dat, umožňuje tok dat o projektových úkolech z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="738ac-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="738ac-112">Následující obrázek ukazuje, jak jsou data synchronizována mezi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="738ac-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="738ac-113">[![Datový tok pro integraci Project Service Automation s Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="738ac-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="738ac-114">Šablona a úkol</span><span class="sxs-lookup"><span data-stu-id="738ac-114">Template and task</span></span>

<span data-ttu-id="738ac-115">Pro přístup k šabloně v centru pro správu Microsoft Power Apps vyberte **Projekty** a poté v pravém horním rohu vyberte **Nový projekt** , aby se vybraly veřejné šablony.</span><span class="sxs-lookup"><span data-stu-id="738ac-115">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="738ac-116">Následující šablona a základní úloha se používají k synchronizaci projektových úkolů z Project Service Automation do Finance:</span><span class="sxs-lookup"><span data-stu-id="738ac-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="738ac-117">**Název šablony v integraci dat** Projektové úkoly (PSA do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="738ac-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="738ac-118">**Název úlohy v projektu:** Projektové úkoly</span><span class="sxs-lookup"><span data-stu-id="738ac-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="738ac-119">Než může dojít k synchronizaci projektových úkolů, musíte synchronizovat účty projektové smlouvy a projekty.</span><span class="sxs-lookup"><span data-stu-id="738ac-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="738ac-120">Sada entit</span><span class="sxs-lookup"><span data-stu-id="738ac-120">Entity set</span></span>

| <span data-ttu-id="738ac-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="738ac-121">Project Service Automation</span></span> | <span data-ttu-id="738ac-122">Finance</span><span class="sxs-lookup"><span data-stu-id="738ac-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="738ac-123">Projektové úkoly</span><span class="sxs-lookup"><span data-stu-id="738ac-123">Project Tasks</span></span>              | <span data-ttu-id="738ac-124">Entita integrace pro projektový úkol</span><span class="sxs-lookup"><span data-stu-id="738ac-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="738ac-125">Tok entity</span><span class="sxs-lookup"><span data-stu-id="738ac-125">Entity flow</span></span>

<span data-ttu-id="738ac-126">Projektové úkoly jsou spravovány v aplikaci Project Service Automation a jsou synchronizovány do Finance jako projektové aktivity.</span><span class="sxs-lookup"><span data-stu-id="738ac-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="738ac-127">Předpoklady a nastavení mapování</span><span class="sxs-lookup"><span data-stu-id="738ac-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="738ac-128">Než může dojít k synchronizaci projektových úkolů, musíte synchronizovat účty projektové smlouvy a projekty.</span><span class="sxs-lookup"><span data-stu-id="738ac-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="738ac-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="738ac-129">Power Query</span></span>

<span data-ttu-id="738ac-130">K filtrování dat musíte použít Microsoft Power Query pro Excel, pokud je splněna následující podmínka:</span><span class="sxs-lookup"><span data-stu-id="738ac-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="738ac-131">V úkolu projektu máte záznamy specifické pro daný prostředek.</span><span class="sxs-lookup"><span data-stu-id="738ac-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="738ac-132">Pokud musíte použít Power Query, postupujte podle těchto pokynů:</span><span class="sxs-lookup"><span data-stu-id="738ac-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="738ac-133">Šablona Project tasks (PSA to Fin and Ops) má výchozí filtr, který vylučuje záznamy specifické pro prostředek z úkolu projektu nastavením filtru na **IsLineTask** na **Nepravdivé**.</span><span class="sxs-lookup"><span data-stu-id="738ac-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="738ac-134">Pokud vytvoříte vlastní šablonu, musíte přidat tento filtr.</span><span class="sxs-lookup"><span data-stu-id="738ac-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="738ac-135">Mapování šablon v integraci dat</span><span class="sxs-lookup"><span data-stu-id="738ac-135">Template mapping in Data integration</span></span>

<span data-ttu-id="738ac-136">Následující obrázek ukazuje příklad mapování úlohy šablony v Integraci dat.</span><span class="sxs-lookup"><span data-stu-id="738ac-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="738ac-137">Mapování zobrazuje informace pole, které budou synchronizovány z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="738ac-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="738ac-138">[![Mapování šablon](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="738ac-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
