---
title: Určení typu nasazení
description: Tento téma poskytuje informace, které vám pomůžou určit hlavní typ nasazení Project Operations pro vaši společnost.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401210"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="2aa1d-103">Určení typu nasazení</span><span class="sxs-lookup"><span data-stu-id="2aa1d-103">Determine your deployment type</span></span>

<span data-ttu-id="2aa1d-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="2aa1d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2aa1d-105">Po zakoupení licence začněte zde a určete nejlepší model nasazení Dynamics 365 Project Operations pomocí [Řízený průběh instalace](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="2aa1d-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="2aa1d-106">Poté, co dokončíte postup instalace s průvodcem, budete přesměrováni na správný portál pro správu, abyste dokončili instalaci.</span><span class="sxs-lookup"><span data-stu-id="2aa1d-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="2aa1d-107">Dokončete instalaci podle informací o nasazení.</span><span class="sxs-lookup"><span data-stu-id="2aa1d-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="2aa1d-108">Stávající zákazníci Dynamics pomocí Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2aa1d-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="2aa1d-109">Project Operations zahrnuje funkce dodávané s Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2aa1d-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="2aa1d-110">Pro tyto zákazníky bude v 1. vlně vydání v roce 2021 uvolněna cesta k upgradu.</span><span class="sxs-lookup"><span data-stu-id="2aa1d-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="2aa1d-111">Stávající zákazníci Dynamics 365 Finance pomocí Projektového řízení a účetnictví</span><span class="sxs-lookup"><span data-stu-id="2aa1d-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="2aa1d-112">Stávající zákazníci řešení Finance, kteří používají funkce správy projektů a účetnictví, je mohou i nadále používat tak, jak jsou.</span><span class="sxs-lookup"><span data-stu-id="2aa1d-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="2aa1d-113">Viz [Project Operations pro scénáře se skladovým materiálem a výrobními příkazy](#pma)</span><span class="sxs-lookup"><span data-stu-id="2aa1d-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="2aa1d-114">Typy nasazení</span><span class="sxs-lookup"><span data-stu-id="2aa1d-114">Deployment types</span></span>
<span data-ttu-id="2aa1d-115">Project Operations podporuje více možností nasazení, aby odpovídaly vašim požadavkům.</span><span class="sxs-lookup"><span data-stu-id="2aa1d-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="2aa1d-116">Ať už jste novým nebo stávajícím zákazníkem Dynamics 365, Project Operations může podpořit vaše potřeby.</span><span class="sxs-lookup"><span data-stu-id="2aa1d-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="2aa1d-117">Náš [Dotazník o nasazení](https://aka.ms/provisionprojectoperations) vám pomůže určit správné nasazení.</span><span class="sxs-lookup"><span data-stu-id="2aa1d-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="2aa1d-118">Výsledky vás povedou k jednomu z následujících typů nasazení:</span><span class="sxs-lookup"><span data-stu-id="2aa1d-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="2aa1d-119">Omezené nasazení – od obchodu po pro forma fakturaci</span><span class="sxs-lookup"><span data-stu-id="2aa1d-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="2aa1d-120">Project Operations pro scénáře se zdroji bez skladových materiálů</span><span class="sxs-lookup"><span data-stu-id="2aa1d-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="2aa1d-121">Project Operations pro scénáře se skladovým materiálem a výrobními příkazy</span><span class="sxs-lookup"><span data-stu-id="2aa1d-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="2aa1d-122">Project Operation podporují scénáře zásob / výrobní zakázky a scénáře bez zásob / zdrojů ve stejném prostředí prostřednictvím konfigurací na úrovni právnických osob.</span><span class="sxs-lookup"><span data-stu-id="2aa1d-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="2aa1d-123">Například společnost Contoso může využívat možnosti skladového materiálu / výrobní objednávky ve svém výrobním závodě v USA (právnická osoba = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="2aa1d-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="2aa1d-124">Společnost Contoso může ve svém servisním zařízení Contoso Robotics Arms ve Velké Británii využívat funkce, které nejsou skladové / založené na zdrojích (právnická osoba = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="2aa1d-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="2aa1d-125">Omezené nasazení – od obchodu po pro forma fakturaci</span><span class="sxs-lookup"><span data-stu-id="2aa1d-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="2aa1d-126">Omezené nasazení zahrnuje následující funkce:</span><span class="sxs-lookup"><span data-stu-id="2aa1d-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="2aa1d-127">Proces prodeje pro projekty, které rozšiřují možnosti aplikace Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="2aa1d-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="2aa1d-128">Plánování projektu pomocí Microsoft Project pro web</span><span class="sxs-lookup"><span data-stu-id="2aa1d-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="2aa1d-129">Multidimenzionální ceny</span><span class="sxs-lookup"><span data-stu-id="2aa1d-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="2aa1d-130">Sjednocené řízení zdrojů</span><span class="sxs-lookup"><span data-stu-id="2aa1d-130">Unified resource management</span></span>
- <span data-ttu-id="2aa1d-131">Sledování času</span><span class="sxs-lookup"><span data-stu-id="2aa1d-131">Time tracking</span></span>
- <span data-ttu-id="2aa1d-132">Základní výdaje</span><span class="sxs-lookup"><span data-stu-id="2aa1d-132">Basic expense</span></span>
- <span data-ttu-id="2aa1d-133">Proforma a fakturace zaměřená na zákazníka</span><span class="sxs-lookup"><span data-stu-id="2aa1d-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="2aa1d-134">Postup nasazení</span><span class="sxs-lookup"><span data-stu-id="2aa1d-134">Deployment steps</span></span>
<span data-ttu-id="2aa1d-135">Určete nejlepší model nasazení Project Operations pomocí [Dotazník o nasazení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="2aa1d-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="2aa1d-136">Pro toto nasazení viz [Zaregistrujte se k odběru náhledu](lite-preview-subscription-sign-up.md) a [Zřídit nové prostředí](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="2aa1d-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="2aa1d-137">Project Operations pro scénáře se zdroji bez skladových materiálů</span><span class="sxs-lookup"><span data-stu-id="2aa1d-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="2aa1d-138">Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě:</span><span class="sxs-lookup"><span data-stu-id="2aa1d-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="2aa1d-139">Proces prodeje pro projekty, které rozšiřují aplikaci Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="2aa1d-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="2aa1d-140">Plánování projektu pomocí Microsoft Project pro web</span><span class="sxs-lookup"><span data-stu-id="2aa1d-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="2aa1d-141">Multidimenzionální ceny</span><span class="sxs-lookup"><span data-stu-id="2aa1d-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="2aa1d-142">Sjednocené řízení zdrojů</span><span class="sxs-lookup"><span data-stu-id="2aa1d-142">Unified resource management</span></span>
- <span data-ttu-id="2aa1d-143">Sledování času</span><span class="sxs-lookup"><span data-stu-id="2aa1d-143">Time tracking</span></span>
- <span data-ttu-id="2aa1d-144">Základní výdaje</span><span class="sxs-lookup"><span data-stu-id="2aa1d-144">Basic expense</span></span>
- <span data-ttu-id="2aa1d-145">Plné výdaje</span><span class="sxs-lookup"><span data-stu-id="2aa1d-145">Full expense</span></span>
- <span data-ttu-id="2aa1d-146">OCR účtenky</span><span class="sxs-lookup"><span data-stu-id="2aa1d-146">Receipt OCR</span></span>
- <span data-ttu-id="2aa1d-147">Proforma a fakturace zaměřená na zákazníka</span><span class="sxs-lookup"><span data-stu-id="2aa1d-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="2aa1d-148">Vykazování výnosů z projektů</span><span class="sxs-lookup"><span data-stu-id="2aa1d-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="2aa1d-149">Postup nasazení</span><span class="sxs-lookup"><span data-stu-id="2aa1d-149">Deployment steps</span></span>
<span data-ttu-id="2aa1d-150">Určete nejlepší model nasazení Project Operations pomocí [Dotazník o nasazení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="2aa1d-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="2aa1d-151">Pro toto nasazení viz [Zaregistrujte se k odběru náhledu](resource-sign-up-preview-subscription.md) a [Zřídit nové prostředí](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="2aa1d-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="2aa1d-152">Project Operations pro scénáře se skladovým materiálem a výrobními příkazy</span><span class="sxs-lookup"><span data-stu-id="2aa1d-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="2aa1d-153">Plánování projektu pomocí strukturovaného rozpisu prací</span><span class="sxs-lookup"><span data-stu-id="2aa1d-153">Project planning using WBS</span></span>
- <span data-ttu-id="2aa1d-154">Správa zdrojů</span><span class="sxs-lookup"><span data-stu-id="2aa1d-154">Resource Management</span></span>
- <span data-ttu-id="2aa1d-155">Doba sledování</span><span class="sxs-lookup"><span data-stu-id="2aa1d-155">Time Tracking</span></span>
- <span data-ttu-id="2aa1d-156">Plné výdaje</span><span class="sxs-lookup"><span data-stu-id="2aa1d-156">Full Expense</span></span>
- <span data-ttu-id="2aa1d-157">OCR účtenky</span><span class="sxs-lookup"><span data-stu-id="2aa1d-157">Receipt OCR</span></span>
- <span data-ttu-id="2aa1d-158">Plná fakturace</span><span class="sxs-lookup"><span data-stu-id="2aa1d-158">Full Invoicing</span></span>
- <span data-ttu-id="2aa1d-159">Uznání výnosů</span><span class="sxs-lookup"><span data-stu-id="2aa1d-159">Revenue Recognition</span></span>
- <span data-ttu-id="2aa1d-160">Výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="2aa1d-160">Production Orders</span></span>
- <span data-ttu-id="2aa1d-161">Podpora materiálů</span><span class="sxs-lookup"><span data-stu-id="2aa1d-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="2aa1d-162">Postup nasazení</span><span class="sxs-lookup"><span data-stu-id="2aa1d-162">Deployment steps</span></span>
<span data-ttu-id="2aa1d-163">Určete nejlepší model nasazení Project Operations pomocí [Dotazník o nasazení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="2aa1d-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="2aa1d-164">Pro toto nasazení viz [Zaregistrujte se k odběru náhledu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) a [Zřídit nové prostředí](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="2aa1d-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

