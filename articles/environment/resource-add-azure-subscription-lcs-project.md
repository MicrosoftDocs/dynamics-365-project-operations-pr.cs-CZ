---
title: Přidání předplatného Azure do projektu LCS
description: Toto téma poskytuje informace o tom, jak připojit vaše předplatné Azure k projektu LCS.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a80c926ba67a1620e39d8c7677a05678454e6340
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880530"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="76ae4-103">Přidání předplatného Azure do projektu LCS</span><span class="sxs-lookup"><span data-stu-id="76ae4-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="76ae4-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="76ae4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="76ae4-105">Prostředí hostovaná v cloudu musí být nasazena pomocí existujícího předplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="76ae4-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="76ae4-106">Toto téma vysvětluje, jak připojit vaše stávající předplatné Azure k projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="76ae4-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="76ae4-107">Udělit souhlas správce</span><span class="sxs-lookup"><span data-stu-id="76ae4-107">Grant admin consent</span></span>

1. <span data-ttu-id="76ae4-108">Ve vašem projektu LCS v sekci **Prostředí** vyberte nastavení **Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="76ae4-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Nastavení aplikace Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="76ae4-110">Na stránce **Nastavení projektu** na kartě **Konektory Azure** vyberte položku **Autorizovat**.</span><span class="sxs-lookup"><span data-stu-id="76ae4-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="76ae4-111">Tato akce umožňuje nasazení prostředí do tohoto projektu.</span><span class="sxs-lookup"><span data-stu-id="76ae4-111">This allows environments to be deployed to this project.</span></span>

![Konektory Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="76ae4-113">Znovu vyberte položku **Autorizovat** a poskytněte tak souhlas správce.</span><span class="sxs-lookup"><span data-stu-id="76ae4-113">Select **Authorize** again to provide admin consent.</span></span>

![Udělit souhlas správce](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="76ae4-115">Přijměte žádost o oprávnění.</span><span class="sxs-lookup"><span data-stu-id="76ae4-115">Accept the permissions request.</span></span>

![Schválení žádosti o oprávnění](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="76ae4-117">Autorizace je nyní dokončena.</span><span class="sxs-lookup"><span data-stu-id="76ae4-117">The authorization is now complete.</span></span> 

![Autorizace byla úspěšná](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="76ae4-119">Poskytnutí přístupu k předplatnému Azure službám Dynamics Deployment Services</span><span class="sxs-lookup"><span data-stu-id="76ae4-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="76ae4-120">Přejděte do části [Fakturace Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) a vyberte své předplatné.</span><span class="sxs-lookup"><span data-stu-id="76ae4-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="76ae4-121">Aby bylo možné nasadit prostředí, služby Dynamics Deployment Services vyžadují přístup k tomuto předplatnému.</span><span class="sxs-lookup"><span data-stu-id="76ae4-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Podrobnosti předplatného Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="76ae4-123">V navigačním podokně vyberte položku **Řízení přístupu (IAM)** a poté vyberte možnost **Přidat přiřazení role**.</span><span class="sxs-lookup"><span data-stu-id="76ae4-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="76ae4-124">V posuvníku na pravé straně vyberte možnost **Role přispěvatele** a v zobrazeném seznamu najděte a vyberte položku **Dynamics Deployment Services**.</span><span class="sxs-lookup"><span data-stu-id="76ae4-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="76ae4-125">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="76ae4-125">Select **Save**.</span></span>

![Přístup k předplatnému](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="76ae4-127">Přidání konektoru předplatného do projektu LCS</span><span class="sxs-lookup"><span data-stu-id="76ae4-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="76ae4-128">Ve vašem projektu LCS na stránce **nastavení Microsoft Azure** vyberte příkaz **Přidat** a přidejte nový konektor.</span><span class="sxs-lookup"><span data-stu-id="76ae4-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="76ae4-129">Zadejte ID vašeho předplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="76ae4-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="76ae4-130">ID předplatného Azure najdete na [portálu Azure](https://ms.portal.azure.com/) v části **Nastavení** v levém dolním rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="76ae4-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="76ae4-131">V poli **Konfigurovat pro použití technologie ARM (Azure Resource Manager)** vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="76ae4-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="76ae4-132">Ujistěte se, že se doména klienta AAD předplatného Azure shoduje s předplatným Azure vlastnícím vámi používanou doménu, a vyberte položku **Další**.</span><span class="sxs-lookup"><span data-stu-id="76ae4-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="76ae4-133">Na obrazovce **Nastavení Microsoft Azure** potvrďte výběr tlačítkem **Další**.</span><span class="sxs-lookup"><span data-stu-id="76ae4-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="76ae4-134">Pokud se na této obrazovce zobrazí chyba, vraťte se do sekce [Poskytnutí přístupu k předplatnému Azure službám Dynamics Deployment Services](#provide) v tomto tématu a ujistěte se, že jste dokončili všechny kroky.</span><span class="sxs-lookup"><span data-stu-id="76ae4-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="76ae4-135">Stáhněte si certifikát pro správu Azure do místní složky ve vašem počítači.</span><span class="sxs-lookup"><span data-stu-id="76ae4-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="76ae4-136">Požádejte svého správce předplatného Azure o nahrání certifikátu na portál Azure Management Portal výběrem předplatného a přechodem na **Nastavení** > **Certifikáty pro správu**.</span><span class="sxs-lookup"><span data-stu-id="76ae4-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="76ae4-137">Tento certifikát umožňuje LCS komunikovat s Azure vaším jménem.</span><span class="sxs-lookup"><span data-stu-id="76ae4-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="76ae4-138">Tento krok můžete přeskočit, pokud má váš uživatel přístup k předplatnému.</span><span class="sxs-lookup"><span data-stu-id="76ae4-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="76ae4-139">Vyberte tlačítko **Další**.</span><span class="sxs-lookup"><span data-stu-id="76ae4-139">Select  **Next**.</span></span>
8. <span data-ttu-id="76ae4-140">Vyberte oblast Azure, do které chcete provést nasazení, a vyberte datové centrum, které je blízko místa, kde plánujete tento systém používat.</span><span class="sxs-lookup"><span data-stu-id="76ae4-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="76ae4-141">Vyberte příkaz **Připojit**.</span><span class="sxs-lookup"><span data-stu-id="76ae4-141">Select  **Connect**.</span></span>

<span data-ttu-id="76ae4-142">Úspěšně jste připojili své předplatné Azure.</span><span class="sxs-lookup"><span data-stu-id="76ae4-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="76ae4-143">Nyní můžete nasadit prostředí Dynamics 365 Finance hostovaná v cloudu.</span><span class="sxs-lookup"><span data-stu-id="76ae4-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
