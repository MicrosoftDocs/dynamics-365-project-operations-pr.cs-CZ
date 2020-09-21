---
title: Přehled aplikace Project Service Automation
description: Toto téma poskytuje informace o Dynamics 365 Project Service Automation na Dynamics 365 Finance integrační řešení.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750357"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="8c830-103">Přehled aplikace Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8c830-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8c830-104">Řešení integrace aplikací Project Service Automation do Finance využívá funkci integrace dat k synchronizaci dat napříč instancemi aplikací Dynamics 365 Finance a Dynamics 365 Project Service Automation přes Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8c830-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="8c830-105">Šablony integrace, která jsou k dispozici s funkcí integrace dat, umožňují tok dat o projektových smlouvách, projektech, řádcích projektových smluv, milníků řádků, projektových úkolů, kategorií transakcí výdajů, odhadů hodinových cen a výdajů z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="8c830-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="8c830-106">Pokud používáte verzi 7.3.0, musíte si nainstalovat aktualizaci KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="8c830-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="8c830-107">Poté budete moci integrovat projekty s pevnou cenou.</span><span class="sxs-lookup"><span data-stu-id="8c830-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="8c830-108">Pokud používáte verzi 7.3.0 a přenášíte transakce poplatků z Project Service Automation, musíte nainstalovat KB 4345320, abyste mohli zahrnout tyto poplatky do faktury projektu.</span><span class="sxs-lookup"><span data-stu-id="8c830-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="8c830-109">Pokud používáte verzi 8.0, budete moci používat projektové úkoly, kategorie transakcí výdajů, odhady hodin, odhady výdajů a zamykání funkcí.</span><span class="sxs-lookup"><span data-stu-id="8c830-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="8c830-110">Pokud používáte verzi 8.0.1 nebo novější, budete moci synchronizovat skutečné údaje.</span><span class="sxs-lookup"><span data-stu-id="8c830-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="8c830-111">Než budete moci integrovat Project Service Automation Finance, musíte nakonfigurovat integrační parametry Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8c830-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="8c830-112">Pro další informace viz [Integrační paramenty Project Service Automation](PSA-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="8c830-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="8c830-113">Toto integrační řešení umožňuje přímou synchronizaci v následujících scénářích:</span><span class="sxs-lookup"><span data-stu-id="8c830-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="8c830-114">Udržujte projektové smlouvy v Project Service Automation a synchronizujte je přímo z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="8c830-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8c830-115">Vytvořte projekty v Project Service Automation a synchronizujte je přímo z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="8c830-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8c830-116">Udržujte řádky projektových smluv v Project Service Automation a synchronizujte je přímo z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="8c830-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8c830-117">Udržujte milníky řádků projektových smluv v Project Service Automation a synchronizujte je přímo z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="8c830-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8c830-118">Udržujte úkoly projektů v Project Service Automation a synchronizujte je přímo z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="8c830-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8c830-119">Udržujte kategorie transakcí výdajů ve Finance a synchronizujte je přímo z Finance do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8c830-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="8c830-120">Vytvořte odhady projektových hodin v Project Service Automation a synchronizujte je přímo z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="8c830-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8c830-121">Vytvořte odhady projektových výdajů v Project Service Automation a synchronizujte je přímo z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="8c830-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8c830-122">Vytvořte v projektu Project Service Automation skutečné údaje o čase, výdajích a poplatcích za projekt a vytvořte transakce projektu v deníku integrace Project Service Automation, aby je bylo možné zaúčtovat ve Finance.</span><span class="sxs-lookup"><span data-stu-id="8c830-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="8c830-123">Synchronizace dat</span><span class="sxs-lookup"><span data-stu-id="8c830-123">Data synchronization</span></span>

<span data-ttu-id="8c830-124">Následující obrázek ukazuje, jak jsou data synchronizována jako součást integrace mezi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="8c830-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="8c830-125">V současné době nejsou k dispozici všechny šablony.</span><span class="sxs-lookup"><span data-stu-id="8c830-125">Not all templates are currently available.</span></span> <span data-ttu-id="8c830-126">Šablony budou vydány, jakmile budou dokončeny.</span><span class="sxs-lookup"><span data-stu-id="8c830-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="8c830-127">[![Integrace Project Service Automation s Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="8c830-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="8c830-128">Systémové požadavky na Finance</span><span class="sxs-lookup"><span data-stu-id="8c830-128">System requirements for Finance</span></span>

<span data-ttu-id="8c830-129">Chcete-li použít integrační řešení Project Service Automation to Finance, musíte nainstalovat Enterprise edition 7.3 s aktualizací platformy 12 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="8c830-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="8c830-130">Systémové pozadavky pro Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8c830-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="8c830-131">Chcete-li použít integrační řešení Project Service Automation to Finance, musíte nainstalovat následující součásti:</span><span class="sxs-lookup"><span data-stu-id="8c830-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="8c830-132">Dynamics 365 Project Service Automation verze 9.0.0.0 nebo vyšší</span><span class="sxs-lookup"><span data-stu-id="8c830-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="8c830-133">Řešení vyhlídky na hotovost pro Dynamics 365 Sales, verze 1.14.0.0 (v14) nebo novější</span><span class="sxs-lookup"><span data-stu-id="8c830-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="8c830-134">Řešení Project Service Automation to Finance pro Dynamics 365 Project Service Automation verzi 1.0.0.0 nebo novější</span><span class="sxs-lookup"><span data-stu-id="8c830-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="8c830-135">Nainstalujte řešení integrace Project Service Automation to Finance do instance Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8c830-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="8c830-136">Stáhněte si řešení integrace řešení Project Service Automation to Finance z [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) a postupujte podle pokynů, které jsou součástí řešení.</span><span class="sxs-lookup"><span data-stu-id="8c830-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
