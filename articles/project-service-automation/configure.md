---
title: Konfigurace Project Service Automation
description: Postup konfigurace Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750318"
---
# <a name="configure-project-service"></a><span data-ttu-id="f0e8b-103">Konfigurace Project Service</span><span class="sxs-lookup"><span data-stu-id="f0e8b-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f0e8b-104">Než budete moci používat možnosti automatizace [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v aplikaci [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] ke správě obchodních vztahů, projektů a zdrojů, musíte provést několik kroků konfigurace, abyste zajistili, že bude řešení [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vyhovovat potřebám vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="f0e8b-105">Mezi tyto kroky patří:</span><span class="sxs-lookup"><span data-stu-id="f0e8b-105">These steps include:</span></span>  
  
-   <span data-ttu-id="f0e8b-106">[Nastavení časových jednotek](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="f0e8b-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="f0e8b-107">Konfigurace časových jednotek v katalogu výrobků, které použijete jako základ pro plánování a fakturování projektů.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="f0e8b-108">[Nastavení měny a směnných kurzů](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="f0e8b-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="f0e8b-109">Nastavení měny pro použití v projektech.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="f0e8b-110">[Vytvoření organizačních jednotek](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="f0e8b-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="f0e8b-111">Nastavení skupin, které vaše společnost používá k rozdělení své činnosti, například podle geografických vlastností, obchodní funkce nebo jiného logického dělení.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="f0e8b-112">[Nastavení četnosti faktur](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="f0e8b-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="f0e8b-113">Nastavení časových období, která chcete použít pro fakturování klientů.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="f0e8b-114">[Konfigurace kategorií transakcí](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="f0e8b-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="f0e8b-115">Nastavení kategorií transakcí, podle kterých mohou vaši konzultanti jejich účtovat fakturovatelné a nefakturovatelné výdaje.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="f0e8b-116">[Konfigurace kategorií výdajů](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="f0e8b-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="f0e8b-117">Nastavení kategorií, podle kterých mohou vaši konzultanti jejich účtovat fakturovatelné a nefakturovatelné výdaje.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="f0e8b-118">[Vytvoření položek katalogu produktů](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="f0e8b-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="f0e8b-119">Přidání produktů, které prodáváte, například licencí na software, do katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="f0e8b-120">[Vytvoření ceníku](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="f0e8b-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="f0e8b-121">Konfigurace různých ceníků podle toho, kolik chcete účtovat klientům za každou roli, kterou jejich projekt vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="f0e8b-122">[Nastavení zdrojů](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="f0e8b-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="f0e8b-123">Přidání dovedností, odborných znalostí, rolí zdrojů a dalších informací o zdrojích, kterou budete pro vaše projekty potřebovat.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f0e8b-124">Viz také</span><span class="sxs-lookup"><span data-stu-id="f0e8b-124">See Also</span></span>  
 <span data-ttu-id="f0e8b-125">[Přehled Project Service Automation](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="f0e8b-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="f0e8b-126">[Konfigurace Project Service Automation](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="f0e8b-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="f0e8b-127">[Příručka pro manažera obchodních vztahů](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f0e8b-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="f0e8b-128">[Příručka pro projektového manažera](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f0e8b-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="f0e8b-129">[Příručka pro manažera zdrojů](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f0e8b-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="f0e8b-130">Příručka – Čas, výdaje a spolupráce</span><span class="sxs-lookup"><span data-stu-id="f0e8b-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
