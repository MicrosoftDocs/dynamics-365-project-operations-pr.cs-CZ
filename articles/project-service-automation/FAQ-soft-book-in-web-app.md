---
title: Jak předběžně rezervovat zdroje v aplikaci verze 2.x?
description: Tento článek popisuje, jak předběžně rezervovat členy týmu projektu s pomocí Project Service.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Applies to Project Service version 2.x
ms.technology: ''
ms.assetid: 27063de4-cb0c-436f-970e-c87ebcab92db
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: aad119c0907cdd31220a0d73e6e7d99ee63e2e13
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750345"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="65358-103">Jak předběžně rezervuji zdroje ve webové aplikaci (Project Service app v2.x)?</span><span class="sxs-lookup"><span data-stu-id="65358-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="65358-104">Nezávazně můžete naplánovat nebo předběžně rezervovat zdroj do projektového týmu pro zobrazení toho, že plánujete přiřazení zdroje k projektu.</span><span class="sxs-lookup"><span data-stu-id="65358-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="65358-105">Předběžné rezervace nespotřebovávají dostupné kapacity zdroje.</span><span class="sxs-lookup"><span data-stu-id="65358-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="65358-106">Předběžně rezervované členy týmu nelze přiřadit k úkolům projektu.</span><span class="sxs-lookup"><span data-stu-id="65358-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="65358-107">Pouze závazně rezervované zdroje a s typem potvrzení Potvrzeno lze přiřadit k úkolům (za předpokladu, že mají dostatek rezervačních hodin k pokrytí úsilí přiřazení).</span><span class="sxs-lookup"><span data-stu-id="65358-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="65358-108">Předběžně rezervovaní členové týmu projektu se zobrazí v mřížce Člen týmu s předběžně rezervovanými hodinami zobrazenými ve sloupci předběžné rezervace.</span><span class="sxs-lookup"><span data-stu-id="65358-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="65358-109">Zobrazí se také na plánovací vývěsce.</span><span class="sxs-lookup"><span data-stu-id="65358-109">They also show up on the schedule board.</span></span> <span data-ttu-id="65358-110">Neoznačují jakoukoli spotřebu kapacity, protože předběžně rezervované zdroje nespotřebovávají kapacitu zdroje.</span><span class="sxs-lookup"><span data-stu-id="65358-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="65358-111">Existují tři způsoby předběžné rezervace člena týmu na projekt s verzí služby Project Service 2.x.</span><span class="sxs-lookup"><span data-stu-id="65358-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="65358-112">Můžete provést předběžnou rezervaci pomocí plánovací vývěsky, použít funkci Správa rezervace nebo vytvořit obecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="65358-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="65358-113">Tyto metody jsou popsány níže.</span><span class="sxs-lookup"><span data-stu-id="65358-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="65358-114">Předběžná rezervace pomocí plánovací vývěsky</span><span class="sxs-lookup"><span data-stu-id="65358-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="65358-115">Chcete-li vytvořit předběžnou rezervaci pomocí plánovací vývěsky, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="65358-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="65358-116">Otevřete plánovací vývěsku.</span><span class="sxs-lookup"><span data-stu-id="65358-116">Open the schedule board.</span></span>
2. <span data-ttu-id="65358-117">Zvolte kartu Projekt na spodním panelu Požadavky na rezervace v plánovací vývěsce.</span><span class="sxs-lookup"><span data-stu-id="65358-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="65358-118">Najděte projekt, na který chcete předběžně rezervovat zdroj.</span><span class="sxs-lookup"><span data-stu-id="65358-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="65358-119">Pokud máte mnoho projektů, klikněte na záhlaví sloupce Projekt a pak použijte filtr k vyhledání projektu.</span><span class="sxs-lookup"><span data-stu-id="65358-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="65358-120">Klikněte na projekt a potom ho přetáhněte na časovou mřížku zdroje.</span><span class="sxs-lookup"><span data-stu-id="65358-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="65358-121">Otevře se panel Vytvořit rezervaci zdroje na pravé straně.</span><span class="sxs-lookup"><span data-stu-id="65358-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="65358-122">Upravte počáteční a koncové datum, vyberte Stav rezervace jako Předběžná a nastavte hodiny.</span><span class="sxs-lookup"><span data-stu-id="65358-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="65358-123">Klikněte na Rezervovat.</span><span class="sxs-lookup"><span data-stu-id="65358-123">Click Book.</span></span>
7. <span data-ttu-id="65358-124">Zpět na projektu se nyní zobrazí zdroj jako člen týmu s předběžně rezervovanými hodinami ve sloupci Předběžná rezervace.</span><span class="sxs-lookup"><span data-stu-id="65358-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="65358-125">Všimněte si, že je nelze přiřadit k úkolům ve strukturovaném rozpisu práce, protože prostředky musí být závazně rezervovány na týmu, aby je bylo možné přiřadit.</span><span class="sxs-lookup"><span data-stu-id="65358-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="65358-126">Předběžná rezervace pomocí funkce Správa rezervací</span><span class="sxs-lookup"><span data-stu-id="65358-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="65358-127">Chcete-li vytvořit předběžnou rezervaci pomocí správy rezervace, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="65358-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="65358-128">V mřížce člena týmu klikněte na Nový.</span><span class="sxs-lookup"><span data-stu-id="65358-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="65358-129">Vyberte rezervovatelný zdroj, roli, od/do.</span><span class="sxs-lookup"><span data-stu-id="65358-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="65358-130">Vyberte metodu přidělení jinou než Žádná:</span><span class="sxs-lookup"><span data-stu-id="65358-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="65358-131">Plná kapacita</span><span class="sxs-lookup"><span data-stu-id="65358-131">Full Capacity</span></span>
- <span data-ttu-id="65358-132">Procentuální kapacita</span><span class="sxs-lookup"><span data-stu-id="65358-132">Percentage Capacity</span></span>
- <span data-ttu-id="65358-133">Rovnoměrně rozdělit podle hodin</span><span class="sxs-lookup"><span data-stu-id="65358-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="65358-134">Vytížení na začátku podle hodin</span><span class="sxs-lookup"><span data-stu-id="65358-134">By Hours Front Load</span></span>
4. <span data-ttu-id="65358-135">Klikněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="65358-135">Click Save.</span></span> <span data-ttu-id="65358-136">Zdroje uvidíte na mřížce týmu a jejich hodiny budou označené jako Závazné.</span><span class="sxs-lookup"><span data-stu-id="65358-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="65358-137">Kliknutím na Správa rezervací spravujte rezervace zdroje.</span><span class="sxs-lookup"><span data-stu-id="65358-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="65358-138">Při otevření plánovací vývěsky rozbalte zdroje pro zobrazení jejich rezervací.</span><span class="sxs-lookup"><span data-stu-id="65358-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="65358-139">Uvidíte rezervaci označenou jako Závazná.</span><span class="sxs-lookup"><span data-stu-id="65358-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="65358-140">Klikněte pravým tlačítkem myši na rezervaci a u možnosti Změnit stav vyberte Předběžná rezervace a potom Předběžná.</span><span class="sxs-lookup"><span data-stu-id="65358-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="65358-141">Stav rezervace je nyní Předběžná.</span><span class="sxs-lookup"><span data-stu-id="65358-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="65358-142">Po uzavření plánovací vývěsky uvidíte, že se hodiny pro zdroj změnily ze závazných na předběžné na mřížce člena týmu.</span><span class="sxs-lookup"><span data-stu-id="65358-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="65358-143">Mějte na paměti, že pokud závazně rezervujete zdroj pro tým a poté mu přiřadíte úkoly ve strukturovaném rozpisu prací, když používáte správu rezervací pro změnu stavu ze závazné na předběžnou, odeberou se z úkolů přiřazení pro tento zdroj, protože pouze závazně rezervované zdroje lze přiřadit k úkolům.</span><span class="sxs-lookup"><span data-stu-id="65358-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="65358-144">Předběžná rezervace vytvořením obecného zdroje</span><span class="sxs-lookup"><span data-stu-id="65358-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="65358-145">Předběžnou rezervaci můžete vytvořit pomocí vygenerování obecného člena týmu zdrojů podle plánovací vývěsky nebo žádosti o zdroj a změnou typu během rezervace.</span><span class="sxs-lookup"><span data-stu-id="65358-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="65358-146">Pro vykonání této akce použijte tento postup:</span><span class="sxs-lookup"><span data-stu-id="65358-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="65358-147">Ve strukturovaném rozpisu prací projektu přiřaďte role k úkolům, pro které chcete vygenerovat obecné členy týmu.</span><span class="sxs-lookup"><span data-stu-id="65358-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="65358-148">Klikněte na Vygenerovat projektový tým.</span><span class="sxs-lookup"><span data-stu-id="65358-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="65358-149">V mřížce člena týmu projektu vyberte obecný zdroj a klikněte na Rezervovat.</span><span class="sxs-lookup"><span data-stu-id="65358-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="65358-150">Na plánovací vývěsce vyberte zdroj, který chcete rezervovat.</span><span class="sxs-lookup"><span data-stu-id="65358-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="65358-151">Na panelu Vytvořit rezervaci zdroje plánovací vývěsky změňte stav rezervace na Předběžná.</span><span class="sxs-lookup"><span data-stu-id="65358-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="65358-152">Klikněte na Rezervovat nebo Rezervovat a Ukončit.</span><span class="sxs-lookup"><span data-stu-id="65358-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="65358-153">Po zavření plánovací vývěsky uvidíte vybraný zdroj přidaný do týmu s předběžně rezervovanými hodinami a přiřazenými hodinami.</span><span class="sxs-lookup"><span data-stu-id="65358-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="65358-154">Uvidíte také, že obecný zdroj zůstane v týmu jako ukazatel, že úkoly jsou přiřazeny předběžně rezervovanému členu týmu.</span><span class="sxs-lookup"><span data-stu-id="65358-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="65358-155">Pokud budete chtít změnit předběžně rezervovaný zdroj člena týmu na závazně rezervovaného člena týmu, abyste mu mohli přiřadit úkoly, proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="65358-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="65358-156">Vyberte zdroj a klikněte na tlačítko Správa rezervací.</span><span class="sxs-lookup"><span data-stu-id="65358-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="65358-157">Při otevření plánovací vývěsky rozbalte zdroje pro zobrazení jejich rezervací.</span><span class="sxs-lookup"><span data-stu-id="65358-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="65358-158">Uvidíte rezervaci označenou jako Předběžná.</span><span class="sxs-lookup"><span data-stu-id="65358-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="65358-159">Klikněte pravým tlačítkem myši na rezervaci a u možnosti Změnit stav vyberte Závazná rezervace a potom Závazná.</span><span class="sxs-lookup"><span data-stu-id="65358-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="65358-160">Stav rezervace je nyní Závazná.</span><span class="sxs-lookup"><span data-stu-id="65358-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="65358-161">Po uzavření plánovací vývěsky uvidíte, že se hodiny pro zdroj změnily ze předběžných na závazné na mřížce člena týmu.</span><span class="sxs-lookup"><span data-stu-id="65358-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="65358-162">Nyní můžete přiřadit zdroj k úkolům (za předpokladu, že existuje shoda mezi závazně rezervovanými hodinami a hodinami úsilí úkolu pro přiřazení).</span><span class="sxs-lookup"><span data-stu-id="65358-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="65358-163">Všimněte si, že pokud jste postupovali podle kroků plnění obecného zdroje ve výše uvedeném bodu 3, při změně stavu předběžně rezervovaného zdroje na závazně rezervovaný, obecný člen týmu se z týmu odstraní.</span><span class="sxs-lookup"><span data-stu-id="65358-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>
