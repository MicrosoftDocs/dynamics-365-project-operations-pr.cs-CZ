---
title: Práce s osobními výdaji ve výkazu výdajů
description: Tento téma poskytuje informace o tom, jak pracovat s osobními výdaji vzniklým zaměstnancům při cestování za obchodními účely.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 5e1162133eec5a85675bf686855d420c50de0eaf045d81c4b417b6fe66ee19fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993143"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>Práce s osobními výdaji ve výkazu výdajů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Během služebních cest může zaměstnanec platit osobní výdaje ze své podnikové kreditní karty. Pokud nebyl definován proces pro zpracování osobních výdajů, může být proces schválení sestavy výdajů narušen, když zaměstnanec odešle svou podrobnou sestavu výdajů.

Existují dvě metody, které můžete použít k práci s osobními výdaji zaměstnance:

  - **Placeno zaměstnancem**: Vaše organizace neplatí osobní výdaje, které jsou uvedeny na účtu firemní kreditní karty. Zaměstnanec místo toho zaplatí dodavateli kreditní karty náklady přímo. 
  - **Placeno společností**: Vaše organizace zaplatí celý účet za firemní kreditní kartu a poté strhne z účtu pracovníka osobní náklady.

Způsob, který vaše organizace používá, se vybírá na stránce **Parametry řízení výdajů**.


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>Povolit funkci rozdělení výdajů, pokud má pole osobní částky definovanou hodnotu

Funkce **Povolit funkci rozdělení výdajů, pokud má pole osobní částky definovanou hodnotu** platí pouze pro sestavy výdajů, které jsou schváleny pomocí pracovního postupu na úrovni řádků. Sestavy jsou schváleny přechodem na **Zpracovat sestavy výdajů** > **Sestavy výdajů, které mi byly přiřazeny** > **Otevřít sestavu výdajů**. 

Chcete-li tuto funkci povolit, přejděte na **Pracovní prostory** > **Správa funkcí**, vyberte **Povolit funkci rozdělení výdajů, pokud má pole osobní částky definovanou hodnotu** a potom vyberte **Aktivovat**. 

Když je funkce povolena, řádky výdajů, které používají tuto funkci, vygenerují při odeslání sestavy dva řádky. Jsou generovány dva řádky, aby schvalovatel mohl schválit každý řádek zvlášť.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
