---
title: Použití ukázkového nastavení a data konfigurace – omezené
description: Toto téma poskytuje informace o tom, jak použít ukázková nastavení a konfigurační data pro Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089111"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="cc7c5-103">Použití ukázkového nastavení a data konfigurace pro Project Operations – omezené</span><span class="sxs-lookup"><span data-stu-id="cc7c5-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="cc7c5-104">_\*\*Omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="cc7c5-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="cc7c5-105">Požadavky</span><span class="sxs-lookup"><span data-stu-id="cc7c5-105">Prerequisites</span></span>

<span data-ttu-id="cc7c5-106">Před zahájením konfigurace musíte mít mít zřízeno prostředí  Common Data Service (CDS) pro Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="cc7c5-107">Pokyny</span><span class="sxs-lookup"><span data-stu-id="cc7c5-107">Instructions</span></span>

1. <span data-ttu-id="cc7c5-108">Stáhněte si [Balíček kmenových dat](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="cc7c5-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="cc7c5-109">Přejděte do složky *ProjOpsDemoDataSetupAndMaster - integrovaný CMT* a spusťte soubor *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="cc7c5-110">Na straně 1 Průvodce konfigurací migrace (CMT) Common Data Service, vyberte **Importovat data** a poté vyberte **Pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migrace konfigurace](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="cc7c5-112">Na stránce 2 průvodce CMT vyberte **Microsoft 365** jako **Typ nasazení**.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="cc7c5-113">Zaškrtněte políčka **Zobrazit seznam dostupných organizací** a **Zobrazit pokročilé**.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="cc7c5-114">Vyberte oblast vašeho klienta, zadejte své přihlašovací údaje a pak vyberte **Přihlásit se**.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Přihlášení do konfigurace](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="cc7c5-116">Na stránce 3 ze seznamu organizací v klientovi vyberte, do které organizace chcete importovat ukázková data, a poté vyberte **Přihlásit se**.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="cc7c5-117">Na stránce 4 vyberte soubor zip *MasterAndSetupData* z rozbalené složky *ProjOpsDemoDataSetupAndMaster - integrovaný CMT*.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![Soubor ZIP](./media/3ZipFile.png)

   ![Vyberte soubor.](./media/4SelectAFile.png)

9. <span data-ttu-id="cc7c5-120">Po výběru souboru zip vyberte **Importovat data**.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Import dat](./media/5ImportData.png)

10. <span data-ttu-id="cc7c5-122">Import bude probíhat přibližně dvě až deset minut v závislosti na rychlosti vaší sítě.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="cc7c5-123">Po dokončení ukončete průvodce CMT.</span><span class="sxs-lookup"><span data-stu-id="cc7c5-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="cc7c5-124">Zkontrolujte ve své organizaci data v následujících 20 entitách:</span><span class="sxs-lookup"><span data-stu-id="cc7c5-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="cc7c5-125">Měna</span><span class="sxs-lookup"><span data-stu-id="cc7c5-125">Currency</span></span>
    -   <span data-ttu-id="cc7c5-126">Účet</span><span class="sxs-lookup"><span data-stu-id="cc7c5-126">Account</span></span>
    -   <span data-ttu-id="cc7c5-127">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="cc7c5-127">Organizational Unit</span></span>
    -   <span data-ttu-id="cc7c5-128">Kontakt</span><span class="sxs-lookup"><span data-stu-id="cc7c5-128">Contact</span></span>
    -   <span data-ttu-id="cc7c5-129">Jednotka</span><span class="sxs-lookup"><span data-stu-id="cc7c5-129">Unit</span></span>
    -   <span data-ttu-id="cc7c5-130">Skupina jednotek</span><span class="sxs-lookup"><span data-stu-id="cc7c5-130">Unit Group</span></span>
    -   <span data-ttu-id="cc7c5-131">Ceník</span><span class="sxs-lookup"><span data-stu-id="cc7c5-131">Price List</span></span>
    -   <span data-ttu-id="cc7c5-132">Ceník projektových parametrů</span><span class="sxs-lookup"><span data-stu-id="cc7c5-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="cc7c5-133">Frekvence faktur</span><span class="sxs-lookup"><span data-stu-id="cc7c5-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="cc7c5-134">Kategorie rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="cc7c5-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="cc7c5-135">Kategorie transakce</span><span class="sxs-lookup"><span data-stu-id="cc7c5-135">Transaction Category</span></span>
    -   <span data-ttu-id="cc7c5-136">Kategorie výdaje</span><span class="sxs-lookup"><span data-stu-id="cc7c5-136">Expense Category</span></span>
    -   <span data-ttu-id="cc7c5-137">Cena role</span><span class="sxs-lookup"><span data-stu-id="cc7c5-137">Role Price</span></span>
    -   <span data-ttu-id="cc7c5-138">Cena kategorie transakce</span><span class="sxs-lookup"><span data-stu-id="cc7c5-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="cc7c5-139">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="cc7c5-139">Characteristic</span></span>
    -   <span data-ttu-id="cc7c5-140">Rezervovatelný zdroj</span><span class="sxs-lookup"><span data-stu-id="cc7c5-140">Bookable Resource</span></span>
    -   <span data-ttu-id="cc7c5-141">Přidružení kategorie rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="cc7c5-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="cc7c5-142">Charakteristika rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="cc7c5-142">Bookable Resource Characteristic</span></span>

    ![Dokončit import](./media/6CompleteImport.png)
