---
title: Kopírování projektu
description: Toto téma obsahuje informace o kopírování projektů v Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007183"
---
# <a name="copy-a-project"></a>Kopírování projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

V Dynamics 365 Project Operations můžete rychle vytvářet nové projekty výběrem volby **Kopírovat projekt** ve formuláři **Projekty**. Chcete-li zkopírovat projekt, otevřete projekt, který chcete zkopírovat, a poté vyberte **Kopírovat projekt**. Akce zkopíruje následující:

- Vlastnosti projektu 
- Strukturovaný rozpis prací
- Členové projektových týmů
- Odhady projektů
- Odhady projektových výdajů
- Odhady materiálu projektu

## <a name="project-properties"></a>Vlastnosti projektu

Při kopírování projektu se zkopírují hodnoty v následujících polích:

- Jméno
- Popis
- Zákazník
- Šablona kalendáře
- Měna
- Smluvní jednotka
- Projektový manažer
- Stav
- Celkový stav projektu
- Komentáře
- Odhady
- Odhadované datum zahájení: Toto je datum, kdy je projekt vytvořen z kopie.
- Odhadované datum dokončení: Toto datum je upraveno na základě data zahájení nového projektu, který byl vytvořen z kopie.
- Úsilí (hodiny)
- Odhadované pracovní náklady
- Odhadované výdajové náklady
- Odhadované náklady na materiál

> [!NOTE]
> Projekt kopírování je dlouhá operace. Kopírují se také záznamy projektu, jejich příslušné atributy a mnoho souvisejících entit. Z důvodu dlouhodobé povahy operace je po spuštění kopírování cílová stránka projektu uzamčena pro úpravy, dokud není operace kopírování dokončena.

## <a name="work-breakdown-structure"></a>Strukturovaný rozpis prací

Když je projekt zkopírován, zkopíruje se celý strukturovaný rozpis prací načtený ze zdrojů. Pojmenované zdroje jsou nahrazeny obecnými zdroji. Pokud pojmenované zdroje nemají stejnou pracovní dobu jako obecný zdroj, plán se přepočítá a doba trvání úkolu se může změnit.

## <a name="project-team-members"></a>Členové projektových týmů

Když se projektový tým zkopíruje ze zdrojového projektu, zkopírují se obecné zdroje. Přiřazení obecných zdrojů jsou rovněž zachována tak, jako byla ve zdrojovém projektu. Pojmenované zdroje budou převedeny na obecné členy týmu.

## <a name="estimates"></a>Odhady

Při kopírování projektu se zkopírují řádky odhadu zdrojů, výdajů a materiálu ze zdrojového projektu. 

Informace o tom, jak programátorsky přistupovat ke kopírování projektu, najdete v části [Vývoj projektových šablon pomocí nástroje kopírovat projekt](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
