---
title: Přehled řádků nabídky založené na produktu – omezený
description: Tohle téma poskytuje informace o práci s řádky nabídky na základě projektu.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369773"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="678b2-103">Přehled řádků nabídky založené na produktu – omezený</span><span class="sxs-lookup"><span data-stu-id="678b2-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="678b2-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="678b2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="678b2-105">V aplikaci Dynamics 365 Project Operations můžete vytvořit řádky nabídky založené na produktu.</span><span class="sxs-lookup"><span data-stu-id="678b2-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="678b2-106">Řádky nabídky založené na produktu mohou být ručně přidané nebo mohou být položkami z katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="678b2-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="678b2-107">Katalog produktů</span><span class="sxs-lookup"><span data-stu-id="678b2-107">Product catalog</span></span>

<span data-ttu-id="678b2-108">Každý produkt v katalogu produktů má výchozí jednotku a skupinu jednotek.</span><span class="sxs-lookup"><span data-stu-id="678b2-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="678b2-109">Pokud několik produktů sdílí stejnou sadu atributů, můžete vytvořit produktovou řadu, která sdílí tyto atributy.</span><span class="sxs-lookup"><span data-stu-id="678b2-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="678b2-110">Společnost například prodává předplacené licence pro různé druhy softwaru.</span><span class="sxs-lookup"><span data-stu-id="678b2-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="678b2-111">Veškerý předplacený software má následující dva atributy:</span><span class="sxs-lookup"><span data-stu-id="678b2-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="678b2-112">Počet uživatelů</span><span class="sxs-lookup"><span data-stu-id="678b2-112">Number of users</span></span>
- <span data-ttu-id="678b2-113">Doba trvání předplatného měřená v měsících</span><span class="sxs-lookup"><span data-stu-id="678b2-113">A subscription duration measured in months</span></span>

<span data-ttu-id="678b2-114">Chcete-li udržovat tento typ katalogu, vytvořte produktovou řadu s názvem **Předplatné softwaru** a jako atributy přidejte počet uživatelů a dobu trvání předplatného.</span><span class="sxs-lookup"><span data-stu-id="678b2-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="678b2-115">Dále můžete přidat jednotlivé produkty do produktové řady **Předplatné softwaru**.</span><span class="sxs-lookup"><span data-stu-id="678b2-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="678b2-116">Přidání položek katalogu produktů do projektové nabídky</span><span class="sxs-lookup"><span data-stu-id="678b2-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="678b2-117">Stránky **Projektová nabídka** a **Projektová smlouva** mají oddíly pro řádky založené na projektu a řádky založené na produktu.</span><span class="sxs-lookup"><span data-stu-id="678b2-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="678b2-118">V případě řádků založených na produktu zahrnuje rozevírací seznam na řádku nabídky nebo řádku projektové smlouvy všechny produkty a jednotky v produktovém ceníku.</span><span class="sxs-lookup"><span data-stu-id="678b2-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="678b2-119">Můžete také přidat produkty, které nejsou součástí produktového ceníku.</span><span class="sxs-lookup"><span data-stu-id="678b2-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="678b2-120">Dále můžete vybrat produkty z jiných ceníků nebo přímo z katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="678b2-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="678b2-121">Vyberete-li produkt přímo z katalogu produktů, použije se pro získání prodejní ceny produktu výchozí ceník tohoto produktu.</span><span class="sxs-lookup"><span data-stu-id="678b2-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="678b2-122">Pokud není nastaven výchozí ceník, je cena nastavena na nulu (0).</span><span class="sxs-lookup"><span data-stu-id="678b2-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="678b2-123">Pokud je řádek nabídky založen na katalogu produktů, můžete přepsat prodejní cenu přímo na řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="678b2-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="678b2-124">Řádek nabídky v poli **Ceny** se dvěma dostupnými hodnotami:</span><span class="sxs-lookup"><span data-stu-id="678b2-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="678b2-125">**Přepsat cenu**</span><span class="sxs-lookup"><span data-stu-id="678b2-125">**Override Pricing**</span></span>
- <span data-ttu-id="678b2-126">**Použít výchozí**</span><span class="sxs-lookup"><span data-stu-id="678b2-126">**Use Default**</span></span>

<span data-ttu-id="678b2-127">Pokud vyberete **Přepsat cenu**, výchozí cena není nastavena.</span><span class="sxs-lookup"><span data-stu-id="678b2-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="678b2-128">Místo toho musíte na řádku nabídky zadat cenu produktu.</span><span class="sxs-lookup"><span data-stu-id="678b2-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="678b2-129">Pokud vyberete **Použít výchozí**, použije se výchozí prodejní cena a pole je uzamčeno pro úpravy.</span><span class="sxs-lookup"><span data-stu-id="678b2-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="678b2-130">Do řádků nabídky založených na produktu jsou vloženy výchozí prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="678b2-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="678b2-131">Pole **Ceny** je pak nastaveno na **Přepsat cenu**, takže můžete upravit výchozí cenu na řádcích nabídky.</span><span class="sxs-lookup"><span data-stu-id="678b2-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="678b2-132">Toto je přepsání přímo pro Project Operations pro chování řádků založených na produktu v Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="678b2-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]