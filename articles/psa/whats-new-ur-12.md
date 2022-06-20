---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 12, V3
description: Tento článek obsahuje informace o novinkách a změnách ve vydání Update 12, V3 aplikace Project Service Automation.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 28539b2e1331c8509e40aaf771f4d88d6f54e022
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922628"
---
# <a name="project-service-automation-update-release-12-v3"></a>Project Service Automation, vydání aktualizace 12, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Dynamics 365 Project Service Automation (PSA). Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 a na stránce řešení nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tento článek uvádí funkce a opravy, které jsou nové nebo se změnily v Project Service Automation V3, vydání Update 12. Tato verze má číslo sestavení V3.10.2.34 a je obvykle k dispozici prostřednictvím automatické aktualizace v říjnu 2019.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
