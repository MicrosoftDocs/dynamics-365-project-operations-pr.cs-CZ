---
title: Kontrola navrhovaných zdrojů
description: Tento článek obsahuje informace o způsobu navrhování projektových zdrojů.
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
ms.openlocfilehash: 2a5b5159ceb8aa5b29dffad59517bc11fbf16871
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183966"
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
    - U požadavku na zdroj by měl kontrolor požadavku změnit stav na **Potřebuje revizi**.
    - Na kartě **Tým** projektu je automaticky změněna hodnota **Stav žádosti** obecného člena týmu na **Potřebuje kontrolu**.

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
