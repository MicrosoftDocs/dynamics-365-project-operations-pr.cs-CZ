---
title: Co je nového, duben 2021 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations z dubna 2021 pro scénáře založené na zdrojích / neskladových položkách.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a060bdc4e4c9f37ec666b1cf4d078986ad1571db
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912416"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového, duben 2021 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Tento článek se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.9.0.221
- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.17

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

V této vydané verzi jsou zahrnuty následující funkce:

- Neuskladněné materiály pro projekty. Mezi klíčové funkce patří:
  - Odhad a stanovení ceny neuskladněných materiálů během prodejního cyklu projektu. Více informací najdete v tématu [Nastavení nákladových a prodejních sazeb pro produkty katalogu - omezené](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Sledování využití neskladovaných materiálů během dodání projektu. Více informací najdete v tématu [Záznam využití materiálu na projektech a projektových úkolech](../material/material-usage-log.md).
  - Fakturace použitého materiálu, který není na skladě. Více informací najdete v tématu [Správa nedokončené fakturace](../proforma-invoicing/manage-billing-backlog.md).
  - Informace o konfiguraci této funkce najdete v části [Konfigurace neskladovaných materiály a nevyřízených faktur dodavatele](../procurement/configure-materials-nonstocked.md)
- Fakturace na základě úkolů: Přidána možnost přidružit projektové úkoly k řádkům projektových smluv, čímž je vystavíte stejné metodě fakturace, četnosti fakturace a zákazníkům jako na řádku smlouvy. Toto přidružení zajišťuje přesnou fakturaci, účetnictví, odhad výnosů a uznání tak, aby fungovaly v souladu s tímto nastavením na projektových úkolech.
- Nová rozhraní API v Dynamics 365 Dataverse umožňují operace vytváření, aktualizace a odstraňování **entit plánování**. Více informací najdete v tématu [Používání rozhraní Schedule API k provádění operací s entitami plánování](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

Následující seznam ukazuje mapy duálního zápisu, které byly upraveny nebo přidány ve verzi Project Operations z dubna 2021.

| **Mapování entity** | **Aktualizovaná verze** | **Komentáře** |
| --- | --- | --- |
| Skutečné hodnoty integrace Project Operations (ms\_dynactuals) | 1.0.0.14 | Mapa byla upravena tak, aby synchronizovala skutečné hodnoty materiálu. |
| Entita integrace Project Operations pro odhady výdajů (msdyn\_estimateslines) | 1.0.0.2 | Přidána synchronizace řádků projektové smlouvy do finančních a provozních aplikací pro podporu fakturace na základě úkolů. |
| Entita integrace Project Operations pro odhady hodin (msdyn\_resourceassignments) | 1.0.0.5 | Přidána synchronizace řádků projektové smlouvy do finančních a provozních aplikací pro podporu fakturace na základě úkolů. |
| Tabulka integrace Project Operations pro odhady materiálu (msdyn\_estimatelines) | 1.0.0.0 | Nová tabulková mapa pro synchronizaci odhadů materiálu z Dataverse do finančních a provozních aplikací. |
| Entita exportu faktury dodavatele projektu integrace Project Operations (msdyn\_projectvendorinvoices) | 1.0.0.0 | Nová tabulková mapa pro synchronizaci hlaviček faktury dodavatelů z finančních a provozních aplikací do Dataverse. |
| Entita exportu řádku faktury dodavatele projektu integrace Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Nová tabulková mapa pro synchronizaci řádků faktury dodavatelů z finančních a provozních aplikací do Dataverse. |

Vždy byste měli spustit nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a řešení Finance a Operations. Pokud není aktivována nejnovější verze mapy, některé funkce a možnosti nemusí fungovat správně. Aktivní verzi mapy můžete vidět ve sloupci **Verze** na stránce **Duální zápis**. Novou verzi mapy můžete aktivovat výběrem **Verze mapy tabulky** výběrem nejnovější verze a poté uložením vybrané verze. Pokud jste přizpůsobili připravenou mapu tabulky, změny znovu použijte. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud narazíte na problém se spuštěním mapy, postupujte podle pokynů v části [Problém s chybějícími sloupci tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) příručky pro řešení potíží s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations v Dynamics 365 Dataverse

| **Oblast funkcí** | **Referenční číslo** | **Aktualizace pro zvýšení kvality** |
| --- | --- | --- |
| Fakturace a ceny | 2124532 | Tlačítko **Opravit fakturu** se zobrazí na proforma faktuře, když je na původní faktuře částka záloh nebo použitá částka záloh. Tlačítko se zobrazuje pouze v prostředí s verzí aplikace Finance 10.0.19 nebo vyšší. |
| Fakturace a ceny | 2224568 | Přidaná logika povolující přizpůsobení, která zahrnuje vyvolání doplňku pro potvrzení faktury. |
| Fakturace a ceny | 2101098 | Vylepšena logika výchozích polí proforma faktury: **Fakturační adresa**, **Fakturační adresa – název** a **Platební podmínky** nyní přebírají výchozí hodnotu z příslušného záznamu zákazníka projektové smlouvy. |
| Fakturace a ceny | 2021413 | Aktualizována pole **Skutečná cena** a **Prodeje** u entity **Úkol**, která nově zahrnují hodnoty prodeje z nevyfakturovaných a fakturovaných výdajů na úkoly. |
| Fakturace a ceny | 2182110 | Při kopírování projektové smlouvy se ID řádku smlouvy znovu vygeneruje v cílové projektové smlouvě, aby se zajistilo, že je jedinečné. |
| Správa příležitostí | 2186741 | Přidaná ověření, která zajištují, že u polí **Původ** a **Typ transakce** nelze aktualizovat existující podrobnosti řádku nabídky. |
| Správa příležitostí | 2191353 | Milníky nesmí být vytvářeny na řádku smlouvy s časem a materiálem. |
| Správa příležitostí | 2216956 | Opraveny problémy ve funkci **Aktualizovat ceny**. |
| Plánování a sledování | 2182979 | Vylepšena funkce kopírování projektu, aby bylo zajištěno, že řádky odhadu výdajů budou zkopírovány z původního projektu. |
| Plánování a sledování | 2184144 | Vylepšena funkce kopírování projektu, aby bylo zajištěno, že název pozice zdroje bude zkopírován z původního projektu. |
| Plánování a sledování | 2184799 | Kopie projektu: Zpřísněna kontrola zajišťující, že odhadované datum zahájení nelze během kopírování změnit. |
| Plánování a sledování | 2185134 | Kopie projektu: Odhadované datum zahájení cílového projektu je nastaveno na dnešní datum. |
| Plánování a sledování | 2196373 | Kopie projektu: Zajištění, aby záznamy projektového manažera a člena týmu nebyly v projektovém týmu duplikovány. |
| Plánování a sledování | 2211833 | Kopie projektu: Přiřazení zdrojů se zkopírují z úlohy zdrojového projektu do cílového projektu. |
| Plánování a sledování | 2186541 | Opraveny problémy v mřížce **Odhady** při seskupování podle zdrojů. |
| Plánování a sledování | 2166906 | Kategorie transakcí z úkolu musí být zkopírována do entity **Přiřazení zdrojů**. |
| Správa zdrojů | 2125362 | Opraveny problémy při vytváření obecného člena týmu pomocí metody přidělování podle hodin. |
| Čas a výdaje | 2113603 | Opraven problém související s přizpůsobením při odstraňování atributů ze stránky **Zadání času**. Systém nyní před přístupem s využitím skriptu zkontroluje, zda atribut na stránce existuje. |
| Čas a výdaje | 2204377 | Zkopírované časové rozvrhy se musí automaticky zobrazit, když během zadávání času vyberete možnost **Kopírovat týden**. |
| Čas a výdaje | 2209059 | Pole **Stav** lze u časových údajů Dynamics 365 Field Service upravit. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Řízení projektů a účetnictví v Dynamics 365 Finance

| **Oblast funkcí** | **Referenční číslo** | **Aktualizace pro zvýšení kvality** |
| --- | --- | --- |
| Přehled řízení projektů a účetnictví | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Odstranění zpětného odhadu nefunguje v části **Pravidelné**.  |
| Přehled řízení projektů a účetnictví | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Funkce **Úprava účetnictví** vytváří problém u účtů hlavní knihy, které mají vybranou možnost **Nepovolit ruční zadání**. |
| Přehled řízení projektů a účetnictví | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Přidána obchodní logika ke zpracování opravných faktur, včetně částky zálohy nebo použité částky zálohy. |
| Přehled řízení projektů a účetnictví | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | WIP - zaúčtování prodejní hodnoty ve fakturaci mezipodnikového projektu vybere neočekávaný účet. |
| Přehled řízení projektů a účetnictví | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Při práci se zálohami v Project Operations způsobí změna výchozího projektu ve smlouvě po fakturaci záloh problémy s příchozími odpočty. |
| Přehled řízení projektů a účetnictví | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | V aplikaci Project Operations by odebrání projektu ze smlouvy mělo v případě potřeby obnovit výchozí projekt smlouvy. |
| Přehled řízení projektů a účetnictví | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | V Project Operations se v seznamu **Přidat řádek** na mezipodnikové faktuře zobrazují nesprávné výdajové řádky. |
| Přehled řízení projektů a účetnictví | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | V Project Operations není stránka **Kupní smlouva** viditelná v právních entitách Finance, které jsou integrovány s Project Operations. |
| Přehled řízení projektů a účetnictví | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Kvůli chybě integrace Dataverse nemůžete v Project Operations převést nabídku na získaný obchod. |
| Přehled řízení projektů a účetnictví | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | Entita **ProjCDSProjectContractEntity** může nastavit fakturační adresu zdroje financování z jiného zákazníka.  |
| Přehled řízení projektů a účetnictví | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | V Project Operations nejsou při vytváření zaúčtování faktury pro transakci vybrány žádné dimenze. |
| Cestování a výdaje | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Zůstatek hotovostní zálohy se neaktualizuje u sestavy výdajů, pokud je schválen a zaúčtován řádek po řádku. |
| Cestování a výdaje | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Daně pro sestavy rozepsaných mezipodnikových výdajů se nepočítají správně. |
| Cestování a výdaje | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Na nové verzi stránky **Sestavy mezipodnikových výdajů** jsou zobrazena další pole související s projekty. |
| Cestování a výdaje | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Na příjemkách záhlaví sestav výdajů se objeví nesprávná chybová zpráva. |
| Cestování a výdaje | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Sestava výdajů je nesprávně zaúčtována v mezipodnikovém scénáři, pokud je daň z prodeje zaúčtována cílové právnické osobě. |
| Cestování a výdaje | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Data odeslání sestavy nejsou vytištěna na sestavách schválených výdajů. |
| Cestování a výdaje | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Pole **Datum schválení** a **Datum zamítnutí** nejsou po schválení výdajů vyplněna. |
| Cestování a výdaje | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Cestovní žádanku vytvořenou pro jednoho pracovníka lze použít v sestavě výdajů jiného pracovníka. |
| Cestování a výdaje | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kategorie výdajů jsou uzamčeny, když přidáváte nový řádek výdajů. |
| Cestování a výdaje | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Rozepsání již rozdělených řádků sestavy výdajů má za následek neúplné zaúčtování dokladu v části Závazky \ Hlavní kniha a vyvolá chybu v Průzkumníku zdrojů účtování, protože je duplikován údaj **TRVEXPTRANS.SOURCEDOCUMENTLINE**. |
| Cestování a výdaje | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Zásady cestovních žádanek nefungují podle očekávání. |
| Cestování a výdaje | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Název účtu dodavatele se nezobrazuje v zaúčtovaných projektových transakcích na sestavách výdajů. |
| Cestování a výdaje | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | V Project Operations nemůžete schválit čas s úkolem u mezipodnikového projektu. |
| Cestování a výdaje | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Kategorie vrácení hotovostní zálohy neaktualizuje zůstatky hotovostní zálohy, když jsou zaúčtovány. |
| Cestování a výdaje | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Prodejní cena se nesprávně počítá ve výkazech výdajů, které byly vytvořeny v cizí měně pomocí importovaných transakcí kreditní kartou a jsou přidruženy k projektu. |
| Cestování a výdaje | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Vrácení zpět datové entity **TrvRequisitionLine** a přidruženého jedinečného indexu. |
| Cestování a výdaje | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Přidáno instrumentace do generování entity **SOURCEDOCUMENTLINE**. |
| Cestování a výdaje | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | V mezipodnikovém scénáři se zobrazí špatný deník dílčí hlavní knihy, pokud je daň z prodeje zaúčtována cílové právnické osobě. |
| Cestování a výdaje | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | V Project Operations nejsou odhady výdajů odstraněny z Finance, když jsou odstraněny z Dataverse. |
| Cestování a výdaje | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Pokud je kategorie výdajů neprojektovou kategorií, finanční dimenze vybrané ve stránce **Výdaje** se nezkopírují do sestavy výdajů. |
