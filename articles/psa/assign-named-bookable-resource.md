---
title: Rezervujte pro projektový tým pojmenované rezervovatelné zdroje a přiřaďte úkoly
description: Toto téma obsahuje informace o rezervaci pojmenovaných zdrojů pro projektové týmy a jejich přiřazování k úkolům.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: defc92e701ae6baf9d54f41dca123a09ef834c35
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073899"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="48c1c-103">Rezervujte pro projektový tým pojmenované rezervovatelné zdroje a přiřaďte úkoly</span><span class="sxs-lookup"><span data-stu-id="48c1c-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="48c1c-104">Pojmenovaný zdroj můžete do vašeho projektového týmu přidat pomocí přímé rezervace pro tým.</span><span class="sxs-lookup"><span data-stu-id="48c1c-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="48c1c-105">Postup je uveden níže.</span><span class="sxs-lookup"><span data-stu-id="48c1c-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="48c1c-106">V Project Service Automation přejděte na **Projekty** a vyberte otevření projektu, pro který provádíte rezervaci.</span><span class="sxs-lookup"><span data-stu-id="48c1c-106">In  Project Service Automation, go to **Projects** , and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="48c1c-107">Na stránce **Projekt** klikněte na kartě **Tým** na **Nový**.</span><span class="sxs-lookup"><span data-stu-id="48c1c-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Přidání člena týmu z karty týmu](media/RM-how-to-1.png)

3. <span data-ttu-id="48c1c-109">V dialogovém okně **Vytvořit: Člen projektového týmu** vyberte rezervovatelný zdroj.</span><span class="sxs-lookup"><span data-stu-id="48c1c-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="48c1c-110">Pole **Role** se vyplní výchozí rolí zdroje, pokud je přiřazena.</span><span class="sxs-lookup"><span data-stu-id="48c1c-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="48c1c-111">V případě potřeby můžete roli změnit.</span><span class="sxs-lookup"><span data-stu-id="48c1c-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="48c1c-112">Vyberte data od a do, kdy bude zdroj vyžadován, a vyberte metodu přidělení kapacity zdroje.</span><span class="sxs-lookup"><span data-stu-id="48c1c-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="48c1c-113">Pokud chcete, aby byl člen týmu schvalovatelem projektu, vyberte **Ano** v poli **Schvalovatel projektu**.</span><span class="sxs-lookup"><span data-stu-id="48c1c-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="48c1c-114">To bude znamenat, že tento člen týmu může schválit odeslané časové a výdajové záznamy pro tento projekt.</span><span class="sxs-lookup"><span data-stu-id="48c1c-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="48c1c-115">Klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="48c1c-115">Click **Save**.</span></span>

![Přidání člena týmu na stručný formulář pro vytvoření](media/RM-how-to-2.png)


<span data-ttu-id="48c1c-117">Nyní můžete rezervovaný zdroj přiřadit k úkolům v projektu.</span><span class="sxs-lookup"><span data-stu-id="48c1c-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="48c1c-118">Chcete-li přiřadit úkoly k novému zdroji, klikněte na stránce **Projekt** na kartu **Plán**.</span><span class="sxs-lookup"><span data-stu-id="48c1c-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="48c1c-119">Výběr zdroje, který se spouští z pole **Zdroje** v mřížce úkolu, zobrazí členy týmu, které můžete vybrat.</span><span class="sxs-lookup"><span data-stu-id="48c1c-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Přiřazení člena týmu k úkolu na kartě plánu](media/RM-how-to-3.png)

<span data-ttu-id="48c1c-121">Ve verzi 3 pro Project Service Automation (PSA) nejsou rezervace zdrojů a přiřazení úkolů úzce spojeny.</span><span class="sxs-lookup"><span data-stu-id="48c1c-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="48c1c-122">To znamená, že pokud použijete výběr zdroje v plánu, můžete členům týmu přiřadit úkoly na více hodin, než jejich rezervace pokrývají projekt.</span><span class="sxs-lookup"><span data-stu-id="48c1c-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="48c1c-123">Rozdíly mezi rezervacemi a přiřazeními členů týmu lze zobrazit na kartě **Tým** nebo na kartě **Vyrovnání zdrojů**. Můžete také vyrovnat rozdíly mezi rezervacemi a přiřazeními zdrojů na podrobnější úrovni.</span><span class="sxs-lookup"><span data-stu-id="48c1c-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Karta Vyrovnání zdrojů](media/RM-how-to-4.png)

<span data-ttu-id="48c1c-125">Pomocí výběru zdroje na kartě **Plán** můžete také vyhledat a vybrat rezervovatelné zdroje, které ještě nejsou součástí projektového týmu.</span><span class="sxs-lookup"><span data-stu-id="48c1c-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="48c1c-126">Tyto jsou ve výběru zdroje zobrazeny jako **Další zdroje**.</span><span class="sxs-lookup"><span data-stu-id="48c1c-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Přiřazení zdroje, který není členem týmu, k úkolu](media/RM-how-to-5.png)

<span data-ttu-id="48c1c-128">Pokud to uděláte, bude zdroj přidán do projektového týmu a přiřazen k úkolu, ale nebudou generovány žádné rezervace.</span><span class="sxs-lookup"><span data-stu-id="48c1c-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Člen týmu s přiřazeními a bez rezervací](media/RM-how-to-6.png)

<span data-ttu-id="48c1c-130">K rezervaci kapacity zdroje pro projekt můžete použít funkci prodloužení rezervace na kartě **Vyrovnání** nebo **Plánovací vývěska**.</span><span class="sxs-lookup"><span data-stu-id="48c1c-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Rozšíření rezervací pro člena týmu na kartě vyrovnání prostředků](media/RM-how-to-7.png)

<span data-ttu-id="48c1c-132">Po rezervaci člena týmu ve vašem projektu můžete použít správu rezervací nebo pomocí Plánovací vývěsky přímo spravovat jejich rezervace.</span><span class="sxs-lookup"><span data-stu-id="48c1c-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
