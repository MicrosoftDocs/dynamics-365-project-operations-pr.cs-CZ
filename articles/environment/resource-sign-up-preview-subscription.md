---
title: Přihlášení k odběru preview Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Toto téma poskytuje informace o tom, jak přihlásit odběr a nasadit Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a03f021b1ae0a87dfc947976b8a16c8246e1684
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073666"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="fca66-103">Přihlášení k odběru preview Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě</span><span class="sxs-lookup"><span data-stu-id="fca66-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="fca66-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="fca66-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fca66-105">Toto téma vysvětluje, jak se přihlásit k odběru preview / nabídky partnera a nasadit prostředí Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě.</span><span class="sxs-lookup"><span data-stu-id="fca66-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fca66-106">Požadavky</span><span class="sxs-lookup"><span data-stu-id="fca66-106">Prerequisites</span></span>

- <span data-ttu-id="fca66-107">Obdržíte e-mail s výzvou k účasti v programu Preview.</span><span class="sxs-lookup"><span data-stu-id="fca66-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="fca66-108">O preview můžete požádat na [webu Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="fca66-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="fca66-109">Uživatel, který nasadí preview, musí mít práva globálního správce klienta Azure.</span><span class="sxs-lookup"><span data-stu-id="fca66-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="fca66-110">Nasazení prostředí Finance vyžaduje platné předplatné Azure, kterému bude účtováno každé prostředí zvlášť.</span><span class="sxs-lookup"><span data-stu-id="fca66-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="fca66-111">V začátcích můžete použít stávající předplatné vaší organizace nebo [zkušební verzi Azure](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="fca66-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="fca66-112">Prostředí CDS bude poskytováno zdarma po omezenou dobu 30 dnů.</span><span class="sxs-lookup"><span data-stu-id="fca66-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="fca66-113">Odebírat</span><span class="sxs-lookup"><span data-stu-id="fca66-113">Subscribe</span></span>

<span data-ttu-id="fca66-114">Až bude váš [požadavek na preview](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) schválen, dostanete od společnosti Microsoft e-mailem tři nabídky.</span><span class="sxs-lookup"><span data-stu-id="fca66-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="fca66-115">Tyto nabídky vám umožňují nasadit Project Operations Preview:</span><span class="sxs-lookup"><span data-stu-id="fca66-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="fca66-116">Dynamics 365 Project Operations (CRM) – zkušební verze Preview</span><span class="sxs-lookup"><span data-stu-id="fca66-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="fca66-117">Office 365 Project Operations – zkušební verze Preview</span><span class="sxs-lookup"><span data-stu-id="fca66-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="fca66-118">Dynamics 365 Finance - Zkušební verze Preview</span><span class="sxs-lookup"><span data-stu-id="fca66-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fca66-119">Tuto úlohu musí v organizaci provést pouze jedna osoba, správce tenanta.</span><span class="sxs-lookup"><span data-stu-id="fca66-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="fca66-120">Pokud nejste předplatitelem tohoto vydání, počkejte, dokud nebude vaše organizace zaregistrována a neobdržíte přihlašovací údaje uživatele.</span><span class="sxs-lookup"><span data-stu-id="fca66-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="fca66-121">Dynamics 365 Project Operations (CRM) – zkušební verze Preview</span><span class="sxs-lookup"><span data-stu-id="fca66-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="fca66-122">Než začnete, ujistěte se, že jste přihlášeni do prohlížeče s pracovním účtem uživatele v klientu, kde chcete Project Operations Preview mít.</span><span class="sxs-lookup"><span data-stu-id="fca66-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="fca66-123">Uplatněte první kód nabídky, **Dynamics 365 Project Operations (CRM) – zkušební verze Preview** , vložením do adresy URL prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="fca66-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Uplatnění nabídky](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="fca66-125">Objednávku potvrďte.</span><span class="sxs-lookup"><span data-stu-id="fca66-125">Confirm your order.</span></span>

![Potvrďte objednávku](./media/17ConfirmOrderNew.png)

<span data-ttu-id="fca66-127">Uvidíte, že nabídka potvrzení byla úspěšně uplatněna.</span><span class="sxs-lookup"><span data-stu-id="fca66-127">You will see confirmation offer was successfully redeemed.</span></span>

![Potvrzení](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="fca66-129">Office 365 Project Operations – zkušební verze Preview</span><span class="sxs-lookup"><span data-stu-id="fca66-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="fca66-130">Opakujte stejné kroky jako u prvního nabídkového kódu.</span><span class="sxs-lookup"><span data-stu-id="fca66-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="fca66-131">Přidejte druhý kód nabídky pomocí stejného uživatelského účtu, který byl použit s prvním kódem nabídky.</span><span class="sxs-lookup"><span data-stu-id="fca66-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="fca66-132">Zkušební verze Preview Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="fca66-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="fca66-133">Stejné kroky opakujte s poslední nabídkou z uvítacího e-mailu.</span><span class="sxs-lookup"><span data-stu-id="fca66-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="fca66-134">Přiřazení licencí</span><span class="sxs-lookup"><span data-stu-id="fca66-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fca66-135">Budete potřebovat přístup správce k portálu Microsoft 365 vaší organizace, abyste mohli dokončit následující kroky.</span><span class="sxs-lookup"><span data-stu-id="fca66-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="fca66-136">Přejděte do [Centra pro správu Microsoft 365](https://portal.office.com/), kde přiřadíte licence vašim uživatelům.</span><span class="sxs-lookup"><span data-stu-id="fca66-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Domovská stránka centra pro správu](./media/14AdminPortal.png)

2. <span data-ttu-id="fca66-138">Na stránce **Aktivní uživatelé** vyberte uživatele, kterým chcete přiřadit licenci.</span><span class="sxs-lookup"><span data-stu-id="fca66-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Přiřazení licencí](./media/15AssignLicenses.png)

3. <span data-ttu-id="fca66-140">Ověřte, že je vybrána položka **Dynamics 365 Project Operations (CRM) – Preview** a licence **Office 365 Project Operations - Preview** a vyberte příkaz **Uložit změny**.</span><span class="sxs-lookup"><span data-stu-id="fca66-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="fca66-141">Nabídku zkušební verze Finance není nutné přiřadit uživateli.</span><span class="sxs-lookup"><span data-stu-id="fca66-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="fca66-142">Zahájení nového projektu v LCS</span><span class="sxs-lookup"><span data-stu-id="fca66-142">Start a new project in LCS</span></span>

<span data-ttu-id="fca66-143">Vytvořte nový projekt LCS podle popisu v tématu [Spuštění nového projektu v LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="fca66-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="fca66-144">Přidání předplatného Azure do projektu LCS</span><span class="sxs-lookup"><span data-stu-id="fca66-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="fca66-145">Chcete-li dokončit tento úkol, postupujte podle pokynů v tématu [Přidání předplatného Azure do projektu LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="fca66-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="fca66-146">Nasazení ukázkového prostředí Finance spolu s Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě</span><span class="sxs-lookup"><span data-stu-id="fca66-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="fca66-147">Postupujte podle pokynů v tématu [Zřízení nového prostředí](resource-provision-new-environment.md) a dokončete nasazení.</span><span class="sxs-lookup"><span data-stu-id="fca66-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="fca66-148">Pro preview použijte typ nasazení [demo prostředí](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment).</span><span class="sxs-lookup"><span data-stu-id="fca66-148">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="fca66-149">Instalace nastavení CDS a dat konfigurace</span><span class="sxs-lookup"><span data-stu-id="fca66-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="fca66-150">Nainstalujte instalační a konfigurační data CDS podle popisu v tématu [Nastavení a použití dat konfigurace ve službě Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="fca66-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="fca66-151">Tento krok dokončete až poté, co se nasadí ukázkové prostředí Finance a budou připravena ukázková data ve FO.</span><span class="sxs-lookup"><span data-stu-id="fca66-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>