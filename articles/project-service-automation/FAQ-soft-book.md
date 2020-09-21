---
title: Předběžná rezervace prostředku
description: Toto téma obsahuje informace o tom, jak předběžně plánovat nebo předběžně rezervovat členy projektového týmu.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.prod: Applies to Project Service version 3.x
ms.technology: ''
ms.assetid: 04e02ff7-1024-4b65-a281-6f149921b63d
ms.author: ruhercul
audience: Admin
ms.openlocfilehash: 07e768d756732e31df82a9865b957dae09c60821
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750301"
---
# <a name="soft-book-a-resource"></a>Předběžná rezervace prostředku

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nezávazně můžete naplánovat nebo předběžně rezervovat zdroj do projektového týmu pro zobrazení toho, že plánujete přiřazení zdroje k projektu. Předběžné rezervace nespotřebovávají dostupné kapacity zdroje a předběžně rezervované členy týmu lze přiřadit k úkolům projektu. Nicméně protože předběžné rezervace nespotřebovávají kapacitu zdroje, můžete stále závazně rezervovat zdroj pro jiné úkoly ve stejném období. Obecné zdroje nelze předběžně rezervovat, stejně jako předběžná rezervace nemůže splnit požadavek na obecný zdroj.

Seznam předběžně rezervovaných členů týmu je uveden na kartě **Tým** stránky **Projekt**, se svými předběžně rezervovanými hodinami zobrazenými ve sloupci **Předběžně rezervované hodiny** v zobrazení **Pojmenovaní členové týmu**. Předběžně rezervovaní členové týmu jsou také uvedeni na Plánovací vývěsce. Protože jsou předběžně rezervováni, Plánovací vývěska nezobrazuje všechny spotřeby kapacity pro tyto zdroje. Předběžně rezervovaný čas se nezobrazí na kartě **Vyrovnání**, ani není zobrazen v poli **Prodloužit rezervace** na kartě **Vyrovnání** Plánovací vývěsky. 

Předběžně rezervovat člena týmu na projektu lze dvěma způsoby: přímo z Plánovací vývěsky nebo přidáním člena týmu na kartě **Tým**. 

## <a name="soft-book-from-the-schedule-board"></a>Předběžná rezervace z Plánovací vývěsky
Chcete-li provést předběžnou rezervaci zdroje z Plánovací vývěsky, postupujte následujícím způsobem. 

1. Otevřete Plánovací vývěsku a poté v panelu **Požadavky na rezervace** vyberte kartu **Projekt**.
2. Najděte projekt, pro který chcete předběžně rezervovat zdroj. Pokud je v seznamu velký počet projektů, vyberte záhlaví sloupce **Projekt** a potom pomocí filtru vyhledejte jeden nebo více projektů.
3. Vyberte projekt a potom ho přetáhněte na časovou mřížku zdroje.
5. V panelu **Vytvořit rezervaci zdroje** upravte počáteční a koncové datum, nastavte **Stav rezervace** na **Předběžná** a pak nastavte hodiny. 
6. Klikněte na **Rezervovat**. Zdroj se nyní zobrazuje na kartě **Tým** jako zdroj pro projekt. V zobrazení **Pojmenovaný člen týmu** uvidíte předběžně rezervované hodiny ve sloupci **Předběžně rezervované hodiny**.

> [!NOTE]
> Nyní můžete přiřadit předběžně rezervované k úkolům na kartě **Plán**. Na kartě **Vyrovnání** zobrazuje zdroj nedostatečnou rezervaci vztahující se k přiřazení úkolů, protože karta **Vyrovnání** zvažuje pouze závazné rezervace. Funkci **Prodloužit rezervace** můžete použít k závazné rezervaci zdroje pro eliminaci nedostatečných závazných rezervací proti přiřazením zdrojů. Budete muset ručně zrušit předběžnou rezervaci pro zdroj pomocí možnosti **Správa rezervací**.

## <a name="soft-book-on-the-team-tab"></a>Předběžná rezervace na kartě Tým

Členy týmu můžete přidat přímo na kartě **Tým** a poté změňte jejich stav rezervace ze **Závazný** na **Předběžný** pomocí možnosti **Správa rezervací**. Pokud tímto způsobem přidáte člena týmu, bude to mít vždy za následek závaznou rezervaci, pokud nezvolíte metodu přidělení **Žádná**.

Chcete-li použít tuto metodu, proveďte následující kroky:

1. Na stránce **Projekt** klikněte na kartě **Tým** na **Nový**.
2. Vyberte rezervovatelný zdroj, roli a data od a do.
3. Vyberte metodu přidělení jinou než **Žádná**.
4. Zvolte **Uložit**. Zdroje uvidíte na mřížce a jejich hodiny budou ve sloupci **Závazně rezervované hodiny**.
5. Kliknutím na **Správa rezervací** spravujte rezervace zdroje.
6. Při otevření Plánovací vývěsky rozbalte zdroje pro zobrazení jejich rezervací. Uvidíte rezervaci zobrazenou jako **Závazná**.
7. Klikněte pravým tlačítkem myši na rezervaci a u možnosti **Změnit stav** vyberte **Předběžná rezervace** \> **Předběžná**. Stav rezervace je nyní **Předběžná**.
8. Po zavření Plánovací vývěsky, uvidíte, že hodiny zdroje byly přesunuty ze sloupce **Závazně rezervované hodiny** do **Předběžně rezervované hodiny** na mřížce karty **Tým** v zobrazení **Pojmenovaní členové týmu**.

> [!NOTE]
> Použijete-li ke změně stavu ze **Závazná** na **Předběžná** **Zachovat rezervace**, tak pokud závazně rezervujete zdroj pro tým a poté mu přiřadíte úkoly, přiřazení úkolů pro tento zdroj se zachovají. Nicméně na kartě **Vyrovnání** bude mít zdroj nedostatečnou rezervaci, protože se zvažují pouze závazné rezervace při vyrovnání rezervací vůči přiřazením. Funkci **Prodloužit rezervace** na kartě **Vyrovnání** můžete použít k závazné rezervaci zdroje pro eliminaci nedostatečných závazných rezervací proti přiřazením zdrojů. Budete muset zrušit předběžnou rezervaci pro zdroj pomocí možnosti **Správa rezervací**.

Pokud budete chtít změnit předběžně rezervovaný zdroj člena týmu na závazně rezervovaného člena týmu, proveďte následující kroky:

1. Na Plánovací vývěsce rozbalte zdroje pro zobrazení jejich rezervací. Uvidíte rezervaci zobrazenou jako **Předběžná**.
2. Klikněte pravým tlačítkem myši na rezervaci a u možnosti **Změnit stav** vyberte **Závazná rezervace** \> **Závazná**. Stav rezervace je nyní **Závazná**.
3. Po zavření Plánovací vývěsky, návratu na projekt a otevření karty **Tým** uvidíte, že hodiny zdroje byly přesunuty ze sloupce **Předběžně rezervované hodiny** do sloupce **Závazně rezervované hodiny** na kartě **Tým** v zobrazení **Pojmenovaní členové týmu**. Pokud byl zdroj přiřazen k úkolům, nebude již zobrazovat nedostatečnou rezervaci na kartě **Vyrovnání**, protože jeho rezervace jsou nyní závazné.

