---
title: Rezervace a přiřazení
description: Toto téma poskytuje informace o rozdílech mezi rezervacemi zdrojů a přiřazeními zdrojů.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073629"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="28249-103">Rezervace a přiřazení</span><span class="sxs-lookup"><span data-stu-id="28249-103">Bookings vs assignments</span></span>

<span data-ttu-id="28249-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="28249-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="28249-105">Rezervace jsou závazné nebo předběžné přidělení zdrojů k projektu.</span><span class="sxs-lookup"><span data-stu-id="28249-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="28249-106">Závazné rezervace spotřebovávají kapacitu zdroje.</span><span class="sxs-lookup"><span data-stu-id="28249-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="28249-107">Přiřazení jsou přiřazení zdrojů k úkolům projektu v plánu projektu.</span><span class="sxs-lookup"><span data-stu-id="28249-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="28249-108">Zdroje mohou být buď skutečné, nebo obecné.</span><span class="sxs-lookup"><span data-stu-id="28249-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="28249-109">V ideálním případě by se pro reálné zdroje měly dohodnout rezervace a přiřazení, protože se neliší.</span><span class="sxs-lookup"><span data-stu-id="28249-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="28249-110">Microsoft Dynamics Project Operationsvšak tuto dohodu nevynucuje.</span><span class="sxs-lookup"><span data-stu-id="28249-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="28249-111">Zobrazení **Vyrovnání** ukazuje projektovému manažerovi místa, kde se neshodují rezervace a přiřazení zdroje.</span><span class="sxs-lookup"><span data-stu-id="28249-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
