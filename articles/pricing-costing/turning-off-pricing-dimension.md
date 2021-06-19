---
title: Vypnutí cenové dimenze
description: Toto téma obsahuje informace o tom, jak vypnout cenové dimenze.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 7b7c1d1b3363c0d158fcf6fda532822354b852a3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004523"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="dca42-103">Vypnutí cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="dca42-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="dca42-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="dca42-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dca42-105">Možná budete muset každých několik let zkontrolovat a aktualizovat cenovou strategii.</span><span class="sxs-lookup"><span data-stu-id="dca42-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="dca42-106">Jakékoli aktualizace, které provedete, mohou vyžadovat, abyste vypnuli existující cenovou dimenzi a vytvořili novou.</span><span class="sxs-lookup"><span data-stu-id="dca42-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="dca42-107">Například jste mohli dříve oceňovat podle **Role**, ale nyní jste se rozhodli oceňovat podle **Pracovních zkušeností**.</span><span class="sxs-lookup"><span data-stu-id="dca42-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="dca42-108">To může vyžadovat vypnutí **Role** jako cenové dimenze a vytvoření **Pracovní zkušenosti** jako nové cenové dimenze.</span><span class="sxs-lookup"><span data-stu-id="dca42-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="dca42-109">Vypnutí cenové dimenze bez ohledu na to, zda je pole předem připravené nebo vlastní, lze provést nastavením polí **Použitelné na náklady** a **Použitelné na prodej** cenové dimenze na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="dca42-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="dca42-110">Když to však uděláte, může se zobrazit chybová zpráva **Cenovou dimenzi nelze aktualizovat ani odstranit, pokud existují přidružené cenové záznamy.**</span><span class="sxs-lookup"><span data-stu-id="dca42-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Chyba obchodního procesu při vypnutí cenové dimenze](media/Business-Process-Error.png)

<span data-ttu-id="dca42-112">Tato chybová zpráva značí, že existují cenové záznamy, které byly dříve nastaveny pro dimenzi, která je vypnuta.</span><span class="sxs-lookup"><span data-stu-id="dca42-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="dca42-113">Všechny záznamy **Cena role** a **Přirážka ceny role**, které odkazují na dimenzi, musí být odstraněny dříve, než bude možné použitelnost dimenze nastavit na **Ne.**</span><span class="sxs-lookup"><span data-stu-id="dca42-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="dca42-114">Toto pravidlo platí pro předem připravené i vlastní cenové dimenze, které jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="dca42-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="dca42-115">Důvodem tohoto ověření je, že záznam **Cena role** musí mít jedinečnou kombinaci dimenzí.</span><span class="sxs-lookup"><span data-stu-id="dca42-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="dca42-116">Například v ceníku s názvem **Nákladové sazby USA 2018** máte následující řádky **Cena role**.</span><span class="sxs-lookup"><span data-stu-id="dca42-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="dca42-117">Standardní funkce</span><span class="sxs-lookup"><span data-stu-id="dca42-117">Standard Title</span></span>         | <span data-ttu-id="dca42-118">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="dca42-118">Org Unit</span></span>    |<span data-ttu-id="dca42-119">Jednotka</span><span class="sxs-lookup"><span data-stu-id="dca42-119">Unit</span></span>   |<span data-ttu-id="dca42-120">Cena</span><span class="sxs-lookup"><span data-stu-id="dca42-120">Price</span></span>  |<span data-ttu-id="dca42-121">Měna</span><span class="sxs-lookup"><span data-stu-id="dca42-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="dca42-122">Systémový inženýr</span><span class="sxs-lookup"><span data-stu-id="dca42-122">Systems Engineer</span></span>|<span data-ttu-id="dca42-123">Contoso (USA)</span><span class="sxs-lookup"><span data-stu-id="dca42-123">Contoso US</span></span>|<span data-ttu-id="dca42-124">hod</span><span class="sxs-lookup"><span data-stu-id="dca42-124">Hour</span></span>| <span data-ttu-id="dca42-125">100</span><span class="sxs-lookup"><span data-stu-id="dca42-125">100</span></span>|<span data-ttu-id="dca42-126">USD</span><span class="sxs-lookup"><span data-stu-id="dca42-126">USD</span></span>|
| <span data-ttu-id="dca42-127">Senior systémový inženýr</span><span class="sxs-lookup"><span data-stu-id="dca42-127">Senior Systems Engineer</span></span>|<span data-ttu-id="dca42-128">Contoso (USA)</span><span class="sxs-lookup"><span data-stu-id="dca42-128">Contoso US</span></span>|<span data-ttu-id="dca42-129">hod</span><span class="sxs-lookup"><span data-stu-id="dca42-129">Hour</span></span>| <span data-ttu-id="dca42-130">150</span><span class="sxs-lookup"><span data-stu-id="dca42-130">150</span></span>| <span data-ttu-id="dca42-131">USD</span><span class="sxs-lookup"><span data-stu-id="dca42-131">USD</span></span>|


<span data-ttu-id="dca42-132">Pokud jako cenovou dimenzi vypnete **Standardní název** a modul ocenění vyhledává cenu, použije pouze hodnotu **Organizační jednotka** ze zadání.</span><span class="sxs-lookup"><span data-stu-id="dca42-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="dca42-133">Pokud je **Organizační jednotka** v zadání „Contoso US“, výsledek bude nedeterministický, protože oba řádky budou shodné.</span><span class="sxs-lookup"><span data-stu-id="dca42-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="dca42-134">Chcete-li se vyhnout tomuto scénáři, při vytváření záznamů **Cena role** systém ověří, zda je kombinace dimenzí jedinečná.</span><span class="sxs-lookup"><span data-stu-id="dca42-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="dca42-135">Pokud je dimenze po vytvoření záznamů **Cena role** vypnutá, může být toto omezení porušeno.</span><span class="sxs-lookup"><span data-stu-id="dca42-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="dca42-136">Proto je nutné, aby před vypnutím dimenze byly odstraněny všechny řádky **Cena role** a **Přirážka ceny role**, které mají tuto hodnotu dimenze vyplněnou.</span><span class="sxs-lookup"><span data-stu-id="dca42-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]