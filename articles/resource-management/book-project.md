---
title: Rezervace na projekt
description: Toto téma obsahuje informace o rezervaci zdroje na projekt.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907997"
---
# <a name="book-to-a-project"></a>Rezervace na projekt

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Jsou chvíle, kdy manažer projektu nebo správce zdrojů bude muset přidělit prostředek projektu, aniž by byl definován konkrétní požadavek od člena obecného týmu. Tohoto lze dosáhnout třemi způsoby.

- Rezervace z mřížky člena týmu
- Rezervace z plánovací vývěsky
- Rezervace z formuláře **Projekt**

## <a name="book-from-the-team-member-grid"></a>Rezervace z mřížky člena týmu

Pokud vaše organizace pracuje v hybridním režimu přidělování prostředků, může projektový manažer rezervovat prostředek přímo do projektu provedením následujících kroků.

1. V projektu přejděte do mřížky členů týmu a vyberte **Nový**.
2. Definujte název pozice a roli zdroje.
3. Vyberte rezervovatelný zdroj z dostupného vyhledávání.
4. Poté, co vyberete prostředek, definujte následující informace o poli pro rezervaci prostředku:

    - Počáteční datum
    - Datum dokončení
    - Metoda přidělení
    - Hodiny, pokud je to relevantní
    - Schvalovatel projektu

6. Zvolte **Uložit a zavřít**

## <a name="book-from-the-schedule-board"></a>Rezervace z plánovací vývěsky

Když správce zdrojů potřebuje rezervovat zdroj přímo do projektu, může použít plánovací tabuli a požadavek projektu. Požadavek na projekt je požadavek na zdroj, který je vždy k dispozici a lze jej rezervovat. Chcete-li provést rezervaci přímo do formuláře na plánovací vývěsce, postupujte dle následujících kroků.

1. Přejděte na plánovací vývěsku a na levé stránce vyfiltrujte zdroje, které pro daný požadavek zvažujete.
2. Ve spodním podokně vyberte kartu **Projekt** pro zobrazení seznamu požadavků projektu.
3. Přetáhněte požadavek na prostředek a definujte následující informace:

    - Počáteční datum
    - Datum dokončení
    - Stav rezervace
    - Metoda rezervace
    - Trvání

## <a name="book-from-the-project-form"></a>Rezervace z formuláře Projekt

Jako projektový manažer možná budete muset rezervovat zdroj na projekt, ale znáte pouze kritéria, nikoli název zdroje. Chcete-li použít asistenta plánování k vyhledání prostředku na základě všech dostupných atributů prostředku, proveďte následující kroky. 

1. Přejděte na projekt a vyberte **Rezervovat** pro otevření pomocníka plánování.
2. Pomocí filtrů na levé straně pomocníka plánování zúžte kritéria a vyberte **Vyhledávání.**
3. Na základě prostředků vrácených ve výsledcích si můžete rezervovat zdroj.

> [!NOTE]
> Tato metoda nevytváří žádné rezervace pro prostředek. Místo toho přidá zdroj do týmu. Poté, co byl člen týmu přidán do projektu, může vedoucí projektu pomocí udržování rezervací nebo rozšíření rezervací přidat požadované rezervace do zdroje.
