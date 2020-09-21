---
title: Analýza projektových nabídek
description: Toto téma poskytuje informace o analýze projektových nabídek.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 57ac8407-26f5-49dd-97ea-e97642789ff5
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 63c826d27863df62301ec1548fdc94158220c3a2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750276"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="b6b06-103">Analýza projektových nabídek</span><span class="sxs-lookup"><span data-stu-id="b6b06-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b6b06-104">Dynamics 365 Project Service Automation analyzuje nabídky projektů za účelem odhadu ziskovosti.</span><span class="sxs-lookup"><span data-stu-id="b6b06-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="b6b06-105">Analyzuje také, v jaké míře je nabídka v souladu s očekáváními zákazníka o datu dodání nebo datu dokončení a o rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="b6b06-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="b6b06-106">Analýza ziskovosti</span><span class="sxs-lookup"><span data-stu-id="b6b06-106">Profitability analysis</span></span>

<span data-ttu-id="b6b06-107">Project Service Automation analyzuje ziskovost pomocí hrubého marže a upravené hrubé marže.</span><span class="sxs-lookup"><span data-stu-id="b6b06-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="b6b06-108">Hrubé marže se vypočítají pomocí následujícího vzorce:</span><span class="sxs-lookup"><span data-stu-id="b6b06-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="b6b06-109">Upravená hrubá marže se vypočítá pomocí následujícího vzorce:</span><span class="sxs-lookup"><span data-stu-id="b6b06-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="b6b06-110">Je-li rozdíl hrubé marže a upravené hrubé marže obrovský, je velká část práce v nabídce klasifikována jako nefakturovatelná.</span><span class="sxs-lookup"><span data-stu-id="b6b06-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="b6b06-111">Analýza očekávání zákazníka</span><span class="sxs-lookup"><span data-stu-id="b6b06-111">Analysis of customer expectations</span></span>

<span data-ttu-id="b6b06-112">Pokud zadáte hodnoty do následujících polí, můžete analyzovat nabídky a generovat grafy pro očekávání zákazníka týkající se plánu a rozpočtu:</span><span class="sxs-lookup"><span data-stu-id="b6b06-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="b6b06-113">Pole **Požadované datum dodávky** v záhlaví nabídky.</span><span class="sxs-lookup"><span data-stu-id="b6b06-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="b6b06-114">Pole **Rozpočet zákazníka** pro každý řádek nabídky (pro řádky založené na projektu a řádky založené na produktu).</span><span class="sxs-lookup"><span data-stu-id="b6b06-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="b6b06-115">Analýza očekávání zákazníka týkající se plánu je provedena porovnáním nejpozdějšího koncového data podrobnosti řádku nabídky s požadovaným datem dodání na všech řádcích nabídky v nabídce.</span><span class="sxs-lookup"><span data-stu-id="b6b06-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="b6b06-116">Analýza očekávání zákazníka týkající se rozpočtu je provedena porovnáním součtu celkového rozpočtu zákazníka s nabízenou částkou na všech řádcích nabídky.</span><span class="sxs-lookup"><span data-stu-id="b6b06-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
