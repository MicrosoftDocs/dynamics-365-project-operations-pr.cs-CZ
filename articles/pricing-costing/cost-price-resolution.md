---
title: Řešení nákladových cen pro odhady a skutečnosti
description: Tento téma poskytuje informace o tom, jak se řeší nákladové ceny pro odhady a skutečné hodnoty.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c2fe2a15d38ab5a1f2a93c6db4ed6b7eb9bbd33d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275665"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Řešení nákladových cen pro odhady a skutečnosti

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

K řešení nákladových cen a nákladového ceníku pro odhady a skutečné hodnoty používá systém informace polích **Datum**, **Měna** a **Smluvní jednotka** souvisejícího projektu. Po vyřešení ceníku nákladů vyřeší aplikace nákladovou sazbu.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Vyřešení nákladových sazeb v řádcích skutečností a odhadů pro čas

Odhad řádků pro čas se vztahuje k podrobnostem řádku nabídky a smlouvy pro přiřazení času a zdrojů v projektu.

Po vyřešení nákladového ceníku systém používá pole **Role**, **Společnost poskytující zdroje** a **Jednotka zdroje** na řádku odhadu pro čas, aby se shodovaly s řádky cen rolí ve vyřešeném ceníku. Tato párování předpokládá, že se používáte předem připravené cenové dimenze pro personální náklady. Pokud jste nakonfigurovali systém, aby pároval pole namísto polí **Role**, **Společnost poskytující zdroje** a **Jednotka zdroje** nebo kromě nich, pak bude použita k načtení odpovídajícího řádku ceny role jiná kombinace. Pokud aplikace najde řádek ceny role, který má nákladovou sazbu pro kombinaci polí **Role**, **Společnost poskytující zdroje** a **Jednotka zdroje**, pak je tato nákladová sazba výchozí. Pokud aplikace neumí spárovat hodnoty polí **Role**, **Společnost poskytující zdroje** a **Jednotka zdroje**, načte řádky cen rolí se shodnou rolí, ale s hodnotami null v poli **Jednotka zdroje**. Poté, co má odpovídající záznam o ceně role, je z tohoto záznamu výchozí cena. 

> [!NOTE]
> Pokud nakonfigurujete jinou prioritu polí **Role**, **Společnost poskytující zdroje** a **Jednotka zdroje** nebo pokud máte jiné dimenze s vyšší prioritou, toto chování se odpovídajícím způsobem změní. Systém načte záznamy cen rolí se shodnými hodnotami každé z hodnot cenových dimenzí v pořadí podle priority s řádky, které mají hodnoty null pro tyto dimenze, uvedenými až nakonec.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Vyřešení nákladových sazeb v řádcích skutečností a odhadů pro výdaj

Řádky odhadu pro výdaje odkazují na detaily řádku nabídky a smlouvy pro výdaje a řádky odhadu výdaje v projektu.

Po vyřešení nákladového ceníku systém používá kombinaci polí **Kategorie** a **Jednotka** na řádku odhadu pro výdaj, aby se shodovaly s řádky **Ceny kategorií** ve vyřešeném ceníku. Pokud systém najde řádek ceny kategorie, který má nákladovou sazbu pro kombinaci polí **Kategorie** a **Jednotka**, pak je nákladová sazba výchozí. Pokud systém nemůže spárovat hodnoty **Kategorie** a **Jednotka** nebo pokud je schopen najít odpovídající řádek ceny kategorie, ale metoda stanovení cen není **Cena za jednotku**, nákladová sazba je standardně nastavena na nulu (0).


[!INCLUDE[footer-include](../includes/footer-banner.md)]