---
title: Určení prodejních cen pro odhady projektu a skutečné hodnoty
description: Tento článek poskytuje informace o tom, jak se určují prodejní ceny pro odhady a skutečné hodnoty projektu.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6504302578d1eb3d00c717ea93cd4c4212acb4e7
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410110"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Určení prodejních cen pro odhady projektu a skutečné hodnoty

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Když jsou určovány prodejní ceny na základě odhadů a skutečností v Microsoft Dynamics 365 Project Operations, systém nejprve použije datum a měnu v příchozím odhadu nebo skutečném kontextu k určení ceníku prodejní ceny. Ve skutečném kontextu konkrétně systém používá pole **Datum transakce** pro určení, který ceník je použitelný. Po určení prodejního ceníku systém určí prodejní nebo fakturační sazbu.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Určení prodejních sazeb v řádcích skutečností a odhadů pro čas

Kontext odhadu pro **Čas** odkazuje na:

- Údaje řádku nabídky pro **Čas**.
- Údaje řádku smlouvy pro **Čas**.
- Přiřazení zdroje k projektu.

Skutečný kontext pro **Čas** odkazuje na:

- Řádky deníku záznamů a oprav pro **Čas**.
- Řádky deníku, které se vytvoří při odeslání časového záznamu.
- Údaje řádku faktury pro **Čas**. 

Po určení prodejního ceníku systém provede následující kroky a zadá výchozí fakturační sazbu.

1. Systém spáruje pole **Role** a **Jednotka zdroje** v kontextu odhadu nebo skutečném odhadu pro **Čas** s řádky cen rolí v ceníku. Tato párování předpokládá, že se používáte předem připravené cenové dimenze pro fakturační sazby. Pokud jste konfigurovali ceny na základě jakýchkoli jiných polí namísto polí **Role** a **Jednotka zdroje** nebo kromě nich, pak to je kombinace polí, která bude použita k načtení odpovídajícího řádku ceny role.
1. Pokud systém najde řádek ceny role, který má fakturační sazbu pro kombinaci polí **Role** a **Jednotka zdroje**, pak je tato fakturační sazba používána jako výchozí.
1. Pokud systém nedokáže spárovat hodnoty polí **Role**, **Jednotka zdroje**, načte řádky cen rolí se shodným polem **Role**, ale s hodnotami null v poli **Jednotka zdroje**. Poté, co systém najde odpovídající záznam ceny role, nastaví fakturační sazba podle tohoto záznamu bude použita jako výchozí. Tato shoda předpokládá předem připravenou konfiguraci pro relativní prioritu **Role** vs. **Jednotka role** jako dimenze prodejních cen.

> [!NOTE]
> Pokud jste konfigurovali jinou prioritu polí **Role** a **Jednotka zdroje** nebo pokud máte jiné dimenze s vyšší prioritou, předchozí chování se odpovídajícím způsobem změní. Systém načte záznamy cen rolí, které mají hodnoty, které odpovídají každé hodnotě dimenze cen v pořadí podle priority. Řádky, které mají pro tyto dimenze hodnoty null, jsou na posledním místě.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Určení prodejních sazeb v řádcích skutečností a odhadů pro výdaje

Kontext odhadu pro **Výdaj** odkazuje na:

- Údaje řádku nabídky pro **Výdaj**.
- Údaje řádku smlouvy pro **Výdaj**.
- Odhady řádku Výdaj na projektu.

Skutečný kontext pro **Výdaj** odkazuje na:

- Řádky deníku záznamů a oprav pro **Výdaj**.
- Řádky deníku, které se vytvoří při odeslání záznamu výdaje.
- Údaje řádku faktury pro **Výdaj**. 

Po určení prodejního ceníku systém provede následující kroky a nastaví výchozí prodejní cenu jednotky.

1. Systém páruje kombinaci polí **Kategorie** a **Jednotka** na řádku odhadu pro **Výdaj**, aby řádek spároval s řádky cen kategorií v ceníku.
1. Pokud systém najde řádek ceny kategorie, který má prodejní sazbu pro kombinaci polí **Kategorie** a **Jednotka**, pak je tato prodejní sazba používána jako výchozí.
1. Pokud systém najde odpovídající řádek ceny kategorie, lze metodu stanovení cen použít k zadání výchozí prodejní ceny. Následující tabulka ukazuje výchozí chování ceny výdajů v Project Operations.

    | Kontext | Způsob ocenění | Výchozí cena |
    | --- | --- | --- |
    | Odhad | Cena za jednotku | Na základě řádku ceny kategorie. |
    |        | Podle nákladů | 0.00 |
    |        | Přirážka k nákladům | 0.00 |
    | Skutečnost | Cena za jednotku | Na základě řádku ceny kategorie. |
    |        | Podle nákladů | Na základě skutečných souvisejících nákladů. |
    |        | Přirážka k nákladům | Je aplikována přirážka definovaná v řádku ceny kategorie na sazbu jednotkové ceny související skutečné ceny. |

1. Pokud systém není schopen spárovat hodnoty polí **Kategorie** a **Jednotka**, je výchozí prodejní sazba nastavena na **0** (nula).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Určení prodejních sazeb na řádcích skutečností a odhadů pro materiál

Kontext odhadu pro **Materiál** odkazuje na:

- Údaje řádku nabídky pro **Materiál**.
- Údaje řádku smlouvy pro **Materiál**.
- Odhady řádku Materiál na projektu.

Skutečný kontext pro **Materiál** odkazuje na:

- Řádky deníku záznamů a oprav pro **Materiál**.
- Řádky deníku, které se vytvoří při odeslání deníku využití materiálu.
- Údaje řádku faktury pro **Materiál**. 

Po určení prodejního ceníku systém provede následující kroky a nastaví výchozí prodejní cenu jednotky.

1. Systém páruje kombinaci polí **Produkt** a **Jednotka** na řádku odhadu **Materiál** s řádky položky ceníku v ceníku.
1. Pokud systém najde řádek položky ceníku, který má sazbu prodeje pro kombinaci polí **Produkt** a **Jednotka** a metoda ocenění je **Částka měny**, použije se prodejní cena uvedená v řádku ceníku. 
1. Pokud se hodnoty pole **Produkt** a **Jednotka** neshodují nebo pokud je metoda stanovení ceny jiná než **Částka měny**, prodejní sazba je nastavena na **0** (nula) ve výchozím nastavení. K tomuto chování dochází, protože Project Operations podporuje pouze metodu ceny **Částka měny** pro materiály, které se používají na projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
