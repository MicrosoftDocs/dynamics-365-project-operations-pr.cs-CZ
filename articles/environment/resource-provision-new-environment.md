---
title: Zřízení nového prostředí
description: Toto téma poskytuje informace o zřízení nového prostředí Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a43b947207b6d4276ef27ec996713bf3883e7906
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073667"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="06abe-103">Zřízení nového prostředí</span><span class="sxs-lookup"><span data-stu-id="06abe-103">Provision a new environment</span></span>

<span data-ttu-id="06abe-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="06abe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="06abe-105">Toto téma poskytuje informace o tom, jak zřídit nové prostředí Dynamics 365 Project Operations pro scénáře založené na zdrojích / neuskladněných zásobách.</span><span class="sxs-lookup"><span data-stu-id="06abe-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="06abe-106">Povolení automatického zřizování Project Operations v projektu LCS</span><span class="sxs-lookup"><span data-stu-id="06abe-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="06abe-107">Pomocí následujících kroků povolíte tok automatického zřizování Project Operations pro váš projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="06abe-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="06abe-108">Přejděte do [LCS](https://lcs.dynamics.com/v2) a vyberte dlaždici **Správa funkce náhledu**.</span><span class="sxs-lookup"><span data-stu-id="06abe-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="06abe-109">V seznamu **Funkce Preview** vyberte **Funkce Project Operations** a poté výběrem možnosti **Povolit funkci verze Preview** povolte aplikaci Project Operations.</span><span class="sxs-lookup"><span data-stu-id="06abe-109">In the **Preview feature** list, select **Project Operations Feature** , and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="06abe-110">Tento krok se provádí pouze jednou za projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="06abe-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="06abe-111">Zřízení prostředí Project Operations</span><span class="sxs-lookup"><span data-stu-id="06abe-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="06abe-112">Otevřete nové [demo prostředí Dynamics 365 Finance](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) nebo nasazení [sandboxu / produkčního prostředí](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="06abe-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="06abe-113">Projděte jednotlivé obrazovky průvodce **Zřízení prostředí**.</span><span class="sxs-lookup"><span data-stu-id="06abe-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="06abe-114">Zkontrolujte, zda je vybrána verze aplikace 10.0.13 nebo vyšší.</span><span class="sxs-lookup"><span data-stu-id="06abe-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="06abe-115">Chcete-li zřídit Project Operations, vyberte v části **Pokročilé nastavení** položku **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="06abe-115">To provision Project Operations, under **Advance settings** , select **Common Data Service**.</span></span> 
4. <span data-ttu-id="06abe-116">Povolte **Nastavení Common Data Service** výběrem **Ano** a poté zadejte informace do požadovaných polí:</span><span class="sxs-lookup"><span data-stu-id="06abe-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="06abe-117">Jméno</span><span class="sxs-lookup"><span data-stu-id="06abe-117">Name</span></span>
  - <span data-ttu-id="06abe-118">Oblast</span><span class="sxs-lookup"><span data-stu-id="06abe-118">Region</span></span>
  - <span data-ttu-id="06abe-119">Jazyk</span><span class="sxs-lookup"><span data-stu-id="06abe-119">Language</span></span>
  - <span data-ttu-id="06abe-120">Měna</span><span class="sxs-lookup"><span data-stu-id="06abe-120">Currency</span></span>
 
5. <span data-ttu-id="06abe-121">V poli **Šablona Common Data Service** vyberte **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="06abe-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="06abe-122">Vyberte typ prostředí pro vaše nasazení.</span><span class="sxs-lookup"><span data-stu-id="06abe-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="06abe-123">Zkušební verze založená na předplatném vám umožní nasadit prostředí CDS po dobu 30 dnů.</span><span class="sxs-lookup"><span data-stu-id="06abe-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Nastavení nasazení](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="06abe-125">Výběrem možnosti **Souhlasím** potvrďte podmínky služby a poté se výběrem možnosti **Hotovo** vraťte do nastavení nasazení.</span><span class="sxs-lookup"><span data-stu-id="06abe-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Souhlas s nasazením](./media/2DeploymentConsent.png)

7. <span data-ttu-id="06abe-127">Vyplňte zbývající požadovaná pole v průvodci a potvrďte nasazení.</span><span class="sxs-lookup"><span data-stu-id="06abe-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="06abe-128">Čas zřízení prostředí se liší podle typu prostředí.</span><span class="sxs-lookup"><span data-stu-id="06abe-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="06abe-129">Zřizování může trvat až šest hodin.</span><span class="sxs-lookup"><span data-stu-id="06abe-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="06abe-130">Po úspěšném dokončení nasazení se prostředí zobrazí jako **Nasazeno**.</span><span class="sxs-lookup"><span data-stu-id="06abe-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="06abe-131">Chcete-li potvrdit úspěšné nasazení prostředí, vyberte možnost **Přihlásit se** a potvrďte dokončení přihlášením do prostředí.</span><span class="sxs-lookup"><span data-stu-id="06abe-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Podrobnosti prostředí ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="06abe-133">Použití ukázkových dat Project Operations Finance (volitelný krok)</span><span class="sxs-lookup"><span data-stu-id="06abe-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="06abe-134">Ukázková data Project Operations Finance se použijí na prostředí hostované v cloudu s verzí služby 10.0.13 podle popisu v [tomto článku](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="06abe-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="06abe-135">Použití aktualizací v prostředí Finance</span><span class="sxs-lookup"><span data-stu-id="06abe-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="06abe-136">Project Operations vyžaduje prostředí Finance s verzí aplikace **10.0.13 (10.0.569.20009)** nebo vyšší.</span><span class="sxs-lookup"><span data-stu-id="06abe-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="06abe-137">K získání této verze možná budete muset na svém prostředí Finance použít aktualizace kvality.</span><span class="sxs-lookup"><span data-stu-id="06abe-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="06abe-138">V LCS, na stránce **Podrobnosti o prostředí** v sekci **Dostupné aktualizace** vyberte možnost **Zobrazit aktualizaci**.</span><span class="sxs-lookup"><span data-stu-id="06abe-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Zobrazení aktualizací](./media/5ViewUpdates.png)

2. <span data-ttu-id="06abe-140">Na stránce **Binární aktualizace** vyberte možnost **Uložit balíček.**</span><span class="sxs-lookup"><span data-stu-id="06abe-140">On the **Binary updates** page, select **Save package.**</span></span>

![Uložení balíčku](./media/6SavePackage.png)

3. <span data-ttu-id="06abe-142">Klikněte na položku **Vybrat vše** a pak vyberte příkaz **Uložit balíček**.</span><span class="sxs-lookup"><span data-stu-id="06abe-142">Click **Select all** and then select **Save package**.</span></span>

![Kontrola a ukládání aktualizací](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="06abe-144">Zadejte název a popis balíčku a poté vyberte příkaz **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="06abe-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="06abe-145">Tento proces může nějakou dobu trvat (v závislosti na rychlosti připojení k internetu).</span><span class="sxs-lookup"><span data-stu-id="06abe-145">Depending on the internet connection, this process might take some time.</span></span>

![Nahrání balíčku do knihovny prostředků](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="06abe-147">Po uložení balíčku vyberte možnost **Hotovo** a uložte tento balíček do knihovny prostředků ve vašem projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="06abe-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="06abe-148">Uložení a ověření balíčku může trvat až 15 minut.</span><span class="sxs-lookup"><span data-stu-id="06abe-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="06abe-149">Chcete-li použít aktualizaci, přejděte na stránku **Podrobnosti o prostředí** v LCS a vyberte příkaz **Údržba** > **Použít aktualizace**.</span><span class="sxs-lookup"><span data-stu-id="06abe-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Údržba prostředí](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="06abe-151">V seznamu aktualizací vyberte balíček, který jste vytvořili, a vyberte příkaz **Použít**.</span><span class="sxs-lookup"><span data-stu-id="06abe-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Instalace aktualizací](./media/10ApplyUpdates.png)

<span data-ttu-id="06abe-153">Údržba prostředí bude nějakou dobu trvat.</span><span class="sxs-lookup"><span data-stu-id="06abe-153">Environment servicing will take some time.</span></span> <span data-ttu-id="06abe-154">Po dokončení se prostředí vrátí do nasazeného stavu.</span><span class="sxs-lookup"><span data-stu-id="06abe-154">After it is complete, the environment will return to a deployed state.</span></span>

![Nasazené prostředí](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="06abe-156">Vytvoření připojení s duálním zápisem</span><span class="sxs-lookup"><span data-stu-id="06abe-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="06abe-157">V projektu LCS přejděte na stránku **Podrobnosti o prostředí**.</span><span class="sxs-lookup"><span data-stu-id="06abe-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="06abe-158">V části **Informace o prostředí Common Data Service** vyberte možnost **Odkaz na CDS pro aplikace**.</span><span class="sxs-lookup"><span data-stu-id="06abe-158">Under **Common Data Service Environment Information** , select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="06abe-159">Po vytvoření odkazu vyberte znovu možnost **Odkaz na CDS pro aplikace**.</span><span class="sxs-lookup"><span data-stu-id="06abe-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="06abe-160">Budete přesměrováni na duální zápis ve Finance.</span><span class="sxs-lookup"><span data-stu-id="06abe-160">You will be redirected to Dual Write in Finance.</span></span>

![Odkaz na CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="06abe-162">Výběrem položky **Použít řešení** získáte přístup k entitám, které budou mapovány v integraci.</span><span class="sxs-lookup"><span data-stu-id="06abe-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Použít řešení](./media/13ApplySolutions.png)

5. <span data-ttu-id="06abe-164">Vyberte obě řešení **Mapa entit duálního zápisu Dynamics 365 Finance and Operations** a **Mapa entit duálního zápisu Dynamics 365 Project Operations** a potom vyberte příkaz **Použít**.</span><span class="sxs-lookup"><span data-stu-id="06abe-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps** , and then select **Apply**.</span></span>

![Potvrzení řešení](./media/14ConfirmSolutions.png)

<span data-ttu-id="06abe-166">Poté, co je řešení použito, se na prostředí použijí entity duálního zápisu.</span><span class="sxs-lookup"><span data-stu-id="06abe-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Použití řešení](./media/15ApplyingSolutions.png)

<span data-ttu-id="06abe-168">Po použití entit se v prostředí zobrazí všechna dostupná mapování.</span><span class="sxs-lookup"><span data-stu-id="06abe-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mapy duálního zápisu](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="06abe-170">Po aktualizaci aktualizujte datové entity</span><span class="sxs-lookup"><span data-stu-id="06abe-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="06abe-171">Ve Finance přejděte do pracovního prostoru **Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="06abe-171">In Finance, go to the **Data management** workspace.</span></span>

![Pracovní prostor správy dat](./media/16DataManagement.png)

2. <span data-ttu-id="06abe-173">Vyberte dlaždici **Parametry architektury**.</span><span class="sxs-lookup"><span data-stu-id="06abe-173">Select the **Framework parameters** tile.</span></span>

![Parametry architektury](./media/17FrameworkParameters.png)

3. <span data-ttu-id="06abe-175">Na stránce **Nastavení entity** vyberte možnost **Aktualizovat seznam entit**.</span><span class="sxs-lookup"><span data-stu-id="06abe-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Aktualizovat seznam entit](./media/18RefreshEntityList.png)

<span data-ttu-id="06abe-177">Aktualizace bude trvat přibližně 20 minut.</span><span class="sxs-lookup"><span data-stu-id="06abe-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="06abe-178">Po dokončení obdržíte upozornění.</span><span class="sxs-lookup"><span data-stu-id="06abe-178">You will receive an alert when it is complete.</span></span>

![Potvrzení aktualizace](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="06abe-180">Spuštění mapování duálního zápisu Project Operations</span><span class="sxs-lookup"><span data-stu-id="06abe-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="06abe-181">V projektu LCS přejděte na stránku **Podrobnosti o prostředí**.</span><span class="sxs-lookup"><span data-stu-id="06abe-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="06abe-182">V části **Informace o prostředí Common Data Service** vyberte možnost **Odkaz na CDS pro aplikace**.</span><span class="sxs-lookup"><span data-stu-id="06abe-182">Under **Common Data Service Environment Information** , select **Link to CDS for Apps.**</span></span> <span data-ttu-id="06abe-183">Poté, co vyberete odkaz, budete přesměrováni na seznam entit v mapováních.</span><span class="sxs-lookup"><span data-stu-id="06abe-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="06abe-184">Spusťte mapování podle popisu v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="06abe-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="06abe-185">Postupujte podle níže uvedené sekvence.</span><span class="sxs-lookup"><span data-stu-id="06abe-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="06abe-186">**Mapování entity**</span><span class="sxs-lookup"><span data-stu-id="06abe-186">**Entity Map**</span></span> | <span data-ttu-id="06abe-187">**Aktualizovat entity**</span><span class="sxs-lookup"><span data-stu-id="06abe-187">**Refresh entity**</span></span> | <span data-ttu-id="06abe-188">**Počáteční synchronizace**</span><span class="sxs-lookup"><span data-stu-id="06abe-188">**Initial sync**</span></span> | <span data-ttu-id="06abe-189">**Předloha pro počáteční synchronizaci**</span><span class="sxs-lookup"><span data-stu-id="06abe-189">**Master for initial sync**</span></span> | <span data-ttu-id="06abe-190">**Spustit požadavky**</span><span class="sxs-lookup"><span data-stu-id="06abe-190">**Run prerequisites**</span></span> | <span data-ttu-id="06abe-191">**Počáteční synchronizace požadavků**</span><span class="sxs-lookup"><span data-stu-id="06abe-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="06abe-192">**Role zdrojů projektu pro všechny společnosti (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="06abe-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="06abe-193">No</span><span class="sxs-lookup"><span data-stu-id="06abe-193">No</span></span> | <span data-ttu-id="06abe-194">Ano</span><span class="sxs-lookup"><span data-stu-id="06abe-194">Yes</span></span> | <span data-ttu-id="06abe-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="06abe-195">Common Data Service</span></span> | <span data-ttu-id="06abe-196">No</span><span class="sxs-lookup"><span data-stu-id="06abe-196">No</span></span> | <span data-ttu-id="06abe-197">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-197">N\A</span></span> |
| <span data-ttu-id="06abe-198">**Právnické osoby (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="06abe-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="06abe-199">No</span><span class="sxs-lookup"><span data-stu-id="06abe-199">No</span></span> | <span data-ttu-id="06abe-200">Ano</span><span class="sxs-lookup"><span data-stu-id="06abe-200">Yes</span></span> | <span data-ttu-id="06abe-201">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="06abe-201">Finance and Operations apps</span></span> | <span data-ttu-id="06abe-202">No</span><span class="sxs-lookup"><span data-stu-id="06abe-202">No</span></span> | <span data-ttu-id="06abe-203">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-203">N\A</span></span> |
| <span data-ttu-id="06abe-204">**Skutečné hodnoty integrace Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="06abe-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="06abe-205">No</span><span class="sxs-lookup"><span data-stu-id="06abe-205">No</span></span> | <span data-ttu-id="06abe-206">No</span><span class="sxs-lookup"><span data-stu-id="06abe-206">No</span></span> | <span data-ttu-id="06abe-207">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-207">N\A</span></span> | <span data-ttu-id="06abe-208">Ano</span><span class="sxs-lookup"><span data-stu-id="06abe-208">Yes</span></span> | <span data-ttu-id="06abe-209">No</span><span class="sxs-lookup"><span data-stu-id="06abe-209">No</span></span> |
| <span data-ttu-id="06abe-210">**Řádky smlouvy založené na projektu (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="06abe-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="06abe-211">No</span><span class="sxs-lookup"><span data-stu-id="06abe-211">No</span></span> | <span data-ttu-id="06abe-212">No</span><span class="sxs-lookup"><span data-stu-id="06abe-212">No</span></span> | <span data-ttu-id="06abe-213">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-213">N\A</span></span> | <span data-ttu-id="06abe-214">No</span><span class="sxs-lookup"><span data-stu-id="06abe-214">No</span></span> | <span data-ttu-id="06abe-215">No</span><span class="sxs-lookup"><span data-stu-id="06abe-215">No</span></span> |
| <span data-ttu-id="06abe-216">**Entita integrace pro vztahy projektových transakcí (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="06abe-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="06abe-217">No</span><span class="sxs-lookup"><span data-stu-id="06abe-217">No</span></span> | <span data-ttu-id="06abe-218">No</span><span class="sxs-lookup"><span data-stu-id="06abe-218">No</span></span> | <span data-ttu-id="06abe-219">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-219">N\A</span></span> | <span data-ttu-id="06abe-220">No</span><span class="sxs-lookup"><span data-stu-id="06abe-220">No</span></span> | <span data-ttu-id="06abe-221">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-221">N\A</span></span> |
| <span data-ttu-id="06abe-222">**Milníky řádku smlouvy integrace Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="06abe-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="06abe-223">No</span><span class="sxs-lookup"><span data-stu-id="06abe-223">No</span></span> | <span data-ttu-id="06abe-224">No</span><span class="sxs-lookup"><span data-stu-id="06abe-224">No</span></span> | <span data-ttu-id="06abe-225">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-225">N\A</span></span> | <span data-ttu-id="06abe-226">No</span><span class="sxs-lookup"><span data-stu-id="06abe-226">No</span></span> | <span data-ttu-id="06abe-227">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-227">N\A</span></span> |
| <span data-ttu-id="06abe-228">**Entita integrace Project Operations pro odhady výdajů (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="06abe-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="06abe-229">No</span><span class="sxs-lookup"><span data-stu-id="06abe-229">No</span></span> | <span data-ttu-id="06abe-230">No</span><span class="sxs-lookup"><span data-stu-id="06abe-230">No</span></span> | <span data-ttu-id="06abe-231">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-231">N\A</span></span> | <span data-ttu-id="06abe-232">No</span><span class="sxs-lookup"><span data-stu-id="06abe-232">No</span></span> | <span data-ttu-id="06abe-233">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-233">N\A</span></span> |
| <span data-ttu-id="06abe-234">**Entita exportu kategorie výdajů projektu integrace Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="06abe-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="06abe-235">No</span><span class="sxs-lookup"><span data-stu-id="06abe-235">No</span></span> | <span data-ttu-id="06abe-236">No</span><span class="sxs-lookup"><span data-stu-id="06abe-236">No</span></span> | <span data-ttu-id="06abe-237">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-237">N\A</span></span> | <span data-ttu-id="06abe-238">No</span><span class="sxs-lookup"><span data-stu-id="06abe-238">No</span></span> | <span data-ttu-id="06abe-239">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-239">N\A</span></span> |
| <span data-ttu-id="06abe-240">**Entita exportu výdajů projektu integrace Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="06abe-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="06abe-241">Ano</span><span class="sxs-lookup"><span data-stu-id="06abe-241">Yes</span></span> | <span data-ttu-id="06abe-242">No</span><span class="sxs-lookup"><span data-stu-id="06abe-242">No</span></span> | <span data-ttu-id="06abe-243">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-243">N\A</span></span> | <span data-ttu-id="06abe-244">No</span><span class="sxs-lookup"><span data-stu-id="06abe-244">No</span></span> | <span data-ttu-id="06abe-245">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-245">N\A</span></span> |
| <span data-ttu-id="06abe-246">**Entita integrace Project Operations pro odhady hodin (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="06abe-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="06abe-247">Ano</span><span class="sxs-lookup"><span data-stu-id="06abe-247">Yes</span></span> | <span data-ttu-id="06abe-248">No</span><span class="sxs-lookup"><span data-stu-id="06abe-248">No</span></span> | <span data-ttu-id="06abe-249">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-249">N\A</span></span> | <span data-ttu-id="06abe-250">No</span><span class="sxs-lookup"><span data-stu-id="06abe-250">No</span></span> | <span data-ttu-id="06abe-251">Neuvedeno</span><span class="sxs-lookup"><span data-stu-id="06abe-251">N\A</span></span> |


4. <span data-ttu-id="06abe-252">Chcete-li entitu aktualizovat, vyberte název mapy a poté vyberte příkaz **Aktualizovat entity**.</span><span class="sxs-lookup"><span data-stu-id="06abe-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Aktualizovat mapu](./media/20RefreshMapping.png)

5. <span data-ttu-id="06abe-254">Po dokončení aktualizace spusťte mapu.</span><span class="sxs-lookup"><span data-stu-id="06abe-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="06abe-255">Před povolením další mapy ověřte, zda je mapa v tabulce ve stavu **Běh**.</span><span class="sxs-lookup"><span data-stu-id="06abe-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="06abe-256">Spuštění map s větším počtem předpokladů může trvat delší dobu.</span><span class="sxs-lookup"><span data-stu-id="06abe-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="06abe-257">Chcete-li spustit mapu s předpoklady, zapněte přepínač **Zobrazit související mapy entit**.</span><span class="sxs-lookup"><span data-stu-id="06abe-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="06abe-258">Pokud je v tabulce **Počáteční synchronizace požadavků** nastavena na **Ne** , ověřte, zda příznak **Počáteční synchronizace** má hodnotu **Vypnuto** ve všech mapách požadavků, než ji spustíte.</span><span class="sxs-lookup"><span data-stu-id="06abe-258">If the table indicates **Prerequisite initial sync** is **No** , verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Spuštění mapy](./media/21RunMap.png)

6. <span data-ttu-id="06abe-260">Ověřte, zda jsou všechny mapy související s projektem v běžícím stavu.</span><span class="sxs-lookup"><span data-stu-id="06abe-260">Validate all project related maps are in the running state.</span></span>

![Všechny mapy běží](./media/22AllMapsRunning.png)

<span data-ttu-id="06abe-262">Vaše prostředí Project Operations je nyní zřízeno a nakonfigurováno.</span><span class="sxs-lookup"><span data-stu-id="06abe-262">Your Project Operations environment is now provisioned and configured.</span></span>