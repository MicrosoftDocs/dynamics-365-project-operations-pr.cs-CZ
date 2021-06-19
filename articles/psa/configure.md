---
title: Konfigurace Project Service Automation
description: Postup konfigurace Project Service
author: ruhercul
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
ms.openlocfilehash: ef1724bb92e62ae21472e133fff0978c4faeeffa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002818"
---
# <a name="configure-project-service"></a><span data-ttu-id="b0eaa-103">Konfigurace Project Service</span><span class="sxs-lookup"><span data-stu-id="b0eaa-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b0eaa-104">Než budete moci používat možnosti automatizace [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v aplikaci [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] ke správě obchodních vztahů, projektů a zdrojů, musíte provést několik kroků konfigurace, abyste zajistili, že bude řešení [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vyhovovat potřebám vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="b0eaa-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="b0eaa-105">Mezi tyto kroky patří:</span><span class="sxs-lookup"><span data-stu-id="b0eaa-105">These steps include:</span></span>  
  
-   <span data-ttu-id="b0eaa-106">[Nastavení časových jednotek](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="b0eaa-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="b0eaa-107">Konfigurace časových jednotek v katalogu výrobků, které použijete jako základ pro plánování a fakturování projektů.</span><span class="sxs-lookup"><span data-stu-id="b0eaa-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="b0eaa-108">[Nastavení měny a směnných kurzů](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="b0eaa-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="b0eaa-109">Nastavení měny pro použití v projektech.</span><span class="sxs-lookup"><span data-stu-id="b0eaa-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="b0eaa-110">[Vytvoření organizačních jednotek](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="b0eaa-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="b0eaa-111">Nastavení skupin, které vaše společnost používá k rozdělení své činnosti, například podle geografických vlastností, obchodní funkce nebo jiného logického dělení.</span><span class="sxs-lookup"><span data-stu-id="b0eaa-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="b0eaa-112">[Nastavení četnosti faktur](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="b0eaa-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="b0eaa-113">Nastavení časových období, která chcete použít pro fakturování klientů.</span><span class="sxs-lookup"><span data-stu-id="b0eaa-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="b0eaa-114">[Konfigurace kategorií transakcí](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="b0eaa-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="b0eaa-115">Nastavení kategorií transakcí, podle kterých mohou vaši konzultanti jejich účtovat fakturovatelné a nefakturovatelné výdaje.</span><span class="sxs-lookup"><span data-stu-id="b0eaa-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="b0eaa-116">[Konfigurace kategorií výdajů](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="b0eaa-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="b0eaa-117">Nastavení kategorií, podle kterých mohou vaši konzultanti jejich účtovat fakturovatelné a nefakturovatelné výdaje.</span><span class="sxs-lookup"><span data-stu-id="b0eaa-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="b0eaa-118">[Vytvoření položek katalogu produktů](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="b0eaa-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="b0eaa-119">Přidání produktů, které prodáváte, například licencí na software, do katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="b0eaa-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="b0eaa-120">[Vytvoření ceníku](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="b0eaa-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="b0eaa-121">Konfigurace různých ceníků podle toho, kolik chcete účtovat klientům za každou roli, kterou jejich projekt vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="b0eaa-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="b0eaa-122">[Nastavení zdrojů](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="b0eaa-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="b0eaa-123">Přidání dovedností, odborných znalostí, rolí zdrojů a dalších informací o zdrojích, kterou budete pro vaše projekty potřebovat.</span><span class="sxs-lookup"><span data-stu-id="b0eaa-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b0eaa-124">Viz také</span><span class="sxs-lookup"><span data-stu-id="b0eaa-124">See Also</span></span>  
 <span data-ttu-id="b0eaa-125">[Přehled Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="b0eaa-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="b0eaa-126">[Konfigurace Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="b0eaa-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="b0eaa-127">[Příručka pro manažera obchodních vztahů](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="b0eaa-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="b0eaa-128">[Příručka pro projektového manažera](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="b0eaa-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="b0eaa-129">[Příručka pro manažera zdrojů](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="b0eaa-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="b0eaa-130">Příručka – Čas, výdaje a spolupráce</span><span class="sxs-lookup"><span data-stu-id="b0eaa-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]