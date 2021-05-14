---
title: Co je nového v prosinci 2020 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Tohle téma poskytuje informace o aktualizacích pro zvýšení kvality, které jsou k dispozici ve verzi Project Operations z prosince 2020 pro scénáře založené na zdrojích / položkách, které nejsou na skladě.
author: sigitac
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5927a638fe8e454aecc9ce8dfc0871ed51d09f5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291926"
---
# <a name="whats-new-december-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového v prosinci 2020 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Toto téma se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.5.0.134
- Řízení projektů a účetnictví v prostředí Dynamics 365 Finance verze 10.0.15

Informace o aktualizaci na toto vydání najdete v části [Aktualizace Project Operations v prostředí Finance](ur5-nonstocked-installation.md).

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi
V této vydané verzi jsou zahrnuty následující funkce:

  - [Mezipodniková fakturace](../project-accounting/intercompany-invoicing-overview.md) 
  - [Zákaznické zálohy](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Aktualizace Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| Oblast funkcí                    | Referenční číslo | Aktualizace pro zvýšení kvality                                                                                                                                               |
|---------------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fakturace a ceny             | 1986009          | Ručně vytvořené řádky deníku mají nekonzistentní výkon, pokud jsou potvrzeny před propojením nebo odpojením projektu od řádku smlouvy                     |
| Fakturace a ceny             | 2028174          | Aktualizace podrobností řádku faktury by se měla řídit logikou deníku oprav                                                                                  |
| Fakturace a ceny             | 2028315          | Upravitelné opravy chování vnořené mřížky                                                                                                                        |
| Fakturace a ceny             | 2031070          | Úprava podrobností řádku opravné faktury musí odpovídat logice deníku oprav                                                                              |
| Fakturace a ceny             | 2034186          | Musí být schopen aktualizovat projekt na řádku smlouvy                                                                                                        |
| Fakturace a ceny             | 2034206          | Stav vyrovnání musí být nastaven během skutečného zrušení při odpojení projektu od řádku smlouvy                                                        |
| Fakturace a ceny             | 2040871          | Povolit aktualizace buněk jednotky a skupiny jednotek v mřížce odhadů výdajů                                                                                       |
| Fakturace a ceny             | 2053754          | Skutečné hodnoty vytvořené z úprav faktury nejsou označeny stavem úpravy a stavem fakturace                                                                |
| Fakturace a ceny             | 2057874          | Správné propojení transakcí vytvořené během úpravy podrobností řádku faktury                                                                                     |
| Fakturace a ceny             | 2057875          | Správné původy transakcí vytvořené během úpravy podrobností řádku faktury                                                                                        |
| Fakturace a ceny           | 2057944          | Stav nepřekročení nastavený jako potvrzený pro skutečnosti, které nejsou připraveny k fakturaci z opravy faktury                                             |
| Fakturace a ceny           | 2066169          | Aktualizujte účetní datum negativního nevyfakturovaného záznamu prodeje při integraci pomocí duálního zápisu                                                            |
| Fakturace a ceny           | 2067622          | Při generování milníků by se měla zobrazit ikona zpracování                                                                                                |
| Fakturace a ceny           | 2067624          | Smluvní částka by měla být při generování milníků označena jako doporučená společností                                                                      |
| Fakturace a ceny           | 2086880          | Skryjte tlačítko **Návrh** na pásu karet pro řádky nabídky založené na projektu                                                                                                |
| Fakturace a ceny           | 2098140          | Zobrazit tlačítko **Správná faktura** pro integrovaná prostředí                                                                                             |
| Nasazení a konfigurace  | 2101152          | Nové prostředí vytvořené pomocí šablony Project Operations z centra pro správu Power Platform musí mít provedené všechny operace po instalaci               |
| Správa příležitostí        | 2086601          | Role a kategorie, které jsou deaktivovány, by se neměly kopírovat do seznamu účtovatelných rolí a účtovatelných kategorií na řádcích nabídky a řádcích smluv |
| Plánování a sledování projektu | 1949065          | Viditelnost dat funguje správně při 200% zvětšení                                                                                                                   |
| Plánování a sledování projektu | 2046317          | Možnost přejmenovat entitu projektu v Project Operations                                                                                   |
| Plánování a sledování projektu | 2057171          | Aktualizovaná chybová zpráva, když je pole **Datum zahájení projektu** prázdné na stránce **Projekt**                                                           |
| Plánování a sledování projektu | 2057197          | Kopie řádku odhadu s odkazem na úlohu není podporována                                                                                                     |
| Plánování a sledování projektu | 2060687          | Varování časového pásma nyní po určité době zmizí                                                                                                      |
| Řízení zdrojů           | 1832887          | ID výchozí kategorie prostředků musí být statické, aby bylo zajištěno opakovatelné načítání dat pro Dataverse a prostředí Finance                                                 |
| Čas a výdaje              | 2081793          | **Název kategorie výdajů** musí být mapován na pole **Popis kategorie výdajů** v aplikaci Finance and Operations                                                  |
| Čas a výdaje              | 2034882          | Tlačítko **Nový** se zobrazí dvakrát na panelu příkazů pro zadání času, když je nainstalován Dynamics 365 Field Service                                          |
| Čas a výdaje              | 2056028          | Aktualizace stránky **Úpravy času**, aby obsahovala časovou osu                                                                                                              |
| Čas a výdaje              | 1983747          | Tabulka zadávání času ukazuje další data                                                                                                                   |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Přehled řízení projektů a účetnictví v Dynamics 365 Finance

| Oblast funkcí                        | Referenční číslo | Aktualizace pro zvýšení kvality                                                                                                                                                                                                                                                   |
|-------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Přehled řízení projektů a účetnictví | [441680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441680)           | Blokování úprav pro vrácení požadavku na položku                                                                                                                                                                                                        |
| Přehled řízení projektů a účetnictví | [446498](https://fix.lcs.dynamics.com/Issue/Details/?bugId=446498)           | Poznámky formuláře se nezobrazují na formátovaných projektových fakturách                                                                                                                                                                                                          |
| Přehled řízení projektů a účetnictví | [453407](https://fix.lcs.dynamics.com/Issue/Details/?bugId=453407)           | MEXICO CFDI 33 pro projektové faktury nemá povoleno aktualizovat způsob platby z návrhu faktury                                                                                                                                                           |
| Přehled řízení projektů a účetnictví | [458149](https://fix.lcs.dynamics.com/Issue/Details/?bugId=458149)           | Parametr, který automaticky nastavuje účetní datum na otevřené období, není v deníku **Integrace**                                                                                                                                                             |
| Přehled řízení projektů a účetnictví | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Položky nabídky Prognóza nejsou viditelné na stránce seznamu **Projekty**                                                                                                                                                                                                      |
| Přehled řízení projektů a účetnictví | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Nelze otevřít **Prohlášení o projektu** > **Transakce a prognóza**                                                                                                                                                                                                      |
| Přehled řízení projektů a účetnictví | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Odebrání a čtení přiřazení prostředků zdvojnásobí položky prognózy projektu v aplikaci Finance                                                                                                                                                                   |
| Přehled řízení projektů a účetnictví | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468)           | Nelze vytvořit odhady projektu v Dataverse, aniž byste na projektu měli řádek smlouvy                                                                                                                                                                 |
| Přehled řízení projektů a účetnictví | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Eliminace selže kvůli chybě nerovnováhy poukazu, když se liší měna společnosti a měna transakce                                                                                                                                            |
| Přehled řízení projektů a účetnictví | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382)           | Filtr pro stav faktury v zaúčtovaných transakcích projektu u projektů s pevnou cenou nefunguje                                                                                                                                                            |
| Přehled řízení projektů a účetnictví | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Nelze aktualizovat datum zahájení úkolu v Dataverse                                                                                                                                                                                                                    |
| Přehled řízení projektů a účetnictví | [507172](https://fix.lcs.dynamics.com/Issue/Details/?bugId=507172)           | Je možné odstranit řádky návrhu faktury v integrovaném scénáři Project Operations                                                                                                                                                                                    |
| Přehled řízení projektů a účetnictví | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989)           | Je možné odstranit řádky návrhu faktury v integrovaném scénáři Project Operations                                                                                                                                                                                    |
| Přehled řízení projektů a účetnictví | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Zabránit povolení funkce více řádků smlouvy bez integrace Dataverse                                                                                                                                                                                        |
| Přehled řízení projektů a účetnictví | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527)           | Fakturovaný výnos na obrazovce odhadu je nulový (0), když fakturace na účet = zisk a ztráta                                                                                                                                                                          |
| Přehled řízení projektů a účetnictví | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364)           | WIP - zaúčtování prodejní hodnoty ve fakturaci mezipodnikového projektu vybere neočekávaný účet                                                                                                                                                                           |
| Přehled řízení projektů a účetnictví | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799)           | Nelze provést rozpoznávání odhadu / výnosu s povoleným Project Operations                                                                                                                                                                         |
| Cestování a výdaje                | [378738](https://fix.lcs.dynamics.com/Issue/Details/?bugId=378738)           | Výdaje zadané delegátem jsou vráceny uživateli výdajů, nikoli delegátovi                                                                                                                                                                                           |
| Cestování a výdaje                | [409489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=409489)           | Delegovaný uživatel pracovního postupu sestavy výdajů odesílající pracovní tok není identifikován jako původce pracovního postupu                                                                                                                                                             |
| Cestování a výdaje                | [464658](https://fix.lcs.dynamics.com/Issue/Details/?bugId=464658)           | Výchozí dimenze v přepisech právnických osob nefungují na mezipodnikových výkazech výdajů                                                                                                                                                                    |
| Cestování a výdaje                | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892)           | Problém s výpočtem redukce jídla za poslední den pro kategorii výdajů na diety                                                                                                                                                                                    |
| Cestování a výdaje                | [473646](https://fix.lcs.dynamics.com/Issue/Details/?bugId=473646)           | Pole **Částka k opravě** na stránce **Cestovní žádost** se neaktualizuje po odstranění řádkové položky výdajů ze sestavy výdajů spojené s cestovní žádostí                                                                                                       |
| Cestování a výdaje                | [474396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=474396)           | Zpráva o výdajích ověřila zásadu po odeslání do pracovního postupu                                                                                                                                                                                           |
| Cestování a výdaje                | [475777](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475777)            | Potvrzení o cestovních výdajích se pro delegáta vstupu nezobrazuje správně                                                                                                                                                                                            |
| Cestování a výdaje                | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714)            | Typ výdajů na zaměstnance nezobrazuje rozepsané výdaje, když je jazyk uživatele nastaven na es-MX                                                                                                                         |
| Cestování a výdaje                | [477831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477831)            | Výkaz výdajů umožňuje zadat nesprávnou podkategorii pro kategorii výdajů                                                                                                                                                                                       |
| Cestování a výdaje                | [478630](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478630)            | Odsouhlasení zálohy v hotovosti se sestavou výdajů nefunguje podle očekávání, pokud je částka sestavy výdajů vyšší než částka zálohy v hotovosti                                                                                                           |
| Cestování a výdaje                | [486680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486680)            | Problémy s výkonem s dotazy souvisejícími s ProjProjectLookup. Zákazník je blokován, protože provedení dotazu trvá dlouho.                                                                                                                     |
| Cestování a výdaje                | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531)            | Zprávy o výdajích zveřejněné pomocí se zapnutými vobami **Povolit seskupování transakcí na základě offsetového platebního účtu** a **Oprava účetního data při zaúčtování** ukazuje, že účetní data nejsou seskupena v tabulce **Rozdělení účetnictví**, která ovlivňuje záznamy DPH |
| Cestování a výdaje                | [491759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491759)            | Importované transakce kreditní kartou v cizí měně vytvářejí nesprávné transakce dodavatele, pokud se používá **Zpětná sazba DPH** na řádcích výkazu výdajů                                                                                                                     |
| Cestování a výdaje                | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175)            | Sestavu mezipodnikových výdajů nelze vytvořit, pokud je ID projektu přidáno na úrovni záhlaví                                                                                                                                                                 |
| Cestování a výdaje                | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491)            | Problém s platbou výdajů, když je částka výdajů vyšší než částka v hotovosti                                                                                                                                                                          |
| Cestování a výdaje                | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556)            | Informace o ID projektu v sestavě mezipodnikových výdajů jsou prázdné, pokud je role uživatele přiřazena konkrétní organizaci                                                                                                                                           |
| Cestování a výdaje                | [513845](https://fix.lcs.dynamics.com/Issue/Details/?bugId=513845)            | Pracovní postup automatického zaúčtování sestavy výdajů je dokončen, ale faktura není zaúčtována                                                                                                                                                                                          |

### <a name="regulatory-updates"></a>Povinné aktualizace
Informace o povinných aktualizacích pro aplikace Finance and Operations viz [Povinné aktualizace](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Můžete se také přihlásit do LCS a zobrazit plánované povinné aktualizace pomocí nástroje pro vyhledávání problémů. Hledání problému vám umožňuje vyhledávat podle země, typu funkce a vydání.


[!INCLUDE[footer-include](../includes/footer-banner.md)]