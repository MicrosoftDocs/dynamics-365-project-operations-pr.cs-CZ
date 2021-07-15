---
title: Přihlášení k odběru preview Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Toto téma poskytuje informace o tom, jak přihlásit odběr a nasadit Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334819"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="a532b-103">Přihlášení k odběru preview Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě</span><span class="sxs-lookup"><span data-stu-id="a532b-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="a532b-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="a532b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a532b-105">Tento téma vysvětluje, jak se přihlásit k nabídce zkušební verze a nasadit prostředí Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě.</span><span class="sxs-lookup"><span data-stu-id="a532b-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a532b-106">Požadavky</span><span class="sxs-lookup"><span data-stu-id="a532b-106">Prerequisites</span></span>
- <span data-ttu-id="a532b-107">Uživatel, který nasadí preview, musí mít práva globálního správce klienta Azure.</span><span class="sxs-lookup"><span data-stu-id="a532b-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="a532b-108">Během prvního uplatnění nabídky můžete vytvořit nájemce.</span><span class="sxs-lookup"><span data-stu-id="a532b-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="a532b-109">Nasazení prostředí Finance vyžaduje platné předplatné Azure, kterému bude účtováno každé prostředí zvlášť.</span><span class="sxs-lookup"><span data-stu-id="a532b-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="a532b-110">V začátcích můžete použít stávající předplatné vaší organizace nebo [zkušební verzi Azure](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="a532b-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="a532b-111">Prostředí CDS bude poskytováno zdarma po omezenou dobu 30 dnů.</span><span class="sxs-lookup"><span data-stu-id="a532b-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a532b-112">Tuto úlohu musí v organizaci provést pouze jedna osoba, správce tenanta.</span><span class="sxs-lookup"><span data-stu-id="a532b-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="a532b-113">Pokud nejste předplatitelem tohoto vydání, počkejte, dokud nebude vaše organizace zaregistrována a neobdržíte přihlašovací údaje uživatele.</span><span class="sxs-lookup"><span data-stu-id="a532b-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="a532b-114">Zkušební verze jsou na jedno použití v klientovi.</span><span class="sxs-lookup"><span data-stu-id="a532b-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="a532b-115">Zkušební verzi můžete spustit pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="a532b-115">You can only run a trial one time.</span></span> <span data-ttu-id="a532b-116">Pro účely zkušebního období vám doporučujeme vytvořit nového klienta.</span><span class="sxs-lookup"><span data-stu-id="a532b-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="a532b-117">Dynamics 365 Project Operations(CE) - zkušební verze</span><span class="sxs-lookup"><span data-stu-id="a532b-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="a532b-118">Než začnete, ujistěte se, že jste přihlášeni do prohlížeče s pracovním účtem uživatele v klientu, kde chcete Project Operations Preview mít.</span><span class="sxs-lookup"><span data-stu-id="a532b-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="a532b-119">Uplatněte první nabídkový kód **Dynamics 365 Project Operations** zde [Zkušební verze Project Operations](https://aka.ms/try-po)</span><span class="sxs-lookup"><span data-stu-id="a532b-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="a532b-120">Objednávku potvrďte.</span><span class="sxs-lookup"><span data-stu-id="a532b-120">Confirm your order.</span></span>

  <span data-ttu-id="a532b-121">Uvidíte, že nabídka potvrzení byla úspěšně uplatněna.</span><span class="sxs-lookup"><span data-stu-id="a532b-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="a532b-122">Zkušební verze Preview Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="a532b-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="a532b-123">Přejděte na [Zkušební verze Dynamics 365 for Finance](https://aka.ms/trypoche) a zopakujte kroky z předchozí části s nabídkou, zaregistrujte se v prostředí hostovaném v cloudu.</span><span class="sxs-lookup"><span data-stu-id="a532b-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="a532b-124">Přiřazení licencí</span><span class="sxs-lookup"><span data-stu-id="a532b-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a532b-125">Budete potřebovat přístup správce k portálu Microsoft 365 vaší organizace, abyste mohli dokončit následující kroky.</span><span class="sxs-lookup"><span data-stu-id="a532b-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="a532b-126">Přejděte do [Centra pro správu Microsoft 365](https://portal.office.com/), kde přiřadíte licence vašim uživatelům.</span><span class="sxs-lookup"><span data-stu-id="a532b-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="a532b-127">Na stránce **Aktivní uživatelé** vyberte uživatele, kterým chcete přiřadit licenci.</span><span class="sxs-lookup"><span data-stu-id="a532b-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="a532b-128">Ověřte, že byla vybrána licence **Dynamics 365 Project Operations** a vyberte **Uložit změny**.</span><span class="sxs-lookup"><span data-stu-id="a532b-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="a532b-129">Nabídku zkušební verze Finance není nutné přiřadit uživateli.</span><span class="sxs-lookup"><span data-stu-id="a532b-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="a532b-130">Zahájení nového projektu v LCS</span><span class="sxs-lookup"><span data-stu-id="a532b-130">Start a new project in LCS</span></span>

<span data-ttu-id="a532b-131">Vytvořte nový projekt LCS podle popisu v tématu [Spuštění nového projektu v LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="a532b-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="a532b-132">Přidání předplatného Azure do projektu LCS</span><span class="sxs-lookup"><span data-stu-id="a532b-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="a532b-133">Chcete-li dokončit tento úkol, postupujte podle pokynů v tématu [Přidání předplatného Azure do projektu LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="a532b-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="a532b-134">Nasazení ukázkového prostředí Finance spolu s Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě</span><span class="sxs-lookup"><span data-stu-id="a532b-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="a532b-135">Postupujte podle pokynů v tématu [Zřízení nového prostředí](resource-provision-new-environment.md) a dokončete nasazení.</span><span class="sxs-lookup"><span data-stu-id="a532b-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="a532b-136">Pro preview použijte typ nasazení [demo prostředí](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment).</span><span class="sxs-lookup"><span data-stu-id="a532b-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="a532b-137">Instalace nastavení CDS a dat konfigurace</span><span class="sxs-lookup"><span data-stu-id="a532b-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="a532b-138">Nainstalujte instalační a konfigurační data CDS podle popisu v tématu [Nastavení a použití dat konfigurace ve službě Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="a532b-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="a532b-139">Tento krok dokončete až po nasazení demo prostředí Finance a připravě demo dat.</span><span class="sxs-lookup"><span data-stu-id="a532b-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
