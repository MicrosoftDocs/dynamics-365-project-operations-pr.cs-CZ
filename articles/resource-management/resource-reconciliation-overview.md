---
title: Přehled odsouhlasení zdrojů
description: Toto téma poskytuje informace o zajištění toho, aby rezervace a přiřazení zdrojů k projektům byly sladěny.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: e2b16a6e1c48769ed4d903e546804ba1c4e1c4fa
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073722"
---
# <a name="resource-reconciliation-overview"></a><span data-ttu-id="9e168-103">Přehled odsouhlasení zdrojů</span><span class="sxs-lookup"><span data-stu-id="9e168-103">Resource reconciliation overview</span></span>

<span data-ttu-id="9e168-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="9e168-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9e168-105">Pro členy týmu jsou rezervace a přiřazení volně provázené.</span><span class="sxs-lookup"><span data-stu-id="9e168-105">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="9e168-106">Jinými slovy, zdroje mohou obsahovat přiřazení, ale žádné rezervace, nebo mohou obsahovat rezervace, ale žádná přiřazení.</span><span class="sxs-lookup"><span data-stu-id="9e168-106">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="9e168-107">V ideálním případě by měly být rezervace a přiřazení zarovnány, aby zdroje měly potvrzenou kapacitu k provádění přiřazení úkolů.</span><span class="sxs-lookup"><span data-stu-id="9e168-107">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="9e168-108">Rezervace mohou být však založeny na dostupnosti a časování úkolů se může při pokračování projektu změnit.</span><span class="sxs-lookup"><span data-stu-id="9e168-108">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="9e168-109">Volné spojení rezervací a přiřazení je proto flexibilní.</span><span class="sxs-lookup"><span data-stu-id="9e168-109">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="9e168-110">Karta **Vyrovnání** ve formuláři **Projekt** projektovým manažerům umožňuje vyrovnat rezervace a přiřazení členů týmů pro projektové týmy.</span><span class="sxs-lookup"><span data-stu-id="9e168-110">The **Reconciliation** tab on the **Project** form lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

<span data-ttu-id="9e168-111">Karta **Vyrovnání** také zobrazuje rezervace a přiřazení až k úrovni jednotlivých přiřazení úkolů pro každého člena týmu.</span><span class="sxs-lookup"><span data-stu-id="9e168-111">The **Reconciliation** tab also shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="9e168-112">Hodiny se zobrazují v buňkách reprezentujících časová období od měsíců po dny.</span><span class="sxs-lookup"><span data-stu-id="9e168-112">Hours are displayed in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="9e168-113">Na kartě je také zobrazen celkový čistý součet pro projekt, spolu se sloupcem **Celkem**.</span><span class="sxs-lookup"><span data-stu-id="9e168-113">The tab also shows an overall net total for the project, together with a **Total** column.</span></span>

<span data-ttu-id="9e168-114">Pro každý zdroj je na kartě vypočten rozdíl mezi rezervacemi člena týmu a souhrnnými přiřazeními člena týmu.</span><span class="sxs-lookup"><span data-stu-id="9e168-114">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="9e168-115">V ideálním případě by tento rozdíl měl být 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="9e168-115">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="9e168-116">Jinými slovy, mezi rezervacemi a přiřazeními by neměl být žádný rozdíl.</span><span class="sxs-lookup"><span data-stu-id="9e168-116">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="9e168-117">Rozdíly jsou barevné a stínované, aby upozornily na dva stavy:</span><span class="sxs-lookup"><span data-stu-id="9e168-117">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="9e168-118">**Nedostatečná rezervace** – v případě, že zdroj obsahuje více přiřazení než rezervací, dojde k nedostatatečné rezervaci.</span><span class="sxs-lookup"><span data-stu-id="9e168-118">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="9e168-119">Vzhledem k tomu, že tato kapacita nebyla rezervována, může projektový manažer tento stav napravit rozšířením rezervací zdroje tak, aby pokryly deficit.</span><span class="sxs-lookup"><span data-stu-id="9e168-119">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="9e168-120">**Nadbytečné rezervace** – k nadbytečným rezervacím dochází, pokud byl zdroj rezervován do projektu, ale nebyl přiřazen k úkolům.</span><span class="sxs-lookup"><span data-stu-id="9e168-120">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="9e168-121">Tento stav může být přijatelný v případech, kdy byl zdroj pro projekt rezervován předtím, než došlo k přiřazení úkolu.</span><span class="sxs-lookup"><span data-stu-id="9e168-121">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="9e168-122">V jiných případech však není plánováno přiřazení zdroje k úkolům.</span><span class="sxs-lookup"><span data-stu-id="9e168-122">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="9e168-123">V těchto případech by měl projektový manažer zvážit zrušení rezervací zdroje, aby bylo možné použít kapacitu pro jiný projekt.</span><span class="sxs-lookup"><span data-stu-id="9e168-123">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="9e168-124">Pokud v některých případech zobrazíte čas na vyšší úrovni než denní úroveň (například úroveň měsíce), můžete u zdroje vidět čistý nulový rozdíl (jinými slovy, rezervace = přiřazení).</span><span class="sxs-lookup"><span data-stu-id="9e168-124">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="9e168-125">Pokud však zobrazíte čas na úrovni týdne, můžete se setkat s tím, že v prvním týdnu jsou přiřazení ve výši nula hodin a rezervace 40 hodin, ale ve druhém týdnu jsou přiřazení 40 hodin a rezervace nula hodin.</span><span class="sxs-lookup"><span data-stu-id="9e168-125">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="9e168-126">Celkově jsou rezervace a přiřazení vyrovnané, liší se však od jednoho týdne k dalšímu.</span><span class="sxs-lookup"><span data-stu-id="9e168-126">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="9e168-127">Když zobrazíte čas na vyšších úrovních, buňky na kartě **Vyrovnání** mají indikátor, který vás upozorní, že se na nižších úrovních vyskytují rozdíly.</span><span class="sxs-lookup"><span data-stu-id="9e168-127">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="9e168-128">Dvojitým kliknutím do buňky můžete provést přiblížení a zobrazit rozdíl.</span><span class="sxs-lookup"><span data-stu-id="9e168-128">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="9e168-129">Kliknutím pravým tlačítkem myši můžete zobrazení oddálit. Výběrem zdroje a následným použitím ovládacího prvku **Další rozdíl** na panelu nástrojů mřížky můžete přejít na další rozdíl mezi rezervacemi a přiřazeními pro daný zdroj.</span><span class="sxs-lookup"><span data-stu-id="9e168-129">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="9e168-130">Poté můžete použít ovládací prvek **Předchozí rozdíl** a vrátit se zpět.</span><span class="sxs-lookup"><span data-stu-id="9e168-130">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="9e168-131">V **Nastavení** také můžete vypnout ukazatel rozdílu a chování navigace.</span><span class="sxs-lookup"><span data-stu-id="9e168-131">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>


<span data-ttu-id="9e168-132">Pokud máte pro zdroj přiřazení úkolů, ale nemáte žádné rezervace, vyberte na stránce **Projekty** , na kartě **Vyrovnání** nedostatečnou rezervaci a pak vyberte **Prodloužit rezervaci**.</span><span class="sxs-lookup"><span data-stu-id="9e168-132">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="9e168-133">Zobrazí se dialogové okno **Prodloužit rezervaci** , ve kterém je uvedena rezervace potřebná k vyřešení nedostatku zdroje.</span><span class="sxs-lookup"><span data-stu-id="9e168-133">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="9e168-134">Zobrazuje také existující rezervace zdroje ve všech projektech nebo jiných plánovatelných entitách.</span><span class="sxs-lookup"><span data-stu-id="9e168-134">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="9e168-135">Pokud vyberete **OK** pro vytvoření rezervace pro zdroj bez ohledu na dostupnost zdroje, můžete způsobit přerezervaci.</span><span class="sxs-lookup"><span data-stu-id="9e168-135">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

<span data-ttu-id="9e168-136">Projektový manažer nebo správce prostředku pak může pomocí Plánovací vývěsky spravovat všechny situace, ve kterých je zdroj přerezervovaný nad svoji kapacitu.</span><span class="sxs-lookup"><span data-stu-id="9e168-136">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
