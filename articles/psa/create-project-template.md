---
title: Vytvoření šablony projektu
description: Postup vytvoření šablony projektu v Project Service
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
ms.openlocfilehash: 148bf1d42b640ff7b58b13bb0c30c7e583d803c8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997233"
---
# <a name="create-a-project-template-project-service"></a>Vytvoření šablony projektu (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Šablony projektů šetří váš čas, pokud se vaše společnost pravidelně uchází o podobné typy projektů. Poskytují standardní sadu rolí a odhadované hodiny pro typ projektu. Manažeři zákaznických účtů a vedoucí projektu mohou vytvořit projekty založené na šabloně projektu nebo mohou zkopírovat šablonu a vytvořit svou vlastní.  
  
## <a name="components-of-project-template"></a>Součásti šablony projektu
 Šablona projektu se skládá ze tří součástí:  
  
- **Strukturovaný rozpis prací**: Strukturovaný rozpis prací v šabloně projektu má stejnou sadu prvků jako v projektu. Můžete vytvořit hierarchii úkolů, přiřadit role k úkolu, definovat atributy plánu, nastavit závislosti a zobrazit všechna data v Ganttově diagramu. Strukturované rozpisy prací v šablonách projektů také podporují režimy úkolů pro každý úkol. Při vytváření pracovního plánu není žádný rozdíl mezi šablonou projektu a projektem.  
  
- **Odhady projektu**: Odhady projektu v šablonách fungují stejným způsobem jako v projektech kromě toho, že nákladové a prodejní ceny jsou vždy výchozími nákladovými a prodejními ceníky definovanými v parametrech [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Zbývající funkce jsou stejné jako v projektu.  
  
- **Vytvoření projektového týmu**: Při vytváření projektového týmu pro šablonu projektu nelze rezervovat pojmenovaný zdroj v šabloně. Můžete použít možnost **Vygenerovat projektový tým** ve strukturovaném rozpisu prací a vygenerovat sadu obecných zdrojů. Můžete také určit požadované dovednosti a odborné znalosti pro obecné zdroje. Nelze nahradit obecný zdroj rezervovatelným zdrojem v šablonách projektů.  
  
## <a name="create-a-project-from-a-template"></a>Vytvoření projektu ze šablony  
 Projekt lze ze šablony vytvořit následujícími způsoby:  
  
-   Při vytváření projektu z nabídky můžete vybrat šablonu projektu ve formuláři pro rychlé vytvoření projektu.  
  
-   Při vytváření projektu kliknutím na tlačítko **Nový projekt** se formulář projektu zobrazí před uložením záznamu. Zde můžete kliknout na pole **Vybrat šablonu** a vybrat požadovanou šablonu ze seznamu předdefinovaných šablon projektů ve vaší organizaci.  
  
-   Kliknutím na tlačítko **Vytvořit projekt ze šablony** na stránce **Šablona projektu** vytvořte projekt ze šablony.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Kopírování součástí šablony do projektu  
 Při kopírování součástí šablony do projektu je několik věcí, které byste měli mít na paměti.  
  
 **Kopírování strukturovaného rozpisu prací**: Pokud má projekt při kopírování strukturovaného rozpisu prací ze šablony projektu jiný kalendář projektu než šablona, bude v plánu úkolů použita pracovní doba z kalendáře projektu. Tím se upraví plán pro pomocný kalendář projektu. A podobně první úkol ve strukturovaném rozpisu prací bude mít datum zahájení projektu, takže zbytek plánu hierarchie úkolů bude aktualizován na základě doby trvání a závislostí, které jsou uvedeny ve strukturovaném rozpisu prací šablony.  
  
 **Kopírování odhadů projektu**: Při kopírování mezi řádky odhadů projektu budou ceníky aktualizovány na základě vlastnící jednotky projektu pro nákladový ceník a zákazníka pro prodejní ceník. Nákladové a prodejní ceny na jednotku se stanovují z těchto ceníků u projektů, které jsou přidruženy k prodejní entitě.  
  
 **Kopírování projektového týmu**: Při kopírování projektového týmu z šablony do projektu jsou zkopírovány obecné zdroje spolu s dovednostmi a odbornými znalostmi definovanými v šabloně. Přiřazení obecných zdrojů je rovněž zachováno jako v šabloně projektu.  
  
### <a name="see-also"></a>Viz také  
 [Příručka pro projektového manažera](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]