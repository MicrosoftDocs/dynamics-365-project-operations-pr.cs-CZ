---
title: Přehled řádků smlouvy založené na produktu – omezený
description: Toto téma poskytuje informace o řádcích smlouvy založených na produktu.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb09140eae5383b882db73195d0360a836ece791
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177863"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="ee099-103">Přehled řádků smlouvy založené na produktu – omezený</span><span class="sxs-lookup"><span data-stu-id="ee099-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="ee099-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="ee099-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ee099-105">V Dynamics 365 Project Operations můžete vytvářet řádky smluv založené na produktu.</span><span class="sxs-lookup"><span data-stu-id="ee099-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="ee099-106">Řádky smlouvy založené na produktu mohou vytvořené ručně nebo mohou být položkami z katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="ee099-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="ee099-107">Katalog produktů</span><span class="sxs-lookup"><span data-stu-id="ee099-107">Product catalog</span></span>

<span data-ttu-id="ee099-108">Produkty v katalogu produktů aplikace mají výchozí jednotku a skupinu jednotek.</span><span class="sxs-lookup"><span data-stu-id="ee099-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="ee099-109">Pokud několik produktů sdílí stejnou sadu atributů, můžete vytvořit produktovou řadu, která má také tyto atributy.</span><span class="sxs-lookup"><span data-stu-id="ee099-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="ee099-110">Všechny produkty v jedné produktové řadě dědí stejnou sadu atributů.</span><span class="sxs-lookup"><span data-stu-id="ee099-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="ee099-111">Společnost například prodává předplacené licence pro různé druhy softwaru.</span><span class="sxs-lookup"><span data-stu-id="ee099-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="ee099-112">Veškerý předplacený software má následující dva atributy:</span><span class="sxs-lookup"><span data-stu-id="ee099-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="ee099-113">Počet uživatelů</span><span class="sxs-lookup"><span data-stu-id="ee099-113">Number of users</span></span>
- <span data-ttu-id="ee099-114">Doba trvání předplatného (v měsících)</span><span class="sxs-lookup"><span data-stu-id="ee099-114">Subscription duration (in months)</span></span>

<span data-ttu-id="ee099-115">Chcete-li udržovat tento typ katalogu, vytvořte produktovou řadu **Předplacený software**.</span><span class="sxs-lookup"><span data-stu-id="ee099-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="ee099-116">Přidejte do produktové řady atributy **Počet uživatelů** a **Délka předplatného**.</span><span class="sxs-lookup"><span data-stu-id="ee099-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="ee099-117">Poté přidejte jednotlivé produkty do produktové řady **Předplacený software**.</span><span class="sxs-lookup"><span data-stu-id="ee099-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="ee099-118">Přidání položek katalogu produktů do projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="ee099-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="ee099-119">Projektové smlouvy mají oddíly pro dva typy řádků: řádky založené na projektu a řádky založené na produktu.</span><span class="sxs-lookup"><span data-stu-id="ee099-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="ee099-120">Řádky založené na produktu zahrnují všechny produkty a jednotky uvedené v ceníku produktů ve smlouvě.</span><span class="sxs-lookup"><span data-stu-id="ee099-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="ee099-121">Můžete také přidat produkty, které nejsou součástí ceníku produktů smlouvy.</span><span class="sxs-lookup"><span data-stu-id="ee099-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="ee099-122">Produkty můžete vybrat z jiných ceníků nebo přímo z katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="ee099-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="ee099-123">Vyberete-li produkt přímo z katalogu produktů, prodejní cena produktu se vybere z výchozího ceníku produktu.</span><span class="sxs-lookup"><span data-stu-id="ee099-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="ee099-124">Pokud není nastaven výchozí ceník, je cena nastavena na 0 (nulu).</span><span class="sxs-lookup"><span data-stu-id="ee099-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="ee099-125">Pokud je řádek smlouvy založen na katalogu produktů, můžete přepsat prodejní cenu přímo v řádku.</span><span class="sxs-lookup"><span data-stu-id="ee099-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="ee099-126">Řádek smlouvy má pole **Ocenění** pole se dvěma hodnotami:</span><span class="sxs-lookup"><span data-stu-id="ee099-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="ee099-127">**Přepsat ocenění**</span><span class="sxs-lookup"><span data-stu-id="ee099-127">**Override pricing**</span></span>
- <span data-ttu-id="ee099-128">**Použít výchozí**</span><span class="sxs-lookup"><span data-stu-id="ee099-128">**Use default**</span></span>

<span data-ttu-id="ee099-129">Pokud pole **Ocenění** nastavíte na **Přepsat ocenění**, není výchozí cena nastavena.</span><span class="sxs-lookup"><span data-stu-id="ee099-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="ee099-130">Zadejte cenu produktu v řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="ee099-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="ee099-131">Pokud nastavíte pole na hodnotu **Použít výchozí**, použije se výchozí prodejní cena a pole nelze upravit.</span><span class="sxs-lookup"><span data-stu-id="ee099-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="ee099-132">Po instalaci Project Operations jsou do řádků smlouvy založených na produktu vloženy výchozí prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="ee099-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="ee099-133">Pole **Ocenění** je pak nastaveno na **Přepsat ocenění**, takže můžete upravit výchozí cenu na řádcích smlouvy.</span><span class="sxs-lookup"><span data-stu-id="ee099-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="ee099-134">Toto přepsání chování řádků založených je specifické pro Project Operations a odlišné vůči aplikaci Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="ee099-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
