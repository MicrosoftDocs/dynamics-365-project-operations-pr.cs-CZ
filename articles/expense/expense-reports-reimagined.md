---
title: Nová verze vyúčtování výdajů
description: Toto téma poskytuje informace o přepracovaném prostředí pro záznam ve výkazu výdajů.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd0d415b9cc85bac91de8fb9427da290ae0c6108
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897128"
---
# <a name="expense-reports-reimagined"></a>Nová verze vyúčtování výdajů

Přepracován byl záznam ve výkazu výdajů, aby se zjednodušil proces a zkrátila doba potřebná k dokončení výkaz. Zde jsou hlavní součásti nového prostředí výdajů:

- Nový pracovní prostor pro správu výdajů, který vám umožní přístup k výdajům vašeho delegáta.
- Nové prostředí pro párování účtenek, které lépe zobrazuje příjmy na úrovni záhlaví a zjednodušuje proces připojování účtenek k výdajovým řádkům.
- Nová mřížka jen pro čtení, která vám umožní zobrazit mnohem více výdajových řádků a dalších sloupců dat. Nyní můžete zobrazit všechny rozepsané a rozdělené řádky spolu s jejich nadřízenými výdaji.
- Zjednodušené podokno pro úpravy nákladů.
- Přepracované chybové, varovné a zprávy o zásadách, které poskytují správný kontext a porozumění problému a jeho řešení. Odstranili jsme několik zpráv, které se objevily dříve, než uživatelé mohli dokončit své úkoly a řešit problémy.
- Nová stránka k určení povinných polí, volitelných polí a polí, která by neměla být zahrnuta. Tato stránka pomáhá snížit počet polí, která je třeba nastavit.
- Nový vzhled a dojem pro výkazy výdajů, aby výkazy již nevypadali, jako by byly navrženy pro pracovníky účtárny.

Chcete-li zapnout nové prostředí, použijte pracovní prostředíá **Správa funkcí** pro zapnutí funkce **Přepracovaný výkaz výdajů**. Po zapnutí této funkce dojde k následujícím akcím:

- Existující pracovní prostor pro výdaje je nahrazen novým pracovním prostorem.
- Je přidána nová položka nabídky pro viditelnost pole výdajů.
- Žádné existující položky nabídky pro výkazy výdajů (stávající stránka) nebo pole výkazu výdajů nejsou odstraněny.
- Pracovní postupy a veškerá schválení vás stále budou zavádět na existujíc stránku s výkazy výdajů.

## <a name="getting-started-video-for-new-users"></a>Video Začínáme pro nové uživatele

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

Video [Zkušenosti s výdaji v Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (zobrazeno výše) je zahrnuto v [playlistu Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) k dispozici na YouTube.

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
| Lepší viditelnost na rozdělené a rozepsané řádky | Rozepsané a rozdělené řádky se přidávají přímo do seznamu výdajů, aby se zvýšila viditelnost a pomohlo vám snadno určit, zda nedošlo k chybám. |
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
