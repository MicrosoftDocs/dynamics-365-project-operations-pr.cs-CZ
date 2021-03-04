---
title: Typy fází projektu
description: Toto téma poskytuje informace o fázích projektu.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 61db23e19614f5c3be5c8b46fbf72463705e409c
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148095"
---
# <a name="project-stage-types"></a>Typy fází projektu 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Fáze projektu jsou koncipovány tak, aby odrážely stav projektu v průběhu jeho vývoje. Přizpůsobení lze použít k automatické aktualizaci fází pomocí toků obchodního procesu, Power Automate nebo rozšíření plug-in.

Ve výchozím toku obchodního procesu jsou definovány následující fáze:

- Nová
- Nabídka
- Plán
- Dodat
- Dokončeno
- Close (Zavřít) 

## <a name="new"></a>Nové

Při vytváření projektu je fáze projektu nastavena na **Nový**. Pokud byl projekt vytvořen ze šablony, může obsahovat plán, odhad a data týmu. V opačném případě je to pouze osnova projektu a zbývající součásti musí být zadány.

## <a name="quote"></a>Nabídka

Když přiřadíte projekt k nabídce nebo když vytvoříte projekt z nabídky, fáze projektu bude nastavena na **Nabídka** a aktualizuje se odhadované datum zahájení a ukončení. Pokud je projekt ve fázi **Nabídka**, zobrazí se podrobnosti o nabídce na kartě **Prodej** na stránce **Entita projektu**.

## <a name="plan"></a>Plán

Pokud vyhrajete nabídku spojenou s projektem a projekt přejde do fáze **Smlouva**, fáze projektu se aktualizuje na **Plán**. Pokud je projekt ve fázi **Plán**, zobrazí se podrobnosti o smlouvě na stránce **Entita projektu**.

## <a name="deliver"></a>Dodat

Když je plán projektu dokončen a jste připraveni ke spuštění projektu, měl by projektový manažer aktualizovat fázi projektu na **Dodat**, aby bylo možné zobrazit, že projekt byl zahájen.

## <a name="complete"></a>Dokončeno 

Po dokončení práce na projektu může projektový manažer aktualizovat fázi na **Dokončeno**. Aktualizací fáze projektu na **Dokončeno** dá projektový manažer najevo, že práce je 100% dokončena, ale že je projekt ponechán otevřený, aby bylo možné zaznamenat všechny nevyřízené časové nebo výdajové záznamy.

## <a name="close"></a>Close (Zavřít)

Jakmile jsou všechny transakce pro projekt zaznamenány, může projektový manažer aktualizovat fázi na **Zavřít**. V tomto okamžiku nelze zaznamenat žádné transakce a projekt je nastaven jen pro čtení.


[!INCLUDE[footer-include](../includes/footer-banner.md)]