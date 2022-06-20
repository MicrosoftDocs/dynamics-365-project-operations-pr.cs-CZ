---
title: Co je nového nebo se změnilo v Project Operations, červenec 2021, pro scénáře založené na skladovém materiálu / výrobě
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations z července 2021 pro scénáře se skladovým materiálem a výrobními příkazy.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: df9a68c5a12e6aec140867eb1db3d88279c05795
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933622"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Co je nového nebo se změnilo v Project Operations, červenec 2021, pro scénáře založené na skladovém materiálu / výrobě

_**Platí pro:** Project Operations pro scénáře založené na skladovém materiálu / výrobě_

Tento článek se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.20
 
### <a name="quality-updates"></a>Aktualizace pro zvýšení kvality
                                                                                                                                                                                  
| Oblast funkcí                      | Referenční číslo| Aktualizace pro zvýšení kvality                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Přehled řízení projektů a účetnictví | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Záznamy o nákladových závazcích z požadavku na objednávku jsou vymazány, jakmile je objednávka uvolněna z vydání požadavku na objednávku.                                                                           |
| Přehled řízení projektů a účetnictví | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Ověření rozpočtu proběhne dvakrát u požadavku na nákup. Tato duplikace znamená, že požadavek nelze uzavřít a příslušná nákupní objednávka se nevytvoří.                                                                                                                        |
| Přehled řízení projektů a účetnictví | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Pravidlo fakturace **Procenta k vyúčtování** nebylo možné dokončit kvůli problému se zaokrouhlováním.                                                                              |
| Přehled řízení projektů a účetnictví | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Když upravíte transakci a procento má desetinná místa, náklady a prodejní cena nebudou správně upraveny.                                      |
| Přehled řízení projektů a účetnictví | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Průzkumník zdrojů účetnictví zobrazuje hodiny pro jeden řádek časového rozvrhu pro více řádků časového rozvrhu s různými aktivitami.                                      |
| Přehled řízení projektů a účetnictví | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Uložené zobrazení a personalizace podrobností řádků časového rozvrhu způsobí, že systém při pokusu o otevření časového rozvrhu vždy otevře podrobnosti prvního časového rozvrhu v seznamu.  |
| Přehled řízení projektů a účetnictví | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Kořenový uzel projektu zmizí a záznamy struktury rozložení práce se po importu odstraní.                                                                                             |
| Přehled řízení projektů a účetnictví | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Když jsou položky přijímány a vydávány částečně z požadavku na položku, systém aktualizuje nesprávný zůstatek spotřeby rozpočtu. |
| Přehled řízení projektů a účetnictví | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Nákupní objednávky zadržení projektu nezobrazují správně součty v podokně **Součty** nebo v mřížce **Nevyřízená faktura**.                                                                  |
| Přehled řízení projektů a účetnictví | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Při uzavírání zásob se úpravy nákladů položky projektu zaúčtují na účet zůstatku místo na účet zisků a ztrát.                                                            |
| Přehled řízení projektů a účetnictví | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Poukaz na transakci zaúčtovaný na projekt a poukaz na odhad používají jako účetní měnu USD, ale částka ukazuje, jaký by byl ekvivalent CAD.              |
| Přehled řízení projektů a účetnictví | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Vázané náklady s požadavkem na položku a nákupní objednávkou jsou v procesu fakturace nákupní objednávky chybné s příjmem produktu a fakturací dílu.       |
| Přehled řízení projektů a účetnictví | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Úprava projektu neaktualizuje správně částku prodeje nepřímými náklady.                                                                                    |
| Přehled řízení projektů a účetnictví | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | V tabulce **Časový rozvrh** chybí definovaný vztah se zobrazením **Pracovník / zdroj**.                                                                                   |
| Přehled řízení projektů a účetnictví | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Nelze vyplnit pole **Číslo aktivity**, když jej vyberete z rozevírací nabídky mezipodnikového časového rozvrhu.                                                                 |
| Přehled řízení projektů a účetnictví | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Nemůžete přidat přizpůsobené pole **Účel** nebo **Popis aktivity** na následující stránky: **Transakce zaúčtovaná v projektu**, **Vytvoření návrhu faktury** nebo **Návrh faktury**.  |
| Přehled řízení projektů a účetnictví | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Při vytváření požadavků na položku pomocí správy dat je k dispozici nesprávná kontrola data dodání (**ProjSalesItemRequirementEntity**).                                              |
| Přehled řízení projektů a účetnictví | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Když vyberete ID kontraktu projektu v Finance, integrované prostředí Project Operations otevře stránku a vytvoří nový záznam namísto otevření existující kontraktu projektu.                                                                                                                 |
| Řízení projektů a účetnictví | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Popisek "@SYS4083080" („Nelze najít jedinečný záznam pracovníka odpovídající zadaným hodnotám“) není přeložen do dánštiny.                                |
| Přehled řízení projektů a účetnictví | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Pole **Skupina DPH zboží** nelze upravit v návrhu faktury.                                                                               |
| Přehled řízení projektů a účetnictví | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Potvrzené náklady jsou nadhodnoceny s neodpočitatelnými částkami daně.                                                                                                    |
| Přehled řízení projektů a účetnictví | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Zaúčtování mezipodnikového časového rozvrhu s více projekty a různými finančními dimenzemi generuje neočekávané hodnoty v hlavní knize.                             |
| Přehled řízení projektů a účetnictví | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Řádky návrhu faktury jsou duplikovány z důvodu více instancí periodického procesu **Import z fázování** běžícího současně.                                      |
| Přehled řízení projektů a účetnictví | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | V zaúčtování návrhu faktury na dobropisu došlo k chybě, takže transakce na poukazu neodpovídají.    |
| Přehled řízení projektů a účetnictví | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Po uvolnění pozastavených nevyřízených faktur se náklady na závazky projektu stanou nesprávnými.                                                                             |
| Řízení projektů a účetnictví | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Nelze vytvořit dobropis pro prodejní objednávku projektu, pokud je daň v jiné měně než měna společnosti.                                      |
| Přehled řízení projektů a účetnictví | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Odstraněním smlouvy se také odstraní adresa spojená se zákazníkem.                                                                                     |
| Přehled řízení projektů a účetnictví | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Návrh faktury, který je výsledkem záporné časové opravy transakce, nelze zaúčtovat.                                                                    |
| Cestování a výdaje                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Daň se ve výkazech výdajů počítá odlišně.                                                                                                                  |
| Cestování a výdaje                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Vydání aktualizace **DB72_Expense.updateTrvExpTransProjTransId()** neumožňuje **trvExpTrans.ReferenceDataAreaId** vytvořit novou číselnou řadu.                    |
| Cestování a výdaje                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | U povinného pole se nezobrazuje podaná částka.                                                                                                             |
| Cestování a výdaje                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Vylepšení výkonu připojení výdajů k výkazu výdajů pomocí uživatelského rozhraní Vynaložené náklady.                                                            |
| Cestování a výdaje                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Můžete odstranit zaúčtované výkazy výdajů.                                                                                           |
| Cestování a výdaje                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Zpráva o výdajové politice se zobrazí několikrát.                                                                                                       |
| Cestování a výdaje                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Pole **Způsob platby** je v podokně **Nový výdaj**.                                                                                                      |
| Cestování a výdaje                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Nástroj **Resetovat stav dokumentu výdajů** by měl resetovat stav výkazu výdajů na **Koncept**, pokud nebyl nalezen pracovní postup. 

### <a name="regulatory-updates"></a>Povinné aktualizace
Informace o regulačních aktualizacích pro finanční a provozní aplikace naleznete v části [Regulační aktualizace](/dynamics365/finance/localizations/regulatory-updates). Můžete se také přihlásit do služby Lifecycle Services (LCS) a zobrazit plánované aktualizace předpisů pomocí vyhledávacího nástroje Vydání. Hledání problému vám umožňuje vyhledávat podle země, typu funkce a vydání.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
