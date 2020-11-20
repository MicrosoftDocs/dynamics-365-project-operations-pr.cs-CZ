---
title: Aktualizace projektu
description: Toto téma poskytuje informace o aktualizaci projektů v aplikaci Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131425"
---
# <a name="update-a-project"></a><span data-ttu-id="f28fe-103">Aktualizace projektu</span><span class="sxs-lookup"><span data-stu-id="f28fe-103">Update a project</span></span>

<span data-ttu-id="f28fe-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="f28fe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f28fe-105">Níže je uveden souhrn polí, která lze aktualizovat na projektu po jeho vytvoření, a všechny příslušné důsledky aktualizací.</span><span class="sxs-lookup"><span data-stu-id="f28fe-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="f28fe-106">Pole podrobností projektu</span><span class="sxs-lookup"><span data-stu-id="f28fe-106">Project detail fields</span></span>

- <span data-ttu-id="f28fe-107">**Název**: Název projektu.</span><span class="sxs-lookup"><span data-stu-id="f28fe-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="f28fe-108">**Popis**: Přehled projektu.</span><span class="sxs-lookup"><span data-stu-id="f28fe-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="f28fe-109">**Zákazník**: Společnost, do které bude projekt dodán.</span><span class="sxs-lookup"><span data-stu-id="f28fe-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="f28fe-110">**Šablona kalendáře**: Pracovní doba projektu.</span><span class="sxs-lookup"><span data-stu-id="f28fe-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="f28fe-111">Když se pole změní, přepočítá se celý plán.</span><span class="sxs-lookup"><span data-stu-id="f28fe-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="f28fe-112">**Měna**: Měna projektu.</span><span class="sxs-lookup"><span data-stu-id="f28fe-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="f28fe-113">Toto pole je výchozí na základě měny definované ve smluvní jednotce.</span><span class="sxs-lookup"><span data-stu-id="f28fe-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="f28fe-114">Při aktualizaci smluvní jednotky se aktualizuje také pole.</span><span class="sxs-lookup"><span data-stu-id="f28fe-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="f28fe-115">**Smluvní jednotka**: Organizační jednotka, která zastupuje skupinu nebo divizi společnosti, která je primárně zodpovědná za získání prodeje a řízení dodávky práce a služeb zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="f28fe-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="f28fe-116">**Projektový manažer**: Člen projektového týmu, který má oprávnění kontrolovat a schvalovat časové údaje a výdaje.</span><span class="sxs-lookup"><span data-stu-id="f28fe-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="f28fe-117">Odhad polí</span><span class="sxs-lookup"><span data-stu-id="f28fe-117">Estimate fields</span></span>

- <span data-ttu-id="f28fe-118">**Odhadované počáteční datum**: Počáteční datum projektu.</span><span class="sxs-lookup"><span data-stu-id="f28fe-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="f28fe-119">Když se toto pole aktualizuje, všechny úkoly na projektu se budou pohybovat úměrně s počátečním novým začátkem.</span><span class="sxs-lookup"><span data-stu-id="f28fe-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="f28fe-120">**Datum dokončení**: Datum, kdy je naplánováno ukončení projektu.</span><span class="sxs-lookup"><span data-stu-id="f28fe-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="f28fe-121">**Úsílí**: Odhadované úsilí projektu.</span><span class="sxs-lookup"><span data-stu-id="f28fe-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="f28fe-122">Když jsou do projektu přidány úkoly, toto pole již nelze upravovat.</span><span class="sxs-lookup"><span data-stu-id="f28fe-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="f28fe-123">**Odhadované náklady na práci**: Odhadované pracovní náklady projektu.</span><span class="sxs-lookup"><span data-stu-id="f28fe-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="f28fe-124">Když jsou do projektu přidány pracovní náklady, toto pole již nelze upravovat.</span><span class="sxs-lookup"><span data-stu-id="f28fe-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="f28fe-125">**Odhadované výdaje**: Odhadované výdaje projektu.</span><span class="sxs-lookup"><span data-stu-id="f28fe-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="f28fe-126">Když jsou do projektu přidány výdaje, toto pole již nelze upravovat.</span><span class="sxs-lookup"><span data-stu-id="f28fe-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="f28fe-127">Pole skutečné hodnoty projektu</span><span class="sxs-lookup"><span data-stu-id="f28fe-127">Project actual fields</span></span>
- <span data-ttu-id="f28fe-128">**Skutečný začátek**: Datum zahájení projektu.</span><span class="sxs-lookup"><span data-stu-id="f28fe-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="f28fe-129">**Skutečné dokončení**: Bude aktualizováno po dokončení projektu.</span><span class="sxs-lookup"><span data-stu-id="f28fe-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="f28fe-130">Pole Stav projektu</span><span class="sxs-lookup"><span data-stu-id="f28fe-130">Project status fields</span></span>

- <span data-ttu-id="f28fe-131">**Celkový stav projektu**: Celkový stav projektu poskytnutý manažerem projektu.</span><span class="sxs-lookup"><span data-stu-id="f28fe-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="f28fe-132">**Komentáře**: Textový komentář týkající se aktuálního stavu projektu poskytnutý manažerem projektu.</span><span class="sxs-lookup"><span data-stu-id="f28fe-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>

