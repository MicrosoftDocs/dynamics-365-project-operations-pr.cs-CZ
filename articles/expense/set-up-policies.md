---
title: Definice zásad výdajů
description: Můžete definovat zásady výdajů, které musí vaši pracovníci dodržovat při zadávání a odesílání výkazů výdajů a cestovních žádanek.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 863d1e44dad9fa0d2174cf77582a1d820988e92d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276070"
---
# <a name="define-expense-policies"></a>Definice zásad výdajů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Můžete definovat zásady, které musí vaši pracovníci dodržovat při zadávání a odesílání výkazů výdajů a cestovních žádanek.         
Implementace zásad výdajů vám pomůže efektivně spravovat výdaje.         

Můžete například nastavit zásadu pro hotelové výdaje v New Yorku, kde se uvádí, že výdaje za noc nesmí překročit 250 USD.       
Pokud pracovník předloží výkaz výdajů nebo cestovní žádanku, kde sazba za pokoj překročí tuto částku, systém oznámí         
pracovníkovi, že byla překročena částka zásady pro výdaj. Můžete nakonfigurovat zprávu, kterou pracovník obdrží, když vy        
definujete zásadu.      
        
Můžete definovat tři typy zásad:         
        
- **Upozornění**: Umožňuje pracovníkovi odeslat výkaz výdajů nebo cestovní žádanku, ale výdaj bude označen pro všechny schvalovatele a         
  a pro pozdější vykázání.        

- **Chyba**: Vyžaduje, aby pracovník před odesláním výkazu výdajů nebo cestovní žádanky revidoval výdaj ohledně splnění zásady.        
 
 - **Odůvodnění**: Vyžaduje, aby pracovník nebo manažer před odesláním výkazu výdajů nebo cestovní žádanky zadal odůvodnění překročení částky zásady.        

## <a name="policy-tips"></a>Tipy pro zásady
Zde je několik návrhů, které vám mohou pomoci při vytváření nových zásad pro správu výdajů: 

- Zásady jsou účinné od data, což znamená, že zásada nebude platit, pokud bude vytvořena s datem po datu, kdy došlo k výdaji. Například dnes vytvoříte novou zásadu k vynucení maximálních výdajů na jídlo ve výši 50 USD. Veškeré stávající výdaje zadané od včerejška nebudou porovnány s touto zásadou.
- Při vytváření zásady pro kategorii výdajů, kterou lze rozčlenit na položky, zvažte přidání podmínky pro typ řádku výdajů. Některé zásady, například požadavek účtenky, nemusí mít pro rozepsané řádky smysl. V této situaci se zásada použije pouze na řádek záhlaví nebo na nerozepsaný řádek. 
- Ve výchozím nastavení se zásady správy výdajů vyhodnocují oproti zdrojové entitě. Pro mezipodnikové scénáře můžete místo toho nastavit zásadu, která se má vyhodnotit podle cílové entity (výpůjční entita). Chcete-li spustit zásady proti cílové entitě, zapněte funkci **Vyhodnotit zásadu výdajů proti vypůjčující právnické osobě** v pracovním prostoru **Správa funkcí**.

## <a name="when-to-evaluate-policies"></a>Kdy vyhodnotit zásady

V parametrech správy výdajů můžete vybrat, zda chcete vyhodnotit zásady správy výdajů při uložení řádku nebo při odeslání výkazu výdajů. Pokud se rozhodnete vyhodnotit při uložení řádku, uživatelé budou mít dříve přehled o tom, co potřebují k dokončení svého výkazu najednou. Jinak můžete zpozdit vyhodnocení zásad a ušetřit čas ověřením na konci, během odesílání do pracovního postupu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]