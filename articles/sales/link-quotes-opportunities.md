---
title: Vytváření projektových nabídek z příležitostí
description: Tento téma poskytuje informace o otevírání nabídky projektu z příležitosti.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898524"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="1a956-103">Vytváření projektových nabídek z příležitostí</span><span class="sxs-lookup"><span data-stu-id="1a956-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="1a956-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="1a956-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1a956-105">Nabídky lze vytvářet z projektových příležitostí následujícími způsoby:</span><span class="sxs-lookup"><span data-stu-id="1a956-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="1a956-106">Na kartě **Nabídky** na stránce **Příležitost projektu**</span><span class="sxs-lookup"><span data-stu-id="1a956-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="1a956-107">Z toku prodejního procesu příležitosti</span><span class="sxs-lookup"><span data-stu-id="1a956-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="1a956-108">Aktualizací odkazu na příležitost u existující nabídky</span><span class="sxs-lookup"><span data-stu-id="1a956-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="1a956-109">Na kartě Nabídky na stránce Příležitost projektu</span><span class="sxs-lookup"><span data-stu-id="1a956-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="1a956-110">Chcete-li vytvořit nabídku projektu z příležitosti, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="1a956-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="1a956-111">Otevřete stránku **Příležitost projektu** a vyberte kartu **Nabídky**.</span><span class="sxs-lookup"><span data-stu-id="1a956-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="1a956-112">Na podmřížce **Nabídky** vyberte **+** a vytvořte novou nabídku projektu na základě příležitosti.</span><span class="sxs-lookup"><span data-stu-id="1a956-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="1a956-113">Všechny řádky příležitostí a související ceníky projektu jsou zkopírovány do nové nabídky příležitosti.</span><span class="sxs-lookup"><span data-stu-id="1a956-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="1a956-114">Z toku prodejního procesu příležitosti</span><span class="sxs-lookup"><span data-stu-id="1a956-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="1a956-115">Chcete-li vytvořit nabídku projektu z toku prodejního procesu příležitosti, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="1a956-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="1a956-116">V toku prodejního procesu příležitosti otevřete příležitost.</span><span class="sxs-lookup"><span data-stu-id="1a956-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="1a956-117">Vyberte fázi **Zařadit**.</span><span class="sxs-lookup"><span data-stu-id="1a956-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="1a956-118">Vyberte **Další** a poté vyberte **+ Vytvořit** pro vytvoření nové nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a956-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="1a956-119">Většina informací na kartě **Souhrn** pro tuto novou nabídku bude ve výchozím nastavení z této příležitosti.</span><span class="sxs-lookup"><span data-stu-id="1a956-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="1a956-120">Zadejte všechny požadované informace, které chybí, nebo podle potřeby aktualizujte výchozí hodnoty na kartě **Souhrn**.</span><span class="sxs-lookup"><span data-stu-id="1a956-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="1a956-121">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="1a956-121">Select **Save**.</span></span> <span data-ttu-id="1a956-122">Nová nabídka je vytvořena a přidružena k příležitosti.</span><span class="sxs-lookup"><span data-stu-id="1a956-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="1a956-123">Nyní si můžete zobrazit informace o nabídce na kartě **Nabídky** na stránce **Příležitost**.</span><span class="sxs-lookup"><span data-stu-id="1a956-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="1a956-124">Proces prodeje příležitosti přechází do další fáze **Návrh**.</span><span class="sxs-lookup"><span data-stu-id="1a956-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="1a956-125">Aktualizací odkazu na příležitost u existující nabídky</span><span class="sxs-lookup"><span data-stu-id="1a956-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="1a956-126">Stávající nabídku lze propojit s příležitostí.</span><span class="sxs-lookup"><span data-stu-id="1a956-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="1a956-127">Chcete-li aktualizovat informace o příležitosti u existující nabídky, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="1a956-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="1a956-128">Otevřete stránku **Nabídka** a vyberte kartu **Souhrn**.</span><span class="sxs-lookup"><span data-stu-id="1a956-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="1a956-129">V poli **Příležitost** vyberte příležitost, kterou chcete propojit s nabídkou.</span><span class="sxs-lookup"><span data-stu-id="1a956-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="1a956-130">Nabídku můžete vidět v mřížce **Nabídky** příležitosti.</span><span class="sxs-lookup"><span data-stu-id="1a956-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="1a956-131">Pomocí prodejního procesu příležitosti lze příležitost posunout do další fáze **Návrh**.</span><span class="sxs-lookup"><span data-stu-id="1a956-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="1a956-132">Když přesunete příležitost do této fáze, můžete vybrat tuto nabídku ze seznamu nabídek spojených s touto příležitostí.</span><span class="sxs-lookup"><span data-stu-id="1a956-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="1a956-133">Výběr této nabídky znamená, že se s ní pohybujete kupředu.</span><span class="sxs-lookup"><span data-stu-id="1a956-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="1a956-134">Všechny ostatní nabídky spojené s touto nabídkou budou stále k dispozici a aktivní, dokud jednu z nich nezískáte.</span><span class="sxs-lookup"><span data-stu-id="1a956-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="1a956-135">Proces prodeje můžete přesunout zpět do předchozí fáze **Zařadit** a vybrat další nabídku, se kterou budete pokračovat.</span><span class="sxs-lookup"><span data-stu-id="1a956-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
