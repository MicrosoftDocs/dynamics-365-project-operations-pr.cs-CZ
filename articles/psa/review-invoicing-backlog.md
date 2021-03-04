---
title: Kontrola nedokončené fakturace u projektů a projektových smluv
description: Toto téma obsahuje informace o tom, jak kontrolovat nedokončené časové, výdajové a produktové záznamy a jak je označit jako připravené k fakturaci.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 092455a131f556e4f943f6bb89d7e38358f0a697
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150480"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="d3051-103">Kontrola nedokončené fakturace u projektů a projektových smluv</span><span class="sxs-lookup"><span data-stu-id="d3051-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d3051-104">Pokud je transakce připravena k vytvoření a zpracování faktury, měla by být označena jako **Připraveno k fakturaci**.</span><span class="sxs-lookup"><span data-stu-id="d3051-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="d3051-105">Toto téma popisuje typy transakcí, které lze vytvořit.</span><span class="sxs-lookup"><span data-stu-id="d3051-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="d3051-106">Kontrola nedokončené fakturace času a materiálu</span><span class="sxs-lookup"><span data-stu-id="d3051-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="d3051-107">PSA při odeslání a schválení časových nebo výdajových záznamů pro projekt vytvoří skutečnou hodnotu projektu.</span><span class="sxs-lookup"><span data-stu-id="d3051-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="d3051-108">Pokud je kombinace projektu a třídy transakce namapována na řádek smlouvy pro projekt s časem a materiálem, jsou při schválení záznamu vytvořeny dvě skutečné hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d3051-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="d3051-109">Skutečné náklady</span><span class="sxs-lookup"><span data-stu-id="d3051-109">Cost actual</span></span> 
- <span data-ttu-id="d3051-110">Skutečný nefakturovaný prodej</span><span class="sxs-lookup"><span data-stu-id="d3051-110">Unbilled sales actual</span></span>

<span data-ttu-id="d3051-111">Skutečné hodnoty nefakturovaného prodeje představují nedokončenou fakturaci a jeho stav fakturace musí být nastaven na **Připraveno k fakturaci**.</span><span class="sxs-lookup"><span data-stu-id="d3051-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="d3051-112">Při vytvoření projektové faktury jsou skutečné hodnoty nefakturovaného prodeje, které jsou označeny jako **Připraveno k fakturaci**, zkopírovány jako podrobnosti řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="d3051-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="d3051-113">Chcete-li zkontrolovat nedokončenou fakturaci času a materiálu, přejděte na **Prodej** \> **Fakturace** \> **Nedokončená fakturace času a materiálu**.</span><span class="sxs-lookup"><span data-stu-id="d3051-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="d3051-114">Vyberte všechny skutečné hodnoty nefakturovaného prodeje, které jsou připraveny k fakturaci a pak vyberte **Připraveno k fakturaci**.</span><span class="sxs-lookup"><span data-stu-id="d3051-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="d3051-115">Stav fakturace těchto skutečných hodnot je změněn na **Připraveno k fakturaci**.</span><span class="sxs-lookup"><span data-stu-id="d3051-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Nedokončená fakturace času a materiálu](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="d3051-117">Kontrola nedokončené fakturace produktů</span><span class="sxs-lookup"><span data-stu-id="d3051-117">Review the product billing backlog</span></span>

<span data-ttu-id="d3051-118">Obsahuje-li projektová smlouva v PSA řádky smlouvy založené na produktu, budou tyto řádky zohledněny pro fakturaci při každém vytvoření faktury pro projektovou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="d3051-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="d3051-119">Všechny produkty, které obsahují řádky smlouvy označené jako **Připraveno k fakturaci**, jsou zkopírovány do projektové faktury jako řádky projektové faktury.</span><span class="sxs-lookup"><span data-stu-id="d3051-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="d3051-120">Chcete-li zkontrolovat nedokončenou fakturaci produktů, přejděte do **Prodej** \> **Fakturace** \> **Nedokončená fakturace produktů**.</span><span class="sxs-lookup"><span data-stu-id="d3051-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="d3051-121">Vyberte všechny řádky smlouvy založené na produktu, které jsou připraveny k fakturaci a pak vyberte **Připraveno k fakturaci**.</span><span class="sxs-lookup"><span data-stu-id="d3051-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="d3051-122">Stav fakturace těchto řádků je změněn na **Připraveno k fakturaci**.</span><span class="sxs-lookup"><span data-stu-id="d3051-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Nedokončená fakturace produktů](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="d3051-124">Kontrola fakturačních milníků u smluv s pevnou cenou</span><span class="sxs-lookup"><span data-stu-id="d3051-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="d3051-125">Každý řádek projektové smlouvy, který obsahuje fakturační metodu s pevnou cenou, musí definovat milníky smlouvy.</span><span class="sxs-lookup"><span data-stu-id="d3051-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="d3051-126">Tyto milníky smlouvy lze fakturovat pouze v případě, že jsou označeny jako **Připraveno k fakturaci**.</span><span class="sxs-lookup"><span data-stu-id="d3051-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="d3051-127">Chcete-li zkontrolovat fakturační milníky, přejděte na **Prodej** \> **Fakturace** \> **Milníky s pevnou cenou**.</span><span class="sxs-lookup"><span data-stu-id="d3051-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="d3051-128">Vyberte milníky, které jsou připraveny k fakturaci a pak vyberte **Připraveno k fakturaci**.</span><span class="sxs-lookup"><span data-stu-id="d3051-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="d3051-129">Stav fakturace těchto milníků je změněn na **Připraveno k fakturaci**.</span><span class="sxs-lookup"><span data-stu-id="d3051-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Milníky s pevnou cenou](media/FPBacklog.png)
