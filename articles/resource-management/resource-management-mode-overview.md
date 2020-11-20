---
title: Přehled režimů správy zdrojů
description: Toto téma poskytuje informace o funkci Správa zdrojů v Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118510"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="87f5e-103">Přehled režimů správy zdrojů</span><span class="sxs-lookup"><span data-stu-id="87f5e-103">Resource management modes overview</span></span>

<span data-ttu-id="87f5e-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="87f5e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="87f5e-105">Dynamics 365 Project Operations podporuje dva režimy provádění celkového toku rezervací.</span><span class="sxs-lookup"><span data-stu-id="87f5e-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="87f5e-106">Režim správy je definován jako parametr projektu a lze jej upravit, pokud se změní vaše obchodní potřeby.</span><span class="sxs-lookup"><span data-stu-id="87f5e-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="87f5e-107">Centrální režim</span><span class="sxs-lookup"><span data-stu-id="87f5e-107">Central mode</span></span>
<span data-ttu-id="87f5e-108">Organizacím, které centralizují přidělení zdrojů k projektům, poskytuje centrální režim způsob, jak zajistit, aby projektoví manažeři mohli definovat požadavky na zdroje na úrovni projektu.</span><span class="sxs-lookup"><span data-stu-id="87f5e-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="87f5e-109">Splnění požadavků na zdroje je delegováno na správce zdrojů.</span><span class="sxs-lookup"><span data-stu-id="87f5e-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="87f5e-110">Manažeři projektů mohou přijímat nebo odmítat zdroje, které navrhuje správce zdrojů.</span><span class="sxs-lookup"><span data-stu-id="87f5e-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Centrální režim](./media/resource-management-central.png)

<span data-ttu-id="87f5e-112">Chcete-li spravovat zdroje v centrálním režimu, přečtěte si:</span><span class="sxs-lookup"><span data-stu-id="87f5e-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="87f5e-113">Přiřazení obecných rezervovatelných zdrojů k úkolu a vygenerování požadavků na zdroj</span><span class="sxs-lookup"><span data-stu-id="87f5e-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="87f5e-114">Rezervace pojmenovaných zdrojů z požadavků na zdroje</span><span class="sxs-lookup"><span data-stu-id="87f5e-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="87f5e-115">Odeslání žádosti o zdroj</span><span class="sxs-lookup"><span data-stu-id="87f5e-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="87f5e-116">Splnění požadavku na zdroj</span><span class="sxs-lookup"><span data-stu-id="87f5e-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="87f5e-117">Přijetí nebo zamítnutí navrženého zdroje projektu z žádosti o zdroj</span><span class="sxs-lookup"><span data-stu-id="87f5e-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="87f5e-118">Hybridní režim</span><span class="sxs-lookup"><span data-stu-id="87f5e-118">Hybrid mode</span></span>
<span data-ttu-id="87f5e-119">U organizací, které vyžadují při přidělování zdrojů flexibilitu, umožňuje hybridní režim projektovým manažerům i správcům zdrojů rezervovat prostředky.</span><span class="sxs-lookup"><span data-stu-id="87f5e-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hybridní režim](./media/resource-management-hybrid.png)

<span data-ttu-id="87f5e-121">Kromě podporovaného procesu v centrálním režimu najdete v následujících tématech přehled správy všech ostatních podporovaných toků rezervací v hybridním režimu:</span><span class="sxs-lookup"><span data-stu-id="87f5e-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="87f5e-122">Rezervace zdroje přímo k projektu:</span><span class="sxs-lookup"><span data-stu-id="87f5e-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="87f5e-123">Rezervujte pro projektový tým pojmenované rezervovatelné zdroje a přiřaďte úkoly</span><span class="sxs-lookup"><span data-stu-id="87f5e-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="87f5e-124">Rezervace zdroje z požadavku na zdroj:</span><span class="sxs-lookup"><span data-stu-id="87f5e-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="87f5e-125">Přiřazení obecných rezervovatelných zdrojů k úkolu a vygenerování požadavků na zdroj</span><span class="sxs-lookup"><span data-stu-id="87f5e-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="87f5e-126">Rezervace pojmenovaných zdrojů z požadavků na zdroje</span><span class="sxs-lookup"><span data-stu-id="87f5e-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
