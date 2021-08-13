---
title: Co je nového nebo se změnilo v Project Operations, květen 2021, pro scénáře založené na skladovém materiálu / výrobě
description: Toto téma poskytuje informace o aktualizacích kvality dostupných ve verzi Project Operations z května 2021 pro scénáře založené na skladovém materiálu / výrobě.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: cfb418606f4186c5371c36946f75c9d946047a61
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334517"
---
# <a name="whats-new-or-changed-in-project-operations-may-2021-for-stockedproduction-based-scenarios"></a>Co je nového nebo se změnilo v Project Operations, květen 2021, pro scénáře založené na skladovém materiálu / výrobě

**Platí pro:** Project Operations pro scénáře založené na skladovém materiálu / výrobě

Toto téma se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

- Řízení projektů a účetnictví v prostředí Dynamics 365 Finance verze 10.0.19
 
### <a name="quality-updates"></a>Aktualizace pro zvýšení kvality
                                                                                                                                                                                  
| Oblast funkcí                      | Referenční číslo| Aktualizace pro zvýšení kvality                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Přehled řízení projektů a účetnictví | [529751](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529751) | Import se nezdaří, když je pro řádky deníku položky projektu vypnuto ověření entity.                                                                                                                                                   |
| Přehled řízení projektů a účetnictví | [550565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550565) | V přehledu účtů WIP je problém s výkonem související s vyhledáváním **GeneralJournalEntry**.                                                                                                                                  |
| Přehled řízení projektů a účetnictví | [539044](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539044) | Na projektu WIP chybí finanční dimenze.                                                                                                                                                                                                    |
| Přehled řízení projektů a účetnictví | [540903](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540903) | Zaúčtování návrhu faktury selhalo, protože bylo špatné **ProjBudgetAllocationLineIdSales** přiřazeno k **ProjBudgetReductionHistory**.                                                                                                                           |
| Přehled řízení projektů a účetnictví | [547090](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547090) | Po importu souboru XML se v hlavním deníku zobrazí nesprávná čísla poukázek.                                                                                                                                                              |
| Přehled řízení projektů a účetnictví | [552160](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552160) | V šabloně strukturovaného rozpisu práce dochází k chybě.                                                                                                                                                                                          |
| Přehled řízení projektů a účetnictví | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Poznámky formuláře** a **Nastavení formuláře** není vidět v nastavení řízení projektu v právnických osobách Finance, když jsou integrovány s Project Operations.                                                                                                             |
| Přehled řízení projektů a účetnictví | [553313](https://fix.lcs.dynamics.com/Issue/Details/?bugId=553313) | Zrušení mezipodnikové prodejní objednávky selže s následující chybou: „Nelze upravit záznam v řádcích nákupní objednávky (PurchLine). Došlo ke konfliktu aktualizací kvůli tomu, že jiný uživatel odstranil záznam nebo změnil jedno nebo více polí v záznamu. " |
| Přehled řízení projektů a účetnictví | [553775](https://fix.lcs.dynamics.com/Issue/Details/?bugId=553775) | Úprava transakcí projektu vytváří nesprávnou finanční dimenzi nákladů projektu.                                                                                                                                                          |
| Přehled řízení projektů a účetnictví | [556751](https://fix.lcs.dynamics.com/Issue/Details/?bugId=556751) | Faktura dodavatele má další výzvu při zpracování nákupní objednávky spojené s projektem.                                                                                                                                                 |
| Přehled řízení projektů a účetnictví | [557925](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557925) | Řádky časového rozvrhu nelze schválit a dojde k následující chybě: „Podmínky aktivace pracovního postupu nejsou platné. Nahlašte tento problém správci systému.“                                                                          |
| Přehled řízení projektů a účetnictví | [559266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559266) | Pokud se zobrazí chyba „Nelze změnit smlouvu projektu, protože existuje transakce pro přidružený projekt XXXXXX“, můžete smlouvu stále změnit na úrovni projektu.                                                                           |
| Přehled řízení projektů a účetnictví | [560432](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560432) | Pokud se zobrazí chyba „Množství nelze fakturovat, protože inventární transakce se stavem Odečteno jsou nedostatečné“, nelze po spuštění přepočtu zásob zaúčtovat fakturu nákupní objednávky.                             |
| Přehled řízení projektů a účetnictví | [562013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=562013) | Když je povolen pracovní postup požadavku na zdroj, při pokusu o otevření stránek s řízením dostupnosti prostředků projektu dochází k problémům s výkonem.                                                                                                               |
| Přehled řízení projektů a účetnictví | [488320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488320) | Stav faktury se změní na **Bez poplatku** po přidání pravidla fakturace k určení jiného projektu do smlouvy o projektu.                                                                                                                                |
| Přehled řízení projektů a účetnictví | [515219](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515219) | Při odebírání zálohové faktury z nákupní objednávky projektu a je povolen parametr **Zaúčtujte náklady na platbu předem oproti projektu**.                                                                                                        |
| Přehled řízení projektů a účetnictví | [526439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526439) | Když zaúčtujete fakturu za objednávku projektu, dojde k chybě, protože chybí automatické označení položky.                                                                                                                            |
| Přehled řízení projektů a účetnictví | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Výchozí popis pro DPH je prázdný, když se typ účtování rovná DPH pro poukázky na faktury projektu.                                                                                                                                           |
| Přehled řízení projektů a účetnictví | [530352](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530352) | Nákupní objednávka projektu zobrazí chybu, pokud odstraníte související prodejní objednávku požadavku na zrušenou položku.                                                                                                                                 |
| Přehled řízení projektů a účetnictví | [530651](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530651) | Když označíte a zrušíte označení nákupních objednávek požadavku na položku projektu, reference se ztratí.                                                                                                                                                               |
| Přehled řízení projektů a účetnictví | [533023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533023) | Při tisku výběrového seznamu pro požadavky na položky projektu je problém s výchozí hodnotou sníženého množství.                                                                                                                                                 |
| Přehled řízení projektů a účetnictví | [535493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535493) | Vypočtená prodejní cena není správná, pokud dojde k nadměrnému doručení.                                                                                                                                                                                 |
| Přehled řízení projektů a účetnictví | [541329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541329) | Chybné zatížení je zaúčtováno, když je uvolněno uchování bez množství faktury v návrhu faktury.                                                                                                                                                |
| Přehled řízení projektů a účetnictví | [541997](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541997) | Když vygenerujete období časového rozvrhu, první období se zobrazí jako týden 53.                                                                                                                                                                         |
| Přehled řízení projektů a účetnictví | [542043](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542043) | Výchozí typy projektů v integračních parametrech Dynamics 365 Project Service Automation by měly být Čas a Materiál a Fixní cena.                                                                                                         |
| Přehled řízení projektů a účetnictví | [543096](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543096) | Odstranění návrhu faktury s pravidly fakturace vygeneruje zaúčtování.                                                                                                                                                                              |
| Přehled řízení projektů a účetnictví | [543463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543463) | Konečný odhad procesu eliminace pomocí metody procento dokončení nelze eliminovat, protože systém nerozpozná tržby.                                                                                                                                      |
| Přehled řízení projektů a účetnictví | [543938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543938) | Když zaúčtujete odhad projektu, záznam odhadu příspěvku se nevytvoří.                                                                                                                                                                            |
| Přehled řízení projektů a účetnictví | [546885](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546885) | Během mezipodnikové fakturace nebyl nalezen hlavní účet na nevyřízené faktuře dodavatele.                                                                                                                                                               |
| Přehled řízení projektů a účetnictví | [547885](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547885) | Pokud smlouva obsahuje požadavky na položku, nemůžete přidat druhý zdroj financování.                                                                                                                                                         |
| Přehled řízení projektů a účetnictví | [550379](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550379) | Systém vytváří revize rozpočtu projektu pro všechny projekty, pokud použijete **Projekt** > **Rozpočet** > **Revize** > **Nový** > **Import**.                                                                                                                         |
| Přehled řízení projektů a účetnictví | [550577](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550577) |  Pokud upravíte transakci s různými měnami transakcí a účetnictví, položky zaúčtování a hlavní knihy jsou nesprávné.                                                                                                                                       |
| Přehled řízení projektů a účetnictví | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Potvrzené náklady jsou nadhodnoceny s neodpočitatelnými částkami daně.                                                                                                                                                                                   |
| Přehled řízení projektů a účetnictví | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Při vytváření účtovací faktury za transakci se nevyberou žádné dimenze.                                                                                                                                                                  |
| Přehled řízení projektů a účetnictví | [559416](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559416) | Metoda **PurchTotals.purchNewTotalAmount()** se volá, když vytvoříte nevyřízenou fakturu dodavatele, která není propojena s nákupní objednávkou, což má za následek problém s výkonem.                                                                                   |
| Přehled řízení projektů a účetnictví | [563694](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563694) | Sloupce **Spotřebovaný rozpočet** a **Zbývající rozpočet** zobrazují nesprávné částky na zůstatcích rozpočtu projektu.                                                                                                                                                |
| Přehled řízení projektů a účetnictví | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Zaúčtují se dvojí transakce při použití fakturace podle úkolů v Dataverse s Project Operations.                                                                                                                                         |
| Přehled řízení projektů a účetnictví | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Procento dokončení pro rozpoznávání výnosů je při použití Project Operations nesprávné.                                                                                                                                                  |
| Přehled řízení projektů a účetnictví | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Časové rozlišení příjmů se zdvojnásobí, pokud používáte v integrovaném scénáři Project Operations nevyřízenou fakturu dodavatele.                                                                                                                                          |
| Přehled řízení projektů a účetnictví | [569736](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569736) | Zveřejněním časového rozvrhu projektu se vytvoří duplicitní transakce.                                                                                                                                                                        |
| Přehled řízení projektů a účetnictví | [569819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569819) | Při zaúčtování deníku spotřeby zboží proti pracovní objednávce dojde k chybě.                                                                                                                                  |
| Přehled řízení projektů a účetnictví | [571197](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571197) | Projektovou výrobní zakázku nelze dokončit z důvodu následující chyby „Odkaz na objekt není nastaven na instanci objektu.“                                                                                                                           |
| Přehled řízení projektů a účetnictví | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Nelze zaúčtovat deník integrace, když je pravidlo profilu výnosů nastaveno na **Nastavení skupiny**.                                                                                                                                                           |
| Přehled řízení projektů a účetnictví | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Nákupní fakturu nelze zaúčtovat u nákupní objednávky projektu, která má řádky s více měrnými jednotkami.                                                                                                                                             |
| Přehled řízení projektů a účetnictví | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Výchozí finanční dimenzi projektu nelze aktualizovat pomocí datové entity **Projekty V2**.                                                                                                                                                          |
| Přehled řízení projektů a účetnictví | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Nelze vytvořit dobropis pro prodejní objednávku projektu, pokud je daň v jiné měně než měna společnosti.                                                                                                                     |
| Přehled řízení projektů a účetnictví | [574104](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574104) | Při vytváření návrhu faktury s více než 100 pravidly fakturace nastal problém.                                                                                                                                                                  |
| Přehled řízení projektů a účetnictví | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Dávkový proces vytváření odhadů projektu trvá příliš dlouho.                                                                                                                                                                      |
| Přehled řízení projektů a účetnictví | [577785](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577785) | Když spustíte funkci **Vyplnit zdroje projektu napříč všemi společnostmi**, dojde k následující chybě „Neplatný název objektu ResRollupCalendar.“                                                                                                                                   |
| Přehled řízení projektů a účetnictví | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Když odstraníte smlouvu, odstraní se také odstraní adresa spojená se zákazníkem.                                                                                                                                                                    |
| Cestování a výdaje                  | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Podmínka pracovního postupu schválení sestavy výdajů není správně vyhodnocena.                                                                                                                                                                           |
| Cestování a výdaje                  | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Zásady výkazu výdajů správně nevyhodnocují ID projektu.                                                                                                                                                                                   |
| Cestování a výdaje                  | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Akce **Rozdělit na osobní** pro mezipodnikové výdajové transakce nefunguje správně.                                                                                                                                                                |
| Cestování a výdaje                  | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Když jsou odstraněny cestovní požadavky, někdy dojde ke smazání zdůvodnění řádku hlášení o výdajích. K tomu dochází, když recid sestavy výdajů a cestovní požadavek jsou stejné.                                                            |
| Cestování a výdaje                  | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | V mobilní aplikaci Expense je problém, když je vyžadováno pole **ID projektu** zásadami výkazu výdajů.                                                                                                                                                |
| Cestování a výdaje                  | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Při pokusu o úpravu mezipodnikového výdaje přidruženého k projektu se zobrazí následující chybová zpráva „Odkaz na objekt není nastaven na instanci objektu.“                                                                           |
| Cestování a výdaje                  | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Po zaúčtování výkazu výdajů je v podřízené účetní knize banky uvedena nesprávná měna a částka.                                                                                                                                                                |
| Cestování a výdaje                  | [555462](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5355462) | Potvrzené náklady projektu nejsou uvolněny po uzavření žádosti o cestování s potvrzenými náklady.                                                                                                                                              |
| Cestování a výdaje                  | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Byla vylepšena funkce Smazat transakce kreditní karty.                                                                                                                                                                                           |
| Cestování a výdaje                  | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | DPH zahrnutá v sestavě výdajů se konzistentně nepočítá, když je v právnické osobě uvedena jiná měna vykazování.                                                                                                         |
| Cestování a výdaje                  | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Výkon je ovlivněn při přidávání nových cestovních výdajů v hotovosti.                                                                                                                                                                                         |
| Cestování a výdaje                  | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Pravidlo zásad výdajů se ve výkazu výdajů nespouští.                                                                                                                                                                                            |
| Cestování a výdaje                  | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Nahráním nové sdílené kategorie pomocí Data Management Framework odeberete všechny podkategorie pro všechny sdílené kategorie.                                                                                                                         |
| Cestování a výdaje                  | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Když vytvoříte řádek výdajů a poté vyberete kategorii, zobrazí se následující chybová zpráva: „Kombinace DOM skupiny DPH a STD skupiny DPH z položky není platná.“                                                                  |
| Cestování a výdaje                  | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | V mobilní aplikaci Expense jsou problémy se synchronizací. 

### <a name="regulatory-updates"></a>Povinné aktualizace
Informace o povinných aktualizacích pro aplikace Finance and Operations viz [Povinné aktualizace](/dynamics365/finance/localizations/regulatory-updates). Můžete se také přihlásit do služby Lifecycle Services (LCS) a zobrazit plánované aktualizace předpisů pomocí vyhledávacího nástroje Vydání. Hledání problému vám umožňuje vyhledávat podle země, typu funkce a vydání.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]