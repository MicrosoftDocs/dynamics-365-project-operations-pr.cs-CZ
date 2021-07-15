---
title: Přehled řádků smlouvy založené na produktu – omezený
description: Toto téma poskytuje informace o řádcích smlouvy založených na produktu.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8464eefbce9ba266360e10039e2a0be78982d8fa
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369728"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="00981-103">Přehled řádků smlouvy založené na produktu – omezený</span><span class="sxs-lookup"><span data-stu-id="00981-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="00981-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="00981-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="00981-105">V aplikaci Dynamics 365 Project Operations můžete vytvořit řádky smlouvy založené na produktu.</span><span class="sxs-lookup"><span data-stu-id="00981-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="00981-106">Řádky smlouvy založené na produktu mohou vytvořené ručně nebo mohou být položkami z katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="00981-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="00981-107">Katalog produktů</span><span class="sxs-lookup"><span data-stu-id="00981-107">Product catalog</span></span>

<span data-ttu-id="00981-108">Produkty v katalogu produktů aplikace mají výchozí jednotku a skupinu jednotek.</span><span class="sxs-lookup"><span data-stu-id="00981-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="00981-109">Pokud několik produktů sdílí stejnou sadu atributů, můžete vytvořit produktovou řadu, která má také tyto atributy.</span><span class="sxs-lookup"><span data-stu-id="00981-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="00981-110">Všechny produkty v jedné produktové řadě dědí stejnou sadu atributů.</span><span class="sxs-lookup"><span data-stu-id="00981-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="00981-111">Společnost například prodává předplacené licence pro různé druhy softwaru.</span><span class="sxs-lookup"><span data-stu-id="00981-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="00981-112">Veškerý předplacený software má následující dva atributy:</span><span class="sxs-lookup"><span data-stu-id="00981-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="00981-113">Počet uživatelů</span><span class="sxs-lookup"><span data-stu-id="00981-113">Number of users</span></span>
- <span data-ttu-id="00981-114">Doba trvání předplatného (v měsících)</span><span class="sxs-lookup"><span data-stu-id="00981-114">Subscription duration (in months)</span></span>

<span data-ttu-id="00981-115">Chcete-li udržovat tento typ katalogu, vytvořte produktovou řadu **Předplacený software**.</span><span class="sxs-lookup"><span data-stu-id="00981-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="00981-116">Přidejte do produktové řady atributy **Počet uživatelů** a **Délka předplatného**.</span><span class="sxs-lookup"><span data-stu-id="00981-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="00981-117">Poté přidejte jednotlivé produkty do produktové řady **Předplacený software**.</span><span class="sxs-lookup"><span data-stu-id="00981-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="00981-118">Přidání položek katalogu produktů do projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="00981-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="00981-119">Projektové smlouvy mají oddíly pro dva typy řádků: řádky založené na projektu a řádky založené na produktu.</span><span class="sxs-lookup"><span data-stu-id="00981-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="00981-120">Řádky založené na produktu zahrnují všechny produkty a jednotky uvedené v ceníku produktů ve smlouvě.</span><span class="sxs-lookup"><span data-stu-id="00981-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="00981-121">Můžete také přidat produkty, které nejsou součástí ceníku produktů smlouvy.</span><span class="sxs-lookup"><span data-stu-id="00981-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="00981-122">Produkty můžete vybrat z jiných ceníků nebo přímo z katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="00981-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="00981-123">Vyberete-li produkt přímo z katalogu produktů, prodejní cena produktu se vybere z výchozího ceníku produktu.</span><span class="sxs-lookup"><span data-stu-id="00981-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="00981-124">Pokud není nastaven výchozí ceník, je cena nastavena na 0 (nulu).</span><span class="sxs-lookup"><span data-stu-id="00981-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="00981-125">Pokud je řádek smlouvy založen na katalogu produktů, můžete přepsat prodejní cenu přímo v řádku.</span><span class="sxs-lookup"><span data-stu-id="00981-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="00981-126">Řádek smlouvy má pole **Ocenění** pole se dvěma hodnotami:</span><span class="sxs-lookup"><span data-stu-id="00981-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="00981-127">**Přepsat ocenění**</span><span class="sxs-lookup"><span data-stu-id="00981-127">**Override pricing**</span></span>
- <span data-ttu-id="00981-128">**Použít výchozí**</span><span class="sxs-lookup"><span data-stu-id="00981-128">**Use default**</span></span>

<span data-ttu-id="00981-129">Pokud pole **Ocenění** nastavíte na **Přepsat ocenění**, není výchozí cena nastavena.</span><span class="sxs-lookup"><span data-stu-id="00981-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="00981-130">Zadejte cenu produktu v řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="00981-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="00981-131">Pokud nastavíte pole na hodnotu **Použít výchozí**, použije se výchozí prodejní cena a pole nelze upravit.</span><span class="sxs-lookup"><span data-stu-id="00981-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="00981-132">Po instalaci Project Operations jsou do řádků smlouvy založených na produktu vloženy výchozí prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="00981-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="00981-133">Pole **Ocenění** je pak nastaveno na **Přepsat ocenění**, takže můžete upravit výchozí cenu na řádcích smlouvy.</span><span class="sxs-lookup"><span data-stu-id="00981-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="00981-134">Toto přepsání chování řádků založených je specifické pro Project Operations a odlišné vůči aplikaci Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="00981-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]