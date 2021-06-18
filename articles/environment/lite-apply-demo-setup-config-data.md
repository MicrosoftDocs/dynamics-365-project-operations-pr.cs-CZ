---
title: Použití ukázkového nastavení a data konfigurace – omezené
description: Toto téma poskytuje informace o tom, jak použít ukázková nastavení a konfigurační data pro Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997143"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="57f1a-103">Použití ukázkového nastavení a data konfigurace pro Project Operations – omezené</span><span class="sxs-lookup"><span data-stu-id="57f1a-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="57f1a-104">_\*\*Omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="57f1a-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="57f1a-105">Požadavky</span><span class="sxs-lookup"><span data-stu-id="57f1a-105">Prerequisites</span></span>

<span data-ttu-id="57f1a-106">Před zahájením konfigurace musíte mít mít zřízeno prostředí  Common Data Service (CDS) pro Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="57f1a-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="57f1a-107">Pokyny</span><span class="sxs-lookup"><span data-stu-id="57f1a-107">Instructions</span></span>

1. <span data-ttu-id="57f1a-108">Stáhněte si [Balíček kmenových dat](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span><span class="sxs-lookup"><span data-stu-id="57f1a-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="57f1a-109">Přejděte do složky *ProjOpsSampleSetupData – pouze CMT CE* a spusťte spustitelný soubor *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="57f1a-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="57f1a-110">Na straně 1 Průvodce konfigurací migrace (CMT) Common Data Service, vyberte **Importovat data** a poté vyberte **Pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="57f1a-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migrace konfigurace](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="57f1a-112">Na stránce 2 průvodce CMT vyberte **Microsoft 365** jako **Typ nasazení**.</span><span class="sxs-lookup"><span data-stu-id="57f1a-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="57f1a-113">Zaškrtněte políčka **Zobrazit seznam dostupných organizací** a **Zobrazit pokročilé**.</span><span class="sxs-lookup"><span data-stu-id="57f1a-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="57f1a-114">Vyberte oblast vašeho klienta, zadejte své přihlašovací údaje a pak vyberte **Přihlásit se**.</span><span class="sxs-lookup"><span data-stu-id="57f1a-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Přihlášení do konfigurace](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="57f1a-116">Na stránce 3 ze seznamu organizací v klientovi vyberte, do které organizace chcete importovat ukázková data, a poté vyberte **Přihlásit se**.</span><span class="sxs-lookup"><span data-stu-id="57f1a-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="57f1a-117">Na stránce 4 vyberte soubor zip *SampleSetupAndConfigData* z rozbalené složky *ProjOpsSampleSetupData – CE pouze CMT*.</span><span class="sxs-lookup"><span data-stu-id="57f1a-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![Soubor ZIP](./media/3ZipFile.png)

   ![Vyberte soubor](./media/4SelectAFile.png)

9. <span data-ttu-id="57f1a-120">Po výběru souboru zip vyberte **Importovat data**.</span><span class="sxs-lookup"><span data-stu-id="57f1a-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Import dat](./media/5ImportData.png)

10. <span data-ttu-id="57f1a-122">Import bude probíhat přibližně dvě až deset minut v závislosti na rychlosti vaší sítě.</span><span class="sxs-lookup"><span data-stu-id="57f1a-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="57f1a-123">Po dokončení ukončete průvodce CMT.</span><span class="sxs-lookup"><span data-stu-id="57f1a-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="57f1a-124">Zkontrolujte ve své organizaci data v následujících 18 entitách:</span><span class="sxs-lookup"><span data-stu-id="57f1a-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="57f1a-125">Měna</span><span class="sxs-lookup"><span data-stu-id="57f1a-125">Currency</span></span>
    -   <span data-ttu-id="57f1a-126">Účet</span><span class="sxs-lookup"><span data-stu-id="57f1a-126">Account</span></span>
    -   <span data-ttu-id="57f1a-127">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="57f1a-127">Organizational Unit</span></span>
    -   <span data-ttu-id="57f1a-128">Kontakt</span><span class="sxs-lookup"><span data-stu-id="57f1a-128">Contact</span></span>
    -   <span data-ttu-id="57f1a-129">Jednotka</span><span class="sxs-lookup"><span data-stu-id="57f1a-129">Unit</span></span>
    -   <span data-ttu-id="57f1a-130">Skupina jednotek</span><span class="sxs-lookup"><span data-stu-id="57f1a-130">Unit Group</span></span>
    -   <span data-ttu-id="57f1a-131">Ceník</span><span class="sxs-lookup"><span data-stu-id="57f1a-131">Price List</span></span>
    -   <span data-ttu-id="57f1a-132">Ceník projektových parametrů</span><span class="sxs-lookup"><span data-stu-id="57f1a-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="57f1a-133">Frekvence faktur</span><span class="sxs-lookup"><span data-stu-id="57f1a-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="57f1a-134">Kategorie rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="57f1a-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="57f1a-135">Kategorie transakce</span><span class="sxs-lookup"><span data-stu-id="57f1a-135">Transaction Category</span></span>
    -   <span data-ttu-id="57f1a-136">Kategorie výdaje</span><span class="sxs-lookup"><span data-stu-id="57f1a-136">Expense Category</span></span>
    -   <span data-ttu-id="57f1a-137">Cena role</span><span class="sxs-lookup"><span data-stu-id="57f1a-137">Role Price</span></span>
    -   <span data-ttu-id="57f1a-138">Cena kategorie transakce</span><span class="sxs-lookup"><span data-stu-id="57f1a-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="57f1a-139">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="57f1a-139">Characteristic</span></span>
    -   <span data-ttu-id="57f1a-140">Rezervovatelný zdroj</span><span class="sxs-lookup"><span data-stu-id="57f1a-140">Bookable Resource</span></span>
    -   <span data-ttu-id="57f1a-141">Přidružení kategorie rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="57f1a-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="57f1a-142">Charakteristika rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="57f1a-142">Bookable Resource Characteristic</span></span>

    ![Dokončit import](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
