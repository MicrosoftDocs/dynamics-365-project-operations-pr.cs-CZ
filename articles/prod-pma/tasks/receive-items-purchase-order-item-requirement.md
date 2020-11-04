---
title: Příjem položek na nákupní objednávce z požadavku na položku.
description: Tento téma vysvětluje, jak přijímat položky na nákupní objednávce z požadavku na položku.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073947"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="eef55-103">Příjem položek na nákupní objednávce z požadavku na položku.</span><span class="sxs-lookup"><span data-stu-id="eef55-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eef55-104">Tento téma vysvětluje, jak přijímat položky na nákupní objednávce z požadavku na položku.</span><span class="sxs-lookup"><span data-stu-id="eef55-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="eef55-105">Použitím požadavku na položku namísto transakce s položkou můžete naplánovat dodávku těsně před skutečným použitím zboží, vytvořit nákupní objednávku, zahrnout položku do rámce obchodní dohody a zahrnout požadavek na položku do plánování výroby.</span><span class="sxs-lookup"><span data-stu-id="eef55-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="eef55-106">Tento úkol používá datovou sadu USSI.</span><span class="sxs-lookup"><span data-stu-id="eef55-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="eef55-107">V navigačním podokně přejděte na **Moduly > Řízení projektů a účetnictví > Projekty > Všechny projekty**.</span><span class="sxs-lookup"><span data-stu-id="eef55-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="eef55-108">V seznamu vyberte odkaz v požadovaném řádku.</span><span class="sxs-lookup"><span data-stu-id="eef55-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="eef55-109">V podokně akcí vyberte **Plán**.</span><span class="sxs-lookup"><span data-stu-id="eef55-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="eef55-110">Vyberte **Požadavky na položku**.</span><span class="sxs-lookup"><span data-stu-id="eef55-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="eef55-111">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="eef55-111">Select **New**.</span></span>
6. <span data-ttu-id="eef55-112">V novém řádku zadejte nebo vyberte hodnotu v poli **Číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="eef55-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="eef55-113">Do pole **Množství** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="eef55-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="eef55-114">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="eef55-114">Select **Save**.</span></span>
9. <span data-ttu-id="eef55-115">V podokně akcí vyberte **Spravovat**.</span><span class="sxs-lookup"><span data-stu-id="eef55-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="eef55-116">Vyberte **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="eef55-116">Select **Functions**.</span></span>
11. <span data-ttu-id="eef55-117">Vyberte **Vytvoření nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="eef55-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="eef55-118">Klikněte na tlačítko **Zahrnout vše**.</span><span class="sxs-lookup"><span data-stu-id="eef55-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="eef55-119">V poli **Účet dodavatele** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="eef55-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="eef55-120">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="eef55-120">Select **OK**.</span></span>
15. <span data-ttu-id="eef55-121">V navigačním podokně přejděte na **Moduly > Závazky > Nákupní objednávky > Všichni nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="eef55-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="eef55-122">V seznamu vyberte odkaz v požadovaném řádku.</span><span class="sxs-lookup"><span data-stu-id="eef55-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="eef55-123">V podokně akcí vyberte **Koupit**.</span><span class="sxs-lookup"><span data-stu-id="eef55-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="eef55-124">Vyberte **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="eef55-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="eef55-125">V podokně akcí vyberte **Získat**.</span><span class="sxs-lookup"><span data-stu-id="eef55-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="eef55-126">Vyberte **Účtenka produktu**.</span><span class="sxs-lookup"><span data-stu-id="eef55-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="eef55-127">Do pole **Účtenka produktu** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="eef55-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="eef55-128">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="eef55-128">Select **OK**.</span></span>

