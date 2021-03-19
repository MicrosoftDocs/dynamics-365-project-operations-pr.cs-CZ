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
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279895"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="066e1-103">Rezervace a přiřazení</span><span class="sxs-lookup"><span data-stu-id="066e1-103">Bookings vs assignments</span></span>

<span data-ttu-id="066e1-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="066e1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="066e1-105">Rezervace jsou závazné nebo předběžné přidělení zdrojů k projektu.</span><span class="sxs-lookup"><span data-stu-id="066e1-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="066e1-106">Závazné rezervace spotřebovávají kapacitu zdroje.</span><span class="sxs-lookup"><span data-stu-id="066e1-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="066e1-107">Rezervace představují organizační koncepty pro týmy, aby mohly pochopit, jak budou zdroje zapojeny do různých projektů.</span><span class="sxs-lookup"><span data-stu-id="066e1-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="066e1-108">Dynamics 365 Project Operations považuje rezervace za koncept na úrovni projektu.</span><span class="sxs-lookup"><span data-stu-id="066e1-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="066e1-109">Na rozdíl od rezervací představuje přiřazení závazek zdrojů k úkolům projektu v plánu projektu.</span><span class="sxs-lookup"><span data-stu-id="066e1-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="066e1-110">Zdroje mohou být pojmenované nebo obecné.</span><span class="sxs-lookup"><span data-stu-id="066e1-110">The resources can be named or generic.</span></span>  <span data-ttu-id="066e1-111">Když je požadavek na zdroj odvozen z přiřazení úkolů projektu, používá Project Operations obrysy přiřazení prostředků k vytvoření obrysů detailů požadavku na prostředek.</span><span class="sxs-lookup"><span data-stu-id="066e1-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="066e1-112">Odkaz na přiřazení zdrojů se však neudržuje.</span><span class="sxs-lookup"><span data-stu-id="066e1-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="066e1-113">Aktualizace rezervací odvozených z požadavku na zdroje neaktualizují žádné přiřazení zdrojů.</span><span class="sxs-lookup"><span data-stu-id="066e1-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="066e1-114">Součet rezervací pro zdroj se obvykle bude rovnat součtu přiřazení zdroje napříč jedním nebo více úkoly.</span><span class="sxs-lookup"><span data-stu-id="066e1-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="066e1-115">Project Operations však tuto dohodu nevynucuje.</span><span class="sxs-lookup"><span data-stu-id="066e1-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="066e1-116">Zobrazení **Vyrovnání** ukazuje projektovému manažerovi místa, kde se neshodují rezervace a přiřazení zdroje.</span><span class="sxs-lookup"><span data-stu-id="066e1-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]