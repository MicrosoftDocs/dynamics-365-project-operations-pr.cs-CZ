---
title: Zaúčtování sestav výdajů
description: Tento článek vysvětluje, jak zaúčtovat sestavy výdajů.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524861"
---
# <a name="post-expense-reports"></a>Zaúčtování sestav výdajů

Jakmile bude sestava výdajů schválena a přenesena do finančního deníku, může být zaúčtována. Když zaúčtujete sestavu výdajů, budou identifikovány výdaje, které jsou způsobilé k vrácení daně z přidané hodnoty (DPH). Úkol ověřovat a vymáhat platby DPH je přidělen zaměstnanci, který je odpovědný za ověření sestavy výdajů.

Pokud jsou výdaje na sestavě výdajů účtovány jiné společnosti než společnosti, která zaměstnává tohoto zaměstnance, musíte ověřit jak společnost, které tyto výdaje patří, tak společnosti, která je dluží. Příklad: zaměstnanec, který odeslal sestavu o výdajích, pracuje pro společnost DAT, ale účtoval výdaj společnosti DIR. V tomto případě je DAT společnost, které tyto výdaje patří, a DIR je společnost, která je dluží. Po ověření těchto řádků deníku můžete zaúčtovat řádky výdajů do hlavní knihy.

Chcete-li zaúčtovat sestavu výdajů, vyberte na stránce **Schválené sestavy výdajů** sestavu výdajů a poté v podokně akcí vyberte příkaz **Zaúčtovat**.

Je také možné zaúčtovat všechny sestavy výdajů v seznamu současně. Vyberte všechny sestavy výdajů a poté vyberte příkaz **Zaúčtovat**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Povolení funkce Schopnost účtovat výdajový závazek v měně dodavatele pro způsob platby v hotovosti

Funkce **Schopnost účtovat výdajový závazek v měně dodavatele pro způsob platby v hotovosti** umožňuje povolit zaúčtování výkazů výdajů v měně dodavatele pro způsob platby v hotovosti.

V současné době, když odesíláte výdaje v hotovosti, výkazy výdajů jsou účtovány v zúčtovací měně. Kvůli převodu částky mezi měnou transakce, zúčtovací měnou a měnou dodavatele je dodavatelům vyplacena nesprávná částka, pokud datum transakce výdaje a datum skutečné platby mají různé směnné kurzy.

Tato funkce zajistí, že zůstatek dodavatele bude zaznamenán v měně dodavatele při zaúčtování výkazu výdajů.

1. Přejděte na **Pracovní prostory** \> **Správa funkcí**.
2. V seznamu vyhledejte a vyberte funkci **Schopnost účtovat výdajový závazek v měně dodavatele pro způsob platby v hotovosti** a poté vyberte **Povolit**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
