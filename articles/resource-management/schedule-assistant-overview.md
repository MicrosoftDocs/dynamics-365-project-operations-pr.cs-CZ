---
title: Přehled pomocníka plánování
description: Toto téma poskytuje informace o práci s Pomocníkem plánování při rezervaci zdrojů.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d58f5f45ca54691b6e736dee5aab7b273a8e042
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014108"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="e091c-103">Přehled pomocníka plánování</span><span class="sxs-lookup"><span data-stu-id="e091c-103">Schedule assistant overview</span></span>

<span data-ttu-id="e091c-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="e091c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e091c-105">Pomocník plánování se používá k rezervaci zdrojů na základě požadavků definovaných projektovým manažerem.</span><span class="sxs-lookup"><span data-stu-id="e091c-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="e091c-106">Pomocník plánování se při hledání zdrojů spoléhá na parametry uvedené v požadavku na zdroj.</span><span class="sxs-lookup"><span data-stu-id="e091c-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="e091c-107">Pomocník plánování doporučuje zdroje, které odpovídají relevantním požadavkům, jako jsou časová okna nebo potřebné dovednosti.</span><span class="sxs-lookup"><span data-stu-id="e091c-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="e091c-108">Poté, co jsou identifikovány vhodné zdroje, může manažer zdrojů nebo projektu rezervovat zdroj pro práci.</span><span class="sxs-lookup"><span data-stu-id="e091c-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e091c-109">Požadavky</span><span class="sxs-lookup"><span data-stu-id="e091c-109">Prerequisites</span></span>

<span data-ttu-id="e091c-110">Pomocník plánování je součástí řešení Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="e091c-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="e091c-111">Toto řešení je součástí a je instalované s Dynamics 365 Project Operations, Dynamics 365 Field Service a Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="e091c-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="e091c-112">Odpovídající požadavky a zdroje</span><span class="sxs-lookup"><span data-stu-id="e091c-112">Matching requirements and resources</span></span>

<span data-ttu-id="e091c-113">Vygenerovaný požadavek na zdroj je založen na podrobnostech, jako jsou:</span><span class="sxs-lookup"><span data-stu-id="e091c-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="e091c-114">Charakteristiky</span><span class="sxs-lookup"><span data-stu-id="e091c-114">Characteristics</span></span>
-   <span data-ttu-id="e091c-115">Role</span><span class="sxs-lookup"><span data-stu-id="e091c-115">Roles</span></span>
-   <span data-ttu-id="e091c-116">Organizační jednotky</span><span class="sxs-lookup"><span data-stu-id="e091c-116">Business units</span></span>
-   <span data-ttu-id="e091c-117">Preference zdroje</span><span class="sxs-lookup"><span data-stu-id="e091c-117">Resource preferences</span></span>
-   <span data-ttu-id="e091c-118">Průběhové křivky úsilí</span><span class="sxs-lookup"><span data-stu-id="e091c-118">Effort contours</span></span>
-   <span data-ttu-id="e091c-119">Časové pásmo</span><span class="sxs-lookup"><span data-stu-id="e091c-119">Time zone</span></span>

<span data-ttu-id="e091c-120">Pomocník plánování používá tyto podrobnosti k filtrování zdrojů.</span><span class="sxs-lookup"><span data-stu-id="e091c-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="e091c-121">Spuštění Pomocníka plánování</span><span class="sxs-lookup"><span data-stu-id="e091c-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="e091c-122">Existují dva způsoby, jak spustit Pomocníka plánování.</span><span class="sxs-lookup"><span data-stu-id="e091c-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="e091c-123">Pokud používáte hybridní režim, můžete v mřížce členů týmu vybrat libovolného člena týmu s nesplněným požadavkem na zdroj a poté vybrat příkaz **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="e091c-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="e091c-124">Pokud používáte centrální režim, správce prostředků vyhledá a vybere zdroj.</span><span class="sxs-lookup"><span data-stu-id="e091c-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="e091c-125">Filtry pomocníka plánování</span><span class="sxs-lookup"><span data-stu-id="e091c-125">Schedule assistant filters</span></span>

<span data-ttu-id="e091c-126">Po spuštění Pomocníka plánování se podrobnosti z požadavku na zdroj zobrazí v levém podokně jako filtrované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="e091c-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="e091c-127">Správce zdrojů nebo projektový manažer může doladit výsledky úpravou filtrů podle potřeb plánování.</span><span class="sxs-lookup"><span data-stu-id="e091c-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="e091c-128">Podokno filtru zobrazuje možnosti související s prací, včetně:</span><span class="sxs-lookup"><span data-stu-id="e091c-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="e091c-129">Zahájení a konec práce</span><span class="sxs-lookup"><span data-stu-id="e091c-129">Work start and end</span></span>
-   <span data-ttu-id="e091c-130">Charakteristiky</span><span class="sxs-lookup"><span data-stu-id="e091c-130">Characteristics</span></span>
-   <span data-ttu-id="e091c-131">Role</span><span class="sxs-lookup"><span data-stu-id="e091c-131">Roles</span></span>
-   <span data-ttu-id="e091c-132">Organizační jednotky</span><span class="sxs-lookup"><span data-stu-id="e091c-132">Organizational units</span></span>
-   <span data-ttu-id="e091c-133">Společnost poskytující zdroje</span><span class="sxs-lookup"><span data-stu-id="e091c-133">Resourcing company</span></span>
-   <span data-ttu-id="e091c-134">Typy zdrojů</span><span class="sxs-lookup"><span data-stu-id="e091c-134">Resource types</span></span>
-   <span data-ttu-id="e091c-135">Preferované zdroje</span><span class="sxs-lookup"><span data-stu-id="e091c-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]