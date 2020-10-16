---
title: Správa komplexních jednotek, jako jsou na uživatele nebo za měsíc pro řádky nabídek založené na produktu
description: Toto téma poskytuje informace o správě komplexních jednotek pro řádky nabídek založených na projektu.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965751"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a><span data-ttu-id="a81b2-103">Správa komplexních jednotek, jako jsou na uživatele nebo za měsíc pro řádky nabídek založené na produktu</span><span class="sxs-lookup"><span data-stu-id="a81b2-103">Managing complex units such as per-user, per-month for product-based quote lines</span></span>

<span data-ttu-id="a81b2-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="a81b2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a81b2-105">Dynamics 365 Project Operations používá množstevní faktory pro podporu prodeje produktů založených na předplatném.</span><span class="sxs-lookup"><span data-stu-id="a81b2-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="a81b2-106">U produktů založených na předplatném je množství v nabídce nebo na řádku projektové smlouvy vyjádřeno jako počet uživatelských měsíců.</span><span class="sxs-lookup"><span data-stu-id="a81b2-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="a81b2-107">Cena předplaceného softwaru je v katalogu obvykle uložena jako cena za uživatele za měsíc.</span><span class="sxs-lookup"><span data-stu-id="a81b2-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="a81b2-108">Během prodejního procesu je cena na řádku nabídky obvykle cena za uživatele za měsíc, která byla sjednána prodejním agentem IT a po uplatnění slevy.</span><span class="sxs-lookup"><span data-stu-id="a81b2-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="a81b2-109">Každá dohoda má různý počet uživatelů a různý počet měsíců předplatného.</span><span class="sxs-lookup"><span data-stu-id="a81b2-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="a81b2-110">Množství použité k výpočtu řádku nabídky je součin počtu uživatelů a počtu měsíců předplatného.</span><span class="sxs-lookup"><span data-stu-id="a81b2-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="a81b2-111">Za účelem podpory tohoto typu prodeje byl v Project Operations zaveden koncept množstevních faktorů.</span><span class="sxs-lookup"><span data-stu-id="a81b2-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="a81b2-112">Množstevní faktory závisí na atributech produktu v Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a81b2-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="a81b2-113">Při konfiguraci určitých vlastností produktu umožňuje Project Operations označit podmnožinu těchto vlastností nebo všechny vlastnosti jako množstevní faktory.</span><span class="sxs-lookup"><span data-stu-id="a81b2-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="a81b2-114">Project Operations ověřuje, zda jsou jako množstevní faktory označeny pouze numerické vlastnosti nebo vlastnosti produktu, které mají číselný datový typ.</span><span class="sxs-lookup"><span data-stu-id="a81b2-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="a81b2-115">Když do řádku nabídky přidáte produkt s množstevními faktory, pole **Množství** se zamkne pouze ke čtení.</span><span class="sxs-lookup"><span data-stu-id="a81b2-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="a81b2-116">Po zadání hodnot vlastností produktu, které jsou množstevními faktory, Project Operations vypočítá množství řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="a81b2-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="a81b2-117">Dynamics 365 Sales může mít například následující vlastnosti:</span><span class="sxs-lookup"><span data-stu-id="a81b2-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="a81b2-118">**Počet uživatelů**: počet uživatelů</span><span class="sxs-lookup"><span data-stu-id="a81b2-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="a81b2-119">**Poč. měsíců**: počet měsíců předplatného</span><span class="sxs-lookup"><span data-stu-id="a81b2-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="a81b2-120">**Jednotka SKU produktu**</span><span class="sxs-lookup"><span data-stu-id="a81b2-120">**Product SKU**</span></span>

<span data-ttu-id="a81b2-121">Vlastnosti **Počet uživatelů** a **Počet měsíců** můžete označit příznakem množstevní faktoru pomocí úpravy vlastností řádku produktu.</span><span class="sxs-lookup"><span data-stu-id="a81b2-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="a81b2-122">Chcete-li vytvořit kvantitativní faktory z vlastností produktu, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="a81b2-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="a81b2-123">V levém navigačním podokně Project Operations přejděte na nabídku **Prodej** > **Produkty**.</span><span class="sxs-lookup"><span data-stu-id="a81b2-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="a81b2-124">Otevřete produkt, pro který potřebujete konfigurovat množstevní faktory.</span><span class="sxs-lookup"><span data-stu-id="a81b2-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="a81b2-125">Ujistěte se, že produkt má již nakonfigurované vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="a81b2-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="a81b2-126">Na stránce **Informace o projektu** pro produkt vyberte kartu **Množstevní faktory**.</span><span class="sxs-lookup"><span data-stu-id="a81b2-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="a81b2-127">V podřízené mřížce vyberte položku **+ Nový výpočet pole**.</span><span class="sxs-lookup"><span data-stu-id="a81b2-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="a81b2-128">Zadejte název množstevního faktoru a vyberte hodnotu vlastnosti, která se mapuje na výpočet pole.</span><span class="sxs-lookup"><span data-stu-id="a81b2-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="a81b2-129">Uložte a zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="a81b2-129">Save and close the form.</span></span> <span data-ttu-id="a81b2-130">Opakujte tyto kroky pro všechny vlastnosti, které se mají použít pro výpočet množství pro řádek nabídky založené na produktu.</span><span class="sxs-lookup"><span data-stu-id="a81b2-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="a81b2-131">Když pro produkt vytvoříte řádek nabídky založené na produktu, množství řádku nabídky se uzamkne.</span><span class="sxs-lookup"><span data-stu-id="a81b2-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="a81b2-132">Množství bude vypočítáno jako součin hodnot vlastností, které zadáte pro daný řádek nabídky.</span><span class="sxs-lookup"><span data-stu-id="a81b2-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>
