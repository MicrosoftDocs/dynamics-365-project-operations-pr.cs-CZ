---
title: Režimy plánování
description: Toto téma poskytuje informace o režimech plánování.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981427"
---
# <a name="scheduling-modes"></a>Režimy plánování

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_


Dynamics 365 Project Operations poskytuje organizacím možnost definovat, jak řídí změny klíčových proměnných v úkolech ve strukturovaném rozpisu prací. Na základě konkrétních potřeb organizace mohou projektoví manažeři při vytváření projektu provádět změny v režimu plánování.

V Project Operations jsou k dispozici tři režimy plánování:

  - Pevná doba trvání (toto je výchozí režim)
  - Pevná práce
  - Pevné jednotky

Hodnoty ovlivněné definicí konkrétního režimu plánování jsou určeny následujícím vzorcem:

  Úsilí (*Práce*) = Doba trvání × Jednotky

Když definujete režim plánování projektu, nastavujete jednu z těchto hodnot, kterou pak nelze změnit. Udržování této hodnoty jako konstanty klade prioritu na tuto hodnotu, která upozorní systém, aby ji nezměnil, když se změní další dvě hodnoty. Následující tabulka poskytuje informace o dopadech výběru konkrétního režimu.

| **V tomto úkolu**             | **Pokud revidujete jednotky**   | **Pokud revidujete dobu trvání** | **Pokud revidujete úsilí**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Úkoly s pevnými jednotkami     | Doba trvání se přepočítá. | Úsilí se přepočítá.    | Doba trvání se přepočítá. |
| Úkol s pevným úsilím    | Doba trvání se přepočítá. | Jednotky jsou přepočítány.    | Doba trvání se přepočítá. |
| Úkol s pevnou dobou trvání  | Úsilí se přepočítá.   | Úsilí se přepočítá.    | Jednotky jsou přepočítány.   |

Další informace o implikacích daného režimu najdete v části [Změna typu úkolu pro přesnější plánování](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). V téma se výraz **Práce** se používá místo **Úsilí**.

## <a name="change-the-organizations-scheduling-mode"></a>Změna režimu plánování organizace

Chcete-li definovat režim plánování organizace, proveďte následující kroky.

1. Přejděte na **Nastavení** \> **Obecné** \> **Parametry** a potom vyberte parametr projektu. 
2. Na stránce **Parametry projektu** vyberte výchozí režim plánování pro organizaci a poté definujte možnost projektového manažera přepsat toto nastavení při vytváření nového projektu.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Změna nastavení režimu plánování na projektu

Pokud organizace umožňuje manažerovi projektu přepsat výchozí režim plánování, může projektový manažer tuto změnu provést, když vytvoří nový projekt. Po uložení projektu však nelze režim plánování změnit.

## <a name="copied-projects"></a>Zkopírované projekty

Protože je projekt vytvořen, když je provedena akce kopírování projektu, manažer projektu nemůže nastavit režim plánování. Cílový projekt bude vždy výchozí do režimu definovaného na úrovni organizace.

## <a name="copied-tasks"></a>Zkopírované úkoly

Když je úkol zkopírován z jednoho projektu do druhého, zdědí úkol režim plánování cílového projektu.
