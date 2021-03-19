---
title: Vytvořit přiřazení zdrojů
description: Toto téma poskytuje informace o vytváření přiřazení obecných a pojmenovaných zdrojů.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a6f4f12a962cb570e8b83d8ee7a01fc0cc2c6155
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287095"
---
# <a name="create-resource-assignments"></a>Vytvořit přiřazení zdrojů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_


Přiřazení zdroje je přímé přidružení člena projektového týmu k úkolu uzlu typu list. Toto téma obsahuje informace o různých způsobech přiřazení zdrojů.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Vytvoření obecného člena týmu prostřednictvím přiřazení úkolu


Když vytvoříte obecného člena týmu prostřednictvím přiřazení úkolů, vytvoříte zástupný symbol nebo obecný zdroj. Tento obecný zdrojpopisuje vlastnosti pojmenovaného zdroje, u kterého chcete, aby pracoval na úkolech. Potom vygenerujete požadavek nebo odešlete žádost pomocí požadavku, který slouží k vyhledávání a rezervaci pojmenovaného zdroje.

1. V mřížce Plán pro daný úkol vyberte ikonu Zdroj v buňce **Zdroj**.
2. Zadejte název sloužící jako zástupný text názvu zdroje. Například Programový manažer.
3. Vyberte **Vytvořit** a v poli **Rychlé vytvoření člena týmu** nastavte roli pro obecný zdroj.
4. Přiřaďte úkoly dle potřeby k tomuto zástupnému zdroji výběrem tohoto zdroje ve **Výběru zdrojů** pro daný úkol. Zdroje uvedené pod položkou **Členové týmu**.
5. Po dokončení přiřazování obecného zdroje vyberte obecný zdroj na kartě **Tým** a poté vyberte **Vygenerovat požadavek** pro vytvoření požadavku na zdroj pro obecný zdroj.
6. Vyberte možnost **Rezervovat** pro obecný zdroj a pak můžete použít plánovací vývěsku pro nalezení a rezervaci skutečného zdroje. Je také možné odeslat požadavek na splnění manažerem zdrojů.
7. Když je generický zdroj zcela splněn (splnění částečného požadavku na zdroj nebude mít za následek přiřazení zdroje) s pojmenovaným zdrojem, je generický prostředek odebrán z týmu. Přiřazení úkolů pro obecný zdroj jsou přiřazeny pojmenovanému zdroji, který splnil požadavek na obecný zdroj.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Přiřazení pojmenovaného zdroje ze seznamu všech rezervovatelných zdrojů

Můžete použít vyhledávací pole ve **Výběru zdrojů** pro vyhledání všech aktivních rezervovatelných zdrojů a přiřadit je k libovolnému úkolu typu list. Zdroje přiřazené tímto způsobem jsou do týmu přidány bez jakýchkoli rezervací. To je podobné jako přidání člena týmu a vybrání metody přidělení **Žádná**. Zdroj se zobrazí se na kartách **Tým**, **Přiřazení zdrojů** a **Vyrovnání** jako zdroj pouze s přiřazením a nedostatečnou rezervací. Zarezervujte je, pokud chcete použít jejich dostupnost.

1. Z mřížky úkolů, vývěsky nebo časové osy přejděte na buňku **Přiřazeno**.
2. Do vyhledávacího pole začněte psát jméno. Výsledky vyhledání názvu se zobrazí ve **Výběru zdrojů** v části **Další zdroje**.
3. Vyberte zdroj, který chcete přiřadit k úkolu, nebo vyberte název zdroje pod položkou **Další týmové zdroje**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]