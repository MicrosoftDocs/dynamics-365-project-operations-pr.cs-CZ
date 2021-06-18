---
title: Použití ukázkových dat na prostředí aplikace Finance hostované v cloudu
description: Toto téma vysvětluje, jak použít ukázková data z Project Operations na prostředí Dynamics 365 Finance hostované v cloudu.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7d8a198b3bfd71ae08bc338d17896519b5ffd6b8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000142"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="cfe25-103">Použití ukázkových dat na prostředí aplikace Finance hostované v cloudu</span><span class="sxs-lookup"><span data-stu-id="cfe25-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="cfe25-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="cfe25-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cfe25-105">Toto téma je použitelné pouze pro Microsoft Dynamics 365 Finance ve verzi 10.0.13 a lze ho provést pouze v prostředí hostovaném v cloudu.</span><span class="sxs-lookup"><span data-stu-id="cfe25-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="cfe25-106">Kroky v tomto tématu dokončete **PŘED** použitím aktualizací kvality na prostředí.</span><span class="sxs-lookup"><span data-stu-id="cfe25-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="cfe25-107">Ve svém projektu LCS otevřete stránku **Podrobnosti o prostředí**.</span><span class="sxs-lookup"><span data-stu-id="cfe25-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="cfe25-108">Všimněte si, že obsahuje podrobnosti potřebné pro připojení k prostředí pomocí protokolu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="cfe25-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Podrobnosti prostředí ](./media/1EnvironmentDetails.png)

<span data-ttu-id="cfe25-110">První sada zvýrazněných přihlašovacích údajů jsou přihlašovací údaje místního účtu a obsahují hypertextový odkaz na připojení ke vzdálené ploše.</span><span class="sxs-lookup"><span data-stu-id="cfe25-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="cfe25-111">Přihlašovací údaje zahrnují uživatelské jméno a heslo správce prostředí.</span><span class="sxs-lookup"><span data-stu-id="cfe25-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="cfe25-112">Druhá sada přihlašovacích údajů se používá pro přihlášení k serveru SQL v tomto prostředí.</span><span class="sxs-lookup"><span data-stu-id="cfe25-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="cfe25-113">Připojte se vzdáleně k prostředí pomocí hypertextového odkazu v části **Místní účty** a k ověření použijte **Přihlašovací údaje místního účtu**.</span><span class="sxs-lookup"><span data-stu-id="cfe25-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="cfe25-114">Přejděte na části **Internetová informační služba** > **Fondy aplikací** > **AOSService** a zastavte službu.</span><span class="sxs-lookup"><span data-stu-id="cfe25-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="cfe25-115">V tomto okamžiku zastavujete službu, abyste mohli pokračovat v nahrazování databáze SQL.</span><span class="sxs-lookup"><span data-stu-id="cfe25-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Zastavit AOS](./media/2StopAOS.png)

4. <span data-ttu-id="cfe25-117">Přejděte do části **Služby** a zastavte následující dvě položky:</span><span class="sxs-lookup"><span data-stu-id="cfe25-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="cfe25-118">Microsoft Dynamics 365 Unified Operations: Služba správy dávek</span><span class="sxs-lookup"><span data-stu-id="cfe25-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="cfe25-119">Microsoft Dynamics 365 Unified Operations: Platforma importu a exportu dat</span><span class="sxs-lookup"><span data-stu-id="cfe25-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Zastavit služby](./media/3StopServices.png)

5. <span data-ttu-id="cfe25-121">Otevřete aplikaci Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="cfe25-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="cfe25-122">Přihlaste se pomocí přihlašovacích údajů serveru SQL a použijte uživatele axdbadmin a jeho heslo, uvedené na stránce LCS **Podrobnosti o prostředí**.</span><span class="sxs-lookup"><span data-stu-id="cfe25-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="cfe25-124">V Průzkumníku objektů zvolte **Databáze** a vyhledejte **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="cfe25-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="cfe25-125">Databázi nahradíte novou databází, která se nachází v [Centru stahování](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="cfe25-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="cfe25-126">Zkopírujte soubor zip na virtuální počítač, ke kterému jste vzdáleně připojeni, a rozbalte obsah archivu.</span><span class="sxs-lookup"><span data-stu-id="cfe25-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="cfe25-127">V aplikaci SQL Server Management Studio pravým tlačítkem klikněte na položku **AxDB** a potom vyberte postupně **Úkoly** > **Obnovit** > **Databáze**.</span><span class="sxs-lookup"><span data-stu-id="cfe25-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Obnova databáze](./media/5RestoreDatabase.png)

9. <span data-ttu-id="cfe25-129">Vyberte **Zdrojové zařízení** a přejděte na soubor extrahovaný z archivu, který jste zkopírovali.</span><span class="sxs-lookup"><span data-stu-id="cfe25-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Zdrojová zařízení](./media/6SourceDevice.png)

10. <span data-ttu-id="cfe25-131">Vyberte položku **Možnosti** a potom vyberte možnosti **Přepsat existující databázi** a **Zavřít stávající připojení k cílové databázi**.</span><span class="sxs-lookup"><span data-stu-id="cfe25-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="cfe25-132">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfe25-132">Select **OK**.</span></span>

![Obnovit nastavení](./media/7RestoreSetting.png)

<span data-ttu-id="cfe25-134">Obdržíte potvrzení, že obnovení AXDB proběhlo úspěšně.</span><span class="sxs-lookup"><span data-stu-id="cfe25-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="cfe25-135">Po obdržení tohoto potvrzení můžete zavřít aplikaci SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="cfe25-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="cfe25-136">Přejděte zpět na nabídku **Internetová informační služba** > **Fondy aplikací** > **AOSService** a spusťte službu AOSService.</span><span class="sxs-lookup"><span data-stu-id="cfe25-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="cfe25-137">Přejděte do části **Služby** a spusťte dvě služby, které jste dříve zastavili.</span><span class="sxs-lookup"><span data-stu-id="cfe25-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="cfe25-138">Vyhledejte nástroj AdminUserProvisioning na tomto virtuálním počítači.</span><span class="sxs-lookup"><span data-stu-id="cfe25-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="cfe25-139">Hledejte soubor K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="cfe25-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="cfe25-140">Spusťte soubor .ext pomocí své uživatelské adresy v poli **E-mailová adresa**.</span><span class="sxs-lookup"><span data-stu-id="cfe25-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="cfe25-141">Vyberte položku **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="cfe25-141">Select **Submit**.</span></span>

![Admin User Provisioning](./media/8AdminUserProvisioning.png)

<span data-ttu-id="cfe25-143">Tato akce může trvat několik minut.</span><span class="sxs-lookup"><span data-stu-id="cfe25-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="cfe25-144">Měla by se zobrazit potvrzovací zpráva, že uživatel správce byl úspěšně aktualizován.</span><span class="sxs-lookup"><span data-stu-id="cfe25-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="cfe25-145">Nakonec spusťte příkazový řádek jako správce a proveďte příkaz iisreset</span><span class="sxs-lookup"><span data-stu-id="cfe25-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Obnova IIS](./media/9IISReset.png)

18. <span data-ttu-id="cfe25-147">Ukončete relaci vzdálené plochy a na stránce LCS **Podrobnosti o prostředí** se přihlaste do prostředí a zkontrolujte, že funguje podle očekávání.</span><span class="sxs-lookup"><span data-stu-id="cfe25-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]