---
title: Hotovostní záloha
description: Toto téma poskytuje informace o hotovostních zálohách.
author: suvaidya
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6da50ac5611fcbd54aef8d8591ee112200468177
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276700"
---
# <a name="cash-advance"></a>Hotovostní záloha

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Hotovostní záloha umožňuje zaměstnancům půjčit si peníze od jejich společnosti před vznikem jakýchkoli výdajů. Když je požadovaná hotovostní záloha schválena a zaplacena, může zaměstnanec použít peníze na výdaje na podnikání, které jim pravděpodobně vzniknou. 

## <a name="create-and-submit-a-cash-advance-request"></a>Vytvořte a odešlete požadavek na hotovostní zálohu
Chcete-li vytvořit novou hotovostní zálohu a odeslat žádost o hotovostní zálohu, postupujte takto: 

1. Pod **Moje výdaje** vyberte **Hotovostní zálohy** > **Nová**. 
2. Na stránce **Nová žádost o hotovostní zálohu** zadejte účel výdajů a vyberte místo, kde vzniknou výdaje.
3. Zadejte požadovanou částku a měnu a poté vyberte **Uložit**. 
4. Až budete připraveni podat žádost o hotovostní zálohu, na stránce **Žádost o hotovostní zálohu** vyberte **Pracovní postup** > **Odeslat**.

## <a name="modify-a-cash-advance-request"></a>Upravte požadavek na hotovostní zálohu

Pokud žádost o hotovostní zálohu nebyla předložena ke schválení, můžete ji upravit.

1. Pod **Moje výdaje: hotovostní zálohy** vyhledejte a vyberte hotovostní zálohu, kterou chcete upravit.
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

Když vytvoříte a odešlete zprávu o výdajích pro hotovostní zálohu, kterou jste již obdrželi, budou náklady automaticky upraveny oproti této záloze. Pokud je vaše hotovostní záloha větší než vyúčtovaná částka, musíte zůstatek společnosti vrátit pomocí kategorie výdajů **Návrat hotovosti**. Pokud je hotovostní záloha zaplacená společností nižší než částka, kterou jste vynaložili, společnost vám musí zůstatek uhradit. 

### <a name="example"></a>Příklad
Plánujete cestovat ze Seattlu do New Yorku na konferenci. Požadavek na hotovostní zálohu pro 3000,00 USD vytvoříte na základě odhadovaných nákladů na vstupenku na konferenci, lety, hotel, stravu a taxi. Nebudete dostávat platby, dokud váš nadřízený neschválí tuto žádost. Poté, co ji váš manažer schválí, bude požadovaná hotovostní záloha vyplacena jako 3000,00 USD na váš bankovní účet. Poté se zúčastníte konference. Po dokončení cesty zjistíte, že celkové výdaje byly pouze 2790,00 USD. Vyberte **Hotovost** v poli **Způsob platby** pole a zadejte své výdaje 2790,00 USD. Odeslaná částka výdajů se automaticky upraví proti hotovostní záloze 3000,00 USD, která vám byla zapůjčena. Nyní dlužíte zůstatek 210,00 USD (3000,00 - 2790,00), který můžete společnosti vrátit pomocí kategorie výdajů **Vrácení hotovosti**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]