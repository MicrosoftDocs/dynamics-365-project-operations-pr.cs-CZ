---
title: Použití doplňku Project Service za účelem plánování práce v aplikaci Microsoft Project | MicrosoftDocs
description: Toto téma obsahuje informace o způsobu přidání, konfigurace a použití doplňku Microsoft project pro Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 6bc74442866caccc02e53afc913a55aab81f9629
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129670"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="a8ea8-103">Použití doplňku Project Service Automation za účelem plánování práce v aplikaci Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="a8ea8-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="a8ea8-104">vám usnadňuje plánování projektů, a to včetně odhadů.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="a8ea8-105">Můžete definovat práci tak, aby náklady, úsilí a hodnota prodeje byly jasné již při odesílání konečného návrhu.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="a8ea8-106">Nyní můžete nainstalovat [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] a plánovat práci ve známém prostředí aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="a8ea8-107">Využívejte výkonné možnosti plánování a správy aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a aktualizujte plán projektu v nástroji Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="a8ea8-108">Chcete-li použít funkci správy dokumentů SharePoint pro uložení souborů [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] projektů [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], musí váš správce aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] zapnout správu dokumentů.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="a8ea8-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] je kompatibilní pouze s aplikací [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="a8ea8-110">Stažení a instalace doplňku</span><span class="sxs-lookup"><span data-stu-id="a8ea8-110">Download and install the add-in</span></span>  
 <span data-ttu-id="a8ea8-111">Připravte si přihlašovací informace pro [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="a8ea8-112">Tyto informace budete potřebovat pro připojení z aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] k [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="a8ea8-113">Z webu Download Center si můžete stáhnout doplněk pro podporovanou verzi Project Service, a to buď [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) nebo [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="a8ea8-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="a8ea8-114">Klikněte na odkaz ke stažení.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-114">Click the download link.</span></span>  

3.  <span data-ttu-id="a8ea8-115">Po dokončení stahování kliknutím na tlačítko **Ano** nainstalujte doplněk.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="a8ea8-116">Konfigurace doplňku</span><span class="sxs-lookup"><span data-stu-id="a8ea8-116">Configure the add-in</span></span>  

1. <span data-ttu-id="a8ea8-117">Otevřete aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a klikněte na kartu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="a8ea8-118">Klepněte na tlačítko **Připojit**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="a8ea8-119">Zadejte své přihlašovací informace a poté klikněte na tlačítko **Přihlásit**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="a8ea8-120">Nyní můžete doplněk začít používat.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="a8ea8-121">Čtení ze šablony</span><span class="sxs-lookup"><span data-stu-id="a8ea8-121">Read from a template</span></span>  
 <span data-ttu-id="a8ea8-122">Plánování projektu zahájíte tím, že budete číst ze šablony vytvořené v nástroji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a zkopírované do aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a8ea8-123">[Vytvoření šablony projektu (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="a8ea8-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="a8ea8-124">Z karty **Project Service** klikněte na tlačítko **Číst** > **Šablona projektu nástroje Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="a8ea8-125">Ze seznamu zvolte šablonu projektu a potom klikněte na tlačítko **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="a8ea8-126">Ve výchozím nastavení jsou úkoly, které jsou zkopírovány ze šablony do projektu, nastaveny jako ručně naplánované.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="a8ea8-127">Přiřazení rolí [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ke zdrojům projektu</span><span class="sxs-lookup"><span data-stu-id="a8ea8-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="a8ea8-128">Otevřete projekt a klikněte na pás karet **Úkol**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="a8ea8-129">Klikněte na nabídku **Ganttův diagram** a pak zvolte **Seznam zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="a8ea8-130">V zobrazení Seznam zdrojů klikněte na rozevírací nabídku **Role zdroje Project Service** a zvolte roli Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="a8ea8-131">Poskytnutí zdrojů projektu</span><span class="sxs-lookup"><span data-stu-id="a8ea8-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="a8ea8-132">Na kartě Project Service vyberte řádek a klikněte na tlačítko **Najít zdroje**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="a8ea8-133">Na obrazovce **Rezervovat zdroj** vyberte zdroj, který chcete použít pro projekt.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="a8ea8-134">Klikněte na tlačítko **Rezervovat** a poté na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="a8ea8-135">Publikování projektu</span><span class="sxs-lookup"><span data-stu-id="a8ea8-135">Publish your project</span></span>  
<span data-ttu-id="a8ea8-136">Po dokončení plánování projektu je dalším krokem import a publikování projektu v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="a8ea8-137">Projekt se importuje do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="a8ea8-138">Použijí se procesy tvorby cen a generování týmu.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="a8ea8-139">Otevřením projektu v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ověřte, že byl vygenerován tým, odhad projektu a strukturovaný rozpis prací.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="a8ea8-140">Následující tabulka uvádí, kde lze nalézt výsledky:</span><span class="sxs-lookup"><span data-stu-id="a8ea8-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="a8ea8-141">**Ganttův diagram**</span><span class="sxs-lookup"><span data-stu-id="a8ea8-141">**Gantt Chart**</span></span>   | <span data-ttu-id="a8ea8-142">Importuje na obrazovku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Strukturovaný rozpis prací**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="a8ea8-143">**Tabulka zdrojů**</span><span class="sxs-lookup"><span data-stu-id="a8ea8-143">**Resource Sheet**</span></span> |   <span data-ttu-id="a8ea8-144">Importuje na obrazovku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Členové týmu projektu**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="a8ea8-145">**Pomocí využití**</span><span class="sxs-lookup"><span data-stu-id="a8ea8-145">**Use Usage**</span></span>    |    <span data-ttu-id="a8ea8-146">Importuje na obrazovku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Odhady projektů**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="a8ea8-147">**Chcete-li importovat a publikovat projekt**</span><span class="sxs-lookup"><span data-stu-id="a8ea8-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="a8ea8-148">Z karty **Project Service** klikněte na tlačítko **Publikovat** > **Nový projekt nástroje Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="a8ea8-149">V dialogovém okně  **Publikovat do nového projektu v aplikaci Project Service** zadejte **Název projektu** a vyberte položku **Zákazník**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="a8ea8-150">Volitelně můžete zaškrtnutím položky **Propojit projektový plán s řešením Project Service Automation** propojit soubor aplikace Project plánu s nástrojem Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="a8ea8-151">Klikněte na **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-151">Click **Publish**.</span></span>  

   <span data-ttu-id="a8ea8-152">Propojení souboru aplikace Project s [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] učiní soubor aplikace Project hlavním souborem a nastaví strukturovaný rozpis prací v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="a8ea8-153">Aby bylo možné provádět změny v plánu projektu, je nutné změny provést v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a publikovat je jako aktualizace do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="a8ea8-154">Úpravy projektu, který byl importován</span><span class="sxs-lookup"><span data-stu-id="a8ea8-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="a8ea8-155">Chcete-li provést změny v plánu projektu, který byl importován do nástroje [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], máte dvě možnosti:</span><span class="sxs-lookup"><span data-stu-id="a8ea8-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="a8ea8-156">Otevření hlavního souboru a jeho úprava v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="a8ea8-157">Zrušte propojení souboru a upravte jej přímo v aplikaci Project Service.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="a8ea8-158">Ve výchozím nastavení je projekt, který je odeslán z aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], uzamčen a lze jej upravovat pouze v aplikaci Project.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="a8ea8-159">Chcete-li upravit soubor v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], je třeba u souboru zrušit propojení.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="a8ea8-160">Upravit v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="a8ea8-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="a8ea8-161">V hlavní nabídce klikněte na příkaz **Project Service** > **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="a8ea8-162">Ze seznamu projektů otevřete ten, který jste vytvořili v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="a8ea8-163">Na pásu karet klikněte na tlačítko **Otevřít v MS Projectu**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="a8ea8-164">Tím se propojený hlavní soubor otevře v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="a8ea8-165">Zrušení propojení souboru a jeho úprava v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="a8ea8-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="a8ea8-166">V hlavní nabídce klikněte na příkaz **Project Service** > **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="a8ea8-167">Ze seznamu projektů otevřete ten, který jste vytvořili v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="a8ea8-168">Na pásu karet klikněte na tlačítko **Odpojit od MS Projectu**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="a8ea8-169">Odeslání souboru aplikace Project do služby SharePoint nebo do Skupin Office</span><span class="sxs-lookup"><span data-stu-id="a8ea8-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="a8ea8-170">Soubor aplikace Project můžete odeslat do služby SharePoint a najít jej v seznamu Přidružené dokumenty pro váš projekt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="a8ea8-171">Váš správce vám musí nakonfigurovat správu dokumentů SharePoint a zapnout ji pro entitu aplikace Project.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="a8ea8-172">Pokud máte nastaveny Skupiny Office, lze soubor aplikace Project uložit také do služby [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="a8ea8-173">Nahrát soubor pro SharePoint</span><span class="sxs-lookup"><span data-stu-id="a8ea8-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="a8ea8-174">V hlavní nabídce klikněte na příkaz **Project Service** > **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="a8ea8-175">Vyberte položku **Do projektových dokumentů aplikace Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="a8ea8-176">V dialogu **Povolit otevření v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** vyberte **Ano** nebo **Ne**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="a8ea8-177">Pokud kliknete na tlačítko **Ano**, budete moci vybrat možnost **Otevřít v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v aplikaci Project Service Automation, spustit aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a načíst soubor aplikace Project z knihovny dokumentů systému SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-177">If you click **Yes**, you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="a8ea8-178">Pokud kliknete na tlačítko **Ne**, odkaz tlačítka **Otevřít v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nebude fungovat.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-178">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="a8ea8-179">Soubor aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] naleznete v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v části **Dokumenty** pro konkrétní projekt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="a8ea8-180">Odeslání souboru pro Skupiny Office</span><span class="sxs-lookup"><span data-stu-id="a8ea8-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="a8ea8-181">V hlavní nabídce klikněte na příkaz **Project Service** > **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="a8ea8-182">Vyberte položku **Do projektových dokumentů aplikace Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="a8ea8-183">V dialogu **Povolit otevření v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** vyberte **Ano** nebo **Ne**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="a8ea8-184">Pokud kliknete na tlačítko **Ano**, budete moci vybrat možnost **Otevřít v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v aplikaci Project Service Automation, spustit aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a načíst soubor aplikace Project z knihovny dokumentů systému SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-184">If you click **Yes**, you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="a8ea8-185">Pokud kliknete na tlačítko **Ne**, odkaz tlačítka **Otevřít v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nebude fungovat.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-185">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="a8ea8-186">Soubor aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] naleznete v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v části **Dokumenty** pro konkrétní projekt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="a8ea8-187">Publikování projektu jako šablony</span><span class="sxs-lookup"><span data-stu-id="a8ea8-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="a8ea8-188">Projekt můžete uložit a znovu použít pomocí jeho uložení jako šablony projektu v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="a8ea8-189">Šablony projektu jsou znovu použitelné plány projektů v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a8ea8-190">[Vytvoření šablony projektu (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="a8ea8-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="a8ea8-191">Z karty **Project Service** klikněte na tlačítko **Publikovat** > **Nová šablona projektu nástroje Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="a8ea8-192">V dialogovém okně  **Publikovat do nové šablony projektu v aplikaci Project Service** zadejte **Název šablony projektu**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="a8ea8-193">Volitelně můžete zaškrtnutím položky **Propojit projektový plán s řešením Project Service Automation** propojit soubor aplikace Project s [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="a8ea8-194">Klikněte na **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-194">Click **Publish**.</span></span>  

<span data-ttu-id="a8ea8-195">Propojení souboru aplikace Project s [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] učiní soubor aplikace Project hlavním souborem a nastaví strukturovaný rozpis prací v šabloně [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="a8ea8-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="a8ea8-196">Aby bylo možné provádět změny v plánu projektu, je nutné změny provést v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a publikovat je jako aktualizace do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a8ea8-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="a8ea8-197">Viz také</span><span class="sxs-lookup"><span data-stu-id="a8ea8-197">See Also</span></span>  
 [<span data-ttu-id="a8ea8-198">Příručka pro projektového manažera</span><span class="sxs-lookup"><span data-stu-id="a8ea8-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
