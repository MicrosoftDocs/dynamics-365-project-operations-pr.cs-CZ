---
title: Nákladové řádky nabídky založené na produktu
description: Toto téma poskytuje informace o použití nákladové ceny na řádku nabídky založené na produktu.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906110"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="cdbf6-103">Nákladové řádky nabídky založené na produktu</span><span class="sxs-lookup"><span data-stu-id="cdbf6-103">Costing product-based quote lines</span></span>

<span data-ttu-id="cdbf6-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="cdbf6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="cdbf6-105">Produktové řádky nabídek v Dynamics 365 Project Operations mají také pole **Nákladová cena**.</span><span class="sxs-lookup"><span data-stu-id="cdbf6-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="cdbf6-106">Toto pole se používá ke sledování nákladové ceny produktu na řádku nabídky a pro výpočty následné ziskovosti.</span><span class="sxs-lookup"><span data-stu-id="cdbf6-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="cdbf6-107">Když je pro katalogový produkt vytvořen řádek nabídky založené na produktu, náklady na řádek nabídky založené na produktu jsou ve výchozím stavu přebírány z pole **Standardní náklady** v katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="cdbf6-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="cdbf6-108">Pole standardních nákladů v katalogu produktů je nastaveno v základní měně organizace.</span><span class="sxs-lookup"><span data-stu-id="cdbf6-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="cdbf6-109">Výchozí jednotková cena na řádku nabídky na základě produktu se převede na měnu prodeje v nabídce.</span><span class="sxs-lookup"><span data-stu-id="cdbf6-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="cdbf6-110">Jednotková cena na řádku nabídky na produktu</span><span class="sxs-lookup"><span data-stu-id="cdbf6-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="cdbf6-111">Účelem jednotkových nákladů na produktové nabídce je umožnit různé náklady na produkt pro každý prodej.</span><span class="sxs-lookup"><span data-stu-id="cdbf6-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="cdbf6-112">Toto není typický scénář, ale někdy může dodavatel snížit cenu produktu v závislosti na zákazníkovi konečného prodeje.</span><span class="sxs-lookup"><span data-stu-id="cdbf6-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="cdbf6-113">Příklad:</span><span class="sxs-lookup"><span data-stu-id="cdbf6-113">For example:</span></span>

<span data-ttu-id="cdbf6-114">Fabrikam Robotics instaluje robotická ramena na montážní linky společnosti A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="cdbf6-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="cdbf6-115">Fabrikam poskytuje instalační služby, ale robotická ramena jsou získávána z Trey Robotics.</span><span class="sxs-lookup"><span data-stu-id="cdbf6-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="cdbf6-116">Pokud instalace robotických ramen ve společnosti A Datum Corporation otevře novou průmyslovou vertikálu pro robotická ramena společnosti Trey, mohl by Trey poskytnout speciální slevu na tento kontrakt společnosti Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="cdbf6-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="cdbf6-117">V tomto případě Fabrikam vytvoří produktovou nabídku pro robotická ramena a pro tuto nabídku zadá speciální cenu za jednotku.</span><span class="sxs-lookup"><span data-stu-id="cdbf6-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="cdbf6-118">Tato cena se liší od standardní ceny společnosti Trey Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="cdbf6-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
