---
title: Aktualizace projektu
description: Toto téma poskytuje informace o aktualizaci projektů v aplikaci Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: b0ec03a2c4dd7bc833b22b7a93fed810b4998a2788f4ff40234e3dd163bd9eb6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000883"
---
# <a name="update-a-project"></a>Aktualizace projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Níže je uveden souhrn polí, která lze aktualizovat na projektu po jeho vytvoření, a všechny příslušné důsledky aktualizací.

## <a name="project-detail-fields"></a>Pole podrobností projektu

- **Název**: Název projektu.
- **Popis**: Přehled projektu.
- **Zákazník**: Společnost, do které bude projekt dodán.
- **Šablona kalendáře**: Pracovní doba projektu. Když se pole změní, přepočítá se celý plán.
- **Měna**: Měna projektu. Toto pole je výchozí na základě měny definované ve smluvní jednotce. Při aktualizaci smluvní jednotky se aktualizuje také pole.
- **Smluvní jednotka**: Organizační jednotka, která zastupuje skupinu nebo divizi společnosti, která je primárně zodpovědná za získání prodeje a řízení dodávky práce a služeb zákazníkovi. 
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