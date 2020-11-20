---
title: Hotovostní záloha
description: Toto téma poskytuje informace o hotovostních zálohách.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c5839fbdab58903555936324139b76f4c94b6c35
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122741"
---
# <a name="cash-advance"></a>Hotovostní záloha

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Hotovostní záloha umožňuje zaměstnancům půjčit si peníze od jejich společnosti před vznikem jakýchkoli výdajů. Když je požadovaná hotovostní záloha schválena a zaplacena, může zaměstnanec použít peníze na výdaje na podnikání, které jim pravděpodobně vzniknou. 

## <a name="create-and-submit-a-cash-advance-request"></a>Vytvořte a odešlete požadavek na hotovostní zálohu

1. V **Moje výdaje** vyberte **Hotovostní zálohy** > **Nová** k vytvoření nové hotovostní zálohy. 
2. Na stránce **Nová žádost o hotovostní zálohu** zadejte účel výdajů a vyberte místo, kde vzniknou výdaje.
3. Zadejte požadovanou částku a měnu a poté vyberte **Uložit**. 
4. Až budete připraveni podat žádost o hotovostní zálohu, na stránce **Žádost o hotovostní zálohu** vyberte **Pracovní postup** > **Odeslat**.

## <a name="modify-a-cash-advance-request"></a>Upravte požadavek na hotovostní zálohu

Pokud žádost o hotovostní zálohu nebyla předložena ke schválení, můžete ji upravit.

1. V **Moje výdaje: hotovostní zálohy** vyhledejte a vyberte hotovostní zálohu, kterou chcete upravit.
2. Vyberte **Upravit** a proveďte nezbytné změny v požadavku na hotovostní zálohu. 
3. Zvolte **Uložit a zavřít**.


## <a name="view-cash-advance-requests"></a>Zobrazit požadavky na hotovostní zálohu
Můžete zkontrolovat seznam všech peněžních záloh, které jsou v konceptu, odeslány, zkontrolovány nebo vyplaceny v **Moje výdaje: hotovostní zálohy**. 

## <a name="approve-cash-advance-requests"></a>Schválit požadavky na hotovostní zálohu

Manažeři nebo uživatelé nakonfigurovaní jako schvalovatelé v pracovním postupu budou moci schválit hotovostní zálohy, které jim byly předloženy ke kontrole. 

1. Chcete-li schválit hotovostní zálohu, v **Zpracovat hotovostní zálohy** vyberte **Hotovostní zálohy k mojí kontrole**.
2. Vyberte hotovostní zálohu, kterou potřebujete zkontrolovat, a vyberte **Schválit**.  

## <a name="pay-cash-advances"></a>Vyplacení hotovostních záloh 
Následující postup obvykle dokončí účetní nebo uživatel s účetními oprávněními.

1. Chcete-li zaúčtovat schválené hotovostní zálohy, vyberte **Schválené zálohy v hotovosti** a potom vyberte **Zaplatit a převést**.  
2. Uveďte podrobnosti deníku o hotovostních zálohách a poté vyberte **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Odešlete zprávu o výdajích proti vyplaceným hotovostním zálohám 

Když vytvoříte a odešlete zprávu o výdajích k hotovostní záloze, kterou jste již obdrželi, budou náklady automaticky upraveny oproti této záloze. Pokud je vaše hotovostní záloha větší než vyúčtovaná částka, musíte zůstatek společnosti vrátit pomocí kategorie výdajů **Návrat hotovosti**. Pokud je hotovostní záloha zaplacená společností nižší než částka, kterou jste zaúčtovali, společnost vám musí zůstatek uhradit. 

### <a name="example"></a>Příklad
Plánujete cestovat na konferenci ze Seattlu do New Yorku. Vytvoříte požadavek na hotovostní zálohu na 3000,00 USD, protože odhadujete, že náklady na konferenční letenku, letenky, hotel, stravu a taxi budou přibližně v této výši. Nedostanete zálohu, dokud váš nadřízený tuto žádost neschválí. Poté, co ji váš manažer schválí, bude požadovaná hotovostní záloha vyplacena jako 3000,00 USD na váš bankovní účet. Poté se zúčastníte konference. Po dokončení cesty zjistíte, že celkové výdaje byly pouze 2790,00 USD. Vyberte **Hotovost** v poli **Způsob platby** a odešle výdaje 2790,00 USD. Odeslaná částka výdajů se automaticky upraví proti hotovostní záloze 3000,00 USD, která vám byla zapůjčena. Nyní dlužíte společnosti zůstatek 210,00 USD (3000,00-2790,00), který můžete společnosti vrátit pomocí kategorie výdajů **Vrátit hotovost**. 
