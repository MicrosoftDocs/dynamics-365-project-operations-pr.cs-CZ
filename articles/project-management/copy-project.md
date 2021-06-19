---
title: Kopírování projektu
description: Toto téma obsahuje informace o kopírování projektů v Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091246"
---
# <a name="copy-a-project"></a><span data-ttu-id="f9205-103">Kopírování projektu</span><span class="sxs-lookup"><span data-stu-id="f9205-103">Copy a project</span></span>

<span data-ttu-id="f9205-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="f9205-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f9205-105">V Dynamics 365 Project Operations můžete rychle vytvářet nové projekty výběrem volby **Kopírovat projekt** ve formuláři **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="f9205-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="f9205-106">Chcete-li zkopírovat projekt, otevřete projekt, který chcete zkopírovat, a poté vyberte **Kopírovat projekt**.</span><span class="sxs-lookup"><span data-stu-id="f9205-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="f9205-107">Akce zkopíruje následující:</span><span class="sxs-lookup"><span data-stu-id="f9205-107">The action will copy the following:</span></span>

- <span data-ttu-id="f9205-108">Vlastnosti projektu</span><span class="sxs-lookup"><span data-stu-id="f9205-108">Project properties</span></span> 
- <span data-ttu-id="f9205-109">Strukturovaný rozpis prací</span><span class="sxs-lookup"><span data-stu-id="f9205-109">Work breakdown structure</span></span>
- <span data-ttu-id="f9205-110">Členové projektových týmů</span><span class="sxs-lookup"><span data-stu-id="f9205-110">Project team members</span></span>
- <span data-ttu-id="f9205-111">Odhady projektů</span><span class="sxs-lookup"><span data-stu-id="f9205-111">Project estimates</span></span>
- <span data-ttu-id="f9205-112">Odhady projektových výdajů</span><span class="sxs-lookup"><span data-stu-id="f9205-112">Project expense estimates</span></span>
- <span data-ttu-id="f9205-113">Odhady materiálu projektu</span><span class="sxs-lookup"><span data-stu-id="f9205-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="f9205-114">Vlastnosti projektu</span><span class="sxs-lookup"><span data-stu-id="f9205-114">Project properties</span></span>

<span data-ttu-id="f9205-115">Při kopírování projektu se zkopírují hodnoty v následujících polích:</span><span class="sxs-lookup"><span data-stu-id="f9205-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="f9205-116">Jméno</span><span class="sxs-lookup"><span data-stu-id="f9205-116">Name</span></span>
- <span data-ttu-id="f9205-117">Popis</span><span class="sxs-lookup"><span data-stu-id="f9205-117">Description</span></span>
- <span data-ttu-id="f9205-118">Zákazník</span><span class="sxs-lookup"><span data-stu-id="f9205-118">Customer</span></span>
- <span data-ttu-id="f9205-119">Šablona kalendáře</span><span class="sxs-lookup"><span data-stu-id="f9205-119">Calendar Template</span></span>
- <span data-ttu-id="f9205-120">Měna</span><span class="sxs-lookup"><span data-stu-id="f9205-120">Currency</span></span>
- <span data-ttu-id="f9205-121">Smluvní jednotka</span><span class="sxs-lookup"><span data-stu-id="f9205-121">Contracting Unit</span></span>
- <span data-ttu-id="f9205-122">Projektový manažer</span><span class="sxs-lookup"><span data-stu-id="f9205-122">Project Manager</span></span>
- <span data-ttu-id="f9205-123">Stav</span><span class="sxs-lookup"><span data-stu-id="f9205-123">Status</span></span>
- <span data-ttu-id="f9205-124">Celkový stav projektu</span><span class="sxs-lookup"><span data-stu-id="f9205-124">Overall Project Status</span></span>
- <span data-ttu-id="f9205-125">Komentáře</span><span class="sxs-lookup"><span data-stu-id="f9205-125">Comments</span></span>
- <span data-ttu-id="f9205-126">Odhady</span><span class="sxs-lookup"><span data-stu-id="f9205-126">Estimates</span></span>
- <span data-ttu-id="f9205-127">Odhadované datum zahájení: Toto je datum, kdy je projekt vytvořen z kopie.</span><span class="sxs-lookup"><span data-stu-id="f9205-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="f9205-128">Odhadované datum dokončení: Toto datum je upraveno na základě data zahájení nového projektu, který byl vytvořen z kopie.</span><span class="sxs-lookup"><span data-stu-id="f9205-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="f9205-129">Úsilí (hodiny)</span><span class="sxs-lookup"><span data-stu-id="f9205-129">Effort (Hours)</span></span>
- <span data-ttu-id="f9205-130">Odhadované pracovní náklady</span><span class="sxs-lookup"><span data-stu-id="f9205-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="f9205-131">Odhadované výdajové náklady</span><span class="sxs-lookup"><span data-stu-id="f9205-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="f9205-132">Odhadované náklady na materiál</span><span class="sxs-lookup"><span data-stu-id="f9205-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="f9205-133">Projekt kopírování je dlouhá operace.</span><span class="sxs-lookup"><span data-stu-id="f9205-133">Copy project is a long running operation.</span></span> <span data-ttu-id="f9205-134">Kopírují se také záznamy projektu, jejich příslušné atributy a mnoho souvisejících entit.</span><span class="sxs-lookup"><span data-stu-id="f9205-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="f9205-135">Z důvodu dlouhodobé povahy operace je po spuštění kopírování cílová stránka projektu uzamčena pro úpravy, dokud není operace kopírování dokončena.</span><span class="sxs-lookup"><span data-stu-id="f9205-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="f9205-136">Strukturovaný rozpis prací</span><span class="sxs-lookup"><span data-stu-id="f9205-136">Work breakdown structure</span></span>

<span data-ttu-id="f9205-137">Když je projekt zkopírován, zkopíruje se celý strukturovaný rozpis prací načtený ze zdrojů.</span><span class="sxs-lookup"><span data-stu-id="f9205-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="f9205-138">Pojmenované zdroje jsou nahrazeny obecnými zdroji.</span><span class="sxs-lookup"><span data-stu-id="f9205-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="f9205-139">Pokud pojmenované zdroje nemají stejnou pracovní dobu jako obecný zdroj, plán se přepočítá a doba trvání úkolu se může změnit.</span><span class="sxs-lookup"><span data-stu-id="f9205-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="f9205-140">Členové projektových týmů</span><span class="sxs-lookup"><span data-stu-id="f9205-140">Project team members</span></span>

<span data-ttu-id="f9205-141">Když se projektový tým zkopíruje ze zdrojového projektu, zkopírují se obecné zdroje.</span><span class="sxs-lookup"><span data-stu-id="f9205-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="f9205-142">Přiřazení obecných zdrojů jsou rovněž zachována tak, jako byla ve zdrojovém projektu.</span><span class="sxs-lookup"><span data-stu-id="f9205-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="f9205-143">Pojmenované zdroje budou převedeny na obecné členy týmu.</span><span class="sxs-lookup"><span data-stu-id="f9205-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="f9205-144">Odhady</span><span class="sxs-lookup"><span data-stu-id="f9205-144">Estimates</span></span>

<span data-ttu-id="f9205-145">Při kopírování projektu se zkopírují řádky odhadu zdrojů, výdajů a materiálu ze zdrojového projektu.</span><span class="sxs-lookup"><span data-stu-id="f9205-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="f9205-146">Informace o tom, jak programátorsky přistupovat ke kopírování projektu, najdete v části [Vývoj projektových šablon pomocí nástroje kopírovat projekt](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="f9205-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
