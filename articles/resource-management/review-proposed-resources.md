---
title: Kontrola navrhovaných zdrojů
description: Toto téma obsahuje informace o způsobu navrhování projektových zdrojů.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401165"
---
# <a name="review-proposed-resources"></a>Kontrola navrhovaných zdrojů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Správci zdrojů mohou navrhnout zdroj projektovému manažerovi pomocí žádosti o zdroj.

1. Z mřížky žádosti nebo ze samotné žádosti vyberte **Najít zdroje**.
2. Na stránce **Pomocník plánování** vyberte zdroj a potom v podokně **Vytvořit rezervaci zdroje** v poli **Stav rezervace** vyberte **Rezervovat**.

Dojde k následujícím aktualizacím stavu:

- Na stránce **Pomocník plánování** jsou ukazatele stavu aktualizovány tak, aby označovaly, že rezervace je navržena, že není závazně rezervována.
- U žádosti o zdroj se stav změní na **Potřebuje kontrolu**.
- Na kartě **Tým** projektu je změněna hodnota **Stav žádosti** obecného člena týmu na **Potřebuje kontrolu**.

Projektový manažer může návrh buď přijmout, nebo zamítnout.

Správci zdrojů mohou při zpracování žádostí o zdroje použít kterýkoli z následujících přístupů:

- Navrhnout více zdrojů pro uspokojení poptávky, pokud není k dispozici žádný zdroj pro splnění požadovaných hodin. Navržené hodiny jsou pak rozděleny mezi více zdrojů, které mohou uspokojit požadované hodiny. V tomto scénáři se hodiny nemohou překrývat.
- Navrhnout méně zdrojů, než je vyžadováno. V tomto scénáři je navrhovaná kapacita zdroje menší než požadovaná doba, kterou žadatel specifikoval. Proto, když žadatel přijme navržené prostředky, je vytvořen nesplněný požadavek na zdroj k zachycení zbývající poptávky.
- Rezervovat více zdrojů pro uspokojení poptávky, pokud není k dispozici žádný zdroj pro dokončení práce.
- Rezervovat méně zdrojů, než je vyžadováno. V tomto scénáři je počet rezervovaných hodin menší než počet požadovaných hodin. Systém vás provede návrhy zdrojů místo rezervací, aby mohl žadatel ověřit a sledovat zbývající poptávku.

## <a name="resource-availability"></a>Dostupnost zdroje

Je důležité, aby správci zdrojů mohli zobrazit dostupnost zdrojů a aktualizovat rezervace. V některých případech neexistuje formální poptávka (žádost o zdroj), ale správce zdrojů musí odpovědět na neplánovanou poptávku, která přichází prostřednictvím kanálů, jako je e-mail, telefonní hovor nebo rychlá zpráva. Správci zdrojů používají k aktualizaci zdrojů a rezervací Plánovací vývěsku.

Jako základ pro výpočet dostupnosti zdroje slouží pracovní doba zdroje. Rezervace zdrojů spotřebovávají kapacitu zdrojů.

Plánovací vývěska používá barvy a stínování k zobrazení rezervací, dostupnosti a přerezervace a také stavu rezervací. Nastavení v Plánovací vývěsce umožňuje zobrazit legendu.

Pokud se vedle konkrétního rezervovatelného zdroje v plánovací vývěsce zobrazí šipka vpravo, lze zdroj rozbalit, aby se zobrazily podrobnosti o práci, pro kterou je zdroj rezervovaný.

Protože Dynamics 365 Project Operations používá modul Universal Resource Scheduling, tak pokud máte nainstalovanou aplikaci Dynamics 365 Field Service můžete také zobrazit podrobnosti o rezervacích zdrojů pro projekty, pracovní objednávky a všechny další entity, na které jste rozšířili plánování.

Chcete-li zobrazit další podrobnosti o konkrétním zdroji, klepněte na něj pravým tlačítkem myši a otevřete kartu zdroje.



[!INCLUDE[footer-include](../includes/footer-banner.md)]