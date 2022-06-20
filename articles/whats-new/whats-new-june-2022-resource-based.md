---
title: Co je nového - červen 2022 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Microsoft Dynamics 365 Project Operations z června 2022 pro scénáře založené na zdrojích / neskladových položkách.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959421"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového - červen 2022 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Tento článek se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.43.0.77
- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

Následující tabulka ukazuje mapy duálního zápisu, které byly upraveny nebo přidány ve verzi Project Operations z června 2022.

| Mapování entity | Aktualizovaná verze | Komentáře |
| --- | --- | --- |
| Entita exportu faktury dodavatele projektu integrace Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Zastaralé pole bylo označeno jako zastaralé a namapováno na nové pole pro sledování stavu faktury dodavatele. |

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a řešení Finance. Některé funkce a možnosti nemusí fungovat správně, pokud není aktivována nejnovější verze mapy. Aktivní verzi mapy můžete zobrazit ve sloupci **Verze** na stránce **Duální zápis**. Novou verzi mapy můžete aktivovat výběrem **Verze mapy tabulky** výběrem nejnovější verze a poté uložením vybrané verze. Pokud jste upravili integrovanou mapu tabulky, použijte změny znovu. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud při spuštění mapy narazíte na problém, postupujte podle pokynů v části [Problém s chybějícími sloupci tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) průvodce řešením problémů s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Subdodávka | 2708885 | Opravena chybová zpráva, která se zobrazuje, když uživatel vytvoří záznam záhlaví rezervace rezervovatelného zdroje, kde není vyplněn žádný rezervovatelný zdroj. |
| Plánování a sledování projektu | 2629441 | Opravena logika spouštění pracovního postupu, aby se zabránilo nekonečné smyčce při aktualizaci projektových úkolů. |
| Čas a výdaje | 2641209 | Import časových záznamů z úkolů/rezervací musí uchovávat odkaz na rezervovatelné zdroje. |
| Plánování a sledování projektu | 2651148 | Záhlaví projektového dokumentu musí být chráněno.|
| Plánování a sledování projektu | 2653145 | Přidána ověření, aby bylo zajištěno, že nelze vytvořit záznam projektu, který má v názvu neplatné znaky. |
| Čas a výdaje | 2654710 | Opraveno filtrování na stránce **Schválení**. |
| Fakturace a ceny | 2667805 | Byla přidána ověření, která pomáhají zabránit vytvoření skutečných fakturovaných prodejů, pokud neexistují podpůrné nevyúčtované skutečné prodeje. |
| Fakturace a ceny | 2668378 | Přidána ověření, která pomáhají zabránit přidání vlastní dimenze cen, pokud není vyplněn logický název a název pole. |
| Subdodávka | 2677485 | Aktualizována cílová verze mapy duálního zápisu řádků faktury dodavatele. |
| Čas a výdaje | 2700428 | Vylepšená logika schvalování, aby bylo zajištěno, že další sady schválení pro projekt lze zpracovat, i když jedna ze sad schválení uvízne v systémových úlohách. |

### <a name="project-management-and-accounting-in-finance"></a>Správa projektů a účetnictví ve Finance

Sháníte-li informace o opravách chyb zahrnutých v této aktualizaci, přihlaste se ke službám Microsoft Dynamics Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
