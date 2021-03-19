---
title: Aktualizace atributů modulů plug-in o nové cenové dimenze
description: Toto téma obsahuje informace o aktualizaci atributů modulů plug-in o cenové dimenze.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274675"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="2c217-103">Aktualizace atributů modulů plug-in o nové cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="2c217-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="2c217-104">Toto téma obsahuje informace o aktualizaci atributů modulů plug-in o cenové dimenze.</span><span class="sxs-lookup"><span data-stu-id="2c217-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="2c217-105">Toto téma se vztahuje pouze na funkce nabídek a smluv v Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="2c217-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2c217-106">Požadavky</span><span class="sxs-lookup"><span data-stu-id="2c217-106">Prerequisites</span></span>
<span data-ttu-id="2c217-107">Než dokončíte kroky v tomto téma, musíte mít dokončené postupy v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="2c217-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="2c217-108">Vytvoření vlastních polí a entit</span><span class="sxs-lookup"><span data-stu-id="2c217-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="2c217-109">Přidání vlastních polí do nastavení ceny a transakčních entit </span><span class="sxs-lookup"><span data-stu-id="2c217-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="2c217-110">[Nastavení vlastních polí jako cenových dimenzí ](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="2c217-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="2c217-111">Pokud jste tyto postupy nedokončili, dokončete je a vraťte se k tomuto tématu.</span><span class="sxs-lookup"><span data-stu-id="2c217-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="2c217-112">Registrace modulů plug-in</span><span class="sxs-lookup"><span data-stu-id="2c217-112">Register a plug-in</span></span>
<span data-ttu-id="2c217-113">Když je vytvořen detail řádku nabídky na stránce **Řádek nabídky** pro řádek nabídky projektu, systém vytvoří dva řádky odhadu.</span><span class="sxs-lookup"><span data-stu-id="2c217-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="2c217-114">Jeden řádek je na straně nákladů odhadu a druhý řádek na straně prodeje.</span><span class="sxs-lookup"><span data-stu-id="2c217-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="2c217-115">To je stejné pro řádky projektové smlouvy.</span><span class="sxs-lookup"><span data-stu-id="2c217-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="2c217-116">Pokud změníte množství nebo pole na straně nákladů, tato změna se projeví i na straně prodeje.</span><span class="sxs-lookup"><span data-stu-id="2c217-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="2c217-117">To je možné, protože moduly plug-in PreOperation na Quotelinedetail a entity podrobností řádků smlouvy spojují konkrétní atributy na straně nákladů s prodejní stranou transakce.</span><span class="sxs-lookup"><span data-stu-id="2c217-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="2c217-118">Pokud potřebujete provést změny hodnot cenové dimenze na prodejní straně i na straně nákladů, je nutné po provedení změn cenové dimenze znovu zaregistrovat následující doplňky.</span><span class="sxs-lookup"><span data-stu-id="2c217-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="2c217-119">Následujcí moduly plug-in je třeba aktualizovat a znovu registrovat:</span><span class="sxs-lookup"><span data-stu-id="2c217-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="2c217-120">PreOperationContractLineDetailUpdate – Aktualizujte **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="2c217-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="2c217-121">PreOperationQuoteLineDetailUpdate – Aktualizujte **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="2c217-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="2c217-122">Pomocí následujících kroků aktualizujte a znovu zaregistrujte moduly plug-in.</span><span class="sxs-lookup"><span data-stu-id="2c217-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="2c217-123">Ortevřete **PluginRegistrationTool** a připojte se ke svému prostředí Project Operations Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2c217-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="2c217-124">Vyberte **Vyhledávání** a zadejte několik prvních písmen pluginu, který má být aktualizován.</span><span class="sxs-lookup"><span data-stu-id="2c217-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="2c217-125">Po nalezení modulu plug-in jej vyberte a vyberte **Vybrat v hlavním formuláři**.</span><span class="sxs-lookup"><span data-stu-id="2c217-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="2c217-126">Vyberte krok **Aktualizujte msdyn_orderlinetransaction**, klikněte pravým tlačítkem myši a vyberte **Aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="2c217-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="2c217-127">V dialogovém okně **Aktualizovat** vyberte tři tečky (**...**) v atributech filtrování.</span><span class="sxs-lookup"><span data-stu-id="2c217-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="2c217-128">Otevře se okno filtrování atributů a poskytuje seznam všech atributů v entitě a dimenzích cen.</span><span class="sxs-lookup"><span data-stu-id="2c217-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="2c217-129">Zaškrtněte políčka u atributů dimenze cen.</span><span class="sxs-lookup"><span data-stu-id="2c217-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="2c217-130">Výběrem **OK** zavřete stránku a pak vyberte možnost **Aktualizovat krok**.</span><span class="sxs-lookup"><span data-stu-id="2c217-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="2c217-131">Opakujte kroky 2 až 7 pro druhý modul plug-in **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="2c217-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="2c217-132">Pro tento modul plug-in musíte aktualizovat krok **Aktualizujte msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="2c217-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="2c217-133">Zavřete **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="2c217-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]