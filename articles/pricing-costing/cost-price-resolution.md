---
title: Řešení nákladových cen pro odhady a skutečnosti
description: Tento článek poskytuje informace o tom, jak se řeší nákladové ceny pro odhady a skutečné hodnoty.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: af17712f0aef4fe3e6e758edd976cc377e90631d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919960"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Řešení nákladových cen pro odhady a skutečnosti

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

K řešení nákladových cen a nákladového ceníku pro odhady a skutečné hodnoty používá systém informace polích **Datum**, **Měna** a **Smluvní jednotka** souvisejícího projektu. Po vyřešení ceníku nákladů vyřeší aplikace nákladovou sazbu.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Vyřešení nákladových sazeb v řádcích skutečností a odhadů pro čas

Odhad řádků pro čas se vztahuje k podrobnostem řádku nabídky a smlouvy pro přiřazení času a zdrojů v projektu.

Po vyřešení nákladového ceníku systém používá pole **Role**, **Společnost poskytující zdroje** a **Jednotka zdroje** na řádku odhadu pro čas, aby se shodovaly s řádky cen rolí ve vyřešeném ceníku. Tato párování předpokládá, že se používáte předem připravené cenové dimenze pro personální náklady. Pokud jste nakonfigurovali systém, aby pároval pole namísto polí **Role**, **Společnost poskytující zdroje** a **Jednotka zdroje** nebo kromě nich, pak bude použita k načtení odpovídajícího řádku ceny role jiná kombinace. Pokud aplikace najde řádek ceny role, který má nákladovou sazbu pro kombinaci polí **Role**, **Společnost poskytující zdroje** a **Jednotka zdroje**, pak je tato nákladová sazba výchozí. Pokud aplikace nedokáže přesně spárovat hodnoty **Role**, **Společnost prostředků** a **Jednotka prostředků**, načte řádky cen rolí se shodnou hodnotou role, ale bude mít nulové hodnoty pro **Jednotka prostředků** a **Společnost prostředků**. Poté, co se najde odpovídající záznam ceny role se shodnou hodnotou ceny role, bude z tohoto záznamu výchozí cena. 

> [!NOTE]
> Pokud nakonfigurujete jinou prioritu polí **Role**, **Společnost poskytující zdroje** a **Jednotka zdroje** nebo pokud máte jiné dimenze s vyšší prioritou, toto chování se odpovídajícím způsobem změní. Systém načte záznamy cen rolí s hodnotami, které odpovídají každé z hodnot cenové dimenze v pořadí podle priority, s řádky, které mají nulové hodnoty pro ty dimenze, které jsou jako poslední v pořadí priority.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Vyřešení nákladových sazeb v řádcích skutečností a odhadů pro výdaj

Řádky odhadu pro výdaje odkazují na detaily řádku nabídky a smlouvy pro výdaje a řádky odhadu výdaje v projektu.

Po vyřešení nákladového ceníku systém používá kombinaci polí **Kategorie** a **Jednotka** na řádku odhadu pro výdaj, aby se shodovaly s řádky **Ceny kategorií** ve vyřešeném ceníku. Pokud systém najde řádek ceny kategorie, který má nákladovou sazbu pro kombinaci polí **Kategorie** a **Jednotka**, pak je nákladová sazba výchozí. Pokud systém nemůže spárovat hodnoty **Kategorie** a **Jednotka** nebo pokud je schopen najít odpovídající řádek ceny kategorie, ale metoda stanovení cen není **Cena za jednotku**, nákladová sazba je standardně nastavena na nulu (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Řešení nákladových sazeb na řádcích skutečností a odhadů pro materiál

Řádky odhadu pro materiál označují údaje řádku nabídky a řádku smlouvy u materiálů a řádky odhadu materiálu na projektu.

Po vyřešení ceníku nákladů systém použije kombinaci polí **Produkt** a **Jednotka** na řádku odhadu, aby se odhad materiálu shodoval s řádky **Ceník položek** na vyřešeném ceníku. Pokud systém najde cenový řádek produktu, která má nákladovou sazbu pro kombinaci polí **Produkt** a **Jednotka**, je nákladová cena výchozí. Pokud systém nedokáže spárovat hodnoty **Produkt** a **Jednotka** neshodují, výchozí náklad jednotky je nula. K tomuto výchozímu nastavení dojde také v případě, že existuje odpovídající řádek položky ceníku, ale metoda stanovení ceny je založena na standardní ceně nebo aktuální ceně, která není v produktu definována.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
