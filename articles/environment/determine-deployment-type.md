---
title: Typy nasazení
description: Tento téma poskytuje informace, které vám pomůžou určit hlavní typ nasazení Project Operations pro vaši společnost.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948798"
---
# <a name="deployment-types"></a><span data-ttu-id="c9ad5-103">Typy nasazení</span><span class="sxs-lookup"><span data-stu-id="c9ad5-103">Deployment types</span></span>

<span data-ttu-id="c9ad5-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="c9ad5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c9ad5-105">Po zakoupení licence začněte zde a určete nejlepší model nasazení Dynamics 365 Project Operations pomocí [Řízený průběh instalace](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="c9ad5-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="c9ad5-106">Poté, co dokončíte postup instalace s průvodcem, budete přesměrováni na správný portál pro správu, abyste dokončili instalaci.</span><span class="sxs-lookup"><span data-stu-id="c9ad5-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="c9ad5-107">Dokončete instalaci podle podrobností nasazení níže.</span><span class="sxs-lookup"><span data-stu-id="c9ad5-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="c9ad5-108">Stávající zákazníci Dynamics pomocí Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c9ad5-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="c9ad5-109">Project Operations zahrnuje funkce dodávané s Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c9ad5-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="c9ad5-110">Pro tyto zákazníky bude v budoucnu vydána cesta k upgradu.</span><span class="sxs-lookup"><span data-stu-id="c9ad5-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="c9ad5-111">Stávající zákazníci Dynamics 365 Finance pomocí Projektového řízení a účetnictví</span><span class="sxs-lookup"><span data-stu-id="c9ad5-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="c9ad5-112">Stávající zákazníci Finance, kteří používají funkce řízení projektů a účetnictví, mohou toto používat tak, jak je.</span><span class="sxs-lookup"><span data-stu-id="c9ad5-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="c9ad5-113">Viz [Project Operations pro scénáře se skladovým materiálem a výrobními příkazy](#pma)</span><span class="sxs-lookup"><span data-stu-id="c9ad5-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="c9ad5-114">Project Operations podporuje více možností nasazení, aby odpovídaly vašim požadavkům.</span><span class="sxs-lookup"><span data-stu-id="c9ad5-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="c9ad5-115">Ať už jste novým nebo stávajícím zákazníkem Dynamics 365, Project Operations může podpořit vaše potřeby.</span><span class="sxs-lookup"><span data-stu-id="c9ad5-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="c9ad5-116">Náš [Dotazník o nasazení](https://aka.ms/provisionprojectoperations) vám pomůže určit správné nasazení.</span><span class="sxs-lookup"><span data-stu-id="c9ad5-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="c9ad5-117">Výsledky vás povedou k jednomu z následujících typů nasazení:</span><span class="sxs-lookup"><span data-stu-id="c9ad5-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="c9ad5-118">Omezené nasazení – od obchodu po pro forma fakturaci</span><span class="sxs-lookup"><span data-stu-id="c9ad5-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="c9ad5-119">Project Operations pro scénáře se zdroji bez skladových materiálů</span><span class="sxs-lookup"><span data-stu-id="c9ad5-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="c9ad5-120">Project Operations pro scénáře se skladovým materiálem a výrobními příkazy</span><span class="sxs-lookup"><span data-stu-id="c9ad5-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="c9ad5-121">Project Operation podporují scénáře zásob / výrobní zakázky a scénáře bez zásob / zdrojů ve stejném prostředí prostřednictvím konfigurací na úrovni právnických osob.</span><span class="sxs-lookup"><span data-stu-id="c9ad5-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="c9ad5-122">Například společnost Contoso může využívat možnosti se skladovým materiálem a výrobními příkazy ve svém výrobním závodě v USA (Právnická osoba = Contoso Manufacturing United States) a neskladovaných / založených na zdrojích ve svých servisních zařízeních Contoso Robotics Arms ve Velké Británii (Právnická osoba = Contoso Robotics United Království).</span><span class="sxs-lookup"><span data-stu-id="c9ad5-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="c9ad5-123"><a name="lite"><a/>Omezené nasazení – od obchodu po pro forma fakturaci</span><span class="sxs-lookup"><span data-stu-id="c9ad5-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="c9ad5-124">Omezené nasazení zahrnuje následující funkce:</span><span class="sxs-lookup"><span data-stu-id="c9ad5-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="c9ad5-125">Plánování projektu pomocí Microsoft Project pro web</span><span class="sxs-lookup"><span data-stu-id="c9ad5-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="c9ad5-126">Multidimenzionální ceny</span><span class="sxs-lookup"><span data-stu-id="c9ad5-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="c9ad5-127">Sjednocené řízení zdrojů</span><span class="sxs-lookup"><span data-stu-id="c9ad5-127">Unified Resource Management</span></span>
- <span data-ttu-id="c9ad5-128">Doba sledování</span><span class="sxs-lookup"><span data-stu-id="c9ad5-128">Time Tracking</span></span>
- <span data-ttu-id="c9ad5-129">Základní výdaje</span><span class="sxs-lookup"><span data-stu-id="c9ad5-129">Basic Expense</span></span>
- <span data-ttu-id="c9ad5-130">Návrh faktury</span><span class="sxs-lookup"><span data-stu-id="c9ad5-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="c9ad5-131">Postup nasazení:</span><span class="sxs-lookup"><span data-stu-id="c9ad5-131">Deployment steps:</span></span>
<span data-ttu-id="c9ad5-132">Určete nejlepší model nasazení Project Operations pomocí [Dotazník o nasazení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="c9ad5-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="c9ad5-133">Pro toto nasazení viz [Zaregistrujte se k odběru náhledu](lite-preview-subscription-sign-up.md) a [Zřídit nové prostředí](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="c9ad5-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="c9ad5-134"><a name="integrated"><a/>Project Operations pro scénáře se zdroji bez skladových materiálů</span><span class="sxs-lookup"><span data-stu-id="c9ad5-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="c9ad5-135">Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě:</span><span class="sxs-lookup"><span data-stu-id="c9ad5-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="c9ad5-136">Plánování projektu pomocí Microsoft Project pro web</span><span class="sxs-lookup"><span data-stu-id="c9ad5-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="c9ad5-137">Multidimenzionální ceny</span><span class="sxs-lookup"><span data-stu-id="c9ad5-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="c9ad5-138">Sjednocené řízení zdrojů</span><span class="sxs-lookup"><span data-stu-id="c9ad5-138">Unified Resource Management</span></span>
- <span data-ttu-id="c9ad5-139">Doba sledování</span><span class="sxs-lookup"><span data-stu-id="c9ad5-139">Time Tracking</span></span>
- <span data-ttu-id="c9ad5-140">Základní výdaje</span><span class="sxs-lookup"><span data-stu-id="c9ad5-140">Basic Expense</span></span>
- <span data-ttu-id="c9ad5-141">Plné výdaje</span><span class="sxs-lookup"><span data-stu-id="c9ad5-141">Full Expense</span></span>
- <span data-ttu-id="c9ad5-142">OCR účtenky</span><span class="sxs-lookup"><span data-stu-id="c9ad5-142">Receipt OCR</span></span>
- <span data-ttu-id="c9ad5-143">Plná fakturace</span><span class="sxs-lookup"><span data-stu-id="c9ad5-143">Full Invoicing</span></span>
- <span data-ttu-id="c9ad5-144">Uznání výnosů</span><span class="sxs-lookup"><span data-stu-id="c9ad5-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="c9ad5-145">Postup nasazení:</span><span class="sxs-lookup"><span data-stu-id="c9ad5-145">Deployment steps:</span></span>
<span data-ttu-id="c9ad5-146">Určete nejlepší model nasazení Project Operations pomocí [Dotazník o nasazení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="c9ad5-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="c9ad5-147">Pro toto nasazení viz [Zaregistrujte se k odběru náhledu](resource-sign-up-preview-subscription.md) a [Zřídit nové prostředí](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="c9ad5-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="c9ad5-148">Project Operations pro scénáře se skladovým materiálem a výrobními příkazy</span><span class="sxs-lookup"><span data-stu-id="c9ad5-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="c9ad5-149">Plánování projektu pomocí strukturovaného rozpisu prací</span><span class="sxs-lookup"><span data-stu-id="c9ad5-149">Project planning using WBS</span></span>
- <span data-ttu-id="c9ad5-150">Správa zdrojů</span><span class="sxs-lookup"><span data-stu-id="c9ad5-150">Resource Management</span></span>
- <span data-ttu-id="c9ad5-151">Doba sledování</span><span class="sxs-lookup"><span data-stu-id="c9ad5-151">Time Tracking</span></span>
- <span data-ttu-id="c9ad5-152">Plné výdaje</span><span class="sxs-lookup"><span data-stu-id="c9ad5-152">Full Expense</span></span>
- <span data-ttu-id="c9ad5-153">OCR účtenky</span><span class="sxs-lookup"><span data-stu-id="c9ad5-153">Receipt OCR</span></span>
- <span data-ttu-id="c9ad5-154">Plná fakturace</span><span class="sxs-lookup"><span data-stu-id="c9ad5-154">Full Invoicing</span></span>
- <span data-ttu-id="c9ad5-155">Uznání výnosů</span><span class="sxs-lookup"><span data-stu-id="c9ad5-155">Revenue Recognition</span></span>
- <span data-ttu-id="c9ad5-156">Výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="c9ad5-156">Production Orders</span></span>
- <span data-ttu-id="c9ad5-157">Podpora materiálů</span><span class="sxs-lookup"><span data-stu-id="c9ad5-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="c9ad5-158">Postup nasazení:</span><span class="sxs-lookup"><span data-stu-id="c9ad5-158">Deployment steps:</span></span>
<span data-ttu-id="c9ad5-159">Určete nejlepší model nasazení Project Operations pomocí [Dotazník o nasazení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="c9ad5-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="c9ad5-160">Pro toto nasazení viz [Zaregistrujte se k odběru náhledu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) a [Zřídit nové prostředí](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="c9ad5-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



