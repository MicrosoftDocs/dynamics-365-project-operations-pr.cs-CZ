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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285835"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="99ba7-103">Proč je výchozí cena skutečných výdajových nákladů nastavena na nulu</span><span class="sxs-lookup"><span data-stu-id="99ba7-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="99ba7-104">Tyto často kladené dotazy se týkají skutečných výdajů, kde je třída transakce nastavena na Výdaje a typ transakce na Náklady.</span><span class="sxs-lookup"><span data-stu-id="99ba7-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="99ba7-105">Poradce při potížích s nákladovými sazbami na skutečných hodnotách výdajových nákladů</span><span class="sxs-lookup"><span data-stu-id="99ba7-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="99ba7-106">Přejděte na položku souvisejícího výdaje a ujistěte se, že je v poli položky výdajů částka.</span><span class="sxs-lookup"><span data-stu-id="99ba7-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="99ba7-107">Pokud původní položka výdajů nemá vyplněno pole částky, izolovali jste problém.</span><span class="sxs-lookup"><span data-stu-id="99ba7-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="99ba7-108">Chcete-li tento problém vyřešit, znovu vytvořte položku výdajů s platnou částkou a schvalte ji.</span><span class="sxs-lookup"><span data-stu-id="99ba7-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]