---
title: Co je nového v listopadu 2021 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Toto téma poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations z listopadu 2021 pro scénáře založené na zdrojích / neskladových položkách.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fb9dad5b04ef2933ed8a8d8211f888f13df5ba40
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942877"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového v listopadu 2021 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

*Platí pro: Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě*

Toto téma se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.22

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

V této vydané verzi jsou zahrnuty následující funkce:

- Rozhraní API plánování projektu nyní podporují vytváření a odstraňování projektových kbelíků.

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

V této verzi nejsou k dispozici žádné aktualizace map duálního zápisu Project Operations. Aktuální seznam a verze map duálního zápisu Project Operations najdete v části [Verze map duálního zápisu Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a řešení Finance. Některé funkce a možnosti nemusí fungovat správně, pokud není aktivována nejnovější verze mapy. Aktivní verzi mapy můžete zobrazit ve sloupci **Verze** na stránce **Duální zápis**. Novou verzi mapy můžete aktivovat výběrem **Verze mapy tabulky** výběrem nejnovější verze a poté uložením vybrané verze. Pokud jste upravili integrovanou mapu tabulky, použijte změny znovu. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud při spuštění mapy narazíte na problém, postupujte podle pokynů v části [Problém s chybějícími sloupci tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) průvodce řešením problémů s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-in-dataverse"></a>Project Operations v Dataverse

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Fakturace a ceny | 2240080 | Pole **Platební podmínky** nesmí být duplikováno na proforma faktuře. |
| Fakturace a ceny | 2358236 | Oprava faktury musí umožňovat opravy, které mají řádky s nulovou cenou. |
| Správa zdrojů | 2410072 | Umožnění nastavit zdroj, který je přiřazený k úkolu jako manažer projektu. |
| Fakturace a ceny | 2430234 | Oprava problému s výpočtem plnění nákladů. |
| Čas a výdaje | 2436978 | Povolení zadávat čas ve formátu hh:mm. |
| Fakturace a ceny | 2448623 | Povolení aktualizace ceníků poté, co jsou přidruženy k organizační jednotce. |
| Čas a výdaje | 2460396 | Možnost smazat záznam času vymazáním buňky. |
| Fakturace a ceny | 2467386 | Povolení odstranit projekt, který má úkol, i když je úkol spojen s vyhranou nabídkou. |
| Čas a výdaje | 2461744 | Zobrazení **Moje neúspěšná schválení** obsahuje pouze schválení projektů ve fázi **Odesláno**. |
| Čas a výdaje | 2464082 | Odebrání odkazu ze schválení projektu do sady schválení, když odpovídá cílový stav. |
| Čas a výdaje | 2468108 | Úloha plánu by neměla nastavit stav **Zpracovává se** pro sadu schválení. |
| Čas a výdaje | 2471503 | Odstranění sad schválení starých sedm dní. |
| Fakturace a ceny | 2480687 | Odkaz na řádek nabídky nesmí být odstraněn, když je vytvořen milník řádku nabídky. |

### <a name="project-management-and-accounting-in-finance"></a>Správa projektů a účetnictví ve Finance

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Přehled řízení projektů a účetnictví | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Částky zadržené dodavatelem v transakcích výdajů projektu se v seznamu transakcí nezobrazují. |
| Přehled řízení projektů a účetnictví | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Mezipodniková faktura dodavatele je poškozená, když je zapnutá integrace faktur dodavatele. |
| Přehled řízení projektů a účetnictví | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Platební podmínky na fakturách projektu nefungují podle očekávání. |
| Přehled řízení projektů a účetnictví | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Po uvolnění zádržného dodavatele má zaúčtování dokladu další řádky, které jsou nesprávné. |
| Přehled řízení projektů a účetnictví | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Když je zaúčtován deník integrace Project Operations, operace selže z důvodu chybějících dimenzí pro účet, do kterého není zaúčtování prováděno. |
| Přehled řízení projektů a účetnictví | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Kartu **Projekt** nelze na nevyřízené faktuře dodavatele upravit, když je k položce přiřazena kategorie zásobování. |
| Přehled řízení projektů a účetnictví | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Pokud nejste přihlášeni do Project Operations Dataverse, chybí navigační podokno. |
| Přehled řízení projektů a účetnictví | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Když zaúčtujete výnos z faktury projektu v případu použitých záloh, dojde k problému, protože transakce na dokladu nejsou vyrovnané. |
| Přehled řízení projektů a účetnictví | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Vytvoření odhadu po zaúčtování návrhu faktury blokuje import řádků oprav. |
| Přehled řízení projektů a účetnictví | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Úprava plně fakturovaného milníku by neměla být možná. |
| Cestování a výdaje | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Když hledáte kategorii v mobilní aplikaci Výdaje, jsou viditelné všechny sestavy výdajů. |
| Cestování a výdaje | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Částky transakcí dodavatele a transakcí DPH, které jsou zaúčtovány z výdajů, které byly vytvořeny z transakce platební kartou, jsou nesprávné. |
| Cestování a výdaje | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Když obnovíte stránku **Sestava výdajů**, zobrazí se nepodstatné varování. |
| Cestování a výdaje | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Když odstraníte prozatímního schvalovatele a poté znovu odešlete sestavu výdajů prostřednictvím pracovního postupu, použije se nesprávný prozatímní schvalovatel. |
| Cestování a výdaje | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Chyba zaúčtování, která souvisí s nastavením ujetých kilometrů. |
