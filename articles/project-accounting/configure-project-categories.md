---
title: Konfigurace kategorií projektu
description: Toto téma obsahuje informace o nastavení kategorií projektu.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b7adf61a82714a0148d9c8b1d2b2b37fd611c1cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287500"
---
# <a name="configure-project-categories"></a><span data-ttu-id="59f4f-103">Konfigurace kategorií projektu</span><span class="sxs-lookup"><span data-stu-id="59f4f-103">Configure project categories</span></span>

<span data-ttu-id="59f4f-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="59f4f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="59f4f-105">Project Operations nabízí robustní funkce pro kategorizaci výnosů a nákladů na projekty.</span><span class="sxs-lookup"><span data-stu-id="59f4f-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="59f4f-106">Kategorie poskytují možnost reportovat a analyzovat transakce projektu a řídit účtování do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="59f4f-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="59f4f-107">Následující diagram ilustruje korelaci mezi kategoriemi transakcí, sdílenými kategoriemi a kategoriemi projektů.</span><span class="sxs-lookup"><span data-stu-id="59f4f-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="59f4f-108">Kategorie transakcí jsou základním seskupením transakcí projektu.</span><span class="sxs-lookup"><span data-stu-id="59f4f-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="59f4f-109">V rámci tohoto seskupení existuje sada sdílených kategorií, které lze sdílet mezi aplikacemi a moduly.</span><span class="sxs-lookup"><span data-stu-id="59f4f-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="59f4f-110">Když se dostaneme ještě dále ke konkrétnostem, kategorie projektů jsou nejpodrobnější úrovní kategorií.</span><span class="sxs-lookup"><span data-stu-id="59f4f-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="59f4f-111">Kategorie projektů jsou specifické pro právnické osoby, moduly a aplikace.</span><span class="sxs-lookup"><span data-stu-id="59f4f-111">Project categories are specific to legal entity, module, and application.</span></span>

![Korelace mezi kategoriemi transakcí, sdílenými kategoriemi a kategoriemi projektů.](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="59f4f-113">Kategorie transakcí</span><span class="sxs-lookup"><span data-stu-id="59f4f-113">Transaction categories</span></span>

<span data-ttu-id="59f4f-114">Kategorie transakcí představují základní seskupení pro projektové transakce a nejsou specifické pro společnost nebo typ transakce.</span><span class="sxs-lookup"><span data-stu-id="59f4f-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="59f4f-115">Společnost Contoso Robotics například používá ke seskupení transakcí projektu kategorie Design, Travel, Installation a Service Transaction.</span><span class="sxs-lookup"><span data-stu-id="59f4f-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="59f4f-116">Kategorie transakcí jsou definovány v modulu Project Operations.</span><span class="sxs-lookup"><span data-stu-id="59f4f-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="59f4f-117">Chcete-li otevřít formulář, přejděte na **Nastavení** \> **Kategorie transakcí**.</span><span class="sxs-lookup"><span data-stu-id="59f4f-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="59f4f-118">Vytvořte novou kategorii transakcí výběrem **Nový** nebo výběrem **Import z aplikace Excel**.</span><span class="sxs-lookup"><span data-stu-id="59f4f-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="59f4f-119">Sdílené kategorie</span><span class="sxs-lookup"><span data-stu-id="59f4f-119">Shared categories</span></span>

<span data-ttu-id="59f4f-120">Dynamics 365 používá koncept Sdílené kategorie ke kategorizaci výdajů v různých aplikacích, například Dynamics 365 Finance, Dynamics 365 Supply Chain a Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="59f4f-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="59f4f-121">Pro každou vytvořenou kategorii transakcí projektové operace automaticky vytvoří čtyři související sdílené kategorie: hodiny, výdaje, poplatky a položka.</span><span class="sxs-lookup"><span data-stu-id="59f4f-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="59f4f-122">Sdílené kategorie můžete zkontrolovat a upravit na **Řízení projektů a účetnictví** \> **Nastavit** \> **Kategorie** \> **Sdílené kategorie**.</span><span class="sxs-lookup"><span data-stu-id="59f4f-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="59f4f-123">Kategorie projektů</span><span class="sxs-lookup"><span data-stu-id="59f4f-123">Project categories</span></span>

<span data-ttu-id="59f4f-124">Kategorie projektu představují nejpodrobnější úroveň konfigurace kategorií a musí být nakonfigurovány samostatně a pro každou společnost účetním projektu.</span><span class="sxs-lookup"><span data-stu-id="59f4f-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="59f4f-125">Přejděte na **Řízení projektů a účetnictví** \> **Nastavit** \> **Kategorie** \> **Kategorie projektu**.</span><span class="sxs-lookup"><span data-stu-id="59f4f-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="59f4f-126">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="59f4f-126">Select **New**.</span></span>
3. <span data-ttu-id="59f4f-127">Vyberte **ID kategorie** sdílené kategorie, kterou jste vytvořili v předchozí části.</span><span class="sxs-lookup"><span data-stu-id="59f4f-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="59f4f-128">Project Operations umožňuje používat pouze ty sdílené kategorie, které jsou spojeny s kategoriemi transakcí.</span><span class="sxs-lookup"><span data-stu-id="59f4f-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="59f4f-129">Vyberte skupinu kategorií.</span><span class="sxs-lookup"><span data-stu-id="59f4f-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="59f4f-130">Skupiny kategorií</span><span class="sxs-lookup"><span data-stu-id="59f4f-130">Category groups</span></span>

<span data-ttu-id="59f4f-131">Skupiny kategorií se používají ke sdílení vlastností, zejména zveřejňování profilů, mezi souvisejícími kategoriemi projektu.</span><span class="sxs-lookup"><span data-stu-id="59f4f-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="59f4f-132">Pro každý typ transakce musí existovat alespoň jedna skupina kategorií a každé kategorii projektu je přiřazena skupina.</span><span class="sxs-lookup"><span data-stu-id="59f4f-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="59f4f-133">Specifikace účtování v Project Operations jsou definovány pravidly profilu nákladů a výnosů profilu projektu, kategoriemi projektů a skupinami kategorií.</span><span class="sxs-lookup"><span data-stu-id="59f4f-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="59f4f-134">Skupiny kategorií můžete nastavit přechodem na **Řízení projektů a účetnictví** \> **Nastavit** \> **Kategorie** \> **Skupiny kategorií**.</span><span class="sxs-lookup"><span data-stu-id="59f4f-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]