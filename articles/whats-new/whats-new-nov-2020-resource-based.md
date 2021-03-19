---
title: Co je nového v listopadu 2020 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Tohle téma poskytuje informace o aktualizacích pro zvýšení kvality, které jsou k dispozici ve verzi Project Operations z listopadu 2020 pro scénáře založené na zdrojích / položkách, které nejsou na skladě.
author: sigitac
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f8e9bce6612e617785264470b7946ffc4795a621
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291836"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového v listopadu 2020 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Toto téma se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

- Project Operations v prostředí CDS verze 4.4.0.70
- Řízení projektů a účetnictví v prostředí Dynamics 365 Finance verze 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Aktualizace Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

### <a name="project-operations-on-cds"></a>Project Operations v CDS

| Oblast funkcí                 | Referenční číslo | Aktualizace pro zvýšení kvality                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Správa příležitostí       | 2036993          | Řádek odhadu a řádky smlouvy přiřazení zdrojů se aktualizují při získání nabídek, když je typ nabídky **Všechny úkoly**.                                                 |
| Fakturace a ceny          | 2070392          | Řádky projektové smlouvy na faktuře se vždy zvyšují při výběru **Aktualizovat transakce faktury**.                                                                         |
| Plánování projektu             | 2043336          | Nelze odstranit záznam člena projektového týmu.                                                                                                                                  |
| Plánování projektu             | 2046013          | Nekonzistentní chování sloupců značek odhadů během načítání vs. při změně typu časové fáze.                                                                                   |
| Plánování projektu             | 2046647          | Počáteční a koncové časy jsou posunuty o hodinu, když jsou požadavky na zdroje generovány ze členů projektového týmu.                                                                      |
| Plánování projektu             | 2053879          | (Podle nadcházejícího uvedení CDS) PublishUnassignedAssignments přeruší pokus o uložení úkolu, když se zobrazí chyba „Hodnota předaná pro ConditionOperator.In je prázdná.“                       |
| Plánování projektu             | 2055501          | Nezadání hodnoty **Datum zahájení projektu** způsobí chybu v plánu.                                                                                                      |
| Plánování projektu             | 2066817          | Nelze vytvořit obecný zdroj pomocí nástroje pro výběr lidí na kartě **Úkoly**.                                                                                                   |
| Plánování projektu             | 2067034          | Tlačítko **Zobrazit podrobnosti** není k dispozici na stránce **Podrobnosti úkolu**.                                                                                                       |
| Řízení zdrojů          | 2046667          | Obecní členové týmu se neodstraní ani po splnění všech zdrojů.                                                                                                    |
| Položka času a rychlého výdaje | 2047499          | Tlačítko **Nový** na stránce Časový záznam otevře stránku **Nový e-mailový podpis**.                                                                                               |
| Položka času a rychlého výdaje | 2059859          | Při vytváření položky výdajů se neočekávaně otevře vyskakovací okno.                                                                                                                         |
| Ostatní                        | 2044181          | (Odinstalování nákupní objednávky) Při pokusu o odinstalaci základních řešení msdyn_ProjectServiceCore_Patch a msdyn Project Service dojde k chybě „Záznam není k dispozici“.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Přehled řízení projektů a účetnictví v Dynamics 365 Finance

| Oblast funkcí        | Referenční číslo | Aktualizace pro zvýšení kvality                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Uznání výnosů | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Odhdované procento dokončení projektu je nesprávné, když smlouva používá cizí měnu a metodu procenta průběhu dokončení práce.                     |
| Uznání výnosů | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Nelze zaúčtovat odhady metodou dokončení **Skutečné náklady**.                                                                                                    |
| Uznání výnosů | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Eliminace selže kvůli chybě nerovnováhy poukazu, když se liší měna společnosti a měna transakce.                                              |
| Řízení výdajů  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Pro uživatele, kteří nejsou správci, se hodnoty vyhledávání pro sloupce výdajových řádků, jako je **ID projektu** a **Kategorie výdajů**, nezobrazují správně v rámci datového konektoru. |
| Řízení výdajů  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Výchozí vlastnost řádku se nezobrazuje pro kategorie výdajů.                                                                                                         |
| Řízení výdajů  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Integrace výdajů musí zahrnovat vlastnost řádku ze sestavy výdajů.                                                                                             |
| Fakturace           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Nelze zaúčtovat návrhy faktur projektu kvůli chybové zprávě, která říká, že kombinace FD nebyla ověřena.                                                    |
| Fakturace           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Nelze zobrazit transakce ze stránky s podrobnostmi o **faktuře**.                                                                                                              |
| Fakturace           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Řádky návrhu faktury lze odstranit.                                                                                                                                  |
| Účetnictví projektu  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Položky nabídky **Prognóza** nejsou viditelné na stránce seznamu **Projekty**.                                                                                                   |
| Účetnictví projektu  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Nelze otevřít **Prohlášení o projektu**   > **Transakce a prognóza**.                                                                                                       |
| Účetnictví projektu  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Úprava účetnictví** není povoleno pro fakturované projektové transakce.                                                                                                  |
| Účetnictví projektu  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Účetní údaje nejsou zahrnuty v tabulce **ProjCDSActualsImport**, když není zaúčtován deník **Integrace**.                                                  |
| Účetnictví projektu  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Položka prognózy projektu se zdvojnásobí, když odeberete a znovu načtete přiřazení zdrojů.                                                                            |
| Účetnictví projektu  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Výběr odkazu ID projektu neotevře adresu URL přímého odkazu na CDS.                                                                                                         |
| Účetnictví projektu  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Nelze aktualizovat datum zahájení úkolu v CDS.                                                                                                                           |
| Účetnictví projektu  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Povolením funkce není možné použít více řádků smlouvy bez integrace CDS.                                                                                   |

### <a name="regulatory-updates"></a>Povinné aktualizace
Informace o povinných aktualizacích pro aplikace Finance and Operations viz [Povinné aktualizace](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Můžete se také přihlásit do LCS a zobrazit plánované povinné aktualizace pomocí nástroje pro vyhledávání problémů. Hledání problému vám umožňuje vyhledávat podle země, typu funkce a vydání.


[!INCLUDE[footer-include](../includes/footer-banner.md)]