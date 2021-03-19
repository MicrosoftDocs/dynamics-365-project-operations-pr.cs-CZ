---
title: Příručka pro manažera zdrojů
description: Příručka k řízení zdrojů v Project Service
author: JohnPBurrows
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
ms.openlocfilehash: 4b9df18e7240450f01271b73eb6ea7e215be38c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282820"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="05897-103">Příručka manažera zdrojů (Project Service)</span><span class="sxs-lookup"><span data-stu-id="05897-103">Resource manager guide (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="05897-104">Funkce [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v aplikaci [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] vám pomáhají nalézt správné zdroje v pravý čas pro správný projekt a přesvědčit se, zda jsou všechny zdroje efektivně využity.</span><span class="sxs-lookup"><span data-stu-id="05897-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="05897-105">Účinně a efektivně nasazujte konzultanty společnosti pomocí [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="05897-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="05897-106">Ty poskytují nástroje, které potřebujete k plánování zdrojů na základě požadavků a plánů konzultačních projektů a na základě dovedností a dostupnosti vašich konzultantů.</span><span class="sxs-lookup"><span data-stu-id="05897-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="05897-107">Můžete rychle najít nejkvalifikovanější konzultanty, kteří jsou k dispozici pro práci na projektech, a můžete snadno vidět, jak je lépe naplánovat v průběhu jednotlivých projektů.</span><span class="sxs-lookup"><span data-stu-id="05897-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="05897-108">Plánování zdrojů vám pomůže s následujícím:</span><span class="sxs-lookup"><span data-stu-id="05897-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="05897-109">Párování zdrojů s projekty na základě toho, jak jejich úroveň dovedností a odborných znalostí vyhovuje žádostem o zdroje projektu.</span><span class="sxs-lookup"><span data-stu-id="05897-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="05897-110">Párování plánu zdrojů s kalendářem projektu na základě jejich dostupnosti a plánovaného volna.</span><span class="sxs-lookup"><span data-stu-id="05897-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="05897-111">Barevně označený kalendář poskytuje vizuální upozornění o dostupnosti zdrojů.</span><span class="sxs-lookup"><span data-stu-id="05897-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="05897-112">Kontrola kapacity všech konzultantů a určení, jak se tato kapacita aktuálně využívá.</span><span class="sxs-lookup"><span data-stu-id="05897-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="05897-113">To pomůže zjistit, kde je konzultant nedostatečně nebo naopak přespříliš využitý, nebo zda ideálně využívá kapacitu.</span><span class="sxs-lookup"><span data-stu-id="05897-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="05897-114">Přiřazení procentní části nebo určitého počtu hodin kapacity pracovníka projektu.</span><span class="sxs-lookup"><span data-stu-id="05897-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="05897-115">Rezervace prostředků skupiny.</span><span class="sxs-lookup"><span data-stu-id="05897-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="05897-116">Předběžná nebo závazná rezervace prostředků a převod předběžně rezervovaných hodin na závazně rezervované hodiny v jednom kroku.</span><span class="sxs-lookup"><span data-stu-id="05897-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="05897-117">Automatické vytvoření projektového týmu podle zdrojů definovaných ve strukturovaném rozpisu prací pro projekt.</span><span class="sxs-lookup"><span data-stu-id="05897-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="05897-118">Splnění žádostí o zdroje (rezervace, návrhy, hledání náhradních zdrojů).</span><span class="sxs-lookup"><span data-stu-id="05897-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="05897-119">Přiřazení zdrojů podle centrálního (přiřazuje správce zdrojů) nebo hybridního modelu (mohou přiřazovat správci zdrojů a ostatní správci).</span><span class="sxs-lookup"><span data-stu-id="05897-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="05897-120">Další informace o nastavení centrálního versus hybridního modelu správy zdrojů naleznete v tématu [Konfigurace nastavení dalších parametrů (Project Service)](../psa/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="05897-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="05897-121">Můžete efektivně spravovat zdroje v projektech a zajistit, že jsou projektům vhodně přiřazeny zdroje.</span><span class="sxs-lookup"><span data-stu-id="05897-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="05897-122">Budete muset provést následující úlohy:</span><span class="sxs-lookup"><span data-stu-id="05897-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="05897-123">[Správa žádostí o zdroje](../psa/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="05897-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="05897-124">Párovat schopnosti a odborné znalosti vašich konzultantů se pravými projekty.</span><span class="sxs-lookup"><span data-stu-id="05897-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="05897-125">[Zobrazení dostupnosti zdrojů](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="05897-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="05897-126">Kontrolovat dostupnost konzultantů v zobrazení kalendáře.</span><span class="sxs-lookup"><span data-stu-id="05897-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="05897-127">[Zobrazení využití zdrojů](../psa/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="05897-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="05897-128">Zobrazit procento času, kdy jsou vaši konzultanti aktuálně rezervováni.</span><span class="sxs-lookup"><span data-stu-id="05897-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="05897-129">[Plánování zdrojů pro projekt](../psa/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="05897-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="05897-130">Naplánovat konzultanty pro projekt.</span><span class="sxs-lookup"><span data-stu-id="05897-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="05897-131">Další informace o odesílání žádostí o zdroje pro jednotlivé projekty naleznete v části [Submit resource requests](../psa/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="05897-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="05897-132">Viz také</span><span class="sxs-lookup"><span data-stu-id="05897-132">See Also</span></span>  
 <span data-ttu-id="05897-133">[Přehled aplikace Project Service](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="05897-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="05897-134">[Příručka pro správce](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="05897-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="05897-135">[Příručka pro manažera obchodních vztahů](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="05897-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="05897-136">[Příručka pro projektového manažera](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="05897-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="05897-137">Příručka – Čas, výdaje a spolupráce</span><span class="sxs-lookup"><span data-stu-id="05897-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]