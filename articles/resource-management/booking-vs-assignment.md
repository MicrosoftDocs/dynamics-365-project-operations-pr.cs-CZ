---
title: Rezervace a přiřazení
description: Toto téma poskytuje informace o rozdílech mezi rezervacemi zdrojů a přiřazeními zdrojů.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130210"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="e7f13-103">Rezervace a přiřazení</span><span class="sxs-lookup"><span data-stu-id="e7f13-103">Bookings vs assignments</span></span>

<span data-ttu-id="e7f13-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="e7f13-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e7f13-105">Rezervace jsou závazné nebo předběžné přidělení zdrojů k projektu.</span><span class="sxs-lookup"><span data-stu-id="e7f13-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="e7f13-106">Závazné rezervace spotřebovávají kapacitu zdroje.</span><span class="sxs-lookup"><span data-stu-id="e7f13-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="e7f13-107">Rezervace představují organizační koncepty pro týmy, aby mohly pochopit, jak budou zdroje zapojeny do různých projektů.</span><span class="sxs-lookup"><span data-stu-id="e7f13-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="e7f13-108">Dynamics 365 Project Operations považuje rezervace za koncept na úrovni projektu.</span><span class="sxs-lookup"><span data-stu-id="e7f13-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="e7f13-109">Na rozdíl od rezervací představuje přiřazení závazek zdrojů k úkolům projektu v plánu projektu.</span><span class="sxs-lookup"><span data-stu-id="e7f13-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="e7f13-110">Zdroje mohou být pojmenované nebo obecné.</span><span class="sxs-lookup"><span data-stu-id="e7f13-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="e7f13-111">Součet rezervací pro zdroj se obvykle bude rovnat součtu přiřazení zdroje napříč jedním nebo více úkoly.</span><span class="sxs-lookup"><span data-stu-id="e7f13-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="e7f13-112">Project Operations však tuto dohodu nevynucuje.</span><span class="sxs-lookup"><span data-stu-id="e7f13-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="e7f13-113">Zobrazení **Vyrovnání** ukazuje projektovému manažerovi místa, kde se neshodují rezervace a přiřazení zdroje.</span><span class="sxs-lookup"><span data-stu-id="e7f13-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
