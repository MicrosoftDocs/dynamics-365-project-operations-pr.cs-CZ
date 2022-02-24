---
title: Typy období
description: Toto téma poskytuje informace o tom, jak nastavit typy období pro odhad výnosů.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531389"
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

