---
title: Nová verze sestav výdajů
description: Toto téma poskytuje informace o přepracovaném prostředí pro záznam ve výkazu výdajů.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 7533f8aca317bd8d72e437592b5251fd3a866ba6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271975"
---
# <a name="redesigned-expense-reports"></a>Nová verze sestav výdajů

Záznam sestavy výdajů byl přepracován, aby se zjednodušil proces vyplňování sestav výdajů a zkrátila potřebná doba. Zde jsou hlavní součásti nového prostředí výdajů:

- Nový pracovní prostor pro správu výdajů, který vám umožní přístup k výdajům vašeho delegáta.
- Nové prostředí pro párování účtenek, které lépe zobrazuje příjmy na úrovni záhlaví a zjednodušuje proces připojování účtenek k výdajovým řádkům.
- Nová mřížka jen pro čtení, která vám umožní zobrazit mnohem více výdajových řádků a dalších sloupců dat. Nyní můžete zobrazit všechny rozepsané a rozdělené řádky spolu s jejich nadřízenými výdaji.
- Zjednodušené podokno pro úpravy nákladů.
- Přepracované chybové, varovné a zprávy o zásadách, které pomáhají zajišťovat, že máte správný kontext k porozumění problému a jeho řešení. Společnost Microsoft odstranila mnoho zpráv, které se objevily dříve, než uživatelé měli příležitost provést své úkoly a vyřešit problémy, například neúplnou zprávu o rozdělení na položky.
- Nová stránka pro určení, která pole jsou vyžadována vaší organizací, která pole jsou volitelná a která pole by neměla být zachycena. Tato stránka pomůže snížit počet polí, která uživatel musí nastavit.
- Nový vzhled a dojem pro výkazy výdajů, aby výkazy již nevypadali, jako by byly navrženy pro pracovníky účtárny.

Chcete-li zapnout nové prostředí, použijte pracovní prostředí **Správa funkcí** pro zapnutí funkce **Přepracovaný výkaz výdajů**. Po zapnutí této funkce dojde k následujícím akcím:

- Existující pracovní prostor pro výdaje je nahrazen novým pracovním prostorem.
- Je přidána nová položka nabídky pro viditelnost pole výdajů.
- Žádné existující položky nabídky pro výkazy výdajů (stávající stránka) nebo pole výkazu výdajů nejsou odstraněny.
- Pracovní postupy a veškerá schválení vás stále budou zavádět na existujíc stránku s výkazy výdajů.

## <a name="new-features"></a>Nové funkce

| Nová funkce | Popis |
|---|----|
| Viditelnost pole výdajů | Nová stránka nastavení umožňuje určit, která pole by měla být pro organizaci zakázána, která pole by měla být vyžadována a která pole jsou doporučena. |
| Povinná pole | Nová jednoduchá konfigurace umožňuje provést některá pole, aniž byste museli používat rámec zásad. |
| Nepovinná pole | Byla přidána druhá stránka pro volitelná pole. Tímto způsobem nebudou mít zaměstnanci pocit, že musí nastavovat pole, ale pole jsou stále snadno přístupná. |
| Přidejte nepřipojené účtenky | Možnost přidat nepřipojené účtenky do výkazu výdajů je viditelnější z pracovního prostoru a na výkazu výdajů. |
| Vylepšené zasílání zpráv | Je lepší viditelnost na výdajové řádky, které mají varování nebo chyby. |
| Snížení počtu zpráv na panelu zpráv| Počet zpráv Infolog byl snížen a bylo vynaloženo úsilí, aby se v mnoha případech zabránilo zobrazování duplicitních zpráv. |
| Seskupené společné akce | Rozhraní bylo vyčištěno přidáním tlačítka nových akcí pro většinu běžných akcí na úrovni řádků a přidáním tlačítka se třemi tečkami (...) pro záhlaví a další méně časté akce. |
| Nový pracovní prostor pro zvýšení viditelnosti | Nový pracovní prostor sjednocuje funkce a odkazy, které uživatelům umožňují přesouvat se do různých oblastí. |
| Přidejte existující výdaje a příjmy během vytváření výdajů | Když vytváříte výkazy výdajů, můžete přidat všechny nebo vybrané výdaje a příjmy. |
| Kalkulátor směnných kurzů | Přidána je kalkulačka směnných kurzů, která umožňuje vypočítat směnný kurz pro transakce s více měnami. |
| Uložte a přidejte nové výdajové řádky | Jsou k dipozici tlačítka **Uložit** a **Nový** při zadávání nových výdajů, která vám pomohou rychle zadat řádky výdajů. |
| Lepší viditelnost na rozdělené a rozepsané řádky | Rozepsané a rozdělené řádky se přidávají přímo do seznamu výdajů, aby se zvýšila viditelnost a pomohlo vám snadno určit, zda nedošlo k chybám zásad nebo jiným chybám. |
| Zobrazit účtenky při rozepisování | Při rozepisování lze zobrazit účtenky. |

Počáteční vydání je zaměřeno na scénáře zadávání výdajů. Jakýkoli scénář kontroly nebo schválení výkazu výdajů bude i nadále používat stávající stránku pro zadávání výdajů.

Následující funkce jsou k dispozici na existující stránce, ale ještě nejsou k dispozici na nové stránce. Tyto funkce budou znovu zavedeny během několika příštích vydání:

- Schválení
- Schválení závazků a možnost úpravy účetnictví
- Více vstupních bodů
- Integrace cestovních žádanek
- Datová entita pro viditelnost výdajového pole
- Zadávání výdajů na denní diety
- Pracovní postup na úrovni řádků
- Prozatímní podpora schvalovatele
- Rozšířené rozepisování


[!INCLUDE[footer-include](../includes/footer-banner.md)]