---
title: Vytvořit přiřazení zdrojů
description: Tento článek poskytuje informace o vytváření přiřazení obecných a pojmenovaných zdrojů.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811985"
---
# <a name="create-resource-assignments"></a>Vytvořit přiřazení zdrojů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_


Přiřazení zdroje je přímé přidružení člena projektového týmu k úkolu uzlu typu list. Tento článek obsahuje informace o různých způsobech přidělení zdrojů.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Vytvoření obecného člena týmu prostřednictvím přiřazení úkolu


Když vytvoříte obecného člena týmu prostřednictvím přiřazení úkolů, vytvoříte zástupný symbol nebo obecný zdroj. Tento obecný zdroj popisuje vlastnosti pojmenovaného zdroje, u kterého chcete, aby pracoval na úkolech. Potom vygenerujete požadavek nebo odešlete žádost pomocí požadavku, který slouží k vyhledávání a rezervaci pojmenovaného zdroje.

1. V mřížce Plán pro daný úkol vyberte ikonu Zdroj v buňce **Zdroj**.
2. Zadejte název sloužící jako zástupný text názvu zdroje. Například Programový manažer.
3. Vyberte **Vytvořit** a v poli **Rychlé vytvoření člena týmu** nastavte roli pro obecný zdroj.
4. Přiřaďte úkoly dle potřeby k tomuto zástupnému zdroji výběrem tohoto zdroje ve **Výběru zdrojů** pro daný úkol. Zdroje uvedené pod položkou **Členové týmu**.
5. Po dokončení přiřazování obecného zdroje vyberte obecný zdroj na kartě **Tým** a poté vyberte **Vygenerovat požadavek** pro vytvoření požadavku na zdroj pro obecný zdroj.
6. Vyberte možnost **Rezervovat** pro obecný zdroj a pak můžete použít plánovací vývěsku pro nalezení a rezervaci skutečného zdroje. Je také možné odeslat požadavek na splnění manažerem zdrojů.
7. Pokud je obecný zdroj plně vyplněn pojmenovaným zdrojem, je obecný zdroj z týmu odebrán. (Splnění částečného požadavku na zdroj nebude mít za následek přiřazení zdroje.) Přiřazení úkolu pro obecný zdroj jsou přiřazována pojmenovanému zdroji, který vyplnil požadavek na zdroj obecného zdroje.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Přiřazení pojmenovaného zdroje ze seznamu všech rezervovatelných zdrojů

Můžete použít vyhledávací pole ve **Výběru zdrojů** pro vyhledání všech aktivních rezervovatelných zdrojů a přiřadit je k libovolnému úkolu typu list. Zdroje přiřazené tímto způsobem jsou do týmu přidány bez jakýchkoli rezervací. To je podobné jako přidání člena týmu a vybrání metody přidělení **Žádná**. Zdroj se zobrazí se na kartách **Tým**, **Přiřazení zdrojů** a **Vyrovnání** jako zdroj pouze s přiřazením a nedostatečnou rezervací. Zarezervujte je, pokud chcete použít jejich dostupnost.

1. Z mřížky úkolů, vývěsky nebo časové osy přejděte na buňku **Přiřazeno**.
2. Do vyhledávacího pole začněte psát jméno. Výsledky vyhledání názvu se zobrazí ve **Výběru zdrojů** v části **Další zdroje**.
3. Vyberte zdroj, který chcete přiřadit k úkolu, nebo vyberte název zdroje pod položkou **Další týmové zdroje**.

## <a name="editing-resource-assignment-contours"></a>Úprava křivek přiřazení zdrojů

Ve výchozím nastavení, když jsou zdroje přiřazeny k úkolu v plánu, jejich práce je lineárně rozdělena do každého zdroje na základě pracovní doby zdroje a režimu plánu projektu. Projektový manažer může použít mřížku přiřazení zdrojů k upřesnění odhadů práce každého zdroje, který je přiřazen k jednomu nebo více úkolům v různých časových škálách. Tato funkce pomáhá projektovým manažerům vytvářet přesnější odhady nákladů a prodeje, které jsou řízeny obrysy přiřazení zdrojů, které se generují, když je zdroj přiřazen k úkolu. Kromě toho mohou projektoví manažeři snadněji zohlednit poptávku po zdrojích, která je nutná k vytvoření poptávky v požadavcích na zdroje.

### <a name="navigation"></a>Navigace

Chcete-li získat přístup k mřížce pro úpravy průběhových křivek, vedoucí projektu nejprve vybere kartu **Úkoly** na hlavní stránce projektu a poté vybere kartu **Přiřazení**.

![Záložka Přiřazení na záložce Úkoly na hlavní stránce projektu.](media/AssignmentGrid.png)

Mřížka podporuje dva způsoby seskupování: **seskupit podle zdroje** a **seskupit podle úkolu**. Na rozdíl od zobrazení mřížky nelze sloupce konfigurovat. Jediné viditelné sloupce jsou **Přiřazeno**, **Název úkolu**, **Začátek přiřazení**, **Dokončení přiřazení** a **Práce přiřazení**.

Když je mřížka zpočátku vykreslena, začíná na nejstarší průběhové křivce přiřazení. Pokud váš plán neobsahuje žádné úkoly, které vyžadují práci, bude mřížka prázdná a nic nevykreslí.

![Prázdná mřížka přiřazení.](media/emptyassignmentgrid.png)

Chcete-li zobrazit své průběhové křivky a různá časová měřítka, je k dispozici také mřížka přiřazení zdrojů pouze pro čtení a mřížka sesouhlasení zdrojů.

### <a name="resource-calendars"></a>Kalendáře zdrojů

Schopnost upravit průběhovou křivku pro konkrétní den se řídí pracovními dny zdroje, jak je uvedeno v jejich kalendáři. Pokud je buňka pro daný zdroj deaktivována, nemá tento zdroj během tohoto období pracovní dny.

Průběhové křivky zdroje mohou přesahovat aktuální datum zahájení a ukončení přiřazeného úkolu. Pokud je průběhová křivka aktualizována tak, že je po nejpozdějším datu ukončení úkolu nebo po nejstarším datu zahájení úkolu, datum ukončení nebo datum zahájení úkolu se podle potřeby změní. Pokud je však průběhová křivka aktualizována tak, že je dřívější než datum zahájení úkolu, který je propojen s předchůdcem, aktualizace se nezdaří, protože přiřazení spustí úkol, aby se spustil před dokončením jeho předchůdce, a toto chování aktuálně není podporováno.

### <a name="co-authoring"></a>Spoluvytváření

Změny v mřížce přiřazení zdrojů se automaticky projeví ve všech souvisejících zobrazeních, včetně zobrazení grafu, časové osy, tabule a mřížky. Pokud projekt kontroluje více uživatelů současně, všechny změny, které jeden uživatel provede, se projeví v mřížce. Naopak všechny změny provedené v mřížce přiřazení zdrojů se zobrazí všem ostatním uživatelům, kteří si prohlížejí projekt ve stejné relaci.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
