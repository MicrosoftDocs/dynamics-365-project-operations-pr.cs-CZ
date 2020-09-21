---
title: Povolení funkcí aplikace Project Finder Mobile
description: Postup povolení funkcí aplikace Project Finder Mobile pro Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750269"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Povolení funkcí aplikace Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Vaše zdroje mohou pomocí aplikace Project Finder Mobile na svých telefonech obsahujících [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vyhledávat nové projekty, na nichž by mohli pracovat, a aktualizovat své dovednosti.  
  
 Aplikace je k dispozici pro telefony [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], telefony se systémem [!INCLUDE[tn_android](../includes/tn-android.md)] a telefony se systémem [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Je nutné nakonfigurovat několik možností v nastavení parametrů pro vaši organizační jednotku, aby mohli uživatelé zobrazovat požadavky na zdroje v rámci projektu a aktualizovat své dovednosti.  
  
> [!NOTE]
>  Aplikace Project Finder Mobile pracuje pouze s aplikací [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] (nikoli s místními instalacemi).  
  
1. Přejděte do nabídky **Project Service > Parametry**.  
  
2. Klikněte na nastavení parametrů, které chcete použít pro povolení funkcí aplikace Project Finder Mobile.  
  
3. V části **Obecné** nastavte možnost **Požadavky na zdroje jsou viditelné zdrojům** na **Ano**.  
  
4. Nastavte možnost **Umožnit zdroji aktualizovat dovednosti** na **Ano**.  
  
   ![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Toto je globální nastavení. Vedoucí projektu mohou nastavit, zda budou jednotlivé projekty zobrazeny na stránce **Projektový tým** daného projektu.  
  
   ![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>E-mailová oznámení  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] odešle e-maily týkající se požadavků na zdroje následujícím příjemcům v následujících časech:  
  
|Příjemce|Událost|  
|---------------|-----------|  
|Vedoucí projektu|-   Když se zdroj zaregistruje do projektu pomocí aplikace Project Finder Mobile.|  
|Zdroj|-   Když byla práce v rámci projektu, na kterou se zdroj zaregistroval, již vykonána jiným zdrojem.<br />-   Když byl schválen nebo zamítnut jejich požadavek na schválení dovedností.<br />-   Když byl schválen nebo zamítnut jejich požadavek na registraci do projektu.|  
  
## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Viz také  
 [Nastavení zdrojů](../project-service/set-up-resources.md)
