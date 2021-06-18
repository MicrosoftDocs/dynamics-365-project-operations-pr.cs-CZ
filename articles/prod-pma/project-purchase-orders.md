---
title: Nákupní objednávky pro projekt
description: Tento článek popisuje různé metody, které můžete použít k vytvoření nákupních objednávek pro projekt. Metoda, kterou použijete, závisí na účelu nákupní objednávky a na tom, kdy jsou zakoupené položky spotřebovány a účtovány projektu.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c3ce2d0c0fb3cecf22157db5cb37eb744027d0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999348"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="f2701-104">Nákupní objednávky pro projekt</span><span class="sxs-lookup"><span data-stu-id="f2701-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2701-105">Tento článek popisuje různé metody, které můžete použít k vytvoření nákupních objednávek pro projekt.</span><span class="sxs-lookup"><span data-stu-id="f2701-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="f2701-106">Metoda, kterou použijete, závisí na účelu nákupní objednávky a na tom, kdy jsou zakoupené položky spotřebovány a účtovány projektu.</span><span class="sxs-lookup"><span data-stu-id="f2701-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="f2701-107">Metody pro vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="f2701-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="f2701-108">K vytvoření nákupní objednávky ve Správě projektů a účetnictví můžete použít jednu z následujících metod.</span><span class="sxs-lookup"><span data-stu-id="f2701-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="f2701-109">Účel nákupní objednávky určuje, kdy bude tato spotřebována a tedy i to, kdy budou její položky účtovány projektu.</span><span class="sxs-lookup"><span data-stu-id="f2701-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f2701-110">Způsob</span><span class="sxs-lookup"><span data-stu-id="f2701-110">Method</span></span></th>
<th><span data-ttu-id="f2701-111">Účel</span><span class="sxs-lookup"><span data-stu-id="f2701-111">Purpose</span></span></th>
<th><span data-ttu-id="f2701-112">Spotřeba položek</span><span class="sxs-lookup"><span data-stu-id="f2701-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f2701-113">Vytvořte nákupní objednávku přímo z projektu.</span><span class="sxs-lookup"><span data-stu-id="f2701-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="f2701-114">Tuto metodu použijte k nákupu položek od externího dodavatele, určených ke spotřebě v projektu.</span><span class="sxs-lookup"><span data-stu-id="f2701-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="f2701-115">Nákupní objednávku můžete vytvořit dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="f2701-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="f2701-116">Přímo z projektu.</span><span class="sxs-lookup"><span data-stu-id="f2701-116">From the project itself.</span></span> <span data-ttu-id="f2701-117">V tomto případě je projekt již pro nákupní objednávku definován.</span><span class="sxs-lookup"><span data-stu-id="f2701-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="f2701-118">Přechodem k nákupní objednávce projektu.</span><span class="sxs-lookup"><span data-stu-id="f2701-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="f2701-119">Chcete-li vytvořit nákupní objednávku, musíte vybrat dodavatele i projekt.</span><span class="sxs-lookup"><span data-stu-id="f2701-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="f2701-120">Položky se spotřebovávají při aktualizaci faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="f2701-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f2701-121">Vytvořte nákupní objednávku z prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="f2701-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="f2701-122">Tuto metodu použijte k nákupu položek při vytváření prodejní objednávky z projektu.</span><span class="sxs-lookup"><span data-stu-id="f2701-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="f2701-123">Položky jsou spotřebovány, když je prodejní objednávka fakturována zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="f2701-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f2701-124">Vytvořte nákupní objednávku z požadavku na položku.</span><span class="sxs-lookup"><span data-stu-id="f2701-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="f2701-125">Tuto metodu použijte k nákupu položek při vytváření požadavku na položku z projektu.</span><span class="sxs-lookup"><span data-stu-id="f2701-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="f2701-126">Položky se spotřebovávají, když se aktualizuje dodací list s požadavkem na položku.</span><span class="sxs-lookup"><span data-stu-id="f2701-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="f2701-127">Když aktualizujete fakturu dodavatele nebo dodací list, budete vyzváni k aktualizaci dodacího listu v požadavku na položku.</span><span class="sxs-lookup"><span data-stu-id="f2701-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="f2701-128">Další informace viz téma [Příjem položek na nákupní objednávce z požadavku na položku](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="f2701-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]