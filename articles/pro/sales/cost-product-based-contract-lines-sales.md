---
title: Nákladové řádky smlouvy založené na produktu – omezené
description: Toto téma poskytuje informace o vytváření
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273685"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="ce486-103">Nákladové řádky smlouvy založené na produktu – omezené</span><span class="sxs-lookup"><span data-stu-id="ce486-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="ce486-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="ce486-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="ce486-105">Řádky smlouvy na základě produktu v Dynamics 365 Project Operations obsahují pole **Nákladová cena**, které ukládá nákladovou cenu produktu pro následné výpočty ziskovosti.</span><span class="sxs-lookup"><span data-stu-id="ce486-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="ce486-106">Když je pro katalogový produkt vytvořena produktový řádek smlouvy, náklady na řádek mají výchozí hodnoty z pole **Standardní náklady** v katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="ce486-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="ce486-107">Pole **Standardní náklad** v katalogu produktů je nastaveno v základní měně organizace.</span><span class="sxs-lookup"><span data-stu-id="ce486-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="ce486-108">Když jsou na řádku smlouvy výchozí jednotkové náklady, převedou se na měnu prodeje na smlouvě.</span><span class="sxs-lookup"><span data-stu-id="ce486-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="ce486-109">Jednotková cena na řádku smlouvy na základě produktu</span><span class="sxs-lookup"><span data-stu-id="ce486-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="ce486-110">Mít jednotkový náklad na řádku smlouvy na základě produktu umožňuje různé náklady na produkt pro každou jednotku.</span><span class="sxs-lookup"><span data-stu-id="ce486-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="ce486-111">I když to není vždy nutné, existují určité scénáře, kdy dodavatel může pro zákazníka zlevnit náklady na produkt.</span><span class="sxs-lookup"><span data-stu-id="ce486-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="ce486-112">Zvažte následující scénář:</span><span class="sxs-lookup"><span data-stu-id="ce486-112">Consider the following scenario:</span></span>

<span data-ttu-id="ce486-113">Fabrikam Robotics instaluje robotická ramena na montážní linky společnosti Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="ce486-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="ce486-114">Fabrikam poskytuje instalační služby, ale robotická ramena pocházejí od společnosti Trey Research.</span><span class="sxs-lookup"><span data-stu-id="ce486-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="ce486-115">Pokud instalace robotických ramen ve společnosti Adatum Corporation otevře novou průmyslovou vertikálu pro robotická ramena společnosti Trey Research, může poskytnout speciální slevu na tento kontrakt společnosti Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="ce486-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="ce486-116">V tomto případě Fabrikam vytvoří produktovou smlouvu pro Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="ce486-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="ce486-117">U této smlouvy se zadává jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="ce486-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="ce486-118">Cena se liší od nákladů na robotická ramena od společnosti Trey Research.</span><span class="sxs-lookup"><span data-stu-id="ce486-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]