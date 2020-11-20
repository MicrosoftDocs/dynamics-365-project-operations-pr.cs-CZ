---
title: Nastavení nákladových a prodejních sazeb pro produkty katalogu – omezené
description: Toto téma poskytuje informace o tom, jak nastavit nákladové a prodejní sazby u položek v katalogu produktů.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176693"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="b3570-103">Nastavení nákladových a prodejních sazeb pro produkty katalogu – omezené</span><span class="sxs-lookup"><span data-stu-id="b3570-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="b3570-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="b3570-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b3570-105">Stanovení cen u položek v katalogu produktů v Dynamics 365 Project Operations je stejné jako v Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="b3570-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="b3570-106">Protože produkty nelze odhadnout ani použít v projektech Project Operations, není nutné nastavovat katalogové ceny produktů v projektových cenících pro nabídky a smlouvy.</span><span class="sxs-lookup"><span data-stu-id="b3570-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="b3570-107">Katalogové ceny produktů by měly být stanoveny v poli **Cena produktu** nabídky, smlouvy nebo účtu.</span><span class="sxs-lookup"><span data-stu-id="b3570-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="b3570-108">Nenastavujte katalogové ceny produktů v projektových cenících pro tyto entity.</span><span class="sxs-lookup"><span data-stu-id="b3570-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="b3570-109">Projektové ceníky jsou exkluzivní funkcí aplikace Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b3570-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="b3570-110">Existuje obchodní logika pro konkrétní aplikaci, která kopíruje ceníky z nabídky do smlouvy.</span><span class="sxs-lookup"><span data-stu-id="b3570-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="b3570-111">Výsledkem je projektový ceník pro určitou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="b3570-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="b3570-112">Operace kopírování může zpozdit proces vyhrání nabídky, pokud bude projektový ceník nabídky příliš velký.</span><span class="sxs-lookup"><span data-stu-id="b3570-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="b3570-113">Produktové ceníky se nekopírují, aby vytvořily vlastní ceníky ve smlouvách.</span><span class="sxs-lookup"><span data-stu-id="b3570-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="b3570-114">To znamená, že produktové ceníky nemají vliv na výkon procesu vyhrání nabídky.</span><span class="sxs-lookup"><span data-stu-id="b3570-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
