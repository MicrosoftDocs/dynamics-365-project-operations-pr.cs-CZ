---
title: Kontrola nedokončené fakturace u projektů a projektových smluv
description: Toto téma obsahuje informace o tom, jak kontrolovat nedokončené časové, výdajové a produktové záznamy a jak je označit jako připravené k fakturaci.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: bdeeb100614cda78d0ba536310bb6b411c863b71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282775"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Kontrola nedokončené fakturace u projektů a projektových smluv

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pokud je transakce připravena k vytvoření a zpracování faktury, měla by být označena jako **Připraveno k fakturaci**. Toto téma popisuje typy transakcí, které lze vytvořit.

## <a name="review-the-time-and-material-billing-backlog"></a>Kontrola nedokončené fakturace času a materiálu

PSA při odeslání a schválení časových nebo výdajových záznamů pro projekt vytvoří skutečnou hodnotu projektu. Pokud je kombinace projektu a třídy transakce namapována na řádek smlouvy pro projekt s časem a materiálem, jsou při schválení záznamu vytvořeny dvě skutečné hodnoty:

- Skutečné náklady 
- Skutečný nefakturovaný prodej

Skutečné hodnoty nefakturovaného prodeje představují nedokončenou fakturaci a jeho stav fakturace musí být nastaven na **Připraveno k fakturaci**. Při vytvoření projektové faktury jsou skutečné hodnoty nefakturovaného prodeje, které jsou označeny jako **Připraveno k fakturaci**, zkopírovány jako podrobnosti řádku faktury.

Chcete-li zkontrolovat nedokončenou fakturaci času a materiálu, přejděte na **Prodej** \> **Fakturace** \> **Nedokončená fakturace času a materiálu**. Vyberte všechny skutečné hodnoty nefakturovaného prodeje, které jsou připraveny k fakturaci a pak vyberte **Připraveno k fakturaci**. Stav fakturace těchto skutečných hodnot je změněn na **Připraveno k fakturaci**.

![Nedokončená fakturace času a materiálu](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Kontrola nedokončené fakturace produktů

Obsahuje-li projektová smlouva v PSA řádky smlouvy založené na produktu, budou tyto řádky zohledněny pro fakturaci při každém vytvoření faktury pro projektovou smlouvu. Všechny produkty, které obsahují řádky smlouvy označené jako **Připraveno k fakturaci**, jsou zkopírovány do projektové faktury jako řádky projektové faktury.

Chcete-li zkontrolovat nedokončenou fakturaci produktů, přejděte do **Prodej** \> **Fakturace** \> **Nedokončená fakturace produktů**. Vyberte všechny řádky smlouvy založené na produktu, které jsou připraveny k fakturaci a pak vyberte **Připraveno k fakturaci**. Stav fakturace těchto řádků je změněn na **Připraveno k fakturaci**.

![Nedokončená fakturace produktů](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Kontrola fakturačních milníků u smluv s pevnou cenou

Každý řádek projektové smlouvy, který obsahuje fakturační metodu s pevnou cenou, musí definovat milníky smlouvy. Tyto milníky smlouvy lze fakturovat pouze v případě, že jsou označeny jako **Připraveno k fakturaci**. 

Chcete-li zkontrolovat fakturační milníky, přejděte na **Prodej** \> **Fakturace** \> **Milníky s pevnou cenou**. Vyberte milníky, které jsou připraveny k fakturaci a pak vyberte **Připraveno k fakturaci**. Stav fakturace těchto milníků je změněn na **Připraveno k fakturaci**.

![Milníky s pevnou cenou](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]