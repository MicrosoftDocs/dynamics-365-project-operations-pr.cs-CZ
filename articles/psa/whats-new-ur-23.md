---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 23, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 23, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: eaae9cc62c449695cb2e999be48c57075aadbb21
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073727"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation, vydání aktualizace 23, V3

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 23 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V 3.10.34.30 a je obvykle k dispozici prostřednictvím automatické aktualizace v srpnu 2020.

## <a name="update-release-23"></a>Aktualizace verze 23

### <a name="bug-fixes"></a>Opravy chyb

**Čas a výdaje**

Byly vyřešeny následující problémy:
- Zpracovnání případu hrany v možnosti **Smazat člena projektového týmu** pro poskytnutí smysluplné výjimky.
- Výsledky importu přiřazení na prázdné obrazovce pro odebrání.

**Správa zdrojů**

Byly vyřešeny následující problémy:

- **Karta zdrojů mřížky využití zrdojů** zobrazuje nesprávná data, pokud je časová stupnice delší než pět dní.
- Když zákazníci vytvoří rezervovatelný zdroj, modul plug-in občas selže při automatickém přidání zdroje do skupiny Microsoft Office 365.
- Zobrazení **Vyrovnání** ukazuje manuální křivky v zobrazení **Týden** nebo **Měsíc** nesprávně.

**Správa projektů**

Byly vyřešeny následující problémy:

- Nadměrný počet entit **RetrieveMultiple for usersettings** způsobuje snížený výkon při schvalování projektů a dalších operacích.
- Vyhledávání zdrojů v mřížce **Plánování úkolů** je omezeno pouze na zobrazení až pěti členů týmu z projektového týmu. 
- Vyhledávání zdrojů v mřížce **Plánování úkolů** nefiltruje neaktivní zdroje.
- Manuální režim nefunguje podle očekávání ve strukturovaném rozpisu prací při plánování projektu.
- Mřížka **Plánování úkolů** ukazuje **Neaktivní kategorie transakcí**.
- Mřížka **Přiřazení zdrojů** se zaokrouhlí nesprávně, když má úkol více přiřazení.
- Hodnoty zaokrouhlení se liší mezi plánovanými náklady a skutečnými náklady na jeden úkol.

**Sales**

Byly vyřešeny následující problémy:

- **Načíst všechny kategorie transakcí** při dvojitém kliknutí vytvoří více řádků.
