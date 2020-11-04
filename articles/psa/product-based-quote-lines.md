---
title: Řádky nabídky založené na produktu
description: Toto téma poskytuje informace o řádcích nabídky založených na produktu.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 55a5b5041a494892e6d96bf24e1bc132a26521dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073960"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="8c06d-103">Řádky nabídky založené na produktu</span><span class="sxs-lookup"><span data-stu-id="8c06d-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="8c06d-104">V aplikaci Dynamics 365 Project Service Automation můžete vytvořit řádky nabídky založené na produktu.</span><span class="sxs-lookup"><span data-stu-id="8c06d-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="8c06d-105">Řádky nabídky založené na produktu mohou být řádky „nezahrnutými do katalogu” nebo mohou být položkami z katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="8c06d-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="8c06d-106">Katalog produktů</span><span class="sxs-lookup"><span data-stu-id="8c06d-106">Product catalog</span></span>

<span data-ttu-id="8c06d-107">Produkty v katalogu produktů aplikace Dynamics 365 mají výchozí jednotku a skupinu jednotek.</span><span class="sxs-lookup"><span data-stu-id="8c06d-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="8c06d-108">Pokud několik produktů sdílí stejnou sadu atributů, můžete vytvořit produktovou řadu, která má také tyto atributy.</span><span class="sxs-lookup"><span data-stu-id="8c06d-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="8c06d-109">Všechny produkty v jedné produktové řadě dědí stejnou sadu atributů.</span><span class="sxs-lookup"><span data-stu-id="8c06d-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="8c06d-110">Společnost například prodává předplacené licence pro různé softwary.</span><span class="sxs-lookup"><span data-stu-id="8c06d-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="8c06d-111">Veškerý předplacený software má následující dva atributy:</span><span class="sxs-lookup"><span data-stu-id="8c06d-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="8c06d-112">Počet uživatelů</span><span class="sxs-lookup"><span data-stu-id="8c06d-112">Number of users</span></span> 
- <span data-ttu-id="8c06d-113">Doba trvání předplatného (v měsících)</span><span class="sxs-lookup"><span data-stu-id="8c06d-113">Subscription duration (in months)</span></span>

<span data-ttu-id="8c06d-114">Dobrým způsobem, jak udržovat tento typ katalogu, je vytvořit produktovou řadu s názvem **Předplatné softwaru** , která jako atributy obsahuje **Počet uživatelů** a **Doba trvání předplatného**.</span><span class="sxs-lookup"><span data-stu-id="8c06d-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software** , and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="8c06d-115">Poté můžete do produktové řady **Předplatné softwaru** přidat jednotlivé produkty, například **Dynamics 365 Sales** nebo **Dynamics 365 Field Service**.</span><span class="sxs-lookup"><span data-stu-id="8c06d-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="8c06d-116">Přidání položek katalogu produktů do projektové nabídky</span><span class="sxs-lookup"><span data-stu-id="8c06d-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="8c06d-117">Stránky projektová nabídka a projektová smlouva mají oddíly pro dva typy řádků: řádky založené na projektu a řádky založené na produktu.</span><span class="sxs-lookup"><span data-stu-id="8c06d-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="8c06d-118">Pro řádky založené na produktu se Dynamics 365 používá k přidávání položek z katalogu produktů do nabídky.</span><span class="sxs-lookup"><span data-stu-id="8c06d-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="8c06d-119">Rozevírací seznam na řádku nabídky nebo řádku projektové smlouvy obsahuje všechny produkty a jednotky v ceníku produktů, který je připojený k nabídce nebo projektové smlouvě.</span><span class="sxs-lookup"><span data-stu-id="8c06d-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="8c06d-120">Můžete také přidat produkty, které nejsou součástí ceníku produktů nabídky.</span><span class="sxs-lookup"><span data-stu-id="8c06d-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="8c06d-121">Dále můžete vybrat produkty z jiných ceníků nebo vybrat produkty přímo z katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="8c06d-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="8c06d-122">Vyberete-li produkt přímo z katalogu produktů, použije se pro získání prodejní ceny produktu výchozí ceník tohoto produktu.</span><span class="sxs-lookup"><span data-stu-id="8c06d-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="8c06d-123">Pokud není nastaven výchozí ceník, je cena nastavena na 0 (nulu).</span><span class="sxs-lookup"><span data-stu-id="8c06d-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="8c06d-124">Pokud je řádek poptávky založen na katalogu produktů, můžete přepsat prodejní cenu přímo na řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="8c06d-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="8c06d-125">Všimněte si, že řádek nabídky v Dynamics 365 obsahuje pole **Ocenění**.</span><span class="sxs-lookup"><span data-stu-id="8c06d-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="8c06d-126">K dispozici jsou dvě hodnoty:</span><span class="sxs-lookup"><span data-stu-id="8c06d-126">Two values are available:</span></span>

- <span data-ttu-id="8c06d-127">Přepsat ocenění</span><span class="sxs-lookup"><span data-stu-id="8c06d-127">Override pricing</span></span>  
- <span data-ttu-id="8c06d-128">Použít výchozí</span><span class="sxs-lookup"><span data-stu-id="8c06d-128">Use default</span></span>

<span data-ttu-id="8c06d-129">Pokud toto pole nastavíte na **Přepsat ocenění** , Dynamics 365 nenastaví výchozí cenu.</span><span class="sxs-lookup"><span data-stu-id="8c06d-129">If you set this field to **Override pricing** , Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="8c06d-130">Na řádku nabídky musíte zadat cenu produktu.</span><span class="sxs-lookup"><span data-stu-id="8c06d-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="8c06d-131">Pokud toto pole nastavíte na **Použít výchozí** , Dynamics 365 použije výchozí prodejní cenu a uzamkne pole, aby nedošlo k úpravám.</span><span class="sxs-lookup"><span data-stu-id="8c06d-131">If you set this field to **Use default** , Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="8c06d-132">Po instalaci PSA jsou do řádků na nabídce založených na produktu vloženy výchozí prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="8c06d-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="8c06d-133">Pole **Ocenění** je pak nastaveno na **Přepsat ocenění** , takže můžete upravit výchozí cenu na řádcích nabídky.</span><span class="sxs-lookup"><span data-stu-id="8c06d-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Nastavení přepisu ocenění](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="8c06d-135">Množstevní faktory pro výrobky</span><span class="sxs-lookup"><span data-stu-id="8c06d-135">Quantity factors for products</span></span>

<span data-ttu-id="8c06d-136">PSA používá množstevní faktory pro podporu prodeje produktů založených na předplatném.</span><span class="sxs-lookup"><span data-stu-id="8c06d-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="8c06d-137">U produktů založených na předplatném je množství v nabídce nebo na řádku projektové smlouvy vyjádřeno jako počet uživatelských měsíců.</span><span class="sxs-lookup"><span data-stu-id="8c06d-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="8c06d-138">Cena předplaceného softwaru je v katalogu obvykle uložena jako cena za uživatele za měsíc.</span><span class="sxs-lookup"><span data-stu-id="8c06d-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="8c06d-139">Místo toho však můžete použít jiné popisy času.</span><span class="sxs-lookup"><span data-stu-id="8c06d-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="8c06d-140">Během prodejního procesu je cena na řádku nabídky obvykle cena za uživatele za měsíc, která byla sjednána prodejním agentem IT a po uplatnění slevy.</span><span class="sxs-lookup"><span data-stu-id="8c06d-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="8c06d-141">Každá dohoda má různý počet uživatelů a různý počet měsíců předplatného.</span><span class="sxs-lookup"><span data-stu-id="8c06d-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="8c06d-142">Množství, které se používá k výpočtu částky řádku nabídky, je součin počtu uživatelů a počtu měsíců předplatného.</span><span class="sxs-lookup"><span data-stu-id="8c06d-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="8c06d-143">Za účelem podpory tohoto typu prodeje byl v PSA zaveden koncept množstevních faktorů.</span><span class="sxs-lookup"><span data-stu-id="8c06d-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="8c06d-144">Množstevní faktory závisí na atributech produktu v Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8c06d-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="8c06d-145">Při konfiguraci určitých vlastností produktu umožňuje PSA označit podmnožinu těchto vlastností nebo všechny vlastnosti jako množstevní faktory.</span><span class="sxs-lookup"><span data-stu-id="8c06d-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="8c06d-146">PSA ověřuje, zda jsou jako množstevní faktory označeny pouze numerické vlastnosti nebo vlastnosti produktu, které mají číselný datový typ.</span><span class="sxs-lookup"><span data-stu-id="8c06d-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="8c06d-147">Pokud je produkt, pro nějž jsou nakonfigurovány množstevní faktory, přidán k řádku nabídky, pole **Množství** na řádku nabídky se stane polem jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="8c06d-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="8c06d-148">Po zadání hodnot vlastností produktu, které jsou množstevními faktory, vypočítá PSA množství řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="8c06d-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="8c06d-149">Dynamics 365 může mít například následující vlastnosti:</span><span class="sxs-lookup"><span data-stu-id="8c06d-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="8c06d-150">**Poč. uživatelů** – počet uživatelů</span><span class="sxs-lookup"><span data-stu-id="8c06d-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="8c06d-151">**Poč. měsíců** – počet měsíců předplatného</span><span class="sxs-lookup"><span data-stu-id="8c06d-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="8c06d-152">**Jednotka SKU produktu**</span><span class="sxs-lookup"><span data-stu-id="8c06d-152">**Product SKU**</span></span> 

<span data-ttu-id="8c06d-153">Vlastnosti **Poč. uživatelů** a **Poč. měsíců** lze pomocí úpravy vlastností řádku produktu označit jako množstevní faktory.</span><span class="sxs-lookup"><span data-stu-id="8c06d-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Označení vlastností Poč. uživatelů a Poč. měsíců jako množstevní faktory](media/basic-guide-11.png)
 
