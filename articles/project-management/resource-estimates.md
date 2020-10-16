---
title: Odhady zdrojů
description: Toto téma poskytuje informace o tom, jak se počítají odhady zdrojů v aplikaci Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928552"
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
