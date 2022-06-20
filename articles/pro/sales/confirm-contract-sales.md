---
title: Potvrzení projektové smlouvy
description: Tento článek poskytuje informace o tom, jak potvrdit smlouvu v Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e92dc42c4ff6bdc40c479511c80d3e500df781a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929988"
---
# <a name="confirm-a-project-contract"></a>Potvrzení projektové smlouvy

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Smlouva o projektu v Dynamics 365 Project Operations může být aktivní z důvodu **Potvrzeno**, nebo uzavřena z důvodu **Ztracená**. Když potvrdíte smlouvu o projektu, stav se aktualizuje z **Návrh** na **Aktivní** a důvod stavu je **Potvrzeno**. Aktivní nebo uzavřenou smlouvu nelze upravit ani znovu otevřít. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Finanční dopad potvrzení smlouvy o projektu

Po potvrzení smlouvy projektu aplikace přepočítá náklady obrácením starších údajů o nákladech a opětovným vytvořením nových údajů o nákladech. Nové náklady jsou poté zpracovány na základě metody fakturace příslušného řádku smlouvy projektu. Pokud skutečné náklady odkazují na řádek smlouvy o čase a materiálu, aplikace automaticky znovu vytvoří odpovídající nevyfakturované skutečné prodejní údaje. Pokud skutečné náklady odkazují na řádek smlouvy s pevnou cenou, aplikace zastaví přepracování skutečných nákladů.

Nepřekročitelné limity, nastavení poplatků a ceny a nákladování na skutečných údajích jsou vyhodnocovány a poté aktualizovány jako součást procesu potvrzení.

## <a name="close-a-project-contract-as-lost"></a>Uzavření smlouvy projektu jako ztracené

Když uzavřete smlouvu projektu jako ztracenou, stav smlouvy se aktualizuje na **Uzavřeno** a důvod stavu je **Ztraceno**. Smlouva o projektu se stane jen pro čtení. Před dokončením změn je k dispozici potvrzovací dialog, protože nemůžete znovu otevřít uzavřenou smlouvu o projektu.

Pokud smlouva projektu, která je uzavřena jako ztracená, odkazuje na projekt na svých řádcích, je tento projekt také označen jako uzavřený. Veškeré rezervace zdrojů od daného dne budou zrušeny. Jakékoli nevyfakturované prodejní údaje o projektové smlouvě, které ještě nejsou na faktuře, budou stornovány.

> [!NOTE]
> V Dynamics 365 Project Operations uzavření smlouvy o projektu jako ztracené nebude mít vliv na tento stav přidružené příležitosti. Příležitost zůstane otevřená a musí být ručně uzavřena.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]