---
title: Kopírování projektu
description: Toto téma poskytuje informace o kopírování projektů v Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907989"
---
# <a name="copy-a-project"></a><span data-ttu-id="f82ff-103">Kopírování projektu</span><span class="sxs-lookup"><span data-stu-id="f82ff-103">Copy a project</span></span>

<span data-ttu-id="f82ff-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="f82ff-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f82ff-105">S Dynamics 365 Project Operations můžete rychle vytvářet nové projekty pomocí akce **Kopírovat projekt** ve formuláři **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="f82ff-105">With Dynamics 365 Project Operations, you can quickly build new projects by using the **Copy Project** action on the **Projects** from.</span></span> <span data-ttu-id="f82ff-106">Chcete-li zkopírovat projekt, vyberte projekt a poté vyberte **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="f82ff-106">To copy a project, select a project, and then select **Copy**.</span></span> <span data-ttu-id="f82ff-107">Akce zkopíruje:</span><span class="sxs-lookup"><span data-stu-id="f82ff-107">The action will copy:</span></span>

- <span data-ttu-id="f82ff-108">Vlastnosti projektu</span><span class="sxs-lookup"><span data-stu-id="f82ff-108">Project properties</span></span>
- <span data-ttu-id="f82ff-109">Strukturovaný rozpis prací</span><span class="sxs-lookup"><span data-stu-id="f82ff-109">The Work breakdown structure</span></span>
- <span data-ttu-id="f82ff-110">Členové projektových týmů</span><span class="sxs-lookup"><span data-stu-id="f82ff-110">Project team members</span></span>
- <span data-ttu-id="f82ff-111">Odhady projektů</span><span class="sxs-lookup"><span data-stu-id="f82ff-111">Project estimates</span></span>
- <span data-ttu-id="f82ff-112">Odhady projektových výdajů</span><span class="sxs-lookup"><span data-stu-id="f82ff-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="f82ff-113">Vlastnosti projektu</span><span class="sxs-lookup"><span data-stu-id="f82ff-113">Project properties</span></span>

<span data-ttu-id="f82ff-114">Při kopírování projektu se zkopírují hodnoty v následujících polích:</span><span class="sxs-lookup"><span data-stu-id="f82ff-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="f82ff-115">Jméno</span><span class="sxs-lookup"><span data-stu-id="f82ff-115">Name</span></span>
- <span data-ttu-id="f82ff-116">Popis</span><span class="sxs-lookup"><span data-stu-id="f82ff-116">Description</span></span>
- <span data-ttu-id="f82ff-117">Zákazník</span><span class="sxs-lookup"><span data-stu-id="f82ff-117">Customer</span></span>
- <span data-ttu-id="f82ff-118">Šablona kalendáře</span><span class="sxs-lookup"><span data-stu-id="f82ff-118">Calendar Template</span></span>
- <span data-ttu-id="f82ff-119">Měna</span><span class="sxs-lookup"><span data-stu-id="f82ff-119">Currency</span></span>
- <span data-ttu-id="f82ff-120">Smluvní jednotka</span><span class="sxs-lookup"><span data-stu-id="f82ff-120">Contracting Unit</span></span>
- <span data-ttu-id="f82ff-121">Projektový manažer</span><span class="sxs-lookup"><span data-stu-id="f82ff-121">Project Manager</span></span>
- <span data-ttu-id="f82ff-122">Stav</span><span class="sxs-lookup"><span data-stu-id="f82ff-122">Status</span></span>
- <span data-ttu-id="f82ff-123">Celkový stav projektu</span><span class="sxs-lookup"><span data-stu-id="f82ff-123">Overall Project Status</span></span>
- <span data-ttu-id="f82ff-124">Komentáře</span><span class="sxs-lookup"><span data-stu-id="f82ff-124">Comments</span></span>
- <span data-ttu-id="f82ff-125">Odhady</span><span class="sxs-lookup"><span data-stu-id="f82ff-125">Estimates</span></span>
- <span data-ttu-id="f82ff-126">Odhadované počáteční datum</span><span class="sxs-lookup"><span data-stu-id="f82ff-126">Estimated Start Date</span></span>
- <span data-ttu-id="f82ff-127">Datum ukončení</span><span class="sxs-lookup"><span data-stu-id="f82ff-127">Finish Date</span></span>
- <span data-ttu-id="f82ff-128">Úsilí (hodiny)</span><span class="sxs-lookup"><span data-stu-id="f82ff-128">Effort (Hours)</span></span>
- <span data-ttu-id="f82ff-129">Odhadované pracovní náklady</span><span class="sxs-lookup"><span data-stu-id="f82ff-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="f82ff-130">Odhadované výdajové náklady</span><span class="sxs-lookup"><span data-stu-id="f82ff-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="f82ff-131">Strukturovaný rozpis prací</span><span class="sxs-lookup"><span data-stu-id="f82ff-131">Work breakdown structure</span></span>

<span data-ttu-id="f82ff-132">Když je projekt zkopírován, zkopíruje se celý strukturovaný rozpis prací načtený ze zdrojů.</span><span class="sxs-lookup"><span data-stu-id="f82ff-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="f82ff-133">Pojmenované zdroje jsou nahrazeny obecnými zdroji.</span><span class="sxs-lookup"><span data-stu-id="f82ff-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="f82ff-134">Pokud pojmenované zdroje nemají stejnou pracovní dobu jako obecný zdroj, plán se přepočítá a doba trvání úkolu se může změnit.</span><span class="sxs-lookup"><span data-stu-id="f82ff-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="f82ff-135">Členové projektových týmů</span><span class="sxs-lookup"><span data-stu-id="f82ff-135">Project team members</span></span>

<span data-ttu-id="f82ff-136">Když se projektový tým zkopíruje ze zdrojového projektu, zkopírují se obecné zdroje.</span><span class="sxs-lookup"><span data-stu-id="f82ff-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="f82ff-137">Přiřazení obecných zdrojů jsou rovněž zachována tak, jako byla ve zdrojovém projektu.</span><span class="sxs-lookup"><span data-stu-id="f82ff-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="f82ff-138">Pojmenované zdroje budou převedeny na obecné členy týmu.</span><span class="sxs-lookup"><span data-stu-id="f82ff-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="f82ff-139">Odhady</span><span class="sxs-lookup"><span data-stu-id="f82ff-139">Estimates</span></span>

<span data-ttu-id="f82ff-140">Při kopírování projektu se zkopírují řádky odhadu zdrojů a výdajů ze zdrojového projektu.</span><span class="sxs-lookup"><span data-stu-id="f82ff-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span>