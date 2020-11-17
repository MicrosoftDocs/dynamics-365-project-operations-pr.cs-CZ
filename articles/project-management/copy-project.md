---
title: Kopírování projektu
description: Toto téma poskytuje informace o kopírování projektů v Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cf80f2a1cd27aae33d123e45dee70d94ea4d01a9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073721"
---
# <a name="copy-a-project"></a><span data-ttu-id="a6055-103">Kopírování projektu</span><span class="sxs-lookup"><span data-stu-id="a6055-103">Copy a project</span></span>

<span data-ttu-id="a6055-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="a6055-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a6055-105">S Dynamics 365 Project Operations můžete rychle vytvářet nové projekty výběrem **Kopírovat projekt** ve formuláři **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="a6055-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="a6055-106">Chcete-li zkopírovat projekt, otevřete projekt, který chcete zkopírovat, a poté vyberte **Kopírovat projekt**.</span><span class="sxs-lookup"><span data-stu-id="a6055-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="a6055-107">Akce zkopíruje:</span><span class="sxs-lookup"><span data-stu-id="a6055-107">The action will copy:</span></span>

- <span data-ttu-id="a6055-108">Vlastnosti projektu</span><span class="sxs-lookup"><span data-stu-id="a6055-108">Project properties</span></span>
- <span data-ttu-id="a6055-109">Strukturovaný rozpis prací</span><span class="sxs-lookup"><span data-stu-id="a6055-109">The Work breakdown structure</span></span>
- <span data-ttu-id="a6055-110">Členové projektových týmů</span><span class="sxs-lookup"><span data-stu-id="a6055-110">Project team members</span></span>
- <span data-ttu-id="a6055-111">Odhady projektů</span><span class="sxs-lookup"><span data-stu-id="a6055-111">Project estimates</span></span>
- <span data-ttu-id="a6055-112">Odhady projektových výdajů</span><span class="sxs-lookup"><span data-stu-id="a6055-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="a6055-113">Vlastnosti projektu</span><span class="sxs-lookup"><span data-stu-id="a6055-113">Project properties</span></span>

<span data-ttu-id="a6055-114">Při kopírování projektu se zkopírují hodnoty v následujících polích:</span><span class="sxs-lookup"><span data-stu-id="a6055-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="a6055-115">Jméno</span><span class="sxs-lookup"><span data-stu-id="a6055-115">Name</span></span>
- <span data-ttu-id="a6055-116">Popis</span><span class="sxs-lookup"><span data-stu-id="a6055-116">Description</span></span>
- <span data-ttu-id="a6055-117">Zákazník</span><span class="sxs-lookup"><span data-stu-id="a6055-117">Customer</span></span>
- <span data-ttu-id="a6055-118">Šablona kalendáře</span><span class="sxs-lookup"><span data-stu-id="a6055-118">Calendar Template</span></span>
- <span data-ttu-id="a6055-119">Měna</span><span class="sxs-lookup"><span data-stu-id="a6055-119">Currency</span></span>
- <span data-ttu-id="a6055-120">Smluvní jednotka</span><span class="sxs-lookup"><span data-stu-id="a6055-120">Contracting Unit</span></span>
- <span data-ttu-id="a6055-121">Projektový manažer</span><span class="sxs-lookup"><span data-stu-id="a6055-121">Project Manager</span></span>
- <span data-ttu-id="a6055-122">Stav</span><span class="sxs-lookup"><span data-stu-id="a6055-122">Status</span></span>
- <span data-ttu-id="a6055-123">Celkový stav projektu</span><span class="sxs-lookup"><span data-stu-id="a6055-123">Overall Project Status</span></span>
- <span data-ttu-id="a6055-124">Komentáře</span><span class="sxs-lookup"><span data-stu-id="a6055-124">Comments</span></span>
- <span data-ttu-id="a6055-125">Odhady</span><span class="sxs-lookup"><span data-stu-id="a6055-125">Estimates</span></span>
- <span data-ttu-id="a6055-126">Odhadované počáteční datum</span><span class="sxs-lookup"><span data-stu-id="a6055-126">Estimated Start Date</span></span>
- <span data-ttu-id="a6055-127">Datum ukončení</span><span class="sxs-lookup"><span data-stu-id="a6055-127">Finish Date</span></span>
- <span data-ttu-id="a6055-128">Úsilí (hodiny)</span><span class="sxs-lookup"><span data-stu-id="a6055-128">Effort (Hours)</span></span>
- <span data-ttu-id="a6055-129">Odhadované pracovní náklady</span><span class="sxs-lookup"><span data-stu-id="a6055-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="a6055-130">Odhadované výdajové náklady</span><span class="sxs-lookup"><span data-stu-id="a6055-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="a6055-131">Strukturovaný rozpis prací</span><span class="sxs-lookup"><span data-stu-id="a6055-131">Work breakdown structure</span></span>

<span data-ttu-id="a6055-132">Když je projekt zkopírován, zkopíruje se celý strukturovaný rozpis prací načtený ze zdrojů.</span><span class="sxs-lookup"><span data-stu-id="a6055-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="a6055-133">Pojmenované zdroje jsou nahrazeny obecnými zdroji.</span><span class="sxs-lookup"><span data-stu-id="a6055-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="a6055-134">Pokud pojmenované zdroje nemají stejnou pracovní dobu jako obecný zdroj, plán se přepočítá a doba trvání úkolu se může změnit.</span><span class="sxs-lookup"><span data-stu-id="a6055-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="a6055-135">Členové projektových týmů</span><span class="sxs-lookup"><span data-stu-id="a6055-135">Project team members</span></span>

<span data-ttu-id="a6055-136">Když se projektový tým zkopíruje ze zdrojového projektu, zkopírují se obecné zdroje.</span><span class="sxs-lookup"><span data-stu-id="a6055-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="a6055-137">Přiřazení obecných zdrojů jsou rovněž zachována tak, jako byla ve zdrojovém projektu.</span><span class="sxs-lookup"><span data-stu-id="a6055-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="a6055-138">Pojmenované zdroje budou převedeny na obecné členy týmu.</span><span class="sxs-lookup"><span data-stu-id="a6055-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="a6055-139">Odhady</span><span class="sxs-lookup"><span data-stu-id="a6055-139">Estimates</span></span>

<span data-ttu-id="a6055-140">Při kopírování projektu se zkopírují řádky odhadu zdrojů a výdajů ze zdrojového projektu.</span><span class="sxs-lookup"><span data-stu-id="a6055-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="a6055-141">Informace o tom, jak programátorsky přistupovat ke kopírování projektu, najdete v části [Vývoj projektových šablon pomocí nástroje kopírovat projekt](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="a6055-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>