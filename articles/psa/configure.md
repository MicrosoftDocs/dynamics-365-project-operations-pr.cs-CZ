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
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fd02611b5b3133e097b2818a725b6c5d667e5ac0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073889"
---
# <a name="configure-project-service"></a><span data-ttu-id="171b0-103">Konfigurace Project Service</span><span class="sxs-lookup"><span data-stu-id="171b0-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="171b0-104">Než budete moci používat možnosti automatizace [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v aplikaci [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] ke správě obchodních vztahů, projektů a zdrojů, musíte provést několik kroků konfigurace, abyste zajistili, že bude řešení [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vyhovovat potřebám vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="171b0-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="171b0-105">Mezi tyto kroky patří:</span><span class="sxs-lookup"><span data-stu-id="171b0-105">These steps include:</span></span>  
  
-   <span data-ttu-id="171b0-106">[Nastavení časových jednotek](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="171b0-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="171b0-107">Konfigurace časových jednotek v katalogu výrobků, které použijete jako základ pro plánování a fakturování projektů.</span><span class="sxs-lookup"><span data-stu-id="171b0-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="171b0-108">[Nastavení měny a směnných kurzů](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="171b0-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="171b0-109">Nastavení měny pro použití v projektech.</span><span class="sxs-lookup"><span data-stu-id="171b0-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="171b0-110">[Vytvoření organizačních jednotek](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="171b0-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="171b0-111">Nastavení skupin, které vaše společnost používá k rozdělení své činnosti, například podle geografických vlastností, obchodní funkce nebo jiného logického dělení.</span><span class="sxs-lookup"><span data-stu-id="171b0-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="171b0-112">[Nastavení četnosti faktur](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="171b0-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="171b0-113">Nastavení časových období, která chcete použít pro fakturování klientů.</span><span class="sxs-lookup"><span data-stu-id="171b0-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="171b0-114">[Konfigurace kategorií transakcí](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="171b0-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="171b0-115">Nastavení kategorií transakcí, podle kterých mohou vaši konzultanti jejich účtovat fakturovatelné a nefakturovatelné výdaje.</span><span class="sxs-lookup"><span data-stu-id="171b0-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="171b0-116">[Konfigurace kategorií výdajů](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="171b0-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="171b0-117">Nastavení kategorií, podle kterých mohou vaši konzultanti jejich účtovat fakturovatelné a nefakturovatelné výdaje.</span><span class="sxs-lookup"><span data-stu-id="171b0-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="171b0-118">[Vytvoření položek katalogu produktů](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="171b0-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="171b0-119">Přidání produktů, které prodáváte, například licencí na software, do katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="171b0-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="171b0-120">[Vytvoření ceníku](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="171b0-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="171b0-121">Konfigurace různých ceníků podle toho, kolik chcete účtovat klientům za každou roli, kterou jejich projekt vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="171b0-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="171b0-122">[Nastavení zdrojů](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="171b0-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="171b0-123">Přidání dovedností, odborných znalostí, rolí zdrojů a dalších informací o zdrojích, kterou budete pro vaše projekty potřebovat.</span><span class="sxs-lookup"><span data-stu-id="171b0-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="171b0-124">Viz také</span><span class="sxs-lookup"><span data-stu-id="171b0-124">See Also</span></span>  
 <span data-ttu-id="171b0-125">[Přehled Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="171b0-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="171b0-126">[Konfigurace Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="171b0-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="171b0-127">[Příručka pro manažera obchodních vztahů](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="171b0-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="171b0-128">[Příručka pro projektového manažera](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="171b0-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="171b0-129">[Příručka pro manažera zdrojů](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="171b0-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="171b0-130">Příručka – Čas, výdaje a spolupráce</span><span class="sxs-lookup"><span data-stu-id="171b0-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)