---
title: Konfigurace dalšího nastavení parametrů
description: Postup konfigurace nastavení dalších parametrů v Project Service
author: JohnPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 75fe0aab8ea8bf41fcb98f4318380c93ac52fef8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919224"
---
# <a name="configure-additional-parameter-settings-project-service"></a>Konfigurace nastavení dalších parametrů (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Po konfiguraci položek uvedených v předchozích článcích je nutné nastavit další parametry projektu pro vaše projekty. Při první instalaci [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] jste vytvořili nastavení parametrů, aby mohly být nejprve vytvořeny všechny záznamy požadované pro fungování [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Nyní je čas vrátit se zpět a nakonfigurovat další pole pro tato nastavení.  
  
 Je třeba, aby byla nakonfigurována následující nastavení:  
  
-   Organizační jednotka  
  
-   Četnost faktur  
  
-   Šablona pracovní doby  
  
-   Ceník  
 
V tomto kroku také určíte, jaký typ přidělování zdrojů požadujete:  
  
- **Centrální**. Pouze správci zdrojů mohou přidělovat zdroje k projektům.  
  
- **Hybridní**. Správci zdrojů, vedoucí projektů a manažeři zákaznických účtů mohou přidělovat zdroje k projektům.  
  
 
Nastavení parametrů projektu:  
  
1. Přejděte do nabídky **Project Service > Parametry**.  
  
2. Klikněte na nastavení parametrů, které chcete konfigurovat (nastavení, které jste vytvořili při první instalaci [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), nebo kliknutím na tlačítko **Nové** vytvořte nové nastavení.  
  
3. V oblasti **Obecné** nastavte všechny možnosti parametrů vašeho projektu.  
  
4. V oblasti **Ceník** přidejte ceník kliknutím na tlačítko **+**, vyberte ceník v rozevíracím seznamu **Ceník projektových parametrů** a klikněte na tlačítko **Uložit**.  
  
5. Klikněte na tlačítko **Uložit** v pravém dolním rohu obrazovky.  

> [!NOTE]
> Aby aplikace Project Service fungovala správně, musí být zachován záznam parametrů projektu. Tento záznam by neměl být vymazán.

### <a name="see-also"></a>Viz také  
 [Nastavení zdrojů](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
