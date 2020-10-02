---
title: Kontrola navrhovaných zdrojů
description: Toto téma obsahuje informace o způsobu navrhování projektových zdrojů.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897353"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="63fbd-103">Kontrola navrhovaných zdrojů</span><span class="sxs-lookup"><span data-stu-id="63fbd-103">Review proposed resources</span></span>

<span data-ttu-id="63fbd-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="63fbd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="63fbd-105">Správci zdrojů mohou navrhnout zdroj projektovému manažerovi pomocí žádosti o zdroj.</span><span class="sxs-lookup"><span data-stu-id="63fbd-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="63fbd-106">Z mřížky žádosti nebo ze samotné žádosti vyberte **Najít zdroje**.</span><span class="sxs-lookup"><span data-stu-id="63fbd-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="63fbd-107">Na stránce **Pomocník plánování** vyberte zdroj a potom v podokně **Vytvořit rezervaci zdroje** v poli **Stav rezervace** vyberte **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="63fbd-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="63fbd-108">Dojde k následujícím aktualizacím stavu:</span><span class="sxs-lookup"><span data-stu-id="63fbd-108">The following status updates occur:</span></span>

- <span data-ttu-id="63fbd-109">Na stránce **Pomocník plánování** jsou ukazatele stavu aktualizovány tak, aby označovaly, že rezervace je navržena, že není závazně rezervována.</span><span class="sxs-lookup"><span data-stu-id="63fbd-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="63fbd-110">U žádosti o zdroj se stav změní na **Potřebuje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="63fbd-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="63fbd-111">Na kartě **Tým** projektu je změněna hodnota **Stav žádosti** obecného člena týmu na **Potřebuje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="63fbd-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="63fbd-112">Projektový manažer může návrh buď přijmout, nebo zamítnout.</span><span class="sxs-lookup"><span data-stu-id="63fbd-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="63fbd-113">Správci zdrojů mohou při zpracování žádostí o zdroje použít kterýkoli z následujících přístupů:</span><span class="sxs-lookup"><span data-stu-id="63fbd-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="63fbd-114">Navrhnout více zdrojů pro uspokojení poptávky, pokud není k dispozici žádný zdroj pro splnění požadovaných hodin.</span><span class="sxs-lookup"><span data-stu-id="63fbd-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="63fbd-115">Navržené hodiny jsou pak rozděleny mezi více zdrojů, které mohou uspokojit požadované hodiny.</span><span class="sxs-lookup"><span data-stu-id="63fbd-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="63fbd-116">V tomto scénáři se hodiny nemohou překrývat.</span><span class="sxs-lookup"><span data-stu-id="63fbd-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="63fbd-117">Navrhnout méně zdrojů, než je vyžadováno.</span><span class="sxs-lookup"><span data-stu-id="63fbd-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="63fbd-118">V tomto scénáři je navrhovaná kapacita zdroje menší než požadovaná doba, kterou žadatel specifikoval.</span><span class="sxs-lookup"><span data-stu-id="63fbd-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="63fbd-119">Proto, když žadatel přijme navržené prostředky, je vytvořen nesplněný požadavek na zdroj k zachycení zbývající poptávky.</span><span class="sxs-lookup"><span data-stu-id="63fbd-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="63fbd-120">Rezervovat více zdrojů pro uspokojení poptávky, pokud není k dispozici žádný zdroj pro dokončení práce.</span><span class="sxs-lookup"><span data-stu-id="63fbd-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="63fbd-121">Rezervovat méně zdrojů, než je vyžadováno.</span><span class="sxs-lookup"><span data-stu-id="63fbd-121">Book fewer resources than are required.</span></span> <span data-ttu-id="63fbd-122">V tomto scénáři je počet rezervovaných hodin menší než počet požadovaných hodin.</span><span class="sxs-lookup"><span data-stu-id="63fbd-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="63fbd-123">Systém vás provede návrhy zdrojů místo rezervací, aby mohl žadatel ověřit a sledovat zbývající poptávku.</span><span class="sxs-lookup"><span data-stu-id="63fbd-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="63fbd-124">Fakturovatelné využití</span><span class="sxs-lookup"><span data-stu-id="63fbd-124">Billable utilization</span></span>

<span data-ttu-id="63fbd-125">Zdroje mohou mít cílové fakturovatelné využití.</span><span class="sxs-lookup"><span data-stu-id="63fbd-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="63fbd-126">Toto cílové využití je buď definováno jako atribut výchozí role zdroje, nebo je nastaveno v záznamu konkrétního rezervovatelného zdroje.</span><span class="sxs-lookup"><span data-stu-id="63fbd-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="63fbd-127">Výpočty využití vycházejí ze skutečných hodin, které zdroje vykázaly pomocí schválených časových záznamů.</span><span class="sxs-lookup"><span data-stu-id="63fbd-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="63fbd-128">K výpočtu využití se používají následující vzorce:</span><span class="sxs-lookup"><span data-stu-id="63fbd-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="63fbd-129">Fakturovatelné využití = skutečné fakturovatelné hodiny ÷ kapacita zdroje</span><span class="sxs-lookup"><span data-stu-id="63fbd-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="63fbd-130">Nefakturovatelné využití = skutečný čas s ID typu fakturace = neúčtovatelné, komplementární nebo nedostupné ÷ kapacita zdroje</span><span class="sxs-lookup"><span data-stu-id="63fbd-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="63fbd-131">Interní = skutečný čas bez prodejní smlouvy ÷ kapacita zdroje</span><span class="sxs-lookup"><span data-stu-id="63fbd-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="63fbd-132">Kapacita zdroje = pracovní doba zdroje – mimo kancelář – nepracovní dny</span><span class="sxs-lookup"><span data-stu-id="63fbd-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="63fbd-133">Zobrazení **Využití zdroje** naleznete v podokně **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="63fbd-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="63fbd-134">Každá buňka v tabulce představuje procentuální hodnotu fakturovatelného využití zdroje v určitém období, například den, týden nebo měsíc.</span><span class="sxs-lookup"><span data-stu-id="63fbd-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="63fbd-135">K obarvení buněk se používají následující vzorce:</span><span class="sxs-lookup"><span data-stu-id="63fbd-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="63fbd-136">**Zelená:** fakturovatelné využití \>= cílové využití zdroje</span><span class="sxs-lookup"><span data-stu-id="63fbd-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="63fbd-137">**Žlutá:** cílové využití – 20 \<= fakturovatelné využití \< cílové využití</span><span class="sxs-lookup"><span data-stu-id="63fbd-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="63fbd-138">**Červená:** fakturovatelné využití \< cílové využití – 20</span><span class="sxs-lookup"><span data-stu-id="63fbd-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="63fbd-139">Vzhledem k tomu, že je zobrazení **Využití zdroje** založeno na Plánovací vývěsce, můžete k filtrování výsledků využít funkce filtrování Plánovací vývěsky.</span><span class="sxs-lookup"><span data-stu-id="63fbd-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="63fbd-140">Mřížka vyžaduje, abyste nastavili cílové využití buď u role, nebo u konkrétního zdroje.</span><span class="sxs-lookup"><span data-stu-id="63fbd-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="63fbd-141">Pro toto nastavení přejděte na **Zdroje** \> **Role zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="63fbd-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="63fbd-142">Navíc musí být ke každému rezervovatelnému zdroji přiřazena výchozí role.</span><span class="sxs-lookup"><span data-stu-id="63fbd-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="63fbd-143">Přejděte na **Zdroje** \> **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="63fbd-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="63fbd-144">Na kartě **Project Service** ověřte, zda je definována role zdroje a zda pole **Je výchozí** je pro ni nastaveno na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="63fbd-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="63fbd-145">Můžete přidat další role, kde **Je výchozí = Ne**.</span><span class="sxs-lookup"><span data-stu-id="63fbd-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="63fbd-146">Role, ve které **Je výchozí = Ano**, slouží k vyhodnocení využití prostředku vůči cíli pro danou roli.</span><span class="sxs-lookup"><span data-stu-id="63fbd-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="63fbd-147">Na kartě **Project Service** můžete také nastavit individuální cílové využití zdroje.</span><span class="sxs-lookup"><span data-stu-id="63fbd-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="63fbd-148">Výpočet využití pak používá toto cílové využití k vyhodnocení cíle zdroje namísto cíle výchozí role zdroje.</span><span class="sxs-lookup"><span data-stu-id="63fbd-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="63fbd-149">Využití je pro zdroj zobrazeno pouze v případě, že tento zdroj má schválenou fakturovatelnou dobu během období zobrazeného v mřížce.</span><span class="sxs-lookup"><span data-stu-id="63fbd-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="63fbd-150">Dostupnost zdroje</span><span class="sxs-lookup"><span data-stu-id="63fbd-150">Resource availability</span></span>

<span data-ttu-id="63fbd-151">Je důležité, aby správci zdrojů mohli zobrazit dostupnost zdrojů a aktualizovat rezervace.</span><span class="sxs-lookup"><span data-stu-id="63fbd-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="63fbd-152">V některých případech neexistuje formální poptávka (žádost o zdroj), ale správce zdrojů musí odpovědět na neplánovanou poptávku, která přichází prostřednictvím kanálů, jako je e-mail, telefonní hovor nebo rychlá zpráva.</span><span class="sxs-lookup"><span data-stu-id="63fbd-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="63fbd-153">Správci zdrojů používají k aktualizaci zdrojů a rezervací Plánovací vývěsku.</span><span class="sxs-lookup"><span data-stu-id="63fbd-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="63fbd-154">Jako základ pro výpočet dostupnosti zdroje slouží pracovní doba zdroje.</span><span class="sxs-lookup"><span data-stu-id="63fbd-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="63fbd-155">Rezervace zdrojů spotřebovávají kapacitu zdrojů.</span><span class="sxs-lookup"><span data-stu-id="63fbd-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="63fbd-156">Plánovací vývěska používá barvy a stínování k zobrazení rezervací, dostupnosti a přerezervace a také stavu rezervací.</span><span class="sxs-lookup"><span data-stu-id="63fbd-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="63fbd-157">Nastavení v Plánovací vývěsce umožňuje zobrazit legendu.</span><span class="sxs-lookup"><span data-stu-id="63fbd-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="63fbd-158">Pokud se vedle konkrétního rezervovatelného zdroje v plánovací vývěsce zobrazí šipka vpravo, lze zdroj rozbalit, aby se zobrazily podrobnosti o práci, pro kterou je zdroj rezervovaný.</span><span class="sxs-lookup"><span data-stu-id="63fbd-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="63fbd-159">Protože Dynamics 365 Project Operations používá modul Universal Resource Scheduling, tak pokud máte nainstalovanou aplikaci Dynamics 365 Field Service můžete také zobrazit podrobnosti o rezervacích zdrojů pro projekty, pracovní objednávky a všechny další entity, na které jste rozšířili plánování.</span><span class="sxs-lookup"><span data-stu-id="63fbd-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="63fbd-160">Chcete-li zobrazit další podrobnosti o konkrétním zdroji, klepněte na něj pravým tlačítkem myši a otevřete kartu zdroje.</span><span class="sxs-lookup"><span data-stu-id="63fbd-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

