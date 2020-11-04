---
title: Nastavení projektových zdrojů
description: Toto téma obsahuje informace o nastavení nebo vyžádání projektových zdrojů.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073952"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="31a93-103">Nastavení projektových zdrojů</span><span class="sxs-lookup"><span data-stu-id="31a93-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31a93-104">Musíte nastavit kalendář a přidružit jej k zaměstnanci nebo pracovníkovi.</span><span class="sxs-lookup"><span data-stu-id="31a93-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="31a93-105">Kalendář se používá k naplánování projektu a pracovní doby zdrojů, které jsou pro projekt rezervovány.</span><span class="sxs-lookup"><span data-stu-id="31a93-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="31a93-106">Během přípravy kalendáře mohou projektoví manažeři provádět vyrovnávání zdrojů jako součást jejich optimalizace.</span><span class="sxs-lookup"><span data-stu-id="31a93-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="31a93-107">Na základě harmonogramu kalendáře lze zdroje omezit.</span><span class="sxs-lookup"><span data-stu-id="31a93-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="31a93-108">Kalendář můžete nastavit na straně **Kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="31a93-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="31a93-109">Když nastavujete pracovníka jako zdroj projektu, můžete vybírat z pracovníků, kteří pracují ve společnosti, pro kterou nastavujete prostředky.</span><span class="sxs-lookup"><span data-stu-id="31a93-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="31a93-110">Případně můžete vybrat pracovníky z jiných společností ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="31a93-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="31a93-111">Tito pracovníci jsou označování jako mezipodnikové zdroje.</span><span class="sxs-lookup"><span data-stu-id="31a93-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="31a93-112">Následující postupy vysvětlují, jak nastavit pracovníka jako projektový zdroj ve vaší společnosti a jak nastavit mezipodnikový projektový zdroj.</span><span class="sxs-lookup"><span data-stu-id="31a93-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="31a93-113">Nastavení pracovníka jako projektový zdroj</span><span class="sxs-lookup"><span data-stu-id="31a93-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="31a93-114">Na stránce **Pracovníci** vyberte v seznamu **Pracovníci** toho pracovníka, kterého přidáváte jako projektový zdroj, a otevřete záznam pracovníka.</span><span class="sxs-lookup"><span data-stu-id="31a93-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="31a93-115">V podokně akcí vyberte **Projekt** &gt; **Nastavení** &gt; **Nastavení projektu**.</span><span class="sxs-lookup"><span data-stu-id="31a93-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="31a93-116">Vyberte kalendář a poté stránku zavřete.</span><span class="sxs-lookup"><span data-stu-id="31a93-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="31a93-117">Můžete také určit výchozí projekty pro zdroj jako typ předběžného přiřazení.</span><span class="sxs-lookup"><span data-stu-id="31a93-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="31a93-118">Předběžné přiřazení lze použít, pokud manažer prostředků nebo projektový manažer předem ví, na kterých projektech bude prostředek pracovat.</span><span class="sxs-lookup"><span data-stu-id="31a93-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="31a93-119">Předběžná přiřazení mohou být také založena na požadavku sponzora projektu nebo zákazníka.</span><span class="sxs-lookup"><span data-stu-id="31a93-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="31a93-120">Chcete-li předem přiřadit projekt, vyberte příslušný projekt na stránce **Přiřadit projekty** na kartě **Projekty** v seznamu **Zbývající projekty**.</span><span class="sxs-lookup"><span data-stu-id="31a93-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="31a93-121">Nastavení mezipodnikového zdroje</span><span class="sxs-lookup"><span data-stu-id="31a93-121">Set up an intercompany resource</span></span>

<span data-ttu-id="31a93-122">Když nastavíte pracovníka jako mezipodnikový zdroj, musíte dokončit nastavení jak ve společnosti poskytující půjčku, tak ve společnosti, která si zdroj půjčuje.</span><span class="sxs-lookup"><span data-stu-id="31a93-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="31a93-123">Ve společnosti poskytující půjčku</span><span class="sxs-lookup"><span data-stu-id="31a93-123">In the lending company</span></span>

1. <span data-ttu-id="31a93-124">V aplikace Finance ověřte, zda je vybrána společnost poskytující půjčku, a poté dokončete postup v předchozí části „Nastavení pracovníka jako projektový zdroj“.</span><span class="sxs-lookup"><span data-stu-id="31a93-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="31a93-125">Na stránce **Mezipodnikové účetnictví** vyberte možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="31a93-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="31a93-126">V poli **ID právnické osoby** vyberte společnost poskytující půjčku.</span><span class="sxs-lookup"><span data-stu-id="31a93-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="31a93-127">Vyplňte zbývající pole podle potřeby a poté vyberte příkaz **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="31a93-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="31a93-128">Na stránce **Cena za převod** vyberte možnost **Nová**.</span><span class="sxs-lookup"><span data-stu-id="31a93-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="31a93-129">V poli **Půjčující si subjekt** vyberte příslušnou společnost.</span><span class="sxs-lookup"><span data-stu-id="31a93-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="31a93-130">Chcete-li půjčující si společnosti zapůjčit pouze zdroj, který jste vytvořili na začátku této části, vyberte v poli **Zdroj** název zdroje, který jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="31a93-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="31a93-131">Chcete-li půjčující si společnosti zpřístupnit všechny zdroje společnosti poskytující půjčku, ponechte pole **Zdroj** prázdné.</span><span class="sxs-lookup"><span data-stu-id="31a93-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="31a93-132">Na stránce **Parametry správy projektu a účetnictví** nastavte na kartě **Mezipodnikové** možnost **Povolit mezipodnikové plánování zdrojů a časové rozvrhy** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="31a93-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="31a93-133">V půjčující si společnosti</span><span class="sxs-lookup"><span data-stu-id="31a93-133">In the borrowing company</span></span>

- <span data-ttu-id="31a93-134">Na stránce **Seznam zdrojů** ve filtru vyhledávání zadejte název zdroje, který jste vytvořili pro společnost poskytující půjčku, abyste ověřili, zda je název zahrnut do seznamu prostředků pro půjčující si společnost.</span><span class="sxs-lookup"><span data-stu-id="31a93-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="31a93-135">Žádosti o projektové zdroje</span><span class="sxs-lookup"><span data-stu-id="31a93-135">Request project resources</span></span>
<span data-ttu-id="31a93-136">Funkce pro plánování projektových zdrojů slouží pouze k tomu, aby manažeři zdrojů distribuovali personální zdroje na zakázkách nebo projektech.</span><span class="sxs-lookup"><span data-stu-id="31a93-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="31a93-137">Chcete-li povolit tuto funkci, proveďte následující úkoly nebo ověřte, že byly dokončeny:</span><span class="sxs-lookup"><span data-stu-id="31a93-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="31a93-138">Nastavte číselné řady.</span><span class="sxs-lookup"><span data-stu-id="31a93-138">Set up number sequences.</span></span>
- <span data-ttu-id="31a93-139">Nastavte pracovní postupy pro správu projektů a účetnictví.</span><span class="sxs-lookup"><span data-stu-id="31a93-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="31a93-140">Povolte pracovní postupy žádostí o zdroje.</span><span class="sxs-lookup"><span data-stu-id="31a93-140">Enable resource request workflows.</span></span>

<span data-ttu-id="31a93-141">Po dokončení předchozích úkolů můžete podle potřeby dokončit následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="31a93-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="31a93-142">Vytvořte požadavek na zdroj z předběžně rezervovaného personálního zdroje.</span><span class="sxs-lookup"><span data-stu-id="31a93-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="31a93-143">Monitorujte žádosti o zdroje.</span><span class="sxs-lookup"><span data-stu-id="31a93-143">Monitor resource requests.</span></span>
- <span data-ttu-id="31a93-144">Vyřizujte žádosti o zdroje.</span><span class="sxs-lookup"><span data-stu-id="31a93-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="31a93-145">Požádejte o personální zdroj ze strukturovaného rozpisu prací.</span><span class="sxs-lookup"><span data-stu-id="31a93-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="31a93-146">Rezervujte si zdroje do projektu bez požadavku na personální zdroj.</span><span class="sxs-lookup"><span data-stu-id="31a93-146">Book resources to a project without having a request for a staffed resource.</span></span>
