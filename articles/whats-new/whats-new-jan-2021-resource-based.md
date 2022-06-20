---
title: Co je nového, leden 2021 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations z ledna 2021 pro scénáře založené na zdrojích / neskladových položkách.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: cd20ba47a45593e7694234b4f58aecd79b1c3736
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910644"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového, leden 2021 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_


Tento článek se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

  - Project Operations v prostředí Dataverse verze 4.6.0.154
  - Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.16

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| **Oblast funkcí** | **Referenční číslo** | **Aktualizace pro zvýšení kvality** |
| --- | --- | --- |
| **Nasazení a konfigurace** | 2106818 | Opraveno přejmenování webového zdroje, které způsobovalo problémy spojené s přizpůsobením stránky. |
| **Fakturace a ceny** | 2091908 | Opravena viditelnost možností **Uzamčení ceny** a **Použít aktuální ceny** na stránce **Faktura**, když je Project Operations nainstalován společně s Dynamics 365 Field Service. |
| **Fakturace a ceny** | 2103058 | Aktualizovaný **Součty projektu**, aby zvládaly nulové hodnoty skutečných nákladů na úkol. |
| **Fakturace a ceny** | 2116100 | Vylepšené chybové zprávy používané s touto funkcí **Správné záznamy skutečností**. |
| **Fakturace a ceny** | 2116129 | Vylepšená viditelnost odhadů výdajů na kartě **Odhady** na stránce **Projekty**. |
| **Fakturace a ceny** | 2119112 | Pevná agregace skutečných prodejů a skutečných nákladů při různých směnných kurzech. |
| **Fakturace a ceny** | 2134705 | Opravena chyba „Nelze přečíst vlastnost **getResourceString** z nedefinováno“, když se otevře stránka **Faktura** a nainstaluje se Field Service. |
| **Správa příležitostí** | 2022195 | Fakturační mřížka podle úkolů na stránce **Projekt** obsahuje ikonu označující, že s daným úkolem je spojena smlouva nebo nabídka. |
| **Správa příležitostí** | 2029135 | Opravená chyba obchodního procesu, ke které dochází, když se uživatel pokusí otevřít řádek faktury na potvrzené faktuře, která má fakturovanou částku zálohy. |
| **Správa příležitostí** | 2040713 | Opravená chyba skriptu, ke které dochází při vytváření faktury ze smlouvy a je nainstalováno Field Service. |
| **Plánování a sledování projektu** | 2090202 | Obchodní pravidla, která se již nepoužívají, byla označena jako **Zastaralé**. |
| **Čas a výdaje** | 2091249 | Přesnější kontroly, aby uživatelé nemohli změnit úkol u odeslaného nebo schváleného časového záznamu. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Řízení projektů a účetnictví v Dynamics 365 Finance

| **Oblast funkcí** | **Referenční číslo** | **Aktualizace pro zvýšení kvality** |
| --- | --- | --- |
| **Přehled řízení projektů a účetnictví** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Nesprávná výše smlouvy na stránce **Na účet** projektu s pevnou cenou s více zdroji financování. |
| **Přehled řízení projektů a účetnictví** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Zástupný symbol **Invoiceproposal.PSAnfRefProjId** nezobrazuje ID projektu pro pracovní postup **Zkontrolovat návrhy faktur projektu**. |
| **Přehled řízení projektů a účetnictví** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Při zaúčtování návrhů faktury projektu se používá nesprávné datum hotovostní slevy. |
| **Přehled řízení projektů a účetnictví** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Odebrání a čtení přiřazení prostředků v Project Operations zdvojnásobí položky prognózy projektu v aplikaci Finance. |
| **Přehled řízení projektů a účetnictví** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | V Project Operations nemůžete vytvořit odhady projektu v Dataverse, aniž byste na projektu měli řádek smlouvy. |
| **Přehled řízení projektů a účetnictví** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Když se náklady zaúčtují do zůstatku, finanční dimenze transakce výdajů na projekt se nesynchronizuje s příslušným dokladem a rozúčtováním sestavy výdajů. |
| **Přehled řízení projektů a účetnictví** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Filtr **Stav faktury** v zaúčtovaných transakcích projektu u projektů s pevnou cenou nefunguje. |
| **Přehled řízení projektů a účetnictví** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Odstranění zpětného odhadu nefunguje v části **Pravidelné**. |
| **Přehled řízení projektů a účetnictví** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Je možné odstranit řádky návrhu faktury v Project Operations při integraci s Dataverse. |
| **Přehled řízení projektů a účetnictví** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Zabránit povolení funkce více řádků smlouvy bez integrace Dataverse. |
| **Přehled řízení projektů a účetnictví** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Když se fakturace na účet rovná zisku a ztrátě, je fakturovaný výnos uveden jako nula na stránce Odhady. |
| **Přehled řízení projektů a účetnictví** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Opravy faktur nefungují v integrovaných prostředích. |
| **Přehled řízení projektů a účetnictví** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Při zaúčtování WIP - prodejní hodnoty ve fakturaci mezipodnikového projektu je vybrán nesprávný účet. |
| **Přehled řízení projektů a účetnictví** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | V Project Operations závislosti na úlohách odhadu v Dataverse nelze aktualizovat. |
| **Přehled řízení projektů a účetnictví** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Opakované mazání integračních deníků Project Operations ve Finance vede ke ztrátě dat. |
| **Přehled řízení projektů a účetnictví** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Při zaúčtování návrhu faktury projektu dojde k následující chybě: „Transakce nevyváží měnu vykazování, když je zpětně odečtena zálohová faktura“. |
| **Přehled řízení projektů a účetnictví** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Chybné ID projektu je zahrnuto v odpočtech po aktualizaci výchozí smlouvy o projektu v Project Operations. |
| **Přehled řízení projektů a účetnictví** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Pokud je povoleno Project Operations, nelze uznání odhadů a výnosů dokončit. |
| **Přehled řízení projektů a účetnictví** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | V Project Operations odebrání projektu ze smlouvy neresetuje výchozí projekt smlouvy. |
| **Přehled řízení projektů a účetnictví** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | V Project Operations se na mezipodnikové faktuře zobrazují nesprávné výdajové řádky na seznamu **Přidat řádek**. |
| **Cestování a výdaje** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Řádky výdajů nelze zaúčtovat, protože na řádku smlouvy chybí nastavení hodin. |
| **Cestování a výdaje** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Pokud je ověření projektu/kategorie povinné, kategorie výdajů přidružené k projektu se v sestavě výdajů nezobrazí. |
| **Cestování a výdaje** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Zůstatek zálohy v hotovosti se neaktualizuje, když je sestava výdajů zaúčtována po řádku. |
| **Cestování a výdaje** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Úloha **Aktualizovat platební údaje** selže po zrušení vypořádání, kde byla faktura vypořádána dvěma nebo více platebními transakcemi. |
| **Cestování a výdaje** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Je problém s výpočtem redukce jídla za poslední den pro kategorii výdajů na diety. |
| **Cestování a výdaje** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Sestava **Typ výdajů na zaměstnance** nezobrazuje rozepsané výdaje, pokud bylo první připojení uživatele v jazyce es-MX. |
| **Cestování a výdaje** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Platba dodavatele za fakturu sestavy výdajů používá nesprávný souhrnný účet pro zaúčtování vypořádání. |
| **Cestování a výdaje** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Když je výdajová sestava zaúčtována se zapnutými volbami **Povolit seskupování transakcí na základě offsetového platebního účtu** a **Oprava účetního data při zaúčtování**, účetní data nejsou seskupena v tabulce **Rozdělení účetnictví**, která ovlivňuje záznamy DPH. |
| **Cestování a výdaje** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Mapování podkategorií výdajů je odstraněno, když je políčko Použití na náklady zrušeno a znovu zaškrtnuto. |
| **Cestování a výdaje** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Sestavu mezipodnikových výdajů nelze vytvořit, pokud je ID projektu přidáno na úrovni záhlaví. |
| **Cestování a výdaje** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Je problém s platbami výdajů, když je částka výdajů vyšší než částka v hotovosti. |
| **Cestování a výdaje** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Pole **ID projektu** v sestavě mezipodnikových výdajů je prázdné, pokud je role uživatele přiřazena konkrétní organizaci. |
| **Cestování a výdaje** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kategorie výdajů je uzamčena při přidávání nového řádku výdajů. |
| **Cestování a výdaje** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Položkování řádků sestavy výdajů, které jsou již rozděleny, vede k neúplnému zaúčtování dokladu závazků \ hlavního registru. Kvůli duplikaci **TRVEXPTRANS.SOURCEDOCUMENTLINE** je průzkumník zdrojů účtování také nefunkční. |
| **Cestování a výdaje** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Přidání indexu do tabulky **TRVREQUISITIONLINE**, pro kterou má zákazník duplikáty, má za následek chybu během upgradu. |
| **Cestování a výdaje** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | V Project Operations čas s mezipodnikovými úkoly v Dataverse nelze vytvořit ani schválit. |

## <a name="regulatory-updates"></a>Povinné aktualizace

Informace o regulačních aktualizacích pro finanční a provozní aplikace naleznete v části [Regulační aktualizace](/dynamics365/finance/localizations/regulatory-updates). Můžete se také přihlásit do LCS a zobrazit plánované povinné aktualizace pomocí nástroje pro vyhledávání problémů. Hledání problému vám umožňuje vyhledávat podle země, typu funkce a vydání.


[!INCLUDE[footer-include](../includes/footer-banner.md)]