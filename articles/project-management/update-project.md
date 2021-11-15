---
title: Vytvoření a aktualizace projektu
description: Toto téma poskytuje informace o aktualizaci projektů v aplikaci Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d0847b5343cf3e353b91eae04c94509f14213ba5
ms.sourcegitcommit: 51224cb3bf7cdeae6614d39fc8d899c83dbad5f2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/23/2021
ms.locfileid: "7678341"
---
# <a name="create-and-update-a-project"></a>Vytvoření a aktualizace projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Následuje souhrn polí, která lze v projektu po jeho vytvoření aktualizovat. Patří sem také jakékoli použitelné důsledky založené na těchto aktualizacích.

## <a name="project-detail-fields"></a>Pole podrobností projektu

- **Název**: Název projektu.
- **Popis**: Přehled projektu.
- **Zákazník**: Společnost, do které bude projekt dodán.
- **Šablona kalendáře**: Pracovní doba projektu. Když se pole změní, přepočítá se celý plán.
- **Měna**: Měna projektu. Výchozí hodnota pro toto pole je založena na měně definované ve smluvní jednotce. Při aktualizaci smluvní jednotky se aktualizuje také pole.
- **Smluvní jednotka**: Organizační jednotka, která zastupuje skupinu nebo divizi společnosti, která je primárně zodpovědná za získání prodeje a řízení dodávky práce a služeb zákazníkovi.  Pokud není definována organizační jednotka projektového manažera, má toto pole výchozí hodnotu definovanou v parametrech projektu.
- **Projektový manažer**: Člen projektového týmu, který má oprávnění kontrolovat a schvalovat časové údaje a výdaje.

## <a name="estimate-fields"></a>Odhad polí

- **Odhadované počáteční datum**: Počáteční datum projektu. Když se toto pole aktualizuje, všechny úkoly na projektu se budou pohybovat úměrně s počátečním novým začátkem.
- **Datum dokončení**: Datum, kdy je naplánováno ukončení projektu.
- **Úsílí**: Odhadované úsilí projektu. Když jsou do projektu přidány úkoly, toto pole již nelze upravovat.
- **Odhadované náklady na práci**: Odhadované pracovní náklady projektu. Když jsou do projektu přidány pracovní náklady, toto pole již nelze upravovat.
- **Odhadované výdaje**: Odhadované výdaje projektu. Když jsou do projektu přidány výdaje, toto pole již nelze upravovat.

## <a name="project-actual-fields"></a>Pole skutečné hodnoty projektu
- **Skutečný začátek**: Datum zahájení projektu.
- **Skutečné dokončení**: Bude aktualizováno po dokončení projektu.

## <a name="project-status-fields"></a>Pole Stav projektu

- **Celkový stav projektu**: Celkový stav projektu poskytnutý manažerem projektu.
- **Komentáře**: Textový komentář týkající se aktuálního stavu projektu poskytnutý manažerem projektu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
