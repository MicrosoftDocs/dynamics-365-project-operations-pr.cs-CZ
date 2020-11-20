---
title: Správa zdrojů
description: Toto téma obsahuje informace o způsobu správy zdrojů.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 548595e3951f824e1c79a641d3f336e381fcaaf9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132325"
---
# <a name="manage-resources"></a><span data-ttu-id="4149b-103">Správa zdrojů</span><span class="sxs-lookup"><span data-stu-id="4149b-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4149b-104">Dynamics 365 Project Service Automation obsahuje řídicí panel správce zdrojů, který poskytuje vizuální přehled o poptávce a využití zdrojů v celé organizaci.</span><span class="sxs-lookup"><span data-stu-id="4149b-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="4149b-105">Grafy na tomto řídicím panelu můžete použít k vizualizaci následujících informací:</span><span class="sxs-lookup"><span data-stu-id="4149b-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="4149b-106">**Poptávka po zdroji** – graf **Aktivní žádost o zdroj** zobrazuje zdroje, které byly odeslány.</span><span class="sxs-lookup"><span data-stu-id="4149b-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="4149b-107">Zdroje jsou agregovány podle role nebo projektu.</span><span class="sxs-lookup"><span data-stu-id="4149b-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="4149b-108">**Neodeslaná poptávka po zdroji** – graf **Nepřiřazená poptávka po zdroji** zobrazuje všechny požadavky na zdroje, které nebyly odeslány.</span><span class="sxs-lookup"><span data-stu-id="4149b-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="4149b-109">Pomáhá správcům zdrojů Zobrazit poptávku, která není pevná a může být odeslána prostřednictvím žádosti o zdroj.</span><span class="sxs-lookup"><span data-stu-id="4149b-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="4149b-110">**Fakturovatelné využití za minulý týden** – graf **Využití podle role** zobrazuje procentuální hodnotu skutečného fakturovatelného využití podle role v rámci organizace vzhledem k jejímu cílovému fakturovatelnému využití podle role.</span><span class="sxs-lookup"><span data-stu-id="4149b-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4149b-111">Chcete-li graf **Využití podle role** zpřístupnit, vytvořte úlohu, která spustí pracovní postup UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="4149b-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="4149b-112">Tato opakovaná úloha se spouští každých sedm dní pro výpočet fakturovatelného využití za předchozích sedm dní.</span><span class="sxs-lookup"><span data-stu-id="4149b-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="4149b-113">Výsledky jsou agregovány podle role.</span><span class="sxs-lookup"><span data-stu-id="4149b-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="4149b-114">Správa členů projektového týmu</span><span class="sxs-lookup"><span data-stu-id="4149b-114">Manage project team members</span></span>

<span data-ttu-id="4149b-115">Projektoví manažeři mohou pomocí řídicího panelu správce zdrojů spravovat zdroje na projektech.</span><span class="sxs-lookup"><span data-stu-id="4149b-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="4149b-116">Mohou například přidat člena týmu přímo do projektu a rezervovat člena týmu, aby splnili požadavky na zdroje, které byly zachyceny obecným zdrojem.</span><span class="sxs-lookup"><span data-stu-id="4149b-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="4149b-117">Přidání člena týmu přímo do projektu</span><span class="sxs-lookup"><span data-stu-id="4149b-117">Add a team member directly to a project</span></span>

<span data-ttu-id="4149b-118">Chcete-li přidat člena týmu přímo do projektu, vyberte na stránce **Projekty**, na kartě **Tým** **Nový**.</span><span class="sxs-lookup"><span data-stu-id="4149b-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="4149b-119">Zobrazí se dialogové okno **Vytvořit: Člen projektového týmu**.</span><span class="sxs-lookup"><span data-stu-id="4149b-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="4149b-120">V tomto dialogovém okně můžete provádět následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="4149b-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="4149b-121">**Rezervace pojmenovaného zdroje** – v poli zdroj **Rezervovatelný zdroj** vyberte název zdroje.</span><span class="sxs-lookup"><span data-stu-id="4149b-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="4149b-122">Potom vyberte roli, nastavte období a vyberte metodu přidělení.</span><span class="sxs-lookup"><span data-stu-id="4149b-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="4149b-123">Pojmenovaný zdroj, který jste vybrali, je přidán do projektu pomocí vybrané metody přidělení a kalendáře zdrojů.</span><span class="sxs-lookup"><span data-stu-id="4149b-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="4149b-124">**Přidání obecného zdroje** – ponechte pole **Rezervovatelný zdroj** prázdné, a poté vyberte roli, nastavte období a vyberte upřednostňovanou metodu přidělení.</span><span class="sxs-lookup"><span data-stu-id="4149b-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="4149b-125">Obecný zdroj je přidán do týmu jako zástupný symbol pro uchování vzoru poptávky, který slouží k rezervaci pojmenovaných zdrojů v týmu.</span><span class="sxs-lookup"><span data-stu-id="4149b-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="4149b-126">Požadavek je proveden podle projektového kalendáře.</span><span class="sxs-lookup"><span data-stu-id="4149b-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="4149b-127">**Přidání pojmenovaného zdroje do týmu bez spotřeby kapacity zdroje** – v poli **Rezervovatelný zdroj** vyberte zdroj.</span><span class="sxs-lookup"><span data-stu-id="4149b-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="4149b-128">Potom vyberte období a jako metodu přidělení vyberte **Žádná**.</span><span class="sxs-lookup"><span data-stu-id="4149b-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="4149b-129">Zdroj je přidán do týmu, ale kapacita zdroje není při rezervaci spotřebována.</span><span class="sxs-lookup"><span data-stu-id="4149b-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="4149b-130">Rezervace člena týmu za účelem splnění požadavků na zdroje pro obecný zdroj</span><span class="sxs-lookup"><span data-stu-id="4149b-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="4149b-131">V programu PSA můžete rezervovat obecný zdroj v projektovém týmu a určit roli, požadovanou kapacitu a způsob distribuce kapacity.</span><span class="sxs-lookup"><span data-stu-id="4149b-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="4149b-132">U požadavku na zdroj můžete zadat atributy, které jsou přidruženy k obecnému zdroji.</span><span class="sxs-lookup"><span data-stu-id="4149b-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="4149b-133">Tyto atributy zahrnují požadované dovednosti, upřednostňovanou organizační jednotku a upřednostňované zdroje.</span><span class="sxs-lookup"><span data-stu-id="4149b-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="4149b-134">Chcete-li pro vývojáře zadat požadované dovednosti u obecného zdroje, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="4149b-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="4149b-135">Chcete-li rezervovat obecný zdroj, vyberte na stránce **Projekty** na kartě **Tým** **Nový**.</span><span class="sxs-lookup"><span data-stu-id="4149b-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Obecný zdroj rezervovaná v týmu](media/Resource-Management-image9.png)

2. <span data-ttu-id="4149b-137">V zobrazení **Všichni členové týmu**, ve sloupci **Požadavek na zdroj** vyberte odkaz pro přidání požadovaných požadovaných dovedností pro obecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="4149b-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Odkaz na požadavek](media/Resource-Management-image10.png)

3. <span data-ttu-id="4149b-139">Na stránce **Požadavek na zdroj**, která se zobrazí, vyberte v mřížce **Dovednosti** výpustku (**…**) a pak vyberte **Přidat novou charakteristiku požadavku**, chcete-li přidat požadované dovednosti pro vývojáře.</span><span class="sxs-lookup"><span data-stu-id="4149b-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Příkaz Přidat novou charakteristiku požadavku](media/Resource-Management-image11.png)

4. <span data-ttu-id="4149b-141">V dialogovém okně **Vytvořit: Charakteristika požadavku**, které se zobrazí, vyberte v poli **Charakteristika** požadovanou dovednost.</span><span class="sxs-lookup"><span data-stu-id="4149b-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="4149b-142">Potom v poli **Hodnota hodnocení** vyberte úroveň odborné způsobilosti pro tuto dovednost.</span><span class="sxs-lookup"><span data-stu-id="4149b-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="4149b-143">Nakonec v poli **Požadavek na zdroj** nastavte požadavek na zdrojové zdroje z organizačních jednotek nebo dokonce pojmenovaných zdrojů.</span><span class="sxs-lookup"><span data-stu-id="4149b-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="4149b-144">Jakmile budete hotovi, zvolte tlačítko **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="4149b-144">When you've finished, select **Save**.</span></span>

    ![Dialogové okno Vytvořit: Charakteristika požadavku](media/Resource-Management-image12.png)

5. <span data-ttu-id="4149b-146">Chcete-li splnit požadavek na zdroj, vyberte na stránce **Požadavek na zdroj** **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="4149b-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Tlačítko Rezervovat na stránce požadavek na zdroj](media/Resource-Management-image13.png)

    <span data-ttu-id="4149b-148">Můžete také vybrat obecný zdroj v mřížce **Všichni členové týmu** a pak vybrat **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="4149b-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Tlačítko Rezervovat nad mřížkou Všichni členové týmu](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="4149b-150">V tomto příkladu je požadováno 40 hodin, ale žádné skutečné rezervované hodiny, protože obecné zdroje nemají rezervace.</span><span class="sxs-lookup"><span data-stu-id="4149b-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="4149b-151">Navíc nejsou přiřazeny žádné hodiny, protože obecný zdroj byl přidán přímo do týmu.</span><span class="sxs-lookup"><span data-stu-id="4149b-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="4149b-152">Nebyl přidáno pomocí přiřazení úkolu.</span><span class="sxs-lookup"><span data-stu-id="4149b-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="4149b-153">Na stránce **Pomocník plánování** můžete filtrovat dostupné zdroje podle požadavků, které jsou specifikovány u požadavku na zdroj.</span><span class="sxs-lookup"><span data-stu-id="4149b-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="4149b-154">Zdroje jsou seřazeny podle parametrů řazení, které jsou specifikovány v Plánovací vývěsce.</span><span class="sxs-lookup"><span data-stu-id="4149b-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Stránka Pomocník plánování](media/Resource-Management-image15.png)

    <span data-ttu-id="4149b-156">Zde jsou některé filtry, které se často používají:</span><span class="sxs-lookup"><span data-stu-id="4149b-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="4149b-157">**Vlastnosti společně s hodnocením** – filtr podle dovedností, certifikací a dalších vlastností zdroje, kromě hodnocení odbornosti.</span><span class="sxs-lookup"><span data-stu-id="4149b-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="4149b-158">**Role** – filtr podle výchozích rolí, které jsou přiřazeny k rezervovatelným zdrojům.</span><span class="sxs-lookup"><span data-stu-id="4149b-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="4149b-159">**Organizační jednotky** – filtr rezervovatelných zdrojů podle organizačních jednotek, ke kterým jsou přiřazeny.</span><span class="sxs-lookup"><span data-stu-id="4149b-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="4149b-160">Pokud nejste spokojeni s výsledky počátečního hledání požadavku, můžete kritéria filtru změnit.</span><span class="sxs-lookup"><span data-stu-id="4149b-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="4149b-161">Chcete-li najít další zdroje, rozbalte podokno **Filtrovat zobrazení** a pak vyberte **Hledat**.</span><span class="sxs-lookup"><span data-stu-id="4149b-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Podokno Filtrovat zobrazení](media/Resource-Management-image16.png)

7. <span data-ttu-id="4149b-163">Chcete-li změnit způsob řazení výsledků, vyberte **Řadit**.</span><span class="sxs-lookup"><span data-stu-id="4149b-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Příkaz Řadit](media/Resource-Management-image17.png)

8. <span data-ttu-id="4149b-165">Vyberte zdroje podle poptávky, která je určena u požadavku, jak je uvedeno v horní části mřížky.</span><span class="sxs-lookup"><span data-stu-id="4149b-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="4149b-166">Výběr buněk v mřížce můžete vymazat a ponechat tuto kapacitu zdroje otevřenou.</span><span class="sxs-lookup"><span data-stu-id="4149b-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="4149b-167">Jako rezervovaný lze najednou vybrat pouze jeden zdroj.</span><span class="sxs-lookup"><span data-stu-id="4149b-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="4149b-168">Chcete-li vybraný zdroj rezervovat, vyberte **Rezervovat** a ponechejte Plánovací vývěsku otevřenou, aby bylo možné vybrat další zdroje.</span><span class="sxs-lookup"><span data-stu-id="4149b-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="4149b-169">Případně vyberte **Rezervovat a ukončit**, chcete-li rezervovat vybraný zdroj a zavřít Plánovací vývěsku.</span><span class="sxs-lookup"><span data-stu-id="4149b-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Zdroj k rezervaci](media/Resource-Management-image19.png)

    <span data-ttu-id="4149b-171">Obdržíte oznámení o rezervovaných hodinách.</span><span class="sxs-lookup"><span data-stu-id="4149b-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="4149b-172">Ukazatele poptávky ukazují, z jaké části je požadavek na rezervaci splněn a kolik zbývá.</span><span class="sxs-lookup"><span data-stu-id="4149b-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="4149b-173">Můžete také zobrazit, jak velká část kapacity vybraného zdroje je spotřebována.</span><span class="sxs-lookup"><span data-stu-id="4149b-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="4149b-174">Chcete-li zobrazit další podrobnosti o rezervaci zdrojů, vyberte možnost **Rozbalit**.</span><span class="sxs-lookup"><span data-stu-id="4149b-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="4149b-175">Vraťte se do zobrazení **Všichni členové týmu**.</span><span class="sxs-lookup"><span data-stu-id="4149b-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="4149b-176">V mřížce si všimněte, že obecný zdroj byl nahrazen pojmenovaným zdrojem, a že je u tohoto zdroje uvedeno 40 hodin jako rezervovaných.</span><span class="sxs-lookup"><span data-stu-id="4149b-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Aktualizovaná mřížka Všichni členové týmu](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="4149b-178">Nejsou zobrazeny žádné přidělené hodiny, protože byly rezervováni přímo v týmu.</span><span class="sxs-lookup"><span data-stu-id="4149b-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="4149b-179">Nebyli rezervováni pomocí přiřazení úkolu.</span><span class="sxs-lookup"><span data-stu-id="4149b-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="4149b-180">Přiřazení obecného zdroje k úkolům a vygenerování požadavků na zdroj</span><span class="sxs-lookup"><span data-stu-id="4149b-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="4149b-181">V PSA můžete vytvářet úkoly a poté k nim přiřazovat obecné zdroje.</span><span class="sxs-lookup"><span data-stu-id="4149b-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="4149b-182">Tímto způsobem může být poptávka po zdroji při odhadu vašeho plánu a finančních čísel představována zástupnými symboly.</span><span class="sxs-lookup"><span data-stu-id="4149b-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="4149b-183">Poté můžete generovat požadavky na zdroje pro obecné zdroje a splnit je.</span><span class="sxs-lookup"><span data-stu-id="4149b-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="4149b-184">Chcete-li vytvořit úlohu, vyberte na stránce **Projekty** na kartě **Plán** **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="4149b-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Byl vytvořen nový úkol](media/Resource-Management-image21.png)

2. <span data-ttu-id="4149b-186">V poli **Zdroje** vyberte symbol **Výběr zdroje**.</span><span class="sxs-lookup"><span data-stu-id="4149b-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="4149b-187">Zobrazí se dialogové okno Výběr zdroje zobrazující existující členy týmu pro projekt.</span><span class="sxs-lookup"><span data-stu-id="4149b-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Výběr zdroje](media/Resource-Management-image22.png)

3. <span data-ttu-id="4149b-189">Zadejte název nového obecného zdroje a pak vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="4149b-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Byl zadán název nového obecného zdroje](media/Resource-Management-image23.png)

4. <span data-ttu-id="4149b-191">V dialogovém okně **Vytvořit: Člen projektového týmu**, které se zobrazí, vyberte v poli **Role** roli obecného zdroje.</span><span class="sxs-lookup"><span data-stu-id="4149b-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="4149b-192">V poli **Jednotka zdroje** vyberte organizační jednotku pro obecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="4149b-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="4149b-193">Pak vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="4149b-193">Then select **Save**.</span></span>

    ![Dialogové okno Vytvořit: Člen projektového týmu](media/Resource-Management-image24.png)

    <span data-ttu-id="4149b-195">Obecný člen týmu je nyní přiřazen k úkolu.</span><span class="sxs-lookup"><span data-stu-id="4149b-195">The generic team member is now assigned to the task.</span></span>

    ![Obecný člen týmu přiřazený k úkolu](media/Resource-Management-image25.png)

    <span data-ttu-id="4149b-197">Na kartě **Tým** se zobrazí nový obecný člen týmu.</span><span class="sxs-lookup"><span data-stu-id="4149b-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="4149b-198">Povšimněte si, že má přiřazené pouze hodiny.</span><span class="sxs-lookup"><span data-stu-id="4149b-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="4149b-199">Tyto hodiny představují součet všech úkolů, které jsou přiřazeny k obecnému členu týmu.</span><span class="sxs-lookup"><span data-stu-id="4149b-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="4149b-200">Obecný člen týmu ještě nemá požadované hodiny ani požadavek na zdroj.</span><span class="sxs-lookup"><span data-stu-id="4149b-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Obecný člen týmu na kartě Tým](media/Resource-Management-image26.png)

5. <span data-ttu-id="4149b-202">Obecného člena týmu můžete nyní přiřadit k jiným úkolům pomocí symbolu Výběr zdroje.</span><span class="sxs-lookup"><span data-stu-id="4149b-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Obecný člen týmu ve Výběru zdroje](media/Resource-Management-image27.png)

    <span data-ttu-id="4149b-204">Po dokončení přiřazení obecného zdroje k úkolům můžete generovat požadavek na zdroj pro obecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="4149b-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="4149b-205">Na kartě **Tým** vyberte obecný zdroj a pak vyberte **Generate Requirement**.</span><span class="sxs-lookup"><span data-stu-id="4149b-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Příkaz Generovat požadavek](media/Resource-Management-image28.png)

    <span data-ttu-id="4149b-207">Po vygenerování požadavku bude mít obecný člen týmu požadované hodiny a odkaz na požadavek na zdroj.</span><span class="sxs-lookup"><span data-stu-id="4149b-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Odkaz Požadavek na zdroj](media/Resource-Management-image29.png)

    <span data-ttu-id="4149b-209">Jakmile provedete rezervaci pojmenovaného zdroje, je obecný zdroj odebrán z týmu a nahrazen pojmenovaným zdrojem.</span><span class="sxs-lookup"><span data-stu-id="4149b-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Obecný zdroj nahrazený pojmenovaným zdrojem](media/Resource-Management-image30.png)

    <span data-ttu-id="4149b-211">Na kartě **Plán** jsou odebrána přiřazení obecných zdrojů a nahrazena pojmenovaným zdrojem.</span><span class="sxs-lookup"><span data-stu-id="4149b-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Přiřazení obecných zdrojů nahrazená pojmenovaným zdrojem na kartě Plán](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="4149b-213">K tomuto chování dochází pouze v případě, že je pojmenovaný zdroj plně rezervovaný pro obecný požadavek na zdroj.</span><span class="sxs-lookup"><span data-stu-id="4149b-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="4149b-214">Pokud některý pojmenovaný zdroj částečně nahradí požadavek na obecný zdroj nebo více pojmenovaných zdrojů nahradí požadavek na obecný zdroj, zůstane obecný zdroj přiřazen k úkolu.</span><span class="sxs-lookup"><span data-stu-id="4149b-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="4149b-215">Na následujícím obrázku byl naplánován úkol v rozsahu 80 hodin, s pětidenní dobu trvání (16 hodin denně po dobu pěti dní) a přiřazen obecnému zdroji s názvem **Funkční**.</span><span class="sxs-lookup"><span data-stu-id="4149b-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![80hodinový, pětidenní úkol, přiřazený obecnému zdroji Funkční](media/Resource-Management-image32.png)

    <span data-ttu-id="4149b-217">Když vygenerujete požadavek, je na 80 hodin po dobu pěti dní.</span><span class="sxs-lookup"><span data-stu-id="4149b-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Požadavek vygenerovaný pro 80 hodin po dobu pěti dní](media/Resource-Management-image33.png)

    <span data-ttu-id="4149b-219">Vzhledem k tomu, že dostupné zdroje pracují pouze osm hodin denně, je nutné ke splnění požadavku použít dva zdroje.</span><span class="sxs-lookup"><span data-stu-id="4149b-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Druhý zdroj](media/Resource-Management-image35.png)

    <span data-ttu-id="4149b-221">Na kartě **Tým** nyní můžete vidět, že obecný zdroj nemá žádné požadované hodiny, ale přiřazené hodiny jsou stále zobrazeny společně se dvěma pojmenovanými zdroji, které tvoří splnění.</span><span class="sxs-lookup"><span data-stu-id="4149b-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Dva pojmenované zdroje na kartě Tým](media/Resource-Management-image36.png)

    <span data-ttu-id="4149b-223">Obecný zdroj zůstává na kartě **Plán** přiřazený k úkolu.</span><span class="sxs-lookup"><span data-stu-id="4149b-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Obecné zdroje na kartě Plán](media/Resource-Management-image37.png)

<span data-ttu-id="4149b-225">PSA nepřiřazuje k úkolu oba zdroje, protože toto chování by vyvolalo méně předvídatelný plán.</span><span class="sxs-lookup"><span data-stu-id="4149b-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="4149b-226">V tomto jednoduchém příkladu je snadné rozdělit hodiny rovnoměrně mezi dva zdroje.</span><span class="sxs-lookup"><span data-stu-id="4149b-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="4149b-227">Ve složitějších scénářích, které zahrnují více úkolů a více zdrojů, by však aplikace PSA musela učinit předpoklady, jak by měla rozdělit rezervace přijaté pro více zdrojů ve více úkolech.</span><span class="sxs-lookup"><span data-stu-id="4149b-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="4149b-228">Proto je v těchto scénářích za analýzu vícenásobných rezervací a jejich přiřazení podle potřeby zodpovědný projektový manažer.</span><span class="sxs-lookup"><span data-stu-id="4149b-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="4149b-229">K rozdělení rezervací přiřadí vedoucí projektu úkoly z obecných zdrojů k pojmenovaným zdrojům a potom použije zobrazení **odsouhlasení**, aby se ujistil, že přidělení pracuje s rezervacemi.</span><span class="sxs-lookup"><span data-stu-id="4149b-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="4149b-230">Úprava požadavku na zdroj</span><span class="sxs-lookup"><span data-stu-id="4149b-230">Edit a resource requirement</span></span>

<span data-ttu-id="4149b-231">Po vytvoření požadavku na zdroj může projektový manažer nebo správce zdrojů chtít upravit podrobnosti a upřesnit kritéria hledání při použití plánovací vývěsky.</span><span class="sxs-lookup"><span data-stu-id="4149b-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="4149b-232">Chcete-li upravit požadavek na zdroj, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="4149b-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="4149b-233">Na stánce **Projekty** vyberte na kartě **Tým** odkaz na libovolný požadavek na obecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="4149b-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="4149b-234">Na stránce **Požadavek na zdroj**, která se zobrazí, můžete aktualizovat několik atributů.</span><span class="sxs-lookup"><span data-stu-id="4149b-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="4149b-235">Zde je uvedeno několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="4149b-235">Here are some examples:</span></span>

    - <span data-ttu-id="4149b-236">Jméno</span><span class="sxs-lookup"><span data-stu-id="4149b-236">Name</span></span>
    - <span data-ttu-id="4149b-237">Od data</span><span class="sxs-lookup"><span data-stu-id="4149b-237">From Date</span></span>
    - <span data-ttu-id="4149b-238">Do data</span><span class="sxs-lookup"><span data-stu-id="4149b-238">To Date</span></span>
    - <span data-ttu-id="4149b-239">Doba trvání</span><span class="sxs-lookup"><span data-stu-id="4149b-239">Duration</span></span>
    - <span data-ttu-id="4149b-240">Typ zdroje</span><span class="sxs-lookup"><span data-stu-id="4149b-240">Resource Type</span></span>

<span data-ttu-id="4149b-241">Na stránce **Požadavek na zdroj** může projektový manažer nebo správce zdrojů definovat i následující informace:</span><span class="sxs-lookup"><span data-stu-id="4149b-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="4149b-242">Dovednosti</span><span class="sxs-lookup"><span data-stu-id="4149b-242">Skills</span></span>
- <span data-ttu-id="4149b-243">Role</span><span class="sxs-lookup"><span data-stu-id="4149b-243">Roles</span></span>
- <span data-ttu-id="4149b-244">Předvolby zdroje</span><span class="sxs-lookup"><span data-stu-id="4149b-244">Resource preferences</span></span>
- <span data-ttu-id="4149b-245">Preferovaná organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="4149b-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="4149b-246">Aktualizace rezervací zdrojů po jejich rezervaci do projektu</span><span class="sxs-lookup"><span data-stu-id="4149b-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="4149b-247">Po přidání obecného nebo pojmenovaného zdroje do projektového týmu můžete změnit rezervace zdrojů.</span><span class="sxs-lookup"><span data-stu-id="4149b-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="4149b-248">Na stránce **Projekty** vyberte na kartě **Tým** člena týmu a poté vyberte **Zachovat rezervace**.</span><span class="sxs-lookup"><span data-stu-id="4149b-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Otevřená Plánovací vývěska pro vybraného člena týmu](media/Resource-Management-image40.png)

    <span data-ttu-id="4149b-250">Zobrazí se Plánovací vývěska a zobrauje rezervace členů projektového týmu.</span><span class="sxs-lookup"><span data-stu-id="4149b-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="4149b-251">Rozbalte záznam člena týmu a zobrazte hodiny, které byly zarezervovány pro tento projekt a další projekty, které spotřebovávají kapacitu tohoto člena týmu.</span><span class="sxs-lookup"><span data-stu-id="4149b-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="4149b-252">Výběrem a přetažením rezervace ji prodlouhujte nebo zkrátíte.</span><span class="sxs-lookup"><span data-stu-id="4149b-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="4149b-253">Zobrazí se dialogové okno **Vytvořit rezervaci zdroje**, které vám umožní upravit rezervaci.</span><span class="sxs-lookup"><span data-stu-id="4149b-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Dialogové okno Vytvořit rezervaci zdroje](media/Resource-Management-image41.png)

3. <span data-ttu-id="4149b-255">Klepněte na rezervaci pravým tlačítkem myši.</span><span class="sxs-lookup"><span data-stu-id="4149b-255">Right-click the booking.</span></span> <span data-ttu-id="4149b-256">Potom můžete pomocí místní nabídky provést následující akce:</span><span class="sxs-lookup"><span data-stu-id="4149b-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="4149b-257">Změnit stav rezervace.</span><span class="sxs-lookup"><span data-stu-id="4149b-257">Change the booking status.</span></span>
    - <span data-ttu-id="4149b-258">Upravit rezervaci.</span><span class="sxs-lookup"><span data-stu-id="4149b-258">Edit the booking.</span></span>
    - <span data-ttu-id="4149b-259">Nahradit zdroj v projektovém týmu.</span><span class="sxs-lookup"><span data-stu-id="4149b-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="4149b-260">Změna stavu rezervace</span><span class="sxs-lookup"><span data-stu-id="4149b-260">Change the booking status</span></span>

<span data-ttu-id="4149b-261">Můžete změnit libovolný výchozí nebo vlastní stav rezervace.</span><span class="sxs-lookup"><span data-stu-id="4149b-261">You can change any default or custom booking status.</span></span>

![Příkaz Změnit stav](media/Resource-Management-image42.png)

<span data-ttu-id="4149b-263">Následující stavy jsou k dispozici v PSA:</span><span class="sxs-lookup"><span data-stu-id="4149b-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="4149b-264">**Zrušeno** – tento stav zruší rezervaci zdroje a uvolní kapacitu zdroje.</span><span class="sxs-lookup"><span data-stu-id="4149b-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="4149b-265">**Závazná rezervace** – tento stav spotřebovává kapacitu zdroje.</span><span class="sxs-lookup"><span data-stu-id="4149b-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="4149b-266">Rezervace má obvykle tento stav, když otevřete **Zachovat rezervace** z mřížky **Všichni členové týmu** na stránce **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="4149b-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="4149b-267">**Předběžná rezervace** – tento stav přidá zdroj k týmu, ale nespotřebovává kapacitu zdroje.</span><span class="sxs-lookup"><span data-stu-id="4149b-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="4149b-268">Označuje, že zdroj byl rezervován pro potenciální práci, ale stále má kapacitu, pokud je potřebný pro jiné práce.</span><span class="sxs-lookup"><span data-stu-id="4149b-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="4149b-269">Vzhledem k celkové dostupnosti zdroje mají předběžné rezervace jiný stav než závazné rezervace.</span><span class="sxs-lookup"><span data-stu-id="4149b-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="4149b-270">**Navrženo** – tento stav představuje návrh správce zdroje nebo projektového manažera pro zdroj.</span><span class="sxs-lookup"><span data-stu-id="4149b-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="4149b-271">Návrhy nespotřebovávají kapacitu zdroje a zdroj není přidán do projektového týmu.</span><span class="sxs-lookup"><span data-stu-id="4149b-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="4149b-272">Chcete-li zdroj v týmu pevně rezervovat, musí projektový manažer tento návrh přijmout.</span><span class="sxs-lookup"><span data-stu-id="4149b-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="4149b-273">Odeslání žádostí o zdroje</span><span class="sxs-lookup"><span data-stu-id="4149b-273">Submit resource requests</span></span>

<span data-ttu-id="4149b-274">Požadavky na zdroj se používají k přenosu poptávky (požadavku na zdroj), která musí být splněna správcem zdroje.</span><span class="sxs-lookup"><span data-stu-id="4149b-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="4149b-275">Pro obecný zdroj, který je již v týmu, můžete odeslat požadavek na zdroj přímo.</span><span class="sxs-lookup"><span data-stu-id="4149b-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="4149b-276">Žádost o zdroj lze splnit dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="4149b-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="4149b-277">Správce zdroje přímo splní žádost.</span><span class="sxs-lookup"><span data-stu-id="4149b-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="4149b-278">V tomto případě je obecný zdroj nahrazen závaznou rezervací, která obsahuje pojmenovaný zdroj.</span><span class="sxs-lookup"><span data-stu-id="4149b-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="4149b-279">Správce zdroje navrhne zdroj projektovému manažerovi a projektový manažer navržený zdroj schválí nebo zamítne.</span><span class="sxs-lookup"><span data-stu-id="4149b-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="4149b-280">Přímé plnění žádostí o zdroje</span><span class="sxs-lookup"><span data-stu-id="4149b-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="4149b-281">Při generování požadavku na zdroj může projektový manažer odeslat žádost o zdroj pro obecný zdroj výběrem zdroje a následným výběrem **Odeslat žádost**.</span><span class="sxs-lookup"><span data-stu-id="4149b-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Tlačítko Odeslat žádost](media/Resource-Management-image45.png)

<span data-ttu-id="4149b-283">Komentáře ke zdroji mohou být poskytnuty správci zdroje, který požadavek plní.</span><span class="sxs-lookup"><span data-stu-id="4149b-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="4149b-284">Po odeslání požadavku se pole **Stav** pro člena týmu změní na **Odesláno**.</span><span class="sxs-lookup"><span data-stu-id="4149b-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Zadání nepovinných komentářů](media/Resource-Management-image46.png)

<span data-ttu-id="4149b-286">Jakmile správce prostředku splní požadavek, bude obecný člen týmu v mřížce **Všichni členové výmu** nahrazen pojmenovaným zdrojem.</span><span class="sxs-lookup"><span data-stu-id="4149b-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Obecný člen týmu nahrazený pojmenovaným zdrojem v mřížce Všichni členové týmu](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="4149b-288">Použití návrhu zdroje pro žádosti o zdroje</span><span class="sxs-lookup"><span data-stu-id="4149b-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="4149b-289">Namísto přímého rezervování zdroje na základě žádosti o zdroj může správce prostředku navrhnout zdroj projektovému manažerovi.</span><span class="sxs-lookup"><span data-stu-id="4149b-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="4149b-290">Správce prostředku může tuto možnost použít, pokud není k dispozici přesná shoda požadavků.</span><span class="sxs-lookup"><span data-stu-id="4149b-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="4149b-291">Když správce prostředku navrhne zdroj, projektový manažer uvidí, že je pole **Stav** pro obecného člena týmu změněno na **Potřebuje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="4149b-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Stav obecného člena týmu byl změněn na Potřebuje kontrolu](media/Resource-Management-image48.png)

<span data-ttu-id="4149b-293">Chcete-li navržený zdroj zobrazit společně s vizualizací účinku rezervace návrhu, klikněte dvakrát na člena týmu, který má stav **Potřebuje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="4149b-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="4149b-294">Pak vyberte kartu **Navržené zdroje**.</span><span class="sxs-lookup"><span data-stu-id="4149b-294">Then select the **Proposed Resources** tab.</span></span>

![Karta Navržené zdroje](media/Resource-Management-image49.png)

<span data-ttu-id="4149b-296">Vyberte **Přijmout všechny návrhy**, abyste přijali všechny navržené zdroje nebo **Zamítnout všechny návrhy**, abyste je zamítli.</span><span class="sxs-lookup"><span data-stu-id="4149b-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="4149b-297">Přijmete-li navržené zdroje, budou v projektu závazně zarezervovány jako členové týmu a nahradí obecné zdroje.</span><span class="sxs-lookup"><span data-stu-id="4149b-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="4149b-298">Všechny navržené zdroje musíte buď přijmout, nebo zamítnout.</span><span class="sxs-lookup"><span data-stu-id="4149b-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="4149b-299">Nemůžete je částečně přijmout nebo zamítnout.</span><span class="sxs-lookup"><span data-stu-id="4149b-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="4149b-300">Nahrazení zdroje v projektovém týmu</span><span class="sxs-lookup"><span data-stu-id="4149b-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="4149b-301">Projektový manažer někdy musí v projektu nahradit rezervovaného člena týmu.</span><span class="sxs-lookup"><span data-stu-id="4149b-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="4149b-302">Na stránce **Projekty** vyberte na kartě **Tým** zdroj, který vyžaduje náhradu a poté vyberte **Zachovat rezervace**.</span><span class="sxs-lookup"><span data-stu-id="4149b-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="4149b-303">Chcete-li zobrazit projekty, ke kterým je zdroj přiřazen, rozbalte ho.</span><span class="sxs-lookup"><span data-stu-id="4149b-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Zdroj rozbalený pro zobrazení přiřazených projektů](media/Resource-Management-image50.png)

3. <span data-ttu-id="4149b-305">Klepněte pravým tlačítkem myši na projekt a vyberte **Nahradit zdroj**.</span><span class="sxs-lookup"><span data-stu-id="4149b-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="4149b-306">Pokud znáte zdroj, kterým chcete nahradit aktuální zdroj, vyberte ho nebo zadejte jeho název a pak vyberte **Znovu přiřadit**.</span><span class="sxs-lookup"><span data-stu-id="4149b-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Zadání náhradního zdroje](media/Resource-Management-image51.png)

    <span data-ttu-id="4149b-308">Můžete také vyhledat zdroj pomocí následujícího postupu:</span><span class="sxs-lookup"><span data-stu-id="4149b-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="4149b-309">Vyberte **Najít náhradu**.</span><span class="sxs-lookup"><span data-stu-id="4149b-309">Select **Find Substitution**.</span></span>

        ![Hledání náhradního zdroje](media/Resource-Management-image52.png)

        <span data-ttu-id="4149b-311">Pomocník plánování vrátí seznam dostupných náhrad.</span><span class="sxs-lookup"><span data-stu-id="4149b-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="4149b-312">V Pomocníkovi plánování můžete dále filtrovat dostupné zdroje a najít vhodnou náhradu.</span><span class="sxs-lookup"><span data-stu-id="4149b-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Seznam dostupných náhrad](media/Resource-Management-image53.png)

    2. <span data-ttu-id="4149b-314">Chcete-li nahradit zdroj, vyberte zdroj, který chcete a pak vyberte **Nahradit**.</span><span class="sxs-lookup"><span data-stu-id="4149b-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Nahradit vybraný zdroj](media/Resource-Management-image54.png)

    <span data-ttu-id="4149b-316">Rezervace a přiřazení budou nahrazeny novým zdrojem.</span><span class="sxs-lookup"><span data-stu-id="4149b-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Rezervace a přiřazení nahrazené novým zdrojem](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="4149b-318">Spárování rezervací a přiřazení člena týmu</span><span class="sxs-lookup"><span data-stu-id="4149b-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="4149b-319">Pro členy týmu jsou rezervace a přiřazení volně provázené.</span><span class="sxs-lookup"><span data-stu-id="4149b-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="4149b-320">Jinými slovy, zdroje mohou obsahovat přiřazení, ale žádné rezervace, nebo mohou obsahovat rezervace, ale žádná přiřazení.</span><span class="sxs-lookup"><span data-stu-id="4149b-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="4149b-321">V ideálním případě by měly být rezervace a přiřazení zarovnány, aby zdroje měly potvrzenou kapacitu k provádění přiřazení úkolů.</span><span class="sxs-lookup"><span data-stu-id="4149b-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="4149b-322">Rezervace mohou být však založeny na dostupnosti a časování úkolů se může při pokračování projektu změnit.</span><span class="sxs-lookup"><span data-stu-id="4149b-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="4149b-323">Volné spojení rezervací a přiřazení je proto flexibilní.</span><span class="sxs-lookup"><span data-stu-id="4149b-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="4149b-324">PSA obsahuje kartu **Vyrovnání** která projektovým manažerům umožňuje vyrovnat rezervace a přiřazení členů týmů pro projektové týmy.</span><span class="sxs-lookup"><span data-stu-id="4149b-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Karta Vyrovnání](media/Resource-Management-image56.png)

<span data-ttu-id="4149b-326">Karta **Vyrovnání** zobrazuje rezervace a přiřazení až k úrovni jednotlivých přiřazení úkolů pro každého člena týmu.</span><span class="sxs-lookup"><span data-stu-id="4149b-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="4149b-327">Zobrazuje hodiny v buňkách reprezentujících časová období od měsíců po dny.</span><span class="sxs-lookup"><span data-stu-id="4149b-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="4149b-328">Na kartě je také zobrazen celkový čistý součet pro projekt, spolu se sloupcem celkem.</span><span class="sxs-lookup"><span data-stu-id="4149b-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="4149b-329">Pro každý zdroj je na kartě vypočten rozdíl mezi rezervacemi člena týmu a souhrnnými přiřazeními člena týmu.</span><span class="sxs-lookup"><span data-stu-id="4149b-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="4149b-330">V ideálním případě by tento rozdíl měl být 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="4149b-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="4149b-331">Jinými slovy, mezi rezervacemi a přiřazeními by neměl být žádný rozdíl.</span><span class="sxs-lookup"><span data-stu-id="4149b-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="4149b-332">Rozdíly jsou barevné a stínované, aby upozornily na dva stavy:</span><span class="sxs-lookup"><span data-stu-id="4149b-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="4149b-333">**Nedostatečná rezervace** – v případě, že zdroj obsahuje více přiřazení než rezervací, dojde k nedostatatečné rezervaci.</span><span class="sxs-lookup"><span data-stu-id="4149b-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="4149b-334">Vzhledem k tomu, že tato kapacita nebyla rezervována, může projektový manažer tento stav napravit rozšířením rezervací zdroje tak, aby pokryly deficit.</span><span class="sxs-lookup"><span data-stu-id="4149b-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="4149b-335">**Nadbytečné rezervace** – k nadbytečným rezervacím dochází, pokud byl zdroj rezervován do projektu, ale nebyl přiřazen k úkolům.</span><span class="sxs-lookup"><span data-stu-id="4149b-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="4149b-336">Tento stav může být přijatelný v případech, kdy byl zdroj pro projekt rezervován předtím, než došlo k přiřazení úkolu.</span><span class="sxs-lookup"><span data-stu-id="4149b-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="4149b-337">V jiných případech však není plánováno přiřazení zdroje k úkolům.</span><span class="sxs-lookup"><span data-stu-id="4149b-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="4149b-338">V těchto případech by měl projektový manažer zvážit zrušení rezervací zdroje, aby bylo možné použít kapacitu pro jiný projekt.</span><span class="sxs-lookup"><span data-stu-id="4149b-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="4149b-339">Pokud v některých případech zobrazíte čas na vyšší úrovni než denní úroveň (například úroveň měsíce), můžete u zdroje vidět čistý nulový rozdíl (jinými slovy, rezervace = přiřazení).</span><span class="sxs-lookup"><span data-stu-id="4149b-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="4149b-340">Pokud však zobrazíte čas na úrovni týdne, můžete se setkat s tím, že v prvním týdnu jsou přiřazení ve výši nula hodin a rezervace 40 hodin, ale ve druhém týdnu jsou přiřazení 40 hodin a rezervace nula hodin.</span><span class="sxs-lookup"><span data-stu-id="4149b-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="4149b-341">Celkově jsou rezervace a přiřazení vyrovnané, liší se však od jednoho týdne k dalšímu.</span><span class="sxs-lookup"><span data-stu-id="4149b-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="4149b-342">Když zobrazíte čas na vyšších úrovních, buňky na kartě **Vyrovnání** mají indikátor, který vás upozorní, že se na nižších úrovních vyskytují rozdíly.</span><span class="sxs-lookup"><span data-stu-id="4149b-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="4149b-343">Dvojitým kliknutím do buňky můžete provést přiblížení a zobrazit rozdíl.</span><span class="sxs-lookup"><span data-stu-id="4149b-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="4149b-344">Kliknutím pravým tlačítkem myši můžete zobrazení oddálit. Výběrem zdroje a následným použitím ovládacího prvku **Další rozdíl** na panelu nástrojů mřížky můžete přejít na další rozdíl mezi rezervacemi a přiřazeními pro daný zdroj.</span><span class="sxs-lookup"><span data-stu-id="4149b-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="4149b-345">Poté můžete použít ovládací prvek **Předchozí rozdíl** a vrátit se zpět.</span><span class="sxs-lookup"><span data-stu-id="4149b-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="4149b-346">V **Nastavení** také můžete vypnout ukazatel rozdílu a chování navigace.</span><span class="sxs-lookup"><span data-stu-id="4149b-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Ukazatel rozdílu](media/Resource-Management-image57.png)

<span data-ttu-id="4149b-348">Pokud máte pro zdroj přiřazení úkolů, ale nemáte žádné rezervace, vyberte na stránce **Projekty**, na kartě **Vyrovnání** nedostatečnou rezervaci a pak vyberte **Prodloužit rezervaci**.</span><span class="sxs-lookup"><span data-stu-id="4149b-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="4149b-349">Zobrazí se dialogové okno **Prodloužit rezervaci**, ve kterém je uvedena rezervace potřebná k vyřešení nedostatku zdroje.</span><span class="sxs-lookup"><span data-stu-id="4149b-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="4149b-350">Zobrazuje také existující rezervace zdroje ve všech projektech nebo jiných plánovatelných entitách.</span><span class="sxs-lookup"><span data-stu-id="4149b-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="4149b-351">Pokud vyberete **OK** pro vytvoření rezervace pro zdroj bez ohledu na dostupnost zdroje, můžete způsobit přerezervaci.</span><span class="sxs-lookup"><span data-stu-id="4149b-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Dialogové okno Prodloužit rezervaci](media/Resource-Management-image58.png)

<span data-ttu-id="4149b-353">Projektový manažer nebo správce prostředku pak může pomocí Plánovací vývěsky spravovat všechny situace, ve kterých je zdroj přerezervovaný nad svoji kapacitu.</span><span class="sxs-lookup"><span data-stu-id="4149b-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
