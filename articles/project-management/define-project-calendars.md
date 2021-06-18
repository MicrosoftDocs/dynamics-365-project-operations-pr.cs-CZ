---
title: Definování kalendářů projektů
description: Tento téma poskytuje informace o tom, jak použít šablonu kalendáře na projekt ke sledování harmonogramu projektu.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998988"
---
# <a name="define-project-calendars"></a><span data-ttu-id="84f53-103">Definování kalendářů projektů</span><span class="sxs-lookup"><span data-stu-id="84f53-103">Define project calendars</span></span>

<span data-ttu-id="84f53-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="84f53-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="84f53-105">Chcete-li vytvořit a spravovat projekt, musíte na projekt použít šablonu kalendáře.</span><span class="sxs-lookup"><span data-stu-id="84f53-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="84f53-106">Šablona kalendáře definuje následující atributy projektu:</span><span class="sxs-lookup"><span data-stu-id="84f53-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="84f53-107">Pracovní doba, včetně času zahájení a ukončení</span><span class="sxs-lookup"><span data-stu-id="84f53-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="84f53-108">Pracovní dny</span><span class="sxs-lookup"><span data-stu-id="84f53-108">Working days</span></span>
- <span data-ttu-id="84f53-109">Výjimky v kalendáři, například nepracovní dny</span><span class="sxs-lookup"><span data-stu-id="84f53-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="84f53-110">Šablona kalendáře, která se použije na projekt, je kopií šablony kalendáře definované v nastavení vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="84f53-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="84f53-111">Pokud změníte šablonu kalendáře, tyto změny se nebudou šířit do pracovní doby projektu.</span><span class="sxs-lookup"><span data-stu-id="84f53-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="84f53-112">Chcete-li změnit pracovní dobu projektu, je nutné použít novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="84f53-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="84f53-113">K vytvoření šablony kalendáře pro vaši organizaci existují dva klíčové požadavky:</span><span class="sxs-lookup"><span data-stu-id="84f53-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="84f53-114">Definujte požadovanou pracovní dobu šablony pomocí nového nebo existujícího rezervovatelného zdroje.</span><span class="sxs-lookup"><span data-stu-id="84f53-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="84f53-115">Vytvořte novou šablonu kalendáře a přidružte ji k rezervovatelnému prostředku.</span><span class="sxs-lookup"><span data-stu-id="84f53-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="84f53-116">**Definujte pracovní dobu šablony**</span><span class="sxs-lookup"><span data-stu-id="84f53-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="84f53-117">Přejděte na **Zdroje** \> **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="84f53-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="84f53-118">Vytvořte nový prostředek, který bude odkazovat v šabloně kalendáře, nebo vyberte existující prostředek.</span><span class="sxs-lookup"><span data-stu-id="84f53-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="84f53-119">Vyberte kartu **Pracovní doba** zdroje a postupujte podle pokynů v části [Nastavení pracovní doby zdroje](/dynamics365/field-service/set-work-hours-resource.md) ke konfiguraci pravidel kalendáře.</span><span class="sxs-lookup"><span data-stu-id="84f53-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="84f53-120">**Vytvořit novou šablonu kalendáře**</span><span class="sxs-lookup"><span data-stu-id="84f53-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="84f53-121">Přejděte na **Nastavení** \> **Šablona kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="84f53-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="84f53-122">Vyberte **Nový** a zadejte název, popis a prostředek šablony.</span><span class="sxs-lookup"><span data-stu-id="84f53-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="84f53-123">Když je prostředek odkazován v šabloně kalendáře, je kopie kalendáře prostředku přidružena k šabloně kalendáře.</span><span class="sxs-lookup"><span data-stu-id="84f53-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="84f53-124">Pokud se změní pracovní doba kopírované šablony, tyto změny se nebudou šířit do šablony kalendáře.</span><span class="sxs-lookup"><span data-stu-id="84f53-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="84f53-125">Nyní můžete šablonu práce přidružit k šabloně kalendáře projektu.</span><span class="sxs-lookup"><span data-stu-id="84f53-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

