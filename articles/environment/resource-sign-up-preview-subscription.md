---
title: Přihlášení k odběru preview Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Toto téma poskytuje informace o tom, jak přihlásit odběr a nasadit Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948802"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="32884-103">Přihlášení k odběru preview Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě</span><span class="sxs-lookup"><span data-stu-id="32884-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="32884-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="32884-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="32884-105">Toto téma vysvětluje, jak se přihlásit k odběru preview / nabídky partnera a nasadit prostředí Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě.</span><span class="sxs-lookup"><span data-stu-id="32884-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="32884-106">Požadavky</span><span class="sxs-lookup"><span data-stu-id="32884-106">Prerequisites</span></span>

- <span data-ttu-id="32884-107">Obdržíte e-mail s výzvou k účasti v programu Preview.</span><span class="sxs-lookup"><span data-stu-id="32884-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="32884-108">O preview můžete požádat na [webu Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="32884-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="32884-109">Uživatel, který nasadí preview, musí mít práva globálního správce klienta Azure.</span><span class="sxs-lookup"><span data-stu-id="32884-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="32884-110">Nasazení prostředí Finance vyžaduje platné předplatné Azure, kterému bude účtováno každé prostředí zvlášť.</span><span class="sxs-lookup"><span data-stu-id="32884-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="32884-111">V začátcích můžete použít stávající předplatné vaší organizace nebo [zkušební verzi Azure](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="32884-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="32884-112">Prostředí CDS bude poskytováno zdarma po omezenou dobu 30 dnů.</span><span class="sxs-lookup"><span data-stu-id="32884-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="32884-113">Odebírat</span><span class="sxs-lookup"><span data-stu-id="32884-113">Subscribe</span></span>

<span data-ttu-id="32884-114">Až bude váš [požadavek na preview](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) schválen, dostanete od společnosti Microsoft e-mailem dvě nabídky.</span><span class="sxs-lookup"><span data-stu-id="32884-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="32884-115">Tyto nabídky vám umožňují nasadit Project Operations Preview:</span><span class="sxs-lookup"><span data-stu-id="32884-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="32884-116">Dynamics 365 Project Operations – zkušební verze Preview</span><span class="sxs-lookup"><span data-stu-id="32884-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="32884-117">Zkušební verze Preview Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="32884-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32884-118">Tuto úlohu musí v organizaci provést pouze jedna osoba, správce tenanta.</span><span class="sxs-lookup"><span data-stu-id="32884-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="32884-119">Pokud nejste předplatitelem tohoto vydání, počkejte, dokud nebude vaše organizace zaregistrována a neobdržíte přihlašovací údaje uživatele.</span><span class="sxs-lookup"><span data-stu-id="32884-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="32884-120">Dynamics 365 Project Operations – zkušební verze Preview</span><span class="sxs-lookup"><span data-stu-id="32884-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="32884-121">První nabídku na **zkušební verzi aplikace Dynamics 365 Project Operations** uplatněte pomocí adresy URL uvedené v uvítacím e-mailu.</span><span class="sxs-lookup"><span data-stu-id="32884-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![První nabídka](./media/1FirstOffer.png)

2. <span data-ttu-id="32884-123">Ověřte, že jste přihlášeni jako uživatel patřící do organizace, která si bude předplácet službu.</span><span class="sxs-lookup"><span data-stu-id="32884-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="32884-124">Pokračujte v uplatnění nabídky.</span><span class="sxs-lookup"><span data-stu-id="32884-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="32884-125">Vyberte položku **Ano, přidat do mého účtu**.</span><span class="sxs-lookup"><span data-stu-id="32884-125">Select **Yes, add it to my account**.</span></span>

![Uplatnění nabídky](./media/2RedeemFirstOffer.png)

![Potvrďte nabídku](./media/3ConfirmFirstOffer.png)

![Nabídka uplatněna](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="32884-129">Zkušební verze Preview Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="32884-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="32884-130">Stejné kroky opakujte s druhou nabídkou z uvítacího e-mailu.</span><span class="sxs-lookup"><span data-stu-id="32884-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="32884-131">Přiřazení licencí</span><span class="sxs-lookup"><span data-stu-id="32884-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32884-132">Budete potřebovat přístup správce k portálu Office 365 vaší organizace, abyste mohli dokončit následující kroky.</span><span class="sxs-lookup"><span data-stu-id="32884-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="32884-133">Přejděte do [Centra pro správu Microsoft 365](https://portal.office.com/), kde přiřadíte licence vašim uživatelům.</span><span class="sxs-lookup"><span data-stu-id="32884-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Portál pro správu služeb Office](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="32884-135">Na stránce **Aktivní uživatelé** vyberte uživatele, kterým chcete přiřadit licenci.</span><span class="sxs-lookup"><span data-stu-id="32884-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Přiřazení licencí](./media/6AssignLicenses.png)

3. <span data-ttu-id="32884-137">Ověřte, že byla vybrána licence Project Operations, a vyberte příkaz **Uložit změny**.</span><span class="sxs-lookup"><span data-stu-id="32884-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="32884-138">Nabídku zkušební verze Finance není nutné přiřadit uživateli.</span><span class="sxs-lookup"><span data-stu-id="32884-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="32884-139">Zahájení nového projektu v LCS</span><span class="sxs-lookup"><span data-stu-id="32884-139">Start a new project in LCS</span></span>

<span data-ttu-id="32884-140">Vytvořte nový projekt LCS podle popisu v tématu [Spuštění nového projektu v LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="32884-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="32884-141">Přidání předplatného Azure do projektu LCS</span><span class="sxs-lookup"><span data-stu-id="32884-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="32884-142">Chcete-li dokončit tento úkol, postupujte podle pokynů v tématu [Přidání předplatného Azure do projektu LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="32884-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="32884-143">Nasazení ukázkového prostředí Finance spolu s Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě</span><span class="sxs-lookup"><span data-stu-id="32884-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="32884-144">Postupujte podle pokynů v tématu [Zřízení nového prostředí](resource-provision-new-environment.md) a dokončete nasazení.</span><span class="sxs-lookup"><span data-stu-id="32884-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="32884-145">Pro preview použijte typ nasazení [demo prostředí](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment).</span><span class="sxs-lookup"><span data-stu-id="32884-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="32884-146">Instalace nastavení CDS a dat konfigurace</span><span class="sxs-lookup"><span data-stu-id="32884-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="32884-147">Nainstalujte instalační a konfigurační data CDS podle popisu v tématu [Nastavení a použití dat konfigurace ve službě Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="32884-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

