---
title: Vypnutí cenové dimenze
description: Toto téma ukazuje, jak nastavit cenové dimenze v řešení Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 689e5a8d-e39a-471d-a6c4-7e2fc3bb5590
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5cf2cd86fb1eba50c8e08b2bd624669ab0b1deb3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750373"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="4dc83-103">Vypnutí cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="4dc83-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="4dc83-104">Možná budete muset každých několik let zkontrolovat a aktualizovat cenovou strategii.</span><span class="sxs-lookup"><span data-stu-id="4dc83-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="4dc83-105">Jakékoli aktualizace, které provedete, mohou vyžadovat, abyste vypnuli existující cenovou dimenzi a vytvořili novou.</span><span class="sxs-lookup"><span data-stu-id="4dc83-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="4dc83-106">Například jste mohli dříve oceňovat podle **Role**, ale nyní jste se rozhodli oceňovat podle **Pracovních zkušeností**.</span><span class="sxs-lookup"><span data-stu-id="4dc83-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="4dc83-107">To může vyžadovat vypnutí **Role** jako cenové dimenze a vytvoření **Pracovní zkušenosti** jako nové cenové dimenze.</span><span class="sxs-lookup"><span data-stu-id="4dc83-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="4dc83-108">Vypnutí cenové dimenze bez ohledu na to, zda je pole předem připravené nebo vlastní, lze provést nastavením polí **Použitelné na náklady** a **Použitelné na prodej** cenové dimenze na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="4dc83-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="4dc83-109">Pokud to však uděláte, může se zobrazit následující chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="4dc83-109">However, when you do this, you might receive the following error message.</span></span>

![Chyba obchodního procesu při vypnutí cenové dimenze](media/Business-Process-Error.png)


<span data-ttu-id="4dc83-111">Tato chybová zpráva značí, že existují cenové záznamy, které byly dříve nastaveny pro dimenzi, která je vypnuta.</span><span class="sxs-lookup"><span data-stu-id="4dc83-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="4dc83-112">Všechny záznamy **Cena role** a **Přirážka ceny role**, které odkazují na dimenzi, musí být odstraněny dříve, než bude možné použitelnost dimenze nastavit na **Ne.**</span><span class="sxs-lookup"><span data-stu-id="4dc83-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="4dc83-113">Toto pravidlo platí pro předem připravené i vlastní cenové dimenze, které jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="4dc83-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="4dc83-114">Důvodem tohoto ověření je, že služba Project Service má omezení, podle kterého každý záznam **Cena role** musí mít jedinečnou kombinaci dimenzí.</span><span class="sxs-lookup"><span data-stu-id="4dc83-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="4dc83-115">Například v ceníku s názvem **Nákladové sazby USA 2018**máte následující řádky **Cena role**.</span><span class="sxs-lookup"><span data-stu-id="4dc83-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="4dc83-116">Standardní název</span><span class="sxs-lookup"><span data-stu-id="4dc83-116">Standard Title</span></span>         | <span data-ttu-id="4dc83-117">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="4dc83-117">Org Unit</span></span>    |<span data-ttu-id="4dc83-118">Jednotka</span><span class="sxs-lookup"><span data-stu-id="4dc83-118">Unit</span></span>   |<span data-ttu-id="4dc83-119">Cena</span><span class="sxs-lookup"><span data-stu-id="4dc83-119">Price</span></span>  |<span data-ttu-id="4dc83-120">Měna</span><span class="sxs-lookup"><span data-stu-id="4dc83-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="4dc83-121">Systémový inženýr</span><span class="sxs-lookup"><span data-stu-id="4dc83-121">Systems Engineer</span></span>|<span data-ttu-id="4dc83-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="4dc83-122">Contoso US</span></span>|<span data-ttu-id="4dc83-123">Hour</span><span class="sxs-lookup"><span data-stu-id="4dc83-123">Hour</span></span>| <span data-ttu-id="4dc83-124">100</span><span class="sxs-lookup"><span data-stu-id="4dc83-124">100</span></span>|<span data-ttu-id="4dc83-125">USD</span><span class="sxs-lookup"><span data-stu-id="4dc83-125">USD</span></span>|
| <span data-ttu-id="4dc83-126">Senior systémový inženýr</span><span class="sxs-lookup"><span data-stu-id="4dc83-126">Senior Systems Engineer</span></span>|<span data-ttu-id="4dc83-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="4dc83-127">Contoso US</span></span>|<span data-ttu-id="4dc83-128">Hour</span><span class="sxs-lookup"><span data-stu-id="4dc83-128">Hour</span></span>| <span data-ttu-id="4dc83-129">150</span><span class="sxs-lookup"><span data-stu-id="4dc83-129">150</span></span>| <span data-ttu-id="4dc83-130">USD</span><span class="sxs-lookup"><span data-stu-id="4dc83-130">USD</span></span>|


<span data-ttu-id="4dc83-131">Pokud jako cenovou dimenzi vypnete **Standardní název** a modul ocenění služeb Project Service vyhledává cenu, použije pouze hodnotu **Organizační jednotka** ze zadání.</span><span class="sxs-lookup"><span data-stu-id="4dc83-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="4dc83-132">Pokud je **Organizační jednotka** v zadání „Contoso US“, výsledek bude nedeterministický, protože oba řádky budou shodné.</span><span class="sxs-lookup"><span data-stu-id="4dc83-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="4dc83-133">Chcete-li se vyhnout tomuto scénáři, při vytváření záznamů **Cena role** služba Project Service ověří, zda je kombinace dimenzí jedinečná.</span><span class="sxs-lookup"><span data-stu-id="4dc83-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="4dc83-134">Pokud je dimenze po vytvoření záznamů **Cena role** vypnutá, může být toto omezení porušeno.</span><span class="sxs-lookup"><span data-stu-id="4dc83-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="4dc83-135">Proto je nutné, aby před vypnutím dimenze byly odstraněny všechny řádky **Cena role** a **Přirážka ceny role**, které mají tuto hodnotu dimenze vyplněnou.</span><span class="sxs-lookup"><span data-stu-id="4dc83-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

