---
title: Vyúčtování výdajů a více schvalovatelů
description: Toto téma poskytuje informace o výkazech výdajů, které vyžadují schválení více než jednou osobou.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9b9826c89e9deb870adb053f82bd049906f56052
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276520"
---
# <a name="expense-reports-and-multiple-approvers"></a>Vyúčtování výdajů a více schvalovatelů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

V závislosti na zásadách schvalování výdajů vaší organizace bude muset schválit odeslaný výkaz více než jedna osoba. Když nastavíte proces pracovního postupu pro schválení výkazu výdajů, můžete přidat prvky pracovního postupu, které zahrnují úkoly nebo kroky pro jednoho nebo více schvalovatelů výkazu výdajů. Můžete například požadovat, aby všechny výkazy výdajů byly schváleny dvěma samostatnými osobami, manažerem zaměstnance, který výdaj odeslal, a koordinátorem závazků.

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