---
title: Poskytnutí odhadů práce pro projekt během prodejního procesu
description: Postup poskytnutí odhadů práce pro projekt během prodejního procesu v Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ddb7f8c0ff8c7fd7e51edb42f9d227f2b91a811b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073830"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Poskytnutí odhadů práce pro projekt během prodejního procesu (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Během prodejního procesu můžete vypracovat prodejní odhady od začátku s řádky nabídky. Funkce [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v aplikaci [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] přinášejí více vědecký a deterministický způsob vypracování prodejních odhadů prostřednictvím analýzy položek práce a přiřazení příslušných atributů, které přispívají k odhadům pro projekt ve strukturovaném rozpisu prací.  
  
 Jakmile prodej uzavřete, můžete použít přiřazený strukturovaný rozpis prací v plánu projektu a upřesnit jej tak, jak je nutné pro úspěšné dokončení projektu.  
  
## <a name="link-a-project-to-a-quote-line"></a>Propojení projektu k řádku nabídky  
 Při vytváření řádku nabídky založené na projektu můžete vytvořit nový projekt z řádku nabídky. Potom můžete použít šablony projektu, což jsou předem nakonfigurované standardní projektové plány a finanční odhady společné ve vaší organizaci nebo kopie plánu projektu a odhady z posledního projektu. Když vytvoříte projekt, výběr šablony projektu poskytuje základ pro upřesnění požadavků na plán projektu, odhady a roli. Vytvořením projektu z nabídky bude projekt automaticky přidružen k řádku nabídky.  
  
## <a name="project-estimate-components"></a>Součásti odhadu projektu  
 Strukturovaný rozpis prací v projektu umožňuje rozdělit práci na úkoly, udržovat hierarchii úkolů a přiřadit odhad úsilí potřebného k dokončení jednotlivých úkolů. Můžete také přiřadit role k úkolu, čímž označíte odhad typu zdroje potřebného k dokončení úkolu a plánu.  
  
 Strukturovaný rozpis prací vám pomůže určit pracovní úsilí a odhady plánu. Ve výchozím nastavení používá projekt výchozí ceníky, které jste definovali dříve. Nákladové a prodejní ceny uvedené v seznamech pomáhají určit finanční odhady pro rozpis prací projektu.  
  
 Pokud je projekt přidružen k nabídce a nabídka má jiný než výchozí ceník, je pro finanční odhady použit ceník nabídky.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Import odhadů z projektu do nabídky  
 Jakmile máte odhady projektu v projektu, můžete tyto odhady importovat do řádku nabídky:  
  
-   V nabídce **Podrobnosti řádku nabídky** klikněte na tlačítko **Import z odhadů**. 

-   Vyberte, zda chcete importovat odhady projekt sumarizované podle typu transakce, role nebo úrovně uzlu strukturovaného rozpisu prací.  
  
### <a name="see-also"></a>Viz také  
 [Příručka pro projektového manažera](../psa/project-manager-guide.md)
