---
title: Jak přiřadit rezervovatelný zdroj k úkolu ve webové aplikaci
description: Přehled způsobů, kterými můžete přiřadit rezervovatelné zdroje.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7b95eff52351904f97c62b3806f17b02db47860b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073968"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="64323-103">Jak přiřadit rezervovatelný zdroj k úkolu ve webové aplikaci (aplikace Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="64323-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="64323-104">Existují dva způsoby, jak přiřadit zdroj k úkolu v aplikaci Project Service.</span><span class="sxs-lookup"><span data-stu-id="64323-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="64323-105">Můžete rezervovat zdroj jako člena týmu a pak ho přiřadit k úkolu.</span><span class="sxs-lookup"><span data-stu-id="64323-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="64323-106">Nebo můžete vytvořit obecného člena týmu prostřednictvím přiřazení role na úkoly, generovat tým a poté splnit podpůrné požadavky s pojmenovaným zdrojem.</span><span class="sxs-lookup"><span data-stu-id="64323-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="64323-107">Všimněte si, že pokud chcete přiřadit rezervovatelný zdroj k úkolu, rezervovatelný člen týmu zdrojů musí mít dostatek dostupných rezervací.</span><span class="sxs-lookup"><span data-stu-id="64323-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="64323-108">Stav rezervace musí být Typ potvrzení Závazně rezervovat a Stav potvrzeno.</span><span class="sxs-lookup"><span data-stu-id="64323-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="64323-109">Pokud není k dispozici dostatek rezervací pro zdroj, Project Service odebere přiřazení a zobrazí následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="64323-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="64323-110">*Nelze přiřadit zdroj k úkolu - Následující zdroje nemají dostatek hodin rezervovaných proti projektu*</span><span class="sxs-lookup"><span data-stu-id="64323-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="64323-111">Rezervace zdroje jako člena týmu a následné přiřazení zdroje k úkolu</span><span class="sxs-lookup"><span data-stu-id="64323-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="64323-112">Při použití této metody přidáte zdroj do projektového týmu a poté přiřadíte zdroje k úkolům v plánu projektu.</span><span class="sxs-lookup"><span data-stu-id="64323-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="64323-113">Zde je postup:</span><span class="sxs-lookup"><span data-stu-id="64323-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="64323-114">V mřížce člena týmu přidejte nového člena týmu výběrem možnosti **Nový**.</span><span class="sxs-lookup"><span data-stu-id="64323-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="64323-115">Na obrazovce rychlého vytvoření člena týmu zvolte název rezervovatelného zdroje a nastavte roli.</span><span class="sxs-lookup"><span data-stu-id="64323-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="64323-116">Zvolte data **Od** a **Do**.</span><span class="sxs-lookup"><span data-stu-id="64323-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="64323-117">![Screenshot znázorňující přidání člena týmu](media/FAQ-Resources-to-Tasks2-1.png "Screenshot znázorňující přidání člena týmu")</span><span class="sxs-lookup"><span data-stu-id="64323-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="64323-118">Vyberte jednu z následujících metod přidělení pro rezervaci zdroje:</span><span class="sxs-lookup"><span data-stu-id="64323-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="64323-119">**Plná kapacita** rezervuje plnou kapacitu zdroje pro zadaná počáteční a koncová data.</span><span class="sxs-lookup"><span data-stu-id="64323-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="64323-120">**Procentuální kapacita** rezervuje zdroj pro procento kapacity zdroje pro daná počáteční a koncová data.</span><span class="sxs-lookup"><span data-stu-id="64323-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="64323-121">**Rovnoměrně rozdělit podle hodin** rezervuje zdroj pro určený počet hodin a distribuuje ho rovnoměrně každý den v období od počátečního do koncového data.</span><span class="sxs-lookup"><span data-stu-id="64323-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="64323-122">**Vytížení na začátku podle hodin** rezervuje zdroj pro určený počet hodin s vytížením na začátku každý den v období od počátečního do koncového data.</span><span class="sxs-lookup"><span data-stu-id="64323-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="64323-123">Nevybírejte **Žádné** , protože to přidá zdroj k týmu, ale nevytvoří žádné rezervace, které absorbují kapacitu zdroje.</span><span class="sxs-lookup"><span data-stu-id="64323-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="64323-124">Vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="64323-124">Select **Save**.</span></span>

    <span data-ttu-id="64323-125">Všimněte si, že hodiny rezervace musí být dostatečné k pokrytí hodin úsilí a datového rozsahu úkolů, ke kterým přiřazujete tento zdroj.</span><span class="sxs-lookup"><span data-stu-id="64323-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="64323-126">Pokud nejsou ve shodě, nelze přiřadit zdroj k úkolu.</span><span class="sxs-lookup"><span data-stu-id="64323-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="64323-127">Na strukturovaném rozpisu prací pro daný úkol klikněte na rozevírací seznam buňky zdroje.</span><span class="sxs-lookup"><span data-stu-id="64323-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="64323-128">A poté:</span><span class="sxs-lookup"><span data-stu-id="64323-128">Then:</span></span> 

    1. <span data-ttu-id="64323-129">Vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="64323-129">Select **Add**.</span></span>
    2. <span data-ttu-id="64323-130">Vyberte rozevírací seznamu pod možností **Zdroje** a vyberte člena týmu, kterého jste přidali výše.</span><span class="sxs-lookup"><span data-stu-id="64323-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="64323-131">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="64323-131">Select **OK**.</span></span> <span data-ttu-id="64323-132">Člen týmu je nyní přiřazen k úkolu.</span><span class="sxs-lookup"><span data-stu-id="64323-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="64323-133">![Screenshot znázorňující přidání zdrojů pomocí WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot znázorňující přidání zdrojů pomocí WBS")</span><span class="sxs-lookup"><span data-stu-id="64323-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="64323-134">V mřížce člena týmu uvidíte agregaci přiřazených hodin zdroje pod položkou Přiřazené hodiny.</span><span class="sxs-lookup"><span data-stu-id="64323-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="64323-135">Bude menší nebo rovna rezervovaným hodinám pro daný zdroj.</span><span class="sxs-lookup"><span data-stu-id="64323-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="64323-136">![Screenshot znázorňující přiřazené hodiny zdroje](media/FAQ-Resources-to-Tasks2-3.png "Screenshot znázorňující přiřazené hodiny zdroje")</span><span class="sxs-lookup"><span data-stu-id="64323-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="64323-137">Pokud úloha, kterou se pokoušíte přiřadit zdroji, začíná po datu ukončení rezervace zdrojů, nebude zdroj v rozevíracím seznamu zobrazen.</span><span class="sxs-lookup"><span data-stu-id="64323-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="64323-138">Všimněte si, že můžete přiřadit zdroj více hodinám než jsou jeho rezervované hodiny, pokud má zdroj nějakou zbývající nepřiřazenou kapacitu.</span><span class="sxs-lookup"><span data-stu-id="64323-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="64323-139">V takovém případě bude zdroj pouze částečně přiřazen ke svým rezervacím.</span><span class="sxs-lookup"><span data-stu-id="64323-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="64323-140">Tyto zbývající nepřiřazené hodiny úloh můžete vidět přidáním sloupce Nevykryté hodiny do strukturovaného rozpisu prací.</span><span class="sxs-lookup"><span data-stu-id="64323-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="64323-141">Pokud jsou zdroje přiřazeny ke svým rezervovaným hodinám (jejich rezervované hodiny se shodují s přiřazenými hodinami), při pokusu o přiřazení dalších úkolů se zobrazí následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="64323-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="64323-142">*Nelze přiřadit zdroj k úkolu - Následující zdroje nemají dostatek hodin rezervovaných proti projektu.*</span><span class="sxs-lookup"><span data-stu-id="64323-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="64323-143">Navíc je při tvorbě projektu přidán výchozí člen týmu projektového manažera, který je přidán do týmu bez jakýchkoli rezervací a nemůže být přiřazen žádnému úkolu.</span><span class="sxs-lookup"><span data-stu-id="64323-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="64323-144">Nezobrazí se v rozevíracím seznamu zdrojů pro úkoly.</span><span class="sxs-lookup"><span data-stu-id="64323-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="64323-145">Chcete-li tento zdroj přiřadit, musíte ho odebrat z týmu a potom ho přidat znovu jinou metodou přidělení než Žádná.</span><span class="sxs-lookup"><span data-stu-id="64323-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="64323-146">Důvod, proč jsou přidáni do týmu při vytváření projektu, je ten, aby projekt měl ve výchozím nastavení alespoň jednoho schvalujícího projektu.</span><span class="sxs-lookup"><span data-stu-id="64323-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="64323-147">Vytvoření obecného člena týmu prostřednictvím přiřazení role na úkoly</span><span class="sxs-lookup"><span data-stu-id="64323-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="64323-148">Tato metoda zajišťuje, že zdroje mají dostatek rezervací pro úkoly.</span><span class="sxs-lookup"><span data-stu-id="64323-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="64323-149">Nejprve je třeba vytvořit zástupce nebo obecný zdroj, který popisuje vlastnosti pojmenovaného zdroje, u kterého chcete, aby pracoval na úkolech, vygenerováním týmu po přiřazení rolí k úkolům.</span><span class="sxs-lookup"><span data-stu-id="64323-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="64323-150">Zde je postup:</span><span class="sxs-lookup"><span data-stu-id="64323-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="64323-151">Na strukturovaném rozpisu prací vyberte požadovaný úkol.</span><span class="sxs-lookup"><span data-stu-id="64323-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="64323-152">Vyberte ikonu rozevíracího seznamu **Přiřazená role** v buňce zdroje.</span><span class="sxs-lookup"><span data-stu-id="64323-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="64323-153">Vyberte rozevírací seznam **Role** a vyberte roli pro obecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="64323-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="64323-154">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="64323-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="64323-155">![Screenshot znázorňující přidání zdroje pomocí WBS](media/FAQ-Resources-to-Tasks2-4.png "Screenshot znázorňující přidání zdroje pomocí WBS")</span><span class="sxs-lookup"><span data-stu-id="64323-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="64323-156">Po dokončení přiřazování rolí k úkolům ve strukturovaném rozpisu prací vyberte **Vygenerovat projektový tým**.</span><span class="sxs-lookup"><span data-stu-id="64323-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="64323-157">Project Service vytvoří minimální počet obecných členů týmu založený na rolích, organizačních jednotkách zdrojů a kalendáři projektu pomocí agregace přiřazení úkolů.</span><span class="sxs-lookup"><span data-stu-id="64323-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="64323-158">![Screenshot znázorňující generování projektového týmu](media/FAQ-Resources-to-Tasks2-5.png "Screenshot znázorňující generování projektového týmu")</span><span class="sxs-lookup"><span data-stu-id="64323-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="64323-159">Na mřížce Člen týmu se zobrazí zdroje typu Obecný zdroj s názvem role a pozice.</span><span class="sxs-lookup"><span data-stu-id="64323-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="64323-160">Pokud jsou potřebné dva zdroje pro roli k dokončení práce, funkce Vygenerovat tým vytvoří dva členy týmu a použije název pozice, aby je nastavila odděleně.</span><span class="sxs-lookup"><span data-stu-id="64323-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="64323-161">![Screenshot znázorňující přidání dvou obecných zdrojů](media/FAQ-Resources-to-Tasks2-6.png "Screenshot znázorňující přidání dvou obecných zdrojů")</span><span class="sxs-lookup"><span data-stu-id="64323-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="64323-162">Požadavek na podpůrný zdroj pro obecného člena týmu můžete otevřít výběrem odkazu v části Požadavek na zdroj.</span><span class="sxs-lookup"><span data-stu-id="64323-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="64323-163">![Screenshot znázorňující požadavek na podpůrný zdroj](media/FAQ-Resources-to-Tasks2-7.png "Screenshot znázorňující požadavek na podpůrný zdroj")</span><span class="sxs-lookup"><span data-stu-id="64323-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="64323-164">Vyberte možnost **Rezervovat** pro obecný zdroj a pak můžete použít plánovací vývěsku pro nalezení a rezervaci skutečného zdroje.</span><span class="sxs-lookup"><span data-stu-id="64323-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="64323-165">Je také možné odeslat požadavek na splnění manažerem zdrojů volbou **Odeslat požadavek**.</span><span class="sxs-lookup"><span data-stu-id="64323-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="64323-166">Když je obecný zdroj naplněn pojmenovaným zdrojem, obecný zdroj je odebrán z týmu a přiřazení úkolů pro obecný zdroj jsou přiřazena k pojmenovanému zdroji, který splnil požadavek na zdroj obecného zdroje.</span><span class="sxs-lookup"><span data-stu-id="64323-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

