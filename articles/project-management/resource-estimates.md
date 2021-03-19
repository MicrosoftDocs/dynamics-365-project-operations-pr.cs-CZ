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
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286510"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]