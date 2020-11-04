---
title: Vyřešení prodejních cen pro odhady a skutečnosti
description: Tento téma poskytuje informace o tom, jak vyřešit prodejní ceny pro odhady a skutečnosti.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c8972bd7710735e9acdbf951079f2da24a00bd7f
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087854"
---
# <a name="resolving-sales-prices-for-estimates-and-actuals"></a>Vyřešení prodejních cen pro odhady a skutečnosti

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Když jsou prodejní ceny u odhadů a skutečností vyřešeny v Dynamics 365 Project Operations, systém k vyřešení prodejního ceníku nejprve použije datum a měnu související projektové nabídky nebo smlouvy. Po vyřešení prodejního ceníku systém vyřeší prodejní nebo fakturační sazbu.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Vyřešení prodejních sazeb v řádcích skutečností a odhadů pro čas

V Project Operations se řádky odhadů pro čas používají k označení řádků nabídek a podrobností řádků smluv pro čas a přiřazení prostředků v projektu.

Po vyřešení prodejního ceníku systém provede následující kroky a nastaví výchozí fakturační sazbu.

1. Systém používá pole **Role** a **Jednotka zdroje** na řádku odhadu pro čas, aby řádek spároval s řádky cen rolí ve vyřešeném ceníku. Tato párování předpokládá, že se používají předem připravené cenové dimenze pro fakturační sazby. Pokud jste konfigurovali ceny na základě jakýchkoli jiných polí namísto polí **Role** a **Jednotka zdroje** nebo kromě nich, pak to je kombinace, která bude použita k načtení odpovídajícího řádku ceny role.
2. Pokud systém najde řádek ceny role, který má fakturační sazbu pro kombinaci polí **Role** a **Jednotka zdroje** , pak je tato fakturační sazba výchozí.
3. Pokud systém neumí spárovat hodnoty polí **Role** a **Jednotka zdroje** , načte řádky cen rolí se shodnou rolí, ale s hodnotami null v poli **Jednotka zdroje**. Poté, co systém najde odpovídající záznam ceny role, nastaví výchozí fakturační sazbu podle tohoto záznamu. Tato shoda předpokládá předem připravenou konfiguraci pro relativní prioritu **Role** vs. **Jednotka role** jako dimenze prodejních cen.

> [!NOTE]
> Pokud jste konfigurovali jinou prioritu polí **Role** a **Jednotka zdroje** nebo pokud máte jiné dimenze s vyšší prioritou, toto chování se odpovídajícím způsobem změní. Systém načte záznamy cen rolí se shodnými hodnotami každé z hodnot cenových dimenzí v pořadí podle priority s řádky, které mají hodnoty null pro tyto dimenze, uvedenými až nakonec.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Vyřešení prodejních sazeb v řádcích skutečností a odhadů pro výdaje

V Project Operations se řádky odhadů pro výdaje používají k označení řádků nabídek a podrobností řádků smluv pro výdaje a řádků odhadů výdajů v projektu.

Po vyřešení prodejního ceníku systém provede následující kroky a nastaví výchozí prodejní cenu jednotky.

1. Systém používá kombinaci polí **Kategorie** a **Jednotka** na řádku odhadu pro výdaje, aby řádek spároval s řádky cen kategorií ve vyřešeném ceníku.
2. Pokud systém najde řádek ceny kategorie, který má prodejní sazbu pro kombinaci polí **Kategorie** a **Jednotka** , pak je tato prodejní sazba výchozí.
3. Pokud systém najde odpovídající řádek ceny kategorie, lze metodu stanovení cen použít ke stanovení výchozí prodejní ceny. Následující tabulka ukazuje výchozí chování ceny výdajů v Project Operations.

    | Kontext | Způsob ocenění | Výchozí cena |
    | --- | --- | --- |
    | Odhad | Cena za jednotku | Na základě řádku ceny kategorie |
    | &nbsp; | Podle nákladů | 0.00 |
    | &nbsp; | Přirážka k nákladům | 0.00 |
    | Skutečnost | Cena za jednotku | Na základě řádku ceny kategorie |
    | &nbsp; | Podle nákladů | Na základě skutečných souvisejících nákladů |
    | &nbsp; | Přirážka k nákladům | Aplikování přirážky definované v řádku ceny kategorie na sazbu jednotkové ceny související skutečné ceny |

4. Pokud systém není schopen spárovat hodnoty polí **Kategorie** a **Jednotka** , je výchozí hodnota prodejní sazby nula (0).
