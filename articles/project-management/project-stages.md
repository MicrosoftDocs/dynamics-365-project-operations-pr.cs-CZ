---
title: Fáze projektu
description: Tento téma poskytuje informace o projektových fázích dostupných v Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 554ad63bc44cbe5a1fe91eb47fedbb74bbedd4b6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073907"
---
# <a name="project-stages"></a><span data-ttu-id="25cf3-103">Fáze projektu</span><span class="sxs-lookup"><span data-stu-id="25cf3-103">Project stages</span></span>

<span data-ttu-id="25cf3-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="25cf3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="25cf3-105">Fáze projektu jsou koncipovány tak, aby odrážely stav projektu v průběhu jeho vývoje.</span><span class="sxs-lookup"><span data-stu-id="25cf3-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="25cf3-106">Přizpůsobení lze použít k automatické aktualizaci fází pomocí toků obchodního procesu, Power Automate nebo rozšíření plug-in.</span><span class="sxs-lookup"><span data-stu-id="25cf3-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="25cf3-107">Ve výchozím toku obchodního procesu jsou definovány následující fáze:</span><span class="sxs-lookup"><span data-stu-id="25cf3-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="25cf3-108">Nové</span><span class="sxs-lookup"><span data-stu-id="25cf3-108">New</span></span>
- <span data-ttu-id="25cf3-109">Nabídka</span><span class="sxs-lookup"><span data-stu-id="25cf3-109">Quote</span></span>
- <span data-ttu-id="25cf3-110">Plán</span><span class="sxs-lookup"><span data-stu-id="25cf3-110">Plan</span></span>
- <span data-ttu-id="25cf3-111">Dodat</span><span class="sxs-lookup"><span data-stu-id="25cf3-111">Deliver</span></span>
- <span data-ttu-id="25cf3-112">Dokončit</span><span class="sxs-lookup"><span data-stu-id="25cf3-112">Complete</span></span>
- <span data-ttu-id="25cf3-113">Uzavřeno</span><span class="sxs-lookup"><span data-stu-id="25cf3-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="25cf3-114">Nové</span><span class="sxs-lookup"><span data-stu-id="25cf3-114">New</span></span>

<span data-ttu-id="25cf3-115">Při vytváření projektu je fáze projektu nastavena na **Nový**.</span><span class="sxs-lookup"><span data-stu-id="25cf3-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="25cf3-116">Pokud byl projekt vytvořen ze šablony, může obsahovat plán, odhad a data týmu.</span><span class="sxs-lookup"><span data-stu-id="25cf3-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="25cf3-117">V opačném případě je to osnova projektu a zbývající součásti musí být zadány.</span><span class="sxs-lookup"><span data-stu-id="25cf3-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="25cf3-118">Nabídka</span><span class="sxs-lookup"><span data-stu-id="25cf3-118">Quote</span></span>

<span data-ttu-id="25cf3-119">Když přiřadíte projekt k nabídce nebo když vytvoříte projekt z nabídky, fáze projektu bude nastavena na **Nabídka** a aktualizuje se odhadované datum zahájení a ukončení.</span><span class="sxs-lookup"><span data-stu-id="25cf3-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote** , and the estimated start and end dates are updated.</span></span> <span data-ttu-id="25cf3-120">Pokud je projekt ve fázi **Nabídka** , zobrazí se podrobnosti o nabídce na kartě **Prodej** na stránce **Entita projektu**.</span><span class="sxs-lookup"><span data-stu-id="25cf3-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="25cf3-121">Plán</span><span class="sxs-lookup"><span data-stu-id="25cf3-121">Plan</span></span>

<span data-ttu-id="25cf3-122">Pokud vyhrajete nabídku spojenou s projektem a projekt přejde do fáze **Smlouva** , fáze projektu se aktualizuje na **Plán**.</span><span class="sxs-lookup"><span data-stu-id="25cf3-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="25cf3-123">Pokud je projekt ve fázi **Plán** , zobrazí se podrobnosti o smlouvě na stránce **Entita projektu**.</span><span class="sxs-lookup"><span data-stu-id="25cf3-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="25cf3-124">Dodat</span><span class="sxs-lookup"><span data-stu-id="25cf3-124">Deliver</span></span>

<span data-ttu-id="25cf3-125">Když je plán projektu dokončen a jste připraveni ke spuštění projektu, měl by projektový manažer aktualizovat fázi projektu na **Dodat** , aby bylo možné zobrazit, že projekt byl zahájen.</span><span class="sxs-lookup"><span data-stu-id="25cf3-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="25cf3-126">Dokončeno</span><span class="sxs-lookup"><span data-stu-id="25cf3-126">Complete</span></span> 

<span data-ttu-id="25cf3-127">Po dokončení práce na projektu může projektový manažer aktualizovat fázi na **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="25cf3-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="25cf3-128">Aktualizací fáze projektu na **Dokončeno** dá projektový manažer najevo, že práce je 100% dokončena, ale že je projekt ponechán otevřený, aby bylo možné zaznamenat všechny nevyřízené časové nebo výdajové záznamy.</span><span class="sxs-lookup"><span data-stu-id="25cf3-128">By updating the project stage to **Complete** , the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="25cf3-129">Close (Zavřít)</span><span class="sxs-lookup"><span data-stu-id="25cf3-129">Close</span></span>

<span data-ttu-id="25cf3-130">Jakmile jsou všechny transakce pro projekt zaznamenány, může projektový manažer aktualizovat fázi na **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="25cf3-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="25cf3-131">V tomto okamžiku nelze zaznamenat žádné transakce a projekt je nastaven jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="25cf3-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
