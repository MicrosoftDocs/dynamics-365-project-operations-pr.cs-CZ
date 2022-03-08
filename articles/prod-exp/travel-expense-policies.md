---
title: Nastavení zásad výdajů
description: Můžete nastavit zásady výdajů, které musí vaši pracovníci dodržovat při zadávání a odesílání výkazů výdajů a cestovních žádanek v aplikaci Microsoft Dynamics 365 Finance.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 050e19016edac53ef22764d227d4ef96d89ba298287b10416febbb55bb00973a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005923"
---
# <a name="set-up-expense-policies"></a>Nastavení zásad výdajů

Můžete definovat zásady, které musí vaši pracovníci dodržovat při zadávání a odesílání výkazů výdajů a cestovních žádanek.         
Implementace zásad výdajů vám pomůže efektivně spravovat výdaje.         

Můžete například nastavit zásadu pro hotelové výdaje v New Yorku, kde se uvádí, že výdaje za noc nesmí překročit 250 USD.       
Pokud pracovník předloží výkaz výdajů nebo cestovní žádanku, ve kterých sazba za pokoj překročí tuto částku, systém oznámí        
pracovníkovi, že byla překročena částka zásady pro výdaj. Můžete nakonfigurovat zprávu, kterou pracovník obdrží, když vy        
definujete zásadu.      
        
Můžete definovat tři typy zásad:         
        
- Upozornění – Umožňuje pracovníkovi odeslat výkaz výdajů nebo cestovní žádanku, ale výdaj bude označen pro všechny schvalovatele a        
  a pro pozdější vykázání.        

- Chyba – Vyžaduje, aby pracovník před odesláním výkazu výdajů nebo cestovní žádanky revidoval výdaj ohledně splnění zásady.       
 
 - Odůvodnění – Vyžaduje, aby pracovník nebo manažer před odesláním výkazu výdajů nebo cestovní žádanky zadal odůvodnění překročení částky zásady.        

## <a name="policy-tips"></a>Tipy pro zásady
Zde je několik návrhů, které vám mohou pomoci při vytváření nových zásad pro správu výdajů. 
* Zásady jsou účinné od data a nezačnou platit, pokud bude zásada vytvořena s datem po datu, kdy došlo k výdaji. Například pokud dnes vytváříte novou zásadu pro vynucení maximálních výdajů na jídlo ve výši 50 USD, nebudou všechny existující výdaje zadané do včerejška kontrolovány proti této zásadě.
* Při vytváření zásady pro kategorii výdajů, kterou lze rozčlenit na položky, zvažte přidání podmínky pro typ řádku výdajů. Některé zásady, jako je požadavek na odevzdání stvrzenky, nemusí mít smysl u rozepsaných řádků a měly by být použity pouze na řádek záhlaví nebo nerozepsaný řádek. 
* Ve výchozím nastavení se zásady správy výdajů vyhodnocují oproti zdrojové entitě. Pro mezipodnikové scénáře můžete místo toho nastavit zásadu, která se má vyhodnotit podle cílové entity (výpůjční entita). Chcete-li spustit zásady proti cílové entitě, zapněte funkci „Vyhodnotit zásadu výdajů proti vypůjčující právnické osobě“ v pracovním prostoru **Správa funkcí**.

## <a name="when-to-evaluate-policies"></a>Kdy vyhodnotit zásady

V parametrech správy výdajů existuje volba, zda chcete vyhodnotit zásady správy výdajů při uložení řádku nebo při odeslání výkazu výdajů. Pokud se rozhodnete vyhodnotit při uložení řádku, zajistíte, že uživatelé budou mít dříve přehled o tom, co potřebují k dokončení svého výkazu najednou. Jinak můžete zpozdit vyhodnocení zásad a ušetřit čas,, když k ověření dojde až na konci, během odesílání do pracovního postupu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]