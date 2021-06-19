---
title: Řešení nákladových cen pro odhady projektu a skutečné hodnoty
description: Tento téma poskytuje informace o řešení nákladových cen na základě projektových odhadů a skutečností.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6b42bc97251aec7259d314fe51b3a012edf597aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004388"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Řešení nákladových cen pro odhady projektu a skutečné hodnoty 

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

K řešení nákladových cen a nákladového ceníku pro odhady a skutečné hodnoty používá systém informace polích **Datum**, **Měna** a **Smluvní jednotka** souvisejícího projektu. Po vyřešení ceníku nákladů vyřeší aplikace nákladovou sazbu.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Vyřešení nákladových sazeb v řádcích skutečností a odhadů pro čas

Odhad řádků pro čas se vztahuje k podrobnostem řádku nabídky a smlouvy pro přiřazení času a zdrojů v projektu.

Po vyřešení ceníku nákladů budou pole **Role** a **Jednotka zdroje** na řádku odhadu pro čas porovnána s cenovými řádky rolí v ceníku. Tato shoda předpokládá, že používáte standardní cenové dimenze mzdových nákladů. Pokud jste nakonfigurovali systém, aby pároval pole namísto polí **Role**, **Jednotka zdroje** nebo kromě nich, pak bude použita k načtení odpovídajícího řádku ceny role jiná kombinace. Pokud aplikace najde řádek ceny role, který má nákladovou sazbu pro kombinaci polí **Role**, **Jednotka zdroje**, pak je tato nákladová sazba výchozí. Pokud aplikace neumí spárovat hodnoty polí **Role**, **Jednotka zdroje**, načte řádky cen rolí se shodnou rolí, ale s hodnotami null v poli **Jednotka zdroje**. Poté, co má odpovídající záznam o ceně role, je z tohoto záznamu výchozí cena. 

> [!NOTE]
> Pokud jste konfigurovali jinou prioritu polí **Role** a **Jednotka zdroje** nebo pokud máte jiné dimenze s vyšší prioritou, toto chování se odpovídajícím způsobem změní. Systém načte záznamy cen rolí se shodnými hodnotami každé z hodnot cenových dimenzí v pořadí podle priority s řádky, které mají hodnoty null pro tyto dimenze, uvedenými až nakonec.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Vyřešení nákladových sazeb v řádcích skutečností a odhadů pro výdaj

Řádky odhadu pro výdaje odkazují na detaily řádku nabídky a smlouvy pro výdaje a řádky odhadu výdaje v projektu.

Po vyřešení ceníku nákladů systém použije kombinaci polí **Kategorie** a **Jednotka** na řádku odhadu výdajů ke srovnání s řádky **Cena kategorie** na vyřešeném ceníku. Pokud systém najde řádek ceny kategorie, který má nákladovou sazbu pro kombinaci polí **Kategorie** a **Jednotka**, pak je nákladová sazba výchozí. Pokud systém nedokáže spárovat hodnoty **Kategorie** a **Jednotka** nebo pokud dokáže najít odpovídající cenový řádek kategorie, ale metoda stanovení cen není **Cena za jednotku**, výchozí cena je nula (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Řešení nákladových sazeb na řádcích skutečností a odhadů pro materiál

Řádky odhadu pro materiál označují údaje řádku nabídky a řádku smlouvy u materiálů a řádky odhadu materiálu na projektu.

Po vyřešení ceníku nákladů systém použije kombinaci polí **Produkt** a **Jednotka** na řádku odhadu, aby se odhad materiálu shodoval s řádky **Ceník položek** na vyřešeném ceníku. Pokud systém najde cenový řádek produktu, která má nákladovou sazbu pro kombinaci polí **Produkt** a **Jednotka**, je nákladová cena výchozí. Pokud systém nedokáže spárovat hodnoty **Produkt** a **Jednotka** nebo pokud je schopen najít odpovídající řádek položky ceníku, ale metoda stanovení ceny je založena na standardních nákladech nebo aktuálních nákladech a ani jedna z nich není na produktu definována, výchozí cena jednotky je nula.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
