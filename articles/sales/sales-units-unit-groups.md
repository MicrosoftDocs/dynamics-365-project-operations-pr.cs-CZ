---
title: Jednotky a skupiny jednotek
description: Tento téma poskytuje informace o tom, jak vytvořit jednotky a skupiny jednotek v Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 3f588e41d001befeac87bb6a4e28a83cf5cfa865
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131020"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="84a42-103">Jednotky a skupiny jednotek</span><span class="sxs-lookup"><span data-stu-id="84a42-103">Units and unit groups</span></span>

<span data-ttu-id="84a42-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="84a42-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="84a42-105">Jednotky jsou množství nebo míry, ve kterých své produkty nebo služby prodáváte.</span><span class="sxs-lookup"><span data-stu-id="84a42-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="84a42-106">Pokud například prodáváte zahradnické potřeby, můžete prodávat semena v jednotkách sáčky, krabice a palety.</span><span class="sxs-lookup"><span data-stu-id="84a42-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="84a42-107">Skupina jednotek je kolekce těchto různých jednotek.</span><span class="sxs-lookup"><span data-stu-id="84a42-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="84a42-108">Chcete-li provést kroky v tomto tématu, ujistěte se, že vám byla přiřazena role správce systému nebo Sales Professional Manager nebo že máte ekvivalentní oprávnění.</span><span class="sxs-lookup"><span data-stu-id="84a42-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="84a42-109">Vytvoření skupiny jednotek</span><span class="sxs-lookup"><span data-stu-id="84a42-109">Create a unit group</span></span>

1. <span data-ttu-id="84a42-110">V mapě webu vyberte **Jednotky**.</span><span class="sxs-lookup"><span data-stu-id="84a42-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="84a42-111">Zvolte **Nová** a v dialogovém okně **Vytvořit skupinu jednotky** zadejte název jednotky.</span><span class="sxs-lookup"><span data-stu-id="84a42-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="84a42-112">V poli **Primární jednotka** zadejte nejnižší běžnou měrnou jednotku, ve které bude produkt prodáván.</span><span class="sxs-lookup"><span data-stu-id="84a42-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="84a42-113">Můžete například zadat „kus“ nebo „unce“.</span><span class="sxs-lookup"><span data-stu-id="84a42-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="84a42-114">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="84a42-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="84a42-115">Přidání jednotek do skupiny jednotek</span><span class="sxs-lookup"><span data-stu-id="84a42-115">Add units to a unit group</span></span>

1. <span data-ttu-id="84a42-116">Otevřete skupinu jednotek a na kartě **Související** vyberte **Jednotky**.</span><span class="sxs-lookup"><span data-stu-id="84a42-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="84a42-117">Uvidíte, že primární jednotka je již přidána.</span><span class="sxs-lookup"><span data-stu-id="84a42-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="84a42-118">Vyberte **Přidat novou jednotku** a na stránce **Rychlé vytvoření: Jednotka** zadejte do pole **Název** název jednotky.</span><span class="sxs-lookup"><span data-stu-id="84a42-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="84a42-119">Do pole **Množství** zadejte množství, které bude jednotka obsahovat.</span><span class="sxs-lookup"><span data-stu-id="84a42-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="84a42-120">Pokud například krabice obsahuje dva kusy, zadejte „2“.</span><span class="sxs-lookup"><span data-stu-id="84a42-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="84a42-121">V poli **Základní jednotka** vyberte základní jednotku pro stanovení nejnižší měrné jednotky pro danou jednotku.</span><span class="sxs-lookup"><span data-stu-id="84a42-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="84a42-122">Můžete například vybrat „Kus“.</span><span class="sxs-lookup"><span data-stu-id="84a42-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="84a42-123">Zvolte **Uložit**:</span><span class="sxs-lookup"><span data-stu-id="84a42-123">Select **Save**:</span></span>
