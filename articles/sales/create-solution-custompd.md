---
title: Vytvoření řešení pro vlastní cenové dimenze
description: Toto téma obsahuje informace o vytvoření řešení vlastních cenových dimenzí.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010328"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="43b82-103">Vytvoření řešení pro vlastní cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="43b82-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="43b82-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="43b82-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="43b82-105">Všechny změny vlastních cenových dimenzí by měly být v samostatném řešení.</span><span class="sxs-lookup"><span data-stu-id="43b82-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="43b82-106">Tento důležitý osvědčený postup umožňuje flexibilitu při aktualizaci nebo odebrání změn podle potřeby, pomůže při opětovném použití vaší práce a usnadní portování těchto změn na jiné instance.</span><span class="sxs-lookup"><span data-stu-id="43b82-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="43b82-107">Po provedení všech požadovaných změn exportujte toto řešení jako **Spravované** řešení a pak jej importujte do jiných instancí za účelem znovupoužití.</span><span class="sxs-lookup"><span data-stu-id="43b82-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="43b82-108">Vytvoření řešení pro vlastní cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="43b82-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="43b82-109">Vyberte **Nastavení** > **Řešení** a pak vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="43b82-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="43b82-110">Pojmenujte řešení *Cenové dimenze <your organization name>*.</span><span class="sxs-lookup"><span data-stu-id="43b82-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="43b82-111">Zadejte zbývající požadované informace a zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="43b82-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Vytvoření řešení pro vlastní cenové dimenze](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="43b82-113">Přidání všech požadovaných entit a souvisejících komponent do řešení cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="43b82-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="43b82-114">Přidejte do svého cenového řešení následující entity Project Service, abyste mohli provést důležité změny schématu v cenovém řešení.</span><span class="sxs-lookup"><span data-stu-id="43b82-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="43b82-115">Po dokončení tohoto postupu entity rozpoznají nové dimenze cen.</span><span class="sxs-lookup"><span data-stu-id="43b82-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="43b82-116">Vyberte **Nastavení** > **Řešení** a potom klikněte dvakrát na **<*název vaší organizace*> cenové dimenze**.</span><span class="sxs-lookup"><span data-stu-id="43b82-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="43b82-117">V Průzkumníku řešení vyberte v levém navigačním podokně **Přidat existující** > **Entity**.</span><span class="sxs-lookup"><span data-stu-id="43b82-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="43b82-118">V dialogovém okně **Součásti řešení** vyberte následující entity:</span><span class="sxs-lookup"><span data-stu-id="43b82-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="43b82-119">**Skutečnost**</span><span class="sxs-lookup"><span data-stu-id="43b82-119">**Actual**</span></span>
   - <span data-ttu-id="43b82-120">**Rezervovatelný zdroj**</span><span class="sxs-lookup"><span data-stu-id="43b82-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="43b82-121">**Řádek odhadu**</span><span class="sxs-lookup"><span data-stu-id="43b82-121">**Estimate Line**</span></span>
   - <span data-ttu-id="43b82-122">**Projektový úkol**</span><span class="sxs-lookup"><span data-stu-id="43b82-122">**Project Task**</span></span>
   - <span data-ttu-id="43b82-123">**Podrobnosti řádku faktury**</span><span class="sxs-lookup"><span data-stu-id="43b82-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="43b82-124">**Řádek deníku**</span><span class="sxs-lookup"><span data-stu-id="43b82-124">**Journal Line**</span></span>
   - <span data-ttu-id="43b82-125">**Podrobnosti řádku projektové smlouvy**</span><span class="sxs-lookup"><span data-stu-id="43b82-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="43b82-126">**Člen projektového týmu**</span><span class="sxs-lookup"><span data-stu-id="43b82-126">**Project Team Member**</span></span>
   - <span data-ttu-id="43b82-127">**Podrobnosti řádku nabídky**</span><span class="sxs-lookup"><span data-stu-id="43b82-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="43b82-128">**Přirážka ceny role**</span><span class="sxs-lookup"><span data-stu-id="43b82-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="43b82-129">**Cena role**</span><span class="sxs-lookup"><span data-stu-id="43b82-129">**Role Price**</span></span>
   - <span data-ttu-id="43b82-130">**Časový záznam**</span><span class="sxs-lookup"><span data-stu-id="43b82-130">**Time Entry**</span></span>
 
   ![Přidat existující entity k vlastnímu řešení cenových dimenzí](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="43b82-132">U každé entity zkontrolujte přidávané komponenty a konečný seznam prostředků entit pro každou entitu.</span><span class="sxs-lookup"><span data-stu-id="43b82-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="43b82-133">Zahrňte všechny formuláře a zobrazení pro všechny vybrané entity.</span><span class="sxs-lookup"><span data-stu-id="43b82-133">Include all forms and views for each of the selected entities.</span></span>

  ![Přidané entity](./media/solution-component-selection.png)


5.  <span data-ttu-id="43b82-135">Po zobrazení výzvy k zahrnutí jakýchkoli závislých entit pro vybrané entity vyberte **Ne, nezahrnovat požadované součásti.**</span><span class="sxs-lookup"><span data-stu-id="43b82-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Včetně závislých entit](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]