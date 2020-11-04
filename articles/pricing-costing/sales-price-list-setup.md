---
title: Nastavení prodejního ceníku
description: Tento téma poskytuje informace o prodejních cenících pro ceny projektů.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d2c797b72666123eb0a18d2d0c1df9fe3d207f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073835"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="06a1b-103">Nastavení prodejního ceníku</span><span class="sxs-lookup"><span data-stu-id="06a1b-103">Sales price list setup</span></span>

<span data-ttu-id="06a1b-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="06a1b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="06a1b-105">U projektových nabídek a smluv má projektový ceník odlišný způsob přepsání ceny než produktový ceník.</span><span class="sxs-lookup"><span data-stu-id="06a1b-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="06a1b-106">Na řádku nabídky založeném na katalogu produktů můžete přepsat cenu rolí a kategorií přímo na řádku nabídky, protože každý řádek nabídky odkazuje přesně na jednu položku katalogu.</span><span class="sxs-lookup"><span data-stu-id="06a1b-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="06a1b-107">Na řádku nabídky založeném na projektu však nemůžete přepsat cenu rolí a kategorií přímo na řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="06a1b-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="06a1b-108">Ceník projektu můžete použít pro práci se dvěma odlišnými vzory přepsání.</span><span class="sxs-lookup"><span data-stu-id="06a1b-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="06a1b-109">Doporučujeme, abyste pro zdroje projektu a položky katalogu měli samostatný ceník, a to z důvodu rozdílů v chování mezi těmito dvěma položkami při přepsání ceny.</span><span class="sxs-lookup"><span data-stu-id="06a1b-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="06a1b-110">Každá z následujících entit může obsahovat jeden nebo více přidružených ceníků pro ocenění projektu:</span><span class="sxs-lookup"><span data-stu-id="06a1b-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="06a1b-111">Zákazník (účet)</span><span class="sxs-lookup"><span data-stu-id="06a1b-111">Customer (account)</span></span> 
- <span data-ttu-id="06a1b-112">Příležitost</span><span class="sxs-lookup"><span data-stu-id="06a1b-112">Opportunity</span></span> 
- <span data-ttu-id="06a1b-113">Nabídka</span><span class="sxs-lookup"><span data-stu-id="06a1b-113">Quote</span></span> 
- <span data-ttu-id="06a1b-114">Projektová smlouva</span><span class="sxs-lookup"><span data-stu-id="06a1b-114">Project Contract</span></span>

<span data-ttu-id="06a1b-115">Přidružení těchto entit k ceníku je označeno pomocí projektových ceníků.</span><span class="sxs-lookup"><span data-stu-id="06a1b-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="06a1b-116">K entitám Zákazník, Příležitost, Nabídka a Projektová smlouva můžete přidružit jeden nebo více ceníků.</span><span class="sxs-lookup"><span data-stu-id="06a1b-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="06a1b-117">Výchozí projektový ceník není automaticky zadán do záznamu zákazníka.</span><span class="sxs-lookup"><span data-stu-id="06a1b-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="06a1b-118">K záznamu zákazníka však můžete ručně připojit Ceník projektu.</span><span class="sxs-lookup"><span data-stu-id="06a1b-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="06a1b-119">Přesto byste měli projektový ceník přiložit ručně pouze v případě, že máte se zákazníkem vlastní cenovou dohodu.</span><span class="sxs-lookup"><span data-stu-id="06a1b-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="06a1b-120">Pokud je projektový ceník připojen k prodejní entitě, ověřují se následující informace:</span><span class="sxs-lookup"><span data-stu-id="06a1b-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="06a1b-121">Ceník má kontext **Prodej**.</span><span class="sxs-lookup"><span data-stu-id="06a1b-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="06a1b-122">Měna ceníku se musí shodovat s měnou zákazníka.</span><span class="sxs-lookup"><span data-stu-id="06a1b-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="06a1b-123">U projektové smlouvy se používá následující pořadí priorit pro automatické nastavení souvisejících projektových ceníků:</span><span class="sxs-lookup"><span data-stu-id="06a1b-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="06a1b-124">Nabídka</span><span class="sxs-lookup"><span data-stu-id="06a1b-124">Quote</span></span>
2. <span data-ttu-id="06a1b-125">Příležitost</span><span class="sxs-lookup"><span data-stu-id="06a1b-125">Opportunity</span></span>
3. <span data-ttu-id="06a1b-126">Zákazník</span><span class="sxs-lookup"><span data-stu-id="06a1b-126">Customer</span></span> 
4. <span data-ttu-id="06a1b-127">Globální nastavení</span><span class="sxs-lookup"><span data-stu-id="06a1b-127">Global settings</span></span> 

<span data-ttu-id="06a1b-128">Je-li ve výchozím nastavení zadán projektový ceník, systém ověří, že měna odpovídá měně zákazníka, a že zadané výchozí ceníky obsahují kontext **Prodeje**.</span><span class="sxs-lookup"><span data-stu-id="06a1b-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="06a1b-129">K entitám Zákazník, Příležitost, Nabídka a Projektová smlouva můžete přidružit několik projektových ceníků.</span><span class="sxs-lookup"><span data-stu-id="06a1b-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="06a1b-130">Tato funkce podporuje výchozí ceny specifické pro datum pro dlouhotrvající projektovou smlouvu, kde můžete vyžadovat více než jeden ceník na obchodní vztah pro aktualizace cen, ke kterým dochází z důvodu inflace.</span><span class="sxs-lookup"><span data-stu-id="06a1b-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="06a1b-131">Pokud však ceníky, které přidružíte k entitě Zákazník, Příležitost, Nabídka nebo Projektová smlouva, mají překrývající se datum účinnosti, mohou být výchozí ceny nesprávné.</span><span class="sxs-lookup"><span data-stu-id="06a1b-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="06a1b-132">Proto byste se měli ujistit, že projektové ceníky s překrývajícími se daty účinnosti nejsou přidruženy k těmto entitám.</span><span class="sxs-lookup"><span data-stu-id="06a1b-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
