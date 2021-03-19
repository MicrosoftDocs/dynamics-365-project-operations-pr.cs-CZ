---
title: Nastavení a použití konfiguračních dat v Common Data Service
description: Toto téma poskytuje informace o tom, jak nastavit a použít konfigurační data v aplikaci Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1651d3b3b85d3dc581bf61976fada249bafd6b7b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289811"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="395c3-103">Nastavení a použití konfiguračních dat v Common Data Service</span><span class="sxs-lookup"><span data-stu-id="395c3-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="395c3-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="395c3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="395c3-105">Požadavky</span><span class="sxs-lookup"><span data-stu-id="395c3-105">Prerequisites</span></span>

<span data-ttu-id="395c3-106">Než začnete konfigurovat data v Common Data Service (CDS), musí být splněny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="395c3-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="395c3-107">Máte zřízeno prostředí CDS a Dynamics 365 Finance pro Project Operations.</span><span class="sxs-lookup"><span data-stu-id="395c3-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="395c3-108">V prostředí CDS jsou sdíleny informace o právnické osobě z Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="395c3-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="395c3-109">To znamená, že entita **Společnost** v CDS má následující záznamy:</span><span class="sxs-lookup"><span data-stu-id="395c3-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="395c3-110">THPM</span><span class="sxs-lookup"><span data-stu-id="395c3-110">THPM</span></span>
  - <span data-ttu-id="395c3-111">USPM</span><span class="sxs-lookup"><span data-stu-id="395c3-111">USPM</span></span>
  - <span data-ttu-id="395c3-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="395c3-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="395c3-113">Instalace nastavení a dat konfigurace</span><span class="sxs-lookup"><span data-stu-id="395c3-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="395c3-114">Stáhněte, odblokujte a rozbalte soubor [Balíček údajů o nastavení a konfiguraci](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="395c3-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="395c3-115">Přejděte do rozbalené složky a spusťte soubor *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="395c3-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="395c3-116">Na straně 1 Průvodce konfigurací migrace (CMT) Common Data Service, vyberte **Importovat data** a poté vyberte **Pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="395c3-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrace konfigurace](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="395c3-118">Na stránce 2 průvodce CMT vyberte **Microsoft 365** jako **Typ nasazení**.</span><span class="sxs-lookup"><span data-stu-id="395c3-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="395c3-119">Zaškrtněte políčka **Zobrazit seznam dostupných organizací** a **Zobrazit pokročilé**.</span><span class="sxs-lookup"><span data-stu-id="395c3-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="395c3-120">Vyberte oblast vašeho klienta, zadejte své přihlašovací údaje a vyberte příkaz **Přihlásit se**.</span><span class="sxs-lookup"><span data-stu-id="395c3-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Přihlášení do konfigurace](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="395c3-122">Na stránce 3 vyberte ze seznamu organizací v klientovi organizaci, do které chcete importovat ukázková data, a vyberte příkaz **Přihlásit se**.</span><span class="sxs-lookup"><span data-stu-id="395c3-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="395c3-123">Na stránce 4 vyberte soubor zip *SampleSetupAndConfigData* z rozbalené složky.</span><span class="sxs-lookup"><span data-stu-id="395c3-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Výběr souboru ZIP](./media/3ZipFile.png)

![Vyberte soubor.](./media/4SelectAFile.png)

9. <span data-ttu-id="395c3-126">Po výběru souboru zip vyberte **Importovat data**.</span><span class="sxs-lookup"><span data-stu-id="395c3-126">After the zip file is selected, select **Import Data**.</span></span>

![Importovat data](./media/5ImportData.png)

10. <span data-ttu-id="395c3-128">Import bude probíhat přibližně dvě až deset minut v závislosti na rychlosti vaší sítě.</span><span class="sxs-lookup"><span data-stu-id="395c3-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="395c3-129">Po dokončení importu ukončete průvodce CMT.</span><span class="sxs-lookup"><span data-stu-id="395c3-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="395c3-130">Zkontrolujte ve své organizaci data v následujících 19 entitách:</span><span class="sxs-lookup"><span data-stu-id="395c3-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="395c3-131">Měna</span><span class="sxs-lookup"><span data-stu-id="395c3-131">Currency</span></span>
  - <span data-ttu-id="395c3-132">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="395c3-132">Organizational Unit</span></span>
  - <span data-ttu-id="395c3-133">Kontakt</span><span class="sxs-lookup"><span data-stu-id="395c3-133">Contact</span></span>
  - <span data-ttu-id="395c3-134">Daňová skupina</span><span class="sxs-lookup"><span data-stu-id="395c3-134">Tax Group</span></span>
  - <span data-ttu-id="395c3-135">Skupina zákazníků</span><span class="sxs-lookup"><span data-stu-id="395c3-135">Customer Group</span></span>
  - <span data-ttu-id="395c3-136">Jednotka</span><span class="sxs-lookup"><span data-stu-id="395c3-136">Unit</span></span>
  - <span data-ttu-id="395c3-137">Skupina jednotek</span><span class="sxs-lookup"><span data-stu-id="395c3-137">Unit Group</span></span>
  - <span data-ttu-id="395c3-138">Ceník</span><span class="sxs-lookup"><span data-stu-id="395c3-138">Price List</span></span>
  - <span data-ttu-id="395c3-139">Ceník projektových parametrů</span><span class="sxs-lookup"><span data-stu-id="395c3-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="395c3-140">Frekvence faktur</span><span class="sxs-lookup"><span data-stu-id="395c3-140">Invoice Frequency</span></span>
  - <span data-ttu-id="395c3-141">Kategorie rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="395c3-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="395c3-142">Kategorie transakce</span><span class="sxs-lookup"><span data-stu-id="395c3-142">Transaction Category</span></span>
  - <span data-ttu-id="395c3-143">Kategorie výdaje</span><span class="sxs-lookup"><span data-stu-id="395c3-143">Expense Category</span></span>
  - <span data-ttu-id="395c3-144">Cena role</span><span class="sxs-lookup"><span data-stu-id="395c3-144">Role Price</span></span>
  - <span data-ttu-id="395c3-145">Cena kategorie transakce</span><span class="sxs-lookup"><span data-stu-id="395c3-145">Transaction Category Price</span></span>
  - <span data-ttu-id="395c3-146">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="395c3-146">Characteristic</span></span>
  - <span data-ttu-id="395c3-147">Rezervovatelný zdroj</span><span class="sxs-lookup"><span data-stu-id="395c3-147">Bookable Resource</span></span>
  - <span data-ttu-id="395c3-148">Přidružení kategorie rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="395c3-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="395c3-149">Charakteristika rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="395c3-149">Bookable Resource Characteristic</span></span>

![Dokončit import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="395c3-151">Aktualizace konfigurací Project Operations</span><span class="sxs-lookup"><span data-stu-id="395c3-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="395c3-152">Přejděte do prostředí CE.</span><span class="sxs-lookup"><span data-stu-id="395c3-152">Navigate to the CE environment.</span></span> <span data-ttu-id="395c3-153">Najdete jej otevřením [Centra pro správu Power Platform](https://admin.powerplatform.microsoft.com/environments), kde vyberete prostředí a poté **Otevřené prostředí**.</span><span class="sxs-lookup"><span data-stu-id="395c3-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Otevření prostředí](./media/7OpenEnvironment.png)

2. <span data-ttu-id="395c3-155">Přejděte do nabídky **Projekty** > **Zdroje** a poté vyberte příkaz **Nový** k vytvoření rezervovatelného zdroje pro vašeho uživatele.</span><span class="sxs-lookup"><span data-stu-id="395c3-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Rezervovatelné zdroje](./media/8BookableResources.png)

3. <span data-ttu-id="395c3-157">Na kartě **Obecné** vyberte uživatele správce.</span><span class="sxs-lookup"><span data-stu-id="395c3-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="395c3-158">Ověřte, zda se časové pásmo shoduje s časovým pásmem, ve kterém se nacházíte.</span><span class="sxs-lookup"><span data-stu-id="395c3-158">Verify that the time zone matches the one you are in.</span></span> 

![Nový rezervovatelný zdroj](./media/9NewBookableResource.png)

4. <span data-ttu-id="395c3-160">Na kartě **Plánování** v poli **Společnost** vyberte společnost **USPM** a poté vyberte příkaz **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="395c3-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Karta Plánování](./media/10SchedulingTab.png)

5. <span data-ttu-id="395c3-162">Vyberte kartu **Pracovní doba**.</span><span class="sxs-lookup"><span data-stu-id="395c3-162">Select the **Work hours** tab.</span></span>  

![Pracovní doba](./media/11WorkHours.png)

6. <span data-ttu-id="395c3-164">Poklepejte na libovolnou hodnotu v kalendáři a vyberte příkaz **Upravit** > **Všechny události v řadě**.</span><span class="sxs-lookup"><span data-stu-id="395c3-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Pracovní kalendář](./media/12WorkCalendar.png)

7. <span data-ttu-id="395c3-166">Změňte pracovní dobu na osmi (8) hodinový pracovní den, označte víkendy jako dny pracovního klidu a ujistěte se, že časové pásmo odpovídá vašemu.</span><span class="sxs-lookup"><span data-stu-id="395c3-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="395c3-167">Zvolte **Uložit a zavřít**.</span><span class="sxs-lookup"><span data-stu-id="395c3-167">Select **Save and close**.</span></span>

![Aktualizace kalendáře](./media/13UpdateCalendar.png)

9. <span data-ttu-id="395c3-169">Přejděte do nabídky **Nastavení** > **Šablony kalendáře** a vyberte položku **Nová**.</span><span class="sxs-lookup"><span data-stu-id="395c3-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Šablony kalendářů](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="395c3-171">Zadejte název, vyberte zdroj šablony, který jste vytvořili, a pak vyberte příkaz **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="395c3-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Uložení šablony kalendáře](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="395c3-173">Přejděte do části **Parametry** a dvakrát klikněte na záznam.</span><span class="sxs-lookup"><span data-stu-id="395c3-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektové parametry](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="395c3-175">Aktualizujte následující pole:</span><span class="sxs-lookup"><span data-stu-id="395c3-175">Update the following fields:</span></span>

 - <span data-ttu-id="395c3-176">**Výchozí společnost**: USPM</span><span class="sxs-lookup"><span data-stu-id="395c3-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="395c3-177">**Výchozí organizační jednotka**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="395c3-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="395c3-178">**Četnost faktur**: Sedmý a poslední den</span><span class="sxs-lookup"><span data-stu-id="395c3-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="395c3-179">**Šablona pracovní doby**: Změňte na šablonu, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="395c3-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="395c3-180">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="395c3-180">Select **Save**.</span></span> 

![Aktualizované projektové parametry](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]