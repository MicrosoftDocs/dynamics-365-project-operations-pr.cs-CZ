---
title: Vytvoření vlastních polí a entit
description: Toto téma vysvětluje, jak vytvořit sady možností a entity ve vlastním řešení na platformě Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 442ff9cf2206bec307cea7ff30b9266502d8f77b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073849"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="fbd58-103">Vytvoření vlastních polí a entit</span><span class="sxs-lookup"><span data-stu-id="fbd58-103">Create custom fields and entities</span></span> 

<span data-ttu-id="fbd58-104">Následující kroky proveďte pokaždé, když chcete na platformě Power Apps vytvořit vlastní sadu možností nebo entitu.</span><span class="sxs-lookup"><span data-stu-id="fbd58-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="fbd58-105">Postupy v tomto tématu by měly být prováděny prostřednictvím webového rozhraní Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="fbd58-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fbd58-106">Doporučujeme provést všechny změny cenových dimenzí v samostatném řešení.</span><span class="sxs-lookup"><span data-stu-id="fbd58-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="fbd58-107">Tento důležitý osvědčený postup poskytuje v budoucnosti flexibilitu pro aktualizaci nebo odebrání změn podle potřeby, pomůže při opětovném použití vaší práce a usnadní portování těchto změn na jinou instanci.</span><span class="sxs-lookup"><span data-stu-id="fbd58-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="fbd58-108">Po provedení všech požadovaných změn exportujte toto řešení jako **Spravované řešení** a importujte ho do jiných instancí za účelem znovupoužití vašeho nastavení cen.</span><span class="sxs-lookup"><span data-stu-id="fbd58-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="fbd58-109">Vytvoření vlastních polí a sad možností v řešení cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="fbd58-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="fbd58-110">Cenová dimenze může být sada možností nebo entita.</span><span class="sxs-lookup"><span data-stu-id="fbd58-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="fbd58-111">Obojí musí být vytvořeno ve vašem řešení ocenění.</span><span class="sxs-lookup"><span data-stu-id="fbd58-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="fbd58-112">Kroky v tomto postupu vysvětlují, jak vytvořit dimenze založené na entitě a dimenze založené na sadě možností.</span><span class="sxs-lookup"><span data-stu-id="fbd58-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="fbd58-113">Dimenze založené na entitě</span><span class="sxs-lookup"><span data-stu-id="fbd58-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="fbd58-114">V PSA klikněte na **Nastavení** > **Řešení** a pak dvakrát klikněte na **\<your organization name> cenové dimenze**.</span><span class="sxs-lookup"><span data-stu-id="fbd58-114">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="fbd58-115">V Průzkumníku řešení vyberte v levém navigačním podokně **Entity**.</span><span class="sxs-lookup"><span data-stu-id="fbd58-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="fbd58-116">Kliknutím na **Nová** vytvoříte novou entitu nazvanou **Standardní funkce**.</span><span class="sxs-lookup"><span data-stu-id="fbd58-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="fbd58-117">Zadejte zbývající požadované informace a klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="fbd58-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definice entity Standardní funkce](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="fbd58-119">Dimenze založené na sadě možností</span><span class="sxs-lookup"><span data-stu-id="fbd58-119">Option set-based dimensions</span></span> 
<span data-ttu-id="fbd58-120">Můžete vytvořit dvě dimenze založené na sadě možností.</span><span class="sxs-lookup"><span data-stu-id="fbd58-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="fbd58-121">Ke sledování ceny práce v místě **Domácí** a práce **U zákazníka** použijte **Místo výkonu práce zdroje** a chcete-li po dokončení práce použít přirážku, použijte **Pracovní dobu zdroje** s hodnotami **Normální** a **Přesčas**.</span><span class="sxs-lookup"><span data-stu-id="fbd58-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="fbd58-122">V PSA klikněte na **Nastavení** > **Řešení** a pak dvakrát klikněte na **\<your organization name> cenové dimenze**.</span><span class="sxs-lookup"><span data-stu-id="fbd58-122">In PSA, click **Settings** > **Solutions** , and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="fbd58-123">V Průzkumníku řešení vyberte v levém navigačním podokně **Sady možností**.</span><span class="sxs-lookup"><span data-stu-id="fbd58-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="fbd58-124">Kliknutím na **Nový** vytvořte novou sadu možností, zadejte zbývající požadované informace a poté klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="fbd58-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="fbd58-125">Cenová dimenze založená na sadě možností s názvem Místo výkonu práce zdroje</span><span class="sxs-lookup"><span data-stu-id="fbd58-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="fbd58-126">Cenová dimenze založená na sadě možností s názvem Pracovní doba zdroje</span><span class="sxs-lookup"><span data-stu-id="fbd58-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="fbd58-127">Vytvoření dat pro dimenze založené na entitě</span><span class="sxs-lookup"><span data-stu-id="fbd58-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="fbd58-128">Data lze pro dimenze založené na entitě vytvořit ručně nebo pomocí importu aplikace Microsoft Excel nebo volání služby.</span><span class="sxs-lookup"><span data-stu-id="fbd58-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="fbd58-129">Pomocí kroků v tomto postupu můžete z dimenze **Standardní funkce** , která je založena na entitě, vytvořit dvě standardní funkce, **Systémový technik** a **Hlavní systémový technik**.</span><span class="sxs-lookup"><span data-stu-id="fbd58-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="fbd58-130">Pokud jsou data, která chcete vytvořit, malá, jako v následujícím příkladu, můžete použít standardní formulář.</span><span class="sxs-lookup"><span data-stu-id="fbd58-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="fbd58-131">Klikněte v PSA na **Rozšířené hledání**.</span><span class="sxs-lookup"><span data-stu-id="fbd58-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="fbd58-132">Vyberte entitu **Standardní funkce** a poté klikněte na **Výsledky**.</span><span class="sxs-lookup"><span data-stu-id="fbd58-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="fbd58-133">Zobrazí se všechny řádky v entitě **Standardní funkce**.</span><span class="sxs-lookup"><span data-stu-id="fbd58-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="fbd58-134">Klikněte na **Nový**.</span><span class="sxs-lookup"><span data-stu-id="fbd58-134">Click **New**.</span></span> <span data-ttu-id="fbd58-135">Do pole **Název** zadejte „Systémový technik” a poté klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="fbd58-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="fbd58-136">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="fbd58-136">Close the form.</span></span> 
4. <span data-ttu-id="fbd58-137">Opakováním kroků 1–3 vytvořte další standardní funkci pro „Hlavního systémového technika”.</span><span class="sxs-lookup"><span data-stu-id="fbd58-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="fbd58-138">Ukázková data pro entitu Standardní funkce</span><span class="sxs-lookup"><span data-stu-id="fbd58-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


