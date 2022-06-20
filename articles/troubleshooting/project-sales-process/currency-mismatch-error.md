---
title: Chyba neshody měn
description: Tento článek poskytuje informace o odstraňování chyby nesouladu měn, ke které dochází při ukládání určitých typů záznamů.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914716"
---
# <a name="currency-mismatch-error"></a>Chyba neshody měn 

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Když uložíte projekt, smlouvu, nabídku nebo rezervovatelný zdroj, může se někdy zobrazit chyba **Měna vlastnící společnosti neodpovídá měně smluvní jednotky. Vyberte jinou vlastnící společnost nebo smluvní jednotku, abyste mohli pokračovat**. Důvodem je nesoulad mezi měnou smluvní jednotky pro záznam a měnou vlastnící společnosti.


## <a name="resolution"></a>Rozlišení

Tento problém lze obejít takto:
- Ověřte měnu smluvní jednotky pro tento záznam. Měnu můžete zobrazit otevřením záznamu organizační jednotky a ověřením hodnoty na kartě **Všeobecné** v poli **Měna**.
- Ověřte měnu vlastnící společnosti. Měnu můžete zobrazit tak, že přejdete na část **Související** > **Hlavní knihy** ve firemním záznamu. Poklepejte na záznam hlavní knihy, který je přidružen ke společnosti, a ověřte hodnotu na kartě **Obecné** v poli **Účetní měna**.

Pokud se měna nastavená ve smluvní jednotce a záznam hlavní knihy neshodují, upravte konfiguraci nebo vyberte jiné hodnoty při ukládání záznamu. Systém vyžaduje, aby se tyto záznamy shodovaly, aby byly zajištěny správné mezipodnikové fakturační toky. Další informace o mezipodnikových konfiguracích najdete v článku [Vytváření mezipodnikových transakcí](../../project-accounting/create-intercompany-transactions.md).

Pokud záznam společnosti nemá žádný přidružený záznam hlavní knihy, znamená to, že při nastavování prostředí chybí konfigurace. Konfigurace musí být opravena správcem systému. Správce systému musí přejít do dialogu **Konfigurace duálního zápisu** a zastavit a restartovat **Mapu duálního zápisu do hlavních knih** s počáteční synchronizací této mapy a jejími předpoklady. Další informace viz [Verze map duálního zápisu Project Operations](../../environment/resource-dual-write-maps.md).
