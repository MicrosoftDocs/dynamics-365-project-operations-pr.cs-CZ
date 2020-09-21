---
title: Fáze projektu
description: Toto téma poskytuje informace o fázích projektu.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750309"
---
# <a name="project-stages"></a>Fáze projektu 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Fáze projektu jsou aktualizovány tak, aby odrážely stav projektu v průběhu jeho vývoje. Výchozí tok obchodního procesu automaticky aktualizuje některé fáze projektu, zatímco jiné aktualizuje ručně projektový manažer. 

Ve výchozím toku obchodního procesu jsou definovány následující fáze:

- Nové
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
