---
title: Obecné plnění požadavků na zdroje
description: Toto téma obsahuje informace o rezervaci pojmenovaných zdrojů pro požadavek na obecný zdroj.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c4d02fd589d4a5d39380688852377f57fceb05b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130299"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="4144d-103">Obecné plnění požadavků na zdroje</span><span class="sxs-lookup"><span data-stu-id="4144d-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="4144d-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="4144d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4144d-105">Pro nahrazení obecného zdroje, který obsahuje požadavek na zdroj, můžete rezervovat pojmenovaný zdroj.</span><span class="sxs-lookup"><span data-stu-id="4144d-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="4144d-106">Na stránce **Projekty** vyberte kartu **Tým**.</span><span class="sxs-lookup"><span data-stu-id="4144d-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="4144d-107">Vyberte ze seznamu obecný zdroj, který obsahuje požadavek na zdroj, a pak zvolte **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="4144d-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="4144d-108">Nebo otevřete požadavek na zdroj a pak zvolte **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="4144d-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="4144d-109">Na stránce **Pomocník plánování** vyberte pojmenovaný zdroj, který chcete rezervovat pro projektový tým, a zvolte **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="4144d-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="4144d-110">Pokud je rezervace dokončena a vyplněna pojmenovaným zdrojem, je obecný zdroj nahrazen pojmenovaným zdrojem.</span><span class="sxs-lookup"><span data-stu-id="4144d-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="4144d-111">Přiřazení v plánu jsou aktualizována také pomocí pojmenovaného zdroje.</span><span class="sxs-lookup"><span data-stu-id="4144d-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="4144d-112">Vyplnění obecného zdroje pomocí několika pojmenovaných zdrojů</span><span class="sxs-lookup"><span data-stu-id="4144d-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="4144d-113">Vyplnění požadavku na obecný zdroj pomocí několika pojmenovaných zdrojů je podobné přiřazení jednoho pojmenovaného zdroje.</span><span class="sxs-lookup"><span data-stu-id="4144d-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="4144d-114">Existuje například úkol s dobou trvání pět dní a úsilím 120 hodin.</span><span class="sxs-lookup"><span data-stu-id="4144d-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="4144d-115">Tento úkol nemůže být dokončen jedním zdrojem, který pracuje typicky osm hodin denně, pět dní v týdnu.</span><span class="sxs-lookup"><span data-stu-id="4144d-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="4144d-116">Požadavek je na 120 hodin robotického inženýrství po dobu pěti dní, což je 24 hodin denně.</span><span class="sxs-lookup"><span data-stu-id="4144d-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="4144d-117">Toto je příklad, kdy je k naplnění obecného požadavku na zdroj potřeba více pojmenovaných zdrojů.</span><span class="sxs-lookup"><span data-stu-id="4144d-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="4144d-118">Pro splnění požadavku budete potřebovat rezervovat více zdrojů.</span><span class="sxs-lookup"><span data-stu-id="4144d-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="4144d-119">Hlavní rozdíl v tomto scénáři spočívá v tom, že obecný zdroj zůstává v týmu přiřazeném k úkolu, a že zarezervovaní pojmenovaní členové týmu zdrojů nejsou přiřazeni jako součást pozice.</span><span class="sxs-lookup"><span data-stu-id="4144d-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="4144d-120">Projektový manažer může přiřadit práci odpovídající pojmenovaným zdrojům.</span><span class="sxs-lookup"><span data-stu-id="4144d-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="4144d-121">Zobrazení **Vyrovnání** může projektovému manažerovi pomoci při rozdělování rezervací mezi více zdrojů pro přiřazení úkolů.</span><span class="sxs-lookup"><span data-stu-id="4144d-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="4144d-122">Není to prováděno automaticky, protože v libovolném scénáři, který je složitější než výše uvedený jednoduchý příklad, kdy například máte balík úkolů, které tvoří požadavek, musí být záměr, jak chce projektový manažer přiřazení provést, vypočten systémem.</span><span class="sxs-lookup"><span data-stu-id="4144d-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="4144d-123">Protože systém nedokáže pochopit záměr, je pravděpodobné, že předpoklady budou jiné, než je zamýšleno, a dojde k nesprávnému nebo nepředvídatelnému výsledku.</span><span class="sxs-lookup"><span data-stu-id="4144d-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="4144d-124">Předvídatelným výsledkem je, že obecný zdroj zůstává přiřazen, dokud projektový manažer záměrně nevytvoří přiřazení pomocí zobrazení **Vyrovnání**.</span><span class="sxs-lookup"><span data-stu-id="4144d-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


