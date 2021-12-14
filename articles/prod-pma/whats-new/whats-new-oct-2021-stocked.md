---
title: Co je nového nebo co se změnilo v Project Operations pro scénáře založené na skladovém materiálu / výrobě, říjen 2021
description: Toto téma poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations z října 2021 pro scénáře založené na skladovém materiálu / výrobě.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 449cab5880c29cf110c9c5a266cbb4b102b5fc83
ms.sourcegitcommit: 2e4483d5b88213a9f33109f7adb989108521327d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2021
ms.locfileid: "7818465"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Co je nového nebo co se změnilo v Project Operations pro scénáře založené na skladovém materiálu / výrobě, říjen 2021

_**Platí pro:** Project Operations pro scénáře založené na skladovém materiálu / výrobě_

Toto téma se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.22
 
## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
|--------------|------------------|----------------|
| Přehled řízení projektů a účetnictví | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Částky nedokončené výroby (NV) a časově rozlišených výnosů nejsou správně stornovány, když je zaúčtována mezipodniková faktura odběratele. |
| Přehled řízení projektů a účetnictví | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Funkce **Zabránit uzavření projektu, pokud existují otevřené transakce** nefunguje. |
| Přehled řízení projektů a účetnictví | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Účtovací klasifikace na volné faktuře automaticky nevyplňuje dimenze z projektů, když je tato funkce povolena. |
| Přehled řízení projektů a účetnictví | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | U jiných než mezipodnikových scénářů nejsou částky nedokončené výroby (NV) a časově rozlišených výnosů správně stornovány, když je zaúčtována projektová faktura. |
| Přehled řízení projektů a účetnictví | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Debetní a kreditní hodnoty se prohodí, když se s deníkem výdajů projektu používá doplněk aplikace Microsoft Excel a pole **Typ offsetového účtu** je nastaveno na **Projekt**. |
| Přehled řízení projektů a účetnictví | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Částka, která je zaúčtována v projektových transakcích, je nadhodnocena na projektové nákupní objednávce, která zahrnuje skladové položky a která má částky neodčitatelné daně, když je označena možnost **UseTax**. |
| Přehled řízení projektů a účetnictví | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Systém rozdělí částku mezi výkazy zisků a ztrát projektu a výkazy NV projektu. |
| Přehled řízení projektů a účetnictví | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Po úpravě požadavku na částečně vrácenou položku jsou zásoby na skladě nesprávné. |
| Přehled řízení projektů a účetnictví | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Názvy zdrojů jsou v Project Operations duplikovány, když jsou upravovány v aplikaci Microsoft Project. |
| Přehled řízení projektů a účetnictví | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Sestavy mezipodnikových výdajů, které mají náklady nevyřízených faktur dodavatele u mezipodnikových závazků, se nejprve zaúčtují jako typ **Projekt – náklady NV**. Během zpracování jsou však náklady související s odhadem zaúčtovány jako typ **Projektové náklady** namísto očekávaného typu **Mezipodnikové náklady**. |
| Přehled řízení projektů a účetnictví | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Výsledky zádržného dodavatele se v transakcích projektových výdajů nezobrazují. |
| Přehled řízení projektů a účetnictví | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Časový výkaz musí zaokrouhlit částku transakce v měně transakce na zadaný počet desetinných míst ve všech účetních distribucích a položkách přidělení finančního deníku. |
| Přehled řízení projektů a účetnictví | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Množství požadavků na položky projektu se automaticky aktualizují, když jsou potvrzeny plánované objednávky. |
| Přehled řízení projektů a účetnictví | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Číslo dokladu, zůstatek dodavatele typu transakce a číslo účtu nelze na zálohové faktuře nákupní objednávky stornovat. |
| Přehled řízení projektů a účetnictví | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Mezipodniková faktura dodavatele je poškozená, když je zapnutá integrace faktur dodavatele. |
| Přehled řízení projektů a účetnictví | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Když vytvoříte deník projektových výdajů, částka nákladů se zobrazí v poli **Dal**. |
| Přehled řízení projektů a účetnictví | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Platební podmínky na fakturách projektu nefungují podle očekávání. |
| Přehled řízení projektů a účetnictví | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Doklady časového rozvrhu lze znovu použít, když je číselná posloupnost nastavena jako souvislá. |
| Přehled řízení projektů a účetnictví | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIE: Logika **Ruční částka uchování** neodpovídá logice **Automatická částka uchování** v návrhu faktury projektové smlouvy. |
| Přehled řízení projektů a účetnictví | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Po uvolnění zádržného dodavatele má zaúčtování dokladu další nesprávné řádky. |
| Přehled řízení projektů a účetnictví | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Když se změní pole **Datum faktury** na stránce **Vytvořit návrh faktury**, může dojít k následující chybě: „Odkaz na objekt není nastaven na instanci objektu.“ |
| Přehled řízení projektů a účetnictví | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Při pokusu o schválení časového rozvrhu z pracovního postupu **TSLine** dojde k chybě a pro sobotu a neděli existuje zásada časového rozvrhu. |
| Přehled řízení projektů a účetnictví | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Typ projektové položky počátečního zůstatku je vyloučen ze **Souhrnů transakcí návrhu faktury**, když je vypočítán celkový součet návrhu faktury. |
| Přehled řízení projektů a účetnictví | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Pokud jsou náklady spotřeby na výrobním příkazu projektu 0 (nula), při pokusu o odhad dojde k následující chybě: „Pokus o dělení nulou.“ |
| Přehled řízení projektů a účetnictví | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Mobilní aplikace časového rozvrhu projektu pro Android přestane reagovat. Problém souvisí s výjimkou **TimeEntryDataManager ArgumentNullException**. |
| Přehled řízení projektů a účetnictví | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Když je zaúčtován deník integrace Project Operations, operace selže z důvodu chybějících dimenzí pro účet. Účet, kterému chybí dimenze, však není účtem, do kterého provádíte zaúčtování. |
| Přehled řízení projektů a účetnictví | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Filtr **Do data** ve vyhledávání není vymazán, když je odstraněn z dialogu **Vybrat** na stránce **Zaúčtovat náklady**. |
| Přehled řízení projektů a účetnictví | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Resetovat všechna přidělení** selže a zobrazí chybu pro časové výkazy, které jsou vytvořeny pro projekt typu **Pouze čas**. |
| Přehled řízení projektů a účetnictví | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Kartu **Projekt** nelze na nevyřízené faktuře dodavatele upravit, když je k položce přiřazena kategorie zásobování. |
| Přehled řízení projektů a účetnictví | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Pokud nejste přihlášeni do Project Operations Dataverse, chybí navigační podokno. |
| Přehled řízení projektů a účetnictví | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | U transakcí mezipodnikových projektových úprav dochází v cílové společnosti k problémům. |
| Přehled řízení projektů a účetnictví | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Potvrzené náklady na projekt počítají nesprávné množství a nákladovou cenu, pokud nákupní objednávku vyřizoval proces **Zpracování nákupní objednávky na konci roku** v hlavní knize. |
| Přehled řízení projektů a účetnictví | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Když je výrobní příkaz projektu obsahující objednávky kvality vykázán jako dokončený, dojde k následující chybě: „Žádná virtuální transakce označená transakcí zásob.“ |
| Přehled řízení projektů a účetnictví | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Když je zaúčtována faktura závazků související s projektem, dojde k následující chybě: „Výčtový text Projekt - náklady - položka neexistuje.“ |
| Přehled řízení projektů a účetnictví | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Nepřímé náklady se zdvojnásobí, když ručně nashromáždíte výnosy. |
| Přehled řízení projektů a účetnictví | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Zaúčtování časově rozlišených výnosů a NV nevytvoří transakce. |
| Přehled řízení projektů a účetnictví | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktivace nevyřízené ceny pro standardní nákladovou položku selže, pokud existuje přijatá projektová nákupní objednávka. |
| Přehled řízení projektů a účetnictví | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Obrácená hodnota NV z účtování faktury je odlišná od původní hodnoty NV zaúčtované z časového záznamu. |
| Přehled řízení projektů a účetnictví | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Když transakce na dokladu nejsou správně vyváženy, dojde k problému při zaúčtování fakturovaného výnosu pro projekt v případech použitých záloh. |
| Přehled řízení projektů a účetnictví | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Vytvoření odhadu po zaúčtování návrhu faktury blokuje import opravných řádků v Project Operations. |
| Přehled řízení projektů a účetnictví | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Úprava plně fakturovaného milníku by neměla být možná. |
| Přehled řízení projektů a účetnictví | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Při použití automatických poplatků nelze zaúčtovat mezipodnikovou fakturu zákazníka pro časový rozvrh a zobrazí se chybová zpráva. |
| Přehled řízení projektů a účetnictví | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Adresa v dílčím projektu není správně aktualizována. |
| Přehled řízení projektů a účetnictví | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Nákladová cena u požadavků na položky se aktualizuje s nákupní cenou pro konsolidované nákupní objednávky. |
| Přehled řízení projektů a účetnictví | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Zaúčtovaná cena není správná po aktualizaci nákupní ceny, když je zapnut parametr **Aktivovat správu změn**. |
| Cestování a výdaje | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Když hledáte kategorii v mobilní aplikaci Výdaje, jsou viditelné všechny výdaje uživatele. |
| Cestování a výdaje | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Částky transakcí dodavatele a transakcí DPH, které jsou zaúčtovány z výdajů, které byly vytvořeny z transakce platební kartou, jsou nesprávné. |
| Cestování a výdaje | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Když obnovíte stránku sestavy výdajů, zobrazí se nepodstatné varování. |
| Cestování a výdaje | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Když odstraníte prozatímního schvalovatele a poté znovu odešlete sestavu prostřednictvím pracovního postupu, použije se nesprávný prozatímní schvalovatel. |
| Cestování a výdaje | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Dojde k chybě zaúčtování, která souvisí s nastavením ujetých kilometrů. |
| Cestování a výdaje | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Přidělení neaktualizuje právnickou osobu, když je nepřipojená transakce znovu přidána do sestavy výdajů o vnitropodnikových nákladech. |

### <a name="regulatory-updates"></a>Povinné aktualizace

Informace o povinných aktualizacích pro aplikace Finance and Operations viz [Povinné aktualizace](/dynamics365/finance/localizations/regulatory-updates). Můžete se také přihlásit do služeb Microsoft Dynamics Lifecycle Services (LCS) a použít nástroj pro vyhledávání problémů k zobrazení plánovaných regulačních aktualizací. Hledání problémů vám umožňuje vyhledávat podle země nebo oblasti, typu funkce a vydání.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
