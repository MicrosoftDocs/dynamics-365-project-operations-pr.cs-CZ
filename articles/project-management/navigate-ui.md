---
title: Navigace v uživatelském rozhraní
description: Tento článek poskytuje informace o správě projektů v Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1db62cd8538444552a1296c6f10b651c9dbd34ef
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923778"
---
# <a name="navigating-the-user-interface"></a>Navigace v uživatelském rozhraní

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

## <a name="overview"></a>Přehled

Hlavní formulář projektu je rozdělen do několika karet. Každá karta představuje jinou úroveň podrobností v rámci projektu.

- **Souhrn** : Poskytuje popis projektu a agreguje plánovaný i skutečný výkon projektu.

    ![Karta Souhrn a pole.](media/navigation7.png)

- **Úkoly** : Poskytuje podrobnosti týkající se strukturovaného rozpisu prací vyjádřeného jako zobrazení mřížky, plánovací vývěska nebo Ganttův diagram.

    ![Karta Úkol a pole.](media/navigation8.png)

- **Tým** : Poskytuje podrobnosti o účastnících projektu. V tomto zobrazení je také shrnuto přidělené úsilí každého člena týmu.

    ![Karta Tým a pole.](media/navigation9.png)

- **Přiřazení zdrojů** : Poskytuje časově odstupňovaný pohled na úsilí každého zdroje v projektu.

    ![Karta Přiřazení zdrojů a pole.](media/navigation10.png)

- **Vyrovnání zdrojů**: Poskytuje časově odstupňovaný pohled na rozdíly mezi přiřazením každého pojmenovaného zdroje a jejich rezervacemi.

    ![Karta Vyrovnání zdrojů a pole.](media/navigation11.png)

- **Odhady** : Poskytuje časově odstupňovaný pohled na odhady nákladů a prodejů projektu.

    ![Karta Odhady a pole.](media/navigation12.png)

- **Sledování** : Poskytuje pohled zobrazující průběh úkolů ve strukturovaném rozpisu prací pro úsilí, náklady a prodej.

    ![Karta Sledování a pole.](media/navigation13.png)

- **Prodej** : Poskytuje přímé odkazy na nabídky a smlouvy přidružené k projektu.

- **Odhady výdajů** : Poskytuje mřížku definující výdaje projektu na základě kategorií výdajů organizace.

    ![Karta Odhady výdajů a pole.](media/navigation14.png)

## <a name="grid-controls"></a>Ovládací prvky mřížky

Následuje stručný přehled typických ovládacích prvků na různých kartách plánování projektu.

### <a name="refresh"></a>Obnovit

**Obnovit** : Načte nejnovější data ze serveru, pokud po načtení mřížky došlo k jakýmkoli změnám.

![Tlačítko Aktualizovat.](media/navigation7.png)

### <a name="group-by"></a>Seskupit podle

**Seskupit podle** : Aktualizuje seskupení řádků v mřížce tak, aby odrážely buď zdroje, role nebo kategorie na základě potřeb uživatele.

![Tlačítko Seskupit podle.](media/navigation6.png)

### <a name="previousnext"></a>Předchozí/Další

**Předchozí**/**Další** : Aktualizujte viditelná časová období na časově rozložených mřížkách.

![Tlačítka Předchozí a Další.](media/navigation2.png)

### <a name="timescale"></a>Časové měřítko

**Časové měřítko** : Změní agregaci časově rozložených dat mezi dny, týdny, měsíci a roky.

![Tlačítko Časové měřítko.](media/navigation3.png)

### <a name="expand"></a>Rozšíření

**Rozšířit** : Vykreslí viditelnou mřížku na celou obrazovku a nabídne tak zobrazení dalších rolí.

![Tlačítko Rozbalit.](media/navigation4.png)

### <a name="time-phase-by"></a>Časově uspořádat podle

**Časově uspořádat podle** : Aktualizujte seskupení řádků v mřížce tak, aby odráželo odhady nákladů pro odhady prodejů. Tento ovládací prvek se vztahuje také na skript odhadu a sledovací mřížku.

![Tlačítko Časově uspořádat podle.](media/navigation0.png)

### <a name="add-column"></a>Přidat sloupec

**Přidat sloupec** : Umožňuje uživateli definovat viditelné sloupce v mřížce. Do mřížek ve formuláři **Plánování projektu** lze přidat pouze předem připravené sloupce.

![Tlačítko Přidat sloupec.](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]