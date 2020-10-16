---
title: Přehled pomocníka plánování
description: Toto téma poskytuje informace o práci s Pomocníkem plánování při rezervaci zdrojů.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907980"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="e4b88-103">Přehled pomocníka plánování</span><span class="sxs-lookup"><span data-stu-id="e4b88-103">Schedule assistant overview</span></span>

<span data-ttu-id="e4b88-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="e4b88-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e4b88-105">Pomocník plánování se používá k rezervaci zdrojů na základě požadavků definovaných projektovým manažerem.</span><span class="sxs-lookup"><span data-stu-id="e4b88-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="e4b88-106">Pomocník plánování se při hledání zdrojů spoléhá na parametry uvedené v požadavku na zdroj.</span><span class="sxs-lookup"><span data-stu-id="e4b88-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="e4b88-107">Pomocník plánování doporučuje zdroje, které odpovídají relevantním požadavkům, jako jsou časová okna nebo potřebné dovednosti.</span><span class="sxs-lookup"><span data-stu-id="e4b88-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="e4b88-108">Poté, co jsou identifikovány vhodné zdroje, může manažer zdrojů nebo projektu rezervovat zdroj pro práci.</span><span class="sxs-lookup"><span data-stu-id="e4b88-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e4b88-109">Požadavky</span><span class="sxs-lookup"><span data-stu-id="e4b88-109">Prerequisites</span></span>

<span data-ttu-id="e4b88-110">Pomocník plánování je součástí řešení Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="e4b88-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="e4b88-111">Toto řešení je součástí a instalováno spolu s Dynamics 365 Project Operations, Dynamics 365 Field Service a Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="e4b88-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="e4b88-112">Odpovídající požadavky a zdroje</span><span class="sxs-lookup"><span data-stu-id="e4b88-112">Matching requirements and resources</span></span>

<span data-ttu-id="e4b88-113">Vygenerovaný požadavek na zdroj je založen na podrobnostech, jako jsou:</span><span class="sxs-lookup"><span data-stu-id="e4b88-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="e4b88-114">Charakteristiky</span><span class="sxs-lookup"><span data-stu-id="e4b88-114">Characteristics</span></span>
-   <span data-ttu-id="e4b88-115">Role</span><span class="sxs-lookup"><span data-stu-id="e4b88-115">Roles</span></span>
-   <span data-ttu-id="e4b88-116">Organizační jednotky</span><span class="sxs-lookup"><span data-stu-id="e4b88-116">Business units</span></span>
-   <span data-ttu-id="e4b88-117">Preference zdroje</span><span class="sxs-lookup"><span data-stu-id="e4b88-117">Resource preferences</span></span>
-   <span data-ttu-id="e4b88-118">Průběhové křivky úsilí</span><span class="sxs-lookup"><span data-stu-id="e4b88-118">Effort contours</span></span>
-   <span data-ttu-id="e4b88-119">Časové pásmo</span><span class="sxs-lookup"><span data-stu-id="e4b88-119">Time zone</span></span>

<span data-ttu-id="e4b88-120">Pomocník plánování používá tyto podrobnosti k filtrování zdrojů.</span><span class="sxs-lookup"><span data-stu-id="e4b88-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="e4b88-121">Spuštění Pomocníka plánování</span><span class="sxs-lookup"><span data-stu-id="e4b88-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="e4b88-122">Existují dva způsoby, jak spustit Pomocníka plánování.</span><span class="sxs-lookup"><span data-stu-id="e4b88-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="e4b88-123">Pokud používáte hybridní režim, můžete v mřížce členů týmu vybrat libovolného člena týmu s nesplněným požadavkem na zdroj a poté vybrat příkaz **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="e4b88-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="e4b88-124">Pokud používáte centrální režim, správce prostředků vyhledá a vybere zdroj.</span><span class="sxs-lookup"><span data-stu-id="e4b88-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="e4b88-125">Filtry pomocníka plánování</span><span class="sxs-lookup"><span data-stu-id="e4b88-125">Schedule assistant filters</span></span>

<span data-ttu-id="e4b88-126">Po spuštění Pomocníka plánování se podrobnosti z požadavku na zdroj zobrazí v levém podokně jako filtrované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="e4b88-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="e4b88-127">Správce zdrojů nebo projektový manažer může doladit výsledky úpravou filtrů podle potřeb plánování.</span><span class="sxs-lookup"><span data-stu-id="e4b88-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="e4b88-128">Podokno filtru zobrazuje možnosti související s prací, včetně:</span><span class="sxs-lookup"><span data-stu-id="e4b88-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="e4b88-129">Zahájení a konec práce</span><span class="sxs-lookup"><span data-stu-id="e4b88-129">Work start and end</span></span>
-   <span data-ttu-id="e4b88-130">Charakteristiky</span><span class="sxs-lookup"><span data-stu-id="e4b88-130">Characteristics</span></span>
-   <span data-ttu-id="e4b88-131">Role</span><span class="sxs-lookup"><span data-stu-id="e4b88-131">Roles</span></span>
-   <span data-ttu-id="e4b88-132">Organizační jednotky</span><span class="sxs-lookup"><span data-stu-id="e4b88-132">Organizational units</span></span>
-   <span data-ttu-id="e4b88-133">Společnost poskytující zdroje</span><span class="sxs-lookup"><span data-stu-id="e4b88-133">Resourcing company</span></span>
-   <span data-ttu-id="e4b88-134">Typy zdrojů</span><span class="sxs-lookup"><span data-stu-id="e4b88-134">Resource types</span></span>
-   <span data-ttu-id="e4b88-135">Preferované zdroje</span><span class="sxs-lookup"><span data-stu-id="e4b88-135">Preferred resources</span></span>
