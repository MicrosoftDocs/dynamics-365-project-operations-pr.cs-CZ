---
title: Finanční odhady pro čas zdroje na projektech
description: Tento téma poskytuje informace o tom, jak se počítají finanční odhady pro čas.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: aab5c11a7dc23331c935403a4f96ec7197ec1572
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592546"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Finanční odhady pro čas zdroje na projektech

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Finanční odhady pro čas se počítají na základě tří faktorů: 

- Typ obecného nebo pojmenovaného člena týmu přiřazeného ke každému úkolu uzlu typu list v projektovém plánu. 
- Druh nebo složitost práce.
- Rozložení úsilí pro přiřazení zdroje k úkolu. 

První dva faktory ovlivňují jednotkové náklady nebo fakturační sazbu přiřazení zdroje. Jednotková cena nebo fakturační sazba přiřazení zdroje je určena atributy přiřazeného zdroje. Mezi tyto atributy patří organizační jednotka, do které prostředek patří, a standardní role prostředku. Ke zdroji můžete také přidat vlastní atributy relevantní pro vaše podnikání, jako je standardní název nebo úroveň zkušeností, a nechat je ovlivnit jednotkové náklady nebo fakturační sazbu úkolu.
Kromě atributů zdroje mohou také atributy práce, jako je například úkol, ovlivnit jednotkovou fakturační sazbu nebo sazbu nákladů úkolu. Například když jsou určité úkoly složitější, přiřazení zdroje k těmto konkrétním úkolům má za následek vyšší jednotkovou cenu nebo fakturační sazbu než u úkolů, které jsou méně složité.   

Třetí faktor udává počet hodin při této sazbě. V případech, kdy úkol pokrývá dvě cenová období, je pravděpodobné, že první část přiřazení zdroje pro tento úkol je nákladově a cenově odlišná než druhá část přiřazení. Odhad úsilí u každého přiřazení zdroje je komplexní hodnota uložená s denním rozložením úsilí za den.

Podrobné pokyny, jak nastavit vlastní atributy práce a zdrojů, jako jsou dimenze cen a kalkulace, najdete v části [Přehled cenových dimenzí](../pricing-costing/pricing-dimensions-overview.md).

Finanční odhad každého přiřazení zdroje se počítá jako **sazba / hod pro přiřazení vynásobená počtem hodin.**  Podobně jako odhad úsilí je finanční odhad nákladů a výnosů pro každé přiřazení zdrojů komplexní hodnota uložená s denním rozdělením peněžní částky za den. 

## <a name="summarizing-financial-estimates-for-time"></a>Shrnutí finančních odhadů za čas
Finanční odhad pro čas u úkolu uzlu typu list je součet finančních odhadů pro všechna přiřazení zdrojů pro danou úlohu.

Finanční odhad pro čas u souhrnného nebo nadřazeného úkolu je součet finančních odhadů pro všechny podřízené úkoly. Toto jsou odhadované náklady práce na projektu. 

![Odhady zdrojů.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Výchozí nákladová cena a měna nákladů

Výchozí nákladová cena pochází z ceníků připojených ke smluvní jednotce projektu. Měna nákladů projektu je vždy měna smluvní jednotky projektu. U přiřazení zdroje je finanční odhad nákladů uložen v měně nákladů projektu. Někdy se měna, ve které je v ceníku nastavena sazba nákladů, liší od projektové měny nákladů. V těchto případech aplikace převede měnu, ve které je nastavena cena nákladů, na projektovou měnu. V mřížce **Odhady** jsou všechny odhady nákladů jsou zobrazeny a shrnuty v projektové měně nákladů. 

## <a name="default-bill-rate-and-sales-currency"></a>Výchozí fakturační sazba a měna prodeje

Výchozí prodejní cena pochází z projektových ceníků připojených k souvisejícím projektové smlouvě, pokud je dohoda vyhrána, nebo ze související projektové nabídky, pokud je dohoda stále ve fázi předprodeje. Měna prodejů projektu je vždy měna projektové nabídky nebo projektové smlouvy. U přiřazení zdroje je finanční odhad prodejů uložen v měně projektových prodejů. Na rozdíl od nákladů se prodejní cena nastavená v ceníku nikdy nemůže lišit od prodejní měny projektu. Neexistuje scénář, kdy je nutná konverze měny. V mřížce **Odhady** jsou všechny odhady prodejů zobrazeny a shrnuty v projektové měně prodejů. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
