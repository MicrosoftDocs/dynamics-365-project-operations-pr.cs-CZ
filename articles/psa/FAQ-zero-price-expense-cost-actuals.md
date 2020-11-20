---
title: Proč je výchozí cena skutečných prodejních výdajů a nákladů nastavena na nulu?
description: Odstranění problému, kdy je výchozí cena skutečných výdajových nákladů nastavena na nulu.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122110"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="6a3f0-103">Proč je výchozí cena skutečných prodejních výdajů a nákladů nastavena na nulu?</span><span class="sxs-lookup"><span data-stu-id="6a3f0-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6a3f0-104">Tyto často kladené dotazy se týkají skutečných výdajů, kde je třída transakce nastavena na Výdaje a typ transakce na Náklady.</span><span class="sxs-lookup"><span data-stu-id="6a3f0-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="6a3f0-105">Poradce při potížích s nákladovými sazbami na skutečných hodnotách výdajových nákladů</span><span class="sxs-lookup"><span data-stu-id="6a3f0-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="6a3f0-106">Přejděte na položku souvisejícího výdaje a ujistěte se, že je v poli položky výdajů částka.</span><span class="sxs-lookup"><span data-stu-id="6a3f0-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="6a3f0-107">Pokud původní položka výdajů nemá vyplněno pole částky, izolovali jste problém.</span><span class="sxs-lookup"><span data-stu-id="6a3f0-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="6a3f0-108">Chcete-li tento problém vyřešit, znovu vytvořte položku výdajů s platnou částkou a schvalte ji.</span><span class="sxs-lookup"><span data-stu-id="6a3f0-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
