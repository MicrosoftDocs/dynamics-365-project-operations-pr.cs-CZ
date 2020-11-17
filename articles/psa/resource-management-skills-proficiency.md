---
title: Dovednosti a modely odborné způsobilosti
description: Toto téma obsahuje informace o způsobu použití dovedností a modelů odborné způsobilosti.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cd243544df062e5801bbfa0a3bd75c4d9a116a6f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074000"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="98401-103">Dovednosti a modely odborné způsobilosti</span><span class="sxs-lookup"><span data-stu-id="98401-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="98401-104">Dovednosti jsou charakteristiky zdrojů, které jsou sdíleny mezi Dynamics 365 Project Service Automation a Dynamics 365 Field Service, pokud je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="98401-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="98401-105">Chcete-li spravovat depozitář dovedností v Project Service Automation, přejděte na **Zdroje** \> **Dovednosti zdroje**.</span><span class="sxs-lookup"><span data-stu-id="98401-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Dovednosti zdroje](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="98401-107">Použití modelů odborné způsobilosti k hodnocení zdrojů</span><span class="sxs-lookup"><span data-stu-id="98401-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="98401-108">Dovednosti pro zdroje jsou hodnoceny pomocí modelů odborné způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="98401-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="98401-109">Individuální hodnocení jsou v modelu odborné způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="98401-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="98401-110">Chcete-li vytvořit model odborné způsobilosti, přejděte na **Zdroje** \> **Modely odborné způsobilosti** a poté vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="98401-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="98401-111">V novém modelu hodnocení uveďte minimální hodnotu hodnocení, maximální hodnotu hodnocení a hodnocenou entitu.</span><span class="sxs-lookup"><span data-stu-id="98401-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="98401-112">V podmřížce **Hodnoty hodnocení** můžete definovat různé hodnoty hodnocení od minimálního po maximální.</span><span class="sxs-lookup"><span data-stu-id="98401-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Definované minimální a maximální hodnocení](media/Resource-Management-image85.png)

<span data-ttu-id="98401-114">Tyto hodnoty hodnocení jsou zobrazeny ve filtrech **Požadavky na zdroje** , **Plánovací vývěska** a **Pomocník plánování**.</span><span class="sxs-lookup"><span data-stu-id="98401-114">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>