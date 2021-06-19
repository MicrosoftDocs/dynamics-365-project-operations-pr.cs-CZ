---
title: Finanční odhady pro materiály na projektech
description: Tento téma poskytuje informace o definování nebo odhadování projektových materiálů.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 768da6adb83b4593a227f60182179b3036f4c040
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002678"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Finanční odhady pro materiály na projektech

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Dynamics 365 Project Operations umožňuje projektovým manažerům definovat náklady na materiál na základě projektu pro každý projekt nebo úkol. Každý odhad materiálu může být spojen s konkrétním úkolem projektu. Výdaje jsou rozděleny do různých kategorií výdajů, které jsou definovány na organizační úrovni. Ceny a kalkulace pro každou kategorii výdajů jsou definovány v ceníku. 

Chcete-li zobrazit, přidat nebo odstranit odhad materiálu projektu, proveďte následující kroky.

1. Přejděte na **Projekty** a vyberte projekt, který chcete aktualizovat.
2. Na kartě **Odhady materiálu** se zobrazí seznam odhadů materiálu projektu.
3. Vyberte **Nový odhad materiálu** k vytvoření nového odhadu materiálu. Nebo vyberte odhad materiálu, který chcete odstranit, a poté vyberte **Odstranit odhad materiálu**.

Následující tabulka poskytuje informace o polích na stránce **Řádek odhadu materiálu** v projektu. 

| **Pole** | **Popis** | **Dopad na příjem dat** |
| --- | --- | --- |
| Úkol | Seznam úkolů v projektu. To zahrnuje souhrnné úkoly a úkoly v uzlech typu list. | Když vyberete úkol pro řádek odhadu materiálu, budou ovlivněny odhadované náklady na materiál a odhadovaný prodej materiálu pro úkol. Pokud je toto pole prázdné, je odhad materiálu sledován a shrnut pouze na úrovni projektu. |
| Vybrat produkt |  Můžete určit, zda je tento řádek odhadu pro existující (katalogový) produkt, nebo zapsaný produkt. | Toto pole určuje, zda vyberete produkt z katalogu, nebo produkt, který není v katalogu. |
| Produkt | ID produktu z katalogu produktů. Když vyberete ID produktu, hodnota v poli **Vybrat produkt** se automaticky aktualizuje na **Stávající produkt**. ID se používá k načtení nákladů a prodejních cen z ceníku. | Neexistuje žádný následný dopad na toto pole. |
| Popis produktu nezahrnutého do katalogu | Textové pole pro zadání názvu produktu. Toto pole je k dispozici pouze, když vyberete produkt **nezahrnutý do katalogu** v poli **Vybrat produkt**.| Neexistuje žádný následný dopad na toto pole. |
| Počáteční datum | Předpovídané datum, kdy se předpokládá použití materiálu. | Neexistuje žádný následný dopad na toto pole. |
| Skupina jednotek | Výchozí hodnota v tomto poli pochází z výchozí skupiny jednotek na katalogovém produktu. Toto pole můžete aktualizovat a vybrat jinou skupinu jednotek. | Neexistuje žádný následný dopad na toto pole. |
| Jednotka | Hodnota v tomto poli pochází z výchozí jednotky vybraného produktu. Toto pole můžete aktualizovat a vybrat jinou jednotku. | Změna jednotky má za následek jinou výchozí jednotkovou cenu a náklad. |
| Množství | Odhadované množství produktu, které bude použito v projektu. | Neexistuje žádný následný dopad na toto pole. |
| Jednotkové náklady | Jednotkové náklady na vybraný produkt a kombinace jednotek stanovené v příslušném ceníku nákladů. | Jednotkové náklady se vždy zobrazují v měně nákladů projektu. Pokud v ceníku neexistují jednotkové náklady pro kombinaci produktu a jednotky, jednotkové náklady se standardně nastaví na 0,00. |
| Cena za jednotku | Cena vybraného produktu a kombinace jednotek stanovené v příslušném ceníku prodeje. | Jednotková cena se vždy zobrazuje v měně prodeje projektu. Pokud v ceníku neexistují jednotková cena pro kombinaci produktu a jednotky, jednotková cena se standardně nastaví na 0,00.|
| Celkové náklady | Částka nákladů, která se počítá jako množství \* jednotková cena.| Částka nákladů se vždy zobrazuje v měně nákladů projektu. |
| Prodej celkem | Částka prodeje, která se počítá jako množství \* jednotková cena. | Částka prodeje se vždy zobrazuje v měně prodeje projektu. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
