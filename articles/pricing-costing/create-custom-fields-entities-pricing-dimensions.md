---
title: Vytvoření vlastních polí a entit jako cenových dimenzí
description: Toto téma poskytuje informace o tom, jak vytvořit vlastní sady možností nebo entity.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898253"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="51112-103">Vytvoření vlastních polí a entit jako cenových dimenzí</span><span class="sxs-lookup"><span data-stu-id="51112-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="51112-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="51112-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="51112-105">Následující kroky proveďte pokaždé, když chcete vytvořit vlastní sadu možností nebo entitu.</span><span class="sxs-lookup"><span data-stu-id="51112-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51112-106">Doporučujeme provést všechny změny cenových dimenzí v samostatném řešení.</span><span class="sxs-lookup"><span data-stu-id="51112-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="51112-107">Tento důležitý osvědčený postup poskytuje v budoucnosti flexibilitu pro aktualizaci nebo odebrání změn podle potřeby, pomůže při opětovném použití vaší práce a usnadní portování těchto změn na jinou instanci.</span><span class="sxs-lookup"><span data-stu-id="51112-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="51112-108">Po provedení všech požadovaných změn exportujte toto řešení jako **Spravované řešení** a importujte ho do jiných instancí za účelem znovupoužití vašeho nastavení cen.</span><span class="sxs-lookup"><span data-stu-id="51112-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="51112-109">Vytvoření vlastního řešení pro cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="51112-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="51112-110">Přejděte na **Nastavení** > **Řešení** a pak zvolte **Nové** a vytvořte nové řešení.</span><span class="sxs-lookup"><span data-stu-id="51112-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="51112-111">Řešení nazvěte **\<your organization name> cenové dimenze**, zadejte zbývající požadované informace a poté vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="51112-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="51112-112">Vytvoření vlastních polí a sad možností v řešení cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="51112-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="51112-113">Cenová dimenze může být sada možností nebo entita.</span><span class="sxs-lookup"><span data-stu-id="51112-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="51112-114">Obojí musí být vytvořeno ve vašem řešení ocenění.</span><span class="sxs-lookup"><span data-stu-id="51112-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="51112-115">Kroky v tomto postupu vysvětlují, jak vytvořit dimenze založené na entitě a dimenze založené na sadě možností.</span><span class="sxs-lookup"><span data-stu-id="51112-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="51112-116">Dimenze založené na entitě</span><span class="sxs-lookup"><span data-stu-id="51112-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="51112-117">Přejděte na **Nastavení** > **Řešení** a potom dvakrát klikněte na **\<your organization name> cenové dimenze**.</span><span class="sxs-lookup"><span data-stu-id="51112-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="51112-118">V Průzkumníku řešení vyberte v levém navigačním podokně **Entity**.</span><span class="sxs-lookup"><span data-stu-id="51112-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="51112-119">Zvolte **Nová** a vytvořte novou entitu nazvanou **Standardní funkce**.</span><span class="sxs-lookup"><span data-stu-id="51112-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="51112-120">Zadejte zbývající požadované informace a zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="51112-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="51112-121">Dimenze založené na sadě možností</span><span class="sxs-lookup"><span data-stu-id="51112-121">Option set-based dimensions</span></span> 
<span data-ttu-id="51112-122">Můžete vytvořit dvě dimenze založené na sadě možností.</span><span class="sxs-lookup"><span data-stu-id="51112-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="51112-123">Ke sledování ceny práce v místě **Domácí** a práce **U zákazníka** použijte **Místo výkonu práce zdroje** a chcete-li po dokončení práce použít přirážku, použijte **Pracovní dobu zdroje** s hodnotami **Normální** a **Přesčas**.</span><span class="sxs-lookup"><span data-stu-id="51112-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="51112-124">Přejděte na **Nastavení** > **Řešení** a dvakrát klikněte na **\<your organization name> cenové dimenze**.</span><span class="sxs-lookup"><span data-stu-id="51112-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="51112-125">V Průzkumníku řešení vyberte v levém navigačním podokně **Sady možností**.</span><span class="sxs-lookup"><span data-stu-id="51112-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="51112-126">Vyberte **Nový** vytvořte novou sadu možností, zadejte zbývající požadované informace a poté zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="51112-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="51112-127">Vytvoření dat pro dimenze založené na entitě</span><span class="sxs-lookup"><span data-stu-id="51112-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="51112-128">Data lze pro dimenze založené na entitě vytvořit ručně nebo pomocí importu aplikace Microsoft Excel nebo volání služby.</span><span class="sxs-lookup"><span data-stu-id="51112-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="51112-129">Pomocí kroků v tomto postupu můžete z dimenze **Standardní funkce**, která je založena na entitě, vytvořit dvě standardní funkce, **Systémový technik** a **Hlavní systémový technik**.</span><span class="sxs-lookup"><span data-stu-id="51112-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="51112-130">Pokud jsou data, která chcete vytvořit, malá, jako v následujícím příkladu, můžete použít standardní formulář.</span><span class="sxs-lookup"><span data-stu-id="51112-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="51112-131">Vyberte **Pokročilé hledání**, vyberte entitu **Standardní funkce** a potom vyberte **Výsledky**.</span><span class="sxs-lookup"><span data-stu-id="51112-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="51112-132">Zobrazí se všechny řádky v entitě **Standardní funkce**.</span><span class="sxs-lookup"><span data-stu-id="51112-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="51112-133">Vyberte **Nový** a v poli **Název** vyberte "Systémový inženýr" a pak zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="51112-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="51112-134">Zavře formulář.</span><span class="sxs-lookup"><span data-stu-id="51112-134">Close the form.</span></span> 
4. <span data-ttu-id="51112-135">Opakováním kroků 1–3 vytvořte další standardní funkci pro „Hlavního systémového technika”.</span><span class="sxs-lookup"><span data-stu-id="51112-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="51112-136">Přidání všech požadovaných entit a souvisejících komponent do řešení cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="51112-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="51112-137">K vašemu řešení cen bude nutné přidat následující entity.</span><span class="sxs-lookup"><span data-stu-id="51112-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="51112-138">Pomocí kroků v tomto postupu můžete provést některé důležité změny schématu v řešení ocenění, aby si entity všimly nových cenových dimenzí.</span><span class="sxs-lookup"><span data-stu-id="51112-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="51112-139">Zvolte **Nastavení** > **Řešení** a dvakrát klikněte na **\<your organization name> cenové dimenze**.</span><span class="sxs-lookup"><span data-stu-id="51112-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="51112-140">V Průzkumníku řešení vyberte v levém navigačním podokně **Přidat existující** > **Entity**.</span><span class="sxs-lookup"><span data-stu-id="51112-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="51112-141">V dialogovém okně **Součásti řešení** vyberte následující entity:</span><span class="sxs-lookup"><span data-stu-id="51112-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="51112-142">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="51112-142">Actual</span></span>
  - <span data-ttu-id="51112-143">Rezervovatelný zdroj</span><span class="sxs-lookup"><span data-stu-id="51112-143">Bookable Resource</span></span>
  - <span data-ttu-id="51112-144">Řádek odhadu</span><span class="sxs-lookup"><span data-stu-id="51112-144">Estimate Line</span></span>
  - <span data-ttu-id="51112-145">Podrobnosti řádku faktury</span><span class="sxs-lookup"><span data-stu-id="51112-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="51112-146">Řádek deníku</span><span class="sxs-lookup"><span data-stu-id="51112-146">Journal Line</span></span>
  - <span data-ttu-id="51112-147">Podrobnosti řádku projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="51112-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="51112-148">Člen projektového týmu</span><span class="sxs-lookup"><span data-stu-id="51112-148">Project Team Member</span></span>
  - <span data-ttu-id="51112-149">Podrobnosti řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="51112-149">Quote Line Detail</span></span>
  - <span data-ttu-id="51112-150">Přirážka ceny role</span><span class="sxs-lookup"><span data-stu-id="51112-150">Role Price Markup</span></span>
  - <span data-ttu-id="51112-151">Cena role</span><span class="sxs-lookup"><span data-stu-id="51112-151">Role Price</span></span> 
  - <span data-ttu-id="51112-152">Časový záznam</span><span class="sxs-lookup"><span data-stu-id="51112-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="51112-153">Nezapomeňte zahrnout všechny formuláře a zobrazení pro všechny vybrané entity.</span><span class="sxs-lookup"><span data-stu-id="51112-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="51112-154">Při zobrazení výzvy k zahrnutí všech závislých entit do výše vybraných entit zvolte **Ne**.</span><span class="sxs-lookup"><span data-stu-id="51112-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

