---
title: Povolení funkcí aplikace Project Finder Mobile
description: Postup povolení funkcí aplikace Project Finder Mobile pro Project Service
author: JohnPBurrows
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f068c32ac957dc5921ccabc989b3b7a347585c19
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007718"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="f7ee1-103">Povolení funkcí aplikace Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f7ee1-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f7ee1-104">Vaše zdroje mohou pomocí aplikace Project Finder Mobile na svých telefonech obsahujících [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vyhledávat nové projekty, na nichž by mohli pracovat, a aktualizovat své dovednosti.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skillsets.</span></span>  
  
 <span data-ttu-id="f7ee1-105">Aplikace je k dispozici pro telefony [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], telefony se systémem [!INCLUDE[tn_android](../includes/tn-android.md)] a telefony se systémem [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="f7ee1-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
    
 <span data-ttu-id="f7ee1-106">Je nutné nakonfigurovat možnosti v nastavení parametrů pro vaši organizační jednotku, aby mohli uživatelé zobrazovat požadavky na zdroje v rámci projektu a aktualizovat své dovednosti.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-106">To allow users to view project resource requirements and update skills, options must be selected in the parameter settings for your organizational unit.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="f7ee1-107">Aplikace Project Finder Mobile pracuje pouze s aplikací [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] (nikoli s místními instalacemi).</span><span class="sxs-lookup"><span data-stu-id="f7ee1-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="f7ee1-108">Přejděte do nabídky **Project Service > Parametry**.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="f7ee1-109">Klikněte na nastavení parametrů, které chcete použít pro povolení funkcí aplikace Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="f7ee1-110">V části **Obecné** nastavte možnost **Požadavky na zdroje jsou viditelné zdrojům** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="f7ee1-111">Nastavte možnost **Umožnit zdroji aktualizovat dovednosti** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="f7ee1-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="f7ee1-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="f7ee1-113">Toto je globální nastavení.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-113">This is a global setting.</span></span> <span data-ttu-id="f7ee1-114">Vedoucí projektu mohou nastavit, zda budou jednotlivé projekty zobrazeny na stránce **Projektový tým** daného projektu.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="f7ee1-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="f7ee1-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="f7ee1-116">E-mailová oznámení</span><span class="sxs-lookup"><span data-stu-id="f7ee1-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="f7ee1-117">odešle e-maily týkající se požadavků na zdroje následujícím příjemcům v následujících časech:</span><span class="sxs-lookup"><span data-stu-id="f7ee1-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="f7ee1-118">Příjemce</span><span class="sxs-lookup"><span data-stu-id="f7ee1-118">Recipient</span></span>|<span data-ttu-id="f7ee1-119">Událost</span><span class="sxs-lookup"><span data-stu-id="f7ee1-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="f7ee1-120">Vedoucí projektu</span><span class="sxs-lookup"><span data-stu-id="f7ee1-120">Project manager</span></span>|<span data-ttu-id="f7ee1-121">– Zdroj zaregistruje do projektu pomocí aplikace Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-121">- A resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="f7ee1-122">Prostředek</span><span class="sxs-lookup"><span data-stu-id="f7ee1-122">Resource</span></span>|<span data-ttu-id="f7ee1-123">– Práce v rámci projektu, na kterou se zdroj zaregistroval, byla již vykonána jiným zdrojem.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-123">- The project work that the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="f7ee1-124">– Byl schválen nebo zamítnut jejich požadavek na schválení dovedností.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-124">- The skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="f7ee1-125">– Byl schválen nebo zamítnut jejich požadavek na registraci do projektu.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-125">- The project sign-up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="f7ee1-126">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="f7ee1-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="f7ee1-127">Viz také</span><span class="sxs-lookup"><span data-stu-id="f7ee1-127">See Also</span></span>  
 [<span data-ttu-id="f7ee1-128">Nastavení zdrojů</span><span class="sxs-lookup"><span data-stu-id="f7ee1-128">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]