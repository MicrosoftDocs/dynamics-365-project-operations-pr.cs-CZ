---
title: Nastavení nákladových a prodejních sazeb pro materiály
description: Tento článek poskytuje informace o tom, jak nastavit nákladové a prodejní sazby pro materiály používané v projektech.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a7d84c2dcaa228e06add2f3cb06a530b29e0e35
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911772"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>Nastavení nákladových a prodejních sazeb pro materiály

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Náklady a prodejní ceny produktů se nastavují v aplikaci Dynamics 365 Project Operations. Náklady a prodejní ceny produktů mohou být uvedeny pouze v jedné měně, kterou musí být měna v záhlaví ceníku.

Chcete-li nastavit náklady a prodejní ceny produktů, proveďte následující kroky. 

1. Přejděte do nabídky **Prodeje** > **Zákazníci** > **Ceníky** a výběrem položky **Nový** vytvořte nový ceník. 
2. V části **Položky ceníku** vyberte v nabídce podmřížky možnost **Nová položka ceníku**. 
3. Na stránce **Rychlé vytvoření** zadejte produkt a jednotku, pro kterou vytváříte novou cenu.

Další informace o tom, jak definovat ceny pro položky katalogu, viz [Definujte cenu produktu pomocí ceníků a položek ceníku](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products) a [Desetinná přesnost v měně a ceně](/dynamics365/sales/decimal-precision-currency-pricing).
> [!NOTE]
> Dynamics 365 Project Operations nepodporuje všechny metody stanovení cen pro produkty jako Dynamics 365 Sales. Jediný způsob stanovení ceny podporovaný pro produkty, které mají být použity v projektech, je *Částka měny*.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
