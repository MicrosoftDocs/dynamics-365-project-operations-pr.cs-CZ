---
title: Přehled odsouhlasení zdrojů
description: Tento článek poskytuje informace, které vám pomohou zajistit, aby rezervace zdrojů a přiřazení k projektům byly v souladu.
author: ruhercul
ms.date: 01/08/2021
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: eaad9187f08be810d730f5a8ca6411ecee85bbc4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926308"
---
# <a name="resource-reconciliation-overview"></a>Přehled odsouhlasení zdrojů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Pro členy týmu jsou rezervace a přiřazení volně provázené. Jinými slovy, zdroje mohou obsahovat přiřazení, ale žádné rezervace, nebo mohou obsahovat rezervace, ale žádná přiřazení. V ideálním případě by měly být rezervace a přiřazení zarovnány, aby zdroje měly potvrzenou kapacitu k provádění přiřazení úkolů. Rezervace mohou být však založeny na dostupnosti a časování úkolů se může při pokračování projektu změnit. Volné spojení rezervací a přiřazení je proto flexibilní.

Karta **Vyrovnání** na stránce **Projekty** projektovým manažerům umožňuje vyrovnat rezervace a přiřazení členů týmů pro projektové týmy.

Karta **Vyrovnání** zobrazuje rezervace a přiřazení až k úrovni jednotlivých přiřazení úkolů pro každého člena týmu. Hodiny se zobrazují v buňkách představují časová období od měsíců po dny. Na kartě je také zobrazen celkový čistý součet pro projekt, spolu se sloupcem **Celkem**.

Pro každý zdroj je na kartě **Vyrovnání** vypočten rozdíl mezi rezervacemi člena týmu a souhrnnými přiřazeními člena týmu. V ideálním případě by tento rozdíl měl být 0 (nula). Jinými slovy, mezi rezervacemi a přiřazeními by neměl být žádný rozdíl. Rozdíly jsou barevné a stínované, aby upozornily na dva stavy:

- **Nedostatečná rezervace** – v případě, že zdroj obsahuje více přiřazení než rezervací, dojde k nedostatatečné rezervaci. Vzhledem k tomu, že tato kapacita nebyla rezervována, může projektový manažer tento stav napravit rozšířením rezervací zdroje tak, aby pokryly deficit.
- **Nadbytečné rezervace** – k nadbytečným rezervacím dochází, pokud byl zdroj rezervován do projektu, ale nebyl přiřazen k úkolům. Tento stav může být přijatelný v případech, kdy byl zdroj pro projekt rezervován předtím, než došlo k přiřazení úkolu. V jiných případech, kde neexistuje žádný plán pro přiřazení zdroje k úkolům, by však vedoucí projektu měl zvážit zrušení rezervací zdroje. Tímto způsobem lze kapacitu využít pro jiný projekt.

Pokud v některých případech zobrazíte čas na vyšší úrovni než denní úroveň (například úroveň měsíce), můžete u zdroje vidět čistý nulový rozdíl (jinými slovy, rezervace rovná se přiřazení). Pokud však zobrazíte čas na úrovni týdne, můžete se setkat s tím, že v prvním týdnu jsou přiřazení ve výši nula hodin a rezervace 40 hodin, ale ve druhém týdnu jsou přiřazení 40 hodin a rezervace nula hodin. Celkově jsou rezervace a přiřazení vyrovnané, liší se však od jednoho týdne k dalšímu.

Když zobrazíte čas na vyšších úrovních, buňky na kartě **Vyrovnání** mají indikátor, který vás upozorní, že se na nižších úrovních vyskytují rozdíly. Dvojitým klepnutím nebo dvojitým kliknutím do buňky můžete provést přiblížení a zobrazit rozdíl. Podržením nebo (kliknutím pravým tlačítkem myši) můžete poté zobrazení oddálit. Výběrem zdroje a následným použitím ovládacího prvku **Další rozdíl** na panelu nástrojů mřížky můžete přejít na další rozdíl mezi rezervacemi a přiřazeními pro daný zdroj. Poté můžete použít ovládací prvek **Předchozí rozdíl** a vrátit se zpět. V **Nastavení** také můžete vypnout ukazatel rozdílu a chování navigace.

Pokud máte pro zdroj přiřazení úkolů, ale nemáte žádné rezervace, vyberte nedostatečnou rezervaci na kartě **Vyrovnání** na stránce **Projekty** a pak vyberte **Prodloužit rezervaci**. Zobrazí se dialogové okno **Prodloužit rezervaci**, ve kterém je uvedena rezervace potřebná k vyřešení nedostatku zdroje. Dialogové okno také zobrazuje existující rezervace zdroje ve všech projektech nebo jiných plánovatelných entitách. Pokud vyberete **OK** pro vytvoření rezervace pro zdroj bez ohledu na dostupnost zdroje, můžete způsobit přerezervaci.

Rezervace vytvořené prostřednictvím akce **Prodloužit rezervaci** jsou spojeny s požadavkem primárního projektu. Při zahájení rozšíření nelze určit konkrétní požadavek, který musí být rozšířen, protože prostředek může být přidružen k více než jednomu požadavku na projekt.

Projektový manažer nebo správce prostředku pak může pomocí Plánovací vývěsky spravovat všechny situace, ve kterých je zdroj přerezervovaný nad svoji kapacitu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]