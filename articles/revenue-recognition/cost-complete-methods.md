---
title: Metody nákladů na dokončení
description: Toto téma poskytuje informace o metodách použitých k výpočtu nákladů na dokončení projektu.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c6d3cd6056466be686f15c9f332c8274aeb0ac19
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013928"
---
# <a name="cost-to-complete-methods"></a>Metody nákladů na dokončení

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Toto téma poskytuje informace o metodách použitých k výpočtu nákladů na dokončení projektu. Existuje několik metod, které můžete použít k výpočtu nákladů na dokončení projektu. 

Když vytvoříte odhad pro projekt, na stránce **Vytvořit odhad** v poli **Metoda nákladů na dokončení** můžete k vybrat jednu z následujících metod nákladů na dokončení.

| Metoda nákladů na dokončení    | Popis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Celkové náklady – skutečné            | Zadejte odhadované náklady ručně do pole **Celkové náklady** nebo **Celkové množství** pomocí tlačítka **Odhad nákladů** na **Stránce odhadů**. Systém odečte skutečné náklady od součtů, které jste zadali. Součet představuje náklady na dokončení projektu. Tato metoda nepoužívá odhady výdajů a přiřazení zdrojů zadané v rámci Project Operations v rámci Microsoft Dataverse. Celkové náklady nebo celkové množství lze podle potřeby aktualizovat ručně.  |
| Celkový odhad - skutečný        | Přiřazení zdrojů a odhady výdajů se používají k určení celkové předpokládané částky projektu. Skutečné náklady jsou porovnány s touto prognózou a vypočítají se náklady na dokončení.                                                                                                                                                                                                                                                                          |
| Jako předchozí odhad         | Zde se používají stejné metody odhadu, jaké byly použity v předchozím období. Tato metoda vyžaduje model předpovědi, pokud předchozí období vyžadovalo model předpovědi.                                                                                                                                                                                                                                                                                                                           |
| Nastavení nákladů na dokončení na nulu | Tato metoda se obvykle používá před odstraněním odhadu projektu a odpovídá celkovým odhadům se zaúčtovanými skutečnými transakcemi a vymaže sloupec **Náklady na dokončení**. Po dokončení je výsledek vždy stoprocentní. Pro každý řádek nákladů, který vytvoříte, je zrušeno zaškrtnutí tlačítka **Prognózy** a celkový odhad je zkopírován z předchozího odhadu nákladů. Skutečná spotřeba za odhadované období se odečte od nákladů na dokončení projektu.              |
| Ze šablony nákladů           | Metoda nákladů na dokončení, která je nastavena v šabloně nákladů, která je přidružena k vybranému odhadu projektu.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]