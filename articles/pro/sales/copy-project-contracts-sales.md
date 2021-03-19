---
title: Kopírování projektových smluv – omezené
description: Toto téma poskytuje informace o kopírování projektových smluv v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a0ffb807c8254f4d392c4750fa0b4a60f7fd26b0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273730"
---
# <a name="copy-project-contracts---lite"></a>Kopírování projektových smluv – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Nové projektové smlouvy můžete snadno vytvořit vytvořením kopií stávajících smluv jedním ze dvou způsobů: 

  - Na stránce se seznamem **Projektových smluv** vyberte projektovou smlouvu a pak vyberte **Kopírovat**.
  - Na stránce s údaji **Projektová smlouva** vyberte **Kopírovat**.

Otevře se dialogová stránka, kde můžete zadat parametry kopírované smlouvy. V dialogovém okně jsou následující pole. V závislosti na vámi vybraných hodnotách v tomto dialogovém okně se může proces kopírování změnit.

| **Pole** | **Popis** | **Dopad na příjem dat** |
| --- | --- | --- |
| Téma | Zadejte téma cílové smlouvy. Když se otevře dialogové okno, systém toto pole nastaví na název zdrojové smlouvy, ke kterému připojí řetězec **-kopie**. | Neexistuje žádný následný dopad na toto pole. |
| Zákazník | Odkaz na záznam společnosti nebo účtu zákazníka. Když se otevře dialogové okno, systém toto pole nastaví na účet ve zdrojové smlouvě. | Toto pole je primárním zákazníkem smlouvy. |
| Smluvní jednotka | Organizační jednotka, která je odpovědná za realizaci projektů asociovaných s touto dohodou. Když se otevře dialogové okno, systém jej nastaví na smluvní jednotku zdrojové smlouvy. | Smluvní jednotka je divize společnosti, která bude realizovat projekty po uzavření obchodu. Každá smluvní jednotka má měnu. Tato měna se používá k vykazování odhadovaných a skutečných nákladů vzniklých během projektu. |
| Měna | Měna, ve které se provádí obchod. Když se otevře dialogové okno, systém nastaví pole na měnu zdrojové smlouvy. Měnu lze změnit. Pokud tomu tak je, pole **Kopírovat ceny** je vždy nastaveno na **Ne**, protože ceníky na zdrojové smlouvě již nejsou relevantní. | Měna se používá pro výchozí ceníky, k sestavení finančního odhadu smlouvy a k fakturaci zákazníkovi, když je obchod vyhrán. |
| Požadované datum dodávky | Datum dodání požadované zákazníkem. | Toto datum se používá jako datum ukončení při vytváření fakturačních dat podle konkrétní frekvence. |
| Kopírování cen | Udává, zda by měla být cena za smlouvu zkopírována ze zdrojové smlouvy. | Pokud je pole nastaveno na **Ano**, reference ceníku projektu a produktu jsou zkopírovány ze zdrojové do cílové smlouvy. Když je vybrána hodnota **Ne**, u ceníků jsou obnoveny původní hodnoty na základě nejnovějších ceníků v parametrech účtu nebo projektu. |

Když na stránce dialogu vyberete možnost **OK**, vytvoří systém kopii smlouvy na základě vybraných parametrů. Nová smlouva se otevře.

Následující informace se nekopírují ze **zdrojové** do **cílové smlouvy**:

  - Rozpisy faktur
  - Zákazníci smlouvy a řádku smlouvy
  - Odkaz na projekt na řádcích smlouvy na základě projektu
  - Rozpočtové údaje zákazníka

Protože tyto informace jsou specifické pro každou smlouvu, tato pole a záznamy se nekopírují. Zkopírují se řádky smlouvy u projektů a produktů, odhady u podrobností řádků smlouvy a hodnoty, které nesmějí být překročeny na úrovni smlouvy. Výchozí sazby cen a nákladů jsou závislé na výběru v poli **Kopírovat ceny**, vybrané na stránce dialogu **Kopírovat parametry**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]