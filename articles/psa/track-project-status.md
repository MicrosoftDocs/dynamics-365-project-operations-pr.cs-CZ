---
title: Sledování stavu projektu
description: Postup sledování stavu projektu v Project Service
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
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073866"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="b93a9-103">Sledování stavu projektu (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b93a9-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b93a9-104">[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] lze použít ke sledování průběhu projektu klienta.</span><span class="sxs-lookup"><span data-stu-id="b93a9-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="b93a9-105">V průběhu platnosti závazku se fáze projektu aktualizují tak, aby odrážely stupeň závazku:</span><span class="sxs-lookup"><span data-stu-id="b93a9-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="b93a9-106">**Nová**</span><span class="sxs-lookup"><span data-stu-id="b93a9-106">**New**</span></span>    | <span data-ttu-id="b93a9-107">Při vytváření projektu je fáze nastavena na **Nový**.</span><span class="sxs-lookup"><span data-stu-id="b93a9-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="b93a9-108">Pokud jste vytvořili projekt ze šablony, v této fázi může mít projekt plán, odhady a data týmu.</span><span class="sxs-lookup"><span data-stu-id="b93a9-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="b93a9-109">Jinak se bude jednat pouze o návrh projektu a bude třeba ručně zadat zbývající části projektu.</span><span class="sxs-lookup"><span data-stu-id="b93a9-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="b93a9-110">**Nabídka**</span><span class="sxs-lookup"><span data-stu-id="b93a9-110">**Quote**</span></span>   |      <span data-ttu-id="b93a9-111">Když přiřadíte projekt k nabídce nebo jej vytvoříte z nabídky, fáze projektu bude nastavena na možnost **Nabídka** a aktualizuje se také odhadované datum zahájení a ukončení.</span><span class="sxs-lookup"><span data-stu-id="b93a9-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote** , and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="b93a9-112">Pokud je projekt ve fázi nabídky, podrobnosti o nabídce se zobrazí na kartě **Prodej** na stránce **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="b93a9-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="b93a9-113">**Plán**</span><span class="sxs-lookup"><span data-stu-id="b93a9-113">**Plan**</span></span>   |                                     <span data-ttu-id="b93a9-114">Pokud vyhrajete nabídku spojenou s projektem a v průběhu platnosti závazku přejdete do fáze smlouvy, fáze projektu se aktualizuje na **Plán**.</span><span class="sxs-lookup"><span data-stu-id="b93a9-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="b93a9-115">Podrobnosti o smlouvě se zobrazí na kartě **Prodej** na stránce **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="b93a9-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="b93a9-116">**Dokončeno**</span><span class="sxs-lookup"><span data-stu-id="b93a9-116">**Complete**</span></span> |                    <span data-ttu-id="b93a9-117">Po dokončení práce na projektu můžete přepnout na fázi **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="b93a9-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="b93a9-118">Pokud je fáze projektu nastavena na možnost Dokončeno, práce je na 100 % ale dokončena, ale projekt zůstává otevřen, aby by mohla být zaznamenána doba čekání nebo položky výdajů.</span><span class="sxs-lookup"><span data-stu-id="b93a9-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="b93a9-119">**Zavřít**</span><span class="sxs-lookup"><span data-stu-id="b93a9-119">**Close**</span></span>   |           <span data-ttu-id="b93a9-120">Když jsou všechny transakce projektu zaznamenány a neočekáváte protokolování dalších, můžete ručně nastavit fázi na **Uzavřeno**.</span><span class="sxs-lookup"><span data-stu-id="b93a9-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="b93a9-121">Pokud je projekt nastaven na **Uzavřeno** , nelze protokolovat žádné další transakce projektu a projekt bude jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="b93a9-121">When the project is set to **Close** , you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="b93a9-122">Sledování stavu projektu</span><span class="sxs-lookup"><span data-stu-id="b93a9-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="b93a9-123">Přejděte do nabídky **Project Service > Projekty**.</span><span class="sxs-lookup"><span data-stu-id="b93a9-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="b93a9-124">Klepněte na projekt, na kterém chcete pracovat.</span><span class="sxs-lookup"><span data-stu-id="b93a9-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="b93a9-125">Na panelu v horní části obrazovky vyberte šipku dolů vedle názvu projektu a potom klikněte na možnost **Sledování projektu**.</span><span class="sxs-lookup"><span data-stu-id="b93a9-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="b93a9-126">Vyberte možnost **Sledování úsilí** nebo **Sledování nákladů** v rozevíracím seznamu nad seznam úkolů.</span><span class="sxs-lookup"><span data-stu-id="b93a9-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="b93a9-127">Dvakrát klikněte na kterýkoli úkol, který chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="b93a9-127">Double-click any task to edit it.</span></span> <span data-ttu-id="b93a9-128">Také můžete přesunout nebo změnit velikost pruhů v Ganttově diagramu, chcete-li změnit čas a průběh úkolu.</span><span class="sxs-lookup"><span data-stu-id="b93a9-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="b93a9-129">Viz také</span><span class="sxs-lookup"><span data-stu-id="b93a9-129">See Also</span></span>  
 [<span data-ttu-id="b93a9-130">Příručka pro projektového manažera</span><span class="sxs-lookup"><span data-stu-id="b93a9-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
