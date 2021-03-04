---
title: Šablony projektů
description: Toto téma poskytuje informace o tom, jak používat šablony projektů pro rychlé nastavení projektu.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: db42c9ea7280274cdc9cc90f1487f27e08f892e5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148050"
---
# <a name="project-templates"></a>Šablony projektů 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Šablona projektu je předdefinovaná struktura, která pomáhá rychle a snadno spustit projekt. Pomocí předdefinované šablony můžete vytvořit nový projekt jediným klepnutím. Pro šablony projektů musíte, stejně jako pro projekty, definovat předpoklady. Pro každou šablonu projektu musíte definovat kalendář projektu a role a ceníky musí být v organizaci předdefinované, aby komponenty šablony obsahovaly užitečná data.

Šablona projektu sestává ze tří komponent: plánu, odhadů projektu a členů projektového týmu.

## <a name="schedule"></a>Naplánovat

Plán v šabloně projektu obsahuje stejnou sadu prvků jako plán v projektu. Můžete vytvořit hierarchii úkolů, přiřadit role k úkolům, definovat atributy plánu a nastavit závislosti. Plán v šabloně projektu podporuje pro jednotlivé úkoly také režimy úkolů. Proto tedy podporuje plánovací modul. K projektu je nutné přidružit projektový kalendář. Při vytváření pracovního plánu není mezi šablonou projektu a projektem žádný rozdíl.

## <a name="project-estimates"></a>Odhady projekt

Odhady projektu v šabloně projektu fungují stejným způsobem jako odhady projektu v projektu. Nákladové a prodejní ceny jsou však vyžádány z výchozích nákladových a prodejních ceníků, které jsou definovány v parametrech.

## <a name="creating-a-project-from-a-template"></a>Vytvoření projektu ze šablony
 
Existuje několik způsobů, jak vytvořit projekt ze šablony projektu:

- Při vytváření projektu z nabídky můžete vybrat šablonu projektu v dialogovém okně **Vytvořit: Projekt**.

> ![Dialogové okno Vytvořit: Projekt](media/project-11.png)

- Při vytváření projektu výběrem **Nový projekt** se před uložením záznamu zobrazí stránka **Projekt**. V poli **Vybrat šablonu** vyberte jednu z předdefinovaných šablon projektů v organizaci.
- Použijte **Vytvořit projekt ze šablony** na stránce **Entita šablona**.

## <a name="copying-components-of-template-to-project"></a>Kopírování komponent šablony do projektu

Při kopírování komponent šablony projektu do projektu může dojít k několika přepsáním v závislosti na nastavení v projektu.

### <a name="copying-the-schedule"></a>Kopírování plánu

Pokud má projekt při kopírování plánu ze šablony projektu jiný kalendář projektu než šablona, bude v plánu úkolů použita pracovní doba z kalendáře projektu. Tímto způsobem se plán upraví, aby odpovídal pomocnému kalendáři projektu. A podobně první úkol v plánu bude mít datum zahájení projektu a plán zbytku hierarchie bude aktualizován na základě doby trvání a závislostí, které jsou uvedeny v šabloně. 

### <a name="copying-project-estimates"></a>Kopírování odhadů projektu 

Při kopírování mezi řádky odhadů projektu jsou ceníky aktualizovány. U nákladového ceníku jsou tyto aktualizace založeny na vlastnící jednotce projektu. U prodejního ceníku jsou založeny na zákazníkovi. U projektů, které jsou přidruženy k entitě prodeje, jsou nákladové a prodejní ceny na jednotku stanoveny na základě těchto ceníků.

### <a name="copying-a-project-team"></a>Kopírování projektového týmu

Při kopírování projektového týmu ze šablony projektu do projektu jsou obecné zdroje zkopírovány spolu s dovednostmi a odbornými znalostmi, které jsou definovány v šabloně. Přiřazení obecných zdrojů jsou rovněž zachována tak, jako byla v šabloně projektu. V šablonách projektů nejsou podporovány pojmenované zdroje.
