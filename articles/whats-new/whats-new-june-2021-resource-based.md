---
title: Co je nového - červen 2021 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Toto téma poskytuje informace o aktualizacích kvality dostupných ve verzi Project Operations z června 2021 pro scénáře založené na zdrojích / položkách, které nejsou na skladě.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 21a446fdb9526c1a2b110c5368516dafb64b5e01
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600780"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového - červen 2021 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Toto téma se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

- Project Operations v prostředí Dynamics 365 Dataverse verze 4.11.0.156 nebo 4.11.0.164.
- Řízení projektů a účetnictví v prostředí finančních a provozních aplikací verze 10.0.19.

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

V této vydané verzi jsou zahrnuty následující funkce:

- Možnost mazání [Řádků návrhu faktury projektu pro scénáře úprav](../invoicing/correct-project-invoice-proposals.md).
- Rozepsané řádky výdajů odrážejí názvy podkategorií ve výkazu výdajů [Přepracované sestavy výdajů - nové funkce](../expense/expense-reports-reimagined.md#new-features).
- Způsob platby je k dispozici v novém podokně výdajů při vytváření nového nákladu.
- Obecná dostupnost rozhraní API Plánu projektu. Tato nová funkce umožňuje zákazníkům provádět programově operace vytváření, aktualizace a odstraňování projektových úkolů, přiřazení zdrojů, závislostí úkolů a záznamů členů projektového týmu. Více informací najdete v tématu [Používání rozhraní API Plánu projektu k provádění operací s entitami plánování](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

V této verzi nejsou k dispozici žádné aktualizace map duálního zápisu Project Operations. 

Aktuální seznam a verze map duálního zápisu Project Operations najdete v části [Verze map duálního zápisu Project Operations](../environment/resource-dual-write-maps.md).

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a finančních a provozních aplikacích. Pokud není aktivována nejnovější verze mapy, některé funkce a možnosti nemusí fungovat správně. Aktivní verzi mapy můžete vidět na stránce **Duální zápis** ve sloupci **Verze**. Aktivujte novou verzi mapy výběrem **Verze mapy tabulky** a výberte nejnovější verzi a uložte vybranou verzi. Pokud jste přizpůsobili připravenou mapu tabulky, změny znovu použijte. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud narazíte na problém se spuštěním mapy, postupujte podle pokynů v [Problém chybějících sloupců tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v příručce pro řešení potíží s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| **Oblast funkcí** | **Referenční číslo** | **Aktualizace pro zvýšení kvality** |
| --- | --- | --- |
| Fakturace a ceny | 2281417 | Opraven problém týkající se selhání akce automatického vytváření faktur prostřednictvím plánu faktur. |
| Fakturace a ceny | 2287835 | Vylepšený výkon potvrzení faktury. |
| Správa příležitostí | 2222555 | Zpoplatnění odhadů materiálu musí být při použití správně zkopírováno, aby bylo možné uvést podrobnosti řádku **Import z odhadu projektu**. |
| Správa příležitostí | 2223427 | Přizpůsobení je nyní povoleno pro akci **GenerateRetainersFromRetainerScheduleOptions**. |
| Správa příležitostí | 2277528 | Opravený výpočet hodnoty milníku fakturace pro řádky smlouvy projektu s více zákazníky. |
| Plánování a sledování projektu | 2226110 | Opraven občasný problém s funkcí **Generovat požadavek** v mřížce **Projektový tým**. |
| Plánování a sledování projektu | 2208109 | Uživatelé nemohou vytvořit projekt v jedné měně se souvisejícími úkoly v jiné měně. |
| Plánování a sledování projektu | 2258228 | Seznam polí, u kterých jsou povoleny úpravy pomocí entit **Plánování** za použití API plánu, byl aktualizován. |
| Plánování a sledování projektu | 2293989 | Správné jazykové a regionální nastavení musí být předáno do mřížky **Projektové úkoly**. |
| Správa zdrojů | 2220493 | Opravena uživatelské prostředí v mřížce **Úkol**, když rychle označíte požadavek na zdroj jako dokončený. |
| Správa zdrojů | 2330496 | Opravený problém načítání **Plánovací vývěsky**. (Aktualizace kvality je k dispozici ve verzi 4.11.0.164) |
| Čas a výdaje | 2194431 | Mřížka **ČAsový záznam** musí ctít začátek týdne, jak je stanoveno v **Nastavení systému**. |
| Čas a výdaje | 2277311 | Po odstranění hodnoty v buňce v mřížce **Časový záznam** kurzor zůstane v mřížce. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Řízení projektů a účetnictví v Dynamics 365 Finance

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Přehled řízení projektů a účetnictví | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Poznámky formuláře** a **Nastavení formuláře** není vidět v **Nastavení řízení projektu** v právnických osobách Finance, které jsou integrovány s Project Operations. |
| Přehled řízení projektů a účetnictví | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Výchozí popis pro DPH je prázdný, když **Typ účtování** = **DPH** pro poukázky na faktury projektu. |
| Přehled řízení projektů a účetnictví | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Zaúčtují se dvojí transakce při použití fakturace podle úkolů v Dataverse s integrací Project Operations. |
| Přehled řízení projektů a účetnictví | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Procento dokončení rozpoznávání výnosů je při použití integrace Project Operations nesprávné. |
| Přehled řízení projektů a účetnictví | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Časové rozlišení příjmů se u integrované scénáře Project Operations zdvojnásobí na nevyřízené faktuře dodavatele. |
| Přehled řízení projektů a účetnictví | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Nelze zaúčtovat deník integrace, když je pravidlo profilu výnosů nastaveno na **Skupina**. |
| Přehled řízení projektů a účetnictví | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Nákupní fakturu nelze zaúčtovat u nákupních objednávek projektu, které mají řádky s více měrnými jednotkami. |
| Přehled řízení projektů a účetnictví | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Výchozí finanční dimenzi projektu nelze aktualizovat pomocí datových entit projektů **V2**. |
| Přehled řízení projektů a účetnictví | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Dávkový proces vytváření odhadů projektu trvá příliš dlouho. |
| Přehled řízení projektů a účetnictví | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Odstraněním smlouvy se také odstraní adresa spojená se zákazníkem. |
| Cestování a výdaje | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Podmínka pracovního postupu schválení sestavy výdajů není správně vyhodnocena. |
| Cestování a výdaje | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Zásady výkazu výdajů správně nevyhodnocují ID projektu. |
| Cestování a výdaje | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Akce **Rozdělit na osobní pro mezipodnikové výdajové transakce** nefunguje správně. |
| Cestování a výdaje | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Když jsou odstraněny určité cestovní požadavky, jsou omylem smazány řádky hlášení o výdajích. K tomu dochází, když recID sestavy výdajů a cestovní požadavek jsou stejné. |
| Cestování a výdaje | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | V mobilní aplikaci Expense je problém, když je vyžadováno pole **ID projektu** v zásadách výkazu výdajů. |
| Cestování a výdaje | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Mezipodnikové výdaje spojené s projektem nelze upravit. Místo toho se zobrazí následující chybová zpráva: „Odkaz na objekt není nastaven na instanci objektu.“ |
| Cestování a výdaje | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Po zaúčtování výkazu výdajů je v podřízené účetní knize banky uvedena nesprávná měna a částka. |
| Cestování a výdaje | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Byla vylepšena funkce *Smazat transakce kreditní karty*.  |
| Cestování a výdaje | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | DPH zahrnutá v sestavě výdajů se konzistentně nepočítá, když je v právnické osobě uvedena jiná měna vykazování. |
| Cestování a výdaje | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Výkon je ovlivněn při přidávání nových cestovních výdajů v hotovosti. |
| Cestování a výdaje | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Pravidla zásad výdajů se ve výkazu výdajů nespouštějí. |
| Cestování a výdaje | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Nahráním nové sdílené kategorie pomocí Data Management Framework odeberete všechny podkategorie pro všechny sdílené kategorie. |
| Cestování a výdaje | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Když vytvoříte řádek výdajů a poté vyberete kategorii, zobrazí se následující chybová zpráva: „Kombinace DOM skupiny DPH a STD skupiny DPH z položky není platná.“ |
| Cestování a výdaje | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | V mobilní aplikaci Expense jsou problémy se synchronizací. |
