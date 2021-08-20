---
title: Typy období
description: Toto téma poskytuje informace o tom, jak nastavit typy období pro odhad výnosů.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 487e3de7895ca0752e6c9033c7bb7007ba89301c01e6205b3bc8a7d750724bc9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998768"
---
# <a name="period-types"></a>Typy období

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Typ období definuje, jak často se odhadují výnosy z projektu. Toto téma poskytuje informace o tom, jak nastavit typy období pro odhad výnosů. 

## <a name="create-and-work-with-period-types"></a>Vytváření a práce s typy období
Chcete-li vytvořit a pracovat s typy období, proveďte následující kroky:

1. Ve vašem prostředí Dynamics 365 Finance přejděte na **Řízení projektů a účetnictví** > **Založit** > **Odhady** > **Typy období**.
2. Výběrem možnosti **Nový** vytvořte nový typ období. Zadejte jméno a popis.
3. Vyberte hodnotu poli **Frekvence**:

    - Pokud vyberete **Týden**, **Dvoutýdenní**, **Půlměsíční**, **Měsíc**, **Den**, **Čtvrtletí** nebo **Rok**, kalendář bude použit ke generování období. 
    - Pokud vyberete **Období účetní knihy**, k vygenerování období se použijí období hlavní knihy z konfigurace hlavní knihy.
    - Pokud vyberete **Neomezený**, můžete zadat vlastní období.
4. Vyberte záznam typu období a poté vyberte **Generovat období** k vytvoření období pro typ období. Na základě zvolené frekvence období můžete mít možnost určit datum zahájení nebo počet období, která se mají vygenerovat.
5. Vyberte **Období**, chcete-li zkontrolovat vygenerovaná období.



[!INCLUDE[footer-include](../includes/footer-banner.md)]