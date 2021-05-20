---
title: Vytvoření šablony pracovní doby
description: Toto téma popisuje postup vytvoření šablony pracovní doby v Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981247"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="dc608-103">Vytvoření šablony pracovní doby (Project Service)</span><span class="sxs-lookup"><span data-stu-id="dc608-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="dc608-104">Chcete-li vytvořit a spravovat projekt, musíte na projekt použít šablonu kalendáře.</span><span class="sxs-lookup"><span data-stu-id="dc608-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="dc608-105">Šablona kalendáře definuje následující atributy projektu:</span><span class="sxs-lookup"><span data-stu-id="dc608-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="dc608-106">Pracovní doba, včetně času zahájení a ukončení</span><span class="sxs-lookup"><span data-stu-id="dc608-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="dc608-107">Pracovní dny</span><span class="sxs-lookup"><span data-stu-id="dc608-107">Working days</span></span>
- <span data-ttu-id="dc608-108">Výjimky v kalendáři, například nepracovní dny</span><span class="sxs-lookup"><span data-stu-id="dc608-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="dc608-109">Šablona kalendáře, která se použije na projekt, je kopií šablony kalendáře definované v nastavení vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="dc608-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="dc608-110">Pokud změníte šablonu kalendáře, tyto změny se nebudou šířit do pracovní doby projektu.</span><span class="sxs-lookup"><span data-stu-id="dc608-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="dc608-111">Chcete-li změnit pracovní dobu projektu, je nutné použít novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="dc608-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="dc608-112">K vytvoření šablony kalendáře pro vaši organizaci existují dva klíčové požadavky:</span><span class="sxs-lookup"><span data-stu-id="dc608-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="dc608-113">Definujte požadovanou pracovní dobu šablony pomocí nového nebo existujícího rezervovatelného zdroje.</span><span class="sxs-lookup"><span data-stu-id="dc608-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="dc608-114">Vytvořte novou šablonu kalendáře a přidružte ji k rezervovatelnému prostředku.</span><span class="sxs-lookup"><span data-stu-id="dc608-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="dc608-115">**Definujte pracovní dobu šablony**</span><span class="sxs-lookup"><span data-stu-id="dc608-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="dc608-116">Přejděte na **Zdroje** \> **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="dc608-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="dc608-117">Vytvořte nový prostředek, který bude odkazovat v šabloně kalendáře, nebo vyberte existující prostředek.</span><span class="sxs-lookup"><span data-stu-id="dc608-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="dc608-118">Vyberte kartu **Pracovní doba** zdroje a postupujte podle pokynů v části [Nastavení pracovní doby zdroje](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) ke konfiguraci pravidel kalendáře.</span><span class="sxs-lookup"><span data-stu-id="dc608-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="dc608-119">**Vytvořit novou šablonu kalendáře**</span><span class="sxs-lookup"><span data-stu-id="dc608-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="dc608-120">Přejděte na **Nastavení** \> **Šablona kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="dc608-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="dc608-121">Vyberte **Nový** a zadejte název, popis a prostředek šablony.</span><span class="sxs-lookup"><span data-stu-id="dc608-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="dc608-122">Když je prostředek odkazován v šabloně kalendáře, je kopie kalendáře prostředku přidružena k šabloně kalendáře.</span><span class="sxs-lookup"><span data-stu-id="dc608-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="dc608-123">Pokud se změní pracovní doba kopírované šablony, tyto změny se nebudou šířit do šablony kalendáře.</span><span class="sxs-lookup"><span data-stu-id="dc608-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="dc608-124">Viz také</span><span class="sxs-lookup"><span data-stu-id="dc608-124">See Also</span></span>  
 [<span data-ttu-id="dc608-125">Nastavení zdrojů</span><span class="sxs-lookup"><span data-stu-id="dc608-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
