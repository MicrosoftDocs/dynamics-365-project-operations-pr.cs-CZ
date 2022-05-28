---
title: Co je nového nebo co se změnilo v Project Operations pro scénáře založené na skladovém materiálu / výrobě, září 2021
description: Toto téma poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations ze září 2021 pro scénáře založené na skladovém materiálu / výrobě.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 24de8626199a3ed56bb6703b78d746ff7a43a089
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582012"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Co je nového nebo co se změnilo v Project Operations pro scénáře založené na skladovém materiálu / výrobě, září 2021

_**Platí pro:** Project Operations pro scénáře založené na skladovém materiálu / výrobě_

Toto téma se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.21
 
## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
|---|---|---|
| Přehled řízení projektů a účetnictví | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Když má role nákupního manažera udělen přístup k jedné právnické osobě, získá také přístup ke všem projektům ve všech právnických osobách. |
| Přehled řízení projektů a účetnictví | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Problém zaokrouhlení daně z přidané hodnoty (DPH) nastane, když je dobropis zúčtován proti původní projektové faktuře. |
| Přehled řízení projektů a účetnictví | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Pro ověření rozpočtu použijte alternativní rozpočet projektu. |
| Přehled řízení projektů a účetnictví | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Cenová skupina **Prodejní cena – hodina** se nepočítá ve strukturovaném rozpisu prací pro projektové nabídky. |
| Přehled řízení projektů a účetnictví | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Odstranění odhadu selže, když je povolena funkce **Povolit měnu projektové smlouvy pro výpočet odhadu**. |
| Přehled řízení projektů a účetnictví | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Faktorizace daně z obratu podle množství je přidána k částce prodejní ceny, když je ve skupině daně z obratu v deníku výdajů projektu použita daň z používání. |
| Přehled řízení projektů a účetnictví | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Podmíněná daň není vypočtena správně u poslední platby, když na faktury za nákupní objednávky jsou uplatněna zadržení a zálohy dodavatele. |
| Přehled řízení projektů a účetnictví | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Trasování úprav nefunguje u deníků počátečních zůstatků. |
| Přehled řízení projektů a účetnictví | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Přidělení revize projektového rozpočtu podle období** je rozděleno přes všechna rozpočtová období. Po odeslání přidělení se záznam nevymaže. |
| Přehled řízení projektů a účetnictví | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Zaúčtování nedokončené výroby (NV) do hlavní knihy mají nesprávnou částku. |
| Přehled řízení projektů a účetnictví | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Schválení deníku projektových hodin nefunguje. |
| Přehled řízení projektů a účetnictví | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Prodejní cena úpravy projektu se neaktualizuje o nepřímé náklady, když je limit financování neoznačený. |
| Přehled řízení projektů a účetnictví | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Požadavek na položku nelze vytvořit, když je fakturováno záhlaví tabulky Prodej a byla dokončena záložní nákupní objednávka pro existující řádky. |
| Přehled řízení projektů a účetnictví | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Částka uchování pro pravidlo fakturace, které má milník pro jiný projekt, není zaúčtována v odpovídajícím ID projektu, které bylo vybráno pro milník. Místo toho je zaúčtováno v prvním projektu. |
| Přehled řízení projektů a účetnictví | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Když vyberete na návrhu faktury **Sadu finančních dimenzí**, dojde k následující chybě: „Nelze přetypovat objekt typu 'Dynamics.AX.Application.FormIntControl' na typ 'Dynamics.AX .Application.FormStringControl'.“ |
| Přehled řízení projektů a účetnictví | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Sestava **Projektová faktura** přeskakuje řádky. |
| Přehled řízení projektů a účetnictví | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Při výpočtu řízení nákladů pro investiční projekt dojde k chybě. |
| Přehled řízení projektů a účetnictví | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Metoda **ProjTable::InitFromCustTable - canDeletePostalAddress** způsobí pokles výkonu. |
| Přehled řízení projektů a účetnictví | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Chybová zpráva by měla obsahovat více informací než jen „Neočekávaná chyba“. |
| Přehled řízení projektů a účetnictví | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Úloha dávky zaúčtování faktury projektu zpracuje a zaúčtuje návrh faktury, i když nebyly vygenerovány její řádky. |
| Přehled řízení projektů a účetnictví | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Problém se zaokrouhlováním nastane, když je klíč konfigurace licence veřejného sektoru vypnutý. Nesprávné náklady nebo prodejní cena jsou generovány v hodinách časového rozvrhu u smluv, které mají více zakládajících zdrojů. |
| Přehled řízení projektů a účetnictví | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Prodejní cena projektu na fakturované nákupní objednávce projektu je vypočtena nesprávně, když má model prodejní ceny hodnotu **Příspěvkový poměr**. |
| Přehled řízení projektů a účetnictví | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Při výpočtu efektivní pracovní sazby pro zaměstnance systém nebere v úvahu aktivní dny mezi nimi. |
| Přehled řízení projektů a účetnictví | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | V mezipodnikovém časovém rozvrhu dojde k chybě účtování z důvodu následující chyby ověření: „Žádný obchodní partner není nakonfigurován pro právnickou osobu.“ |
| Přehled řízení projektů a účetnictví | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Popis z nákupní objednávky, která má kategorii výdajů, se nenačte v seznamu zaúčtovaných transakcí projektu. |
| Přehled řízení projektů a účetnictví | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | U deníků položek, které jsou zaúčtovány do projektu, došlo k nesprávné konverzi. |
| Přehled řízení projektů a účetnictví | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Nákupní objednávku můžete potvrdit, i když byl překročen limit financování. |
| Přehled řízení projektů a účetnictví | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Oddíl **Oprava/zrušení faktury** na volné faktuře zmizí, když je vybráno ID projektu. |
| Přehled řízení projektů a účetnictví | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Při zaúčtování návrhu projektové faktury z projektové prodejní objednávky, která obsahuje skladovou položku, dochází k problémům s výkonem. |
| Přehled řízení projektů a účetnictví | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Faktury za projektový nákup nelze zaúčtovat, protože došlo k následující chybě: „Funkce AccDistProcessorProjectExtension.createForProjectRevenueLine byla nesprávně volána.“ |
| Přehled řízení projektů a účetnictví | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Aktualizace vytváření dávkových úloh odhadu projektu za účelem podpory provádění více dílčích úkolů. |
| Přehled řízení projektů a účetnictví | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Stav časového rozvrhu nelze aktualizovat na **Koncept** když pracovní postup uvízne ve stavu **Zrušeno**. |
| Přehled řízení projektů a účetnictví | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Pokud existuje více řádků, zadržené částky se v návrhu faktury dobropisu nevypočítají. |
| Přehled řízení projektů a účetnictví | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Když se pokusíte změnit částku na vygenerované faktuře z nákupní objednávky, dojde k následující chybě: „Transakce na dokladu se nevyrovnají podle XX/XX/XXXX. (účetní měna: 0,00 – měna vykazování: 0,01).“ |
| Přehled řízení projektů a účetnictví | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Když je návrh projektové faktury zaúčtován v dávkovém režimu, dochází k problému s výkonem z důvodu spojení s tabulkou **GeneralJournalAccountEntry**. |
| Přehled řízení projektů a účetnictví | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Při zaúčtování časového rozvrhu dochází k problémům s výkonem. |
| Přehled řízení projektů a účetnictví | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Hierarchie odhadů nákladů ve strukturovaném rozpisu prací není správně uspořádána po rozbalení všech úkolů nebo po ručním rozbalení jednoho úkolu. |
| Přehled řízení projektů a účetnictví | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Excelovou šablonu nabídky projektu nelze přidat do nabídky **Otevřít v Excelu**. |
| Přehled řízení projektů a účetnictví | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Číslo osvobození od daně pro právnickou osobu není součástí vytištěné projektové faktury. |
| Přehled řízení projektů a účetnictví | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Při úpravě projektu ve vztahu k řádkům kreditu se v chybě jednotky zásob neaktualizují žádné finanční údaje. |
| Přehled řízení projektů a účetnictví | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Po použití aktualizace KB 461935 nemůžete zveřejňovat odhady, pokud se přepnete na nepřetržité číselné řady. |
| Přehled řízení projektů a účetnictví | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** způsobí, že mobilní aplikace časového rozvrhu projektu pro Android přestane reagovat. |
| Přehled řízení projektů a účetnictví | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Obrácená hodnota NV z účtování faktury je odlišná od původní hodnoty NV zaúčtované z časového záznamu. |
| Přehled řízení projektů a účetnictví | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | V případech použitých záloh nejsou transakce na dokladu vyváženy, když je zaúčtován fakturovaný výnos pro projekt. |
| Přehled řízení projektů a účetnictví | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Pokud je povolena funkce **Vylepšení výkonu plánování zdrojů projektu**, desetinné hodnoty u dostupnosti zdrojů a kapacity jsou nesprávně zaokrouhleny. |
| Přehled řízení projektů a účetnictví | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Pokud je povolena funkce **Vytvářet odhady projektů pomocí více dávkových úloh**, vytváření odhadů v dávce, která má více dílčích úkolů, funguje pouze pro aktuální období. |
| Cestování a výdaje | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Zásada cestovních žádanek je ignorována a pracovní postup je schválen bez chyb. |
| Cestování a výdaje | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Aplikace mobilních výdajů neukládá v řádku výdajů následující informace:</p><ul><li>ID projektu</li><li>Zda je výdaj zúčtovatelný</li><li>Číslo aktivity</li></ul> |
| Cestování a výdaje | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Pole **Připojené účtenky** je nastaveno na **Ano**, i když k řádku výdajů není připojena žádná účtenka. |
| Cestování a výdaje | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Při pokusu o změnu kategorie výdajů na **Osobní** se zobrazí chybová zpráva. |
| Cestování a výdaje | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Po rozdělení transakce kreditní kartou na osobní výdaje nemůžete připojit účtenku ani upravit nadřazené výdaje. |
| Cestování a výdaje | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Zásady výdajů pro mezipodnikové transakce s ID projektu nefungují správně. |
| Cestování a výdaje | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | U sestav zaúčtovaných výdajů chybí datum zaúčtování. |
| Cestování a výdaje | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | V mobilní aplikaci výdajů dochází k problémům s platebními metodami. |
| Cestování a výdaje | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Cestovní žádanku vytvořenou pro jednoho pracovníka lze použít v sestavě výdajů jiného pracovníka před datem delegáta. |
| Cestování a výdaje | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Když vytvoříte výdaj, změny hodnot finanční dimenze se správně neaktualizují na úrovni rozúčtování v pracovním prostoru **Správa výdajů**. |
| Cestování a výdaje | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Stav schválení hlavní řádky výdajů se nesynchronizuje se stavem schválení pracovního postupu rozepsané řádky. |
| Cestování a výdaje | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Pokud zaúčtujete sestavu výdajů a je povolena vratka daně, dojde k chybě. |
| Cestování a výdaje | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Delegát nemůže odstranit doklady o výdajích za ukončeného zaměstnance. |
| Cestování a výdaje | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Odstranění řádku výdajů trvá déle, než se očekávalo, a ovlivňuje výkon. |
| Cestování a výdaje | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** způsobí osamocený záznam **TaxUncommitted**, protože se odstraní pouze **SourceDocumentLine**. |
| Cestování a výdaje | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** nebere ohled při vytvoření nové číselné řady na **trvExpTrans.ReferenceDataAreaId**. |

## <a name="regulatory-updates"></a>Povinné aktualizace

Informace o regulačních aktualizacích pro finanční a provozní aplikace naleznete v části [Regulační aktualizace](/dynamics365/finance/localizations/regulatory-updates). Můžete se také přihlásit do služeb Microsoft Dynamics Lifecycle Services (LCS) a použít nástroj pro vyhledávání problémů k zobrazení plánovaných regulačních aktualizací. Hledání problémů vám umožňuje vyhledávat podle země nebo oblasti, typu funkce a vydání.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
