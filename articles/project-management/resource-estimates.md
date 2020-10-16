---
title: Odhady zdrojů
description: Toto téma poskytuje informace o tom, jak se počítají odhady zdrojů v aplikaci Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928552"
---
# <a name="resource-estimates"></a><span data-ttu-id="19833-103">Odhady zdrojů</span><span class="sxs-lookup"><span data-stu-id="19833-103">Resource estimates</span></span>

<span data-ttu-id="19833-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="19833-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="19833-105">Odhady zdrojů pocházejí z časově odstupňovaného úsilí, které je definováno ve strukturovaném rozpisu prací spolu s příslušnými cenovými dimenzemi.</span><span class="sxs-lookup"><span data-stu-id="19833-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="19833-106">Výpočet je obvykle prováděn podle vzorce **rychlost / hod pro každou roli x hodin.**</span><span class="sxs-lookup"><span data-stu-id="19833-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="19833-107">Časově odstupňované úsilí pro každý zdroj je uloženo v záznamu přiřazení zdroje.</span><span class="sxs-lookup"><span data-stu-id="19833-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="19833-108">Cena je uložena v předem definovaném ceníku.</span><span class="sxs-lookup"><span data-stu-id="19833-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="19833-109">Převod jednotek se použije na základě příslušného ceníku.</span><span class="sxs-lookup"><span data-stu-id="19833-109">Unit conversion is applied based on the applicable price list.</span></span>

![Odhady zdrojů](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="19833-111">Výchozí nákladová cena a měna nákladů</span><span class="sxs-lookup"><span data-stu-id="19833-111">Default cost price and cost currency</span></span>

<span data-ttu-id="19833-112">Výchozí hodnoty nákladových cen jsou převzaty z organizační jednotky.</span><span class="sxs-lookup"><span data-stu-id="19833-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="19833-113">Výchozí fakturační sazba a měna prodeje</span><span class="sxs-lookup"><span data-stu-id="19833-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="19833-114">Prodejní ceny se aplikují jednou za každý obchod.</span><span class="sxs-lookup"><span data-stu-id="19833-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="19833-115">Hierarchie výchozích prodejních ceníků je následující:</span><span class="sxs-lookup"><span data-stu-id="19833-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="19833-116">Organizace</span><span class="sxs-lookup"><span data-stu-id="19833-116">Organization</span></span>
2. <span data-ttu-id="19833-117">Zákazník</span><span class="sxs-lookup"><span data-stu-id="19833-117">Customer</span></span>
3. <span data-ttu-id="19833-118">Nabídka / smlouva</span><span class="sxs-lookup"><span data-stu-id="19833-118">Quote/contract</span></span>
