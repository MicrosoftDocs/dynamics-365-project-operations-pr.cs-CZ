---
title: Vytvoření šablony pracovní doby
description: Postup vytvoření šablony pracovní doby v Project Service
author: ruhercul
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
ms.openlocfilehash: c34634817fc8e4c993261024a8b19d45052bf5e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073790"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="1fd46-103">Vytvoření šablony pracovní doby (Project Service)</span><span class="sxs-lookup"><span data-stu-id="1fd46-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="1fd46-104">Před vytvořením plánů projektu je třeba nastavit kalendář projektu, který definuje počet pracovních hodin denně v plánu a všechny zavírací dny.</span><span class="sxs-lookup"><span data-stu-id="1fd46-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="1fd46-105">Provedete to pomocí šablony pracovní doby, která obsahuje podrobnosti o počtu pracovních hodin za den, dnech volna a jiných zavíracích dnech.</span><span class="sxs-lookup"><span data-stu-id="1fd46-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="1fd46-106">Při vytváření projektu přiřadíte šablonu ke kalendáři projektu a použijete plán pro projekt.</span><span class="sxs-lookup"><span data-stu-id="1fd46-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="1fd46-107">Šablony pracovních hodin můžete vytvořit dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="1fd46-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="1fd46-108">Vytvořte šablonu pracovní doby na základě kalendáře zdroje.</span><span class="sxs-lookup"><span data-stu-id="1fd46-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="1fd46-109">Vytvořte novou šablonu pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="1fd46-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="1fd46-110">Vytvoření šablony pracovní doby na základě kalendáře zdroje</span><span class="sxs-lookup"><span data-stu-id="1fd46-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="1fd46-111">Přejděte do nabídky **Project Service > Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="1fd46-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="1fd46-112">Vyberte zdroj, na kterém chcete založit svou pracovní dobu.</span><span class="sxs-lookup"><span data-stu-id="1fd46-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="1fd46-113">Klikněte na tlačítko **Uložit kalendář jako** , zadejte název šablony pracovní doby a potom klikněte na tlačítko **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="1fd46-113">Click **Save Calendar As** , enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="1fd46-114">Po dokončení úprav možností klikněte na tlačítko **Uložit a zavřít**.</span><span class="sxs-lookup"><span data-stu-id="1fd46-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="1fd46-115">Klikněte na tlačítko **Uložit** v pravém dolním rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="1fd46-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="1fd46-116">Vytvoření nové šablony pracovní doby</span><span class="sxs-lookup"><span data-stu-id="1fd46-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="1fd46-117">Přejděte do nabídky **Project Service > Šablona pracovní doby**.</span><span class="sxs-lookup"><span data-stu-id="1fd46-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="1fd46-118">Klikněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="1fd46-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="1fd46-119">Zadejte název šablony pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="1fd46-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="1fd46-120">Vyberte zdroj, na kterém chcete pracovní dobu založit, a klikněte na tlačítko **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="1fd46-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="1fd46-121">Viz také</span><span class="sxs-lookup"><span data-stu-id="1fd46-121">See Also</span></span>  
 [<span data-ttu-id="1fd46-122">Nastavení zdrojů</span><span class="sxs-lookup"><span data-stu-id="1fd46-122">Set up resources</span></span>](../psa/set-up-resources.md)