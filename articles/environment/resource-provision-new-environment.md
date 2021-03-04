---
title: Zřízení nového prostředí
description: Toto téma poskytuje informace o zřízení nového prostředí Project Operations.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09af2a7693c45d1d0b9c75420d018cc50d2cc0fa
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727782"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="8ca84-103">Zřízení nového prostředí</span><span class="sxs-lookup"><span data-stu-id="8ca84-103">Provision a new environment</span></span>

<span data-ttu-id="8ca84-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="8ca84-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8ca84-105">Toto téma poskytuje informace o zřízování nového prostředí Dynamics 365 Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě.</span><span class="sxs-lookup"><span data-stu-id="8ca84-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="8ca84-106">Povolení automatického zřizování Project Operations v projektu LCS</span><span class="sxs-lookup"><span data-stu-id="8ca84-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="8ca84-107">Pomocí následujících kroků povolíte tok automatického zřizování Project Operations pro váš projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="8ca84-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="8ca84-108">Přejděte do [LCS](https://lcs.dynamics.com/v2) a vyberte dlaždici **Správa funkce náhledu**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="8ca84-109">V seznamu **Funkce Preview** vyberte **Funkce Project Operations** a poté výběrem možnosti **Povolit funkci verze Preview** povolte aplikaci Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8ca84-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="8ca84-110">Tento krok se provádí pouze jednou za projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="8ca84-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="8ca84-111">Zřízení prostředí Project Operations</span><span class="sxs-lookup"><span data-stu-id="8ca84-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="8ca84-112">Otevřete nové [demo prostředí Dynamics 365 Finance](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) nebo nasazení [sandboxu / produkčního prostředí](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="8ca84-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="8ca84-113">Projděte jednotlivé obrazovky průvodce **Zřízení prostředí**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="8ca84-114">Zkontrolujte, zda je vybrána verze aplikace 10.0.13 nebo vyšší.</span><span class="sxs-lookup"><span data-stu-id="8ca84-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="8ca84-115">Chcete-li zřídit Project Operations, vyberte v části **Pokročilé nastavení** položku **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="8ca84-116">Povolte **Nastavení Common Data Service** výběrem **Ano** a poté zadejte informace do požadovaných polí:</span><span class="sxs-lookup"><span data-stu-id="8ca84-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="8ca84-117">Jméno</span><span class="sxs-lookup"><span data-stu-id="8ca84-117">Name</span></span>
  - <span data-ttu-id="8ca84-118">Oblast</span><span class="sxs-lookup"><span data-stu-id="8ca84-118">Region</span></span>
  - <span data-ttu-id="8ca84-119">Jazyk</span><span class="sxs-lookup"><span data-stu-id="8ca84-119">Language</span></span>
  - <span data-ttu-id="8ca84-120">Měna</span><span class="sxs-lookup"><span data-stu-id="8ca84-120">Currency</span></span>
 
5. <span data-ttu-id="8ca84-121">V poli **Šablona Common Data Service** vyberte **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="8ca84-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="8ca84-122">Vyberte typ prostředí pro vaše nasazení.</span><span class="sxs-lookup"><span data-stu-id="8ca84-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="8ca84-123">Zkušební verze založená na předplatném vám umožní nasadit prostředí CDS po dobu 30 dnů.</span><span class="sxs-lookup"><span data-stu-id="8ca84-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Nastavení nasazení](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="8ca84-125">Výběrem možnosti **Souhlasím** potvrďte podmínky služby a poté se výběrem možnosti **Hotovo** vraťte do nastavení nasazení.</span><span class="sxs-lookup"><span data-stu-id="8ca84-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Souhlas s nasazením](./media/2DeploymentConsent.png)

7. <span data-ttu-id="8ca84-127">Volitelné – použití ukázkových dat na prostředí.</span><span class="sxs-lookup"><span data-stu-id="8ca84-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="8ca84-128">Přejdete do **Pokročilé nastavení**, vyberte **Přizpůsobte konfiguraci databáze SQL** a nastavte **Určete datovou sadu pro databázi aplikací** na **Ukázka**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="8ca84-129">Vyplňte zbývající požadovaná pole v průvodci a potvrďte nasazení.</span><span class="sxs-lookup"><span data-stu-id="8ca84-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="8ca84-130">Čas zřízení prostředí se liší v závislosti na typu prostředí.</span><span class="sxs-lookup"><span data-stu-id="8ca84-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="8ca84-131">Zřizování může trvat až šest hodin.</span><span class="sxs-lookup"><span data-stu-id="8ca84-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="8ca84-132">Po úspěšném dokončení nasazení se prostředí zobrazí jako **Nasazeno**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="8ca84-133">Chcete-li potvrdit, že se prostředí úspěšně nasadilo, vyberte **Přihlásit se** a potvrďte přihlášením do prostředí.</span><span class="sxs-lookup"><span data-stu-id="8ca84-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Podrobnosti prostředí ](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="8ca84-135">Použití aktualizací v prostředí Finance</span><span class="sxs-lookup"><span data-stu-id="8ca84-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="8ca84-136">Project Operations vyžaduje prostředí Finance s verzí aplikace **10.0.13 (10.0.569.20009)** nebo vyšší.</span><span class="sxs-lookup"><span data-stu-id="8ca84-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="8ca84-137">K získání této verze možná budete muset na svém prostředí Finance použít aktualizace kvality.</span><span class="sxs-lookup"><span data-stu-id="8ca84-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="8ca84-138">V LCS, na stránce **Podrobnosti o prostředí** v sekci **Dostupné aktualizace** vyberte možnost **Zobrazit aktualizaci**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Zobrazení aktualizací](./media/5ViewUpdates.png)

2. <span data-ttu-id="8ca84-140">Na stránce **Binární aktualizace** vyberte možnost **Uložit balíček.**</span><span class="sxs-lookup"><span data-stu-id="8ca84-140">On the **Binary updates** page, select **Save package.**</span></span>

![Uložení balíčku](./media/6SavePackage.png)

3. <span data-ttu-id="8ca84-142">Klikněte na položku **Vybrat vše** a pak vyberte příkaz **Uložit balíček**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-142">Click **Select all** and then select **Save package**.</span></span>

![Kontrola a ukládání aktualizací](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="8ca84-144">Zadejte název a popis balíčku a poté vyberte příkaz **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="8ca84-145">Tento proces může nějakou dobu trvat (v závislosti na rychlosti připojení k internetu).</span><span class="sxs-lookup"><span data-stu-id="8ca84-145">Depending on the internet connection, this process might take some time.</span></span>

![Nahrání balíčku do knihovny prostředků](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="8ca84-147">Po uložení balíčku vyberte možnost **Hotovo** a uložte tento balíček do knihovny prostředků ve vašem projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="8ca84-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="8ca84-148">Uložení a ověření balíčku může trvat až 15 minut.</span><span class="sxs-lookup"><span data-stu-id="8ca84-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="8ca84-149">Chcete-li použít aktualizaci, přejděte na stránku **Podrobnosti o prostředí** v LCS a vyberte příkaz **Údržba** > **Použít aktualizace**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Údržba prostředí](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="8ca84-151">V seznamu aktualizací vyberte balíček, který jste vytvořili, a vyberte příkaz **Použít**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Instalace aktualizací](./media/10ApplyUpdates.png)

<span data-ttu-id="8ca84-153">Údržba prostředí bude nějakou dobu trvat.</span><span class="sxs-lookup"><span data-stu-id="8ca84-153">Environment servicing will take some time.</span></span> <span data-ttu-id="8ca84-154">Po dokončení se prostředí vrátí do nasazeného stavu.</span><span class="sxs-lookup"><span data-stu-id="8ca84-154">After it is complete, the environment will return to a deployed state.</span></span>

![Nasazené prostředí](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="8ca84-156">Vytvoření připojení s duálním zápisem</span><span class="sxs-lookup"><span data-stu-id="8ca84-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="8ca84-157">V projektu LCS přejděte na stránku **Podrobnosti o prostředí**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="8ca84-158">V části **Informace o prostředí Common Data Service** vyberte možnost **Odkaz na CDS pro aplikace**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="8ca84-159">Po vytvoření odkazu vyberte znovu možnost **Odkaz na CDS pro aplikace**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="8ca84-160">Budete přesměrováni na duální zápis ve Finance.</span><span class="sxs-lookup"><span data-stu-id="8ca84-160">You will be redirected to Dual Write in Finance.</span></span>

![Odkaz na CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="8ca84-162">Výběrem položky **Použít řešení** získáte přístup k entitám, které budou mapovány v integraci.</span><span class="sxs-lookup"><span data-stu-id="8ca84-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Použít řešení](./media/13ApplySolutions.png)

5. <span data-ttu-id="8ca84-164">Vyberte obě řešení, **Mapa entit duálního zápisu Dynamics 365 Finance and Operations** a **Mapa entit duálního zápisu Dynamics 365 Project Operations** a potom vyberte **Použít**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Potvrzení řešení](./media/14ConfirmSolutions.png)

<span data-ttu-id="8ca84-166">Poté, co je řešení použito, se na prostředí použijí entity duálního zápisu.</span><span class="sxs-lookup"><span data-stu-id="8ca84-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Použití řešení](./media/15ApplyingSolutions.png)

<span data-ttu-id="8ca84-168">Po použití entit se v prostředí zobrazí všechna dostupná mapování.</span><span class="sxs-lookup"><span data-stu-id="8ca84-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mapy duálního zápisu](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="8ca84-170">Po aktualizaci aktualizujte datové entity</span><span class="sxs-lookup"><span data-stu-id="8ca84-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="8ca84-171">Ve Finance přejděte do pracovního prostoru **Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-171">In Finance, go to the **Data management** workspace.</span></span>

![Pracovní prostor správy dat](./media/16DataManagement.png)

2. <span data-ttu-id="8ca84-173">Vyberte dlaždici **Parametry architektury**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-173">Select the **Framework parameters** tile.</span></span>

![Parametry architektury](./media/17FrameworkParameters.png)

3. <span data-ttu-id="8ca84-175">Na stránce **Nastavení entity** vyberte možnost **Aktualizovat seznam entit**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Aktualizovat seznam entit](./media/18RefreshEntityList.png)

<span data-ttu-id="8ca84-177">Aktualizace bude trvat přibližně 20 minut.</span><span class="sxs-lookup"><span data-stu-id="8ca84-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="8ca84-178">Po dokončení obdržíte upozornění.</span><span class="sxs-lookup"><span data-stu-id="8ca84-178">You will receive an alert when it is complete.</span></span>

![Potvrzení aktualizace](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="8ca84-180">Aktualizovat nastavení zabezpečení v Project Operations na Dataverse</span><span class="sxs-lookup"><span data-stu-id="8ca84-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="8ca84-181">Přejděte na Project Operations v prostředí Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8ca84-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="8ca84-182">Přejděte do části **Nastavení** > **Zabezpečení** > **Role zabezpečení**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="8ca84-183">Na stránce **Role zabezpečení** v seznamu rolí vyberte **uživatel aplikace dual-write** a vyberte kartu **Vlastní entity**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="8ca84-184">Ověřte, zda role má oprávnění **Číst** a **Připojit k** pro:</span><span class="sxs-lookup"><span data-stu-id="8ca84-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="8ca84-185">**Typ směnného kurzu měny**</span><span class="sxs-lookup"><span data-stu-id="8ca84-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="8ca84-186">**Účtová osnova**</span><span class="sxs-lookup"><span data-stu-id="8ca84-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="8ca84-187">**Fiskální kalendář**</span><span class="sxs-lookup"><span data-stu-id="8ca84-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="8ca84-188">**Registr**</span><span class="sxs-lookup"><span data-stu-id="8ca84-188">**Ledger**</span></span>

5. <span data-ttu-id="8ca84-189">Po aktualizaci role zabezpečení přejděte na **Nastavení** > **Bezpečnostní** > **týmy** a vyberte výchozí tým v zobrazení týmu **Místní vlastník firmy**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="8ca84-190">Vyberte **Správa rolí** a ověřte, že bezpečnostní oprávnění **uživatel aplikace dual-write** je tomuto týmu přiděleno.</span><span class="sxs-lookup"><span data-stu-id="8ca84-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="8ca84-191">Spuštění mapování duálního zápisu Project Operations</span><span class="sxs-lookup"><span data-stu-id="8ca84-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="8ca84-192">V projektu LCS přejděte na stránku **Podrobnosti o prostředí**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="8ca84-193">V části **Informace o prostředí Common Data Service** vyberte možnost **Odkaz na CDS pro aplikace**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="8ca84-194">Poté, co vyberete odkaz, budete přesměrováni na seznam entit v mapováních.</span><span class="sxs-lookup"><span data-stu-id="8ca84-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="8ca84-195">Spusťte mapování podle popisu v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="8ca84-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="8ca84-196">Postupujte podle níže uvedené sekvence.</span><span class="sxs-lookup"><span data-stu-id="8ca84-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="8ca84-197">**Mapování entity**</span><span class="sxs-lookup"><span data-stu-id="8ca84-197">**Entity Map**</span></span> | <span data-ttu-id="8ca84-198">**Aktualizovat entity**</span><span class="sxs-lookup"><span data-stu-id="8ca84-198">**Refresh entity**</span></span> | <span data-ttu-id="8ca84-199">**Počáteční synchronizace**</span><span class="sxs-lookup"><span data-stu-id="8ca84-199">**Initial sync**</span></span> | <span data-ttu-id="8ca84-200">**Předloha pro počáteční synchronizaci**</span><span class="sxs-lookup"><span data-stu-id="8ca84-200">**Master for initial sync**</span></span> | <span data-ttu-id="8ca84-201">**Spustit požadavky**</span><span class="sxs-lookup"><span data-stu-id="8ca84-201">**Run prerequisites**</span></span> | <span data-ttu-id="8ca84-202">**Počáteční synchronizace požadavků**</span><span class="sxs-lookup"><span data-stu-id="8ca84-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="8ca84-203">**Role zdrojů projektu pro všechny společnosti (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="8ca84-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="8ca84-204">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-204">No</span></span> | <span data-ttu-id="8ca84-205">Ano</span><span class="sxs-lookup"><span data-stu-id="8ca84-205">Yes</span></span> | <span data-ttu-id="8ca84-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8ca84-206">Common Data Service</span></span> | <span data-ttu-id="8ca84-207">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-207">No</span></span> | <span data-ttu-id="8ca84-208">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-208">N\A</span></span> |
| <span data-ttu-id="8ca84-209">**Právnické osoby (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="8ca84-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="8ca84-210">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-210">No</span></span> | <span data-ttu-id="8ca84-211">Ano</span><span class="sxs-lookup"><span data-stu-id="8ca84-211">Yes</span></span> | <span data-ttu-id="8ca84-212">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8ca84-212">Finance and Operations apps</span></span> | <span data-ttu-id="8ca84-213">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-213">No</span></span> | <span data-ttu-id="8ca84-214">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-214">N\A</span></span> |
| <span data-ttu-id="8ca84-215">**Registr (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="8ca84-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="8ca84-216">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-216">No</span></span> | <span data-ttu-id="8ca84-217">Ano</span><span class="sxs-lookup"><span data-stu-id="8ca84-217">Yes</span></span> | <span data-ttu-id="8ca84-218">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8ca84-218">Finance and Operations apps</span></span> | <span data-ttu-id="8ca84-219">Ano</span><span class="sxs-lookup"><span data-stu-id="8ca84-219">Yes</span></span> | <span data-ttu-id="8ca84-220">Ano, aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8ca84-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="8ca84-221">**Skutečné hodnoty integrace Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="8ca84-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="8ca84-222">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-222">No</span></span> | <span data-ttu-id="8ca84-223">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-223">No</span></span> | <span data-ttu-id="8ca84-224">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-224">N\A</span></span> | <span data-ttu-id="8ca84-225">Ano</span><span class="sxs-lookup"><span data-stu-id="8ca84-225">Yes</span></span> | <span data-ttu-id="8ca84-226">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-226">No</span></span> |
| <span data-ttu-id="8ca84-227">**Řádky smlouvy založené na projektu (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="8ca84-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="8ca84-228">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-228">No</span></span> | <span data-ttu-id="8ca84-229">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-229">No</span></span> | <span data-ttu-id="8ca84-230">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-230">N\A</span></span> | <span data-ttu-id="8ca84-231">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-231">No</span></span> | <span data-ttu-id="8ca84-232">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-232">No</span></span> |
| <span data-ttu-id="8ca84-233">**Entita integrace pro vztahy projektových transakcí (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="8ca84-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="8ca84-234">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-234">No</span></span> | <span data-ttu-id="8ca84-235">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-235">No</span></span> | <span data-ttu-id="8ca84-236">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-236">N\A</span></span> | <span data-ttu-id="8ca84-237">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-237">No</span></span> | <span data-ttu-id="8ca84-238">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-238">N\A</span></span> |
| <span data-ttu-id="8ca84-239">**Milníky řádku smlouvy integrace Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="8ca84-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="8ca84-240">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-240">No</span></span> | <span data-ttu-id="8ca84-241">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-241">No</span></span> | <span data-ttu-id="8ca84-242">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-242">N\A</span></span> | <span data-ttu-id="8ca84-243">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-243">No</span></span> | <span data-ttu-id="8ca84-244">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-244">N\A</span></span> |
| <span data-ttu-id="8ca84-245">**Entita integrace Project Operations pro odhady výdajů (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="8ca84-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="8ca84-246">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-246">No</span></span> | <span data-ttu-id="8ca84-247">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-247">No</span></span> | <span data-ttu-id="8ca84-248">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-248">N\A</span></span> | <span data-ttu-id="8ca84-249">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-249">No</span></span> | <span data-ttu-id="8ca84-250">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-250">N\A</span></span> |
| <span data-ttu-id="8ca84-251">**Entita exportu kategorie výdajů projektu integrace Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="8ca84-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="8ca84-252">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-252">No</span></span> | <span data-ttu-id="8ca84-253">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-253">No</span></span> | <span data-ttu-id="8ca84-254">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-254">N\A</span></span> | <span data-ttu-id="8ca84-255">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-255">No</span></span> | <span data-ttu-id="8ca84-256">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-256">N\A</span></span> |
| <span data-ttu-id="8ca84-257">**Entita exportu výdajů projektu integrace Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="8ca84-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="8ca84-258">Ano</span><span class="sxs-lookup"><span data-stu-id="8ca84-258">Yes</span></span> | <span data-ttu-id="8ca84-259">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-259">No</span></span> | <span data-ttu-id="8ca84-260">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-260">N\A</span></span> | <span data-ttu-id="8ca84-261">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-261">No</span></span> | <span data-ttu-id="8ca84-262">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-262">N\A</span></span> |
| <span data-ttu-id="8ca84-263">**Entita integrace Project Operations pro odhady hodin (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="8ca84-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="8ca84-264">Ano</span><span class="sxs-lookup"><span data-stu-id="8ca84-264">Yes</span></span> | <span data-ttu-id="8ca84-265">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-265">No</span></span> | <span data-ttu-id="8ca84-266">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-266">N\A</span></span> | <span data-ttu-id="8ca84-267">No</span><span class="sxs-lookup"><span data-stu-id="8ca84-267">No</span></span> | <span data-ttu-id="8ca84-268">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="8ca84-268">N\A</span></span> |


4. <span data-ttu-id="8ca84-269">Chcete-li entitu aktualizovat, vyberte název mapy a poté vyberte příkaz **Aktualizovat entity**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Aktualizovat mapu](./media/20RefreshMapping.png)

5. <span data-ttu-id="8ca84-271">Po dokončení aktualizace spusťte mapu.</span><span class="sxs-lookup"><span data-stu-id="8ca84-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="8ca84-272">Před povolením další mapy ověřte, zda je mapa v tabulce ve stavu **Běh**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="8ca84-273">Spuštění map s větším počtem předpokladů může trvat delší dobu.</span><span class="sxs-lookup"><span data-stu-id="8ca84-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="8ca84-274">Chcete-li spustit mapu s předpoklady, zapněte přepínač **Zobrazit související mapy entit**.</span><span class="sxs-lookup"><span data-stu-id="8ca84-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="8ca84-275">Pokud je v tabulce **Počáteční synchronizace požadavků** nastavena na **Ne**, ověřte, zda příznak **Počáteční synchronizace** má hodnotu **Vypnuto** ve všech mapách požadavků, než ji spustíte.</span><span class="sxs-lookup"><span data-stu-id="8ca84-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Spuštění mapy](./media/21RunMap.png)

6. <span data-ttu-id="8ca84-277">Ověřte, zda jsou všechny mapy související s projektem v běžícím stavu.</span><span class="sxs-lookup"><span data-stu-id="8ca84-277">Validate all project related maps are in the running state.</span></span>

![Všechny mapy běží](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="8ca84-279">Použití dat konfigurace v prostředí CDS pro Project Operations (volitelně)</span><span class="sxs-lookup"><span data-stu-id="8ca84-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="8ca84-280">Pokud jste použili ukázková data v prostředí Finance, viz [Nastavení a použití konfiguračních dat v Common Data Service pro Project Operations](resource-apply-pro-setup-config-data.md) pro použití ukázkových dat v prostředí CDS.</span><span class="sxs-lookup"><span data-stu-id="8ca84-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="8ca84-281">Vaše prostředí Project Operations je nyní zřízeno a nakonfigurováno.</span><span class="sxs-lookup"><span data-stu-id="8ca84-281">Your Project Operations environment is now provisioned and configured.</span></span> 
