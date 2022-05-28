---
title: Nastavení nákladových a prodejních sazeb pro výdaje
description: Toto téma poskytuje informace o tom, jak nastavit nákladové a prodejní sazby u kategorií transakcí a výdajů.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: de7f95f9dcb1dff866d165dba9aaaedb480c1ad5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598434"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Nastavení nákladových a prodejních sazeb pro výdaje

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Pro kategorie transakcí můžete nastavit náklady a prodejní ceny v Dynamics 365 Project Operations. Protože nákladové a prodejní ceny jsou určeny pro výdaje, musí být každá kategorie transakcí, která je zahrnuje, také nastavena jako kategorie výdajů. Toto nastavení zajišťuje přesnost následných funkcí. Nákladové a prodejní ceny pro kategorie transakcí lze uvést pouze v jedné měně, kterou musí být měna v záhlaví ceníku.

Chcete-li nastavit nákladové a prodejní sazby pro kategorie transakcí, proveďte následující kroky. 

1. Přejděte do nabídky **Prodeje** > **Zákazníci** > **Ceníky**.
2. Chcete-li vytvořit nový ceník, vyberte možnost **Nový**. 
3. V části **Ceny kategorií** v nabídce podmřížky vyberte možnost **+ Nová cena kategorie**. 
4. Na stránce **Vytvořit** zadejte kategorii transakce a jednotku, pro kterou vytváříte novou cenu.

V následující tabulce je uveden seznam polí na kartě **Všeobecné** a stránce **Vytvořit** řádku ceny kategorie, na které byste měli pamatovat při vytváření cen kategorií v prodejním nebo nákladovém ceníku.

| Pole | Místo | Popis | Dopad na následné složky |
| --- | --- | --- | --- |
| Kategorie transakce | Karta **Všeobecné** a stránky **Vytvořit** | Vyberte kategorii transakcí, pro kterou vytváříte prodejní nebo nákladovou cenu. | Kategorie transakcí u příchozího odhadu nebo skutečné hodnoty pro výdaje bude porovnána s tímto řádkem, aby byla určena výchozí nákladová nebo prodejní sazba kategorie transakce. |
| Rozpis jednotky | Karta **Všeobecné** a stránky **Vytvořit** | Výchozí hodnoty rozpisu jednotky pocházejí z rozpisu jednotky kategorie transakcí. | Toto pole nemá žádný následný dopad. |
| Jednotka | Karta **Všeobecné** a stránky **Vytvořit** | Vyberte jednotku, pro kterou nastavujete sazby. | Jednotka u příchozího odhadu nebo skutečné hodnoty je porovnána s jednotkou na tomto řádku, aby byla nastavena výchozí sazba pro odhad nebo skutečnou hodnotu výdajů. |
| Způsob ocenění | Karta **Všeobecné** a stránky **Vytvořit** | Možné hodnoty pole **Způsob ocenění** jsou **Cena za jednotku**, **Podle nákladů** a **Přirážka k nákladům**. | Během nastavení ceny výběr způsobu **Cena za jednotku** uzamkne pole **Procento** na řádku ceny kategorie. Když je vybrán způsob **Podle nákladů**, uzamknou se pole **Cena** a **Procento** v prodejním ceníku. Výběr způsobu **Přirážka k nákladům** zamkne pole **Cena** v prodejním ceníku. Na řádku příchozí skutečné hodnoty pro výdaje vedou způsoby ocenění **Podle nákladů** nebo **Přirážka k nákladům** k tomu, že odpovídajícímu nevyfakturovanému řádku prodeje bude přiřazena cena, která se rovná ceně skutečného nákladu nebo se vypočítá jako přirážka k ceně. |
| Cena | Karta **Všeobecné** a stránky **Vytvořit** | Nastavte jednotkovou sazbu pro kategorii transakce a kombinaci jednotek. Například sazba za ujetou vzdálenost je 10 USD na míli a 8 USD na kilometr. | Sazba za ujetou vzdálenost bude sazba, která je výchozí pro jednotkovou cenu nebo náklad řádku příchozího odhadu nebo skutečnosti pro třídu výdajových transakcí.|
| Procenta | Karta **Všeobecné** a stránky **Vytvořit** | Nastavte procento přirážky k nákladům pro kategorii transakce a kombinaci jednotek. Například sazba za prodej letenek by měla být zvýšena o 10 procent nad náklady vzniklých výdajů za letenky. | Toto procento přirážky k nákladům je použitelné pouze v prodejním ceníku, když je vybraná metoda výpočtu ceny **Přirážka k nákladům**. |
| Měna | Karta **Všeobecné** a stránky **Vytvořit** | Ve výchozím nastavení tato hodnota pochází z měny v záhlaví ceníku. U cen kategorie transakcí nelze měnu přepsat. | Tato měna je výchozí pro jednotkovou cenu příchozího skutečného řádku pro třídu výdajových transakcí pro náklady a prodej. |

## <a name="pricing-methods-for-expenses"></a>Metody oceňování výdajů

Když nastavíte ceny kategorie, které jsou relevantní pouze v kontextu ocenění výdajů, můžete použít jeden z následujících tří způsobů ocenění:

- **Cena za jednotku**
- **Podle nákladů**
- **Přirážka k nákladům**

### <a name="price-per-unit"></a>Cena za jednotku
Když je tento způsob ocenění vybrán v řádku ceny kategorie, který je propojen s prodejním ceníkem, výchozí cena je pro kombinaci kategorie a jednotky v odhadu i ve skutečné hodnotě. Odhad odkazuje na řádky odhadu projektu pro výdaje, detail řádku nabídky a detail řádku smlouvy pro výdaje.

### <a name="at-cost"></a>Podle nákladů
Když je tento způsob ocenění vybrán v řádku ceny kategorie, který je propojen s prodejním ceníkem, výchozí cena je pro kombinaci kategorie a jednotky pouze pro skutečný výdaj. Například nevyfakturované skutečné prodeje pro třídu výdajových transakcí. Jednotková cena je nastavena u nevyfakturovaných skutečných prodejů z jednotkové ceny u skutečného nákladu pro tento výdaj. Výchozí cena založená na nákladech se nestanoví u projektových odhadů výdajů ani u podrobností řádku nabídky a řádku smlouvy pro výdaje.

### <a name="markup-over-cost"></a>Přirážka k nákladům
Když je tento způsob ocenění vybrán v řádku ceny kategorie, který je propojen s prodejním ceníkem, výchozí cena je pro kombinaci kategorie a jednotky pouze pro skutečný výdaj. Například nevyfakturované skutečné prodeje pro třídu výdajových transakcí. Tato jednotková cena je nastavena na nevyfakturovaný prodej skutečný na vypočítanou hodnotu z jednotkové ceny na skutečný náklad pro daný výdaj po uplatnění definovaného procenta přirážky. Výchozí cena založená na nákladech se nestanoví u projektových odhadů výdajů ani u podrobností řádku nabídky a řádku smlouvy pro výdaje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
