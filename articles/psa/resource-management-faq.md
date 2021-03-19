---
title: Nejčastější dotazy ke správě zdrojů
description: Toto téma poskytuje odpovědi na časté otázky týkající se správy zdrojů.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 20562b98ccc8451ab57dd42fb8c2f9f303811dbe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283135"
---
# <a name="resource-management-faq"></a><span data-ttu-id="a1506-103">Nejčastější dotazy ke správě zdrojů</span><span class="sxs-lookup"><span data-stu-id="a1506-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="a1506-104">Jaký je rozdíl mezi členem týmu a požadavkem na zdroj?</span><span class="sxs-lookup"><span data-stu-id="a1506-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="a1506-105">Člena projektového týmu lze přiřadit k úkolům, rezervovat nebo přerezervovat a nastavit jako schvalovatele.</span><span class="sxs-lookup"><span data-stu-id="a1506-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="a1506-106">Požadavek na zdroj může existovat bez člena projektového týmu jako koncept poznámky k poptávce.</span><span class="sxs-lookup"><span data-stu-id="a1506-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="a1506-107">Jaký je rozdíl mezi navrženými a předběžně rezervovanými hodinami?</span><span class="sxs-lookup"><span data-stu-id="a1506-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="a1506-108">Navržené hodiny a předběžně rezervované hodiny se liší viditelností.</span><span class="sxs-lookup"><span data-stu-id="a1506-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="a1506-109">Navržené hodiny jsou viditelné pouze správcům zdrojů a projektovému manažerovi, který poptávku inicioval pomocí žádosti o zdroj.</span><span class="sxs-lookup"><span data-stu-id="a1506-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="a1506-110">Předběžně rezervované hodiny jsou viditelné všem uživatelům, kteří mají přístup k Plánovací vývěsce.</span><span class="sxs-lookup"><span data-stu-id="a1506-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="a1506-111">Jak lze zobrazit předběžně rezervované hodiny pro zdroje v týmu?</span><span class="sxs-lookup"><span data-stu-id="a1506-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="a1506-112">Předběžné rezervace lze provést při rezervaci požadavku na zdroj.</span><span class="sxs-lookup"><span data-stu-id="a1506-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="a1506-113">Zdroje, které jsou v projektovém týmu předběžně rezervované, se zobrazí jako členové týmu, kteří mají předběžně rezervované hodiny.</span><span class="sxs-lookup"><span data-stu-id="a1506-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="a1506-114">Zobrazí se také v Plánovací vývěsce.</span><span class="sxs-lookup"><span data-stu-id="a1506-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="a1506-115">Jak změnit požadované hodiny a počáteční a koncová data pro zdroj (obecný nebo pojmenovaný), který jsem rezervoval?</span><span class="sxs-lookup"><span data-stu-id="a1506-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="a1506-116">Chcete-li provést libovolné požadované změny vyberte po rezervaci zdrojů vyberte **Spravovat rezervace**.</span><span class="sxs-lookup"><span data-stu-id="a1506-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="a1506-117">Jaké typy zdrojů podporuje Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="a1506-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="a1506-118">**Uživatel** a **Kontakt** jsou jediné typy zdrojů podporované v Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a1506-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="a1506-119">I když můžete vytvářet další typy zdrojů (například **Vybavení** a **Skupina**), není pro ně podporován žádný případ komplexního použití.</span><span class="sxs-lookup"><span data-stu-id="a1506-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="a1506-120">Jaký je rozdíl mezi přiřazením a rezervací?</span><span class="sxs-lookup"><span data-stu-id="a1506-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="a1506-121">Přiřazení jsou přiřazení zdrojů k úkolům projektu v plánu projektu.</span><span class="sxs-lookup"><span data-stu-id="a1506-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="a1506-122">Zdroje mohou být buď skutečné, nebo obecné.</span><span class="sxs-lookup"><span data-stu-id="a1506-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="a1506-123">Rezervace jsou závazné nebo předběžné přidělení zdrojů k projektu.</span><span class="sxs-lookup"><span data-stu-id="a1506-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="a1506-124">Závazné rezervace spotřebovávají kapacitu zdroje.</span><span class="sxs-lookup"><span data-stu-id="a1506-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="a1506-125">V ideálním případě by se pro reálné zdroje měly dohodnout rezervace a přiřazení, protože se neliší.</span><span class="sxs-lookup"><span data-stu-id="a1506-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="a1506-126">PSA však tuto dohodu nevynucuje.</span><span class="sxs-lookup"><span data-stu-id="a1506-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="a1506-127">Zobrazení Vyrovnání ukazuje projektovému manažerovi místa, kde se neshodují rezervace a přiřazení zdroje.</span><span class="sxs-lookup"><span data-stu-id="a1506-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]