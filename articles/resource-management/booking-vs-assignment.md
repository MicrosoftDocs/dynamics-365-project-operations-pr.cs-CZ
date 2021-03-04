---
title: Rezervace a přiřazení
description: Toto téma poskytuje informace o rozdílech mezi rezervacemi zdrojů a přiřazeními zdrojů.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841164"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="7da2c-103">Rezervace a přiřazení</span><span class="sxs-lookup"><span data-stu-id="7da2c-103">Bookings vs assignments</span></span>

<span data-ttu-id="7da2c-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="7da2c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7da2c-105">Rezervace jsou závazné nebo předběžné přidělení zdrojů k projektu.</span><span class="sxs-lookup"><span data-stu-id="7da2c-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="7da2c-106">Závazné rezervace spotřebovávají kapacitu zdroje.</span><span class="sxs-lookup"><span data-stu-id="7da2c-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="7da2c-107">Rezervace představují organizační koncepty pro týmy, aby mohly pochopit, jak budou zdroje zapojeny do různých projektů.</span><span class="sxs-lookup"><span data-stu-id="7da2c-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="7da2c-108">Dynamics 365 Project Operations považuje rezervace za koncept na úrovni projektu.</span><span class="sxs-lookup"><span data-stu-id="7da2c-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="7da2c-109">Na rozdíl od rezervací představuje přiřazení závazek zdrojů k úkolům projektu v plánu projektu.</span><span class="sxs-lookup"><span data-stu-id="7da2c-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="7da2c-110">Zdroje mohou být pojmenované nebo obecné.</span><span class="sxs-lookup"><span data-stu-id="7da2c-110">The resources can be named or generic.</span></span>  <span data-ttu-id="7da2c-111">Když je požadavek na zdroj odvozen z přiřazení úkolů projektu, používá Project Operations obrysy přiřazení prostředků k vytvoření obrysů detailů požadavku na prostředek.</span><span class="sxs-lookup"><span data-stu-id="7da2c-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="7da2c-112">Odkaz na přiřazení zdrojů se však neudržuje.</span><span class="sxs-lookup"><span data-stu-id="7da2c-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="7da2c-113">Aktualizace rezervací odvozených z požadavku na zdroje neaktualizují žádné přiřazení zdrojů.</span><span class="sxs-lookup"><span data-stu-id="7da2c-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="7da2c-114">Součet rezervací pro zdroj se obvykle bude rovnat součtu přiřazení zdroje napříč jedním nebo více úkoly.</span><span class="sxs-lookup"><span data-stu-id="7da2c-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="7da2c-115">Project Operations však tuto dohodu nevynucuje.</span><span class="sxs-lookup"><span data-stu-id="7da2c-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="7da2c-116">Zobrazení **Vyrovnání** ukazuje projektovému manažerovi místa, kde se neshodují rezervace a přiřazení zdroje.</span><span class="sxs-lookup"><span data-stu-id="7da2c-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>


