---
title: Nastavení a použití konfiguračních dat v Common Data Service
description: Toto téma poskytuje informace o tom, jak nastavit a použít konfigurační data v aplikaci Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001283"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="28ef2-103">Nastavení a použití konfiguračních dat v Common Data Service</span><span class="sxs-lookup"><span data-stu-id="28ef2-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="28ef2-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="28ef2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="28ef2-105">Požadavky</span><span class="sxs-lookup"><span data-stu-id="28ef2-105">Prerequisites</span></span>

<span data-ttu-id="28ef2-106">Než začnete konfigurovat data v Common Data Service (CDS), musí být splněny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="28ef2-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="28ef2-107">Máte zřízeno prostředí CDS a Dynamics 365 Finance pro Project Operations.</span><span class="sxs-lookup"><span data-stu-id="28ef2-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="28ef2-108">V prostředí CDS jsou sdíleny informace o právnické osobě z Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="28ef2-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="28ef2-109">To znamená, že entita **Společnost** v CDS má následující záznamy:</span><span class="sxs-lookup"><span data-stu-id="28ef2-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="28ef2-110">THPM</span><span class="sxs-lookup"><span data-stu-id="28ef2-110">THPM</span></span>
  - <span data-ttu-id="28ef2-111">USPM</span><span class="sxs-lookup"><span data-stu-id="28ef2-111">USPM</span></span>
  - <span data-ttu-id="28ef2-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="28ef2-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="28ef2-113">Instalace nastavení a dat konfigurace</span><span class="sxs-lookup"><span data-stu-id="28ef2-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="28ef2-114">Stáhněte, odblokujte a rozbalte soubor [Balíček údajů o nastavení a konfiguraci](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="28ef2-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="28ef2-115">Přejděte do rozbalené složky a spusťte soubor *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="28ef2-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="28ef2-116">Na straně 1 Průvodce konfigurací migrace (CMT) Common Data Service, vyberte **Importovat data** a poté vyberte **Pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="28ef2-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrace konfigurace](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="28ef2-118">Na stránce 2 průvodce CMT vyberte **Microsoft 365** jako **Typ nasazení**.</span><span class="sxs-lookup"><span data-stu-id="28ef2-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="28ef2-119">Zaškrtněte políčka **Zobrazit seznam dostupných organizací** a **Zobrazit pokročilé**.</span><span class="sxs-lookup"><span data-stu-id="28ef2-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="28ef2-120">Vyberte oblast vašeho klienta, zadejte své přihlašovací údaje a vyberte příkaz **Přihlásit se**.</span><span class="sxs-lookup"><span data-stu-id="28ef2-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Přihlášení do konfigurace](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="28ef2-122">Na stránce 3 vyberte ze seznamu organizací v klientovi organizaci, do které chcete importovat ukázková data, a vyberte příkaz **Přihlásit se**.</span><span class="sxs-lookup"><span data-stu-id="28ef2-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="28ef2-123">Na stránce 4 vyberte soubor zip *SampleSetupAndConfigData* z rozbalené složky.</span><span class="sxs-lookup"><span data-stu-id="28ef2-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Výběr souboru ZIP](./media/3ZipFile.png)

![Vyberte soubor.](./media/4SelectAFile.png)

9. <span data-ttu-id="28ef2-126">Po výběru souboru zip vyberte **Importovat data**.</span><span class="sxs-lookup"><span data-stu-id="28ef2-126">After the zip file is selected, select **Import Data**.</span></span>

![Importovat data](./media/5ImportData.png)

10. <span data-ttu-id="28ef2-128">Import bude probíhat přibližně dvě až deset minut v závislosti na rychlosti vaší sítě.</span><span class="sxs-lookup"><span data-stu-id="28ef2-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="28ef2-129">Po dokončení importu ukončete průvodce CMT.</span><span class="sxs-lookup"><span data-stu-id="28ef2-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="28ef2-130">Zkontrolujte ve své organizaci data v následujících 26 entitách:</span><span class="sxs-lookup"><span data-stu-id="28ef2-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="28ef2-131">Měna</span><span class="sxs-lookup"><span data-stu-id="28ef2-131">Currency</span></span>
  - <span data-ttu-id="28ef2-132">Účtová osnova</span><span class="sxs-lookup"><span data-stu-id="28ef2-132">Chart of Accounts</span></span>
  - <span data-ttu-id="28ef2-133">Fiskální kalendář</span><span class="sxs-lookup"><span data-stu-id="28ef2-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="28ef2-134">Typy směnného kurzu měny</span><span class="sxs-lookup"><span data-stu-id="28ef2-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="28ef2-135">Datum platby</span><span class="sxs-lookup"><span data-stu-id="28ef2-135">Payment Day</span></span>
  - <span data-ttu-id="28ef2-136">Plán plateb</span><span class="sxs-lookup"><span data-stu-id="28ef2-136">Payment Schedule</span></span>
  - <span data-ttu-id="28ef2-137">Platební podmínka</span><span class="sxs-lookup"><span data-stu-id="28ef2-137">Payment Term</span></span>
  - <span data-ttu-id="28ef2-138">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="28ef2-138">Organizational Unit</span></span>
  - <span data-ttu-id="28ef2-139">Kontakt</span><span class="sxs-lookup"><span data-stu-id="28ef2-139">Contact</span></span>
  - <span data-ttu-id="28ef2-140">Daňová skupina</span><span class="sxs-lookup"><span data-stu-id="28ef2-140">Tax Group</span></span>
  - <span data-ttu-id="28ef2-141">Skupina zákazníků</span><span class="sxs-lookup"><span data-stu-id="28ef2-141">Customer Group</span></span>
  - <span data-ttu-id="28ef2-142">Skupina prodejců</span><span class="sxs-lookup"><span data-stu-id="28ef2-142">Vendor Group</span></span>
  - <span data-ttu-id="28ef2-143">Jednotka</span><span class="sxs-lookup"><span data-stu-id="28ef2-143">Unit</span></span>
  - <span data-ttu-id="28ef2-144">Skupina jednotek</span><span class="sxs-lookup"><span data-stu-id="28ef2-144">Unit Group</span></span>
  - <span data-ttu-id="28ef2-145">Ceník</span><span class="sxs-lookup"><span data-stu-id="28ef2-145">Price List</span></span>
  - <span data-ttu-id="28ef2-146">Ceník projektových parametrů</span><span class="sxs-lookup"><span data-stu-id="28ef2-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="28ef2-147">Frekvence faktur</span><span class="sxs-lookup"><span data-stu-id="28ef2-147">Invoice Frequency</span></span>
  - <span data-ttu-id="28ef2-148">Kategorie rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="28ef2-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="28ef2-149">Kategorie transakce</span><span class="sxs-lookup"><span data-stu-id="28ef2-149">Transaction Category</span></span>
  - <span data-ttu-id="28ef2-150">Kategorie výdaje</span><span class="sxs-lookup"><span data-stu-id="28ef2-150">Expense Category</span></span>
  - <span data-ttu-id="28ef2-151">Cena role</span><span class="sxs-lookup"><span data-stu-id="28ef2-151">Role Price</span></span>
  - <span data-ttu-id="28ef2-152">Cena kategorie transakce</span><span class="sxs-lookup"><span data-stu-id="28ef2-152">Transaction Category Price</span></span>
  - <span data-ttu-id="28ef2-153">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="28ef2-153">Characteristic</span></span>
  - <span data-ttu-id="28ef2-154">Rezervovatelný zdroj</span><span class="sxs-lookup"><span data-stu-id="28ef2-154">Bookable Resource</span></span>
  - <span data-ttu-id="28ef2-155">Přidružení kategorie rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="28ef2-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="28ef2-156">Charakteristika rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="28ef2-156">Bookable Resource Characteristic</span></span>

![Dokončit import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="28ef2-158">Aktualizace konfigurací Project Operations</span><span class="sxs-lookup"><span data-stu-id="28ef2-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="28ef2-159">Přejděte do prostředí CE.</span><span class="sxs-lookup"><span data-stu-id="28ef2-159">Navigate to the CE environment.</span></span> <span data-ttu-id="28ef2-160">Najdete jej otevřením [Centra pro správu Power Platform](https://admin.powerplatform.microsoft.com/environments), kde vyberete prostředí a poté **Otevřené prostředí**.</span><span class="sxs-lookup"><span data-stu-id="28ef2-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Otevření prostředí](./media/7OpenEnvironment.png)

2. <span data-ttu-id="28ef2-162">Přejděte do nabídky **Projekty** > **Zdroje** a poté vyberte příkaz **Nový** k vytvoření rezervovatelného zdroje pro vašeho uživatele.</span><span class="sxs-lookup"><span data-stu-id="28ef2-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Rezervovatelné zdroje](./media/8BookableResources.png)

3. <span data-ttu-id="28ef2-164">Na kartě **Obecné** vyberte uživatele správce.</span><span class="sxs-lookup"><span data-stu-id="28ef2-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="28ef2-165">Ověřte, zda se časové pásmo shoduje s časovým pásmem, ve kterém se nacházíte.</span><span class="sxs-lookup"><span data-stu-id="28ef2-165">Verify that the time zone matches the one you are in.</span></span> 

![Nový rezervovatelný zdroj](./media/9NewBookableResource.png)

4. <span data-ttu-id="28ef2-167">Na kartě **Plánování** v poli **Společnost** vyberte společnost **USPM** a poté vyberte příkaz **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="28ef2-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Karta Plánování](./media/10SchedulingTab.png)

5. <span data-ttu-id="28ef2-169">Vyberte kartu **Pracovní doba**.</span><span class="sxs-lookup"><span data-stu-id="28ef2-169">Select the **Work hours** tab.</span></span>  

![Pracovní doba](./media/11WorkHours.png)

6. <span data-ttu-id="28ef2-171">Poklepejte na libovolnou hodnotu v kalendáři a vyberte příkaz **Upravit** > **Všechny události v řadě**.</span><span class="sxs-lookup"><span data-stu-id="28ef2-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Pracovní kalendář](./media/12WorkCalendar.png)

7. <span data-ttu-id="28ef2-173">Změňte pracovní dobu na osmi (8) hodinový pracovní den, označte víkendy jako dny pracovního klidu a ujistěte se, že časové pásmo odpovídá vašemu.</span><span class="sxs-lookup"><span data-stu-id="28ef2-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="28ef2-174">Zvolte **Uložit a zavřít**.</span><span class="sxs-lookup"><span data-stu-id="28ef2-174">Select **Save and close**.</span></span>

![Aktualizace kalendáře](./media/13UpdateCalendar.png)

9. <span data-ttu-id="28ef2-176">Přejděte do nabídky **Nastavení** > **Šablony kalendáře** a vyberte položku **Nová**.</span><span class="sxs-lookup"><span data-stu-id="28ef2-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Šablony kalendářů](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="28ef2-178">Zadejte název, vyberte zdroj šablony, který jste vytvořili, a pak vyberte příkaz **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="28ef2-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Uložení šablony kalendáře](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="28ef2-180">Přejděte do části **Parametry** a dvakrát klikněte na záznam.</span><span class="sxs-lookup"><span data-stu-id="28ef2-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektové parametry](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="28ef2-182">Aktualizujte následující pole:</span><span class="sxs-lookup"><span data-stu-id="28ef2-182">Update the following fields:</span></span>

 - <span data-ttu-id="28ef2-183">**Výchozí společnost**: USPM</span><span class="sxs-lookup"><span data-stu-id="28ef2-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="28ef2-184">**Výchozí organizační jednotka**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="28ef2-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="28ef2-185">**Četnost faktur**: Sedmý a poslední den</span><span class="sxs-lookup"><span data-stu-id="28ef2-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="28ef2-186">**Šablona pracovní doby**: Změňte na šablonu, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="28ef2-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="28ef2-187">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="28ef2-187">Select **Save**.</span></span> 

![Aktualizované projektové parametry](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
