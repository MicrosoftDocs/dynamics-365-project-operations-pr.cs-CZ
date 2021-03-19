---
title: Více schvalovatelů na sestavě výdajů
description: Toto téma poskytuje informace o výkazech výdajů, které vyžadují schválení více osobami.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fbe1c93c5359a6be493e3c4e1b27b06dbb48002
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271705"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Více schvalovatelů na sestavě výdajů

V závislosti na zásadách schvalování výdajů vaší organizace bude muset schválit sestavu výdajů odeslanou zaměstnancem více než jedna osoba. Když nastavíte proces pracovního postupu pro schválení výkazu výdajů, můžete přidat prvky pracovního postupu, které zahrnují úkoly nebo kroky pro jednoho nebo více schvalovatelů výkazu výdajů. Můžete například požadovat, aby všechny výkazy výdajů byly schváleny nejprve manažerem zaměstnance, který výdaj odeslal, a poté koordinátorem závazků.

Pokud se rozhodnete vyžadovat více schvalovatelů výkazů výdajů, můžete přidat prvky pracovního toku některým z následujících způsobů:

- Přidejte jeden prvek schvalování, který má jeden krok. Krok může například vyžadovat, aby byl výkaz výdajů přiřazen skupině uživatelů a aby byl schválen 50 procenty členů skupiny uživatelů.
- Přidejte jeden prvek schvalování, který má více kroků. Například prvek schvalování může mít následující kroky:

    1. Manažer zaměstnance, který odeslal výkaz výdajů, ho schválí.
    2. Úředník závazků ověří účtenky a položky výkazu výdajů.
    3. Vlastník rozpočtu schválí výkaz výdajů.

- Přidejte několik prvků schvalování, z nichž každý má jeden krok. Můžete například přidat samostatný prvek schválení pro každý z následujících kroků:

    1. Manažer zaměstnance schválí výkaz výdajů.
    2. Vlastník rozpočtu schválí výkaz výdajů.


[!INCLUDE[footer-include](../includes/footer-banner.md)]