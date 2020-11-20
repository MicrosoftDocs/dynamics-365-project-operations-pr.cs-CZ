---
title: Odhady zdrojů
description: Toto téma poskytuje informace o tom, jak se počítají odhady zdrojů v aplikaci Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127344"
---
# <a name="resource-estimates"></a>Odhady zdrojů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Odhady zdrojů pocházejí z časově odstupňovaného úsilí, které je definováno ve strukturovaném rozpisu prací spolu s příslušnými cenovými dimenzemi. Výpočet je obvykle prováděn podle vzorce **rychlost / hod pro každou roli x hodin.** Časově odstupňované úsilí pro každý zdroj je uloženo v záznamu přiřazení zdroje. Cena je uložena v předem definovaném ceníku. Převod jednotek se použije na základě příslušného ceníku.

![Odhady zdrojů](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Výchozí nákladová cena a měna nákladů

Výchozí hodnoty nákladových cen jsou převzaty z organizační jednotky.

## <a name="default-bill-rate-and-sales-currency"></a>Výchozí fakturační sazba a měna prodeje

Prodejní ceny se aplikují jednou za každý obchod. Hierarchie výchozích prodejních ceníků je následující:

1. Organizace
2. Zákazník
3. Nabídka / smlouva
