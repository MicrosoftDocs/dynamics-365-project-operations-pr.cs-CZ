---
title: Aktualizace odhadu nákladů při dokončení
description: Tento téma poskytuje informace o aktualizaci projekce úsilí na projekt.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286420"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="55746-103">Aktualizace odhadu nákladů při dokončení</span><span class="sxs-lookup"><span data-stu-id="55746-103">Update estimate at completion</span></span>

<span data-ttu-id="55746-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="55746-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="55746-105">Je běžné, že projektový manažer reviduje původní odhady úkolu.</span><span class="sxs-lookup"><span data-stu-id="55746-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="55746-106">Předpovědi projektu jsou vnímání odhadů projektového manažera podle aktuálního stavu projektu.</span><span class="sxs-lookup"><span data-stu-id="55746-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="55746-107">Nedoporučujeme však, aby projektoví manažeři směrná čísla měnili, protože směrný plán projektu představuje stanovený zdroj pravdy pro odhady plánů a nákladů projektu a všichni účastníci projektu se na něm shodli.</span><span class="sxs-lookup"><span data-stu-id="55746-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="55746-108">Projektový manažer může předpovědět úsilí na úkoly dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="55746-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="55746-109">Přepsat výchozí odhad na dokončení (ETC) novým odhadem skutečně zbývajícího úsilí na úkol.</span><span class="sxs-lookup"><span data-stu-id="55746-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="55746-110">Přepsat výchozí procento pokroku novým odhadem skutečného pokroku u úkolu.</span><span class="sxs-lookup"><span data-stu-id="55746-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="55746-111">Každý z těchto přístupů způsobuje přepočet hodnot ETC, EAC a procenta pokroku a očekávané odchylky úsilí daného úkolu.</span><span class="sxs-lookup"><span data-stu-id="55746-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="55746-112">Přepočítají se hodnoty EAC, ETC a procento pokroku souhrnných úkolů a vytvoří se nová projekce odchylky úsilí.</span><span class="sxs-lookup"><span data-stu-id="55746-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]