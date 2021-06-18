---
title: Správa časových pásem
description: Když je projekt vytvořen, jeho časové pásmo je založeno na časovém pásmu definovaném v použité šabloně pracovní doby.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1480d68105be1041e791de567b180178b330d71e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997728"
---
# <a name="manage-time-zones"></a><span data-ttu-id="3e99f-103">Správa časových pásem</span><span class="sxs-lookup"><span data-stu-id="3e99f-103">Manage time zones</span></span>

<span data-ttu-id="3e99f-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="3e99f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="3e99f-105">Projekty</span><span class="sxs-lookup"><span data-stu-id="3e99f-105">Projects</span></span>

<span data-ttu-id="3e99f-106">Když je projekt vytvořen, časové pásmo je založeno na časovém pásmu definovaném v použité šabloně pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="3e99f-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="3e99f-107">Na kartě **Projekt** jsou datumy jsou vždy relativní k časovému pásmu uživatele, který je přihlášen na každé kartě, kromě karty **Úkol**. Při prohlížení strukturovaného rozpisu prací se datumy vždy zobrazí v časovém pásmu projektu.</span><span class="sxs-lookup"><span data-stu-id="3e99f-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="3e99f-108">Úlohy</span><span class="sxs-lookup"><span data-stu-id="3e99f-108">Tasks</span></span>

<span data-ttu-id="3e99f-109">Když je úkol vytvořen, čas zahájení, čas ukončení a počet hodin/den se řídí pracovní dobou projektu.</span><span class="sxs-lookup"><span data-stu-id="3e99f-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="3e99f-110">Například pokud je úkol vytvořen s projektem, jehož časové pásmo je -8 PST a má následující pracovní dobu: 9:00–17:00 od pondělí do pátku, jakýkoli úkol vytvořený bez přiřazení bude respektovat počáteční čas a čas ukončení kalendáře projektu.</span><span class="sxs-lookup"><span data-stu-id="3e99f-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="3e99f-111">Správa zdrojů pomocí časových pásem</span><span class="sxs-lookup"><span data-stu-id="3e99f-111">Manage resources with time zones</span></span>

<span data-ttu-id="3e99f-112">Pro přesné a předvídatelné výsledky při používání funkce **Prodloužit rezervaci** musí být splněny dva klíčové předpoklady:</span><span class="sxs-lookup"><span data-stu-id="3e99f-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="3e99f-113">Uživatel musí konfigurovat časové pásmo svého zařízení tak, aby odpovídalo časovému pásmu definovanému v systémové možnosti **Nastavení přizpůsobení**.</span><span class="sxs-lookup"><span data-stu-id="3e99f-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Nastavení časového pásma v systému Windows 10](media/reconcile-assignments-03.png)

  ![Nastavení časového pásma v nastavení personalizace](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="3e99f-116">Rezervovatelný zdroj musí mít alespoň jednu minutu pracovní doby, která se překrývá s průběhovými křivkami, které slouží k definování požadovaného rozšíření.</span><span class="sxs-lookup"><span data-stu-id="3e99f-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="3e99f-117">Například následující zdroje s pracovní dobou, která spadá mezi 9:00 a 19:00.</span><span class="sxs-lookup"><span data-stu-id="3e99f-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Porovnání průběhových křivek zdroje](media/reconcile-assignments-05.png)

<span data-ttu-id="3e99f-119">Následující tabulka znázorňuje:</span><span class="sxs-lookup"><span data-stu-id="3e99f-119">The following table shows:</span></span>

- <span data-ttu-id="3e99f-120">Šablona kalendáře projektu</span><span class="sxs-lookup"><span data-stu-id="3e99f-120">A project calendar template</span></span>
- <span data-ttu-id="3e99f-121">Zdroj A: Tento zdroj má stejný kalendář a je ve stejném časovém pásmu jako projekt.</span><span class="sxs-lookup"><span data-stu-id="3e99f-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="3e99f-122">Čas zahájení rezervace bude 9:00.</span><span class="sxs-lookup"><span data-stu-id="3e99f-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="3e99f-123">Zdroj B: Tento prostředek se nachází v jiném časovém pásmu než projekt a začíná v 7:00 v jejich časovém pásmu.</span><span class="sxs-lookup"><span data-stu-id="3e99f-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="3e99f-124">Rezervace však začnou v 9:00, protože to je nejčasnější počáteční čas průběhové křivky přiřazení.</span><span class="sxs-lookup"><span data-stu-id="3e99f-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="3e99f-125">Zdroje C a D: Zdroje jsou umístěny v různých časových pásmech, která se liší navzájem a také vůči projektu, a jejich rezervace začínají nejdříve v příslušných dostupných počátečních časech.</span><span class="sxs-lookup"><span data-stu-id="3e99f-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="3e99f-126">Entita</span><span class="sxs-lookup"><span data-stu-id="3e99f-126">Entity</span></span>  |<span data-ttu-id="3e99f-127">Kalendář</span><span class="sxs-lookup"><span data-stu-id="3e99f-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="3e99f-128">Šablona kalendáře projektu</span><span class="sxs-lookup"><span data-stu-id="3e99f-128">Project calendar template</span></span>   | ![kalendář projektu](media/reconcile-assignments-06.png) |
|<span data-ttu-id="3e99f-130">Zdroj A</span><span class="sxs-lookup"><span data-stu-id="3e99f-130">Resource A</span></span>  | ![Kalendář zdroje A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="3e99f-132">Zdroj B</span><span class="sxs-lookup"><span data-stu-id="3e99f-132">Resource B</span></span>  |  ![Kalendář zdroje B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="3e99f-134">Zdroj C</span><span class="sxs-lookup"><span data-stu-id="3e99f-134">Resource C</span></span>  |  ![Kalendář zdroje C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="3e99f-136">Zdroj D</span><span class="sxs-lookup"><span data-stu-id="3e99f-136">Resource D</span></span>  | ![Kalendář zdroje D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="3e99f-138">Když přejdete na zobrazení **Vyrovnání**, zobrazí se přiřazení zdrojů a přidružené nedostatečné rezervace.</span><span class="sxs-lookup"><span data-stu-id="3e99f-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Zobrazení odsouhlasení před rozšířením](media/reconcile-assignments-10.png)

<span data-ttu-id="3e99f-140">Poté, co byla u každého zdroje použita funkce rozšířené rezervace, jsou rezervace úspěšně rozšířeny u každého zdroje, protože pracovní doba každého zdroje se překrývala s průběhovými křivkami nedostatečné rezervace.</span><span class="sxs-lookup"><span data-stu-id="3e99f-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Zobrazení odsouhlasení po prodloužení rezervace](media/reconcile-assignments-11.png) 

<span data-ttu-id="3e99f-142">Všimněte si, že při detailnějším pohledu na podrobnosti rezervací se ukážou rozdíly v počátečním čase rezervací.</span><span class="sxs-lookup"><span data-stu-id="3e99f-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="3e99f-143">Rezervace začínají nejdříve v počátečním čase průběhové křivky přiřazení a nejdříve v dostupném počátečním čase zdroje.</span><span class="sxs-lookup"><span data-stu-id="3e99f-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Nové rezervace zdrojů na plánovací vývěsce](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]