---
title: Odhady prodeje a projekty
description: Toto téma obsahuje informace o způsobu využití plánu a odhadů v prodejním procesu.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 49d109be3d55e7f208edb2698e420f40bb7843df
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998403"
---
# <a name="sales-estimates-and-projects"></a>Odhady prodeje a projekty

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Během prodejního procesu můžete vytvořit odhady prodeje propojením projektu s prodejní nabídkou. Tímto způsobem může během prodejního procesu proběhnout deterministický odhad, aby bylo možné využít funkce plánování a odhadů projektů. Pokud prodej projde, lze jako základ pro další upřesnění plánu projektu použít plán, který byl použit pro účely odhadu prodeje.

## <a name="linking-a-project-to-a-quote-line"></a>Propojení projektu k řádku nabídky

Při vytváření řádku nabídky založeného na projektu můžete vytvořit nový projekt nebo přidružit existující projekt na stránce **Řádek nabídky**. 

> ![Formulář Řádek nabídky](media/project-8.png)
 
Při vytváření nového projektu z podrobností řádku nabídky můžete využít šablony projektů. Šablony projektů jsou modelové projekty, které představují standardní plány projektů a finanční odhady, které jsou v organizaci typické. Mohou také představovat kopie projektových plánů a odhadů z minulých projektů.

> ![Podrobnosti řádku nabídky](media/project-9.png)
  
Při vytváření projektu z nabídky bude projekt automaticky přidružen k řádku nabídky.

## <a name="components-of-estimates-in-a-project"></a>Komponenty odhadů v projektu

Plán vám umožňuje rozdělit práci na úkoly, udržovat hierarchii úkolů, zjistit, jaké zdroje jsou požadovány k dokončení úkolu, a přiřadit odhad úsilí, které je nutné k dokončení úkolu.

Odhady pracovního úsilí a plánování můžete definovat pomocí polí na kartě **Plán** na stránce **Projekt**. Vzhledem k tomu, že je k projektu přidružen ceník, jsou finanční odhady vypočteny pomocí nákladových a prodejních cen, které jsou definovány v ceníku.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Import odhadů z projektu do nabídky

Po definování odhadů projektu je můžete importovat do řádku nabídky. Chcete-li odhady projektu shrnout podle typu transakce, role nebo úrovně úkolu, vyberte na stránce **Podrobnosti řádku nabídky** na pásu karet **Import z odhadů**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]