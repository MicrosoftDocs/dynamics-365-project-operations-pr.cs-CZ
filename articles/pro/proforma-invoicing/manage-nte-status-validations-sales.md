---
title: Správa nepřekročitelných stavů a ověření
description: Tohle téma poskytuje informace o kontrolách nepřekročitelného limitu prováděných v Project Project.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b08a6834fa0bc5254f4baab15b40c7f733d0dc6ec7e6c4fceea2836e5e4c656a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003493"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Správa nepřekročitelných stavů a ověření 

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

## <a name="not-to-exceed-on-approvals"></a>Nepřekročitelný limit při schválení

Když odešlete záznam o čase, výdaji nebo použití materiálu, vytvoří se záznam o schválení. Pokud je schválení účtovatelné a mapuje se na řádek smlouvy času a materiálu, systém provede kontrolu ověření nepřekročitelného limitu na následujících úrovních:

  - Kontrola limitu nastaveného pro zákazníka na řádku projektové smlouvy
  - Kontrola limitu nastaveného na řádku smlouvy
  - Kontrola limitu nastaveného pro zákazníka
  - Kontrola limitu nastaveného na smlouvě

Kontroly na každé úrovni zajišťují, aby částka prodejní hodnoty pro tohle schválení neporušila nepřekročitelný limit na této úrovni po zaúčtování pro již zaznamenanou částku nedokončené fakturace a fakturovanou částku k datu na této úrovni.

Pokud kontrola projde, bude schválení udělen stav ověření **Úspěch**.

Pokud kontrola selže, bude schválení udělen stav ověření **Chyba**. Podrobnosti ověření nepřekročitelného limitu informují uživatele, na jaké úrovni se ověření nezdařilo.

Když je zadaný čas, výdaje nebo položka využití materiálu považována za neúčtovatelnou, je stav ověření nepřekročitelnosti nastaven na **Nelze použít** s údaji ověření rovnými **Nelze použít**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Nepřekročitelný limit u nefakturovaných skutečných hodnot prodeje

Po schválení záznamu o čase, výdaji nebo použití materiálu se vytvoří záznamy skutečných nákladů a nevyfakturovaných prodejů. Pokud je vytvářená skutečná hodnota nefakturovaného prodeje účtovatelná a mapuje se na řádek smlouvy času a materiálu, aplikace provede kontrolu ověření nepřekročitelného limitu na následujících úrovních:

  - Kontrola limitu nastaveného pro zákazníka na řádku projektové smlouvy
  - Kontrola limitu nastaveného na řádku smlouvy
  - Kontrola limitu nastaveného pro zákazníka
  - Kontrola limitu nastaveného na smlouvě

Kontroly na každé úrovni zajišťují, aby částka prodejní hodnoty pro tuto skutečnou hodnotu neporušila nepřekročitelný limit na této úrovni po zaúčtování pro již zaznamenanou částku nedokončené fakturace a fakturovanou částku k datu na této úrovni.

Pokud kontrola proběhne úspěšně, skutečná hodnota nefakturovaného prodeje dostane stav nepřekročitelného limitu **Potvrzeno**.

Pokud kontrola selže, skutečná hodnota nefakturovaného prodeje dostane stav nepřekročitelného limitu **Chyba**. Podrobnosti ověření informují uživatele, na jaké úrovni se ověření nezdařilo.

Když je skutečná hodnota nefakturovaného prodeje považována za neúčtovatelnou nebo neplacenou, pokud na žádné ze čtyř úrovní není nastaven nepřekročitelný limit, nebo pokud je vytvářená skutečná hodnota Náklady, Záloha, Jednotka zdroje nebo Meziorganizační prodej, pole **Nepřekročitelný stav** a **Podrobnosti ověření nepřekročení** musí být nastavena na **Nelze použít**.

## <a name="reset-the-not-to-exceed-status"></a>Obnovení nepřekročitelného stavu

Můžete provést hromadné obnovení nepřekročitelného stavu. Projektoví manažeři mohou upravit ověření nepřekročení tak, aby upřednostňovalo fakturaci jednoho konkrétního souboru práce, času, výdajů nebo využití materiálu před ostatními, které jsou již potvrzeny z dostupné nepřekročitelné částky.

Poté, co se u nefakturovaných skutečných hodnot prodeje obnoví nepřekročitelný stav, potvrzená částka se sníží. Manažer projektu může vybrat jinou položku práce, času, výdajů nebo použití materiálu, u které se dříve nepodařilo nepřekročit ověření a přehodnotit. Se snížením přidělené částky tyto skutečné hodnoty nyní procházejí ověřováním, které pomáhá vedoucímu projektu uplatňovat větší vliv a kontrolu nad fakturovatelnými transakcemi za dané období.

Chcete-li obnovit nepřekročitelný stav, vyberte jednu nebo více skutečných hodnot ze zobrazení **Nedokončená fakturace času a materiálu** nebo **Skutečné hodnoty** a poté vyberte **Resetovat stav nepřekročení**.

Nepřekročitelný stav se obnoví na **Nevyhodnocený** u všech příslušných vybraných skutečných hodnot. Skutečné hodnoty s obnoveným nepřekročitelný stavem jsou nefakturované skutečné hodnoty prodeje, které ještě nejsou fakturovány, nejsou na konceptu faktury a jsou označeny jako účtovatelné. Všechny ostatní vybrané skutečné hodnoty jsou ignorovány.

## <a name="reevaluate-not-to-exceed-status"></a>Opětovné vyhodnocení stavu nepřekročení

Můžete provést hromadné opětovné vyhodnocení nepřekročitelného stavu. Opětovné vyhodnocení nepřekročitelného stavu je užitečné, když:

  - Došlo k novému vyjednání nepřekročitelných limitů se zákazníkem a je třeba přehodnotit skutečné hodnoty.
  - Projektový manažer chce doladit fakturaci nefakturovaných prodejů upřednostněním jednoho souboru práce před druhým.

Chcete-li opětovně vyhodnotit nepřekročitelný stav, vyberte jednu nebo více skutečných hodnot ze zobrazení **Nedokončená fakturace času a materiálu** nebo **Skutečné hodnoty** a poté vyberte **Znovu vyhodnotit stav nepřekročení**.

Všechny příslušné vybrané skutečné hodnoty s nepřekročitelným limitem budou vyhodnoceny podle nastavení nepřekročitelného limitu. Skutečné hodnoty, které jsou relevantní pro opětovné vyhodnocení nepřekročitelného stavu, jsou nefakturované skutečné hodnoty prodeje, které nejsou fakturovány, nejsou na konceptu faktury a jsou označeny jako účtovatelné. Jakékoli další vybrané skutečné hodnoty.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
