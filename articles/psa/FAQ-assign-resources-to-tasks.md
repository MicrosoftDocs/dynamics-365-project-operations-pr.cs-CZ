---
title: Přiřazení zdroje k úkolu
description: Toto téma obsahuje informace o způsobu přiřazení zdrojů k úkolům.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073969"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="a1be5-103">Přiřazení zdroje k úkolu</span><span class="sxs-lookup"><span data-stu-id="a1be5-103">Assign a resource to a task</span></span>

<span data-ttu-id="a1be5-104">Existují tři způsoby, jak přiřadit zdroj k úkolu v Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a1be5-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="a1be5-105">Rezervace zdroje jako člena týmu a následné přiřazení zdroje k úkolu</span><span class="sxs-lookup"><span data-stu-id="a1be5-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="a1be5-106">Můžete přidat zdroj do projektového týmu a poté přiřadit zdroj k úkolům v plánu projektu.</span><span class="sxs-lookup"><span data-stu-id="a1be5-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="a1be5-107">Na kartě **Člen týmu** přidejte nového člena týmu výběrem možnosti **Nový**.</span><span class="sxs-lookup"><span data-stu-id="a1be5-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="a1be5-108">Otevře se panel **Rychlé vytvoření člena týmu** , kde můžete zvolit název rezervovatelného zdroje a nastavit roli.</span><span class="sxs-lookup"><span data-stu-id="a1be5-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="a1be5-109">Vyberte jednu z následujících metod přidělení pro rezervaci zdroje:</span><span class="sxs-lookup"><span data-stu-id="a1be5-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="a1be5-110">**Plná kapacita** rezervuje plnou kapacitu zdroje pro zadaná počáteční a koncová data.</span><span class="sxs-lookup"><span data-stu-id="a1be5-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="a1be5-111">**Procentuální kapacita** rezervuje zdroj pro procento kapacity zdroje pro daná počáteční a koncová data.</span><span class="sxs-lookup"><span data-stu-id="a1be5-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="a1be5-112">**Rovnoměrně rozdělit podle hodin** rezervuje zdroj pro určený počet hodin a distribuuje ho rovnoměrně každý den v období od počátečního do koncového data.</span><span class="sxs-lookup"><span data-stu-id="a1be5-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="a1be5-113">**Vytížení na začátku podle hodin** rezervuje zdroj pro určený počet hodin s vytížením na začátku každý den v období od počátečního do koncového data.</span><span class="sxs-lookup"><span data-stu-id="a1be5-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="a1be5-114">**Žádné** přidá zdroj k týmu, ale nevytvoří žádné rezervace, které absorbují kapacitu zdroje.</span><span class="sxs-lookup"><span data-stu-id="a1be5-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="a1be5-115">Na mřížce **Plán** zvolte pro úkol ikonu **Zdroj** v buňce zdroje a pak v části **Členové týmu** vyberte člena týmu, kterého jste právě přidali.</span><span class="sxs-lookup"><span data-stu-id="a1be5-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members** , select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="a1be5-116">Na kartách **Člen týmu** a **Vyrovnání** se u zdroje zobrazují rezervované a přiřazené hodiny.</span><span class="sxs-lookup"><span data-stu-id="a1be5-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="a1be5-117">Tyto hodiny by měly být stejné, ale není to nutné, protože rezervace a přiřazení nejsou pevně spjaty.</span><span class="sxs-lookup"><span data-stu-id="a1be5-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="a1be5-118">Karta **Vyrovnání** uvádí podrobnosti, pokud jsou odlišné, například při přiřazení více hodin zdroji, než jste rezervovali.</span><span class="sxs-lookup"><span data-stu-id="a1be5-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="a1be5-119">Tyto informace můžete v případě potřeby opravit rozšířením rezervací zdroje nebo změnou přiřazení.</span><span class="sxs-lookup"><span data-stu-id="a1be5-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="a1be5-120">Vytvoření obecného člena týmu prostřednictvím přiřazení úkolu</span><span class="sxs-lookup"><span data-stu-id="a1be5-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="a1be5-121">Pokud pomocí přiřazení úkolu vytvoříte obecného člena týmu, vytvoříte zástupce nebo obecný zdroj, který popisuje vlastnosti pojmenovaného zdroje, u kterého chcete, aby pracoval na úkolech.</span><span class="sxs-lookup"><span data-stu-id="a1be5-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="a1be5-122">Potom vygenerujete požadavek (nebo odešlete žádost pomocí požadavku), který slouží k vyhledávání a rezervaci pojmenovaného zdroje.</span><span class="sxs-lookup"><span data-stu-id="a1be5-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="a1be5-123">V mřížce **Plán** vyberte pro daný úkol ikonu **Zdroj** v buňce zdroje.</span><span class="sxs-lookup"><span data-stu-id="a1be5-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="a1be5-124">Zadejte název sloužící jako zástupný text názvu zdroje.</span><span class="sxs-lookup"><span data-stu-id="a1be5-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="a1be5-125">Například Programový manažer.</span><span class="sxs-lookup"><span data-stu-id="a1be5-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="a1be5-126">Vyberte **Vytvořit** a v poli **Rychlé vytvoření člena týmu** nastavte roli pro obecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="a1be5-126">Select **Create** , and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="a1be5-127">Můžete pokračovat k přiřazení úkolů tomuto zástupnému zdroji výběrem tohoto zdroje ve **Výběru zdrojů** pro daný úkol.</span><span class="sxs-lookup"><span data-stu-id="a1be5-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="a1be5-128">Jsou uvedeny pod položkou **Členové týmu**.</span><span class="sxs-lookup"><span data-stu-id="a1be5-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="a1be5-129">Po dokončení přiřazování obecného zdroje vyberte obecný zdroj na kartě **Tým** a poté vyberte **Vygenerovat požadavek** pro vytvoření požadavku na zdroj pro obecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="a1be5-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="a1be5-130">Vyberte **Rezervovat** pro obecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="a1be5-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="a1be5-131">Poté můžete použít Plánovací vývěsku k vyhledání a rezervaci skutečného zdroje.</span><span class="sxs-lookup"><span data-stu-id="a1be5-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="a1be5-132">Je také možné odeslat požadavek na splnění manažerem zdrojů.</span><span class="sxs-lookup"><span data-stu-id="a1be5-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="a1be5-133">Když je obecný zdroj naplněn pojmenovaným zdrojem, obecný zdroj je odebrán z týmu a přiřazení úkolů pro obecný zdroj jsou přiřazena k pojmenovanému zdroji, který splnil požadavek na zdroj obecného zdroje.</span><span class="sxs-lookup"><span data-stu-id="a1be5-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="a1be5-134">Přiřazení pojmenovaného zdroje ze seznamu všech rezervovatelných zdrojů</span><span class="sxs-lookup"><span data-stu-id="a1be5-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="a1be5-135">Můžete použít vyhledávací pole ve **Výběru zdrojů** pro vyhledání všech rezervovatelných zdrojů a přiřadit je k úkolu.</span><span class="sxs-lookup"><span data-stu-id="a1be5-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="a1be5-136">Zdroje přiřazené tímto způsobem jsou do týmu přidány bez jakýchkoli rezervací.</span><span class="sxs-lookup"><span data-stu-id="a1be5-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="a1be5-137">To je podobné jako přidání člena týmu a vybrání metody přidělení Žádná.</span><span class="sxs-lookup"><span data-stu-id="a1be5-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="a1be5-138">Zdroj se zobrazí se na kartách **Tým** a **Vyrovnání** jako zdroj pouze s přiřazením a nedostatečnou rezervací.</span><span class="sxs-lookup"><span data-stu-id="a1be5-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="a1be5-139">Zarezervujte je, pokud chcete použít jejich dostupnost.</span><span class="sxs-lookup"><span data-stu-id="a1be5-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="a1be5-140">V mřížce **Plán** vyberte pro daný úkol ikonu **Zdroj** v buňce zdroje.</span><span class="sxs-lookup"><span data-stu-id="a1be5-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="a1be5-141">Začněte psát název.</span><span class="sxs-lookup"><span data-stu-id="a1be5-141">Start typing a name.</span></span> <span data-ttu-id="a1be5-142">Výsledky vyhledání názvu se zobrazí ve **Výběru zdrojů** v části **Další zdroje**.</span><span class="sxs-lookup"><span data-stu-id="a1be5-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="a1be5-143">Vyberte zdroj, který chcete k úkolu přiřadit.</span><span class="sxs-lookup"><span data-stu-id="a1be5-143">Select the resource that you want to assign to the task.</span></span>

