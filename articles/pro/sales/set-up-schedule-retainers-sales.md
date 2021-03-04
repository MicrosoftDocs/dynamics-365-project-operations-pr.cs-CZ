---
title: Nastavit plán záloh
description: Tohle téma poskytuje informace, jak nastavit plán záloh v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1c264b544660cf7a0b116f09b6bd7c94fcf0457e
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596364"
---
# <a name="set-up-a-retainer-schedule"></a>Nastavit plán záloh

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Plány záloh lze nastavit na stránce **Projektová smlouva** v Dynamics 365 Project Operations.

1. Na stránce **Projektová smlouva** na kartě **Zálohy** vyberte **Nastavení plánu záloh**.
2. Na otevřené stránce dialogového okna jsou uvedena pole z následující tabulky. Tabulka poskytuje představu o tom, jak zadané hodnoty ovlivňují plán záloh, který bude vytvořen.

| Pole | Popis | Dopad na následné složky |
| --- | --- | --- |
| Zákazník projektové smlouvy | Zákazníki na smlouvě, kterému bude fakturována tato záloha. | Pokud máte na smlouvě více zákazníků a potřebujete každému z nich fakturovat konkrétní zálohu nebo částku zálohy, ručně vytvořte jednu fakturu pro každého zákazníka. |
| Začátek plánu záloh | Zadejte datum zahájení plánu záloh. | Toto datum nemusí být datem vytvoření první zálohy. Datum vytvoření první zálohy je také ovlivněno četností fakturace. |
| Konec plánu záloh | Zadejte datum ukončení plánu záloh. | Toto datum nemusí být datem vytvoření poslední zálohy. Datum vytvoření poslední zálohy je také ovlivněno četností fakturace. |
| Počet záloh, které mají být vytvořeny | Když zadáte počet záloh, které chcete vytvořit, systém použije počáteční datum a četnost k vytvoření čísla v tomto poli. | Když je toto pole ručně aktualizováno, systém ignoruje hodnotu v poli **Konec plánu záloh** a místo toho vytvoří konkrétní počet záloh. |
| Frekvence faktur | Jak často aplikace vytvoří zálohy. | Tato hodnota přímo ovlivňuje počet záloh a vytvořená data. |
| Celková částka | Celková částka je částka rozdělená na jednotlivé zálohy, které budou vytvořeny. | Neexistuje žádný následný dopad na toto pole. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]