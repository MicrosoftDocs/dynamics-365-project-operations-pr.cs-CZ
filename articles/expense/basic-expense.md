---
title: Položka výdajů (omezené)
description: Tento téma poskytuje informace o tom, jak pracovat se zadáním výdajů v omezeném nasazení.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d87094882751f0751a8d9d539fa4cdcfc6b7b0d7
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590938"
---
# <a name="expense-entry-lite"></a>Položka výdajů (omezené)

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Základní nebo omezená správa nákladů je schopnost zaznamenávat jednoduché výdaje. Můžete zaznamenat výdaje proti projektu a poté je schvalovatel projektu zkontroluje a schválí.

Další informace o možnostech výdajů v Dynamics 365 Project Operations viz [Přehled výdajů](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Zachyťte základní výdaje

Můžete zachytit své výdaje, abyste je mohli předat schvalovateli.

1. přejděte na **Výdaje** a vyberte **Nový**.
2. Na stránce **Nový výdaj** zadejte požadované informace o výdajích a poté vyberte **Uložit**.

## <a name="submit-a-basic-expense"></a>Odešlete základní výdaje

Jakmile dokončíte získávání všech svých výdajů a jste připraveni je schválit, musíte je odeslat.

1. přejděte na **Výdaje** a vyberte výdaj. Nebo vyberte všechny výdaje pomocí zaškrtávacího políčka v záhlaví.
2. Vyberte položku **Odeslat**. Systém zpracuje vybrané položky a poté vytvoří žádosti o schválení výdajů.

## <a name="add-an-attachment"></a>Přidat přílohu

Možná budete muset poskytnout schvalovateli další dokumentaci o svých výdajích. Na časové ose záznamu výdajů můžete připojit potvrzení. Vyberte **Upravit** a v sekci **Časová osa** vyberte ikonu kancelářské sponky a přiložte potvrzení.

## <a name="recall-a-basic-expense"></a>Odvolání základního výdaje

Pokud omylem zadáte výdaj, můžete jej odvolat. Čas potřebný k vyvolání položky výdajů závisí na fázi jejího schválení.  Pokud schvalovatel dosud neschválil záznam, může k odvolání dojít okamžitě. Pokud však již byl záznam schválen, je schvalovatel požádán o schválení odvolání a zrušení transakcí.

1. Přejděte na **Výdaje** a poté v seznamu výdajů vyberte výdaj, který chcete odvolat.
2. Vyberte **Odvolat**. Pokud položka výdajů ještě nebyla schválena, systém ji okamžitě vyvolá. Pokud položka výdajů již byla schválena, je vytvořen požadavek na odvolání, který informuje schvalovatele, že chcete výdaj zrušit. Schvalovatel poté potvrdí, že lze provést zrušení, a záznam bude vrácen.

## <a name="delete-a-basic-expense"></a>Odstranit základní výdaje

Výdaje, které dosud nebyly odeslány, lze smazat. Chcete-li odstranit již odeslaný výdaj, musíte jej nejprve odvolat.

## <a name="see-also"></a>Viz také

- [Přehled schválení](../approvals/approvals-overview.md)
