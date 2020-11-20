---
title: Povolení funkcí aplikace Project Finder Mobile
description: Postup povolení funkcí aplikace Project Finder Mobile pro Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: af267b5adc48b6edec57de196f91e338c058558c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132955"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="ee7bf-103">Povolení funkcí aplikace Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ee7bf-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ee7bf-104">Vaše zdroje mohou pomocí aplikace Project Finder Mobile na svých telefonech obsahujících [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vyhledávat nové projekty, na nichž by mohli pracovat, a aktualizovat své dovednosti.</span><span class="sxs-lookup"><span data-stu-id="ee7bf-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="ee7bf-105">Aplikace je k dispozici pro telefony [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], telefony se systémem [!INCLUDE[tn_android](../includes/tn-android.md)] a telefony se systémem [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="ee7bf-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="ee7bf-106">Je nutné nakonfigurovat několik možností v nastavení parametrů pro vaši organizační jednotku, aby mohli uživatelé zobrazovat požadavky na zdroje v rámci projektu a aktualizovat své dovednosti.</span><span class="sxs-lookup"><span data-stu-id="ee7bf-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ee7bf-107">Aplikace Project Finder Mobile pracuje pouze s aplikací [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] (nikoli s místními instalacemi).</span><span class="sxs-lookup"><span data-stu-id="ee7bf-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="ee7bf-108">Přejděte do nabídky **Project Service > Parametry**.</span><span class="sxs-lookup"><span data-stu-id="ee7bf-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="ee7bf-109">Klikněte na nastavení parametrů, které chcete použít pro povolení funkcí aplikace Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="ee7bf-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="ee7bf-110">V části **Obecné** nastavte možnost **Požadavky na zdroje jsou viditelné zdrojům** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ee7bf-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="ee7bf-111">Nastavte možnost **Umožnit zdroji aktualizovat dovednosti** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ee7bf-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="ee7bf-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="ee7bf-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="ee7bf-113">Toto je globální nastavení.</span><span class="sxs-lookup"><span data-stu-id="ee7bf-113">This is a global setting.</span></span> <span data-ttu-id="ee7bf-114">Vedoucí projektu mohou nastavit, zda budou jednotlivé projekty zobrazeny na stránce **Projektový tým** daného projektu.</span><span class="sxs-lookup"><span data-stu-id="ee7bf-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="ee7bf-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="ee7bf-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="ee7bf-116">E-mailová oznámení</span><span class="sxs-lookup"><span data-stu-id="ee7bf-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="ee7bf-117">odešle e-maily týkající se požadavků na zdroje následujícím příjemcům v následujících časech:</span><span class="sxs-lookup"><span data-stu-id="ee7bf-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="ee7bf-118">Příjemce</span><span class="sxs-lookup"><span data-stu-id="ee7bf-118">Recipient</span></span>|<span data-ttu-id="ee7bf-119">Událost</span><span class="sxs-lookup"><span data-stu-id="ee7bf-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="ee7bf-120">Vedoucí projektu</span><span class="sxs-lookup"><span data-stu-id="ee7bf-120">Project manager</span></span>|<span data-ttu-id="ee7bf-121">-   Když se zdroj zaregistruje do projektu pomocí aplikace Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="ee7bf-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="ee7bf-122">Zdroj</span><span class="sxs-lookup"><span data-stu-id="ee7bf-122">Resource</span></span>|<span data-ttu-id="ee7bf-123">-   Když byla práce v rámci projektu, na kterou se zdroj zaregistroval, již vykonána jiným zdrojem.</span><span class="sxs-lookup"><span data-stu-id="ee7bf-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="ee7bf-124">-   Když byl schválen nebo zamítnut jejich požadavek na schválení dovedností.</span><span class="sxs-lookup"><span data-stu-id="ee7bf-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="ee7bf-125">-   Když byl schválen nebo zamítnut jejich požadavek na registraci do projektu.</span><span class="sxs-lookup"><span data-stu-id="ee7bf-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="ee7bf-126">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="ee7bf-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="ee7bf-127">Viz také</span><span class="sxs-lookup"><span data-stu-id="ee7bf-127">See Also</span></span>  
 [<span data-ttu-id="ee7bf-128">Nastavení zdrojů</span><span class="sxs-lookup"><span data-stu-id="ee7bf-128">Set up resources</span></span>](../psa/set-up-resources.md)
