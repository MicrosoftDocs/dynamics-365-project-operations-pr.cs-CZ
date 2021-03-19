---
title: Povolení funkcí aplikace Project Finder Mobile
description: Postup povolení funkcí aplikace Project Finder Mobile pro Project Service
author: JohnPBurrows
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: 5e4f3bf15589181e3095400c131d322184578afa
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284620"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Povolení funkcí aplikace Project Finder Mobile (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Vaše zdroje mohou pomocí aplikace Project Finder Mobile na svých telefonech obsahujících [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vyhledávat nové projekty, na nichž by mohli pracovat, a aktualizovat své dovednosti.  
  
 Aplikace je k dispozici pro telefony [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], telefony se systémem [!INCLUDE[tn_android](../includes/tn-android.md)] a telefony se systémem [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
    
 Je nutné nakonfigurovat možnosti v nastavení parametrů pro vaši organizační jednotku, aby mohli uživatelé zobrazovat požadavky na zdroje v rámci projektu a aktualizovat své dovednosti.
  
> [!NOTE]
>  Aplikace Project Finder Mobile pracuje pouze s aplikací [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] (nikoli s místními instalacemi).  
  
1. Přejděte do nabídky **Project Service > Parametry**.  
  
2. Klikněte na nastavení parametrů, které chcete použít pro povolení funkcí aplikace Project Finder Mobile.  
  
3. V části **Obecné** nastavte možnost **Požadavky na zdroje jsou viditelné zdrojům** na **Ano**.  
  
4. Nastavte možnost **Umožnit zdroji aktualizovat dovednosti** na **Ano**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Toto je globální nastavení. Vedoucí projektu mohou nastavit, zda budou jednotlivé projekty zobrazeny na stránce **Projektový tým** daného projektu.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>E-mailová oznámení  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] odešle e-maily týkající se požadavků na zdroje následujícím příjemcům v následujících časech:  
  
|Příjemce|Událost|  
|---------------|-----------|  
|Vedoucí projektu|– Zdroj zaregistruje do projektu pomocí aplikace Project Finder Mobile.|  
|Prostředek|– Práce v rámci projektu, na kterou se zdroj zaregistroval, byla již vykonána jiným zdrojem.<br />– Byl schválen nebo zamítnut jejich požadavek na schválení dovedností.<br />– Byl schválen nebo zamítnut jejich požadavek na registraci do projektu.|  
  
## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Viz také  
 [Nastavení zdrojů](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]