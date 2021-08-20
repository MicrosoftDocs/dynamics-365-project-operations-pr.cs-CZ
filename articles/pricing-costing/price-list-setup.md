---
title: Nastavení ceníků
description: Toto téma obsahuje informace o způsobu nastavení nákladových a prodejních ceníků.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 227e9a6f0ce6fd3fa1c2b0bd9afa014a3ec4f9758ead0dfb408156535692575c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009478"
---
# <a name="set-up-price-lists"></a>Nastavení ceníků

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Ceníky v Dynamics 365 Project Operations představují katalog sazeb. Sazby vyjadřují nákladové, prodejní a fakturační sazby. V závislosti na tom, zda ceník vyjadřuje nákladové sazby nebo prodejní a fakturační sazby, má kontext ceníku hodnotu **Prodej** nebo **Náklady**.

Následující rozšíření jsou specifická pro Project Operations a jsou aplikována na ceníky z Dynamics 365 Sales.

- **Kontext** : Toto pole má podporované hodnoty **Náklady** a **Odbyt**. Hodnota **Nákup** není podporována. Nastavte kontext na **Náklady**, chcete-li vytvořit nákladový ceník. U prodejního ceníku nastavte kontext na **Prodej**. Nákladové ceníky stanoví cenu pro typ nákladů v záznamech odhadů a skutečností. Prodejní ceníky stanoví cenu v záznamech odhadů a skutečností u nevyfakturovaných a fakturovaných typů prodeje.
- **Časová jednotka** : Toto je výchozí jednotka času, pro kterou je cena nastavena v související tabulce **Cena role** pro tento ceník.
- **Entita Ceník** : Toto skryté pole pochází z Project Operations a slouží k rozlišení ceníků, které jsou specifické pro konkrétní nabídku nebo smlouvu, od standardních a globálně použitelných ceníků.

## <a name="price-list-header"></a>Záhlaví ceníku

Následující tabulka obsahuje pole na kartě **Všeobecné** ceníku, která jsou jedinečná pro Project Operations nebo mají významné změny v chování oproti ceníkům aplikace Sales.

| Pole | Místo | Popis | Dopad na následné složky |
| --- | --- | --- | --- |
| Jméno | Karta **Všeobecné** a formuláře **Vytvořit** | Identita ceníku. | Ceník je zobrazen s touto hodnotou na všech stránkách seznamů a v rozevíracích seznamech.|
| Kontext | Karta **Všeobecné** a formuláře **Vytvořit** | Toto pole lze nastavit na **Náklady** nebo **Prodej**. | Ceník nastavený na **Náklady** se používá k vyhledání ceny pro odhady nákladů a skutečné náklady. Ceník nastavený na **Prodej** se používá k vyhledání ceny pro odhady prodejů a skutečné prodeje. Pouze ceníky, jejichž kontext je nastaven na **Prodej**, lze připojit k projektovým ceníkům pro zákazníky, projektové nabídky a projektové smlouvy. |
| Počáteční datum | Karta **Všeobecné** a formuláře **Vytvořit** | Počáteční datum období, ve kterém je ceník účinný. | Spolu s polem **Datum ukončení** se toto pole používá k určení, který ceník je použitelný pro určitý odhad nebo skutečný řádek. |
| Koncové datum | Karta **Všeobecné** a formuláře **Vytvořit** | Koncové datum období, ve kterém je ceník účinný. | Spolu s polem **Počáteční datum** se toto pole používá k určení, který ceník je použitelný pro určitý odhad nebo skutečný řádek. |
| Měna | Karta **Všeobecné** a formuláře **Vytvořit** | Toto pole se používá jako výchozí měna pro každý řádek role, kategorie nebo položky ceníku vztahující se k tomuto ceníku. | U ceníků s kontextem **Prodej** nelze řádky role, kategorie nebo položky ceníku vytvořit v jiné měně než v této. U ceníků s kontextem **Náklady** můžete vytvořit řádek ceny role v jakékoli měně. Zde definovaná měna se použije jako výchozí. Uživatelské nastavení, které souvisí s cenami rolí, může přepsat tuto hodnotu a povolit nastavení sazby nákladů práce v jakékoli měně. Sazby nákladů kategorie a náklady položky ceníku lze nastavit pouze v měně definované zde. |
| Časová jednotka | Karta **Všeobecné** a formuláře **Vytvořit** | Toto pole se používá jako výchozí časová jednotka pro každý řádek role vztahující se k tomuto ceníku. | Tato hodnota pole se používá pouze při nastavení ceny související role. U ceníků s kontextem **Náklady** a **Prodej** můžete vytvořit řádek ceny role v jakékoli časové jednotce. Zde definovaná časová jednotka se použije jako výchozí. Uživatelské nastavení souvisejících cen rolí může přepsat tuto hodnotu a povolit nastavení sazby nákladů práce a fakturace v jakékoli časové jednotce. |
| Popis | Karta **Všeobecné** a formuláře **Vytvořit** | Toto textové pole umožňuje vytvořit víceřádkový popis ceníku. | Toto pole je zobrazeno v **Přidružených** zobrazeních ceníků v různých entitách, které mají související ceníky. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]