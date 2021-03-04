---
title: Nastavení nákladových a prodejních sazeb pro produkty katalogu – omezené
description: Toto téma poskytuje informace o tom, jak nastavit nákladové a prodejní sazby u položek v katalogu produktů.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764542"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="c7578-103">Nastavení nákladových a prodejních sazeb pro produkty katalogu – omezené</span><span class="sxs-lookup"><span data-stu-id="c7578-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="c7578-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="c7578-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c7578-105">Nastavení cen pro položky katalogu produktů v Dynamics 365 Project Operations je stejné jako v Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="c7578-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="c7578-106">V Project Operations nelze produkty odhadovat ani používat na projektech, takže není nutné nastavovat ceny katalogů produktů v cenících projektů pro nabídky a smlouvy.</span><span class="sxs-lookup"><span data-stu-id="c7578-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="c7578-107">Použijte pole **Cena produktu** pole nabídky, smlouvy nebo účtu k nastavení cen katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="c7578-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="c7578-108">Nenastavujte ceny katalogů produktů v cenících projektů.</span><span class="sxs-lookup"><span data-stu-id="c7578-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="c7578-109">Projektové ceníky jsou exkluzivní funkcí aplikace Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c7578-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="c7578-110">Obchodní logika pro konkrétní aplikaci kopíruje ceníky z nabídky do smlouvy.</span><span class="sxs-lookup"><span data-stu-id="c7578-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="c7578-111">Výsledkem je projektový ceník pro určitou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="c7578-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="c7578-112">Operace kopírování může zpozdit proces vyhrání nabídky, pokud bude projektový ceník nabídky příliš velký.</span><span class="sxs-lookup"><span data-stu-id="c7578-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="c7578-113">Produktové ceníky se nekopírují, aby vytvořily vlastní ceníky ve smlouvách.</span><span class="sxs-lookup"><span data-stu-id="c7578-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="c7578-114">Protože se nejedná o žádné kopírování, není ovlivněn výkon procesu nabídky.</span><span class="sxs-lookup"><span data-stu-id="c7578-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>
