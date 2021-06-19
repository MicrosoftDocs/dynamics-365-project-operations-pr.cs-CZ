---
title: Kopírování příležitostí na základě projektu
description: Toto téma poskytuje informace o tom, jak kopírovat příležitosti založené na projektu v Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae724d18e768b838f388b6fd089bfa657c937da1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013433"
---
# <a name="copy-project-based-opportunities"></a>Kopírování příležitostí na základě projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_


Příležitosti projektu lze snadno kopírovat, a vytvářet tak nové příležitosti projektu. 

1. Přejděte na stránku se seznamem **Příležitosti projektu** a vyberte příležitost ze seznamu. Nebo otevřete stránku s podrobnostmi o konkrétní příležitosti. 
2. Na kterékoli stránce vyberte **Kopírovat**. Otevře se dialogová stránka, která obsahuje následující informace o poli. V závislosti na vámi vybraných hodnotách v tomto dialogovém okně se může proces kopírování změnit.

    | **Pole** | **Popis** | **Dopad na příjem dat** |
    | --- | --- | --- |
    | Téma | Zadejte relevantní téma cílové příležitosti. Když se otevře dialogové okno, systém jej nastaví na téma zdrojové příležitosti, ke kterému připojí řetězec **-kopie**. | Neexistuje žádný následný dopad na toto pole. |
    | Účet | Odkazuje na záznam společnosti nebo účtu zákazníka. Když se otevře dialogové okno, systém jej nastaví na účet ve zdrojové příležitosti. | Toto pole je primárním zákazníkem příležitosti. |
    | Smluvní jednotka | Organizační jednotka, která je odpovědná za realizaci projektů asociovaných s tímto obchodem. Když se otevře dialogové okno, systém jej nastaví na smluvní jednotku zdrojové příležitosti. | Smluvní jednotka je divize společnosti, která realizuje projekty po uzavření obchodu. Každá smluvní jednotka má měnu a tato měna se používá k vykazování odhadovaných a skutečných nákladů vzniklých během projektu. |
    | Měna | Měna, ve které se provádí obchod. Když se otevře dialogové okno, systém jej nastaví na měnu zdrojové příležitosti. | Měna se používá k nastavení výchozího ceníku a sestavení finančních odhadů z nabídky. Měna se nakonec použije k fakturaci zákazníkovi, když je obchod vyhrán. |
    | Kopírování cen | Hodnota Ano/ne, která označuje, zda by měla být cena příležitosti zkopírována ze zdrojové příležitosti. | Pokud je vybrána možnost **Ano**, ceníky jsou zkopírovány ze zdroje do cílové příležitosti. Když je vybrána hodnota **Ne**, u ceníků jsou obnoveny původní hodnoty na základě nejnovějších ceníků, které byly nastaveny. |

3. Vyberte **OK**. Systém vytvoří kopii projektové příležitosti na základě vybraných parametrů a otevře se nová projektová příležitost.


[!INCLUDE[footer-include](../includes/footer-banner.md)]