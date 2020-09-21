---
title: Použití existujícího pole ve službě Project Service jako cenové dimenze
description: Toto téma obsahuje informace o používání existujících polí Project Service jako cenových dimenzí.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: ed86e0c4-b2ea-4b3b-b9e3-cbfb3b512591
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: b280e2aeecc9d63fb65b77fad809edff817aff65
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750341"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="398f6-103">Použití existujícího pole ve službě Project Service jako cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="398f6-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="398f6-104">Project Service Automation (PSA) obsahuje mnoho polí v entitě **Skutečnosti**, která lze používat jako cenové dimenze pro tvorbu cen na základě zdrojů v organizacích projektů.</span><span class="sxs-lookup"><span data-stu-id="398f6-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="398f6-105">Například jedno společné pole je **Rezervovatelný zdroj**.</span><span class="sxs-lookup"><span data-stu-id="398f6-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="398f6-106">Menší společnosti, které mají méně než 20–30 fakturovatelných zdrojů, mohou zjistit, že mít sazby fakturace a nákladové sazby u jednotlivých zdrojů je jednodušší.</span><span class="sxs-lookup"><span data-stu-id="398f6-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="398f6-107">Avšak s tím, jak roste fakturovatelná pracovní síla, mohlo by být nereálné ji spravovat, protože nákladové sazby a sazby fakturace se začnou lišit po povýšení zdrojů, získání dalších zkušeností nebo jiných dovedností.</span><span class="sxs-lookup"><span data-stu-id="398f6-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="398f6-108">Vzhledem k tomu, že tento přístup stále funguje pro společnosti určité velikosti, podívejte se na téma [Použití rezervovatelného zdroje jako cenové dimenze](bookable-resource-pricing-dimension.md), abyste pochopili, jak lze existující pole Project Service použít jako cenovou dimenzi.</span><span class="sxs-lookup"><span data-stu-id="398f6-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="398f6-109">Dalším příkladem je kategorie transakce.</span><span class="sxs-lookup"><span data-stu-id="398f6-109">Another example is that of transaction category.</span></span> <span data-ttu-id="398f6-110">Zákazníci a implementátoři použili kategorii transakce ve skupině PSA ke klasifikaci práce a použití tohoto pole na cenu a náklady na základě kategorie práce.</span><span class="sxs-lookup"><span data-stu-id="398f6-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="398f6-111">Další informace naleznete v tématu [Použití kategorie transakce jako cenové dimenze](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="398f6-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
