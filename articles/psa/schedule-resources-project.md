---
title: Plánování zdrojů pro projekt
description: Postup plánování zdrojů pro projekt v Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073986"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="bca7f-103">Plánování zdrojů pro projekt (Project Service)</span><span class="sxs-lookup"><span data-stu-id="bca7f-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="bca7f-104">Můžete zkontrolovat dostupnost zdrojů, chcete-li získat celkový přehled o tom, jak jsou zdroje rezervovány, nebo můžete filtrovat zobrazení podle dovedností, týmu, umístění a dalších možností.</span><span class="sxs-lookup"><span data-stu-id="bca7f-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="bca7f-105">Plánovací vývěska zobrazuje seznam zdrojů a jejich dostupnost.</span><span class="sxs-lookup"><span data-stu-id="bca7f-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="bca7f-106">Vyberte režim zobrazení pro zobrazení dostupnosti podle **Hodin** , **Dne** , **Týdne** nebo **Měsíce**.</span><span class="sxs-lookup"><span data-stu-id="bca7f-106">Select a view mode to show availability by **Hours** , **Day** , **Week** , or **Month**.</span></span>  
  
<span data-ttu-id="bca7f-107">Před použitím plánovací vývěsky je třeba ji nastavit.</span><span class="sxs-lookup"><span data-stu-id="bca7f-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="bca7f-108">Další informace naleznete v tématu [Konfigurace plánovací vývěsky (Field Service nebo Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="bca7f-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="bca7f-109">Pokud používáte starší verzi, naleznete informace o dostupnosti zdrojů v části [Zobrazení dostupnosti zdrojů](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="bca7f-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="bca7f-110">Abyste mohli používat funkci rezervace plánovací vývěsky, geografické kódování a služby zjišťování polohy, je třeba zapnout mapy.</span><span class="sxs-lookup"><span data-stu-id="bca7f-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="bca7f-111">V hlavní nabídce vyberte **Plánování zdrojů** > **Správa**.</span><span class="sxs-lookup"><span data-stu-id="bca7f-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="bca7f-112">Klikněte na **Parametry plánování**.</span><span class="sxs-lookup"><span data-stu-id="bca7f-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="bca7f-113">Otevřete záznam a přejděte dolů do části **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="bca7f-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="bca7f-114">V poli **Připojit k mapám** vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="bca7f-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="bca7f-115">Přijměte podmínky a uložte záznam.</span><span class="sxs-lookup"><span data-stu-id="bca7f-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="bca7f-116">V hlavní nabídce vyberte **Project Service** > **Plánovací vývěska**.</span><span class="sxs-lookup"><span data-stu-id="bca7f-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="bca7f-117">Požadavek na rezervaci odsud lze ručně naplánovat několika způsoby.</span><span class="sxs-lookup"><span data-stu-id="bca7f-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="bca7f-118">Zvolte metodu, která u vás funguje.</span><span class="sxs-lookup"><span data-stu-id="bca7f-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="bca7f-119">Nalezení dostupných zdrojů</span><span class="sxs-lookup"><span data-stu-id="bca7f-119">Find available resources</span></span>

1.  <span data-ttu-id="bca7f-120">V seznamu **Požadavek na rezervaci** klikněte pravým tlačítkem myši na nenaplánovanou rezervaci a vyberte některou z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="bca7f-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="bca7f-121">Zvolte **Najít dostupnost – aktuální zdroje** pro vyhledání dostupného zdroje ze seznamu na plánovací vývěsce.</span><span class="sxs-lookup"><span data-stu-id="bca7f-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="bca7f-122">Zvolte **Najít dostupnost – všechny zdroje** pro vyhledání dostupného zdroje ze zdrojů v systému.</span><span class="sxs-lookup"><span data-stu-id="bca7f-122">Choose **Find availability - All Resources** , to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="bca7f-123">Následně filtry zobrazí možnosti pro vybraný požadavek na rezervaci.</span><span class="sxs-lookup"><span data-stu-id="bca7f-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="bca7f-124">Pokud vidíte volnou pozici, klikněte pravým tlačítkem myši na časový úsek na plánovací vývěsce a zvolte **Rezervovat zde**.</span><span class="sxs-lookup"><span data-stu-id="bca7f-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="bca7f-125">Nebo přetáhněte požadavek na rezervaci na dostupný časový úsek.</span><span class="sxs-lookup"><span data-stu-id="bca7f-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="bca7f-126">Rezervování zdroje pomocí denního zobrazení a vyhledání málo rezervovaných zdrojů</span><span class="sxs-lookup"><span data-stu-id="bca7f-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="bca7f-127">Na plánovací vývěsce zvolte **Režim zobrazení** a vyberte **Dny**.</span><span class="sxs-lookup"><span data-stu-id="bca7f-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="bca7f-128">Bude k dispozici zobrazení mřížky uvádějící, kolik hodin denně je zdroj rezervován a které dny je volný.</span><span class="sxs-lookup"><span data-stu-id="bca7f-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="bca7f-129">Klikněte na jméno zdroje, který chcete rezervovat, a potom zvolte **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="bca7f-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="bca7f-130">V dialogovém okně **Rezervace zdrojů (vytvoření)** zvolte projekt, pro který chcete daný zdroj rezervovat, a také způsob rezervace a počáteční a koncový čas.</span><span class="sxs-lookup"><span data-stu-id="bca7f-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="bca7f-131">Až budete hotovi, vyberte **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="bca7f-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="bca7f-132">Zobrazit na plánovací vývěsce</span><span class="sxs-lookup"><span data-stu-id="bca7f-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="bca7f-133">Vyberte neplánovaný požadavek na rezervaci ze seznamu ve spodní části.</span><span class="sxs-lookup"><span data-stu-id="bca7f-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="bca7f-134">Přetáhněte požadavek na rezervaci na dostupnou pozici zdroje/času na plánovací vývěsce.</span><span class="sxs-lookup"><span data-stu-id="bca7f-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="bca7f-135">Až budete hotovi, vyberte **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="bca7f-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="bca7f-136">Další materiály</span><span class="sxs-lookup"><span data-stu-id="bca7f-136">Additional resources</span></span>  
 [<span data-ttu-id="bca7f-137">Příručka pro manažera zdrojů</span><span class="sxs-lookup"><span data-stu-id="bca7f-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)