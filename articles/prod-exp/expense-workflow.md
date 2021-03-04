---
title: Pracovní postup správy výdajů
description: Tento téma vysvětluje, jak můžete použít systém pracovního postupu v Microsoft Dynamics 365 Finance k nastavení procesu kontroly pro sestavy výdajů ve správě výdajů.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbee90450749c89f643d96e4d41a387c45e9abc5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960554"
---
# <a name="expense-management-workflow"></a>Pracovní postup správy výdajů

Systém pracovního postupu v Microsoft můžete použít k nastavení procesu kontroly pro sestavy výdajů ve správě výdajů. Můžete nastavit pracovní postup, který k určení toho, kdo schvaluje sestavy výdajů, používá následující kritéria:

- Hierarchie podřízenosti zaměstnanců a předdefinované limity schválení
- Víceúrovňové schválení, které podporuje prozatímní schvalovatele a konečného schvalovatele
- Finanční dimenze a odpovědnost za projekt
- Přiřazení konkrétním uživatelům nebo skupinám uživatelů

Je možné vytvořit schválení pracovního postupu pro sestavy výdajů, cestovní požadavky, zálohy v hotovosti a vymáhání daně z přidané hodnoty (DPH).

**Příklad**

Následující proces je příkladem pracovního postupu správy výdajů pro sestavu výdajů.

1. Zaměstnanec vytvoří a uloží sestavu výdajů.
2. Zaměstnance odešle sestavu výdajů ke schválení. Schvalovatel je identifikován na základě pravidel, která byla definována při nastavení pracovního postupu.
3. Schvalovatel obdrží oznámení, že sestava výdajů je připraven ke schválení. Schvalovatel zkontroluje sestava výdajů a ověří, zda jsou splněny následující podmínky:

    - Výdaje neporušují žádné zásady výdajů. Pokud výdaj porušuje zásady, schvalovatel ověří, zda sestava výdajů obsahuje platné obchodní odůvodnění.
    - Elektronické účtenky jsou připojeny k sestavě výdajů.

4. Schvalovatel sestavu výdajů schválí.
5. Sestava výdajů je přiřazena koordinátorovi závazků k zaúčtování.
6. Dojde k jednomu z následujících kroků v závislosti na tom, zda je nakonfigurováno automatické zaúčtování:

    - Pokud je nakonfigurováno automatické zaúčtování, je zpracována sestava výdajů k platbě a je aktualizován stav sestav výdajů.
    - Pokud automatické účtování není nakonfigurováno, koordinátor závazků ověří, zda byly odeslány všechny původní příjmy a zda jsou příjmy v souladu s výdaji v sestavě výdajů. Všechny daňové zásady, které jsou zadány v sestavě výdajů, musí být také ověřeny jako správné.

Po ověření těchto požadavků se sestava výdajů zaúčtuje.

Po zaúčtování sestavy výdajů je platba pro sestavu výdajů autorizována a zaměstnanci jsou proplaceny peníze.


[!INCLUDE[footer-include](../includes/footer-banner.md)]