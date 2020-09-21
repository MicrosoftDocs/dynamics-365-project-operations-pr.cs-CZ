---
title: Fáze projektu
description: Toto téma poskytuje informace o fázích projektu.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750309"
---
# <a name="project-stages"></a><span data-ttu-id="64cdb-103">Fáze projektu</span><span class="sxs-lookup"><span data-stu-id="64cdb-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="64cdb-104">Fáze projektu jsou aktualizovány tak, aby odrážely stav projektu v průběhu jeho vývoje.</span><span class="sxs-lookup"><span data-stu-id="64cdb-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="64cdb-105">Výchozí tok obchodního procesu automaticky aktualizuje některé fáze projektu, zatímco jiné aktualizuje ručně projektový manažer.</span><span class="sxs-lookup"><span data-stu-id="64cdb-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="64cdb-106">Ve výchozím toku obchodního procesu jsou definovány následující fáze:</span><span class="sxs-lookup"><span data-stu-id="64cdb-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="64cdb-107">Nové</span><span class="sxs-lookup"><span data-stu-id="64cdb-107">New</span></span>
- <span data-ttu-id="64cdb-108">Nabídka</span><span class="sxs-lookup"><span data-stu-id="64cdb-108">Quote</span></span>
- <span data-ttu-id="64cdb-109">Plán</span><span class="sxs-lookup"><span data-stu-id="64cdb-109">Plan</span></span>
- <span data-ttu-id="64cdb-110">Dodat</span><span class="sxs-lookup"><span data-stu-id="64cdb-110">Deliver</span></span>
- <span data-ttu-id="64cdb-111">Dokončeno</span><span class="sxs-lookup"><span data-stu-id="64cdb-111">Complete</span></span>
- <span data-ttu-id="64cdb-112">Close (Zavřít)</span><span class="sxs-lookup"><span data-stu-id="64cdb-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="64cdb-113">Nové</span><span class="sxs-lookup"><span data-stu-id="64cdb-113">New</span></span>

<span data-ttu-id="64cdb-114">Při vytváření projektu je fáze projektu nastavena na **Nový**.</span><span class="sxs-lookup"><span data-stu-id="64cdb-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="64cdb-115">Pokud byl projekt vytvořen ze šablony, může obsahovat plán, odhad a data týmu.</span><span class="sxs-lookup"><span data-stu-id="64cdb-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="64cdb-116">V opačném případě je to pouze osnova projektu a zbývající součásti musí být zadány.</span><span class="sxs-lookup"><span data-stu-id="64cdb-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="64cdb-117">Nabídka</span><span class="sxs-lookup"><span data-stu-id="64cdb-117">Quote</span></span>

<span data-ttu-id="64cdb-118">Když přiřadíte projekt k nabídce nebo když vytvoříte projekt z nabídky, fáze projektu bude nastavena na **Nabídka** a aktualizuje se odhadované datum zahájení a ukončení.</span><span class="sxs-lookup"><span data-stu-id="64cdb-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="64cdb-119">Pokud je projekt ve fázi **Nabídka**, zobrazí se podrobnosti o nabídce na kartě **Prodej** na stránce **Entita projektu**.</span><span class="sxs-lookup"><span data-stu-id="64cdb-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="64cdb-120">Plán</span><span class="sxs-lookup"><span data-stu-id="64cdb-120">Plan</span></span>

<span data-ttu-id="64cdb-121">Pokud vyhrajete nabídku spojenou s projektem a projekt přejde do fáze **Smlouva**, fáze projektu se aktualizuje na **Plán**.</span><span class="sxs-lookup"><span data-stu-id="64cdb-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="64cdb-122">Pokud je projekt ve fázi **Plán**, zobrazí se podrobnosti o smlouvě na stránce **Entita projektu**.</span><span class="sxs-lookup"><span data-stu-id="64cdb-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="64cdb-123">Dodat</span><span class="sxs-lookup"><span data-stu-id="64cdb-123">Deliver</span></span>

<span data-ttu-id="64cdb-124">Když je plán projektu dokončen a jste připraveni ke spuštění projektu, měl by projektový manažer aktualizovat fázi projektu na **Dodat**, aby bylo možné zobrazit, že projekt byl zahájen.</span><span class="sxs-lookup"><span data-stu-id="64cdb-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="64cdb-125">Dokončeno</span><span class="sxs-lookup"><span data-stu-id="64cdb-125">Complete</span></span> 

<span data-ttu-id="64cdb-126">Po dokončení práce na projektu může projektový manažer aktualizovat fázi na **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="64cdb-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="64cdb-127">Aktualizací fáze projektu na **Dokončeno** dá projektový manažer najevo, že práce je 100% dokončena, ale že je projekt ponechán otevřený, aby bylo možné zaznamenat všechny nevyřízené časové nebo výdajové záznamy.</span><span class="sxs-lookup"><span data-stu-id="64cdb-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="64cdb-128">Close (Zavřít)</span><span class="sxs-lookup"><span data-stu-id="64cdb-128">Close</span></span>

<span data-ttu-id="64cdb-129">Jakmile jsou všechny transakce pro projekt zaznamenány, může projektový manažer aktualizovat fázi na **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="64cdb-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="64cdb-130">V tomto okamžiku nelze zaznamenat žádné transakce a projekt je nastaven jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="64cdb-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
