---
title: Řešení prodejních cen pro odhady projektu a skutečné hodnoty
description: Tento článek poskytuje informace o vyřešení nákladových cen u projektových odhadů a skutečných hodnot.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9a6a19a866ab3218f2a0fa297b5f6a00ed809d2f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917476"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Řešení prodejních cen pro odhady projektu a skutečné hodnoty

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Když jsou vyřešeny prodejní ceny na základě odhadů a skutečností v Dynamics 365 Project Operations, systém nejprve použije datum a měnu související nabídky projektu nebo smlouvy k vyřešení ceníku prodejní ceny. Po vyřešení prodejního ceníku systém vyřeší prodejní nebo fakturační sazbu.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Vyřešení prodejních sazeb v řádcích skutečností a odhadů pro čas

V Project Operations se řádky odhadů pro čas používají k označení řádků nabídek a podrobností řádků smluv pro čas a přiřazení prostředků v projektu.

Po vyřešení prodejního ceníku systém provede následující kroky a nastaví výchozí fakturační sazbu.

1. Systém používá pole **Role** a **Jednotka zdroje** na řádku odhadu pro čas, aby řádek spároval s řádky cen rolí ve vyřešeném ceníku. Tato párování předpokládá, že se používají předem připravené cenové dimenze pro fakturační sazby. Pokud jste konfigurovali ceny na základě jakýchkoli jiných polí namísto polí **Role** a **Jednotka zdroje** nebo kromě nich, pak to je kombinace, která bude použita k načtení odpovídajícího řádku ceny role.
2. Pokud systém najde řádek ceny role, který má fakturační sazbu pro kombinaci polí **Role** a **Jednotka zdroje**, pak je tato fakturační sazba výchozí.
3. Pokud systém neumí spárovat hodnoty polí **Role** a **Jednotka zdroje**, načte řádky cen rolí se shodnou rolí, ale s hodnotami null v poli **Jednotka zdroje**. Poté, co systém najde odpovídající záznam ceny role, nastaví výchozí fakturační sazbu podle tohoto záznamu. Tato shoda předpokládá předem připravenou konfiguraci pro relativní prioritu **Role** vs. **Jednotka role** jako dimenze prodejních cen.

> [!NOTE]
> Pokud jste konfigurovali jinou prioritu polí **Role** a **Jednotka zdroje** nebo pokud máte jiné dimenze s vyšší prioritou, toto chování se odpovídajícím způsobem změní. Systém načte záznamy cen rolí se shodnými hodnotami každé z hodnot cenových dimenzí v pořadí podle priority s řádky, které mají hodnoty null pro tyto dimenze, uvedenými až nakonec.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Vyřešení prodejních sazeb v řádcích skutečností a odhadů pro výdaje

V Project Operations se řádky odhadů pro výdaje používají k označení řádků nabídek a podrobností řádků smluv pro výdaje a řádků odhadů výdajů v projektu.

Po vyřešení prodejního ceníku systém provede následující kroky a nastaví výchozí prodejní cenu jednotky.

1. Systém používá kombinaci polí **Kategorie** a **Jednotka** na řádku odhadu pro výdaje, aby řádek spároval s řádky cen kategorií ve vyřešeném ceníku.
2. Pokud systém najde řádek ceny kategorie, který má prodejní sazbu pro kombinaci polí **Kategorie** a **Jednotka**, pak je tato prodejní sazba výchozí.
3. Pokud systém najde odpovídající řádek ceny kategorie, lze metodu stanovení cen použít ke stanovení výchozí prodejní ceny. Následující tabulka ukazuje výchozí chování ceny výdajů v Project Operations.

    | Kontext | Způsob ocenění | Výchozí cena |
    | --- | --- | --- |
    | Odhad | Cena za jednotku | Na základě řádku ceny kategorie |
    | &nbsp; | Podle nákladů | 0.00 |
    | &nbsp; | Přirážka k nákladům | 0.00 |
    | Skutečnost | Cena za jednotku | Na základě řádku ceny kategorie |
    | &nbsp; | Podle nákladů | Na základě skutečných souvisejících nákladů |
    | &nbsp; | Přirážka k nákladům | Aplikování přirážky definované v řádku ceny kategorie na sazbu jednotkové ceny související skutečné ceny |

4. Pokud systém není schopen spárovat hodnoty polí **Kategorie** a **Jednotka**, je výchozí hodnota prodejní sazby nula (0).

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Řešení prodejních sazeb na řádcích skutečností a odhadů pro materiál

V aplikaci Project Operations se řádky odhadu pro materiál používají k označení podrobností řádku nabídky a řádku smlouvy u materiálů a řádky odhadu materiálu na projektu.

Po vyřešení prodejního ceníku systém provede následující kroky a nastaví výchozí prodejní cenu jednotky.

1. Systém používá kombinaci polí **Produkt** a **Jednotka** na řádku odhadu materiálu pro spárování s řádky položky ceníku v ceníku, který byl vyřešen.
2. Pokud systém najde řádek položky ceníku, který má sazbu prodeje pro kombinaci polí **Produkt** a **Jednotka** a metoda ocenění je **Částka měny**, použije se prodejní cena uvedená v řádku ceníku.
3. Pokud se hodnoty polí **Produkt** a **Jednotka** neshodují, výchozí sazba prodeje je nula.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
