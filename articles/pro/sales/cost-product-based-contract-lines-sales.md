---
title: Nákladové řádky smlouvy založené na produktu
description: Toto téma poskytuje informace o vytváření
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/20/2020
ms.locfileid: "4074011"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="c651e-103">Nákladové řádky smlouvy založené na produktu</span><span class="sxs-lookup"><span data-stu-id="c651e-103">Costing product-based contract lines</span></span>

<span data-ttu-id="c651e-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="c651e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c651e-105">Řádky smlouvy na základě produktu v Dynamics 365 Project Operations zahrnují pole **Nákladová cena** , kam se ukládá nákladová cena produktu pro následné výpočty ziskovosti.</span><span class="sxs-lookup"><span data-stu-id="c651e-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="c651e-106">Když je pro katalogový produkt vytvořen řádek smlouvy založené na produktu, náklady na řádek smlouvy založené na produktu jsou ve výchozím stavu přebírány z pole **Standardní náklady** v katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="c651e-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="c651e-107">Pole **Standardní náklad** v katalogu produktů je nastaveno v základní měně organizace.</span><span class="sxs-lookup"><span data-stu-id="c651e-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="c651e-108">Když jsou na řádku smlouvy výchozí jednotkové náklady, převedou se na měnu prodeje na smlouvě.</span><span class="sxs-lookup"><span data-stu-id="c651e-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="c651e-109">Jednotková cena na řádku smlouvy na základě produktu</span><span class="sxs-lookup"><span data-stu-id="c651e-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="c651e-110">Mít jednotkový náklad na řádku smlouvy na základě produktu umožňuje různé náklady na produkt pro každou jednotku.</span><span class="sxs-lookup"><span data-stu-id="c651e-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="c651e-111">I když to není vždy nutné, existují určité scénáře, kdy dodavatel může pro zákazníka zlevnit náklady na produkt.</span><span class="sxs-lookup"><span data-stu-id="c651e-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="c651e-112">Zvažte následující scénář:</span><span class="sxs-lookup"><span data-stu-id="c651e-112">Consider the following scenario:</span></span>

<span data-ttu-id="c651e-113">Fabrikam Robotics instaluje robotická ramena na montážní linky společnosti Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="c651e-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="c651e-114">Fabrikam poskytuje instalační služby, ale robotická ramena jsou získávána z Trey Research.</span><span class="sxs-lookup"><span data-stu-id="c651e-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="c651e-115">Pokud instalace robotických ramen ve společnosti Adatum Corporation otevře novou průmyslovou vertikálu pro robotická ramena společnosti Trey Research, může poskytnout speciální slevu na tento kontrakt společnosti Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="c651e-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="c651e-116">V tomto případě Fabrikam vytvoří řádek smlouvy na základě produktu pro Robotic Arms a zadá jednotkové náklady na tuto smlouvu, které se liší od standardních nákladů na robotická ramena od Trey Research.</span><span class="sxs-lookup"><span data-stu-id="c651e-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
