---
title: Rezervace pojmenovaných zdrojů z požadavků na zdroje
description: Toto téma obsahuje informace o rezervaci pojmenovaných zdrojů pro požadavek na obecný zdroj.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: c2f97107de938975491770ab4e2ed18a3145d0e3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013388"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="975d3-103">Rezervace pojmenovaných zdrojů z požadavků na zdroje</span><span class="sxs-lookup"><span data-stu-id="975d3-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="975d3-104">Pro nahrazení obecného zdroje, který obsahuje požadavek na zdroj, můžete rezervovat pojmenovaný zdroj.</span><span class="sxs-lookup"><span data-stu-id="975d3-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="975d3-105">V Project Service Automation (PSA) klikněte na stránce **Projekty** na kartu **Tým**.</span><span class="sxs-lookup"><span data-stu-id="975d3-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="975d3-106">Vyberte ze seznamu obecný zdroj, který obsahuje požadavek na zdroj, a pak klikněte na **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="975d3-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="975d3-107">Nebo otevřete požadavek na zdroj a pak klikněte na **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="975d3-107">Or, open the resource requirement and then click **Book**.</span></span>


![Rezervace obecného člena týmu](media/RM-how-to-14.png)


3. <span data-ttu-id="975d3-109">Na stránce **Pomocník plánování** vyberte pojmenovaný zdroj, který chcete rezervovat pro projektový tým, a klikněte na tlačítko **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="975d3-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Rezervace obecného člena týmu pomocí pomocníka pro plánování](media/RM-how-to-15.png)

<span data-ttu-id="975d3-111">Pokud je rezervace dokončena a vyplněna pojmenovaným zdrojem, je obecný zdroj nahrazen pojmenovaným zdrojem.</span><span class="sxs-lookup"><span data-stu-id="975d3-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Nahrazení obecného člena týmu pojmenovaným členem týmu](media/RM-how-to-16.png)

<span data-ttu-id="975d3-113">Přiřazení v plánu jsou aktualizována také pomocí pojmenovaného zdroje.</span><span class="sxs-lookup"><span data-stu-id="975d3-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Pojmenovaný člen týmu přiřazený k úkolům projektu](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="975d3-115">Vyplnění obecného zdroje pomocí několika pojmenovaných zdrojů</span><span class="sxs-lookup"><span data-stu-id="975d3-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="975d3-116">Vyplnění požadavku na obecný zdroj pomocí několika pojmenovaných zdrojů je podobné přiřazení jednoho pojmenovaného zdroje.</span><span class="sxs-lookup"><span data-stu-id="975d3-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="975d3-117">Existuje například úkol s dobou trvání pět dní a úsilím 120 hodin.</span><span class="sxs-lookup"><span data-stu-id="975d3-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="975d3-118">Tento úkol nemůže být dokončen jedním zdrojem, který pracuje typicky osm hodin denně, pět dní v týdnu.</span><span class="sxs-lookup"><span data-stu-id="975d3-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Úkol, který potřebuje 120 hodin úsilí po dobu pěti dnů](media/RM-how-to-21.png)

<span data-ttu-id="975d3-120">Požadavek je na 120 hodin robotického inženýrství po dobu pěti dní, což je 24 hodin denně.</span><span class="sxs-lookup"><span data-stu-id="975d3-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Požadavek na den](media/RM-how-to-22.png)

<span data-ttu-id="975d3-122">Toto je příklad, kdy je k naplnění obecného požadavku na zdroj potřeba více pojmenovaných zdrojů.</span><span class="sxs-lookup"><span data-stu-id="975d3-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="975d3-123">Pro splnění požadavku budete potřebovat rezervovat více zdrojů.</span><span class="sxs-lookup"><span data-stu-id="975d3-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Rezervace více zdrojů pro splnění požadavku](media/RM-how-to-23.png)

<span data-ttu-id="975d3-125">Hlavní rozdíl v tomto scénáři spočívá v tom, že obecný zdroj zůstává v týmu přiřazeném k úkolu, a že zarezervovaní pojmenovaní členové týmu zdrojů nejsou přiřazeni jako součást pozice.</span><span class="sxs-lookup"><span data-stu-id="975d3-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="975d3-126">Projektový manažer může přiřadit práci odpovídající pojmenovaným zdrojům.</span><span class="sxs-lookup"><span data-stu-id="975d3-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="975d3-127">Zobrazení **Vyrovnání** může projektovému manažerovi pomoci při rozdělování rezervací mezi více zdrojů pro přiřazení úkolů.</span><span class="sxs-lookup"><span data-stu-id="975d3-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="975d3-128">Není to prováděno automaticky, protože v libovolném scénáři, který je složitější než výše uvedený jednoduchý příklad, kdy například máte balík úkolů, které tvoří požadavek, musí být záměr, jak chce projektový manažer přiřazení provést, vypočten systémem.</span><span class="sxs-lookup"><span data-stu-id="975d3-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="975d3-129">Protože systém nedokáže pochopit záměr, je pravděpodobné, že předpoklady budou jiné, než je zamýšleno, a dojde k nesprávnému nebo nepředvídatelnému výsledku.</span><span class="sxs-lookup"><span data-stu-id="975d3-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="975d3-130">Předvídatelným výsledkem je, že obecný zdroj zůstává přiřazen, dokud projektový manažer záměrně nevytvoří přiřazení pomocí zobrazení **Vyrovnání**.</span><span class="sxs-lookup"><span data-stu-id="975d3-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]