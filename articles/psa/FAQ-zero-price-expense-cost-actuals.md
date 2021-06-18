---
title: Proč je výchozí cena skutečných prodejních výdajů a nákladů nastavena na nulu?
description: Odstranění problému, kdy je výchozí cena skutečných výdajových nákladů nastavena na nulu.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 03c958635dec66b0f243872dfb929eba6a20119b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992692"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="5769d-103">Proč je výchozí cena skutečných výdajových nákladů nastavena na nulu</span><span class="sxs-lookup"><span data-stu-id="5769d-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5769d-104">Tyto často kladené dotazy se týkají skutečných výdajů, kde je třída transakce nastavena na Výdaje a typ transakce na Náklady.</span><span class="sxs-lookup"><span data-stu-id="5769d-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="5769d-105">Poradce při potížích s nákladovými sazbami na skutečných hodnotách výdajových nákladů</span><span class="sxs-lookup"><span data-stu-id="5769d-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="5769d-106">Přejděte na položku souvisejícího výdaje a ujistěte se, že je v poli položky výdajů částka.</span><span class="sxs-lookup"><span data-stu-id="5769d-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="5769d-107">Pokud původní položka výdajů nemá vyplněno pole částky, izolovali jste problém.</span><span class="sxs-lookup"><span data-stu-id="5769d-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="5769d-108">Chcete-li tento problém vyřešit, znovu vytvořte položku výdajů s platnou částkou a schvalte ji.</span><span class="sxs-lookup"><span data-stu-id="5769d-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]