---
title: Nastavení a použití dat konfigurace ve službě Common Data Service pro Project Operations
description: Toto téma poskytuje informace o tom, jak nastavit a použít konfigurační data v aplikaci Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948800"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="84bcd-103">Nastavení a použití dat konfigurace ve službě Common Data Service pro Project Operations</span><span class="sxs-lookup"><span data-stu-id="84bcd-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="84bcd-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="84bcd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="84bcd-105">Instalace nastavení a dat konfigurace</span><span class="sxs-lookup"><span data-stu-id="84bcd-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="84bcd-106">Stáhněte, odblokujte a rozbalte soubor [Balíček údajů o nastavení a konfiguraci](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="84bcd-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="84bcd-107">Přejděte do rozbalené složky a spusťte soubor *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="84bcd-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="84bcd-108">Na straně 1 Průvodce konfigurací migrace (CMT) Common Data Service, vyberte **Importovat data** a poté vyberte **Pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="84bcd-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrace konfigurace](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="84bcd-110">Na stránce 2 průvodce CMT vyberte **Office 365** jako **Typ nasazení**.</span><span class="sxs-lookup"><span data-stu-id="84bcd-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="84bcd-111">Zaškrtněte políčka **Zobrazit seznam dostupných organizací** a **Zobrazit pokročilé**.</span><span class="sxs-lookup"><span data-stu-id="84bcd-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="84bcd-112">Vyberte oblast vašeho klienta, zadejte své přihlašovací údaje a vyberte příkaz **Přihlásit se**.</span><span class="sxs-lookup"><span data-stu-id="84bcd-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Přihlášení do konfigurace](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="84bcd-114">Na stránce 3 vyberte ze seznamu organizací v klientovi organizaci, do které chcete importovat ukázková data, a vyberte příkaz **Přihlásit se**.</span><span class="sxs-lookup"><span data-stu-id="84bcd-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="84bcd-115">Na stránce 4 vyberte soubor zip *SampleSetupAndConfigData* z rozbalené složky.</span><span class="sxs-lookup"><span data-stu-id="84bcd-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Výběr souboru ZIP](./media/3ZipFile.png)

![Vyberte soubor.](./media/4SelectAFile.png)

9. <span data-ttu-id="84bcd-118">Po výběru souboru zip vyberte **Importovat data**.</span><span class="sxs-lookup"><span data-stu-id="84bcd-118">After the zip file is selected, select **Import Data**.</span></span>

![Importovat data](./media/5ImportData.png)

10. <span data-ttu-id="84bcd-120">Import bude probíhat přibližně dvě až deset minut v závislosti na rychlosti vaší sítě.</span><span class="sxs-lookup"><span data-stu-id="84bcd-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="84bcd-121">Po dokončení importu ukončete průvodce CMT.</span><span class="sxs-lookup"><span data-stu-id="84bcd-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="84bcd-122">Zkontrolujte ve své organizaci data v následujících 19 entitách:</span><span class="sxs-lookup"><span data-stu-id="84bcd-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="84bcd-123">Měna</span><span class="sxs-lookup"><span data-stu-id="84bcd-123">Currency</span></span>
  - <span data-ttu-id="84bcd-124">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="84bcd-124">Organizational Unit</span></span>
  - <span data-ttu-id="84bcd-125">Kontakt</span><span class="sxs-lookup"><span data-stu-id="84bcd-125">Contact</span></span>
  - <span data-ttu-id="84bcd-126">Daňová skupina</span><span class="sxs-lookup"><span data-stu-id="84bcd-126">Tax Group</span></span>
  - <span data-ttu-id="84bcd-127">Skupina zákazníků</span><span class="sxs-lookup"><span data-stu-id="84bcd-127">Customer Group</span></span>
  - <span data-ttu-id="84bcd-128">Jednotka</span><span class="sxs-lookup"><span data-stu-id="84bcd-128">Unit</span></span>
  - <span data-ttu-id="84bcd-129">Skupina jednotek</span><span class="sxs-lookup"><span data-stu-id="84bcd-129">Unit Group</span></span>
  - <span data-ttu-id="84bcd-130">Ceník</span><span class="sxs-lookup"><span data-stu-id="84bcd-130">Price List</span></span>
  - <span data-ttu-id="84bcd-131">Ceník projektových parametrů</span><span class="sxs-lookup"><span data-stu-id="84bcd-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="84bcd-132">Frekvence faktur</span><span class="sxs-lookup"><span data-stu-id="84bcd-132">Invoice Frequency</span></span>
  - <span data-ttu-id="84bcd-133">Kategorie rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="84bcd-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="84bcd-134">Kategorie transakce</span><span class="sxs-lookup"><span data-stu-id="84bcd-134">Transaction Category</span></span>
  - <span data-ttu-id="84bcd-135">Kategorie výdaje</span><span class="sxs-lookup"><span data-stu-id="84bcd-135">Expense Category</span></span>
  - <span data-ttu-id="84bcd-136">Cena role</span><span class="sxs-lookup"><span data-stu-id="84bcd-136">Role Price</span></span>
  - <span data-ttu-id="84bcd-137">Cena kategorie transakce</span><span class="sxs-lookup"><span data-stu-id="84bcd-137">Transaction Category Price</span></span>
  - <span data-ttu-id="84bcd-138">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="84bcd-138">Characteristic</span></span>
  - <span data-ttu-id="84bcd-139">Rezervovatelný zdroj</span><span class="sxs-lookup"><span data-stu-id="84bcd-139">Bookable Resource</span></span>
  - <span data-ttu-id="84bcd-140">Přidružení kategorie rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="84bcd-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="84bcd-141">Charakteristika rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="84bcd-141">Bookable Resource Characteristic</span></span>

![Dokončit import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="84bcd-143">Aktualizace konfigurací Project Operations</span><span class="sxs-lookup"><span data-stu-id="84bcd-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="84bcd-144">Přejděte do prostředí CE.</span><span class="sxs-lookup"><span data-stu-id="84bcd-144">Navigate to the CE environment.</span></span> <span data-ttu-id="84bcd-145">Najdete jej otevřením [Centra pro správu Power Platform](https://admin.powerplatform.microsoft.com/environments), kde vyberete prostředí a poté **Otevřené prostředí**.</span><span class="sxs-lookup"><span data-stu-id="84bcd-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Otevření prostředí](./media/7OpenEnvironment.png)

2. <span data-ttu-id="84bcd-147">Přejděte do nabídky **Projekty** > **Zdroje** a poté vyberte příkaz **Nový** k vytvoření rezervovatelného zdroje pro vašeho uživatele.</span><span class="sxs-lookup"><span data-stu-id="84bcd-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Rezervovatelné zdroje](./media/8BookableResources.png)

3. <span data-ttu-id="84bcd-149">Na kartě **Obecné** vyberte uživatele správce.</span><span class="sxs-lookup"><span data-stu-id="84bcd-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="84bcd-150">Ověřte, zda se časové pásmo shoduje s časovým pásmem, ve kterém se nacházíte.</span><span class="sxs-lookup"><span data-stu-id="84bcd-150">Verify that the time zone matches the one you are in.</span></span> 

![Nový rezervovatelný zdroj](./media/9NewBookableResource.png)

4. <span data-ttu-id="84bcd-152">Na kartě **Plánování** v poli **Společnost** vyberte společnost **USPM** a poté vyberte příkaz **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="84bcd-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Karta Plánování](./media/10SchedulingTab.png)

5. <span data-ttu-id="84bcd-154">Vyberte kartu **Pracovní doba**.</span><span class="sxs-lookup"><span data-stu-id="84bcd-154">Select the **Work hours** tab.</span></span>  

![Pracovní doba](./media/11WorkHours.png)

6. <span data-ttu-id="84bcd-156">Poklepejte na libovolnou hodnotu v kalendáři a vyberte příkaz **Upravit** > **Všechny události v řadě**.</span><span class="sxs-lookup"><span data-stu-id="84bcd-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Pracovní kalendář](./media/12WorkCalendar.png)

7. <span data-ttu-id="84bcd-158">Změňte pracovní dobu na osmi (8) hodinový pracovní den, označte víkendy jako dny pracovního klidu a ujistěte se, že časové pásmo odpovídá vašemu.</span><span class="sxs-lookup"><span data-stu-id="84bcd-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="84bcd-159">Zvolte **Uložit a zavřít**.</span><span class="sxs-lookup"><span data-stu-id="84bcd-159">Select **Save and close**.</span></span>

![Aktualizace kalendáře](./media/13UpdateCalendar.png)

9. <span data-ttu-id="84bcd-161">Přejděte do nabídky **Nastavení** > **Šablony kalendáře** a vyberte položku **Nová**.</span><span class="sxs-lookup"><span data-stu-id="84bcd-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Šablony kalendářů](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="84bcd-163">Zadejte název, vyberte zdroj šablony, který jste vytvořili, a pak vyberte příkaz **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="84bcd-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Uložení šablony kalendáře](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="84bcd-165">Přejděte do části **Parametry** a dvakrát klikněte na záznam.</span><span class="sxs-lookup"><span data-stu-id="84bcd-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektové parametry](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="84bcd-167">Aktualizujte následující pole:</span><span class="sxs-lookup"><span data-stu-id="84bcd-167">Update the following fields:</span></span>

 - <span data-ttu-id="84bcd-168">**Výchozí společnost**: USPM</span><span class="sxs-lookup"><span data-stu-id="84bcd-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="84bcd-169">**Výchozí organizační jednotka**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="84bcd-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="84bcd-170">**Četnost faktur**: Sedmý a poslední den</span><span class="sxs-lookup"><span data-stu-id="84bcd-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="84bcd-171">**Šablona pracovní doby**: Změňte na šablonu, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="84bcd-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="84bcd-172">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="84bcd-172">Select **Save**.</span></span> 

![Aktualizované projektové parametry](./media/17UpdatedProjectParameters.png)
