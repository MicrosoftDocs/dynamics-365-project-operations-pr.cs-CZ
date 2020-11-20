---
title: Správa nepřekročitelných stavů a ověření
description: Tohle téma poskytuje informace o kontrolách nepřekročitelného limitu prováděných v Project Project.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129985"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Správa nepřekročitelných stavů a ověření 

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

## <a name="not-to-exceed-on-approvals"></a>Nepřekročitelný limit při schválení

Po zadání položky času nebo výdaje se vytvoří záznam o schválení. Pokud je schválení účtovatelné a mapuje se na řádek smlouvy času a materiálu, systém provede kontrolu ověření nepřekročitelného limitu na následujících úrovních:

  - Kontrola limitu nastaveného pro zákazníka na řádku projektové smlouvy
  - Kontrola limitu nastaveného na řádku smlouvy
  - Kontrola limitu nastaveného pro zákazníka
  - Kontrola limitu nastaveného na smlouvě

Kontroly na každé úrovni zajišťují, aby částka prodejní hodnoty pro tohle schválení neporušila nepřekročitelný limit na této úrovni po zaúčtování pro již zaznamenanou částku nedokončené fakturace a fakturovanou částku k datu na této úrovni.

Pokud kontrola projde, bude schválení udělen stav ověření **Úspěch**.

Pokud kontrola selže, bude schválení udělen stav ověření **Chyba**. Podrobnosti ověření nepřekročitelného limitu informují uživatele, na jaké úrovni se ověření nezdařilo.

Pokud je předaná položka času nebo výdajů považována za neúčtovatelnou, stav ověření nepřekročitelného limitu je nastaven na **Nelze použít** s podrobnostmi o ověření, které jsou stejné jako u **Nelze použít**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Nepřekročitelný limit u nefakturovaných skutečných hodnot prodeje

Po schválení položky času nebo výdajů se vytvoří záznamy skutečných hodnot nákladů a nefakturovaných prodejů. Pokud je vytvářená skutečná hodnota nefakturovaného prodeje účtovatelná a mapuje se na řádek smlouvy času a materiálu, aplikace provede kontrolu ověření nepřekročitelného limitu na následujících úrovních:

  - Kontrola limitu nastaveného pro zákazníka na řádku projektové smlouvy
  - Kontrola limitu nastaveného na řádku smlouvy
  - Kontrola limitu nastaveného pro zákazníka
  - Kontrola limitu nastaveného na smlouvě

Kontroly na každé úrovni zajišťují, aby částka prodejní hodnoty pro tuto skutečnou hodnotu neporušila nepřekročitelný limit na této úrovni po zaúčtování pro již zaznamenanou částku nedokončené fakturace a fakturovanou částku k datu na této úrovni.

Pokud kontrola proběhne úspěšně, skutečná hodnota nefakturovaného prodeje dostane stav nepřekročitelného limitu **Potvrzeno**.

Pokud kontrola selže, skutečná hodnota nefakturovaného prodeje dostane stav nepřekročitelného limitu **Chyba**. Podrobnosti ověření informují uživatele, na jaké úrovni se ověření nezdařilo.

Když je skutečná hodnota nefakturovaného prodeje považována za neúčtovatelnou nebo neplacenou, pokud na žádné ze čtyř úrovní není nastaven nepřekročitelný limit, nebo pokud je vytvářená skutečná hodnota Náklady, Záloha, Jednotka zdroje nebo Meziorganizační prodej, pole **Nepřekročitelný stav** a **Podrobnosti ověření nepřekročení** musí být nastavena na **Nelze použít**.

## <a name="reset-the-not-to-exceed-status"></a>Obnovení nepřekročitelného stavu

Můžete provést hromadné obnovení nepřekročitelného stavu. To umožňuje projektovým manažerům upravit ověření nepřekročitelného limitu, aby byla upřednostněna fakturace jednoho konkrétního souboru práce, času nebo výdajů před ostatními, které jsou již potvrzeny z dostupné nepřekročitelné částky.

Poté, co se u nefakturovaných skutečných hodnot prodeje obnoví nepřekročitelný stav, potvrzená částka se sníží. Manažer projektu může vybrat jiný soubor práce, času nebo výdajů, které dříve neprošly ověřením nepřekročitelného limitu, a znovu je vyhodnotit. Se snížením potvrzené částky nyní tyto skutečné částky projdou ověřením. To pomáhá projektovému manažeru uplatňovat větší vliv a kontrolu nad fakturovatelnými transakcemi za dané období.

Chcete-li obnovit nepřekročitelný stav, vyberte jednu nebo více skutečných hodnot ze zobrazení **Nedokončená fakturace času a materiálu** nebo **Skutečné hodnoty** a poté vyberte **Resetovat stav nepřekročení**.

Nepřekročitelný stav se obnoví na **Nevyhodnocený** u všech příslušných vybraných skutečných hodnot. Skutečné hodnoty s obnoveným nepřekročitelný stavem jsou nefakturované skutečné hodnoty prodeje, které ještě nejsou fakturovány, nejsou na konceptu faktury a jsou označeny jako účtovatelné. Všechny ostatní vybrané skutečné hodnoty jsou ignorovány.

## <a name="reevaluate-not-to-exceed-status"></a>Opětovné vyhodnocení stavu nepřekročení

Můžete provést hromadné opětovné vyhodnocení nepřekročitelného stavu. Opětovné vyhodnocení nepřekročitelného stavu je užitečné, když:

  - Došlo k novému vyjednání nepřekročitelných limitů se zákazníkem a je třeba přehodnotit skutečné hodnoty.
  - Projektový manažer chce doladit fakturaci nefakturovaných prodejů upřednostněním jednoho souboru práce před druhým.

Chcete-li opětovně vyhodnotit nepřekročitelný stav, vyberte jednu nebo více skutečných hodnot ze zobrazení **Nedokončená fakturace času a materiálu** nebo **Skutečné hodnoty** a poté vyberte **Znovu vyhodnotit stav nepřekročení**.

Všechny příslušné vybrané skutečné hodnoty s nepřekročitelným limitem budou vyhodnoceny podle nastavení nepřekročitelného limitu. Skutečné hodnoty, které jsou relevantní pro opětovné vyhodnocení nepřekročitelného stavu, jsou nefakturované skutečné hodnoty prodeje, které nejsou fakturovány, nejsou na konceptu faktury a jsou označeny jako účtovatelné. Jakékoli další vybrané skutečné hodnoty.
