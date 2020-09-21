---
title: Zobrazení fakturovatelného využití zdrojů
description: Toto téma obsahuje informace o zobrazení využití zdrojů.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 656511ac-6851-42d6-abd4-0c7e77ea5d9c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8953015ced24ff10f0bec2570a840cf4e130b01a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750283"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="48c56-103">Zobrazení fakturovatelného využití zdrojů</span><span class="sxs-lookup"><span data-stu-id="48c56-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="48c56-104">**Zobrazení využití** na stránce **Využití zdrojů v Project Service** zobrazuje fakturovatelné využití pro každý rezervovatelný zdroj.</span><span class="sxs-lookup"><span data-stu-id="48c56-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="48c56-105">Protože je zobrazení založeno na plánovací vývěsce, naleznete tam mnoho stejných funkcí.</span><span class="sxs-lookup"><span data-stu-id="48c56-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Obrazovka Zobrazení využití](media/FAQ-utilization-1.png)
 

<span data-ttu-id="48c56-107">Výpočet fakturovatelného využití probíhá takto:</span><span class="sxs-lookup"><span data-stu-id="48c56-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="48c56-108">Fakturovatelné využití = (skutečné fakturovatelné hodiny) / (kapacita zdroje)</span><span class="sxs-lookup"><span data-stu-id="48c56-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="48c56-109">Buňky představují vypočítané fakturovatelné využití za vybrané období (dny, týdny nebo měsíce).</span><span class="sxs-lookup"><span data-stu-id="48c56-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="48c56-110">Barvy v každé buňce zobrazují fakturovatelné využití zdroje ve srovnání s jejich cílovým fakturovatelným využitím.</span><span class="sxs-lookup"><span data-stu-id="48c56-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="48c56-111">Cílové využití může být nastaveno na výchozí roli zdroje nebo na samotném jednotlivém zdroji.</span><span class="sxs-lookup"><span data-stu-id="48c56-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="48c56-112">Výpočet pohlíží nejdříve na jednotlivé pro cíl, a pak na výchozí roli zdroje.</span><span class="sxs-lookup"><span data-stu-id="48c56-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="48c56-113">Nastavení cíle u zdroje</span><span class="sxs-lookup"><span data-stu-id="48c56-113">Set target on a resource</span></span>

1. <span data-ttu-id="48c56-114">Přejděte na **Zdroje** \> **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="48c56-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="48c56-115">Vyberte zdroj pro otevření záznamu.</span><span class="sxs-lookup"><span data-stu-id="48c56-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="48c56-116">Na kartě **Project Service** můžete nastavit cílové využití zdroje.</span><span class="sxs-lookup"><span data-stu-id="48c56-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Snímek obrazovky s použitím karty Project Service pro nastavení cílového využití](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="48c56-118">Nastavení cílového využití u role</span><span class="sxs-lookup"><span data-stu-id="48c56-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="48c56-119">Přejděte na **Zdroje** \> **Role zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="48c56-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="48c56-120">Vyberte roli a otevřete záznam.</span><span class="sxs-lookup"><span data-stu-id="48c56-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="48c56-121">Nastavte cílové využití pro roli.</span><span class="sxs-lookup"><span data-stu-id="48c56-121">Set the target utilization for the role.</span></span>

> ![Snímek obrazovky s použitím možnosti Role zdroje pro nastavení cílového využití](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="48c56-123">Výpočet fakturovatelného využití zdroje</span><span class="sxs-lookup"><span data-stu-id="48c56-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="48c56-124">Pro výpočet fakturovatelného využití zdroje budete muset splnit některé předpoklady.</span><span class="sxs-lookup"><span data-stu-id="48c56-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="48c56-125">Nastavení výchozí role pro individuální zdroj</span><span class="sxs-lookup"><span data-stu-id="48c56-125">Set default role for individual resource</span></span>

<span data-ttu-id="48c56-126">Za prvé, cílové využití musí být nastaveno buď na jednotlivý zdroj nebo na role zdroje.</span><span class="sxs-lookup"><span data-stu-id="48c56-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="48c56-127">Pokud používáte role zdroje pro cíle, musí mít každý jednotlivý zdroj výchozí roli.</span><span class="sxs-lookup"><span data-stu-id="48c56-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="48c56-128">Pro toto nastavení přejděte na **Zdroje** \> **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="48c56-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="48c56-129">Vyberte zdroj, otevřete záznam a pak vyberte kartu služba **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="48c56-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="48c56-130">V mřížce **Role zdroje** se ujistěte, že pro daný zdroj existuje jedna role a **Je výchozí** je nastaveno na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="48c56-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="48c56-131">Změna typu fakturace pro roli zdroje</span><span class="sxs-lookup"><span data-stu-id="48c56-131">Change billing type for resource role</span></span>

<span data-ttu-id="48c56-132">Role zdroje musí být nastaveny tak, aby měly typ fakturace **Účtovatelný**.</span><span class="sxs-lookup"><span data-stu-id="48c56-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="48c56-133">Přejděte na **Zdroje** \> **Role zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="48c56-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="48c56-134">Otevřete záznam, který chcete aktualizovat a poté nastavte výchozí typ fakturace na **Účtovatelný**.</span><span class="sxs-lookup"><span data-stu-id="48c56-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="48c56-135">Nastavení pracovní doby pro roli zdroje</span><span class="sxs-lookup"><span data-stu-id="48c56-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="48c56-136">Zdroj musí mít pracovní dobu pro výpočet kapacity.</span><span class="sxs-lookup"><span data-stu-id="48c56-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="48c56-137">Přejděte na **Zdroje** \> **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="48c56-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="48c56-138">Vyberte zdroj pro otevření záznamu a pak vyberte **Zobrazit pracovní dobu**.</span><span class="sxs-lookup"><span data-stu-id="48c56-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="48c56-139">Je možná hromadná aktualizace seznamu zdrojů použitím **Šablony pracovní doby** ze zobrazení **Seznam zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="48c56-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="48c56-140">Poradce při potížích se skutečnými fakturovatelnými hodinami</span><span class="sxs-lookup"><span data-stu-id="48c56-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="48c56-141">Skutečné fakturovatelné hodiny pocházejí z entity **Skutečné hodnoty**.</span><span class="sxs-lookup"><span data-stu-id="48c56-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="48c56-142">Skutečné hodnoty s typem fakturace **Účtovatelné** jsou zahrnuty do výpočtu a z tohoto důvodu musíte mít projekty, kde jsou skutečné hodnoty účtovatelné.</span><span class="sxs-lookup"><span data-stu-id="48c56-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="48c56-143">Pokud nevidíte fakturovatelné využití, zde je několik věcí, které můžete zkontrolovat:</span><span class="sxs-lookup"><span data-stu-id="48c56-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="48c56-144">Zdroj má definovanou pracovní dobu pro kapacitu.</span><span class="sxs-lookup"><span data-stu-id="48c56-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="48c56-145">Zdroj má buď individuálně definovaný cíl využití nebo má k němu přiřazenou výchozí roli.</span><span class="sxs-lookup"><span data-stu-id="48c56-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="48c56-146">Role má definován cíl využití.</span><span class="sxs-lookup"><span data-stu-id="48c56-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="48c56-147">Skutečné hodnoty mají pro období, pro které očekáváte výpočet využití, typ fakturace **Účtovatelné**.</span><span class="sxs-lookup"><span data-stu-id="48c56-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="48c56-148">Pokud se skutečné hodnoty zobrazují s jinými typy fakturace než účtovatelné, zkontrolujte následující:</span><span class="sxs-lookup"><span data-stu-id="48c56-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="48c56-149">Role použitá pro skutečné hodnoty má výchozí typ fakturace jiný než fakturovatelný.</span><span class="sxs-lookup"><span data-stu-id="48c56-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="48c56-150">Role na řádku smlouvy projektu byla nastavena na nefakturovatelnou.</span><span class="sxs-lookup"><span data-stu-id="48c56-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="48c56-151">Projekt nemá přidružený řádek smlouvy.</span><span class="sxs-lookup"><span data-stu-id="48c56-151">The project does not have an associated contract line.</span></span>

