---
title: Kopírování nabídek založených na projektu
description: Toto téma poskytuje informace o tom, jak kopírovat nabídky založené na projektu v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b1ce6c2b644319f2d822010a34c57c591f82edc9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278140"
---
# <a name="copy-project-based-quotes"></a>Kopírování nabídek založených na projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Novou projektovou nabídku můžete snadno vytvořit zkopírováním existující nabídky. 

- Chcete-li zkopírovat projektovou nabídku, vyberte na stránce seznamu **Projektové nabídky** nebo na stránce detailů **Projektová nabídka** projektovou nabídku, kterou chcete zkopírovat, a poté vyberte příkaz **Kopírovat**.

Otevře se dialogová stránka, kde můžete zadat parametry kopie. V následující tabulce jsou uvedena pole, která najdete v dialogové stránce. V závislosti na vámi vybraných hodnotách se může proces kopírování změnit.

| **Pole** | **Popis** | **Dopad na příjem dat** |
| --- | --- | --- |
| Téma | Zadejte příslušné téma nebo název cílové nabídky. Když se otevře dialog, systém jej nastaví na téma zdrojové nabídky, ke kterému připojí řetězec **-kopie**. | |
| Potenciální zákazník | Odkaz na záznam společnosti nebo účtu zákazníka. Když se otevře dialogové okno, systém jej nastaví na účet ve zdrojové nabídce. | Toto pole je primárním zákazníkem nabídky. |
| Smluvní jednotka | Organizační jednotka, která je odpovědná za realizaci projektů asociovaných s touto dohodou.
Když se otevře dialogové okno, systém jej nastaví na smluvní jednotku zdrojové nabídky. | Smluvní jednotka je divize společnosti, která bude realizovat projekty po uzavření obchodu. Každá smluvní jednotka má měnu. Měna se používá k vykazování odhadovaných a skutečných nákladů vzniklých během realizace projektu. |
| Měna | Toto je měna, ve které se provádí obchod. Když se otevře dialogové okno, systém jej nastaví na měnu zdrojové nabídky. To lze upravit, a pokud se jedná o změnu, je pole **Kopírovat ceny** vždy nastaveno na **Ne**. Došlo k tomu proto, že ceníky zdrojové nabídky již nejsou relevantní. | Měna se používá k nastavení výchozího ceníku, k sestavení finančního odhadu nabídky a případně k fakturaci zákazníkovi, když je obchod vyhrán. |
| Požadované datum dodávky | Toto je datum dodání požadované zákazníkem. | Toto se používá jako datum ukončení při vytváření fakturačních dat podle konkrétní frekvence. |
| Kopírování cen | Hodnota Ano/Ne udává, zda by měla být cena za nabídku zkopírována ze zdrojové nabídky. | Když je vybrána hodnota **Ano**, ceník projektu a reference ceníku produktu jsou zkopírovány ze zdrojové nabídky do cílové nabídky. Když je vybrána hodnota **Ne**, u ceníků jsou obnoveny původní hodnoty na základě nejnovějších ceníků, které byly nastaveny v parametrech účtu nebo projektu. |

Když na stránce dialogu vyberete možnost **OK**, vytvoří systém kopii projektové nabídky na základě parametrů vybraných v dialogu. Otevře se nová projektová nabídka. 

> [!NOTE]
> Následující informace se nekopírují ze zdrojové do cílové nabídky:
>
> - Rozpisy faktur
> - Nabídka a zákazníci na řádku nabídky
> - Projektové reference u řádků nabídek založených na projektu – Informace o rozpočtu zákazníka
>
>Protože tyto informace jsou specifické pro každou nabídku zvlášť, tato pole a záznamy se nekopírují. Zkopírují se řádky nabídek u projektů a produktů, odhady u podrobností řádků nabídek a hodnoty, které nesmějí být překročeny na úrovni nabídky. Výchozí sazby cen a nákladů jsou závislé na možnosti **Kopírovat ceny**, vybrané na stránce dialogu **Kopírovat parametry**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]