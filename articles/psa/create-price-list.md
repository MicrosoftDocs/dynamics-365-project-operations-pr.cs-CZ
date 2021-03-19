---
title: Vytvoření ceníku
description: Postup vytvoření ceníku v Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0732ccca43e404412efae8a91873e43c28d041ca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290306"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="569e8-103">Vytvoření ceníku (Project Service)</span><span class="sxs-lookup"><span data-stu-id="569e8-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="569e8-104">Ceníky poskytují šablonu, kterou mohou vaši manažeři použít ke tvorbě nabídek a projektů a pro stanovení nákladů projektu.</span><span class="sxs-lookup"><span data-stu-id="569e8-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="569e8-105">Poskytují seznam položek řádku rolí a nákladů, stejně jako ceny, které za ně budete účtovat.</span><span class="sxs-lookup"><span data-stu-id="569e8-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="569e8-106">Můžete vytvořit několik ceníků, abyste mohli udržovat samostatné struktury cen pro různé regiony, v nichž prodáváte své produkty, nebo pro různé prodejní kanály.</span><span class="sxs-lookup"><span data-stu-id="569e8-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="569e8-107">Je vhodné vytvořit alespoň jeden ceník pro každou měnu, kterou budete chtít používat k fakturaci zákazníků.</span><span class="sxs-lookup"><span data-stu-id="569e8-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="569e8-108">Chcete-li vytvořit finanční odhady pro dodávané práce, zkontrolujte, zda má každý projekt seznam pomocných nákladů a prodejních cen.</span><span class="sxs-lookup"><span data-stu-id="569e8-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="569e8-109">Nastavte výchozí nákladový a prodejní ceník, který platí pro všechny projekty vytvořené v organizaci.</span><span class="sxs-lookup"><span data-stu-id="569e8-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="569e8-110">Ceníky jsou závislé na rolích a kategoriích výdajů, proto se před vytvořením ceníku přesvědčte, zda jste již nakonfigurovali role a výdajové kategorie, které chcete použít při vytváření ceníku.</span><span class="sxs-lookup"><span data-stu-id="569e8-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="569e8-111">Přejděte do části **Project Service > Ceníky**.</span><span class="sxs-lookup"><span data-stu-id="569e8-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="569e8-112">Klikněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="569e8-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="569e8-113">V části **Kontext** vyberte, zda je tento ceník pro **Náklady**, **Nákup** nebo **Prodej**.</span><span class="sxs-lookup"><span data-stu-id="569e8-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="569e8-114">Do pole **Název** zadejte název pro tento ceník.</span><span class="sxs-lookup"><span data-stu-id="569e8-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="569e8-115">V poli **Měna** vyberte měnu, kterou chcete použít pro účtování a oceňování.</span><span class="sxs-lookup"><span data-stu-id="569e8-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="569e8-116">V poli **Časová jednotka** určete dobu, k níž se cena vztahuje, například den nebo hodinu.</span><span class="sxs-lookup"><span data-stu-id="569e8-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="569e8-117">Podle potřeby vyplňte pole  **Počáteční datum**, **Koncové datum** a **Popis**.</span><span class="sxs-lookup"><span data-stu-id="569e8-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="569e8-118">Kliknutím na tlačítko **Uložit** vytvořte záznam, abyste mohli pokračovat v jeho úpravách.</span><span class="sxs-lookup"><span data-stu-id="569e8-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="569e8-119">Chcete-li přidat cenu role do ceníku, klikněte na tlačítko **+** pod polem **Ceny rolí.**.</span><span class="sxs-lookup"><span data-stu-id="569e8-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="569e8-120">V podokně **Cena role** vyplňte údaje a poté klikněte na položku **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="569e8-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="569e8-121">Pokračujte podle potřeby v přidávání cen rolí.</span><span class="sxs-lookup"><span data-stu-id="569e8-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="569e8-122">Když jste hotovi, klikněte na tlačítko **Uložit** v pravém dolním rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="569e8-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="569e8-123">Chcete-li přidat cenu kategorie výdajů do ceníku, klikněte na tlačítko **+** pod polem **Ceny kategorií**.</span><span class="sxs-lookup"><span data-stu-id="569e8-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="569e8-124">V podokně **Cena kategorie transakce** vyplňte údaje a poté klikněte na položku **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="569e8-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="569e8-125">Pokračujte podle potřeby v přidávání cen kategorií.</span><span class="sxs-lookup"><span data-stu-id="569e8-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="569e8-126">Když jste hotovi, klikněte na tlačítko **Uložit** v pravém dolním rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="569e8-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="569e8-127">Chcete-li přidat položky ceníku do ceníku, klikněte na tlačítko **+** pod částí **Položky ceníku**.</span><span class="sxs-lookup"><span data-stu-id="569e8-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="569e8-128">V podokně **Položka ceníku** vyplňte údaje a poté klikněte na položku **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="569e8-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="569e8-129">Pokračujte podle potřeby v přidávání položek ceníku.</span><span class="sxs-lookup"><span data-stu-id="569e8-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="569e8-130">Když jste hotovi, klikněte na tlačítko **Uložit** v pravém dolním rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="569e8-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="569e8-131">Chcete-li přidat vztahy mezi oblastmi do ceníku, klikněte na tlačítko **+** pod částí **Vztahy mezi oblastmi**.</span><span class="sxs-lookup"><span data-stu-id="569e8-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="569e8-132">V okně **Nové připojení** vyplňte údaje a poté klikněte na položku **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="569e8-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="569e8-133">Pokračujte podle potřeby v přidávání vztahů mezi oblastmi.</span><span class="sxs-lookup"><span data-stu-id="569e8-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="569e8-134">Když jste hotovi, klikněte na tlačítko **Uložit** v pravém dolním rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="569e8-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="569e8-135">Viz také</span><span class="sxs-lookup"><span data-stu-id="569e8-135">See Also</span></span>  
 [<span data-ttu-id="569e8-136">Konfigurace Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="569e8-136">Configure Project Service Automation</span></span>](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]