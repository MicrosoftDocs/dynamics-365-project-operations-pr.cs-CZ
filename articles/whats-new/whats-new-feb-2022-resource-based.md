---
title: Co je nového, únor 2022 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Toto téma poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations z února 2022 pro scénáře založené na zdrojích / neskladových položkách.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 76ae00517c857415c89d7a03f421686dad28da93
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600826"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového, únor 2022 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

*Platí pro: Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě*

Toto téma se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.28.0.120
- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.24

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

- Od této verze můžete do jednoho projektu přidat až 300 členů týmu. Dříve byl limit na počet členů týmu 150. Další informace naleznete v části [Projektové lilmity](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Aktualizace mapování duálního zápisu Project Operations

Následující seznam ukazuje mapy duálního zápisu, které byly upraveny nebo přidány ve verzi Project Operations z února 2022.

| Mapování entity | Aktualizovaná verze | Komentáře |
| --- | --- | --- |
| Entita exportu výdajů projektu integrace Project Operations (msdyn\_expenses) | 1.0.0.3 | Rozšířeno pro synchronizaci projektových aktivit do Dataverse. |

Aktuální seznam a verze map pro duální zápis Project Operations viz [Verze mapy s duálním zápisem Project Operations](../environment/resource-dual-write-maps.md).

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a řešení Finance. Některé funkce a možnosti nemusí fungovat správně, pokud není aktivována nejnovější verze mapy. Aktivní verzi mapy můžete zobrazit ve sloupci **Verze** na stránce **Duální zápis**. Novou verzi mapy můžete aktivovat výběrem **Verze mapy tabulky** výběrem nejnovější verze a poté uložením vybrané verze. Pokud jste upravili integrovanou mapu tabulky, použijte změny znovu. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud při spuštění mapy narazíte na problém, postupujte podle pokynů v části [Problém s chybějícími sloupci tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) průvodce řešením problémů s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Fakturace a ceny | 2415109 | Výchozí hodnota v poli **Platební podmínky operací** musí být záznam zákazníka projektové smlouvy a záznam proforma faktury. |
| Fakturace a ceny | 2497369 | Oprava materiálu musí sledovat hodnotu data v parametrech **Oprava**. |
| Fakturace a ceny | 2498697 | Vylepšena konfigurace zabezpečení pro **Odvolání časového záznamu**. |
| Fakturace a ceny | 2513824 | U scénářů založených na zdrojích nesmí ID kategorie transakce v Project Operations přesáhnout 28 znaků. |
| Fakturace a ceny | 2517455 | Akce **Aktualizovat transakce řádku faktury** nesmí být spuštěna vícekrát současně pro stejnou fakturu. |
| Fakturace a ceny | 2517465 | Akce **Deaktivujte podrobnosti řádku faktury** je zablokována, protože není podporována. |
| Fakturace a ceny | 2556660 | Opravena kontrola účinnosti data, která se provádí v ceníku připojeném k záznamu parametrů projektu. |
| Správa příležitostí | 2369202 | Opravena obchodní logika, která ověřuje, že ceníky, které mají překrývající se data účinnosti, mohou být připojeny ke stejné projektové smlouvě. |
| Správa příležitostí | 2385965 | Opraveno chování na kartě **Zákazníci** na stránce **Projektová smlouva**, když vyberete **Uložit a zavřít**. |
| Čas a výdaje | 2538503 | Projektový úkol musí být k dispozici v entitě **Skutečné hodnoty projektu** poté, co je zaúčtována zpráva o výdajích. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Řízení projektů a účetnictví v Dynamics 365 Finance

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Přehled řízení projektů a účetnictví | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Během importu dobropisů dodavatele dojde k chybě. V chybové zprávě je uvedeno: "Zadržená částka nemůže být větší než zbývající čistá částka." |
| Přehled řízení projektů a účetnictví | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Pokud návrh faktury obsahuje jakékoli transakce s nulovým poplatkem, které jsou skutečnými nevyfakturovanými tržbami, nemůže dojít k fakturaci. |
| Přehled řízení projektů a účetnictví | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Zaúčtovaná cena není správná po aktualizaci nákupní ceny, když je zapnuto **Aktivovat správu změn**.|
| Přehled řízení projektů a účetnictví | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Odhad účtování pro projekt s pevnou cenou používá nesprávnou měnu a částku v dokladu odhadu, i když je funkce **Povolit měnu projektové smlouvy pro výpočet odhadu** povolena. |
| Přehled řízení projektů a účetnictví | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Rozšíření** by nemělo volat k povolení sledování změn bez zachycení výjimek pro entity, které mají konfigurační klíče, které nejsou povoleny. |
| Přehled řízení projektů a účetnictví | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Dávková úloha je opravena, když je zaúčtováno více rozšířených žurnálů a dojde k chybě. |
| Cestování a výdaje | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Kvůli problému s vyúčtováním, který souvisí s hotovostními zálohami na výkazech výdajů, není částka daně zahrnuta jako součást hotovostní zálohy. |
| Cestování a výdaje | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Informace o dani z prodeje nejsou zahrnuty v sestavě **Výdaj - Zaúčtované transakce**. |
| Cestování a výdaje | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Porušení zásad výdajů **Jsou vyžadovány účtenky** nesprávně zobrazuje varování ve výkazech výdajů. |
| Cestování a výdaje | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Transakce projektu nezahrnuje nevratnou daň z obratu v celkové částce prodeje, pokud je transakce výsledkem výdaje za kilometrovou vzdálenost. |
| Cestování a výdaje | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Když má řádek s položkami daň, nemůžete změnit datum řádku položky a dojde k chybě stavu zdrojového dokumentu. |

## <a name="removed-and-deprecated-features"></a>Odstraněné a zastaralé funkce

Téma [Odebrané nebo zastaralé funkce v Project Operations](removed-depreciated-features-project.md) popisuje funkce, které byly odstraněny nebo které byly zastaralé pro Dynamics 365 Project Operations.

- Odebraná funkce již v produktu není k dispozici.
- Zastaralá funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Oznámení o zastarání se objeví v tématu [Odebrané nebo zastaralé funkce v Project Operations](removed-depreciated-features-project.md) 12 měsíců před odebráním funkce z produktu.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je nutné provést v kompilátoru.
