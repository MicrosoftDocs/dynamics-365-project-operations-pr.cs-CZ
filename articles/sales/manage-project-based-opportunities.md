---
title: Správa příležitostí založených na projektech
description: Toto téma poskytuje informace o tom, jak pracovat s příležitostmi, které souvisejí s projekty.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ce9ad1458d338d63469c3d6fddb98b9cbbced31
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948367"
---
# <a name="manage-project-based-opportunities"></a><span data-ttu-id="7bd0d-103">Správa příležitostí založených na projektech</span><span class="sxs-lookup"><span data-stu-id="7bd0d-103">Manage project-based opportunities</span></span>

<span data-ttu-id="7bd0d-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="7bd0d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7bd0d-105">Projektové společnosti mají své doručovací činnosti obvykle rozložené do více zemí a geografických oblastí.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-105">Project-based companies typically have their operations for delivery spread across multiple countries and geographies.</span></span> <span data-ttu-id="7bd0d-106">Náklady na realizaci a dodání projektu se mohou lišit v závislosti na tom, která geografická oblast nebo divize řídí dodávku.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-106">The cost of the project execution and delivery can vary  based on which geography or division manages the delivery.</span></span> <span data-ttu-id="7bd0d-107">To pak může mít dopad na obchodní marže.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-107">In turn, this can impact the margins of the deal.</span></span> <span data-ttu-id="7bd0d-108">Poskytování služeb založených na projektu obvykle zahrnuje velké množství času vynaloženého lidskými zdroji, značné výdaje na cestování, náklady na materiál a další výdaje.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-108">Delivery of project-based services typically involves large quantities of human resource time, considerable expenses for travel, material costs, and other expenses.</span></span>

<span data-ttu-id="7bd0d-109">Příležitosti založené na projektu v Dynamics 365 Project Operations jsou navrženy s rozšířením příležitostí v Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-109">Project-based opportunities in Dynamics 365 Project Operations are designed with extensions to Dynamics 365 Sales.</span></span> <span data-ttu-id="7bd0d-110">Téma poskytuje podrobnosti o různých polích a obchodní logice obsažené v dalších funkcích, které jsou vyžadovány projektovými společnostmi ke správě příležitostí založených na projektu.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-110">The topic provides details about the different fields and business logic included in the additional functionality that is required by project-based companies to manage project-based opportunities.</span></span>

## <a name="view-all-project-based-opportunities"></a><span data-ttu-id="7bd0d-111">Zobrazení všech příležitostí založených na projektech</span><span class="sxs-lookup"><span data-stu-id="7bd0d-111">View all project-based opportunities</span></span>

<span data-ttu-id="7bd0d-112">Seznam všech příležitostí založených na projektech je uveden na stránce seznamu **Příležitost**.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-112">A list of all the project-based opportunities can be seen from the **Opportunity** list page.</span></span> 

1. <span data-ttu-id="7bd0d-113">Přejděte na **Prodej** > **Příležitosti**.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-113">Go to **Sales** > **Opportunities**.</span></span>
2. <span data-ttu-id="7bd0d-114">K výběru jiných filtrovaných pohledů na příležitosti použijte **Přepínač zobrazení** .</span><span class="sxs-lookup"><span data-stu-id="7bd0d-114">Use the **View switcher** to select other filtered views of the opportunities.</span></span> <span data-ttu-id="7bd0d-115">Můžete si vytvořit vlastní pohledy s vlastními kritérii filtru ke konfiguraci těchto zobrazení a možností navigace.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-115">You can create your own views with custom filter criteria to configure these views and navigation options.</span></span>

<span data-ttu-id="7bd0d-116">Na této stránce se seznamem nebo na stránce s podrobnostmi lze vytvářet nebo odstranit projektové příležitosti.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-116">Project Opportunities can be created or deleted from this list page or the detail page.</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="7bd0d-117">Tok obchodního procesu u obchodů založených na projektu</span><span class="sxs-lookup"><span data-stu-id="7bd0d-117">Business process flow for project-based deals</span></span>

<span data-ttu-id="7bd0d-118">Následující toky obchodního procesu jsou podporovány u obchodů založených na projektu v aplikaci Project Operations:</span><span class="sxs-lookup"><span data-stu-id="7bd0d-118">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="7bd0d-119">Obchodní proces od zájemce po příležitost</span><span class="sxs-lookup"><span data-stu-id="7bd0d-119">Lead to Opportunity business process</span></span>
- <span data-ttu-id="7bd0d-120">Prodejní proces příležitosti</span><span class="sxs-lookup"><span data-stu-id="7bd0d-120">Opportunity sales process</span></span>

### <a name="lead-to-opportunity-business-process"></a><span data-ttu-id="7bd0d-121">Obchodní proces od zájemce po příležitost</span><span class="sxs-lookup"><span data-stu-id="7bd0d-121">Lead to opportunity business process</span></span> 
<span data-ttu-id="7bd0d-122">Obchodní proces od zájemce po příležitost podporuje následující fáze:</span><span class="sxs-lookup"><span data-stu-id="7bd0d-122">The lead to opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="7bd0d-123">Fáze</span><span class="sxs-lookup"><span data-stu-id="7bd0d-123">Stage</span></span> | <span data-ttu-id="7bd0d-124">Mapovaná entita</span><span class="sxs-lookup"><span data-stu-id="7bd0d-124">Mapped entity</span></span> | <span data-ttu-id="7bd0d-125">Funkce</span><span class="sxs-lookup"><span data-stu-id="7bd0d-125">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7bd0d-126">Zařadit</span><span class="sxs-lookup"><span data-stu-id="7bd0d-126">Qualify</span></span> | <span data-ttu-id="7bd0d-127">Potenciální zákazník</span><span class="sxs-lookup"><span data-stu-id="7bd0d-127">Lead</span></span> | <span data-ttu-id="7bd0d-128">Zařazením zájemce vytvoříte účet, kontaktní osobu nebo příležitost.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-128">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="7bd0d-129">Vytvořit</span><span class="sxs-lookup"><span data-stu-id="7bd0d-129">Develop</span></span> | <span data-ttu-id="7bd0d-130">Příležitost</span><span class="sxs-lookup"><span data-stu-id="7bd0d-130">Opportunity</span></span> | <span data-ttu-id="7bd0d-131">Vypracováním příležitosti přidáte další informace o provedené práci, klíčových účastnících a konkurenci.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-131">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="7bd0d-132">Navrhnout</span><span class="sxs-lookup"><span data-stu-id="7bd0d-132">Propose</span></span> | <span data-ttu-id="7bd0d-133">Příležitost</span><span class="sxs-lookup"><span data-stu-id="7bd0d-133">Opportunity</span></span> | <span data-ttu-id="7bd0d-134">Vypracujte návrh a získejte souhlas od interního kontrolního týmu.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-134">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="7bd0d-135">Uzavřeno</span><span class="sxs-lookup"><span data-stu-id="7bd0d-135">Close</span></span> | <span data-ttu-id="7bd0d-136">Příležitost</span><span class="sxs-lookup"><span data-stu-id="7bd0d-136">Opportunity</span></span> | <span data-ttu-id="7bd0d-137">Vyhrajte příležitost uzavřít obchod.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-137">Win the opportunity to close the deal.</span></span> |

### <a name="opportunity-sales-process"></a><span data-ttu-id="7bd0d-138">Prodejní proces příležitosti</span><span class="sxs-lookup"><span data-stu-id="7bd0d-138">Opportunity sales process</span></span>
<span data-ttu-id="7bd0d-139">Prodejní proces příležitosti v Project Operations je rozšířením obchodního toku prodejního procesu příležitosti v aplikaci Sales.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-139">The Opportunity sales process in Project Operations is an extension to the Opportunity sales process business flow in the Sales application.</span></span> <span data-ttu-id="7bd0d-140">Tento obchodní proces je navržen tak, aby podporoval následující fáze v příležitosti založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-140">This business process is designed out-of-the-box to support the following stages in a project-based opportunity.</span></span>

| <span data-ttu-id="7bd0d-141">Fáze</span><span class="sxs-lookup"><span data-stu-id="7bd0d-141">Stage</span></span> | <span data-ttu-id="7bd0d-142">Mapovaná entita</span><span class="sxs-lookup"><span data-stu-id="7bd0d-142">Mapped entity</span></span> | <span data-ttu-id="7bd0d-143">Funkce</span><span class="sxs-lookup"><span data-stu-id="7bd0d-143">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7bd0d-144">Zařadit</span><span class="sxs-lookup"><span data-stu-id="7bd0d-144">Qualify</span></span> | <span data-ttu-id="7bd0d-145">Příležitost</span><span class="sxs-lookup"><span data-stu-id="7bd0d-145">Opportunity</span></span> | <span data-ttu-id="7bd0d-146">Zařazením zájemce vytvoříte účet, kontaktní osobu nebo příležitost.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-146">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="7bd0d-147">Navrhnout</span><span class="sxs-lookup"><span data-stu-id="7bd0d-147">Propose</span></span> | <span data-ttu-id="7bd0d-148">Nabídka</span><span class="sxs-lookup"><span data-stu-id="7bd0d-148">Quote</span></span> | <span data-ttu-id="7bd0d-149">Vypracujte návrh pomocí projektových nabídek a získejte souhlas od interního kontrolního týmu.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-149">Develop the proposal using project quotes and get approval from the internal review team.</span></span> |
| <span data-ttu-id="7bd0d-150">Smlouva</span><span class="sxs-lookup"><span data-stu-id="7bd0d-150">Contract</span></span> | <span data-ttu-id="7bd0d-151">Projektová smlouva</span><span class="sxs-lookup"><span data-stu-id="7bd0d-151">Project Contract</span></span> | <span data-ttu-id="7bd0d-152">Vyhrajte nabídku, vytvořte smlouvu a začněte s realizací a dodávkou projektu.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-152">Win the quote to create the contract and begin execution and delivery on the project.</span></span> |
| <span data-ttu-id="7bd0d-153">Uzavřeno</span><span class="sxs-lookup"><span data-stu-id="7bd0d-153">Close</span></span> | <span data-ttu-id="7bd0d-154">Projektová smlouva</span><span class="sxs-lookup"><span data-stu-id="7bd0d-154">Project Contract</span></span> | <span data-ttu-id="7bd0d-155">Úspěšně dokončete práci a uzavřete projektovou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-155">Finish the work successfully and close the project contract.</span></span> |

> [!NOTE]
> <span data-ttu-id="7bd0d-156">Pokud vaše projektová dohoda začala zájemcem, má přednost obchodní proces od zájemce po příležitost.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-156">If your project-based deal started with a Lead, the Lead to Opportunity business process takes precedence.</span></span>
>
> <span data-ttu-id="7bd0d-157">Pokud vaše projektová dohoda začala příležitostí, má přednost prodejní proces příležitosti.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-157">If your project-based deal started with an Opportunity, the Opportunity sales process takes precedence.</span></span>

<span data-ttu-id="7bd0d-158">Můžete upravit tok obchodního procesu produktu nebo vytvořit vlastní toky obchodního procesu a podle potřeby sledovat prodejní proces.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-158">You can edit the product business process flow or create your own business process flows to track your sales process as needed.</span></span> <span data-ttu-id="7bd0d-159">Další informace o toku obchodního procesu naleznete v tématu [Přehled toků obchodního procesu](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span><span class="sxs-lookup"><span data-stu-id="7bd0d-159">For more information about the business process flow, see [Business process flows overview](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]