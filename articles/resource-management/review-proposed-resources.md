---
title: Kontrola navrhovaných zdrojů
description: Toto téma obsahuje informace o způsobu navrhování projektových zdrojů.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000743"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="231ef-103">Kontrola navrhovaných zdrojů</span><span class="sxs-lookup"><span data-stu-id="231ef-103">Review proposed resources</span></span>

<span data-ttu-id="231ef-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="231ef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="231ef-105">Správci zdrojů mohou navrhnout zdroj projektovému manažerovi pomocí žádosti o zdroj.</span><span class="sxs-lookup"><span data-stu-id="231ef-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="231ef-106">Z mřížky žádosti nebo ze samotné žádosti vyberte **Najít zdroje**.</span><span class="sxs-lookup"><span data-stu-id="231ef-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="231ef-107">Na stránce **Pomocník plánování** vyberte zdroj a potom v podokně **Vytvořit rezervaci zdroje** v poli **Stav rezervace** vyberte **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="231ef-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="231ef-108">Dojde k následujícím aktualizacím stavu:</span><span class="sxs-lookup"><span data-stu-id="231ef-108">The following status updates occur:</span></span>

- <span data-ttu-id="231ef-109">Na stránce **Pomocník plánování** jsou ukazatele stavu aktualizovány tak, aby označovaly, že rezervace je navržena, že není závazně rezervována.</span><span class="sxs-lookup"><span data-stu-id="231ef-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="231ef-110">U žádosti o zdroj se stav změní na **Potřebuje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="231ef-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="231ef-111">Na kartě **Tým** projektu je změněna hodnota **Stav žádosti** obecného člena týmu na **Potřebuje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="231ef-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="231ef-112">Projektový manažer může návrh buď přijmout, nebo zamítnout.</span><span class="sxs-lookup"><span data-stu-id="231ef-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="231ef-113">Správci zdrojů mohou při zpracování žádostí o zdroje použít kterýkoli z následujících přístupů:</span><span class="sxs-lookup"><span data-stu-id="231ef-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="231ef-114">Navrhnout více zdrojů pro uspokojení poptávky, pokud není k dispozici žádný zdroj pro splnění požadovaných hodin.</span><span class="sxs-lookup"><span data-stu-id="231ef-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="231ef-115">Navržené hodiny jsou pak rozděleny mezi více zdrojů, které mohou uspokojit požadované hodiny.</span><span class="sxs-lookup"><span data-stu-id="231ef-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="231ef-116">V tomto scénáři se hodiny nemohou překrývat.</span><span class="sxs-lookup"><span data-stu-id="231ef-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="231ef-117">Navrhnout méně zdrojů, než je vyžadováno.</span><span class="sxs-lookup"><span data-stu-id="231ef-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="231ef-118">V tomto scénáři je navrhovaná kapacita zdroje menší než požadovaná doba, kterou žadatel specifikoval.</span><span class="sxs-lookup"><span data-stu-id="231ef-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="231ef-119">Proto, když žadatel přijme navržené prostředky, je vytvořen nesplněný požadavek na zdroj k zachycení zbývající poptávky.</span><span class="sxs-lookup"><span data-stu-id="231ef-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="231ef-120">Rezervovat více zdrojů pro uspokojení poptávky, pokud není k dispozici žádný zdroj pro dokončení práce.</span><span class="sxs-lookup"><span data-stu-id="231ef-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="231ef-121">Rezervovat méně zdrojů, než je vyžadováno.</span><span class="sxs-lookup"><span data-stu-id="231ef-121">Book fewer resources than are required.</span></span> <span data-ttu-id="231ef-122">V tomto scénáři je počet rezervovaných hodin menší než počet požadovaných hodin.</span><span class="sxs-lookup"><span data-stu-id="231ef-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="231ef-123">Systém vás provede návrhy zdrojů místo rezervací, aby mohl žadatel ověřit a sledovat zbývající poptávku.</span><span class="sxs-lookup"><span data-stu-id="231ef-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="231ef-124">Dostupnost zdroje</span><span class="sxs-lookup"><span data-stu-id="231ef-124">Resource availability</span></span>

<span data-ttu-id="231ef-125">Je důležité, aby správci zdrojů mohli zobrazit dostupnost zdrojů a aktualizovat rezervace.</span><span class="sxs-lookup"><span data-stu-id="231ef-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="231ef-126">V některých případech neexistuje formální poptávka (žádost o zdroj), ale správce zdrojů musí odpovědět na neplánovanou poptávku, která přichází prostřednictvím kanálů, jako je e-mail, telefonní hovor nebo rychlá zpráva.</span><span class="sxs-lookup"><span data-stu-id="231ef-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="231ef-127">Správci zdrojů používají k aktualizaci zdrojů a rezervací Plánovací vývěsku.</span><span class="sxs-lookup"><span data-stu-id="231ef-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="231ef-128">Jako základ pro výpočet dostupnosti zdroje slouží pracovní doba zdroje.</span><span class="sxs-lookup"><span data-stu-id="231ef-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="231ef-129">Rezervace zdrojů spotřebovávají kapacitu zdrojů.</span><span class="sxs-lookup"><span data-stu-id="231ef-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="231ef-130">Plánovací vývěska používá barvy a stínování k zobrazení rezervací, dostupnosti a přerezervace a také stavu rezervací.</span><span class="sxs-lookup"><span data-stu-id="231ef-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="231ef-131">Nastavení v Plánovací vývěsce umožňuje zobrazit legendu.</span><span class="sxs-lookup"><span data-stu-id="231ef-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="231ef-132">Pokud se vedle konkrétního rezervovatelného zdroje v plánovací vývěsce zobrazí šipka vpravo, lze zdroj rozbalit, aby se zobrazily podrobnosti o práci, pro kterou je zdroj rezervovaný.</span><span class="sxs-lookup"><span data-stu-id="231ef-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="231ef-133">Protože Dynamics 365 Project Operations používá modul Universal Resource Scheduling, tak pokud máte nainstalovanou aplikaci Dynamics 365 Field Service můžete také zobrazit podrobnosti o rezervacích zdrojů pro projekty, pracovní objednávky a všechny další entity, na které jste rozšířili plánování.</span><span class="sxs-lookup"><span data-stu-id="231ef-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="231ef-134">Chcete-li zobrazit další podrobnosti o konkrétním zdroji, klepněte na něj pravým tlačítkem myši a otevřete kartu zdroje.</span><span class="sxs-lookup"><span data-stu-id="231ef-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]