---
title: Vytvoření vlastních polí a entit jako cenových dimenzí
description: Toto téma poskytuje informace o tom, jak vytvořit vlastní sady možností nebo entity.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275620"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="38db2-103">Vytvoření vlastních polí a entit jako cenových dimenzí</span><span class="sxs-lookup"><span data-stu-id="38db2-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="38db2-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="38db2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="38db2-105">Následující kroky proveďte, když chcete vytvořit vlastní sadu možností nebo entitu pro použití jako cenové dimenze.</span><span class="sxs-lookup"><span data-stu-id="38db2-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="38db2-106">Další informace viz [Přehled cenových dimenzí](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="38db2-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="38db2-107">Doporučujeme provést všechny změny cenových dimenzí v samostatném řešení.</span><span class="sxs-lookup"><span data-stu-id="38db2-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="38db2-108">Tento důležitý osvědčený postup poskytuje v budoucnu flexibilitu pro aktualizaci nebo odstranění změn podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="38db2-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="38db2-109">To také pomůže s opětovným použitím vaší práce a usnadní přenos těchto změn do jiné instance. Po provedení všech požadovaných změn exportujte toto řešení jako **Spravované řešení** a importujte jej do jiných instancí, abyste mohli znovu použít nastavení cen.</span><span class="sxs-lookup"><span data-stu-id="38db2-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="38db2-110">Vytvoření vlastních polí a sad možností v řešení cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="38db2-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="38db2-111">Cenová dimenze může být sada možností nebo entita.</span><span class="sxs-lookup"><span data-stu-id="38db2-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="38db2-112">Obojí musí být vytvořeno ve vašem řešení ocenění.</span><span class="sxs-lookup"><span data-stu-id="38db2-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="38db2-113">Kroky v tomto postupu vysvětlují, jak vytvořit dimenze založené na entitě a dimenze založené na sadě možností.</span><span class="sxs-lookup"><span data-stu-id="38db2-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="38db2-114">Dimenze založené na entitě</span><span class="sxs-lookup"><span data-stu-id="38db2-114">Entity-based dimensions</span></span>
<span data-ttu-id="38db2-115">Chcete-li vytvořit dimenze založené na entitách, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="38db2-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="38db2-116">Přejděte na **Nastavení** > **Řešení** a potom dvakrát klikněte na **\<your organization name> cenové dimenze**.</span><span class="sxs-lookup"><span data-stu-id="38db2-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="38db2-117">V Průzkumníku řešení vyberte v levém navigačním podokně **Entity**.</span><span class="sxs-lookup"><span data-stu-id="38db2-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="38db2-118">Zvolte **Nová** a vytvořte novou entitu nazvanou **Standardní funkce**.</span><span class="sxs-lookup"><span data-stu-id="38db2-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="38db2-119">Zadejte zbývající požadované informace a zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="38db2-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definice entity Standardní funkce](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="38db2-121">Dimenze založené na sadě možností</span><span class="sxs-lookup"><span data-stu-id="38db2-121">Option set-based dimensions</span></span> 
<span data-ttu-id="38db2-122">Můžete vytvořit dvě dimenze založené na sadě možností.</span><span class="sxs-lookup"><span data-stu-id="38db2-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="38db2-123">Použijte **Místo práce zdroje**, chcete-li sledovat cenu místa práce **Doma** a práce **U zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="38db2-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="38db2-124">Použijte **Pracovní dobu zdroje** s hodnotami **Pravidelný** a **Přesčas** pro použití přirážky po dokončení práce.</span><span class="sxs-lookup"><span data-stu-id="38db2-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="38db2-125">Následující obrázek poskytuje zobrazení dimenze **Místo práce zdroje**.</span><span class="sxs-lookup"><span data-stu-id="38db2-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Cenová dimenze založená na sadě možností s názvem Místo výkonu práce zdroje](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="38db2-127">Následující obrázek poskytuje zobrazení dimenze **Pracovní doba zdroje**.</span><span class="sxs-lookup"><span data-stu-id="38db2-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Cenová dimenze založená na sadě možností s názvem Pracovní doba zdroje](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="38db2-129">Přejděte na **Nastavení** > **Řešení** a dvakrát klikněte na **\<your organization name> cenové dimenze**.</span><span class="sxs-lookup"><span data-stu-id="38db2-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="38db2-130">V Průzkumníku řešení vyberte v levém navigačním podokně **Sady možností**.</span><span class="sxs-lookup"><span data-stu-id="38db2-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="38db2-131">Vyberte **Nový** vytvořte novou sadu možností, zadejte zbývající požadované informace a poté zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="38db2-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="38db2-132">Vytvoření dat pro dimenze založené na entitě</span><span class="sxs-lookup"><span data-stu-id="38db2-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="38db2-133">Data lze pro dimenze založené na entitě vytvořit ručně nebo pomocí importu aplikace Microsoft Excel nebo volání služby.</span><span class="sxs-lookup"><span data-stu-id="38db2-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="38db2-134">Pomocí kroků v tomto postupu můžete z dimenze **Standardní funkce**, která je založena na entitě, vytvořit dvě standardní funkce, **Systémový technik** a **Hlavní systémový technik**.</span><span class="sxs-lookup"><span data-stu-id="38db2-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="38db2-135">Pokud jsou data, která chcete vytvořit, malá, jako v následujícím příkladu, můžete použít standardní formulář.</span><span class="sxs-lookup"><span data-stu-id="38db2-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="38db2-136">Vyberte **Rozšířené hledání**.</span><span class="sxs-lookup"><span data-stu-id="38db2-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="38db2-137">Vyberte entitu **Standardní funkce** a poté vyberte **Výsledky**.</span><span class="sxs-lookup"><span data-stu-id="38db2-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="38db2-138">Zobrazí se všechny řádky v entitě **Standardní funkce**.</span><span class="sxs-lookup"><span data-stu-id="38db2-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="38db2-139">Vyberte **Nový** a v poli **Název** vyberte "Systémový inženýr" a pak zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="38db2-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="38db2-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="38db2-140">Close the page.</span></span> 
5. <span data-ttu-id="38db2-141">Opakováním kroků 1–3 vytvořte další standardní funkci pro „Hlavního systémového technika”.</span><span class="sxs-lookup"><span data-stu-id="38db2-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Ukázková data pro entitu Standardní funkce](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]