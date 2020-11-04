---
title: Navrhování projektových zdrojů
description: Toto téma obsahuje informace o navrhování projektových zdrojů.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 18d7dcd95806841c952ea621ec65b513ef614958
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073999"
---
# <a name="propose-project-resources"></a><span data-ttu-id="2bb9e-103">Navrhování projektových zdrojů</span><span class="sxs-lookup"><span data-stu-id="2bb9e-103">Propose project resources</span></span>

<span data-ttu-id="2bb9e-104">Správci zdrojů mohou navrhnout zdroj projektovému manažerovi pomocí žádosti o zdroj.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="2bb9e-105">Z mřížky žádosti nebo ze samotné žádosti vyberte **Najít zdroje**.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="2bb9e-106">Na stránce **Pomocník plánování** vyberte zdroj a potom v podokně **Vytvořit rezervaci zdroje** v poli **Stav rezervace** vyberte **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Vybraný navržený zdroj](media/Resource-Management-image62.png)

<span data-ttu-id="2bb9e-108">Dojde k následujícím aktualizacím stavu:</span><span class="sxs-lookup"><span data-stu-id="2bb9e-108">The following status updates occur:</span></span>

- <span data-ttu-id="2bb9e-109">Na stránce **Pomocník plánování** jsou ukazatele stavu aktualizovány tak, aby označovaly, že rezervace je navržena, že není závazně rezervována.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Ukazatele stavu pro navrženou rezervaci na stránce Pomocník plánování](media/Resource-Management-image63.png)

- <span data-ttu-id="2bb9e-111">U žádosti o zdroj se stav změní na **Potřebuje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Stav žádosti o zdroj změněný na Potřebuje kontrolu](media/Resource-Management-image64.png)

- <span data-ttu-id="2bb9e-113">Na kartě **Tým** projektu je změněna hodnota **Stav žádosti** obecného člena týmu na **Potřebuje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Stav žádosti obecného člena týmu změněný na Potřebuje kontrolu na kartě Tým](media/Resource-Management-image48.png)

<span data-ttu-id="2bb9e-115">Projektový manažer může návrh buď přijmout, nebo zamítnout.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="2bb9e-116">Správci zdrojů mohou při zpracování žádostí o zdroje použít kterýkoli z následujících přístupů:</span><span class="sxs-lookup"><span data-stu-id="2bb9e-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="2bb9e-117">Navrhnout více zdrojů pro uspokojení poptávky, pokud není k dispozici žádný zdroj pro splnění požadovaných hodin.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="2bb9e-118">Navržené hodiny jsou pak rozděleny mezi více zdrojů, které mohou uspokojit požadované hodiny.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="2bb9e-119">V tomto scénáři se hodiny nemohou překrývat.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="2bb9e-120">Navrhnout méně zdrojů, než je vyžadováno.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="2bb9e-121">V tomto scénáři je navrhovaná kapacita zdroje menší než požadovaná doba, kterou žadatel specifikoval.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="2bb9e-122">Proto, když žadatel přijme navržené prostředky, je vytvořen nesplněný požadavek na zdroj k zachycení zbývající poptávky.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="2bb9e-123">Rezervovat více zdrojů pro uspokojení poptávky, pokud není k dispozici žádný zdroj pro dokončení práce.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="2bb9e-124">Rezervovat méně zdrojů, než je vyžadováno.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-124">Book fewer resources than are required.</span></span> <span data-ttu-id="2bb9e-125">V tomto scénáři je počet rezervovaných hodin menší než počet požadovaných hodin.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="2bb9e-126">Systém vás provede návrhy zdrojů místo rezervací, aby mohl žadatel ověřit a sledovat zbývající poptávku.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="2bb9e-127">Fakturovatelné využití</span><span class="sxs-lookup"><span data-stu-id="2bb9e-127">Billable utilization</span></span>

<span data-ttu-id="2bb9e-128">Zdroje mohou mít cílové fakturovatelné využití.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="2bb9e-129">Toto cílové využití je buď definováno jako atribut výchozí role zdroje, nebo je nastaveno v záznamu konkrétního rezervovatelného zdroje.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="2bb9e-130">Výpočty využití vycházejí ze skutečných hodin, které zdroje vykázaly pomocí schválených časových záznamů.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="2bb9e-131">K výpočtu využití se používají následující vzorce:</span><span class="sxs-lookup"><span data-stu-id="2bb9e-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="2bb9e-132">Fakturovatelné využití = skutečné fakturovatelné hodiny ÷ kapacita zdroje</span><span class="sxs-lookup"><span data-stu-id="2bb9e-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="2bb9e-133">Nefakturovatelné využití = skutečný čas s ID typu fakturace = neúčtovatelné, komplementární nebo nedostupné ÷ kapacita zdroje</span><span class="sxs-lookup"><span data-stu-id="2bb9e-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="2bb9e-134">Interní = skutečný čas bez prodejní smlouvy ÷ kapacita zdroje</span><span class="sxs-lookup"><span data-stu-id="2bb9e-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="2bb9e-135">Kapacita zdroje = pracovní doba zdroje – mimo kancelář – nepracovní dny</span><span class="sxs-lookup"><span data-stu-id="2bb9e-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="2bb9e-136">Zobrazení **Využití zdroje** naleznete v podokně **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Zobrazení Využití zdroje](media/Resource-Management-image65.png)

<span data-ttu-id="2bb9e-138">Každá buňka v tabulce představuje procentuální hodnotu fakturovatelného využití zdroje v určitém období, například den, týden nebo měsíc.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="2bb9e-139">K obarvení buněk se používají následující vzorce:</span><span class="sxs-lookup"><span data-stu-id="2bb9e-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="2bb9e-140">**Zelená:** fakturovatelné využití \>= cílové využití zdroje</span><span class="sxs-lookup"><span data-stu-id="2bb9e-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="2bb9e-141">**Žlutá:** cílové využití – 20 \<= fakturovatelné využití \< cílové využití</span><span class="sxs-lookup"><span data-stu-id="2bb9e-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="2bb9e-142">**Červená:** fakturovatelné využití \< cílové využití – 20</span><span class="sxs-lookup"><span data-stu-id="2bb9e-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="2bb9e-143">Vzhledem k tomu, že je zobrazení **Využití zdroje** založeno na Plánovací vývěsce, můžete k filtrování výsledků využít funkce filtrování Plánovací vývěsky.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="2bb9e-144">Mřížka vyžaduje, abyste nastavili cílové využití buď u role, nebo u konkrétního zdroje.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="2bb9e-145">Pro toto nastavení přejděte na **Zdroje** \> **Role zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="2bb9e-146">Navíc musí být ke každému rezervovatelnému zdroji přiřazena výchozí role.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="2bb9e-147">Přejděte na **Zdroje** \> **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="2bb9e-148">Na kartě **Project Service** ověřte, zda je definována role zdroje a zda pole **Je výchozí** je pro ni nastaveno na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="2bb9e-149">Můžete přidat další role, kde **Je výchozí = Ne**.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="2bb9e-150">Role, ve které **Je výchozí = Ano** , slouží k vyhodnocení využití prostředku vůči cíli pro danou roli.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Nastavení výchozí role](media/Resource-Management-image67.png)

<span data-ttu-id="2bb9e-152">Na kartě **Project Service** můžete také nastavit individuální cílové využití zdroje.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="2bb9e-153">Výpočet využití pak používá toto cílové využití k vyhodnocení cíle zdroje namísto cíle výchozí role zdroje.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="2bb9e-154">Využití je pro zdroj zobrazeno pouze v případě, že tento zdroj má schválenou fakturovatelnou dobu během období zobrazeného v mřížce.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="2bb9e-155">Dostupnost zdroje</span><span class="sxs-lookup"><span data-stu-id="2bb9e-155">Resource availability</span></span>

<span data-ttu-id="2bb9e-156">Je důležité, aby správci zdrojů mohli zobrazit dostupnost zdrojů a aktualizovat rezervace.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="2bb9e-157">V některých případech neexistuje formální poptávka (žádost o zdroj), ale správce zdrojů musí odpovědět na neplánovanou poptávku, která přichází prostřednictvím kanálů, jako je e-mail, telefonní hovor nebo rychlá zpráva.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="2bb9e-158">Správci zdrojů používají k aktualizaci zdrojů a rezervací Plánovací vývěsku.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="2bb9e-159">Jako základ pro výpočet dostupnosti zdroje slouží pracovní doba zdroje.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="2bb9e-160">Rezervace zdrojů spotřebovávají kapacitu zdrojů.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-160">Resource bookings consume the capacity of the resources.</span></span>

![Plánovací vývěska](media/Resource-Management-image68.png)

<span data-ttu-id="2bb9e-162">Plánovací vývěska používá barvy a stínování k zobrazení rezervací, dostupnosti a přerezervace a také stavu rezervací.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="2bb9e-163">Nastavení v Plánovací vývěsce umožňuje zobrazit legendu.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="2bb9e-164">Pokud se vedle konkrétního rezervovatelného zdroje v plánovací vývěsce zobrazí šipka vpravo, lze zdroj rozbalit, aby se zobrazily podrobnosti o práci, pro kterou je zdroj rezervovaný.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Rozbalený rezervovatelný zdroj v Plánovací vývěsce](media/Resource-Management-image69.png)

<span data-ttu-id="2bb9e-166">Protože Dynamics 365 Project Service Automation používá modul Universal Resource Scheduling, tak pokud máte nainstalovanou aplikaci Dynamics 365 Field Service můžete také zobrazit podrobnosti o rezervacích zdrojů pro projekty, pracovní objednávky a všechny další entity, na které jste rozšířili plánování.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Podrobnosti rezervací zdrojů pro projekty a pracovní objednávky](media/Resource-Management-image70.png)

<span data-ttu-id="2bb9e-168">Chcete-li zobrazit další podrobnosti o konkrétním zdroji, klepněte na něj pravým tlačítkem myši a otevřete kartu zdroje.</span><span class="sxs-lookup"><span data-stu-id="2bb9e-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Karta zdroje](media/Resource-Management-image71.png)
