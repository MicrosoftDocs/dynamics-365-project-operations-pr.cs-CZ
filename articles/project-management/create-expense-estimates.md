---
title: Finanční odhady pro výdaje na projektech
description: Tento téma poskytuje informace o definování nebo odhadu nákladů na projekt.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c14dc31d666d0e0d026cf9cddfa1e78dee40f717
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589464"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Finanční odhady pro výdaje na projektech
_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Dynamics 365 Project Operations umožňuje projektovým manažerům definovat výdaje na základě projektu pro každý projekt nebo úkol. Každá položka výdajů může být spojena s konkrétním úkolem projektu. Výdaje jsou rozděleny do různých kategorií výdajů, které jsou definovány na organizační úrovni. Ceny a kalkulace pro každou kategorii výdajů jsou definovány v ceníku. 

Chcete-li zobrazit, přidat nebo odstranit náklady na projekt, proveďte následující kroky.

1. Přejděte na **Projekty** a vyberte projekt, na kterém chcete pracovat.
2. Vyberte kartu **Odhady projektu** a zobrazte seznam výdajů projektu.
3. Vyberte **Nový výdaj**, chcete-li přidat výdaj. Nebo vyberte výdaj, který chcete odstranit, a poté vyberte **Smazat výdaj**.

Následující tabulka poskytuje informace o polích na stránce **Řádek odhadu výdajů** v projektu. 

| **Pole** | **Popis** | **Dopad na příjem dat** |
| --- | --- | --- |
| Úkol | Seznam úkolů v projektu. To zahrnuje souhrnné úkoly a úkoly v uzlech typu list. | Výběr úkolu pro řádek odhadu výdajů ovlivní odhadované náklady a prodej odhadovaných výdajů na úkol. Pokud je toto pole prázdné, je odhad výdajů je sledován a shrnut pouze na úrovni projektu. |
| Kategorie | Seznam kategorií transakcí, které mají v aplikaci propojené kategorie výdajů. | Výběr kategorie zvyšuje ceny a náklady na řádku odhadu výdajů. |
| Počáteční datum | Předpokládané datum, kdy dojde k výdaji. | Neexistuje žádný následný dopad na toto pole. |
| Skupina jednotek | Výchozí hodnota v tomto poli pochází ze skupiny jednotek, která je nastavena jako výchozí na vybrané kategorii. Toto pole můžete aktualizovat a vybrat jinou skupinu jednotek. | Neexistuje žádný následný dopad na toto pole. |
| Jednotka | Výchozí hodnota v tomto poli je výchozí jednotka vybrané kategorie. Toto pole můžete aktualizovat a vybrat jinou jednotku. | Změna jednotky má za následek jinou výchozí jednotkovou cenu a náklad. |
| Množství | Množství odhadovaných výdajů, které vám vzniknou. | Neexistuje žádný následný dopad na toto pole. |
| Jednotkové náklady | Jednotkové náklady na vybranou kombinaci kategorie a jednotky stanovené v příslušném ceníku nákladů | Jednotkové náklady se vždy zobrazují v měně nákladů projektu. |
| Cena za jednotku | Cena vybrané kombinace kategorie jednotky stanovené v příslušném ceníku prodeje. | Jednotková cena se vždy zobrazuje v měně prodeje projektu. |
| Celkové náklady | Částka nákladů, která se počítá jako množství \* jednotková cena.| Částka nákladů se vždy zobrazuje v měně nákladů projektu. |
| Prodej celkem | Částka prodeje, která se počítá jako množství \* jednotková cena. | Částka prodeje se vždy zobrazuje v měně prodeje projektu. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
