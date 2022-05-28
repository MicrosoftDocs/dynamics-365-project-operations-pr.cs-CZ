---
title: Co je nového, květen 2021 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Tento téma poskytuje informace o aktualizacích kvality, které jsou k dispozici v omezeném nasazení Project Operations z května 2021 pro scénáře založené na zdrojích / položkách, které nejsou na skladě.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d0af6d99a24619b3613a3aaa027404556b1b81c4
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723760"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového, květen 2021 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Toto téma se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

- Project Operations v prostředí Dynamics 365 Dataverse verze 4.10.0.186
- Řízení projektů a účetnictví v prostředí finančních a provozních aplikací verze 10.0.18

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

V této vydané verzi jsou zahrnuty následující funkce:

- [Režimy plánování](../project-management/scheduling-modes.md): Projektoví manažeři mohou definovat, zda by měl být projekt řízen pomocí fixního trvání, pevné práce nebo režimu plánování pevných jednotek.
- [Nastavení počet kilometrů pomocí úrovní sazeb najetých kilometrů](../expense/set-up-mileage.md): Aktualizujte úrovně rychlosti najetých kilometrů pro výkazy výdajů zaměstnanců.

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

Následující seznam ukazuje mapy duálního zápisu, které byly upraveny nebo přidány ve verzi Project Operations z května 2021.

| Mapování entity | Aktualizovaná verze | Komentáře |
| --- | --- | --- |
| Zdroj financování projektu (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Synchronizace platebních podmínek projektové smlouvy se zákazníkem. |
| Návrh faktury projektu V2 (faktury) | 1.0.0.3 | Synchronizace platebních podmínek proforma faktury. |
| Entita exportu řádku faktury dodavatele projektu integrace Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Aktualizace pro zvýšení kvality |
| Projekty V2 (msdyn\_projects) | 1.0.0.2 | Aktualizace pro zvýšení kvality |

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a finančních a provozních aplikacích. Pokud není aktivována nejnovější verze mapy, některé funkce a možnosti nemusí fungovat správně. Aktivní verzi mapy můžete vidět ve sloupci **Verze** na stránce **Duální zápis**. Novou verzi mapy můžete aktivovat výběrem **Verze mapy tabulky** výběrem nejnovější verze a poté uložením vybrané verze. Pokud jste přizpůsobili připravenou mapu tabulky, změny znovu použijte. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud narazíte na problém se spuštěním mapy, postupujte podle pokynů v části [Problém s chybějícími sloupci tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) příručky pro řešení potíží s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| **Oblast funkcí** | **Referenční číslo** | **Aktualizace pro zvýšení kvality** |
| --- | --- | --- |
| Fakturace a ceny | 2227635 | Hodnoty v polích **Skupina jednotek** a **Jednotka** mají výchozí hodnoty z produktu v mřížce **Odhady materiálu**. |
| Fakturace a ceny | 2234127 | Pole **ID úkolu** se nyní správně integruje do skutečných hodnot projektu Dataverse, když je zaúčtována faktura dodavatele. |
| Fakturace a ceny | 2235564 | Uložení řádku deníku zajistí, že měna zobrazená v položce řádku deníku po uložení odpovídá výchozí měně řádku. |
| Fakturace a ceny | 2246671 | Pokud transakce bude neúčtovatelná během fakturace, obrátí se původní nevyfakturovaný záznam prodeje a vytvoří se nový nevyfakturovaný záznam prodeje jako nezúčtovatelný. |
| Fakturace a ceny | 2264042 | Platná oprava faktury nesmí být blokována, pokud existuje údaj opravy faktury, který není v prostředí platný. |
| Fakturace a ceny | 2146367 | Mapování dvojitého zápisu záhlaví faktury projektu je rozšířeno o platební podmínky. |
|   Správa příležitostí | 2086888 | Nepřidávejte role a kategorie, které jsou deaktivovány, než zkopírujete nabídku do fakturovatelných rolí a kategorií nově zkopírované nabídky. |
|   Správa příležitostí | 2234376 | Pole jen pro čtení jsou v mřížce **Odhady materiálu** zašedlá. |
|   Správa příležitostí | 2238337 | Cenovou nabídku založenou na kontaktu lze uložit, i když není spojena s ceníkem projektu. |
|   Správa příležitostí | 2239810 | Uzavření nabídky jako ztracené také uzavře přidružený projekt a zruší veškeré rezervace. |
| Plánování a sledování projektu | 2099559 | Přidána další ověření stavu systému před otevřením mřížky **Projektové úkoly**. |
| Plánování a sledování projektu | 2178987 | Opravena přechodná chyba, ke které došlo při výběru **Další fáze** na stránce **Projekt**. |
| Správa zdrojů | 2224817 | Funkce pro rozšíření rezervací má jako výchozí hodnotu správný stav rezervace. |
| Časový záznam | 2202476 | Stránka **Zadání času** nyní používá ovládání reakce na mřížku a opravuje problémy, jako je například nesoulad mřížky. |
| Časový záznam | 2223377 | Zadání času je před částí **Související** na stránce **Rezervovatelný zdroj** skryto, aby nedošlo k záměně s použitelností. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Řízení projektů a účetnictví v Dynamics 365 Finance

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Přehled řízení projektů a účetnictví | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations pro scénáře na základě prostředků: nemůžete převést nabídku na vyhranou kvůli chybě integrace. |
| Přehled řízení projektů a účetnictví | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: objeví se chyba, když se pokusíte přidružit řádek smlouvy k ID projektu z důvodu kontroly překrývajících se řádků smlouvy a typů transakcí. |
| Přehled řízení projektů a účetnictví | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | Entita **ProjCDSProjectContractEntity** nastaví fakturační adresu zdroje financování z jiného zákazníka. |
| Cestování a výdaje | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Při nastavování počtu najetých kilometrů může dojít k chybě zveřejňování. |
| Cestování a výdaje | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Funkce **Rozdělit na osobní** nefunguje pro transakce výdajů v cizí měně. |
| Cestování a výdaje | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Rozbalovací nabídka kategorie výdajů zobrazuje nesprávné kategorie pro delegáty bez ohledu na to, zda jsou nastaveni jako zdroj. |
| Cestování a výdaje | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Sestavu mezipodnikových výdajů nemůžete uložit kvůli chybě **Ověření zdroje/kategorie**. |
| Cestování a výdaje | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Chybný výpočet najetých kilometrů v účtování výkazu výdajů má rozdělené řádky. |
| Cestování a výdaje | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Nemůžete zaúčtovat mezipodnikový výdajový výkaz, když je zahrnuta DPH a typ offsetového účtu je u platební metody **Pracovník**. |
| Cestování a výdaje | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Vrácení zpět datové entity **TrvRequisitionLine** a přidruženého jedinečného indexu. |
| Cestování a výdaje | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Sestava výdajů podporuje vytváření a aktualizaci řádků zdrojových dokumentů. |
| Cestování a výdaje | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | V mezipodnikovém scénáři se zobrazí nesprávný deník dílčí hlavní knihy, pokud je DPH zaúčtována cílové právnické osobě. |
| Cestování a výdaje | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: odhad výdajů není odstraněn z Finance, když je odstraněn z Dataverse. |
| Cestování a výdaje | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Pokud je kategorie výdajů neprojektovou kategorií, finanční dimenze vybrané ve stránce **Výdaje** se nezkopírují do sestavy výdajů. |
