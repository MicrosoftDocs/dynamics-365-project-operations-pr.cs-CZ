---
title: Určení typu nasazení
description: Tento téma poskytuje informace, které vám pomůžou určit hlavní typ nasazení Project Operations pro vaši společnost.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073784"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="becee-103">Určení typu nasazení</span><span class="sxs-lookup"><span data-stu-id="becee-103">Determine your deployment type</span></span>

<span data-ttu-id="becee-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="becee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="becee-105">Po zakoupení licence začněte zde a určete nejlepší model nasazení Dynamics 365 Project Operations pomocí [Řízený průběh instalace](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="becee-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="becee-106">Poté, co dokončíte postup instalace s průvodcem, budete přesměrováni na správný portál pro správu, abyste dokončili instalaci.</span><span class="sxs-lookup"><span data-stu-id="becee-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="becee-107">Dokončete instalaci podle informací o nasazení.</span><span class="sxs-lookup"><span data-stu-id="becee-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="becee-108">Stávající zákazníci Dynamics pomocí Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="becee-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="becee-109">Project Operations zahrnuje funkce dodávané s Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="becee-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="becee-110">Pro tyto zákazníky bude v budoucnu vydána cesta k upgradu.</span><span class="sxs-lookup"><span data-stu-id="becee-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="becee-111">Stávající zákazníci Dynamics 365 Finance pomocí Projektového řízení a účetnictví</span><span class="sxs-lookup"><span data-stu-id="becee-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="becee-112">Stávající zákazníci Finance, kteří používají funkce řízení projektů a účetnictví, mohou toto používat tak, jak je.</span><span class="sxs-lookup"><span data-stu-id="becee-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="becee-113">Viz [Project Operations pro scénáře se skladovým materiálem a výrobními příkazy](#pma)</span><span class="sxs-lookup"><span data-stu-id="becee-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="becee-114">Typy nasazení</span><span class="sxs-lookup"><span data-stu-id="becee-114">Deployment types</span></span>
<span data-ttu-id="becee-115">Project Operations podporuje více možností nasazení, aby odpovídaly vašim požadavkům.</span><span class="sxs-lookup"><span data-stu-id="becee-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="becee-116">Ať už jste novým nebo stávajícím zákazníkem Dynamics 365, Project Operations může podpořit vaše potřeby.</span><span class="sxs-lookup"><span data-stu-id="becee-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="becee-117">Náš [Dotazník o nasazení](https://aka.ms/provisionprojectoperations) vám pomůže určit správné nasazení.</span><span class="sxs-lookup"><span data-stu-id="becee-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="becee-118">Výsledky vás povedou k jednomu z následujících typů nasazení:</span><span class="sxs-lookup"><span data-stu-id="becee-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="becee-119">Omezené nasazení – od obchodu po pro forma fakturaci</span><span class="sxs-lookup"><span data-stu-id="becee-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="becee-120">Project Operations pro scénáře se zdroji bez skladových materiálů</span><span class="sxs-lookup"><span data-stu-id="becee-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="becee-121">Project Operations pro scénáře se skladovým materiálem a výrobními příkazy</span><span class="sxs-lookup"><span data-stu-id="becee-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="becee-122">Project Operation podporují scénáře zásob / výrobní zakázky a scénáře bez zásob / zdrojů ve stejném prostředí prostřednictvím konfigurací na úrovni právnických osob.</span><span class="sxs-lookup"><span data-stu-id="becee-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="becee-123">Například společnost Contoso může využívat možnosti skladového materiálu / výrobní objednávky ve svém výrobním závodě v USA (právnická osoba = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="becee-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="becee-124">Společnost Contoso může ve svém servisním zařízení Contoso Robotics Arms ve Velké Británii využívat funkce, které nejsou skladové / založené na zdrojích (právnická osoba = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="becee-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="becee-125">Omezené nasazení – od obchodu po pro forma fakturaci</span><span class="sxs-lookup"><span data-stu-id="becee-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="becee-126">Omezené nasazení zahrnuje následující funkce:</span><span class="sxs-lookup"><span data-stu-id="becee-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="becee-127">Plánování projektu pomocí Microsoft Project pro web</span><span class="sxs-lookup"><span data-stu-id="becee-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="becee-128">Multidimenzionální ceny</span><span class="sxs-lookup"><span data-stu-id="becee-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="becee-129">Sjednocené řízení zdrojů</span><span class="sxs-lookup"><span data-stu-id="becee-129">Unified Resource Management</span></span>
- <span data-ttu-id="becee-130">Doba sledování</span><span class="sxs-lookup"><span data-stu-id="becee-130">Time Tracking</span></span>
- <span data-ttu-id="becee-131">Základní výdaje</span><span class="sxs-lookup"><span data-stu-id="becee-131">Basic Expense</span></span>
- <span data-ttu-id="becee-132">Návrh faktury</span><span class="sxs-lookup"><span data-stu-id="becee-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="becee-133">Postup nasazení</span><span class="sxs-lookup"><span data-stu-id="becee-133">Deployment steps</span></span>
<span data-ttu-id="becee-134">Určete nejlepší model nasazení Project Operations pomocí [Dotazník o nasazení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="becee-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="becee-135">Pro toto nasazení viz [Zaregistrujte se k odběru náhledu](lite-preview-subscription-sign-up.md) a [Zřídit nové prostředí](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="becee-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="becee-136">Project Operations pro scénáře se zdroji bez skladových materiálů</span><span class="sxs-lookup"><span data-stu-id="becee-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="becee-137">Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě:</span><span class="sxs-lookup"><span data-stu-id="becee-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="becee-138">Plánování projektu pomocí Microsoft Project pro web</span><span class="sxs-lookup"><span data-stu-id="becee-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="becee-139">Multidimenzionální ceny</span><span class="sxs-lookup"><span data-stu-id="becee-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="becee-140">Sjednocené řízení zdrojů</span><span class="sxs-lookup"><span data-stu-id="becee-140">Unified Resource Management</span></span>
- <span data-ttu-id="becee-141">Doba sledování</span><span class="sxs-lookup"><span data-stu-id="becee-141">Time Tracking</span></span>
- <span data-ttu-id="becee-142">Základní výdaje</span><span class="sxs-lookup"><span data-stu-id="becee-142">Basic Expense</span></span>
- <span data-ttu-id="becee-143">Plné výdaje</span><span class="sxs-lookup"><span data-stu-id="becee-143">Full Expense</span></span>
- <span data-ttu-id="becee-144">OCR účtenky</span><span class="sxs-lookup"><span data-stu-id="becee-144">Receipt OCR</span></span>
- <span data-ttu-id="becee-145">Plná fakturace</span><span class="sxs-lookup"><span data-stu-id="becee-145">Full Invoicing</span></span>
- <span data-ttu-id="becee-146">Uznání výnosů</span><span class="sxs-lookup"><span data-stu-id="becee-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="becee-147">Postup nasazení</span><span class="sxs-lookup"><span data-stu-id="becee-147">Deployment steps</span></span>
<span data-ttu-id="becee-148">Určete nejlepší model nasazení Project Operations pomocí [Dotazník o nasazení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="becee-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="becee-149">Pro toto nasazení viz [Zaregistrujte se k odběru náhledu](resource-sign-up-preview-subscription.md) a [Zřídit nové prostředí](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="becee-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="becee-150">Project Operations pro scénáře se skladovým materiálem a výrobními příkazy</span><span class="sxs-lookup"><span data-stu-id="becee-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="becee-151">Plánování projektu pomocí strukturovaného rozpisu prací</span><span class="sxs-lookup"><span data-stu-id="becee-151">Project planning using WBS</span></span>
- <span data-ttu-id="becee-152">Správa zdrojů</span><span class="sxs-lookup"><span data-stu-id="becee-152">Resource Management</span></span>
- <span data-ttu-id="becee-153">Doba sledování</span><span class="sxs-lookup"><span data-stu-id="becee-153">Time Tracking</span></span>
- <span data-ttu-id="becee-154">Plné výdaje</span><span class="sxs-lookup"><span data-stu-id="becee-154">Full Expense</span></span>
- <span data-ttu-id="becee-155">OCR účtenky</span><span class="sxs-lookup"><span data-stu-id="becee-155">Receipt OCR</span></span>
- <span data-ttu-id="becee-156">Plná fakturace</span><span class="sxs-lookup"><span data-stu-id="becee-156">Full Invoicing</span></span>
- <span data-ttu-id="becee-157">Uznání výnosů</span><span class="sxs-lookup"><span data-stu-id="becee-157">Revenue Recognition</span></span>
- <span data-ttu-id="becee-158">Výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="becee-158">Production Orders</span></span>
- <span data-ttu-id="becee-159">Podpora materiálů</span><span class="sxs-lookup"><span data-stu-id="becee-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="becee-160">Postup nasazení</span><span class="sxs-lookup"><span data-stu-id="becee-160">Deployment steps</span></span>
<span data-ttu-id="becee-161">Určete nejlepší model nasazení Project Operations pomocí [Dotazník o nasazení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="becee-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="becee-162">Pro toto nasazení viz [Zaregistrujte se k odběru náhledu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) a [Zřídit nové prostředí](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="becee-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

