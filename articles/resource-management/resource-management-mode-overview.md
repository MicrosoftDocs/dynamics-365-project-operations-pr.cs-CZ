---
title: Přehled režimů správy zdrojů
description: Toto téma poskytuje informace o funkci Správa zdrojů v Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073668"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="d458d-103">Přehled režimů správy zdrojů</span><span class="sxs-lookup"><span data-stu-id="d458d-103">Resource management modes overview</span></span>

<span data-ttu-id="d458d-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="d458d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d458d-105">Dynamics 365 Project Operations podporuje dva režimy provádění celkového toku rezervací.</span><span class="sxs-lookup"><span data-stu-id="d458d-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="d458d-106">Režim správy je definován jako parametr projektu a lze jej upravit, pokud se změní vaše obchodní potřeby.</span><span class="sxs-lookup"><span data-stu-id="d458d-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="d458d-107">Centrální režim</span><span class="sxs-lookup"><span data-stu-id="d458d-107">Central mode</span></span>
<span data-ttu-id="d458d-108">Organizacím, které centralizují přidělení zdrojů k projektům, poskytuje centrální režim způsob, jak zajistit, aby projektoví manažeři mohli definovat požadavky na zdroje na úrovni projektu.</span><span class="sxs-lookup"><span data-stu-id="d458d-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="d458d-109">Splnění požadavků na zdroje je delegováno na správce zdrojů.</span><span class="sxs-lookup"><span data-stu-id="d458d-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="d458d-110">Manažeři projektů mohou přijímat nebo odmítat zdroje, které navrhuje správce zdrojů.</span><span class="sxs-lookup"><span data-stu-id="d458d-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Centrální režim](./media/resource-management-central.png)

<span data-ttu-id="d458d-112">Chcete-li spravovat zdroje v centrálním režimu, přečtěte si:</span><span class="sxs-lookup"><span data-stu-id="d458d-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="d458d-113">Přiřazení obecných rezervovatelných zdrojů k úkolu a vygenerování požadavků na zdroj</span><span class="sxs-lookup"><span data-stu-id="d458d-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="d458d-114">Rezervace pojmenovaných zdrojů z požadavků na zdroje</span><span class="sxs-lookup"><span data-stu-id="d458d-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="d458d-115">Odeslání žádosti o zdroj</span><span class="sxs-lookup"><span data-stu-id="d458d-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="d458d-116">Splnění požadavku na zdroj</span><span class="sxs-lookup"><span data-stu-id="d458d-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="d458d-117">Přijetí nebo zamítnutí navrženého zdroje projektu z žádosti o zdroj</span><span class="sxs-lookup"><span data-stu-id="d458d-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="d458d-118">Hybridní režim</span><span class="sxs-lookup"><span data-stu-id="d458d-118">Hybrid mode</span></span>
<span data-ttu-id="d458d-119">U organizací, které vyžadují při přidělování zdrojů flexibilitu, umožňuje hybridní režim projektovým manažerům i správcům zdrojů rezervovat prostředky.</span><span class="sxs-lookup"><span data-stu-id="d458d-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hybridní režim](./media/resource-management-hybrid.png)

<span data-ttu-id="d458d-121">Kromě podporovaného procesu v centrálním režimu najdete v následujících tématech přehled správy všech ostatních podporovaných toků rezervací v hybridním režimu:</span><span class="sxs-lookup"><span data-stu-id="d458d-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="d458d-122">Rezervace zdroje přímo k projektu:</span><span class="sxs-lookup"><span data-stu-id="d458d-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="d458d-123">Rezervujte pro projektový tým pojmenované rezervovatelné zdroje a přiřaďte úkoly</span><span class="sxs-lookup"><span data-stu-id="d458d-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="d458d-124">Rezervace zdroje z požadavku na zdroj:</span><span class="sxs-lookup"><span data-stu-id="d458d-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="d458d-125">Přiřazení obecných rezervovatelných zdrojů k úkolu a vygenerování požadavků na zdroj</span><span class="sxs-lookup"><span data-stu-id="d458d-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="d458d-126">Rezervace pojmenovaných zdrojů z požadavků na zdroje</span><span class="sxs-lookup"><span data-stu-id="d458d-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
