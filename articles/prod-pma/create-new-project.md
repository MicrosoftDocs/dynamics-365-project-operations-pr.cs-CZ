---
title: Vytvořit nový projekt
description: Toto téma obsahuje informace o způsobu vytvoření nového projektu.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006233"
---
# <a name="create-a-new-project"></a><span data-ttu-id="6e952-103">Vytvořit nový projekt</span><span class="sxs-lookup"><span data-stu-id="6e952-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e952-104">Pomocí následujících kroků vytvořte nový projekt.</span><span class="sxs-lookup"><span data-stu-id="6e952-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="6e952-105">Na stránce **Správa projektu** vyberte **Nový projekt** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="6e952-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="6e952-106">**Typ projektu:** Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="6e952-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="6e952-107">**Název projektu:** Fáze 2 upgradu XYZ</span><span class="sxs-lookup"><span data-stu-id="6e952-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="6e952-108">**Projektová skupina:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="6e952-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="6e952-109">**ID projektové smlouvy:** 00000002</span><span class="sxs-lookup"><span data-stu-id="6e952-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="6e952-110">Vyberte příkaz **Vytvořit projekt**.</span><span class="sxs-lookup"><span data-stu-id="6e952-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="6e952-111">Přiřazení zdroje k projektu</span><span class="sxs-lookup"><span data-stu-id="6e952-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="6e952-112">Na stránce **Pracovníci** vyberte v seznamu **Pracovníci** záznam pro toho pracovníka, kterému jste předtím přiřadili kompetence, a otevřete záznam pracovníka.</span><span class="sxs-lookup"><span data-stu-id="6e952-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="6e952-113">V podokně akcí na kartě **Projekt** vyberte ve skupině **Nastavení** příkaz **Přiřadit projekty**.</span><span class="sxs-lookup"><span data-stu-id="6e952-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="6e952-114">Na stránce **Přiřazení projektů ověření prostředku** na kartě **Projekty** v poli **Přidat projekt k vybraným projektům** filtrujte podle projektu **Fáze 2 upgradu XYZ**.</span><span class="sxs-lookup"><span data-stu-id="6e952-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="6e952-115">V podokně **Zbývající projekty** vyberte projekt a poté jej kliknutím na tlačítko se šipkou přidejte do podokna **Vybrané projekty**.</span><span class="sxs-lookup"><span data-stu-id="6e952-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="6e952-116">Můžete také podle potřeby přiřadit kategorie ke zdroji.</span><span class="sxs-lookup"><span data-stu-id="6e952-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="6e952-117">Typ kategorie je buď **Náklady** nebo **Výnosy**.</span><span class="sxs-lookup"><span data-stu-id="6e952-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="6e952-118">Typ kategorie určuje vaše organizace.</span><span class="sxs-lookup"><span data-stu-id="6e952-118">The category type is determined by your organization.</span></span> <span data-ttu-id="6e952-119">Pokud zdroji nejsou přiřazeny žádné kategorie, vyhledá Finance výchozí kategorii na základě hodinových cen nákladů a výnosů.</span><span class="sxs-lookup"><span data-stu-id="6e952-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="6e952-120">Nastavení charakteristik projektového zdroje a role</span><span class="sxs-lookup"><span data-stu-id="6e952-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="6e952-121">Manažer projektu může použít funkci projektového zajišťování zdrojů k vytvoření rolí, které jsou pro projekt vyžadovány.</span><span class="sxs-lookup"><span data-stu-id="6e952-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="6e952-122">Role lze použít, pokud jsou potvrzené zdroje stále neznámé, když probíhá rezervace zdrojů.</span><span class="sxs-lookup"><span data-stu-id="6e952-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="6e952-123">Role lze dočasně rezervovat jako plánované zdroje, abyste mohli pokračovat ve fázích plánování projektu.</span><span class="sxs-lookup"><span data-stu-id="6e952-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="6e952-124">[![Příklad role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="6e952-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="6e952-125">**Scénář:** Contoso byla najata k provedení projektu Čas a materiál, který má schválenou chartu projektu.</span><span class="sxs-lookup"><span data-stu-id="6e952-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="6e952-126">Nižší projektový manažer stále dokončuje rozsah projektu.</span><span class="sxs-lookup"><span data-stu-id="6e952-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="6e952-127">Správce prostředků aktuálně identifikuje konkrétní zdroje, které budou vyhrazeny pro práci na novém projektu.</span><span class="sxs-lookup"><span data-stu-id="6e952-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="6e952-128">Vzhledem ke kritické povaze projektu si sponzor projektu požádal o přidělení role vyššího projektového manažera.</span><span class="sxs-lookup"><span data-stu-id="6e952-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="6e952-129">Správce zdrojů musí získat nový zdroj a definovat roli v systému v případě, že nižší projektový manažer vyžaduje během plánování projektu informace o zdroji.</span><span class="sxs-lookup"><span data-stu-id="6e952-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="6e952-130">Následující kroky ukazují, jak může správce zdrojů nastavit roli vyššího projektového manažera a asociovat s ním charakteristiky zdrojů.</span><span class="sxs-lookup"><span data-stu-id="6e952-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="6e952-131">Později lze roli použít k vyhledání dostupných zdrojů, které odpovídají požadovaným kompetencím zdrojů.</span><span class="sxs-lookup"><span data-stu-id="6e952-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="6e952-132">Na stránce **Nastavení rolí** vyberte **Nová** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="6e952-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="6e952-133">**ID role:** Vyšší projektový manažer</span><span class="sxs-lookup"><span data-stu-id="6e952-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="6e952-134">**ID role:** Vyšší projektový manažer</span><span class="sxs-lookup"><span data-stu-id="6e952-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="6e952-135">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="6e952-135">Select **Create**.</span></span>
3. <span data-ttu-id="6e952-136">Vyberte roli **Vyšší projektový manažer** a poté vyberte **Konfigurovat charakteristiky**.</span><span class="sxs-lookup"><span data-stu-id="6e952-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="6e952-137">V poli **Typ charakteristiky** vyberte **Dovednost**.</span><span class="sxs-lookup"><span data-stu-id="6e952-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="6e952-138">V poli **Dostupné charakteristiky** zadejte hledanou dovednost.</span><span class="sxs-lookup"><span data-stu-id="6e952-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="6e952-139">V poli **Typ charakteristiky** vyberte **Certifikát**.</span><span class="sxs-lookup"><span data-stu-id="6e952-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="6e952-140">V poli **Dostupné charakteristiky** zadejte hledaný typ certifikátu.</span><span class="sxs-lookup"><span data-stu-id="6e952-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="6e952-141">Přiřazení projektového zdroje k projektu</span><span class="sxs-lookup"><span data-stu-id="6e952-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="6e952-142">Na stránce **Všechny projekty** vyberte projekt **Fáze 2 upgradu XYZ**.</span><span class="sxs-lookup"><span data-stu-id="6e952-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="6e952-143">Na kartě **Projektový tým a plánování** vyberte možnost **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="6e952-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="6e952-144">V poli **Role** vyberte **Člen týmu**.</span><span class="sxs-lookup"><span data-stu-id="6e952-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="6e952-145">Vyberte **Rezervovat z kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="6e952-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="6e952-146">Na stránce **Dostupnost zdrojů** vyberte možnost **Nastavení zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="6e952-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="6e952-147">Na stránce **Upravit nastavení zobrazení** zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="6e952-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="6e952-148">**Formát pro zobrazení rozsahu dat:** Den</span><span class="sxs-lookup"><span data-stu-id="6e952-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="6e952-149">**Zobrazit popisy dostupnosti:** Ano</span><span class="sxs-lookup"><span data-stu-id="6e952-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="6e952-150">**Zobrazit zbývající kapacitu:** Ano</span><span class="sxs-lookup"><span data-stu-id="6e952-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="6e952-151">V seznamu zdrojů vyberte zdroj.</span><span class="sxs-lookup"><span data-stu-id="6e952-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="6e952-152">Vyberte **Závazná rezervace** a **Plná kapacita**.</span><span class="sxs-lookup"><span data-stu-id="6e952-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="6e952-153">Přiřazení zdroje k výchozí roli</span><span class="sxs-lookup"><span data-stu-id="6e952-153">Assign a resource to a default role</span></span>

<span data-ttu-id="6e952-154">Chcete-li pomoci správcům projektů nebo zdrojů s procházením hierarchie zdrojů, které lze pro projekt rezervovat.</span><span class="sxs-lookup"><span data-stu-id="6e952-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="6e952-155">Můžete přiřadit výchozí roli k existujícímu zdroji nebo nově získanému zdroji.</span><span class="sxs-lookup"><span data-stu-id="6e952-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="6e952-156">Například když byl Daniel najat, měl zkušenosti a dovednosti, aby mohl plnit roli obchodního analytika.</span><span class="sxs-lookup"><span data-stu-id="6e952-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="6e952-157">Správce zdrojů přidělil tuto Danielovi jako výchozí.</span><span class="sxs-lookup"><span data-stu-id="6e952-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="6e952-158">Proto správce zdrojů přidal Daniela do fondu obchodních analytiků, kteří jsou k dispozici pro práci na projektech.</span><span class="sxs-lookup"><span data-stu-id="6e952-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="6e952-159">Během rezervace zdrojů mohou projektoví manažeři filtrovat zdroje rolí, které jsou k dispozici pro práci na projektech.</span><span class="sxs-lookup"><span data-stu-id="6e952-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="6e952-160">Tuto informaci mohou použít jako jedno z kritérií při provádění multikriteriální rozhodovací analýzy během plnění zdrojů.</span><span class="sxs-lookup"><span data-stu-id="6e952-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="6e952-161">Mohou také přidat do filtru další charakteristiky zdrojů, aby vyhledali zdroje, které mají specifické dovednosti, vzdělání a zkušenosti pro daný projekt.</span><span class="sxs-lookup"><span data-stu-id="6e952-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="6e952-162">**Scénář:** Byl zahájen schválený projekt a role vyššího projektového manažera byla rezervována jako plánovaný zdroj během fáze plánování projektu.</span><span class="sxs-lookup"><span data-stu-id="6e952-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="6e952-163">Správce prostředků nyní získal zdroj ke splnění role vyššího projektového manažera.</span><span class="sxs-lookup"><span data-stu-id="6e952-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="6e952-164">Na stránce **Seznam zdrojů** vyberte položku **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="6e952-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="6e952-165">Na stránce **Role zdroje** vyberte **Nová** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="6e952-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="6e952-166">**Platí od:** Zadejte aktuální datum.</span><span class="sxs-lookup"><span data-stu-id="6e952-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="6e952-167">**Vypršení platnosti:** Zadejte **Nikdy**.</span><span class="sxs-lookup"><span data-stu-id="6e952-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="6e952-168">**Role:** Zadejte **Vyšší projektový manažer**.</span><span class="sxs-lookup"><span data-stu-id="6e952-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="6e952-169">Vyberte tlačítko **Uložit** a potom zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6e952-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="6e952-170">Na kartě **Kompetence** přidejte dovednost **Správa projektu** a certifikát **PMP**.</span><span class="sxs-lookup"><span data-stu-id="6e952-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]