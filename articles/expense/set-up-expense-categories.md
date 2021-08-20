---
title: Nastavení kategorií výdajů
description: Toto téma poskytuje informace o tom, jak nastavit kategorie výdajů a sdílené kategorie pro sestavy výdajů.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8f5b1a5d069b8d73051406369ecba2c4547eaa38e0d5bde2e34f52c5b7b724bd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993098"
---
# <a name="set-up-expense-categories"></a>Nastavení kategorií výdajů

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Když zaměstnanci vytvářejí sestavy výdajů, musí být každý zaznamenaný výdaj přidružen ke kategorii výdajů. Kategorie výdajů jsou odvozeny ze sdílených kategorií, které lze sdílet mezi právnickými osobami ve vaší organizaci. V závislosti na tom, jak je vaše organizace definována, lze tyto kategorie výdajů sdílet také v jiných oblastech. Na základě definice vaší organizace a pokynů od implementačního týmu musíte určit, zda kategorie, které se používají ve správě výdajů, budou použity pouze ve správě výdajů, nebo zda by měly být sdíleny v jiných oblastech.

> [!NOTE]
> Tyto kategorie lze sdílet mezi moduly Řízení a účetnictví projektů a Správa výdajů, nebo mezi moduly Řízení a účetnictví projektů a Výroba. Nelze je však sdílet mezi moduly Správa výdajů a Výroba.

Než budete moci zahájit proces instalace, je třeba učinit následující rozhodnutí pro každou kategorii výdajů:

- Jaká je kategorie výdajů? Mezi příklady patří kategorie letů, hotelů nebo najetých kilometrů.
- Lze kategorii výdajů použít také v modulu Řízení a účetnictví projektů? Když to jde, musíte rovněž učinit následující rozhodnutí:

    - Které nákladové účty budou použity pro následující výdaje?

        - Náklady
        - Přidělení mezd
        - Hodnota nákladů nedokončené práce
        - Náklady – položka
        - Nedokončená výroba – hodnota nákladů – položka
        - Časově rozlišená ztráta
        - NV – časově rozlišená ztráta

    - Které účty výnosů budou použity pro následující zdroje výnosů?

        - Fakturované výnosy
        - Časově rozlišené výnosy – hodnota prodeje
        - NV – prodej
        - Časově rozlišené výnosy – výroba
        - NV – výroba
        - Časově rozlišené výnosy – zisk
        - NV – zisk
        - Časově rozlišené výnosy – předplatné
        - NV – předplatné

- Jaký je typ výdajů?
- Jaký je výchozí způsob platby pro kategorii výdajů?
- Musí být výdaje v kategorii výdajů rozepsány?
- Jaký je hlavní výchozí účet pro kategorii výdajů?
- Jaká je výchozí skupina daně z prodeje zboží pro kategorii výdajů?
- Jsou pro kategorii výdajů povoleny další způsoby platby? Pokud ano, které to jsou?
- Existují v této kategorii výdajů podkategorie? Když existují podkategorie, musíte rovněž učinit následující rozhodnutí:

    - Jsou některé z podkategorií vyloučeny z vymáhání daní?
    - Jaká je skupina daně z prodeje zboží u podkategorií?


[!INCLUDE[footer-include](../includes/footer-banner.md)]