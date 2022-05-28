---
title: Kontrola navrhovaných zdrojů
description: Toto téma obsahuje informace o způsobu navrhování projektových zdrojů.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3d2ab3ba9e5b18a2b42acaa2dc51ad94b8189274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584956"
---
# <a name="review-proposed-resources"></a>Kontrola navrhovaných zdrojů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Správci zdrojů mohou navrhnout zdroj projektovému manažerovi pomocí žádosti o zdroj.

Chcete-li zkontrolovat navrhované zdroje, postupujte takto:

1. Z mřížky **Žádost** nebo ze samotné žádosti vyberte **Najít zdroje**.
2. Na stránce **Pomocník plánování**, vyberte zdroj a potvrďte, že všechny navrhované hodiny jsou zahrnuty v navrhované rezervaci.
3. V podokně **Vytvořit rezervaci zdrojů** nastavte pole **Stav rezervace** na **Navrženo** a vyberte **Rezervovat**.

    > [!NOTE]
    > Nastavení **Stav rezervace** na **Navrženo** nerezervuje zdroj závazně a nenahrazuje obecný zdroj s pojmenovaným členem týmu.

    Dojde k následujícím aktualizacím stavu:

    - Na stránce **Pomocník plánování** jsou ukazatele stavu aktualizovány tak, aby označovaly, že rezervace je navržena, že není závazně rezervována.
    - U žádosti o zdroj se stav změní na **Potřebuje kontrolu**.
    - Na kartě **Tým** projektu je změněna hodnota **Stav žádosti** obecného člena týmu na **Potřebuje kontrolu**.

Projektový manažer může návrh buď přijmout, nebo zamítnout.

Správci zdrojů mohou při zpracování žádostí o zdroje použít kterýkoli z následujících přístupů:

- Navrhnout více zdrojů pro uspokojení poptávky, pokud není k dispozici žádný zdroj pro splnění požadovaných hodin. Navržené hodiny jsou pak rozděleny mezi více zdrojů, které mohou uspokojit požadované hodiny. V tomto scénáři se hodiny nemohou překrývat.
- Navrhnout méně zdrojů, než je vyžadováno. V tomto scénáři je navrhovaná kapacita zdroje menší než požadovaná doba, kterou žadatel specifikoval. Proto, když žadatel přijme navržené zdroje, je vytvořen nesplněný požadavek na zdroj k zachycení zbývající poptávky.
- Rezervovat více zdrojů pro uspokojení poptávky, pokud není k dispozici žádný zdroj pro dokončení práce.
- Rezervujte méně zdrojů, než je vyžadováno. V tomto scénáři je počet rezervovaných hodin menší než počet požadovaných hodin. Systém vás provede návrhy zdrojů místo rezervací, aby mohl žadatel ověřit a sledovat zbývající poptávku.

## <a name="resource-availability"></a>Dostupnost zdroje

Je důležité, aby správci zdrojů mohli zobrazit dostupnost zdrojů a aktualizovat rezervace. V některých případech neexistuje žádná formální poptávka (požadavek na zdroje). Správce zdrojů však musí reagovat na neplánovanou poptávku, která přichází prostřednictvím jiných kanálů, jako jsou e -maily, telefonní hovory nebo rychlé zprávy. Správci zdrojů používají k aktualizaci zdrojů a rezervací **Plánovací vývěsku**.

Jako základ pro výpočet dostupnosti zdroje slouží pracovní doba zdroje. Rezervace zdrojů spotřebovávají kapacitu zdrojů.

**Plánovací vývěska** používá barvy a stínování k zobrazení rezervací, dostupnosti a přerezervace a také stavu rezervací. Nastavení na **Plánovací vývěska** umožňuje zobrazit legendu.

Pokud se vedle konkrétního rezervovatelného zdroje v **Plánovací vývěsce** zobrazí šipka vpravo, lze zdroj rozbalit. Zobrazí se podrobnosti o práci, pro kterou je zdroj rezervovaný.

Protože Dynamics 365 Project Operations používá modul Universal Resource Scheduling, tak pokud máte nainstalovanou aplikaci Dynamics 365 Field Service můžete také zobrazit podrobnosti o rezervacích zdrojů pro projekty, pracovní objednávky a všechny další entity, na které jste rozšířili plánování.

Chcete-li zobrazit další podrobnosti o konkrétním zdroji, klepněte na něj pravým tlačítkem myši a otevřete kartu zdroje.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
