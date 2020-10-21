---
title: Položka výdajů (omezené)
description: Tento téma poskytuje informace o tom, jak pracovat se zadáním výdajů v omezeném nasazení.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965753"
---
# <a name="expense-entry-lite"></a>Položka výdajů (omezené)

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Základní nebo omezená správa nákladů je schopnost zaznamenávat jednoduché výdaje. Můžete zaznamenat výdaje proti projektu a poté je schvalovatel projektu zkontroluje a schválí.

Další informace o možnostech výdajů v Dynamics 365 Project Operations najdete v [Přehledu výdajů](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Zachyťte základní výdaje

Můžete zachytit své výdaje, abyste je mohli předat schvalovateli.

1. přejděte na **Výdaje** a vyberte **Nový**.
2. Na stránce **Nový výdaj** zadejte požadované informace o výdajích a poté vyberte **Uložit**.

## <a name="submit-a-basic-expense"></a>Odešlete základní výdaje

Jakmile dokončíte získávání všech svých výdajů a jste připraveni je schválit, musíte je odeslat.

1. přejděte na **Výdaje** a vyberte výdaj. Nebo vyberte všechny výdaje pomocí zaškrtávacího políčka v záhlaví.
2. Vyberte položku **Odeslat**. Systém zpracuje vybrané položky a poté vytvoří žádosti o schválení výdajů.

## <a name="recall-a-basic-expense"></a>Odvolání základního výdaje

Pokud omylem zadáte výdaj, můžete jej odvolat. Čas potřebný k vyvolání položky výdajů závisí na fázi jejího schválení.  Pokud schvalovatel dosud neschválil záznam, může k odvolání dojít okamžitě. Pokud však již byl záznam schválen, je schvalovatel požádán o schválení odvolání a zrušení transakcí.

1. Přejděte na **Výdaje** a poté v seznamu výdajů vyberte výdaj, který chcete odvolat.
2. Vyberte **Odvolat**. Pokud položka výdajů ještě nebyla schválena, systém ji okamžitě vyvolá. Pokud položka výdajů již byla schválena, je vytvořen požadavek na odvolání, který informuje schvalovatele, že chcete výdaj zrušit. Schvalovatel poté potvrdí, že lze provést zrušení, a záznam bude vrácen.

## <a name="delete-a-basic-expense"></a>Odstranit základní výdaje

Výdaje, které dosud nebyly odeslány, lze smazat. Chcete-li odstranit již odeslaný výdaj, musíte jej nejprve odvolat.

## <a name="see-also"></a>Viz také

- [Přehled schválení](../approvals/approvals-overview.md)
