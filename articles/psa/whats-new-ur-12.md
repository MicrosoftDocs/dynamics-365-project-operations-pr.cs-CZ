---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 12, V3
description: Tohle téma poskytuje informace o tom, co je nového v aktualizaci verze 12 pro aplikaci Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: daf0e6c7a4b1b953cb808cfefab74475c47d3996
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143820"
---
# <a name="project-service-automation-update-release-12-v3"></a>Project Service Automation, vydání aktualizace 12, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Dynamics 365 Project Service Automation (PSA). Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 a na stránce řešení nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 12 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.2.34 a je obvykle k dispozici prostřednictvím automatické aktualizace v říjnu 2019.

## <a name="update-release-12"></a>Aktualizace verze 12

### <a name="bug-fixes"></a>Opravy chyb

- Čas a výdaje

    - Opraveno: Zprávy o chybách časového záznamu byly aktualizovány o relevantnější kontext.
    - Opraveno: Mřížka časového záznamu a plán správně zobrazují svislý posuvník v případě potřeby.
    - Opraveno: Odeslané výdaje nebo časové záznamy lze schválit.
    - Opraveno: Zpráva potvrzovacího dialogového okna pro schválení zrušení byla opravena, aby reflektovala stav schválení, když je změněn ze **Schváleno** na **Odesláno**.
    - Opraveno: Pole **Cena**, **Jednotka** a **Množství** jsou nyní po schválení uzamčena v záznamu Výdaje.

- Správa projektů

    - Opraveno: Akce **Nový** na hlavním formuláři **Člen týmu** byla odstraněna.
    - Opraveno: Přiřazení zdrojů bylo aktualizováno, aby zohledňovalo chyby nepřesného zaokrouhlování, které vedou k posunu koncového data úlohy.
    - Opraveno: V mřížce úloh se uživateli zobrazí příslušné chyby na straně serveru.
    - Opraveno: Jméno člena týmu se nyní v názvu úlohy vykreslí místo názvu pozice.

- Správa zdrojů

    - Opraveno: Podrobnosti o požadavcích na zdroje pro projekty vytvořené ze šablony nyní používají kalendář projektu.
    - Opraveno: Dovednosti a kompetence jsou standardně nastaveny od hlavních dat role po požadavek na zdroj vytvořené pro tuto roli.

- Sales

    - Opraveno: Duplicitní ID objektů nalezená na formuláři **Hlavní smlouva**.
    - Opraveno: Logika byla aktualizována, aby karta **Analýza nabídky** byla viditelná, takže zobrazuje nastavení metadat karty.
    - Opraveno: Datum účtování ve skutečném záznamu nyní pochází od data záznamu času/výdajů a nikoli od data schválení.
