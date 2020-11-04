---
title: Řádky příležitosti založené na produktu
description: Toto téma poskytuje informace o položkách v řádcích příležitostí založených na produktu v aplikaci Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073706"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="f8918-103">Řádky příležitosti založené na produktu</span><span class="sxs-lookup"><span data-stu-id="f8918-103">Product-based opportunity lines</span></span>

<span data-ttu-id="f8918-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="f8918-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f8918-105">Řádky příležitostí založené na produktu jsou řádkové položky v příležitosti.</span><span class="sxs-lookup"><span data-stu-id="f8918-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="f8918-106">Tyto řádky jsou zákazníkovi dodávány jako samostatné řádkové položky na konečné faktuře bez dalších služeb s přidanou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="f8918-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="f8918-107">Přidružené výdaje a spotřeba se u úkolů souvisejících projektů nesledují.</span><span class="sxs-lookup"><span data-stu-id="f8918-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="f8918-108">Řádky založené na produktu mohou být katalogové položky nebo produkty nezahrnuté do katalogu.</span><span class="sxs-lookup"><span data-stu-id="f8918-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="f8918-109">Většina funkcí v řádcích příležitostí založených na produktu odpovídá funkcím poskytovaným aplikací Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="f8918-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="f8918-110">Další informace o řádcích příležitostí založených na produktu najdete v tématu [Přidání produktů k příležitosti](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="f8918-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="f8918-111">Jeden pojem vyskytující se v řádcích příležitostí založených na produktu, který je specifický pro příležitosti založené na projektu, je **Rozpočet zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="f8918-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="f8918-112">Toto pole slouží ke sledování částky, kterou je zákazník ochoten zaplatit za řádkovou položku.</span><span class="sxs-lookup"><span data-stu-id="f8918-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="f8918-113">Pokud je metoda výnosu souhrnu příležitostí nastavena na **Vypočteno systémem** , jsou hodnoty zákaznického rozpočtu napříč produktovými a projektovými řádky shrnuty pro výpočet odhadovaných výnosů.</span><span class="sxs-lookup"><span data-stu-id="f8918-113">If the revenue method of the Opportunity summary is set to **System Calculated** , the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
