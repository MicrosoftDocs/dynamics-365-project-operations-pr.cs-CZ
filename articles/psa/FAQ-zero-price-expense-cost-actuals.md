---
title: Proč je výchozí cena skutečných prodejních výdajů a nákladů nastavena na nulu?
description: Odstranění problému, kdy je výchozí cena skutečných výdajových nákladů nastavena na nulu.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073801"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="5c30f-103">Proč je výchozí cena skutečných prodejních výdajů a nákladů nastavena na nulu?</span><span class="sxs-lookup"><span data-stu-id="5c30f-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5c30f-104">Tyto často kladené dotazy se týkají skutečných výdajů, kde je třída transakce nastavena na Výdaje a typ transakce na Náklady.</span><span class="sxs-lookup"><span data-stu-id="5c30f-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="5c30f-105">Poradce při potížích s nákladovými sazbami na skutečných hodnotách výdajových nákladů</span><span class="sxs-lookup"><span data-stu-id="5c30f-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="5c30f-106">Přejděte na položku souvisejícího výdaje a ujistěte se, že je v poli položky výdajů částka.</span><span class="sxs-lookup"><span data-stu-id="5c30f-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="5c30f-107">Pokud původní položka výdajů nemá vyplněno pole částky, izolovali jste problém.</span><span class="sxs-lookup"><span data-stu-id="5c30f-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="5c30f-108">Chcete-li tento problém vyřešit, znovu vytvořte položku výdajů s platnou částkou a schvalte ji.</span><span class="sxs-lookup"><span data-stu-id="5c30f-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
