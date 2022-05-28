---
title: Co je nového, květen 2022 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Toto téma poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Microsoft Dynamics 365 Project Operations z května 2022 pro scénáře založené na zdrojích / neskladových položkách.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d3ac63f0d33d36cc5b6d4cea3ab8167e5974cfe6
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8709969"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového, květen 2022 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Toto téma se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.42.0.70
- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

V této verzi nejsou k dispozici žádné aktualizace map duálního zápisu Project Operations. Aktuální seznam a verze map duálního zápisu Project Operations najdete v části [Verze map duálního zápisu Project Operations](../environment/resource-dual-write-maps.md).

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a řešení Finance. Některé funkce a možnosti nemusí fungovat správně, pokud není aktivována nejnovější verze mapy. Aktivní verzi mapy můžete zobrazit ve sloupci **Verze** na stránce **Duální zápis**. Novou verzi mapy můžete aktivovat výběrem **Verze mapy tabulky** výběrem nejnovější verze a poté uložením vybrané verze. Pokud jste upravili integrovanou mapu tabulky, použijte změny znovu. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud při spuštění mapy narazíte na problém, postupujte podle pokynů v části [Problém s chybějícími sloupci tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) průvodce řešením problémů s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality
### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Řízení zdrojů | 2634019 | Vylepšené chybové zprávy pro obchodní ověření při přidávání obecných členů týmu jako zdrojů. |
| Plánování a sledování projektu | 2648515 | Omezené aktualizace **ownerid**, **stav** a **status** v plánovacích entitách. |
| Fakturace a ceny | 2653167 | Oddělovač desetinných míst v mřížce **Odhady** musí odpovídat nastavení formátu v **Osobní možnosti**. |
| Fakturace a ceny| 2662251 | Hodnoty v polích **Opravená jednotka** a **Skupina jednotek** jsou výchozí při vytváření záznamů v odhadech materiálu. |
| Fakturace a ceny| 2571408 | Skutečné nevyfakturované tržby jsou při vytváření konceptu faktury opatřeny razítkem ID proforma faktury. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Řízení projektů a účetnictví v Dynamics 365 Finance

Sháníte-li informace o opravách chyb zahrnutých v této aktualizaci, přihlaste se ke službám Microsoft Dynamics Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
