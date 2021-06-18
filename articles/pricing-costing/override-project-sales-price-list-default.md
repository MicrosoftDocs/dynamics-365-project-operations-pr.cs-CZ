---
title: Přepsání prodejních ceníků projektu
description: Tohle téma poskytuje informace o vytváření vlastních prodejních ceníků.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: db2ff6acaad6ab4cbcc98d3d5b06b36ed23b758f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995073"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="2020e-103">Přepsání prodejních ceníků projektu</span><span class="sxs-lookup"><span data-stu-id="2020e-103">Override project sales price lists</span></span>

<span data-ttu-id="2020e-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="2020e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="2020e-105">Projektový ceník konkrétního zákazníka</span><span class="sxs-lookup"><span data-stu-id="2020e-105">Customer-specific project price lists</span></span>

<span data-ttu-id="2020e-106">Cenové smlouvy konkrétních zákazníků lze nastavit jako projektové ceníky v záznamu obchodního vztahu v Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="2020e-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="2020e-107">Chcete-li nastavit projektový ceník konkrétního zákazníka, v oblasti **Prodej** přejděte k záznamu obchodního vztahu.</span><span class="sxs-lookup"><span data-stu-id="2020e-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="2020e-108">Otevřete stránku seznamu **Obchodní vztahy**.</span><span class="sxs-lookup"><span data-stu-id="2020e-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="2020e-109">Vyhledejte a poklepejte na záznam zákazníka a otevřete stránku s podrobnostmi **Obchodní vztah**.</span><span class="sxs-lookup"><span data-stu-id="2020e-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="2020e-110">Na kartě **Projektové ceníky** vyberte **+ Nový projektový ceník**.</span><span class="sxs-lookup"><span data-stu-id="2020e-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="2020e-111">Na stránce **Nový projektový ceník** vyberte z rozevíracího seznamu ceník.</span><span class="sxs-lookup"><span data-stu-id="2020e-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="2020e-112">Jsou zde pouze ceníky, jejichž kontext je nastaven na **Prodej** a jejichž měna odpovídá měně obchodního vztahu.</span><span class="sxs-lookup"><span data-stu-id="2020e-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="2020e-113">Pojmenujte přidružení a poté vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2020e-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="2020e-114">Vytvoří se projektový ceník konkrétního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="2020e-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="2020e-115">Tento ceník bude určovat výchozí projektové ceny u projektových nabídek nebo smluv vytvořených pro tohoto zákazníka, kde datum vytvoření projektové nabídky nebo smlouvy spadá do data účinnosti ceníku.</span><span class="sxs-lookup"><span data-stu-id="2020e-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="2020e-116">Vlastní ceny projektových nabídek</span><span class="sxs-lookup"><span data-stu-id="2020e-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="2020e-117">V případě projektových nabídek můžete mít ceny projektu, které začínají s výchozím standardním ceníkem vycházejícím z parametrů zákazníka nebo projektu.</span><span class="sxs-lookup"><span data-stu-id="2020e-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="2020e-118">Když potřebujete vlastní ceny za práci související s projektem pro konkrétní nabídku, můžete ji získat z přidružené entity projektových ceníků.</span><span class="sxs-lookup"><span data-stu-id="2020e-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="2020e-119">Provedením následujících kroků nastavíte ceny projektu pro konkrétní nabídku.</span><span class="sxs-lookup"><span data-stu-id="2020e-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="2020e-120">Otevřete projektovou nabídku a vyberte kartu **Projektové ceníky**.</span><span class="sxs-lookup"><span data-stu-id="2020e-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="2020e-121">V podmřížce vyberte **Vytvořit vlastní ceny**.</span><span class="sxs-lookup"><span data-stu-id="2020e-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="2020e-122">Všechny projektové ceníky, které jsou připojeny k nabídce, jsou zkopírovány do nových ceníků.</span><span class="sxs-lookup"><span data-stu-id="2020e-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="2020e-123">Názvy nových ceníků odrážejí název nabídky s razítkem data a času, kdy byly tyto ceníky vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="2020e-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="2020e-124">Můžete použít každý z těchto ceníků a aktualizovat ceny práce (cena role) a nákladů (cena kategorie).</span><span class="sxs-lookup"><span data-stu-id="2020e-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="2020e-125">Tyto ceny se budou vztahovat pouze na tuto projektovou nabídku.</span><span class="sxs-lookup"><span data-stu-id="2020e-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="2020e-126">Projektové ceníky na projektové smlouvě</span><span class="sxs-lookup"><span data-stu-id="2020e-126">Price lists on a project contract</span></span>

<span data-ttu-id="2020e-127">Na projektové smlouvě je cena projektu vždy výchozí jako vlastní ceník s názvem smlouvy a vytvořeným razítkem data a času připojeným k názvu.</span><span class="sxs-lookup"><span data-stu-id="2020e-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="2020e-128">To platí, ať už byla smlouva vytvořena při získání nabídky, nebo pokud byla smlouva vytvořena úplně od začátku.</span><span class="sxs-lookup"><span data-stu-id="2020e-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="2020e-129">V případě potřeby můžete toto přidružení k vlastnímu ceníku odebrat a místo toho přidružit standardní ceník k projektové smlouvě.</span><span class="sxs-lookup"><span data-stu-id="2020e-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="2020e-130">Když přidružíte standardní ceník k projektovým ceníkům nabídky nebo smlouvy, jakékoli změny provedené v cenách v ceníku ovlivní všechny nabídky a smlouvy, které používají ceník.</span><span class="sxs-lookup"><span data-stu-id="2020e-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]