---
title: Kopírovat ceníky
description: Tento téma poskytuje informace o tom, jak kopírovat ceníky ve službě Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e49a95a04e9506e983d920c49d4c504d9f944c88
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275710"
---
# <a name="copy-price-lists"></a>Kopírovat ceníky

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

V Dynamics 365 Project Operations můžete vytvářet kopie ceníků. Můžete například vytvořit ceníky pro nadcházející rok pomocí ceníku z aktuálního roku.  Nebo můžete zkopírovat ceník pro fakturační sazby a prodejní ceny z ceníků pro náklady. 

Chcete-li vytvořit kopii ceníku, proveďte následující kroky.

1. Otevřete ceník, ze kterého chcete vytvořit kopii, a vyberte **Kopírovat**.
2. Zadejte všechny potřebné informace ke zkopírování ceníku. V následující tabulce jsou uvedeny věci, které je třeba mít na paměti při zadávání informací.

| Pole | Popis | Dopad na následné složky |
| --- | --- | --- |
| Jméno | Název zdrojového ceníku s připojeným slovem **-kopie**. | Ceník obsahuje tuto hodnotu na všech stránkách seznamů a v rozevíracích seznamech. |
| Kontext | Zadejte požadovaný kontext pro cílový ceník. | Ceník, který má kontext nastavený na **Náklady**, se používá k vyhledání ceny pro odhady nákladů a skutečné náklady. Ceník, který má kontext nastavený na **Prodej**, se používá k vyhledání ceny pro odhady prodejů a skutečné prodeje. Pouze ceníky, jejichž kontext je nastaven na **Prodej**, lze připojit k projektovým ceníkům pro zákazníka, nabídky a smlouvy. |
| Počáteční datum | Počáteční datum období, ve kterém je ceník účinný. | Spolu s polem **Datum ukončení** se toto pole používá k určení, který ceník je použitelný pro určitý odhad nebo skutečný řádek. |
| Koncové datum | Koncové datum období, ve kterém je ceník účinný. | Spolu s polem **Počáteční datum** se toto pole používá k určení, který ceník je použitelný pro určitý odhad nebo skutečný řádek. |
| Měna | Měna zdrojového ceníku. Tu lze změnit. | Když se změní, všechny výsledné cenové řádky pro práci, výdaje a položky katalogu produktů se během kopírování převedou na měnu cílového ceníku. |
| Časová jednotka | Měna zdrojového ceníku. Tu lze změnit. | Když se změní, všechny výsledné cenové řádky pro práci se během kopírování převedou na jednotku cílového ceníku. Použije se převod z nastavení jednotky pro časovou jednotku zdrojového ceníku a časovou jednotku cílového ceníku. |
| Popis | Popis zdrojového ceníku s připojeným slovem **-kopie**. Toto je textové pole a umožňuje vytvořit víceřádkový popis ceníku. | Toto pole je zobrazeno v **Přidružených** zobrazeních ceníků v různých entitách, které mají související ceníky. |

3. Uložit ceník. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Úprava ceníku uplatněním přirážky ke všem cenám

1. Na kartách **Role**, **Kategorie** a **Položka ceníku** můžete vybrat **Aktualizovat ceny**, čímž použijete přirážku na všechny ceny v podmřížce. 
2. Na dialogové stránce, která se otevře, zadejte přirážku. Můžete také zadat záporné procento přirážky a snížit ceny o určité procento. 
3. Vyberte **OK** na stránce dialogového okna a poté ověřte, že ceny v podmřížce odpovídají provedeným změnám.


[!INCLUDE[footer-include](../includes/footer-banner.md)]