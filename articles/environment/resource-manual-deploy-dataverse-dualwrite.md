---
title: Ruční nasazení aplikace Project Operations Dataverse s podporou duálního zápisu
description: Toto téma vysvětluje, jak ručně nasadit aplikaci Project Operations Dataverse tak, aby podporovala duální zápis.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274000"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="44635-103">Ruční nasazení aplikace Project Operations Dataverse s podporou duálního zápisu</span><span class="sxs-lookup"><span data-stu-id="44635-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="44635-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="44635-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="44635-105">Toto téma vysvětluje, jak ručně nasadit Microsoft Dynamics 365 Project Operations v Microsoft Dataverse tak, aby podporovala duální zápis.</span><span class="sxs-lookup"><span data-stu-id="44635-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="44635-106">Project Operations detekuje konfiguraci prostředí a přidá další podporu pro duální zápis, pokud jsou splněny předpoklady.</span><span class="sxs-lookup"><span data-stu-id="44635-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="44635-107">Během nasazení do Microsoft Dynamics Lifecycle Services (LCS), pokud jste postupovali podle pokynů v tomto tématu, můžete přeskočit nasazení integrace Microsoft Power Platform (dříve známá jako prostředí Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="44635-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="44635-108">Proces nasazení Project Operations v Dataverse podporující dvojitý zápis má čtyři hlavní kroky:</span><span class="sxs-lookup"><span data-stu-id="44635-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="44635-109">[Vytvořte nové prostředí v Dataverse, který podporuje duální zápis](#create).</span><span class="sxs-lookup"><span data-stu-id="44635-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="44635-110">[Přidejte do prostředí předpoklady pro duální zápis](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="44635-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="44635-111">[Přidejte aplikaci Project Operations Dataverse](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="44635-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="44635-112">[Propojte svá prostředí](#link)</span><span class="sxs-lookup"><span data-stu-id="44635-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="44635-113">Vytvořte nové prostředí v Dataverse, které podporuje duální zápis.</span><span class="sxs-lookup"><span data-stu-id="44635-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="44635-114">Chcete-li tento postup dokončit, musíte se přihlásit jako správce.</span><span class="sxs-lookup"><span data-stu-id="44635-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="44635-115">Otevřete [Centrum pro správu Power Platform](https://admin.powerplatform.com) a přihlaste se jako správce.</span><span class="sxs-lookup"><span data-stu-id="44635-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="44635-116">Vytvořit nové prostředí a pojmenujte jej.</span><span class="sxs-lookup"><span data-stu-id="44635-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="44635-117">Vyberte typ prostředí.</span><span class="sxs-lookup"><span data-stu-id="44635-117">Select the environment type.</span></span> <span data-ttu-id="44635-118">Pokud jste se zaregistrovali k nabídce zkušební verze, vyberte **Zkušební verze (na základě předplatného)**.</span><span class="sxs-lookup"><span data-stu-id="44635-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="44635-119">Potvrďte oblast nasazení.</span><span class="sxs-lookup"><span data-stu-id="44635-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="44635-120">Povolte možnost **Vytvořit databázi pro toto prostředí**.</span><span class="sxs-lookup"><span data-stu-id="44635-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="44635-121">Potvrďte jazyk a poté potvrďte, že měna odpovídá měně vaší aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="44635-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="44635-122">Povolte možnost **Aplikace Dynamics 365** a potvrďte, že je pole **Automaticky nasadit tyto aplikace** nastaveno na **Žádné**.</span><span class="sxs-lookup"><span data-stu-id="44635-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="44635-123">Přidejte skupinu zabezpečení, pokud je požadována.</span><span class="sxs-lookup"><span data-stu-id="44635-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="44635-124">Výběrem možnosti **Uložit** vytvořte prostředí.</span><span class="sxs-lookup"><span data-stu-id="44635-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="44635-125">Počkejte, až se nasazení dokončí a prostředí dosáhne stavu **Připraveno**.</span><span class="sxs-lookup"><span data-stu-id="44635-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="44635-126">Přidejte do prostředí předpoklady pro duální zápis.</span><span class="sxs-lookup"><span data-stu-id="44635-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="44635-127">Podpora duálního zápisu zahrnuje další pole, která se přidávají ke klíčovým entitám, jako je například entita **Společnost**.</span><span class="sxs-lookup"><span data-stu-id="44635-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="44635-128">Pokud přidáváte podporu duálního zápisu do existujícího prostředí, možná budete muset aktualizovat data, abyste podporu povolili.</span><span class="sxs-lookup"><span data-stu-id="44635-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="44635-129">Informace o tom, jak provést bootstrap daa, viz [Bootstrap dat společnosti](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="44635-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="44635-130">Další informace o duálním zápisu najdete v části [Systémové požadavky pro duální zápis](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="44635-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="44635-131">Dokončením tohoto postupu přidáte do svého prostředí předpoklady pro duální zápis.</span><span class="sxs-lookup"><span data-stu-id="44635-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="44635-132">Otevřete prostředí, které jste právě vytvořili, a přejděte na **Zdroj** \> **Aplikace Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="44635-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="44635-133">Vyberte **Základní řešení pro duální zápis** v seznamu aplikací a nainstalujte jej.</span><span class="sxs-lookup"><span data-stu-id="44635-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="44635-134">Počkejte, až bude instalace dokončena.</span><span class="sxs-lookup"><span data-stu-id="44635-134">Wait until the installation is completed.</span></span> <span data-ttu-id="44635-135">Potom vyberte **Řešení orchestrace aplikace pro duální zápis** v seznamu aplikací a nainstalujte jej.</span><span class="sxs-lookup"><span data-stu-id="44635-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="44635-136">Přidejte aplikaci Project Operations Dataverse.</span><span class="sxs-lookup"><span data-stu-id="44635-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="44635-137">Tento postup můžete dokončit, pouze pokud jste před instalací Project Operations dokončili předchozí postupy.</span><span class="sxs-lookup"><span data-stu-id="44635-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="44635-138">Během instalace systém analyzuje konfiguraci prostředí a v případě potřeby přidává podporu pro duální zápis.</span><span class="sxs-lookup"><span data-stu-id="44635-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="44635-139">Otevřete prostředí, které jste vytvořili dříve, a přejděte na **Zdroj** \> **Aplikace Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="44635-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="44635-140">Vyberte **Microsoft Dynamics 365 Project Operations** v seznamu aplikací a nainstalujte jej.</span><span class="sxs-lookup"><span data-stu-id="44635-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="44635-141">Propojte svá prostředí</span><span class="sxs-lookup"><span data-stu-id="44635-141">Link your environments</span></span>

<span data-ttu-id="44635-142">Po nasazení prostředí Dataverse můžete nastavit odkaz ve vašich aplikacích Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="44635-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="44635-143">Postupujte podle pokynů v [Propojte prostředí pomocí průvodce duálním zápisem](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span><span class="sxs-lookup"><span data-stu-id="44635-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
