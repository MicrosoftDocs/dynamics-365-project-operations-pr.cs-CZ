---
title: Použití ukázkového nastavení a data konfigurace
description: Toto téma poskytuje informace o tom, jak použít ukázková nastavení a konfigurační data pro Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073645"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="54221-103">Použít ukázkové nastavení a konfigurační data pro omezené nasazení Project Operations - od obchodu po pro forma fakturaci</span><span class="sxs-lookup"><span data-stu-id="54221-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="54221-104">_\*\*Omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="54221-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="54221-105">Stáhněte si [Balíček kmenových dat](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="54221-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="54221-106">Přejděte do složky *ProjOpsDemoDataSetupAndMaster - integrovaný CMT* a spusťte soubor *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="54221-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="54221-107">Na straně 1 Průvodce konfigurací migrace (CMT) Common Data Service, vyberte **Importovat data** a poté vyberte **Pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="54221-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrace konfigurace](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="54221-109">Na stránce 2 průvodce CMT vyberte **Microsoft 365** jako **Typ nasazení**.</span><span class="sxs-lookup"><span data-stu-id="54221-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="54221-110">Zaškrtněte políčka **Zobrazit seznam dostupných organizací** a **Zobrazit pokročilé**.</span><span class="sxs-lookup"><span data-stu-id="54221-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="54221-111">Vyberte oblast vašeho klienta, zadejte své přihlašovací údaje a pak vyberte **Přihlásit se**.</span><span class="sxs-lookup"><span data-stu-id="54221-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Přihlášení do konfigurace](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="54221-113">Na stránce 3 ze seznamu organizací v klientovi vyberte, do které organizace chcete importovat ukázková data, a poté vyberte **Přihlásit se**.</span><span class="sxs-lookup"><span data-stu-id="54221-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="54221-114">Na stránce 4 vyberte soubor zip *MasterAndSetupData* z rozbalené složky *ProjOpsDemoDataSetupAndMaster - integrovaný CMT*.</span><span class="sxs-lookup"><span data-stu-id="54221-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Soubor ZIP](./media/3ZipFile.png)

![Vyberte soubor.](./media/4SelectAFile.png)

9. <span data-ttu-id="54221-117">Po výběru souboru zip vyberte **Importovat data**.</span><span class="sxs-lookup"><span data-stu-id="54221-117">After the zip file is selected, select **Import Data**.</span></span>

![Import dat](./media/5ImportData.png)

10. <span data-ttu-id="54221-119">Import bude probíhat přibližně dvě až deset minut v závislosti na rychlosti vaší sítě.</span><span class="sxs-lookup"><span data-stu-id="54221-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="54221-120">Po dokončení ukončete průvodce CMT.</span><span class="sxs-lookup"><span data-stu-id="54221-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="54221-121">Zkontrolujte ve své organizaci data v následujících 20 entitách:</span><span class="sxs-lookup"><span data-stu-id="54221-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="54221-122">Měna</span><span class="sxs-lookup"><span data-stu-id="54221-122">Currency</span></span>
- <span data-ttu-id="54221-123">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="54221-123">Organizational Unit</span></span>
- <span data-ttu-id="54221-124">Kontakt</span><span class="sxs-lookup"><span data-stu-id="54221-124">Contact</span></span>
- <span data-ttu-id="54221-125">Daňová skupina</span><span class="sxs-lookup"><span data-stu-id="54221-125">Tax Group</span></span>
- <span data-ttu-id="54221-126">Skupina zákazníků</span><span class="sxs-lookup"><span data-stu-id="54221-126">Customer Group</span></span>
- <span data-ttu-id="54221-127">Jednotka</span><span class="sxs-lookup"><span data-stu-id="54221-127">Unit</span></span>
- <span data-ttu-id="54221-128">Skupina jednotek</span><span class="sxs-lookup"><span data-stu-id="54221-128">Unit Group</span></span>
- <span data-ttu-id="54221-129">Ceník</span><span class="sxs-lookup"><span data-stu-id="54221-129">Price List</span></span>
- <span data-ttu-id="54221-130">Ceník projektových parametrů</span><span class="sxs-lookup"><span data-stu-id="54221-130">Project Parameter Price List</span></span>
- <span data-ttu-id="54221-131">Frekvence faktur</span><span class="sxs-lookup"><span data-stu-id="54221-131">Invoice Frequency</span></span>
- <span data-ttu-id="54221-132">Podrobnosti četnosti faktury</span><span class="sxs-lookup"><span data-stu-id="54221-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="54221-133">Kategorie rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="54221-133">Bookable Resource Category</span></span>
- <span data-ttu-id="54221-134">Kategorie transakce</span><span class="sxs-lookup"><span data-stu-id="54221-134">Transaction Category</span></span>
- <span data-ttu-id="54221-135">Kategorie výdaje</span><span class="sxs-lookup"><span data-stu-id="54221-135">Expense Category</span></span>
- <span data-ttu-id="54221-136">Cena role</span><span class="sxs-lookup"><span data-stu-id="54221-136">Role Price</span></span>
- <span data-ttu-id="54221-137">Cena kategorie transakce</span><span class="sxs-lookup"><span data-stu-id="54221-137">Transaction Category Price</span></span>
- <span data-ttu-id="54221-138">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="54221-138">Characteristic</span></span>
- <span data-ttu-id="54221-139">Rezervovatelný zdroj</span><span class="sxs-lookup"><span data-stu-id="54221-139">Bookable Resource</span></span>
- <span data-ttu-id="54221-140">Přidružení kategorie rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="54221-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="54221-141">Charakteristika rezervovatelného zdroje</span><span class="sxs-lookup"><span data-stu-id="54221-141">Bookable Resource Characteristic</span></span>

![Dokončit import](./media/6CompleteImport.png)
