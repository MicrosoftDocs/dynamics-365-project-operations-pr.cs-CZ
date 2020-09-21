---
title: Vytvoření vlastních polí a entit
description: Toto téma vysvětluje, jak vytvořit sady možností a entity ve vlastním řešení na platformě Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750400"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="73906-103">Vytvoření vlastních polí a entit</span><span class="sxs-lookup"><span data-stu-id="73906-103">Create custom fields and entities</span></span> 

<span data-ttu-id="73906-104">Následující kroky proveďte pokaždé, když chcete na platformě Power Apps vytvořit vlastní sadu možností nebo entitu.</span><span class="sxs-lookup"><span data-stu-id="73906-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="73906-105">Postupy v tomto tématu by měly být prováděny prostřednictvím webového rozhraní Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="73906-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73906-106">Doporučujeme provést všechny změny cenových dimenzí v samostatném řešení.</span><span class="sxs-lookup"><span data-stu-id="73906-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="73906-107">Tento důležitý osvědčený postup poskytuje v budoucnosti flexibilitu pro aktualizaci nebo odebrání změn podle potřeby, pomůže při opětovném použití vaší práce a usnadní portování těchto změn na jinou instanci.</span><span class="sxs-lookup"><span data-stu-id="73906-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="73906-108">Po provedení všech požadovaných změn exportujte toto řešení jako **Spravované řešení** a importujte ho do jiných instancí za účelem znovupoužití vašeho nastavení cen.</span><span class="sxs-lookup"><span data-stu-id="73906-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="73906-109">Vytvoření vlastního řešení pro cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="73906-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="73906-110">V PSA klikněte na **Nastavení** > **Řešení** a pak kliknutím na **Nové** vytvořte nové řešení.</span><span class="sxs-lookup"><span data-stu-id="73906-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="73906-111">Řešení nazvěte **\<název vaší organizace> cenové dimenze**, zadejte zbývající požadované informace a poté klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="73906-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Vytvoření vlastního řešení pro cenové dimenze](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="73906-113">Vytvoření vlastních polí a sad možností v řešení cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="73906-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="73906-114">Cenová dimenze může být sada možností nebo entita.</span><span class="sxs-lookup"><span data-stu-id="73906-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="73906-115">Obojí musí být vytvořeno ve vašem řešení ocenění.</span><span class="sxs-lookup"><span data-stu-id="73906-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="73906-116">Kroky v tomto postupu vysvětlují, jak vytvořit dimenze založené na entitě a dimenze založené na sadě možností.</span><span class="sxs-lookup"><span data-stu-id="73906-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="73906-117">Dimenze založené na entitě</span><span class="sxs-lookup"><span data-stu-id="73906-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="73906-118">V PSA klikněte na **Nastavení** > **Řešení** a potom klikněte dvakrát na **\<název vaší organizace> cenové dimenze**.</span><span class="sxs-lookup"><span data-stu-id="73906-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="73906-119">V Průzkumníku řešení vyberte v levém navigačním podokně **Entity**.</span><span class="sxs-lookup"><span data-stu-id="73906-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="73906-120">Kliknutím na **Nová** vytvoříte novou entitu nazvanou **Standardní funkce**.</span><span class="sxs-lookup"><span data-stu-id="73906-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="73906-121">Zadejte zbývající požadované informace a klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="73906-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definice entity Standardní funkce](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="73906-123">Dimenze založené na sadě možností</span><span class="sxs-lookup"><span data-stu-id="73906-123">Option set-based dimensions</span></span> 
<span data-ttu-id="73906-124">Můžete vytvořit dvě dimenze založené na sadě možností.</span><span class="sxs-lookup"><span data-stu-id="73906-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="73906-125">Ke sledování ceny práce v místě **Domácí** a práce **U zákazníka** použijte **Místo výkonu práce zdroje** a chcete-li po dokončení práce použít přirážku, použijte **Pracovní dobu zdroje** s hodnotami **Normální** a **Přesčas**.</span><span class="sxs-lookup"><span data-stu-id="73906-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="73906-126">V PSA klikněte na **Nastavení** > **Řešení** a potom klikněte dvakrát na **\<název vaší organizace> cenové dimenze**.</span><span class="sxs-lookup"><span data-stu-id="73906-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="73906-127">V Průzkumníku řešení vyberte v levém navigačním podokně **Sady možností**.</span><span class="sxs-lookup"><span data-stu-id="73906-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="73906-128">Kliknutím na **Nový** vytvořte novou sadu možností, zadejte zbývající požadované informace a poté klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="73906-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="73906-129">Cenová dimenze založená na sadě možností s názvem Místo výkonu práce zdroje</span><span class="sxs-lookup"><span data-stu-id="73906-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="73906-130">Cenová dimenze založená na sadě možností s názvem Pracovní doba zdroje</span><span class="sxs-lookup"><span data-stu-id="73906-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="73906-131">Vytvoření dat pro dimenze založené na entitě</span><span class="sxs-lookup"><span data-stu-id="73906-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="73906-132">Data lze pro dimenze založené na entitě vytvořit ručně nebo pomocí importu aplikace Microsoft Excel nebo volání služby.</span><span class="sxs-lookup"><span data-stu-id="73906-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="73906-133">Pomocí kroků v tomto postupu můžete z dimenze **Standardní funkce**, která je založena na entitě, vytvořit dvě standardní funkce, **Systémový technik** a **Hlavní systémový technik**.</span><span class="sxs-lookup"><span data-stu-id="73906-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="73906-134">Pokud jsou data, která chcete vytvořit, malá, jako v následujícím příkladu, můžete použít standardní formulář.</span><span class="sxs-lookup"><span data-stu-id="73906-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="73906-135">Klikněte v PSA na **Rozšířené hledání**.</span><span class="sxs-lookup"><span data-stu-id="73906-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="73906-136">Vyberte entitu **Standardní funkce** a poté klikněte na **Výsledky**.</span><span class="sxs-lookup"><span data-stu-id="73906-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="73906-137">Zobrazí se všechny řádky v entitě **Standardní funkce**.</span><span class="sxs-lookup"><span data-stu-id="73906-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="73906-138">Klikněte na **Nový**.</span><span class="sxs-lookup"><span data-stu-id="73906-138">Click **New**.</span></span> <span data-ttu-id="73906-139">Do pole **Název** zadejte „Systémový technik” a poté klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="73906-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="73906-140">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="73906-140">Close the form.</span></span> 
4. <span data-ttu-id="73906-141">Opakováním kroků 1–3 vytvořte další standardní funkci pro „Hlavního systémového technika”.</span><span class="sxs-lookup"><span data-stu-id="73906-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="73906-142">Ukázková data pro entitu Standardní funkce</span><span class="sxs-lookup"><span data-stu-id="73906-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="73906-143">Přidání všech požadovaných entit PSA a souvisejících komponent do Řešení cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="73906-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="73906-144">K vašemu řešení ocenění bude nutné přidat následující entity Project Service.</span><span class="sxs-lookup"><span data-stu-id="73906-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="73906-145">Pomocí kroků v tomto postupu můžete provést některé důležité změny schématu v řešení ocenění, aby si entity všimly nových cenových dimenzí.</span><span class="sxs-lookup"><span data-stu-id="73906-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="73906-146">V PSA klikněte na **Nastavení** > **Řešení** a potom klikněte dvakrát na **\<název vaší organizace> cenové dimenze**.</span><span class="sxs-lookup"><span data-stu-id="73906-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="73906-147">V Průzkumníku řešení vyberte v levém navigačním podokně **Přidat existující** > **Entity**.</span><span class="sxs-lookup"><span data-stu-id="73906-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="73906-148">V dialogovém okně **Součásti řešení** vyberte následující entity:</span><span class="sxs-lookup"><span data-stu-id="73906-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="73906-149">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="73906-149">Actual</span></span>
- <span data-ttu-id="73906-150">Rezervovatelný zdroj</span><span class="sxs-lookup"><span data-stu-id="73906-150">Bookable Resource</span></span>
- <span data-ttu-id="73906-151">Řádek odhadu</span><span class="sxs-lookup"><span data-stu-id="73906-151">Estimate Line</span></span>
- <span data-ttu-id="73906-152">Podrobnosti řádku faktury</span><span class="sxs-lookup"><span data-stu-id="73906-152">Invoice Line Detail</span></span>
- <span data-ttu-id="73906-153">Řádek deníku</span><span class="sxs-lookup"><span data-stu-id="73906-153">Journal Line</span></span>
- <span data-ttu-id="73906-154">Podrobnosti řádku projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="73906-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="73906-155">Člen projektového týmu</span><span class="sxs-lookup"><span data-stu-id="73906-155">Project Team Member</span></span>
- <span data-ttu-id="73906-156">Podrobnosti řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="73906-156">Quote Line Detail</span></span>
- <span data-ttu-id="73906-157">Přirážka ceny role</span><span class="sxs-lookup"><span data-stu-id="73906-157">Role Price Markup</span></span>
- <span data-ttu-id="73906-158">Cena role</span><span class="sxs-lookup"><span data-stu-id="73906-158">Role Price</span></span> 
- <span data-ttu-id="73906-159">Časový záznam</span><span class="sxs-lookup"><span data-stu-id="73906-159">Time Entry</span></span> 

> ![Přidat existující entity k řešení cenových dimenzí](media/Existing-entities-to-PD-solution.png)

> ![Vybrat součásti řešení](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="73906-162">Nezapomeňte zahrnout všechny formuláře a zobrazení pro všechny vybrané entity.</span><span class="sxs-lookup"><span data-stu-id="73906-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="73906-163">Při zobrazení výzvy k zahrnutí všech závislých entit do výše vybraných entit klikněte na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="73906-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Nezahrnovat všechny související komponenty](media/Do-not-include-required.png)


