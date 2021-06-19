---
title: Přiřaďte k úkolu a projektovému týmu obecné rezervovatelné zdroje
description: Toto téma obsahuje informace o rezervaci obecných zdrojů pro úkoly a projektové týmy.
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
ms.openlocfilehash: a1e22337d3fd3e7ff4147a9547fd3c272f4185d3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009383"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="6578c-103">Přiřaďte k úkolu obecný rezervovatelný zdroj a vygenerujte požadavky na zdroj</span><span class="sxs-lookup"><span data-stu-id="6578c-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6578c-104">Kromě rezervace a přiřazování pojmenovaných nebo skutečných zdrojů pro váš projekt můžete k projektovým úkolům přiřadit obecné zdroje.</span><span class="sxs-lookup"><span data-stu-id="6578c-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="6578c-105">Tyto zdroje mohou sloužit jako zástupné symboly pro pojmenované zdroje, dokud nebudete připraveni k obsazení vašeho projektu pojmenovanými zdroji.</span><span class="sxs-lookup"><span data-stu-id="6578c-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="6578c-106">V Project Service Automation (PSA) otevřete stránku **Projekt** a na kartě **Plán** zadejte do buňky plánu **Zdroj** název pozice obecného zdroje.</span><span class="sxs-lookup"><span data-stu-id="6578c-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="6578c-107">Nebo klepnutím na ikonu **Zdroje** v buňce otevřete okno pro výběr zdroje a zadejte název obecného zdroje, který chcete vytvořit.</span><span class="sxs-lookup"><span data-stu-id="6578c-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Vytvoření a přiřazení obecného člena týmu](media/RM-how-to-9.png)

<span data-ttu-id="6578c-109">Otevře se panel **Vytvořit: Člen projektového týmu**.</span><span class="sxs-lookup"><span data-stu-id="6578c-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="6578c-110">Zadejte roli a organizační jednotku obecného zdroje člena týmu a pak klepněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="6578c-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Vytvoření obecného člena týmu](media/RM-how-to-10.png)

3. <span data-ttu-id="6578c-112">Poté, co jste vytvořili nový obecný zdroj člena týmu, je přiřazen k úkolu.</span><span class="sxs-lookup"><span data-stu-id="6578c-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="6578c-113">Tento obecný zdroj můžete dále přiřadit k dalším úkolům v plánu úkolů.</span><span class="sxs-lookup"><span data-stu-id="6578c-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Přiřazení existujícího obecného člena týmu k úkolům](media/RM-how-to-11.png)

4. <span data-ttu-id="6578c-115">Po přiřazení obecného zdroje můžete vygenerovat požadavek na zdroj a splnit ji přímou rezervací nebo odesláním žádosti o zdroj správci zdrojů.</span><span class="sxs-lookup"><span data-stu-id="6578c-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Generování požadavku na obecného člena týmu](media/RM-how-to-12.png)

<span data-ttu-id="6578c-117">V mřížce člena týmu můžete kromě toho, že budete moci použít výběr zdroje výše uvedeným způsobem, přidat obecné zdroje přímo.</span><span class="sxs-lookup"><span data-stu-id="6578c-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="6578c-118">Zdroje jsou přidávány prostřednictvím požadavku na zdroj, který je založen na počátečních a koncových datech a metodě přidělení určené v panelu **Vytvořit: Člen projektového týmu**.</span><span class="sxs-lookup"><span data-stu-id="6578c-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="6578c-119">Rozdíl můžete vidět, pokud přidáte obecného člena týmu přímo a potom k tomuto obecnému zdroji přiřadíte více úkolů, než je počet hodin potřebný k pokrytí.</span><span class="sxs-lookup"><span data-stu-id="6578c-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="6578c-120">Chcete-li vygenerovat požadavek na vyrovnání požadovaných hodin oproti přiřazením, klikněte na **Generovat požadavek**.</span><span class="sxs-lookup"><span data-stu-id="6578c-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="6578c-121">Můžete také kliknout na odkaz **Požadavek na zdroj** v mřížce týmu a tím otevřít požadavek a přidat dovednosti, upřednostňované zdroje atd.</span><span class="sxs-lookup"><span data-stu-id="6578c-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Požadavek na zdroj](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]