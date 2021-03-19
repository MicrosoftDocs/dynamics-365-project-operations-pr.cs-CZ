---
title: Vytvoření rezervace projektu z Plánovací vývěsky
description: Toto téma obsahuje informace o způsobu vytvoření rezervace projektu z plánovací vývěsky.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 5d815210ee78f3c728c0722e03bab2f790c953ee
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286105"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="83526-103">Vytvoření rezervace projektu z Plánovací vývěsky</span><span class="sxs-lookup"><span data-stu-id="83526-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="83526-104">Zdroj na projekt můžete rezervovat buď přímo z karty **Tým** projektu nebo generováním požadavku na zdroj z přiřazení obecného člena týmu a poté naplněním generovaného požadavku členem projektového týmu.</span><span class="sxs-lookup"><span data-stu-id="83526-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="83526-105">Můžete také rezervovat zdroj na projektu přímo z Plánovací vývěsky.</span><span class="sxs-lookup"><span data-stu-id="83526-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="83526-106">To lze vyřešit třemi způsoby:</span><span class="sxs-lookup"><span data-stu-id="83526-106">There are three ways to do this:</span></span>

- <span data-ttu-id="83526-107">**Rezervace z vygenerovaného požadavku na zdroj:** po vytvoření obecného zdroje a přiřazení úkolů v rámci projektu můžete vygenerovat požadavek na zdroj.</span><span class="sxs-lookup"><span data-stu-id="83526-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="83526-108">**Rezervace z primárního požadavku:** primární požadavky se zobrazují na kartě **Projekt** na plánovací vývěsce.</span><span class="sxs-lookup"><span data-stu-id="83526-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="83526-109">**Rezervace z nového požadavku na zdroj:** můžete vytvořit úplně nový požadavek na zdroj a přidružit ho k projektu.</span><span class="sxs-lookup"><span data-stu-id="83526-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="83526-110">Na plánovací vývěsce se tento požadavek na zdroj zobrazuje na kartě **Otevřené požadavky**.</span><span class="sxs-lookup"><span data-stu-id="83526-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="83526-111">Rezervace z generovaného požadavku na zdroj</span><span class="sxs-lookup"><span data-stu-id="83526-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="83526-112">Můžete vytvořit obecný zdroj a přiřadit k němu jeden nebo více úkolů v rámci projektu.</span><span class="sxs-lookup"><span data-stu-id="83526-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="83526-113">Poté můžete vygenerovat požadavek na zdroj z obecného člena týmu.</span><span class="sxs-lookup"><span data-stu-id="83526-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="83526-114">Na Plánovací vývěsce se tento zdroj zobrazí na kartě **Otevřené požadavky**. Můžete chtít použít filtry sloupců na mřížce, pokud máte mnoho otevřených požadavků.</span><span class="sxs-lookup"><span data-stu-id="83526-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="83526-115">![Otevření karty Požadavky na plánovací vývěsce](media/FAQ-Project-Booking-Schedule-Board-1.png "Snímek obrazovky tabulky rezervací a přiřazení")</span><span class="sxs-lookup"><span data-stu-id="83526-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="83526-116">Vyberte požadavek.</span><span class="sxs-lookup"><span data-stu-id="83526-116">Select the requirement.</span></span> <span data-ttu-id="83526-117">Karta **Najít dostupnost** se zobrazí v horní části vybraného řádku.</span><span class="sxs-lookup"><span data-stu-id="83526-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="83526-118">Pokud vyberete tuto kartu, otevře se režim Pomocníka plánování plánovací vývěsky a poté vyfiltruje dostupné zdroje, které splňují požadavek na zdroj.</span><span class="sxs-lookup"><span data-stu-id="83526-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="83526-119">Potom můžete rezervovat zdroj.</span><span class="sxs-lookup"><span data-stu-id="83526-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="83526-120">Také můžete přetáhnout a umístit vybraný řádek z dolní části Plánovací vývěsky do buňky zdroje v mřížce výše.</span><span class="sxs-lookup"><span data-stu-id="83526-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="83526-121">Po přetažení se otevře panel **Vytvořit rezervaci zdroje** na pravé straně.</span><span class="sxs-lookup"><span data-stu-id="83526-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="83526-122">Výběr **Rezervace** zarezervuje zdroj na projektový tým.</span><span class="sxs-lookup"><span data-stu-id="83526-122">Selecting **Book** books the resource onto the project team.</span></span>

![Panel Vytvořit rezervaci zdroje](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="83526-124">Rezervace z primárního požadavku</span><span class="sxs-lookup"><span data-stu-id="83526-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="83526-125">Vytvoření projektu v aplikaci Project Service automaticky vytvoří požadavek na zdroj nazvaný Primární požadavek.</span><span class="sxs-lookup"><span data-stu-id="83526-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="83526-126">Jedná se o prázdný požadavek, umožňující rychle rezervovat zdroj pomocí Plánovací vývěsky bez generování požadavku nebo vytvoření požadavku od samého začátku.</span><span class="sxs-lookup"><span data-stu-id="83526-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="83526-127">Vzhledem k tomu, že požadavek je prázdný, bude nutné zadat data, stejně jako metodu přidělení a popřípadě hodiny.</span><span class="sxs-lookup"><span data-stu-id="83526-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="83526-128">Chcete-li rezervovat zdroj s Primárním požadavkem, zvolte na Plánovací vývěsce kartu **Projekt**. Možná budete chtít použít filtr sloupce ve sloupci **Projekt**, pokud máte příliš mnoho projektů.</span><span class="sxs-lookup"><span data-stu-id="83526-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="83526-129">![Filtry sloupců na plánovací vývěsce](media/FAQ-Project-Booking-Schedule-Board-2.png "Snímek obrazovky tabulky rezervací a přiřazení")</span><span class="sxs-lookup"><span data-stu-id="83526-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="83526-130">Vyberte požadavek, který má pouze název projektu jako svůj název a má nulovou dobu trvání (0).</span><span class="sxs-lookup"><span data-stu-id="83526-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="83526-131">Zvolte kartu **Najít dostupnost**, která se zobrazí na řádku.</span><span class="sxs-lookup"><span data-stu-id="83526-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="83526-132">To převede Plánovací vývěsku do režimu Pomocníka plánování a zobrazí dostupné prostředky, které lze rezervovat na projekt.</span><span class="sxs-lookup"><span data-stu-id="83526-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="83526-133">Protože **Primární požadavek** je prázdným požadavkem s nulovou dobou trvání (0), budete muset nastavit dobu trvání na panelu **Vytvořit rezervaci zdrojů** při výběru a rezervaci zdroje.</span><span class="sxs-lookup"><span data-stu-id="83526-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="83526-134">Můžete také vybrat **Primární požadavek projektu** v dolní části Plánovací vývěsky a přetáhnout a umístit ho na zdroj za účelem jeho rezervace.</span><span class="sxs-lookup"><span data-stu-id="83526-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="83526-135">Protože **Primární požadavek** je prázdným požadavkem s nulovou dobou trvání (0), budete muset nastavit dobu trvání na panelu **Vytvořit rezervaci zdrojů** při výběru a rezervaci zdroje.</span><span class="sxs-lookup"><span data-stu-id="83526-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="83526-136">Když rezervujete zdroj prostřednictvím **Primary Requirement** na Plánovací vývěsce, přidáte ho do projektového týmu bez jakýchkoli přiřazení.</span><span class="sxs-lookup"><span data-stu-id="83526-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="83526-137">Rezervace z nového požadavku na zdroj</span><span class="sxs-lookup"><span data-stu-id="83526-137">Book from a new resource requirement</span></span>
<span data-ttu-id="83526-138">Chcete-li provést rezervaci z nového požadavku na zdroj, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="83526-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="83526-139">Přejděte na **Požadavky na zdroj** a poté vyberte **Nový**, chcete-li vytvořit nový požadavek na zdroj.</span><span class="sxs-lookup"><span data-stu-id="83526-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="83526-140">Na kartě **Projekt** vyberte projekt, ke kterému chcete požadavek na projekt přidružit.</span><span class="sxs-lookup"><span data-stu-id="83526-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="83526-141">Tento nově vytvořený požadavek se na Plánovací vývěsce zobrazuje jako **Otevřený požadavek**, který můžete splnit.</span><span class="sxs-lookup"><span data-stu-id="83526-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="83526-142">Rezervace zdroje za účelem jeho přidání do projektového týmu.</span><span class="sxs-lookup"><span data-stu-id="83526-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="83526-143">Nyní, když je zdroj rezervován, musíte ručně přiřadit úkoly.</span><span class="sxs-lookup"><span data-stu-id="83526-143">Now that the resource is booked, you must assign tasks manually.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]