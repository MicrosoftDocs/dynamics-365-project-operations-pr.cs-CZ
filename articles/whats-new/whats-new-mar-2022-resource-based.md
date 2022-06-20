---
title: Co je nového, březen 2022 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations z března 2022 pro scénáře založené na zdrojích / neskladových položkách.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910898"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového, březen 2022 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

*Platí pro: Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě*

Tento článek se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.30.0.99
- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.25

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

Denní diety jsou nyní podporovány v novém a přepracovaném moderním nákladovém pracovním prostoru. Společnosti, které používají denní diety, mohou tuto funkci povolit, aby uživatelům poskytla snadný způsob, jak je podávat a dostávat proplacené výdaje za diety. Další informace popisuje článek [Výdaje na denní diety](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

Následující seznam ukazuje mapy duálního zápisu, které byly upraveny nebo přidány ve verzi Project Operations z března 2022.

| **Mapování entity** | **Aktualizovaná verze** | **Komentáře** |
| --- | --- | --- |
| Entita exportu řádku faktury dodavatele projektu integrace Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.3 | Mapování byla aktualizována tak, aby byla v souladu s entitou řádku faktury dodavatele v Dataverse. <br>Neaktivujte verzi mapování 1.0.0.4. Bude připraven k použití v kombinaci s prostředím Finance verze 10.0.26 v příští měsíční aktualizaci. |

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a řešení Finance. Některé funkce a možnosti nemusí fungovat správně, pokud není aktivována nejnovější verze mapy. Aktivní verzi mapy můžete zobrazit ve sloupci **Verze** na stránce **Duální zápis**. Novou verzi mapy můžete aktivovat výběrem **Verze mapy tabulky** výběrem nejnovější verze a poté uložením vybrané verze. Pokud jste upravili integrovanou mapu tabulky, použijte změny znovu. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud při spuštění mapy narazíte na problém, postupujte podle pokynů v části [Problém s chybějícími sloupci tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) průvodce řešením problémů s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Čas a výdaje | 2388011 | Při hromadném schvalování zobrazit předkladatelům zadání času komentáře k zamítnutí. |
| Plánování a sledování projektu | 2495294 | Podrobnosti projektu nesmí být upravitelné na stránce **Podrobnosti úkolu**. |
| Fakturace a ceny | 2499605 | Milníky smlouvy, které jsou vytvořeny z milníků nabídek, jsou nesprávně označeny jako pouze pro čtení. |
| Plánování a sledování projektu | 2506050 | Pokud nedojde k žádné změně k uložení, sada operací zůstane nevyřízená po dobu jedné hodiny. Sada je pak nesprávně označena jako **Nezdařilo se**, přičemž by měla být dokončena okamžitě. |
| Fakturace a ceny | 2507401 | Výchozí smluvní jednotky jsou v projektech nesprávně zadány z důvodu nesprávného ukládání do mezipaměti. |
| Fakturace a ceny | 2541660 | **Ověření vytvoření prodejní objednávky** v duálním zápisu by mělo být pouze pro zakázky založené na projektu. |
| Fakturace a ceny | 2552745 | Daň se nerozděluje mezi zákazníky, kteří si nastavili pravidla rozdělené fakturace. |
| Fakturace a ceny | 2558859 | Vylepšené chybové zprávy při nastavování dimenzí cen. |
| Fakturace a ceny | 2558933 | **Import z odhadů projektu** selže, když **msdyn\_projekt** je přidáno jako cenová dimenze. |
| Fakturace a ceny | 2559101 | Smazání parametru projektu není blokováno a způsobuje problémy. |
| Správa příležitostí | 2570390 | Zásuvný modul pro duální zápis vynucuje typ účtu u nabídek, objednávek a příležitostí **Zákazník**, i když tento typ účtu není správný. |
| Fakturace a ceny | 2586097 | Skutečné hodnoty rozdělených fakturovaných nákladů nejsou stornovány, když je projekt odstraněn z řádku projektové smlouvy. |
| Fakturace a ceny | 2589619 | Daň ze zapsaného materiálu se přenáší do nevyfakturovaných skutečných prodejů a faktury. |
| Správa příležitostí | 2594015 | Cenovou nabídku nelze uzavřít jako vyhranou pro zákazníky, kteří mají platební podmínky **Net60**. |
| Plánování a sledování projektu | 2595841 | V aplikaci Project for the Web uživatelé obdrží chybovou zprávu o chybějící **msdyn\_actualstart**, když vytvoří nový požadavek na zdroj. |
| Čas a výdaje | 2602511 | Pole **Odmítnuto uživatelem** pro zadání času ukazuje **Systém** místo pojmenovaného uživatele jako odmítajícího. |
| Čas a výdaje | 2602528 | Schvalovatel projektu může schvalovat čas na projektech, kde není uveden jako schvalovatel. |
| Fakturace a ceny | 2608550 | Opravnou fakturu lze potvrdit i v případě, že nedošlo k žádným změnám oproti originálu. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Řízení projektů a účetnictví v Dynamics 365 Finance

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Přehled řízení projektů a účetnictví | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Mezi Finance a Project Operations je nesoulad v povolené délce pole **ID kategorie**. |
| Přehled řízení projektů a účetnictví | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Projekty s pevnou cenou nelze eliminovat, když pole **Fakturace na účet** nastaveno na **Zisk a ztráta** a je použit princip **Dokončené procento**. |
| Přehled řízení projektů a účetnictví | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Nesprávná výchozí skupina daně z prodeje je zadána z nastavení projektu na řádcích výdajů v deníku integrace Project Operations. |
| Přehled řízení projektů a účetnictví | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | V integrovaném nasazení s Project Operations nelze upravit rozměry záhlaví návrhu faktury projektu. |
| Přehled řízení projektů a účetnictví | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Mezipodnikové faktury dodavatelů nesmí být integrovány s Dataverse. |
| Přehled řízení projektů a účetnictví | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | V měně zůstatků zákazníků a měně vykazování je nesoulad. |
| Přehled řízení projektů a účetnictví | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Fakturu za projekt můžete zaúčtovat i v případě, že zákazník čeká na všechny faktury. |
| Přehled řízení projektů a účetnictví | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Tlačítko **Smazat všechny řádky** chybí u návrhů projektových faktur, které mají zobrazení **Hlavička** a **Řádky**. |
| Přehled řízení projektů a účetnictví | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Když zaúčtujete fakturu dodavatele, dojde k následující chybě: "Účetní datum faktury musí být ve stejném účetním roce jako související nákupní objednávka." Spusťte proces na konci roku nákupní objednávky nebo změňte datum na aktuální účetní rok." |
| Cestování a výdaje | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Závazné náklady na projekt se neuvolní poté, co se uvolní závazné náklady cestovní žádanky. |
| Cestování a výdaje | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Při odeslání sestavy výdajů dojde k následující chybě: "Trasování zásobníku: Společnost neexistuje." |
| Cestování a výdaje | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Výchozí **ID projektu** není uvedeno ve výkazech výdajů, když je vybrán parametr **Vyžadovat aktivitu pro deník** v projektu. |
| Cestování a výdaje | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Tlačítko **Zaúčtovat výdaje** nefunguje správně v Project Operations pro scénáře se zdroji bez skladových materiálů. |
| Cestování a výdaje | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Vyskytl se problém se **Sazbou za míli** pro výkaz ujetých kilometrů, který zahrnuje cestující. |
| Cestování a výdaje | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Sazby za ujeté kilometry pro zaměstnance nejsou správně sečteny, když se používají dva různé typy vozidel v kategorii výdajů **Úrovně sazeb za ujeté kilometry**. |
| Cestování a výdaje | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Vyhledávání pro pole **Projekt** na řádku požadavku na cestu nevrací správný seznam projektů. |
| Cestování a výdaje | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Stav kilometrů v revizi** zobrazuje varování ve výkazech výdajů. |
| Cestování a výdaje | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Služba optického rozpoznávání znaků (OCR) účtenky nefunguje kvůli problému s adresou URL výdajové služby OCR. |
| Cestování a výdaje | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Je-li povolena funkce **Schopnost rychle rozepsat opakující se výdaje**, částky na řádcích položek ve výkazech výdajů se mění částky pokaždé, když se otevře stránka **Rozepsat**. |
| Cestování a výdaje | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Výkaz výdajů nelze odstranit, pokud má prozatímní seznam více než jednoho schvalovatele. |

## <a name="removed-and-deprecated-features"></a>Odstraněné a zastaralé funkce

Článek [Odebrané nebo zastaralé funkce v Project Operations](removed-depreciated-features-project.md) popisuje funkce, které byly odstraněny nebo které byly zastaralé pro Dynamics 365 Project Operations.

- Odebraná funkce již v produktu není k dispozici.
- Zastaralá funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Oznámení o zastarání se objeví v článku [Odebrané nebo zastaralé funkce v Project Operations](removed-depreciated-features-project.md) 12 měsíců před odebráním funkce z produktu.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je nutné provést v kompilátoru.
