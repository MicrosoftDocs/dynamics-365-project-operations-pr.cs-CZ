---
title: Aktualizace odhadu nákladů při dokončení
description: Tento téma poskytuje informace o aktualizaci projekce úsilí na projekt.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897758"
---
# <a name="update-estimate-at-completion"></a>Aktualizace odhadu nákladů při dokončení

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Je běžné, že projektový manažer reviduje původní odhady úkolu. Předpovědi projektu jsou vnímání odhadů projektového manažera podle aktuálního stavu projektu. Nedoporučujeme však, aby projektoví manažeři směrná čísla měnili, protože směrný plán projektu představuje stanovený zdroj pravdy pro odhady plánů a nákladů projektu a všichni účastníci projektu se na něm shodli.

Projektový manažer může předpovědět úsilí na úkoly dvěma způsoby:

- Přepsat výchozí odhad na dokončení (ETC) novým odhadem skutečně zbývajícího úsilí na úkol. 
- Přepsat výchozí procento pokroku novým odhadem skutečného pokroku u úkolu.

Každý z těchto přístupů způsobuje přepočet hodnot ETC, EAC a procenta pokroku a očekávané odchylky úsilí daného úkolu. Přepočítají se hodnoty EAC, ETC a procento pokroku souhrnných úkolů a vytvoří se nová projekce odchylky úsilí.
