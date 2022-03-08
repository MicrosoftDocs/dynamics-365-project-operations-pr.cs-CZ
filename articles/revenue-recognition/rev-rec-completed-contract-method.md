---
title: Správa odhadů výnosů
description: Toto téma poskytuje informace o tom, jak pracovat s odhady výnosů projektů.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8d118826f8c63b9540435e320924d4562ab191ba126088560f5def1c1ff0b908
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996518"
---
# <a name="manage-revenue-estimates"></a>Správa odhadů výnosů

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Můžete vytvářet, počítat, zaúčtovat, stornovat nebo eliminovat odhady tržeb. Můžete to udělat buď ručně, nebo pomocí pravidelného procesu. Toto téma poskytuje informace o tom, jak pracovat s odhady výnosů projektů.

### <a name="manage-revenue-estimates-manually"></a>Správa odhadů výnosů ručně

V projektu odhadu výnosů s pevnou cenou nebo na stránce **Dotaz na odhad** (**Řízení projektů a účetnictví** > **Sestavy a dotazy** > **Dotazy a sestavy výnosů**), vyberte **Odhady**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Spravujte odhady výnosů pomocí pravidelného procesu

Přejděte na **Řízení projektů a účetnictví** > **Periodické** > **Odhady** a vyberte odpovídající proces.

## <a name="create-a-revenue-estimate"></a>Vytvořte odhad příjmů

Chcete-li vytvořit odhad výnosů, proveďte následující postup. 

1. Přejděte na **Řízení projektů a účetnictví** > **Periodické** > **Odhady**.
2. Vyberte **Nové**. Na stránce **Vytvoření odhadu** vyberte následující parametry:

   - **Kód období**: Tento kód určuje, jak často se odhady účtují.
   - **Datum odhadu**: Datum zpracování odhadu.
   - **Kontinuální**: Zaškrtnutím tohoto políčka vytvoříte odhady pouze v případě, že odhady byly zaúčtovány v předchozím období, nebo pokud je odhad prvním vytvořeným odhadem. Pokud to není vybráno, vytvoří se odhady, i když odhady nebyly zaúčtovány v předchozím období.
   - **Metoda Náklady na dokončení**: Definujte, jak odhadnout zbývající práci projektu. Další informace viz [Metoda Náklady na dokončení](cost-complete-methods.md).
   - **Způsob dokončení**: Vyberte metodu dokončení z následujících možností:
     - **Automaticky**: Procento dokončení se vypočítá automaticky a na základě nákladových řádků zahrnutých do výpočtu. Šablona nákladů definuje nákladové řádky, které jsou zahrnuty.
     - **Ručně**: Procento dokončení se rovná procentu dokončení posledního odhadu. Po vytvoření odhadu můžete změnit **Ruční výpočet** na stránce **Odhady**.
     - **Ze šablony nákladů**: Kombinace automatické a manuální metody. Tato možnost je nastavena automaticky nebo ručně, v závislosti na výchozí hodnotě v šabloně nákladů.
   - **Předpovědní model**: Vyberte model předpovědi pro odhad.
   - **Vytisknout seznam odhadů**: Vytvořit a zobrazit seznam odhadů. Seznam obsahuje stav aktuální funkce. Na sestavě můžete vytisknout všechna varování týkající se odhadu. Následující podmínky způsobí, že se v seznamu odhadů zobrazí varování:
     - Procento dokončení více než 100 procent.
     - Procento dokončení méně než 0 procent.
     - Záporná částka ve sloupci **K dokončení**.
     - Odhad bez odpovídající částky smlouvy.
     - Odhad bez připojeného odhadu nákladů.
   - **Zobrazit Infolog**: Tuto možnost vyberte, chcete-li obdržet zprávu, která obsahuje informace o projektech odhadu, které byly zpracovány při spuštění úlohy.


## <a name="post-wip-or-accruals"></a>Zaúčtujte nedokončenou práci nebo časové rozlišení

Poté, co jsou odhady vyhodnoceny, jsou udržovány, snižovány nebo zvyšovány. Poté můžete odeslat WIP, když pracujete s principem hodnocení **Dokončená smlouva**, nebo zaúčtujte časové rozlišení, když pracujete s principem hodnocení **Dokončené procento**.
  
Stav odhadovaného období se změní z **Vytvořeno** na **Zaúčtováno**.

## <a name="reverse-wip-or-accruals"></a>Reverzní WIP nebo časové rozlišení

Možnost storna použijte k připsání již zaúčtovaných WIP nebo časového rozlišení a poté vytvořte odhady pro dané období.

> [!NOTE]
> Chcete-li stornovat období, které se nachází mezi jinými obdobími, stornujte požadované období odhadu a poté je znovu zaúčtujte. Protože všechna následující období závisí na odhadech z předchozího období, nevynechávejte žádná období.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Odstraňte projekt odhadu a dokončete projekt

Posledním krokem v procesu odhadu je odstranění projektu odhadu a ukončení projektu s pevnou cenou, když procento dokončení dosáhne 100 procent.

Při spuštění eliminace dojde k následujícímu:

- U projektu s pevnou cenou s dokončenou smlouvou jsou hodnoty WIP vymazány z rozvahových účtů a účtovány do účtů zisků a ztrát.
- U projektu s pevnou cenou s dokončeným procentem se časová rozlišení odeberou z účtů zisků a ztrát.

Odhad změní stav na **Eliminováno**.

> [!NOTE]
> Ve zvláštních případech může procento přesáhnout 100 procent. Pokud k tomu dojde, snižte procento dokončení pomocí volby **Metoda Nastavte náklady na dokončení na nulu**, čímž dosáhnete 100 procent.

## <a name="reverse-elimination"></a>Storno eliminace

1. Přejděte na **Řízení projektů a účetnictví** > **Periodické** > **Odhady** > **Storno eliminace**. 
2. V podokně akcí na kartě **Proces** ve skupině **Udržovat** vyberte **Odhad**. 
3. Vyberte **Storno eliminace**.

Tato stránka slouží ke stornu všech eliminací se stanoveným datem odhadu a se stavem odhadu **Eliminováno**. Stav transakce se změní po výběru příslušných polí.

Tím se také automaticky změní stav projektu na **V procesu**, pokud je fáze projektu nastavena na dokončeno. Stav odhadu období projektu se změní zpět na **Zaúčtováno**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]