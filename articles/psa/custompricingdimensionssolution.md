---
title: Vytvoření vlastních řešení pro cenové dimenze
description: Toto téma vysvětluje, jak vytvořit vlastní řešení při vytváření vlastních cenových dimenzí.
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
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073789"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="8bb27-103">Vytvoření vlastních řešení pro cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="8bb27-103">Create custom solutions for pricing dimensions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8bb27-104">Všechny změny vlastních cenových dimenzí by měly být v samostatném řešení.</span><span class="sxs-lookup"><span data-stu-id="8bb27-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="8bb27-105">Tento důležitý osvědčený postup poskytuje v budoucnosti flexibilitu pro aktualizaci nebo odebrání změn podle potřeby, pomůže při opětovném použití vaší práce a usnadní portování těchto změn na jinou instanci.</span><span class="sxs-lookup"><span data-stu-id="8bb27-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="8bb27-106">Po provedení všech požadovaných změn exportujte toto řešení jako **Spravované řešení** a importujte ho do jiných instancí za účelem znovupoužití vašeho nastavení cen.</span><span class="sxs-lookup"><span data-stu-id="8bb27-106">After you make the required changes, export this solution as a **Managed solution** , and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="8bb27-107">Vyberte **Nastavení** > **Řešení** a pak vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="8bb27-107">Select **Settings** > **Solutions** , and then select **New**.</span></span> 
2. <span data-ttu-id="8bb27-108">Řešení nazvěte **\<your organization name> cenové dimenze** , zadejte zbývající požadované informace a poté vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8bb27-108">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>

> ![Vytvoření vlastního řešení pro cenové dimenze](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="8bb27-110">Přidání všech požadovaných entit a souvisejících komponent do řešení cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="8bb27-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="8bb27-111">K vašemu řešení ocenění bude nutné přidat následující entity Project Service.</span><span class="sxs-lookup"><span data-stu-id="8bb27-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="8bb27-112">Provedením kroků v tomto postupu můžete provést některé důležité změny schématu v řešení ocenění, aby si entity všimly nových cenových dimenzí.</span><span class="sxs-lookup"><span data-stu-id="8bb27-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="8bb27-113">Zvolte **Nastavení** > **Řešení** a pak dvakrát klikněte na **\<your organization name> cenové dimenze**.</span><span class="sxs-lookup"><span data-stu-id="8bb27-113">Select **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="8bb27-114">V Průzkumníku řešení vyberte v levém navigačním podokně **Přidat existující** > **Entity**.</span><span class="sxs-lookup"><span data-stu-id="8bb27-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="8bb27-115">V dialogovém okně **Součásti řešení** vyberte následující entity:</span><span class="sxs-lookup"><span data-stu-id="8bb27-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="8bb27-116">Skutečnost</span><span class="sxs-lookup"><span data-stu-id="8bb27-116">Actual</span></span>
- <span data-ttu-id="8bb27-117">Rezervovatelný zdroj</span><span class="sxs-lookup"><span data-stu-id="8bb27-117">Bookable Resource</span></span>
- <span data-ttu-id="8bb27-118">Řádek odhadu</span><span class="sxs-lookup"><span data-stu-id="8bb27-118">Estimate Line</span></span>
- <span data-ttu-id="8bb27-119">Projektový úkol</span><span class="sxs-lookup"><span data-stu-id="8bb27-119">Project Task</span></span>
- <span data-ttu-id="8bb27-120">Podrobnosti řádku faktury</span><span class="sxs-lookup"><span data-stu-id="8bb27-120">Invoice Line Detail</span></span>
- <span data-ttu-id="8bb27-121">Řádek deníku</span><span class="sxs-lookup"><span data-stu-id="8bb27-121">Journal Line</span></span>
- <span data-ttu-id="8bb27-122">Podrobnosti řádku projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="8bb27-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="8bb27-123">Člen projektového týmu</span><span class="sxs-lookup"><span data-stu-id="8bb27-123">Project Team Member</span></span>
- <span data-ttu-id="8bb27-124">Podrobnosti řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="8bb27-124">Quote Line Detail</span></span>
- <span data-ttu-id="8bb27-125">Přirážka ceny role</span><span class="sxs-lookup"><span data-stu-id="8bb27-125">Role Price Markup</span></span>
- <span data-ttu-id="8bb27-126">Cena role</span><span class="sxs-lookup"><span data-stu-id="8bb27-126">Role Price</span></span> 
- <span data-ttu-id="8bb27-127">Časový záznam</span><span class="sxs-lookup"><span data-stu-id="8bb27-127">Time Entry</span></span> 

> ![Přidat existující entity k řešení cenových dimenzí](media/Existing-entities-to-PD-solution.png)

> ![Vybrat součásti řešení](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="8bb27-130">Nezapomeňte zahrnout všechny formuláře a zobrazení pro všechny vybrané entity.</span><span class="sxs-lookup"><span data-stu-id="8bb27-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="8bb27-131">Při zobrazení výzvy k zahrnutí všech závislých entit do vybraných entit zvolte **Ne**.</span><span class="sxs-lookup"><span data-stu-id="8bb27-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Nezahrnovat všechny související komponenty](media/Do-not-include-required.png)


