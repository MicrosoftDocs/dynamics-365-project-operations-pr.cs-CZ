---
title: Měna
description: Tento téma poskytuje informace o tom, jak přidávat a odebírat typy měn v Project Operations.
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
ms.openlocfilehash: d53bae2f64e7b427f762161ff08917598217bb5a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898343"
---
# <a name="currency"></a><span data-ttu-id="c9322-103">Měna</span><span class="sxs-lookup"><span data-stu-id="c9322-103">Currency</span></span>

<span data-ttu-id="c9322-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="c9322-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c9322-105">Měny určují ceny produktů, které obsahuje katalog produktů, a náklady na transakce, jako jsou prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="c9322-105">Currencies determine the prices for products in the product catalog and the cost of transactions, such as sales orders.</span></span> <span data-ttu-id="c9322-106">Pokud se vaši zákazníci nacházejí v různých zeměpisných oblastech, přidejte jejich měny, aby bylo možné spravovat transakce.</span><span class="sxs-lookup"><span data-stu-id="c9322-106">If your customers are spread across geographies, add their currencies to manage your transactions.</span></span> <span data-ttu-id="c9322-107">Přidejte měny, které jsou nejvhodnější pro vaše současné i budoucí obchodní potřeby.</span><span class="sxs-lookup"><span data-stu-id="c9322-107">Add the currencies that are most appropriate for your current and future business needs.</span></span>  

> [!NOTE]
> <span data-ttu-id="c9322-108">Pokud je vaše prostředí Common Data Service, jste v centru pro správu Power Platform a vyberete stránku **Měny** (**Prostředí** > [vyberte prostředí]> **Nastavení** > **Obchodování** > **Měny**), stránka bude prázdná.</span><span class="sxs-lookup"><span data-stu-id="c9322-108">If your environment is a Common Data Service environment, you are in the Power Platform admin center, and you select the **Currencies** page (**Environments** > [select environment] > **Settings** > **Business** > **Currencies**), the page will be blank.</span></span> <span data-ttu-id="c9322-109">Důvodem je, že nastavení měny není podporováno v prostředích Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c9322-109">This is because setting a currency is not supported in Common Data Service environments.</span></span>

## <a name="add-a-currency"></a><span data-ttu-id="c9322-110">Přidání měny</span><span class="sxs-lookup"><span data-stu-id="c9322-110">Add a currency</span></span>  
<span data-ttu-id="c9322-111">Než zahájíte tento postup, ověřte, zda vaše role zabezpečení obsahuje oprávnění správce systému.</span><span class="sxs-lookup"><span data-stu-id="c9322-111">Before you start this procedure, verify that your security role includes system admin permissions.</span></span> 

1. <span data-ttu-id="c9322-112">V centru pro správu Power Platform vyberte prostředí.</span><span class="sxs-lookup"><span data-stu-id="c9322-112">In the Power Platform admin center, select an environment.</span></span> 
2. <span data-ttu-id="c9322-113">Vyberte **Nastavení** > **Obchodní**.</span><span class="sxs-lookup"><span data-stu-id="c9322-113">Select **Settings** > **Business**.</span></span>
3. <span data-ttu-id="c9322-114">Vyberte **Měny**.</span><span class="sxs-lookup"><span data-stu-id="c9322-114">Select **Currencies**.</span></span>  
4. <span data-ttu-id="c9322-115">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="c9322-115">Select **New**.</span></span>  
5. <span data-ttu-id="c9322-116">Podle potřeby doplňte odpovídající informace.</span><span class="sxs-lookup"><span data-stu-id="c9322-116">Fill in the information, as required.</span></span>  


   |          <span data-ttu-id="c9322-117">Pole</span><span class="sxs-lookup"><span data-stu-id="c9322-117">Field</span></span>          |                                                                                                                                                                                                                                                                                                                                                                            <span data-ttu-id="c9322-118">Popis</span><span class="sxs-lookup"><span data-stu-id="c9322-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    <span data-ttu-id="c9322-119">**Typ měny**</span><span class="sxs-lookup"><span data-stu-id="c9322-119">**Currency Type**</span></span>    | <span data-ttu-id="c9322-120">- **Systém** – Tuto možnost vyberte, pokud chcete používat měny dostupné v modelem řízených aplikacích v Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c9322-120">- **System** - Select this option if you want to use the currencies available in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="c9322-121">Výběrem tlačítka **Vyhledávání** můžete měnu vyhledat.</span><span class="sxs-lookup"><span data-stu-id="c9322-121">To search for a currency,  select **Lookup**.</span></span> <span data-ttu-id="c9322-122">Když vyberete kód měny, pro vybrané měny se automaticky přidají **Název měny** a **Symbol měny**.</span><span class="sxs-lookup"><span data-stu-id="c9322-122">When you select a currency code, **Currency Name** and **Currency Symbol** are automatically added for the selected currency.</span></span><br /><span data-ttu-id="c9322-123">- **Vlastní** – Tuto možnost vyberte, pokud chcete přidat měnu, která není dostupná v modelem řízených aplikacích v Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c9322-123">- **Custom** - Select this option if you want to add a currency that's not available in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="c9322-124">V tomto případě je nutné ručně zadat hodnoty pro položky **Kód měny**, **Přesnost měny**, **Název měny**, **Symbol měny** a **Převod měny**.</span><span class="sxs-lookup"><span data-stu-id="c9322-124">In this case, you must manually enter the values for **Currency Code**, **Currency Precision**, **Currency Name**, **Currency Symbol**, and **Currency Conversion**.</span></span> |
   |    <span data-ttu-id="c9322-125">**Kód měny**</span><span class="sxs-lookup"><span data-stu-id="c9322-125">**Currency Code**</span></span>    |                                                                                                                                                                                                                                                                                                                                            <span data-ttu-id="c9322-126">Zkratka měny.</span><span class="sxs-lookup"><span data-stu-id="c9322-126">Short form for the currency.</span></span> <span data-ttu-id="c9322-127">Například **USD** pro americký dolar.</span><span class="sxs-lookup"><span data-stu-id="c9322-127">For example, **USD** for United States Dollar.</span></span>                                                                                                                                                                                                                                                                                                                                            |
   | <span data-ttu-id="c9322-128">**Přesnost měny**</span><span class="sxs-lookup"><span data-stu-id="c9322-128">**Currency Precision**</span></span>  |                                                                                                                                                                                  <span data-ttu-id="c9322-129">Zadejte počet desetinných míst, jež chcete použít pro tuto měnu.</span><span class="sxs-lookup"><span data-stu-id="c9322-129">Type the number of decimals that you want to use for the currency.</span></span>  <span data-ttu-id="c9322-130">Můžete přidat hodnotu mezi 0 a 4.</span><span class="sxs-lookup"><span data-stu-id="c9322-130">You can add a value between 0 and 4.</span></span> <span data-ttu-id="c9322-131">**Poznámka:** Pokud jste nastavili hodnotu přesnosti v dialogovém okně **Nastavení systému**, tato hodnota se zde zobrazí.</span><span class="sxs-lookup"><span data-stu-id="c9322-131">**Note:**  If you've set a precision value in the **System Settings** dialog box, that value will appear here.</span></span>                                                                                                                                                                                  |
   |    <span data-ttu-id="c9322-132">**Název měny**</span><span class="sxs-lookup"><span data-stu-id="c9322-132">**Currency Name**</span></span>    |                                                                                                                                                                                                                                         <span data-ttu-id="c9322-133">Pokud jste vybrali kód měny ze seznamu dostupných měn v modelem řízených aplikacích v Dynamics 365, zobrazí se zde název měny pro vybraný kód.</span><span class="sxs-lookup"><span data-stu-id="c9322-133">If you selected a currency code from the list of available currencies in model-driven apps in Dynamics 365, the currency name for the selected code is displayed here.</span></span> <span data-ttu-id="c9322-134">Pokud jste vybrali jako typ měny položku **Vlastní**, zadejte název měny.</span><span class="sxs-lookup"><span data-stu-id="c9322-134">If you selected **Custom** as the currency type, type the name of the currency.</span></span>                                                                                                                                                                                                                                          |
   |   <span data-ttu-id="c9322-135">**Symbol měny**</span><span class="sxs-lookup"><span data-stu-id="c9322-135">**Currency Symbol**</span></span>   |                                                                                                                                                                                                                                                                      <span data-ttu-id="c9322-136">Pokud jste vybrali kód měny ze seznamu dostupných měn, zobrazí se zde symbol pro vybranou měnu.</span><span class="sxs-lookup"><span data-stu-id="c9322-136">If you selected a currency code from the list of available currencies, the symbol for the selected currency is displayed here.</span></span> <span data-ttu-id="c9322-137">Pokud jste vybrali jako typ měny položku **Vlastní**, zadejte symbol nové měny.</span><span class="sxs-lookup"><span data-stu-id="c9322-137">If you selected **Custom** as the currency type, enter the symbol for the new currency.</span></span>                                                                                                                                                                                                                                                                       |
   | <span data-ttu-id="c9322-138">**Převod měny**</span><span class="sxs-lookup"><span data-stu-id="c9322-138">**Currency Conversion**</span></span> |                                                                                                                                                                                                                                     <span data-ttu-id="c9322-139">Zadejte hodnotu vybrané měny vzhledem k jednomu americkému dolaru.</span><span class="sxs-lookup"><span data-stu-id="c9322-139">Type the value of the selected currency in terms of one US dollar.</span></span> <span data-ttu-id="c9322-140">Jedná se o částku, pomocí které se vybraná měna převádí na základní měnu.</span><span class="sxs-lookup"><span data-stu-id="c9322-140">This is the amount at which the selected currency converts to the base currency.</span></span> <span data-ttu-id="c9322-141">**Důležité:** Nazapomeňte tuto hodnotu často aktualizovat, aby se zabránilo nepřesným výpočtům v transakcích.</span><span class="sxs-lookup"><span data-stu-id="c9322-141">**Important:**  Make sure you update this value as frequently as required to avoid any inaccurate calculations in your transactions.</span></span>                                                                                                                                                                                                                                      |


6. <span data-ttu-id="c9322-142">Jakmile budete hotovi, na panelu příkazů vyberte tlačítko **Uložit** nebo **Uložit a zavřít**.</span><span class="sxs-lookup"><span data-stu-id="c9322-142">When you're done, on the command bar, select **Save** or **Save and Close**.</span></span>  

   > [!TIP]
   >  <span data-ttu-id="c9322-143">Chcete-li měnu upravit, vyberte měnu a poté zadejte nebo vyberte nové hodnoty.</span><span class="sxs-lookup"><span data-stu-id="c9322-143">To edit a currency, select the currency, and then enter or select the new values.</span></span>  

## <a name="delete-a-currency"></a><span data-ttu-id="c9322-144">Odstranění měny</span><span class="sxs-lookup"><span data-stu-id="c9322-144">Delete a currency</span></span>  

1. <span data-ttu-id="c9322-145">V centru pro správu Power Platform vyberte prostředí.</span><span class="sxs-lookup"><span data-stu-id="c9322-145">In the Power Platform admin center, select an environment.</span></span> 
2. <span data-ttu-id="c9322-146">Vyberte **Nastavení** > **Obchodní**.</span><span class="sxs-lookup"><span data-stu-id="c9322-146">Select **Settings** > **Business**.</span></span>
3. <span data-ttu-id="c9322-147">Vyberte **Měny**.</span><span class="sxs-lookup"><span data-stu-id="c9322-147">Select **Currencies**.</span></span>  
4. <span data-ttu-id="c9322-148">Ze zobrazeného seznamu měn vyberte měnu, kterou chcete odstranit.</span><span class="sxs-lookup"><span data-stu-id="c9322-148">From the list of currencies displayed, select the currency to delete.</span></span>  
5. <span data-ttu-id="c9322-149">Vyberte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="c9322-149">Select **Delete**.</span></span>  
6. <span data-ttu-id="c9322-150">Potvrďte odstranění.</span><span class="sxs-lookup"><span data-stu-id="c9322-150">Confirm the deletion.</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="c9322-151">Nelze odstranit měny, které se používají v jiných záznamech. Můžete je pouze deaktivovat.</span><span class="sxs-lookup"><span data-stu-id="c9322-151">You can't delete currencies that are in use by other records; you can only deactivate them.</span></span> <span data-ttu-id="c9322-152">Při deaktivaci záznamů měny nedojde k odebrání informací o měně uložených v existujících záznamech, například příležitostech nebo objednávkách.</span><span class="sxs-lookup"><span data-stu-id="c9322-152">Deactivating currency records doesn't remove the currency information stored in existing records, such as opportunities or orders.</span></span> <span data-ttu-id="c9322-153">Deaktivovanou měnu však nebudete moci vybrat pro nové transakce.</span><span class="sxs-lookup"><span data-stu-id="c9322-153">However, you won't be able to select the deactivated currency for new transactions.</span></span>  