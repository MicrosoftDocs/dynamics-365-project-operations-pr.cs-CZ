---
title: Aktualizace Project Operations v prostředí Finance
description: Tohle téma poskytuje informace, jak aktualizovat Project Operations v prostředí Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011048"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="e1c46-103">Aktualizace Project Operations v prostředí Finance</span><span class="sxs-lookup"><span data-stu-id="e1c46-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="e1c46-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="e1c46-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="e1c46-105">Tohle téma poskytuje informace, jak aktualizovat Dynamics 365 Project Operations v prostředí Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="e1c46-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="e1c46-106">K aktualizaci Project Operations na Update 5 (UR5) jsou vyžadovány tři postupy:</span><span class="sxs-lookup"><span data-stu-id="e1c46-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="e1c46-107">Importujte balíček do projektu náhledu</span><span class="sxs-lookup"><span data-stu-id="e1c46-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="e1c46-108">Nainstaluje aktualizaci</span><span class="sxs-lookup"><span data-stu-id="e1c46-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="e1c46-109">Aktualizujte prostředí Dataverse</span><span class="sxs-lookup"><span data-stu-id="e1c46-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="e1c46-110">Importujte balíček do projektu LCS</span><span class="sxs-lookup"><span data-stu-id="e1c46-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="e1c46-111">Přihlaste se do [Lifecycle Services (LCS)](https://lcs.dynamics.com/) jako vlastník projektu nebo manažer prostředí.</span><span class="sxs-lookup"><span data-stu-id="e1c46-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="e1c46-112">Ze seznamu projektů vyberte svůj projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="e1c46-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="e1c46-113">Na stránce **Projekt** ve skupině **Prostředí** otevřete prostředí, které chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="e1c46-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="e1c46-114">Ověřte, že prostředí běží.</span><span class="sxs-lookup"><span data-stu-id="e1c46-114">Verify that the environment is running.</span></span> <span data-ttu-id="e1c46-115">Pokud není spuštěno, spusťte prostředí.</span><span class="sxs-lookup"><span data-stu-id="e1c46-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="e1c46-116">V části **Nová verze** pod **Dostupné aktualizace** vyberte **Zobrazit aktualizaci** u 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="e1c46-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Tlačítko Zobrazit aktualizaci](media/view-update.png)

6. <span data-ttu-id="e1c46-118">Na stránce **Binární aktualizace** vyberte možnost **Uložit balíček**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="e1c46-119">Na stránce **Zkontrolovat a uložit aktualizace** vyberte možnost **Uložit balíček**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="e1c46-120">V podokně **Uložit balíček do knihovny prostředků**, které se otevře, zadejte název balíčku a poté vyberte **Uložit balíček**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="e1c46-121">Když LCS dokončí ukládání balíčku, aktivuje se tlačítko **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="e1c46-122">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-122">Select **Done**.</span></span> <span data-ttu-id="e1c46-123">LCS ověří balíček.</span><span class="sxs-lookup"><span data-stu-id="e1c46-123">LCS will verify the package.</span></span> <span data-ttu-id="e1c46-124">Ověření může trvat několik minut nebo až hodinu.</span><span class="sxs-lookup"><span data-stu-id="e1c46-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="e1c46-125">Nainstalujte aktualizaci balíčku</span><span class="sxs-lookup"><span data-stu-id="e1c46-125">Apply the package update</span></span>

1. <span data-ttu-id="e1c46-126">V LCS na stránce **Podrobnosti o prostředí** vyberte **Udržovat** > **Použít aktualizace**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="e1c46-127">Ze seznamu vyberte balíček, který jste dříve uložili, a poté vyberte **Použít**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="e1c46-128">Vyberte **Ano** k potvrzení, že chcete balíček nasadit.</span><span class="sxs-lookup"><span data-stu-id="e1c46-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Dialogové okno Potvrdit nasazení balíčku](media/confirm-package-deployment.png)

4. <span data-ttu-id="e1c46-130">Vyberte **Ano** k potvrzení, že chcete aplikaci aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="e1c46-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Dialogové okno Potvrdit aktualizaci aplikace](media/confirm-application-update.png)

<span data-ttu-id="e1c46-132">Spustí se nasazení a aktualizace aplikace.</span><span class="sxs-lookup"><span data-stu-id="e1c46-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="e1c46-133">Na stránce **Podrobnosti o prostředí** se v pravém horním rohu aktualizuje stav prostředí **Servis**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="e1c46-134">Aktualizace bude dokončena přibližně za dvě hodiny.</span><span class="sxs-lookup"><span data-stu-id="e1c46-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="e1c46-135">Informace o vydání aplikace se aktualizují na **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** a stav prostředí se aktualizuje na **Nasazeno**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="e1c46-136">Aktualizace prostředí Dataverse</span><span class="sxs-lookup"><span data-stu-id="e1c46-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="e1c46-137">Přihlaste se k [centru pro správu Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="e1c46-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="e1c46-138">V seznamu vyhledejte a otevřete prostředí, které jste použili k instalaci Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e1c46-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="e1c46-139">Na stránce **Prostředí** vyberte **Zdroj** > **Aplikace Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="e1c46-140">V seznamu vyhledejte **Microsoft Dynamics 365 Project Operations** a ve sloupci **Stav** vyberte **Aktualizace je k dispozici**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="e1c46-141">Zaškrtněte **Souhlasím s podmínkami služby** a poté vyberte **Aktualizace**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="e1c46-142">Bude nainstalována nejnovější verze řešení.</span><span class="sxs-lookup"><span data-stu-id="e1c46-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="e1c46-143">Po dokončení instalace budete mít nainstalovanou verzi 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="e1c46-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="e1c46-144">Konfigurace nových funkcí</span><span class="sxs-lookup"><span data-stu-id="e1c46-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="e1c46-145">Aktivace mapování duálního zápisu</span><span class="sxs-lookup"><span data-stu-id="e1c46-145">Enable dual-write mapping</span></span>

<span data-ttu-id="e1c46-146">Po dokončení aktualizace v prostředí Finance a Dataverse prostředí můžete povolit požadovaná mapování duálního zápisu.</span><span class="sxs-lookup"><span data-stu-id="e1c46-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="e1c46-147">K povolení mapování duálního zápisu proveďte následující postupy.</span><span class="sxs-lookup"><span data-stu-id="e1c46-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="e1c46-148">Aktualizujte nastavení zabezpečení v prostředí Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="e1c46-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="e1c46-149">Aktualizace datových entit</span><span class="sxs-lookup"><span data-stu-id="e1c46-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="e1c46-150">Aktualizujte a spusťte mapování duálního zápisu</span><span class="sxs-lookup"><span data-stu-id="e1c46-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="e1c46-151">Aktualizujte nastavení zabezpečení v prostředí Dataverse</span><span class="sxs-lookup"><span data-stu-id="e1c46-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="e1c46-152">Následující aktualizace bezpečnostních oprávnění pro entity jsou vyžadovány jako součást aktualizace UR5.</span><span class="sxs-lookup"><span data-stu-id="e1c46-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="e1c46-153">V prostředí Dataverse přejděte do **Nastavení** a ve skupině **Systém** vyberte **Zabezpečení**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Nastavení prostředí Dataverse](media/Picture21.png)

2. <span data-ttu-id="e1c46-155">Vyberte **Role zabezpečení**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="e1c46-156">Ze seznamu rolí vyberte **uživatel aplikace duálního zápisu** a vyberte kartu **Vlastní entity**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="e1c46-157">Ověřte, zda role má oprávnění **Číst** a **Připojit k** pro:</span><span class="sxs-lookup"><span data-stu-id="e1c46-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="e1c46-158">**Typ směnného kurzu měny**</span><span class="sxs-lookup"><span data-stu-id="e1c46-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="e1c46-159">**Účtová osnova**</span><span class="sxs-lookup"><span data-stu-id="e1c46-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="e1c46-160">**Fiskální kalendář**</span><span class="sxs-lookup"><span data-stu-id="e1c46-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="e1c46-161">**Registr**</span><span class="sxs-lookup"><span data-stu-id="e1c46-161">**Ledger**</span></span>

5. <span data-ttu-id="e1c46-162">Po aktualizaci role zabezpečení přejděte na **Nastavení** > **Zabezpečení** > **Týmy**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="e1c46-163">Ověřte, že role **uživatel aplikace dvojitého zápisu** byla na tým aplikována.</span><span class="sxs-lookup"><span data-stu-id="e1c46-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="e1c46-164">Aktualizujte datové entity z aktualizace</span><span class="sxs-lookup"><span data-stu-id="e1c46-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="e1c46-165">Ve prostředí Finance otevřete pracovní prostor **Správa dat** a poté otevřete stránku **Parametry rámce**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="e1c46-166">Na kartě **Nastavení entity** kartu vyberte **Obnovit seznam entit**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="e1c46-167">Vyberte **Zavřít** pro potvrzení aktualizace entity.</span><span class="sxs-lookup"><span data-stu-id="e1c46-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="e1c46-168">Tento proces zabere přibližně 20 minut.</span><span class="sxs-lookup"><span data-stu-id="e1c46-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="e1c46-169">Až bude aktualizace dokončena, budete upozorněni.</span><span class="sxs-lookup"><span data-stu-id="e1c46-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="e1c46-170">Aktualizace mapování duálního zápisu</span><span class="sxs-lookup"><span data-stu-id="e1c46-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="e1c46-171">V pracovním prostoru **Správa dat** vyberte **Duální zápis**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="e1c46-172">Vyberte **Použít řešení**, vyberte obě řešení v seznamu a poté vyberte **Použít**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="e1c46-173">Na stránce **Duální zápis** vyberte následující mapové tabulky a poté vyberte **Stop**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="e1c46-174">**Skutečné hodnoty integrace Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="e1c46-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="e1c46-175">**Kategorie výdajů projektu integrace Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="e1c46-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="e1c46-176">**Entita exportu skutečných hodnot výdajů projektu integrace Project Operations (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="e1c46-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="e1c46-177">Na stránce **Verze tabulky mapy** použijte novou verzi mapy na každou ze tří entit.</span><span class="sxs-lookup"><span data-stu-id="e1c46-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="e1c46-178">Na stránce **Duální zápis** vyberte příkaz Spustit a restartujte mapy.</span><span class="sxs-lookup"><span data-stu-id="e1c46-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="e1c46-179">Ze seznamu map vyberte mapu **Registr (msdyn_ledgers)** se všemi předpoklady a zaškrtněte **Počáteční synchronizace**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="e1c46-180">V poli **Předloha pro počáteční synchronizaci** vyberte **Aplikace Finance and Operations** a poté vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="e1c46-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Synchronizace mapy registru](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]