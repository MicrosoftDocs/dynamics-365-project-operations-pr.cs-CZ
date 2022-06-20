---
title: Rezervace pojmenovaných zdrojů z požadavků na zdroje
description: Tento článek obsahuje informace o rezervaci pojmenovaných zdrojů pro požadavek na obecný zdroj.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9598490da1905227e517da8ba90f8ffd1df88566
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916234"
---
# <a name="book-named-resources-from-resource-requirements"></a>Rezervace pojmenovaných zdrojů z požadavků na zdroje

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pro nahrazení obecného zdroje, který obsahuje požadavek na zdroj, můžete rezervovat pojmenovaný zdroj.

1. V Project Service Automation (PSA) klikněte na stránce **Projekty** na kartu **Tým**.
2. Vyberte ze seznamu obecný zdroj, který obsahuje požadavek na zdroj, a pak klikněte na **Rezervovat**. Nebo otevřete požadavek na zdroj a pak klikněte na **Rezervovat**.


![Rezervace obecného člena týmu.](media/RM-how-to-14.png)


3. Na stránce **Pomocník plánování** vyberte pojmenovaný zdroj, který chcete rezervovat pro projektový tým, a klikněte na tlačítko **Rezervovat**.

![Rezervace obecného člena týmu pomocí pomocníka pro plánování.](media/RM-how-to-15.png)

Pokud je rezervace dokončena a vyplněna pojmenovaným zdrojem, je obecný zdroj nahrazen pojmenovaným zdrojem.

![Nahrazení obecného člena týmu pojmenovaným členem týmu.](media/RM-how-to-16.png)

Přiřazení v plánu jsou aktualizována také pomocí pojmenovaného zdroje.

![Pojmenovaný člen týmu přiřazený k úkolům projektu.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Vyplnění obecného zdroje pomocí několika pojmenovaných zdrojů
Vyplnění požadavku na obecný zdroj pomocí několika pojmenovaných zdrojů je podobné přiřazení jednoho pojmenovaného zdroje. Existuje například úkol s dobou trvání pět dní a úsilím 120 hodin. Tento úkol nemůže být dokončen jedním zdrojem, který pracuje typicky osm hodin denně, pět dní v týdnu. 

![Úkol, který potřebuje 120 hodin úsilí po dobu pěti dnů.](media/RM-how-to-21.png)

Požadavek je na 120 hodin robotického inženýrství po dobu pěti dní, což je 24 hodin denně.

![Požadavek na den.](media/RM-how-to-22.png)

Toto je příklad, kdy je k naplnění obecného požadavku na zdroj potřeba více pojmenovaných zdrojů. Pro splnění požadavku budete potřebovat rezervovat více zdrojů.

![Rezervace více zdrojů pro splnění požadavku.](media/RM-how-to-23.png)

Hlavní rozdíl v tomto scénáři spočívá v tom, že obecný zdroj zůstává v týmu přiřazeném k úkolu, a že zarezervovaní pojmenovaní členové týmu zdrojů nejsou přiřazeni jako součást pozice. Projektový manažer může přiřadit práci odpovídající pojmenovaným zdrojům. Zobrazení **Vyrovnání** může projektovému manažerovi pomoci při rozdělování rezervací mezi více zdrojů pro přiřazení úkolů. Není to prováděno automaticky, protože v libovolném scénáři, který je složitější než výše uvedený jednoduchý příklad, kdy například máte balík úkolů, které tvoří požadavek, musí být záměr, jak chce projektový manažer přiřazení provést, vypočten systémem. Protože systém nedokáže pochopit záměr, je pravděpodobné, že předpoklady budou jiné, než je zamýšleno, a dojde k nesprávnému nebo nepředvídatelnému výsledku. Předvídatelným výsledkem je, že obecný zdroj zůstává přiřazen, dokud projektový manažer záměrně nevytvoří přiřazení pomocí zobrazení **Vyrovnání**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
