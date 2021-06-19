---
title: Obecné plnění požadavků na zdroje
description: Toto téma obsahuje informace o rezervaci pojmenovaných zdrojů pro požadavek na obecný zdroj.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e36875a0d5dcb24d9669e2ea989c6fc7db7bcd7c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005828"
---
# <a name="generic-resource-requirement-fulfillment"></a>Obecné plnění požadavků na zdroje

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Pro nahrazení obecného zdroje, který obsahuje požadavek na zdroj, můžete rezervovat pojmenovaný zdroj.

1. Na stránce **Projekty** vyberte kartu **Tým**.
2. Vyberte ze seznamu obecný zdroj, který obsahuje požadavek na zdroj, a pak zvolte **Rezervovat**. Nebo otevřete požadavek na zdroj a pak zvolte **Rezervovat**.
3. Na stránce **Pomocník plánování** vyberte pojmenovaný zdroj, který chcete rezervovat pro projektový tým, a zvolte **Rezervovat**.

Pokud je rezervace dokončena a vyplněna pojmenovaným zdrojem, je obecný zdroj nahrazen pojmenovaným zdrojem.

Přiřazení v plánu jsou aktualizována také pomocí pojmenovaného zdroje.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Vyplnění obecného zdroje pomocí několika pojmenovaných zdrojů
Vyplnění požadavku na obecný zdroj pomocí několika pojmenovaných zdrojů je podobné přiřazení jednoho pojmenovaného zdroje. Existuje například úkol s dobou trvání pět dní a úsilím 120 hodin. Tento úkol nemůže být dokončen jedním zdrojem, který pracuje typicky osm hodin denně, pět dní v týdnu. 

Požadavek je na 120 hodin robotického inženýrství po dobu pěti dní, což je 24 hodin denně.

Toto je příklad, kdy je k naplnění obecného požadavku na zdroj potřeba více pojmenovaných zdrojů. Pro splnění požadavku budete potřebovat rezervovat více zdrojů.

Hlavní rozdíl v tomto scénáři spočívá v tom, že obecný zdroj zůstává v týmu přiřazeném k úkolu, a že zarezervovaní pojmenovaní členové týmu zdrojů nejsou přiřazeni jako součást pozice. Projektový manažer může přiřadit práci odpovídající pojmenovaným zdrojům. Zobrazení **Vyrovnání** může projektovému manažerovi pomoci při rozdělování rezervací mezi více zdrojů pro přiřazení úkolů. Není to prováděno automaticky, protože v libovolném scénáři, který je složitější než výše uvedený jednoduchý příklad, kdy například máte balík úkolů, které tvoří požadavek, musí být záměr, jak chce projektový manažer přiřazení provést, vypočten systémem. Protože systém nedokáže pochopit záměr, je pravděpodobné, že předpoklady budou jiné, než je zamýšleno, a dojde k nesprávnému nebo nepředvídatelnému výsledku. Předvídatelným výsledkem je, že obecný zdroj zůstává přiřazen, dokud projektový manažer záměrně nevytvoří přiřazení pomocí zobrazení **Vyrovnání**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]