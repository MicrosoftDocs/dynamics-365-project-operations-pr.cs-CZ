---
title: Přehled odsouhlasení zdrojů
description: Toto téma poskytuje informace o zajištění toho, aby rezervace a přiřazení zdrojů k projektům byly sladěny.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e2b16a6e1c48769ed4d903e546804ba1c4e1c4fa
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073722"
---
# <a name="resource-reconciliation-overview"></a>Přehled odsouhlasení zdrojů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Pro členy týmu jsou rezervace a přiřazení volně provázené. Jinými slovy, zdroje mohou obsahovat přiřazení, ale žádné rezervace, nebo mohou obsahovat rezervace, ale žádná přiřazení. V ideálním případě by měly být rezervace a přiřazení zarovnány, aby zdroje měly potvrzenou kapacitu k provádění přiřazení úkolů. Rezervace mohou být však založeny na dostupnosti a časování úkolů se může při pokračování projektu změnit. Volné spojení rezervací a přiřazení je proto flexibilní.

Karta **Vyrovnání** ve formuláři **Projekt** projektovým manažerům umožňuje vyrovnat rezervace a přiřazení členů týmů pro projektové týmy.

Karta **Vyrovnání** také zobrazuje rezervace a přiřazení až k úrovni jednotlivých přiřazení úkolů pro každého člena týmu. Hodiny se zobrazují v buňkách reprezentujících časová období od měsíců po dny.

Na kartě je také zobrazen celkový čistý součet pro projekt, spolu se sloupcem **Celkem**.

Pro každý zdroj je na kartě vypočten rozdíl mezi rezervacemi člena týmu a souhrnnými přiřazeními člena týmu. V ideálním případě by tento rozdíl měl být 0 (nula). Jinými slovy, mezi rezervacemi a přiřazeními by neměl být žádný rozdíl. Rozdíly jsou barevné a stínované, aby upozornily na dva stavy:

- **Nedostatečná rezervace** – v případě, že zdroj obsahuje více přiřazení než rezervací, dojde k nedostatatečné rezervaci. Vzhledem k tomu, že tato kapacita nebyla rezervována, může projektový manažer tento stav napravit rozšířením rezervací zdroje tak, aby pokryly deficit.
- **Nadbytečné rezervace** – k nadbytečným rezervacím dochází, pokud byl zdroj rezervován do projektu, ale nebyl přiřazen k úkolům. Tento stav může být přijatelný v případech, kdy byl zdroj pro projekt rezervován předtím, než došlo k přiřazení úkolu. V jiných případech však není plánováno přiřazení zdroje k úkolům. V těchto případech by měl projektový manažer zvážit zrušení rezervací zdroje, aby bylo možné použít kapacitu pro jiný projekt.

Pokud v některých případech zobrazíte čas na vyšší úrovni než denní úroveň (například úroveň měsíce), můžete u zdroje vidět čistý nulový rozdíl (jinými slovy, rezervace = přiřazení). Pokud však zobrazíte čas na úrovni týdne, můžete se setkat s tím, že v prvním týdnu jsou přiřazení ve výši nula hodin a rezervace 40 hodin, ale ve druhém týdnu jsou přiřazení 40 hodin a rezervace nula hodin. Celkově jsou rezervace a přiřazení vyrovnané, liší se však od jednoho týdne k dalšímu.

Když zobrazíte čas na vyšších úrovních, buňky na kartě **Vyrovnání** mají indikátor, který vás upozorní, že se na nižších úrovních vyskytují rozdíly. Dvojitým kliknutím do buňky můžete provést přiblížení a zobrazit rozdíl. Kliknutím pravým tlačítkem myši můžete zobrazení oddálit. Výběrem zdroje a následným použitím ovládacího prvku **Další rozdíl** na panelu nástrojů mřížky můžete přejít na další rozdíl mezi rezervacemi a přiřazeními pro daný zdroj. Poté můžete použít ovládací prvek **Předchozí rozdíl** a vrátit se zpět. V **Nastavení** také můžete vypnout ukazatel rozdílu a chování navigace.


Pokud máte pro zdroj přiřazení úkolů, ale nemáte žádné rezervace, vyberte na stránce **Projekty** , na kartě **Vyrovnání** nedostatečnou rezervaci a pak vyberte **Prodloužit rezervaci**. Zobrazí se dialogové okno **Prodloužit rezervaci** , ve kterém je uvedena rezervace potřebná k vyřešení nedostatku zdroje. Zobrazuje také existující rezervace zdroje ve všech projektech nebo jiných plánovatelných entitách. Pokud vyberete **OK** pro vytvoření rezervace pro zdroj bez ohledu na dostupnost zdroje, můžete způsobit přerezervaci.

Projektový manažer nebo správce prostředku pak může pomocí Plánovací vývěsky spravovat všechny situace, ve kterých je zdroj přerezervovaný nad svoji kapacitu.

