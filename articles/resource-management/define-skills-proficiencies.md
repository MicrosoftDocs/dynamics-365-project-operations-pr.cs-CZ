---
title: Definování dovedností a odbornosti
description: Toto téma obsahuje informace o způsobu nastavení modelů odborné způsobilosti pro ocenění zdrojů.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 24538ed1d610a0cae4c2badc0fd33c2f738a8338
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073724"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="f4a4d-103">Definování dovedností a odbornosti</span><span class="sxs-lookup"><span data-stu-id="f4a4d-103">Define skills and proficiencies</span></span>

<span data-ttu-id="f4a4d-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="f4a4d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f4a4d-105">Dovednosti jsou charakteristiky zdrojů, které jsou sdíleny mezi Dynamics 365 Project Operations a aplikací Dynamics 365 Field Service, pokud ji máte.</span><span class="sxs-lookup"><span data-stu-id="f4a4d-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="f4a4d-106">Chcete-li spravovat depozitář dovedností v Project Operations, přejděte na **Zdroje** \> **Dovednosti zdroje**.</span><span class="sxs-lookup"><span data-stu-id="f4a4d-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="f4a4d-107">Použití modelů odborné způsobilosti k hodnocení zdrojů</span><span class="sxs-lookup"><span data-stu-id="f4a4d-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="f4a4d-108">Dovednosti pro zdroje jsou hodnoceny pomocí modelů odborné způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="f4a4d-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="f4a4d-109">Individuální hodnocení jsou v modelu odborné způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="f4a4d-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="f4a4d-110">Chcete-li vytvořit model odborné způsobilosti, přejděte na **Zdroje** \> **Modely odborné způsobilosti** a poté vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="f4a4d-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="f4a4d-111">V novém modelu hodnocení uveďte minimální hodnotu hodnocení, maximální hodnotu hodnocení a hodnocenou entitu.</span><span class="sxs-lookup"><span data-stu-id="f4a4d-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="f4a4d-112">V podmřížce **Hodnoty hodnocení** můžete definovat různé hodnoty hodnocení od minimálního po maximální.</span><span class="sxs-lookup"><span data-stu-id="f4a4d-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="f4a4d-113">Tyto hodnoty hodnocení jsou zobrazeny ve filtrech **Požadavky na zdroje** , **Plánovací vývěska** a **Pomocník plánování**.</span><span class="sxs-lookup"><span data-stu-id="f4a4d-113">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
