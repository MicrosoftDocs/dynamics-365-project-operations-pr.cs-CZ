---
title: Kopírování projektu
description: Toto téma obsahuje informace o kopírování projektů v Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479511"
---
# <a name="copy-a-project"></a><span data-ttu-id="5da32-103">Kopírování projektu</span><span class="sxs-lookup"><span data-stu-id="5da32-103">Copy a project</span></span>

<span data-ttu-id="5da32-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="5da32-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5da32-105">V Dynamics 365 Project Operations můžete rychle vytvářet nové projekty výběrem volby **Kopírovat projekt** ve formuláři **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="5da32-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="5da32-106">Chcete-li zkopírovat projekt, otevřete projekt, který chcete zkopírovat, a poté vyberte **Kopírovat projekt**.</span><span class="sxs-lookup"><span data-stu-id="5da32-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="5da32-107">Akce zkopíruje:</span><span class="sxs-lookup"><span data-stu-id="5da32-107">The action will copy:</span></span>

- <span data-ttu-id="5da32-108">Vlastnosti projektu (odhadované datum zahájení je zkopírováno ze zdrojového projektu)</span><span class="sxs-lookup"><span data-stu-id="5da32-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="5da32-109">Strukturovaný rozpis prací</span><span class="sxs-lookup"><span data-stu-id="5da32-109">The Work breakdown structure</span></span>
- <span data-ttu-id="5da32-110">Členové projektových týmů</span><span class="sxs-lookup"><span data-stu-id="5da32-110">Project team members</span></span>
- <span data-ttu-id="5da32-111">Odhady projektů</span><span class="sxs-lookup"><span data-stu-id="5da32-111">Project estimates</span></span>
- <span data-ttu-id="5da32-112">Odhady projektových výdajů</span><span class="sxs-lookup"><span data-stu-id="5da32-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="5da32-113">Vlastnosti projektu</span><span class="sxs-lookup"><span data-stu-id="5da32-113">Project properties</span></span>

<span data-ttu-id="5da32-114">Při kopírování projektu se zkopírují hodnoty v následujících polích:</span><span class="sxs-lookup"><span data-stu-id="5da32-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="5da32-115">Jméno</span><span class="sxs-lookup"><span data-stu-id="5da32-115">Name</span></span>
- <span data-ttu-id="5da32-116">Popis</span><span class="sxs-lookup"><span data-stu-id="5da32-116">Description</span></span>
- <span data-ttu-id="5da32-117">Zákazník</span><span class="sxs-lookup"><span data-stu-id="5da32-117">Customer</span></span>
- <span data-ttu-id="5da32-118">Šablona kalendáře</span><span class="sxs-lookup"><span data-stu-id="5da32-118">Calendar Template</span></span>
- <span data-ttu-id="5da32-119">Měna</span><span class="sxs-lookup"><span data-stu-id="5da32-119">Currency</span></span>
- <span data-ttu-id="5da32-120">Smluvní jednotka</span><span class="sxs-lookup"><span data-stu-id="5da32-120">Contracting Unit</span></span>
- <span data-ttu-id="5da32-121">Projektový manažer</span><span class="sxs-lookup"><span data-stu-id="5da32-121">Project Manager</span></span>
- <span data-ttu-id="5da32-122">Stav</span><span class="sxs-lookup"><span data-stu-id="5da32-122">Status</span></span>
- <span data-ttu-id="5da32-123">Celkový stav projektu</span><span class="sxs-lookup"><span data-stu-id="5da32-123">Overall Project Status</span></span>
- <span data-ttu-id="5da32-124">Komentáře</span><span class="sxs-lookup"><span data-stu-id="5da32-124">Comments</span></span>
- <span data-ttu-id="5da32-125">Odhady</span><span class="sxs-lookup"><span data-stu-id="5da32-125">Estimates</span></span>
- <span data-ttu-id="5da32-126">Odhadované počáteční datum</span><span class="sxs-lookup"><span data-stu-id="5da32-126">Estimated Start Date</span></span>
- <span data-ttu-id="5da32-127">Datum ukončení</span><span class="sxs-lookup"><span data-stu-id="5da32-127">Finish Date</span></span>
- <span data-ttu-id="5da32-128">Úsilí (hodiny)</span><span class="sxs-lookup"><span data-stu-id="5da32-128">Effort (Hours)</span></span>
- <span data-ttu-id="5da32-129">Odhadované pracovní náklady</span><span class="sxs-lookup"><span data-stu-id="5da32-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="5da32-130">Odhadované výdajové náklady</span><span class="sxs-lookup"><span data-stu-id="5da32-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="5da32-131">Strukturovaný rozpis prací</span><span class="sxs-lookup"><span data-stu-id="5da32-131">Work breakdown structure</span></span>

<span data-ttu-id="5da32-132">Když je projekt zkopírován, zkopíruje se celý strukturovaný rozpis prací načtený ze zdrojů.</span><span class="sxs-lookup"><span data-stu-id="5da32-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="5da32-133">Pojmenované zdroje jsou nahrazeny obecnými zdroji.</span><span class="sxs-lookup"><span data-stu-id="5da32-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="5da32-134">Pokud pojmenované zdroje nemají stejnou pracovní dobu jako obecný zdroj, plán se přepočítá a doba trvání úkolu se může změnit.</span><span class="sxs-lookup"><span data-stu-id="5da32-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="5da32-135">Členové projektových týmů</span><span class="sxs-lookup"><span data-stu-id="5da32-135">Project team members</span></span>

<span data-ttu-id="5da32-136">Když se projektový tým zkopíruje ze zdrojového projektu, zkopírují se obecné zdroje.</span><span class="sxs-lookup"><span data-stu-id="5da32-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="5da32-137">Přiřazení obecných zdrojů jsou rovněž zachována tak, jako byla ve zdrojovém projektu.</span><span class="sxs-lookup"><span data-stu-id="5da32-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="5da32-138">Pojmenované zdroje budou převedeny na obecné členy týmu.</span><span class="sxs-lookup"><span data-stu-id="5da32-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="5da32-139">Odhady</span><span class="sxs-lookup"><span data-stu-id="5da32-139">Estimates</span></span>

<span data-ttu-id="5da32-140">Při kopírování projektu se zkopírují řádky odhadu zdrojů a výdajů ze zdrojového projektu.</span><span class="sxs-lookup"><span data-stu-id="5da32-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="5da32-141">Informace o tom, jak programátorsky přistupovat ke kopírování projektu, najdete v části [Vývoj projektových šablon pomocí nástroje kopírovat projekt](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="5da32-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
