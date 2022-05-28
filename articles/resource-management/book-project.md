---
title: Rezervace na projekt
description: Toto téma obsahuje informace o rezervaci zdroje na projekt.
author: ruhercul
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b47ae8cb38be6d29804aec8b069e6a8aec0ffb70
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591352"
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
    - Duration
   
   > [!NOTE]
   > V současné době Dynamics 365 Project Operations nepodporuje plánovací vývěsku.   

## <a name="book-from-the-project-form"></a>Rezervace z formuláře Projekt

Jako projektový manažer možná budete muset rezervovat zdroj na projekt, ale znáte pouze kritéria, nikoli název zdroje. Chcete-li použít asistenta plánování k vyhledání prostředku na základě všech dostupných atributů prostředku, proveďte následující kroky. 

1. Přejděte na projekt a vyberte **Rezervovat** pro otevření pomocníka plánování.
2. Pomocí filtrů na levé straně pomocníka plánování zúžte kritéria a vyberte **Vyhledávání.**
3. Na základě prostředků vrácených ve výsledcích si můžete rezervovat zdroj.

> [!NOTE]
> Tato metoda nevytváří žádné rezervace pro prostředek. Místo toho přidá zdroj do týmu. Poté, co byl člen týmu přidán do projektu, může vedoucí projektu pomocí udržování rezervací nebo rozšíření rezervací přidat požadované rezervace do zdroje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
