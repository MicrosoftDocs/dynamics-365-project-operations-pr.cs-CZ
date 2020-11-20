---
title: Správa komplexních jednotek pro řádky smlouvy založené na produktu – omezené
description: Tohle téma poskytuje informace o podpoře prodeje produktů založených na předplatném.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177368"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="3678c-103">Správa komplexních jednotek pro řádky smlouvy založené na produktu – omezené</span><span class="sxs-lookup"><span data-stu-id="3678c-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="3678c-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="3678c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3678c-105">Dynamics 365 Project Operations používá množstevní faktory pro podporu prodeje produktů založených na předplatném.</span><span class="sxs-lookup"><span data-stu-id="3678c-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="3678c-106">U produktů založených na předplatném je množství ve smlouvě nebo na řádku projektové smlouvy vyjádřeno jako počet uživatelských měsíců.</span><span class="sxs-lookup"><span data-stu-id="3678c-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="3678c-107">Cena předplaceného softwaru je v katalogu uložena jako cena za uživatele za měsíc.</span><span class="sxs-lookup"><span data-stu-id="3678c-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="3678c-108">Během prodejního procesu je cena na řádku smlouvy obvykle cena za uživatele za měsíc, která byla sjednána prodejním agentem a po uplatnění slevy.</span><span class="sxs-lookup"><span data-stu-id="3678c-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="3678c-109">Každá dohoda má různý počet uživatelů a různý počet měsíců předplatného.</span><span class="sxs-lookup"><span data-stu-id="3678c-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="3678c-110">Množství, které se používá k výpočtu částky řádku smlouvy, je součin počtu uživatelů a počtu měsíců předplatného.</span><span class="sxs-lookup"><span data-stu-id="3678c-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="3678c-111">Za účelem podpory tohoto typu prodeje podporuje Project Operations koncept *množstevních faktorů*.</span><span class="sxs-lookup"><span data-stu-id="3678c-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="3678c-112">Množstevní faktory závisí na atributech produktu.</span><span class="sxs-lookup"><span data-stu-id="3678c-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="3678c-113">Při konfiguraci určitých vlastností produktu můžete označit podmnožinu těchto vlastností nebo všechny vlastnosti jako množstevní faktory.</span><span class="sxs-lookup"><span data-stu-id="3678c-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="3678c-114">Project Operations ověřuje, zda jsou jako množstevní faktory označeny pouze numerické vlastnosti nebo vlastnosti produktu, které mají číselný datový typ.</span><span class="sxs-lookup"><span data-stu-id="3678c-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="3678c-115">Když je produkt s konfigurovanými množstevními faktory přidán do řádku smlouvy, pole **Množství** se stane jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="3678c-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="3678c-116">Po zadání hodnot vlastností produktu, které jsou množstevními faktory, Project Operations vypočítá množství řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="3678c-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="3678c-117">Dynamics 365 Sales může mít například následující vlastnosti:</span><span class="sxs-lookup"><span data-stu-id="3678c-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="3678c-118">**Počet uživatelů**: počet uživatelů.</span><span class="sxs-lookup"><span data-stu-id="3678c-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="3678c-119">**Poč. měsíců**: počet měsíců předplatného.</span><span class="sxs-lookup"><span data-stu-id="3678c-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="3678c-120">**SKU produktu**: skladová jednotka (SKU) pro produkt.</span><span class="sxs-lookup"><span data-stu-id="3678c-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="3678c-121">Vlastnosti **Počet uživatelů** a **Počet měsíců** lze pomocí úpravy vlastností řádku produktu označit jako množstevní faktory.</span><span class="sxs-lookup"><span data-stu-id="3678c-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="3678c-122">Chcete-li z vlastností produktu vytvořit množstevní faktory, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="3678c-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="3678c-123">Na stránce **Project Operations** vyberte **Prodej – produkty**.</span><span class="sxs-lookup"><span data-stu-id="3678c-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="3678c-124">Otevřete produkt, pro který potřebujete nastavit množstevní faktory.</span><span class="sxs-lookup"><span data-stu-id="3678c-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="3678c-125">Ujistěte se, že produkt má již nastavené vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="3678c-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="3678c-126">Na stránce **Informace o projektu** vyberte stránku kartu **Množstevní faktory**.</span><span class="sxs-lookup"><span data-stu-id="3678c-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="3678c-127">V podřízené mřížce vyberte položku **+ Nový výpočet pole**.</span><span class="sxs-lookup"><span data-stu-id="3678c-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="3678c-128">Zadejte název **množstevního faktoru** a vyberte hodnotu vlastnosti, která se mapuje na výpočet pole.</span><span class="sxs-lookup"><span data-stu-id="3678c-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="3678c-129">Uložte a zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="3678c-129">Save and close the form.</span></span>
7. <span data-ttu-id="3678c-130">Opakujte kroky 2–6 pro všechny vlastnosti, které společně tvoří množství pro řádek smlouvy na základě produktu.</span><span class="sxs-lookup"><span data-stu-id="3678c-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="3678c-131">S nastavenými množstevními faktory, když uživatel vytvoří pro tento produkt řádek kontraktu, je množství řádku smlouvy uzamčeno.</span><span class="sxs-lookup"><span data-stu-id="3678c-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="3678c-132">Množství se poté vypočítá jako produkt hodnot vlastností pro daný řádek smlouvy.</span><span class="sxs-lookup"><span data-stu-id="3678c-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>
