---
title: Kopírování projektových smluv
description: Tento článek poskytuje informace o kopírování projektových smluv v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410312"
---
# <a name="copy-project-based-contracts"></a>Kopírování projektových smluv

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Nové projektové smlouvy můžete snadno vytvořit vytvořením kopií stávajících smluv jedním ze dvou způsobů:

- Na stránce se seznamem **Projektových smluv** vyberte projektovou smlouvu a pak vyberte **Kopírovat**.
- Na stránce s údaji **Projektová smlouva** vyberte **Kopírovat**.

V obou případech se otevře dialogová stránka, kde můžete nastavit parametry kopírované smlouvy. V dialogovém okně jsou následující pole. V závislosti na vámi vybraných hodnotách se může proces kopírování změnit.

| Pole | Description | Dopad na následné složky |
| --- | --- | --- |
| Popis | Zadejte téma cílové smlouvy. Když se otevře dialogové okno, systém toto pole nastaví na název zdrojové smlouvy, ke kterému připojí slovo „kopie“. | Neexistuje žádný následný dopad na toto pole. |
| zákazníku | Odkaz na záznam společnosti nebo účtu zákazníka. Když se otevře dialogové okno, systém toto pole nastaví na účet ve zdrojové smlouvě. | Toto pole je primárním zákazníkem smlouvy. |
| Vlastnící společnost | Společnost, která je odpovědná za realizaci projektů asociovaných s touto dohodou. Když se otevře dialogové okno, systém toto pole nastaví na vlastnící společnost ve zdrojové smlouvě. | Vlastnící společnost je právnická osoba, která bude projekt realizovat po uzavření obchodu. Měna vlastnící společnosti musí odpovídat měně smluvní jednotky. |
| Smluvní jednotka | Organizační jednotka, která je odpovědná za realizaci projektů asociovaných s touto dohodou. Když se dialogové okno otevře, systém nastaví pole na smluvní jednotku zdrojové smlouvy. | Smluvní jednotka je divize společnosti, která bude realizovat projekty po uzavření obchodu. Každá smluvní jednotka má měnu. Tato měna se používá k vykazování odhadovaných a skutečných nákladů vzniklých během projektu. |
| Měna | Měna, ve které se provádí obchod. Když se otevře dialogové okno, systém nastaví pole na měnu zdrojové smlouvy. Měnu lze změnit. Pokud tomu tak je, pole **Kopírovat ceny** je vždy nastaveno na **Ne**, protože ceníky na zdrojové smlouvě již nejsou relevantní. | Tato měna se používá pro výchozí ceníky, ke generování finančního odhadu smlouvy a k fakturaci zákazníkovi, když je obchod vyhrán. |
| Požadované datum dodávky | Datum dodání požadované zákazníkem. | Toto datum se používá jako datum ukončení při vytváření fakturačních dat podle konkrétní frekvence. |
| Kopírování cen | Hodnota, která udává, zda by měla být cena za smlouvu zkopírována ze zdrojové smlouvy. | Pokud je pole nastaveno na **Ano**, reference ceníku projektu a produktu jsou zkopírovány ze zdrojové do cílové smlouvy. Když je vybrána hodnota **Ne**, u ceníků jsou obnoveny výchozí hodnoty na základě nejnovějších ceníků v parametrech účtu nebo projektu. |

Když na stránce dialogu vyberete možnost **OK** v dialogovém okně, vytvoří systém kopii smlouvy na základě hodnot parametrů, které nastavíte. Pak se otevře nová smlouva.

Následující informace se **nezkopírují** ze zdrojové smlouvy do cílové smlouvy, protože jsou specifické pro každou smlouvu:

- Rozpisy faktur
- Zákazníci smlouvy a řádku smlouvy
- Odkaz na projekt na řádcích smlouvy na základě projektu
- Rozpočtové údaje zákazníka

Zkopírují se řádky smlouvy u projektů a produktů, odhady u podrobností řádků smlouvy a hodnoty, které nesmějí být překročeny na úrovni smlouvy. Zadání výchozích cen a sazeb nákladů jsou závislé na výběru v poli **Kopírovat ceny**, vybrané v dialogovém okně **Kopírovat parametry**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
