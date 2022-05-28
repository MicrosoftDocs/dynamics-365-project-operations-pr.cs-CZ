---
title: Sledování stavu projektu
description: Postup sledování stavu projektu v Project Service
author: ruhercul
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
ms.openlocfilehash: 58274886a9f9ce6ae49c64c1d7ac491e29c7d06c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593374"
---
# <a name="track-a-projects-status-project-service"></a>Sledování stavu projektu (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] lze použít ke sledování průběhu projektu klienta.  

V průběhu platnosti závazku se fáze projektu aktualizují tak, aby odrážely stupeň závazku:  

| Úloha | Description | 
|------------|----------|
| **New** | Při vytváření projektu je fáze nastavena na **Nový**. Pokud jste vytvořili projekt ze šablony, v této fázi může mít projekt plán, odhady a data týmu. Jinak se bude jednat pouze o návrh projektu a bude třeba ručně zadat zbývající části projektu. |
| **Nabídka** |  Když přiřadíte projekt k nabídce nebo jej vytvoříte z nabídky, fáze projektu bude nastavena na možnost **Nabídka** a aktualizuje se také odhadované datum zahájení a ukončení. Pokud je projekt ve fázi nabídky, podrobnosti o nabídce se zobrazí na kartě **Prodej** na stránce **Projekt**. |
| **Plán** |  Pokud vyhrajete nabídku spojenou s projektem a v průběhu platnosti závazku přejdete do fáze smlouvy, fáze projektu se aktualizuje na **Plán**. Podrobnosti o smlouvě se zobrazí na kartě **Prodej** na stránce **Projekt**. |
| **Dokončeno** | Po dokončení práce na projektu můžete přepnout na fázi **Dokončeno**. Pokud je fáze projektu nastavena na možnost Dokončeno, práce je na 100 % ale dokončena, ale projekt zůstává otevřen, aby by mohla být zaznamenána doba čekání nebo položky výdajů. |
| **Zavřít** | Když jsou všechny transakce projektu zaznamenány a neočekáváte protokolování dalších, můžete ručně nastavit fázi na **Uzavřeno**. Pokud je projekt nastaven na **Uzavřeno**, nelze protokolovat žádné další transakce projektu a projekt bude jen pro čtení. |

## <a name="to-track-a-projects-status"></a>Sledování stavu projektu  

1.  Přejděte do nabídky **Project Service > Projekty**.  

2.  Klepněte na projekt, na kterém chcete pracovat.  

3.  Na panelu v horní části obrazovky vyberte šipku dolů vedle názvu projektu a potom klikněte na možnost **Sledování projektu**.  

4.  Vyberte možnost **Sledování úsilí** nebo **Sledování nákladů** v rozevíracím seznamu nad seznam úkolů.  

5.  Dvakrát klikněte na kterýkoli úkol, který chcete upravit. Také můžete přesunout nebo změnit velikost pruhů v Ganttově diagramu, chcete-li změnit čas a průběh úkolu.  

### <a name="see-also"></a>Viz také  
 [Příručka pro projektového manažera](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
