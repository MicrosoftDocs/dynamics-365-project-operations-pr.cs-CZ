---
title: Fáze projektu
description: Tento téma poskytuje informace o projektových fázích dostupných v Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b11c67ebd21fdf423eeae2db8154f26787c2e64f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897938"
---
# <a name="project-stages"></a>Fáze projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Fáze projektu jsou koncipovány tak, aby odrážely stav projektu v průběhu jeho vývoje. Přizpůsobení lze použít k automatické aktualizaci fází pomocí toků obchodního procesu, Power Automate nebo rozšíření plug-in.

Ve výchozím toku obchodního procesu jsou definovány následující fáze:

- Nové
- Nabídka
- Plán
- Dodat
- Dokončit
- Uzavřeno 

## <a name="new"></a>Nové

Při vytváření projektu je fáze projektu nastavena na **Nový**. Pokud byl projekt vytvořen ze šablony, může obsahovat plán, odhad a data týmu. V opačném případě je to osnova projektu a zbývající součásti musí být zadány.

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

