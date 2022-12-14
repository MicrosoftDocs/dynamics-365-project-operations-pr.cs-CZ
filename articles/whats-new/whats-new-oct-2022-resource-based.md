---
title: Co je nového, říjen 2022 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Microsoft Dynamics 365 Project Operations z října 2022 pro scénáře založené na zdrojích / neskladových položkách.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806594"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového, říjen 2022 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Tento článek se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.57.0.176
- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.30

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

| Oblast funkcí | Název funkce | Více informací |
| --- | --- | --- |
| Plánování a sledování projektu | **Externí plánování Project Operations**<br>Režim externího plánování umožňuje zákazníkům nativně vytvářet, aktualizovat a odstraňovat entity, které souvisejí se strukturovaným rozpisem prací, pomocí nativních rozhraní API Dataverse bez aktuálních omezení, která jsou vynucována aplikací Microsoft Project for the Web. | [Externí plánování](/dynamics365/project-operations/project-management/external-scheduling) |
| Nasazení a konfigurace | <p>**Umožnit zákazníkům vybrat si typ nasazení**<br>Produktem řízené aktualizace (PDU) Project Operations se používají k automatické instalaci řešení duálního zápisu Project Operations, když jsou v prostředí nainstalována řešení jádra a orchestrace duálního zápisu.</p><p>Tato funkce zavádí nový parametr **Chování při upgradu řešení** v parametrech projektu. Když je tento parametr nastaven na **Pouze Lite**, PUD už nebudou automaticky instalovat řešení duálního zápisu Project Operations, i když jsou v prostředí nainstalována řešení jádra a orchestrace duálního zápisu. Toto chování bude přínosem pro zákazníky, kteří plánují používat řešení duálního zápisu k integraci prodejních objednávek do finančních a provozních aplikací, ale chtějí používat Project Operations ve zjednodušeném režimu (tj. bez integrace do finančních a provozních aplikací).</p> | |
| Fakturace a ceny | <p>**Převod měn pro prodejní transakci nevyfakturovaných nákladů v integrovaných prostředích**<br>Pro zákazníky, kteří používají Project Operations integrované s finančními a provozními aplikacemi (to znamená s typem nasazení zdroje/nezásoby), směnné kurzy obvykle ovládají finanční a provozní aplikace. Pokud by však kategorie nákladů měla být oceněna pomocí metody výpočtu ceny „v ceně“ nebo „přirážka k nákladům“, když je zákazníkovi fakturována, směnný kurz, který se používá k výpočtu částky prodeje, použije směnné kurzy v Dataverse, nikoli směnné kurzy z finančních a provozních aplikací.</p><p>Tato funkce zavádí nový parametr **Chování při převodu měny** v parametrech projektu. Když je tento parametr nastaven na **Rozšířené se záložním řešením**, nevyfakturované prodejní částky u nákladových transakcí se počítají pomocí směnných kurzů z finančních a provozních aplikací.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

V této verzi nejsou k dispozici žádné aktualizace map duálního zápisu Project Operations. Aktuální seznam a verze map duálního zápisu Project Operations najdete v části [Verze map duálního zápisu Project Operations](../environment/resource-dual-write-maps.md).

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a řešení Finance. Některé funkce a možnosti nemusí fungovat správně, pokud není aktivována nejnovější verze mapy. Aktivní verzi mapy můžete zobrazit ve sloupci **Verze** na stránce **Duální zápis**. Novou verzi mapy můžete aktivovat výběrem **Verze mapy tabulky** výběrem nejnovější verze a poté uložením vybrané verze. Pokud jste upravili integrovanou mapu tabulky, použijte změny znovu. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud při spuštění mapy narazíte na problém, postupujte podle pokynů v části [Problém s chybějícími sloupci tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) průvodce řešením problémů s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Fakturace a ceny | 2316317 | Systém umožňuje vytvářet faktury, které nemají žádné fakturovatelné transakce. |
| Fakturace a ceny | 2737300 | Před otevřením formuláře ověřte dostupnost pole **Zákazník**. |
| Fakturace a ceny | 2744948 | Přidejte kontrolu nuly pro způsob fakturace. |
| Fakturace a ceny | 2763515 | Popisovač chyby nulové reference, když chybí prodejní smlouva faktury. |
| Fakturace a ceny | 2844301 | Vytvoření dávkové faktury se nezdařilo kvůli chybě. |
| Fakturace a ceny | 2845869 | Nesprávné uložení organizační služby. |
| Fakturace a ceny | 2853729 | Údaje o roli a ceně se aktualizují při změně typu fakturace. |
| Fakturace a ceny | 2940350 | Při stanovení skutečných cen musí být automaticky zadány pouze aktivní ceníky. |
| Nasazení a konfigurace | 3001206 | Entita msdyn\_replaylogheader brání upgradům zákaznických organizací. |
| Správa příležitostí | 2755582 | Popisovač výjimek null v Pomocníkovi pravidla rozdělení fakturace. |
| Správa příležitostí | 2761477 | Při použití rozdělené fakturace po odstranění milníku (záhlaví) zůstanou osiřelé milníky. |
| Správa příležitostí | 2767595 | Když je záznam o využití materiálu otevřen v hlavním formuláři, rezervovatelný zdroj pro záznam se změní na aktuálně přihlášeného uživatele. |
| Plánování a sledování projektu | 2790384 | Časový limit čekající OperationSet je příliš krátký. |
| Plánování a sledování projektu | 2957840 | Úkoly nelze ukládat a sloupce nelze přidávat na stránku **Úkoly** v integrovaném Project Operations. |
| Správa zdrojů | 2751560 | Nekonzistentní preferované organizační jednotky v požadavku na zdroj. |
| Subdodávka | 2853245 | Párování pro skutečné hodnoty řádku faktury dodavatele neaktualizuje stav ověření, pokud je řádek smlouvy již propojen s řádkem faktury dodavatele. |
| Subdodávka | 2907231 | Fáze procesu dodavatelských faktur nemůže postoupit. |
| Čas a výdaje | 2867363 | Záznamy nevypadnou ze zobrazení Absence/Dovolená ke schválení, když jsou ve frontě ke schválení. |
| Čas a výdaje | 2894405 | TESA: Nepoužívaný adresář POC způsobuje problémy s dodržováním předpisů. |

### <a name="project-management-and-accounting-in-finance"></a>Správa projektů a účetnictví ve Finance

Sháníte-li informace o opravách chyb zahrnutých v této aktualizaci, přihlaste se ke službám Microsoft Dynamics Lifecycle Services a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
