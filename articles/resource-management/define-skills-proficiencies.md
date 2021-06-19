---
title: Definování dovedností a odbornosti
description: Toto téma obsahuje informace o způsobu nastavení modelů odborné způsobilosti pro ocenění zdrojů.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 982f64677b74f2195eacc287fc07b80c34f7acc0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015323"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="23950-103">Definování dovedností a odbornosti</span><span class="sxs-lookup"><span data-stu-id="23950-103">Define skills and proficiencies</span></span>

<span data-ttu-id="23950-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="23950-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="23950-105">Dovednosti jsou charakteristiky zdrojů, které jsou sdíleny mezi Dynamics 365 Project Operations a Dynamics 365 Field Service, pokud je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="23950-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="23950-106">Chcete-li spravovat depozitář dovedností v Project Operations, přejděte na **Zdroje** \> **Dovednosti zdroje**.</span><span class="sxs-lookup"><span data-stu-id="23950-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="23950-107">Použití modelů odborné způsobilosti k hodnocení zdrojů</span><span class="sxs-lookup"><span data-stu-id="23950-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="23950-108">Dovednosti pro zdroje jsou hodnoceny pomocí modelů odborné způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="23950-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="23950-109">Individuální hodnocení jsou v modelu odborné způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="23950-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="23950-110">Chcete-li vytvořit model odborné způsobilosti, přejděte na **Zdroje** \> **Modely odborné způsobilosti** a poté vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="23950-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="23950-111">V novém modelu hodnocení uveďte minimální hodnotu hodnocení, maximální hodnotu hodnocení a hodnocenou entitu.</span><span class="sxs-lookup"><span data-stu-id="23950-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="23950-112">V podmřížce **Hodnoty hodnocení** můžete definovat různé hodnoty hodnocení od minimálního po maximální.</span><span class="sxs-lookup"><span data-stu-id="23950-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="23950-113">Tyto hodnoty hodnocení jsou zobrazeny ve filtrech **Požadavky na zdroje**, **Plánovací vývěska** a **Pomocník plánování**.</span><span class="sxs-lookup"><span data-stu-id="23950-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]