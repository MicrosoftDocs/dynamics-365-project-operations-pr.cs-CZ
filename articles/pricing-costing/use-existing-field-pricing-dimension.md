---
title: Pole Project Operations jako cenové dimenze
description: Toto téma obsahuje informace o používání polí jako cenových dimenzí v Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a29460b2a9dc9a9755e7e28a6cd9712c6b06e8c6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004478"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="f0161-103">Pole Project Operations jako cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="f0161-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="f0161-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="f0161-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f0161-105">Entita **Skutečné hodnoty** má mnoho polí, která lze použít jako cenové dimenze pro ceny založené na zdrojích.</span><span class="sxs-lookup"><span data-stu-id="f0161-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="f0161-106">Například jedno společné pole je **Rezervovatelný zdroj**.</span><span class="sxs-lookup"><span data-stu-id="f0161-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="f0161-107">Menší společnosti, které mají méně než 20–30 fakturovatelných zdrojů, mohou zjistit, že mít sazby fakturace a nákladové sazby u jednotlivých zdrojů je jednodušší.</span><span class="sxs-lookup"><span data-stu-id="f0161-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="f0161-108">Jak však roste fakturovatelná pracovní síla, mohlo by se stát nerealistické udržovat sazby specifické pro zdroje.</span><span class="sxs-lookup"><span data-stu-id="f0161-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="f0161-109">Náklady na zdroje a fakturační sazby se začínají lišit, když se zdroje povyšují, získávají více zkušeností nebo získávají jinou sadu dovedností.</span><span class="sxs-lookup"><span data-stu-id="f0161-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="f0161-110">Dalším příkladem je kategorie transakce.</span><span class="sxs-lookup"><span data-stu-id="f0161-110">Another example is that of transaction category.</span></span> <span data-ttu-id="f0161-111">Zákazníci a implementátoři použili kategorii transakce ke klasifikaci práce a použití tohoto pole na cenu a náklady na základě kategorie práce.</span><span class="sxs-lookup"><span data-stu-id="f0161-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]