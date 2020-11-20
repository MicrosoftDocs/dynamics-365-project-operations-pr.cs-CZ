---
title: Rezervace na projekt
description: Toto téma obsahuje informace o rezervaci zdroje na projekt.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c87b0c32ef081f601ed79c11687f008bb454dd45
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131065"
---
# <a name="book-to-a-project"></a><span data-ttu-id="b05a1-103">Rezervace na projekt</span><span class="sxs-lookup"><span data-stu-id="b05a1-103">Book to a project</span></span>

<span data-ttu-id="b05a1-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="b05a1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b05a1-105">Jsou chvíle, kdy manažer projektu nebo správce zdrojů bude muset přidělit prostředek projektu, aniž by byl definován konkrétní požadavek od člena obecného týmu.</span><span class="sxs-lookup"><span data-stu-id="b05a1-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="b05a1-106">Tohoto lze dosáhnout třemi způsoby.</span><span class="sxs-lookup"><span data-stu-id="b05a1-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="b05a1-107">Rezervace z mřížky člena týmu</span><span class="sxs-lookup"><span data-stu-id="b05a1-107">Book from the team member grid</span></span>
- <span data-ttu-id="b05a1-108">Rezervace z plánovací vývěsky</span><span class="sxs-lookup"><span data-stu-id="b05a1-108">Book from the schedule board</span></span>
- <span data-ttu-id="b05a1-109">Rezervace z formuláře **Projekt**</span><span class="sxs-lookup"><span data-stu-id="b05a1-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="b05a1-110">Rezervace z mřížky člena týmu</span><span class="sxs-lookup"><span data-stu-id="b05a1-110">Book from the team member grid</span></span>

<span data-ttu-id="b05a1-111">Pokud vaše organizace pracuje v hybridním režimu přidělování prostředků, může projektový manažer rezervovat prostředek přímo do projektu provedením následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="b05a1-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="b05a1-112">V projektu přejděte do mřížky členů týmu a vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="b05a1-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="b05a1-113">Definujte název pozice a roli zdroje.</span><span class="sxs-lookup"><span data-stu-id="b05a1-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="b05a1-114">Vyberte rezervovatelný zdroj z dostupného vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b05a1-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="b05a1-115">Poté, co vyberete prostředek, definujte následující informace o poli pro rezervaci prostředku:</span><span class="sxs-lookup"><span data-stu-id="b05a1-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="b05a1-116">Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="b05a1-116">Start date</span></span>
    - <span data-ttu-id="b05a1-117">Datum dokončení</span><span class="sxs-lookup"><span data-stu-id="b05a1-117">Finish date</span></span>
    - <span data-ttu-id="b05a1-118">Metoda přidělení</span><span class="sxs-lookup"><span data-stu-id="b05a1-118">Allocation method</span></span>
    - <span data-ttu-id="b05a1-119">Hodiny, pokud je to relevantní</span><span class="sxs-lookup"><span data-stu-id="b05a1-119">Hours, if applicable</span></span>
    - <span data-ttu-id="b05a1-120">Schvalovatel projektu</span><span class="sxs-lookup"><span data-stu-id="b05a1-120">Project approver</span></span>

6. <span data-ttu-id="b05a1-121">Zvolte **Uložit a zavřít**</span><span class="sxs-lookup"><span data-stu-id="b05a1-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="b05a1-122">Rezervace z plánovací vývěsky</span><span class="sxs-lookup"><span data-stu-id="b05a1-122">Book from the schedule board</span></span>

<span data-ttu-id="b05a1-123">Když správce zdrojů potřebuje rezervovat zdroj přímo do projektu, může použít plánovací tabuli a požadavek projektu.</span><span class="sxs-lookup"><span data-stu-id="b05a1-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="b05a1-124">Požadavek na projekt je požadavek na zdroj, který je vždy k dispozici a lze jej rezervovat.</span><span class="sxs-lookup"><span data-stu-id="b05a1-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="b05a1-125">Chcete-li provést rezervaci přímo do formuláře na plánovací vývěsce, postupujte dle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="b05a1-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="b05a1-126">Přejděte na plánovací vývěsku a na levé stránce vyfiltrujte zdroje, které pro daný požadavek zvažujete.</span><span class="sxs-lookup"><span data-stu-id="b05a1-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="b05a1-127">Ve spodním podokně vyberte kartu **Projekt** pro zobrazení seznamu požadavků projektu.</span><span class="sxs-lookup"><span data-stu-id="b05a1-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="b05a1-128">Přetáhněte požadavek na prostředek a definujte následující informace:</span><span class="sxs-lookup"><span data-stu-id="b05a1-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="b05a1-129">Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="b05a1-129">Start date</span></span>
    - <span data-ttu-id="b05a1-130">Datum dokončení</span><span class="sxs-lookup"><span data-stu-id="b05a1-130">Finish date</span></span>
    - <span data-ttu-id="b05a1-131">Stav rezervace</span><span class="sxs-lookup"><span data-stu-id="b05a1-131">Booking status</span></span>
    - <span data-ttu-id="b05a1-132">Metoda rezervace</span><span class="sxs-lookup"><span data-stu-id="b05a1-132">Booking method</span></span>
    - <span data-ttu-id="b05a1-133">Trvání</span><span class="sxs-lookup"><span data-stu-id="b05a1-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="b05a1-134">Rezervace z formuláře Projekt</span><span class="sxs-lookup"><span data-stu-id="b05a1-134">Book from the Project form</span></span>

<span data-ttu-id="b05a1-135">Jako projektový manažer možná budete muset rezervovat zdroj na projekt, ale znáte pouze kritéria, nikoli název zdroje.</span><span class="sxs-lookup"><span data-stu-id="b05a1-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="b05a1-136">Chcete-li použít asistenta plánování k vyhledání prostředku na základě všech dostupných atributů prostředku, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="b05a1-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="b05a1-137">Přejděte na projekt a vyberte **Rezervovat** pro otevření pomocníka plánování.</span><span class="sxs-lookup"><span data-stu-id="b05a1-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="b05a1-138">Pomocí filtrů na levé straně pomocníka plánování zúžte kritéria a vyberte **Vyhledávání.**</span><span class="sxs-lookup"><span data-stu-id="b05a1-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="b05a1-139">Na základě prostředků vrácených ve výsledcích si můžete rezervovat zdroj.</span><span class="sxs-lookup"><span data-stu-id="b05a1-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="b05a1-140">Tato metoda nevytváří žádné rezervace pro prostředek.</span><span class="sxs-lookup"><span data-stu-id="b05a1-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="b05a1-141">Místo toho přidá zdroj do týmu.</span><span class="sxs-lookup"><span data-stu-id="b05a1-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="b05a1-142">Poté, co byl člen týmu přidán do projektu, může vedoucí projektu pomocí udržování rezervací nebo rozšíření rezervací přidat požadované rezervace do zdroje.</span><span class="sxs-lookup"><span data-stu-id="b05a1-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
