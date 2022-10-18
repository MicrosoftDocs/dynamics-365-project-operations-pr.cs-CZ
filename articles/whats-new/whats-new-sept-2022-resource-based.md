---
title: Co je nového, září 2022 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Microsoft Dynamics 365 Project Operations ze září 2022 pro scénáře založené na zdrojích / neskladových položkách.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634797"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového, září 2022 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Tento článek se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.46.0.60
- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.29

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

| Oblast funkcí | Název funkce | Více informací |
| --- | --- | --- |
| Správa příležitostí | **Revize a aktivace nabídek**<br>Project Operations přináší plnou podporu prodejního procesu. Nabídky projektu lze aktivovat, aby představovaly stav, kdy je nabídka pouze pro čtení a prochází kontrolou. Aktivované nabídky lze revidovat a vytvářet nové nabídky, které mají zvýšené číslo revize. Aktivované nabídky projektu a revize nabídky lze uzavírat jako získané nebo ztracené. | [Aktivace a úprava nabídky projektu](/dynamics365/project-operations/sales/activation-and-revision) |
| Fakturace a ceny | **Výchozí cena bez ohledu na časové pásmo**<br>Project Operations zavedly koncept nezávislosti data časového pásma u všech skutečných událostí projektu. Nové pole, **Datum transakce**, je nyní k dispozici na řádcích deníku a skutečných hodnotách a bude sloužit k uložení data, kdy k transakci došlo, ale bez převodu tohoto data na koordinovaný univerzální čas. Toto datum bude použito pro následné procesy, jako je prodlení s cenou a vytvoření faktury. | <p>[Určení nákladových sazeb pro odhady a skutečné hodnoty projektu](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Určení prodejních cen pro odhady projektu a skutečné hodnoty](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Fakturace a ceny | **Přepisy ceny platné k datu v Project Operations**<br>Přepisy cen platné k datu poskytují způsob, jak přepsat nebo změnit konkrétní ceny v ceníku. | [Přepsání cen s datem platnosti](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subdodávka | **Odsouhlasení subdodávek a faktur dodavatele**<br>Tato funkce umožňuje zákazníkům vytvářet subdodávky na nákup času zdrojů, kategorií výdajů a materiálů, které se používají pro práci na projektu. Umožňuje také zákazníkům zaznamenávat ve finančních a provozních aplikacích faktury dodavatelů, které budou k dispozici projektovým manažerům v Dataverse pro ověření. | <p>[Řízení subdodávek](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Vytváření faktur dodavatele](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Čas a výdaje | **Globální schvalovatel**<br>Tato funkce umožňuje nezávislého dodavatele softwaru (ISV) a centralizované schvalování bez ohledu na stav projektu nebo člena týmu v projektu. | [Zabezpečení a schválení](/dynamics365/project-operations/approvals/approvals-security) |
| Řízení výdajů | **Schopnost účtovat výdajový závazek v měně dodavatele**<br>Tato funkce umožňuje účtovat výdajové sestavy v měně dodavatele pro způsob platby v hotovosti. | [Schopnost účtovat výdajový závazek v měně dodavatele](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Zadávání projektů | **Platby dodavatelů typu „Zaplatit po uhrazení platby“**<br>Tato funkce umožňuje použití funkce Platit po zaplacený (PWP) s neskladovými prostředími Project Operations. Umožňuje zablokovat/zadržet platby dodavatele na základě podmínek uchování, dokud platba nepřijde od zákazníka. | [Platby dodavatelů typu „Zaplatit po uhrazení platby“](/dynamics365/project-operations/procurement/pay-when-paid) |
| Zadávání projektů | **Požadavky na nákup projektu**<br>Tato funkce umožňuje uživatelům vytvářet nákupní objednávky související s projektem v právnických osobách, kde je zapnutá integrace Project Operations na Dynamics 365 Customer Engagement. Nákupní zakázky projektu lze použít k evidenci nákupu neskladovaného materiálu oproti projektu osobou oddělení nákupu. Nákupní objednávky projektu nebudou synchronizovány s Dataverse. Můžete však použít virtuální entitu k zobrazení řádků nákupní objednávky projektu v Dataverse pro informace projektového manažera. Náklady na fakturu dodavatele související s projektem jsou integrovány s entitou Skutečné hodnoty projektu v Dataverse. Náklady projektu se zaznamenávají do poddeníku pomocí deníku integrace Project Operations. | |
|Plánování a sledování projektu|**K provádění operací s entitami plánování použijte rozhraní API pro plánování projektu** </br> </br>Rozhraní API pro úpravu průběhových křivek přiřazení zdrojů umožňuje vývojářům programově specifikovat úsilí příjemce úkolu v libovolném podporovaném časovém období pro podrobnější časově rozložené plánování úsilí.|[K provádění operací s entitami plánování použijte rozhraní API pro plánování projektu](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

Následující tabulka ukazuje mapy duálního zápisu, které byly upraveny nebo přidány ve verzi Project Operations ze září 2022.

| Mapování entity | Aktualizovaná verze | Komentáře |
| -------------- | ------------------- | ------------|
| Skutečné hodnoty integrace Project Operations (msdyn_actuals) | 1.0.0.15 | Tato mapa podporuje zpracování skutečného stavu subdodávek pomocí Project Operations pro scénáře založené na zdrojích. |
| Entita exportu faktury dodavatele projektu integrace Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Tato mapa podporuje zpracování skutečného stavu subdodávek pomocí Project Operations pro scénáře založené na zdrojích. |
| Entita exportu řádku faktury dodavatele projektu integrace Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Tato mapa podporuje zpracování skutečného stavu subdodávek pomocí Project Operations pro scénáře založené na zdrojích. |

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a řešení Finance. Některé funkce a možnosti nemusí fungovat správně, pokud není aktivována nejnovější verze mapy. Aktivní verzi mapy můžete zobrazit ve sloupci **Verze** na stránce **Duální zápis**. Novou verzi mapy můžete aktivovat výběrem **Verze mapy tabulky** výběrem nejnovější verze a poté uložením vybrané verze. Pokud jste upravili integrovanou mapu tabulky, použijte změny znovu. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud při spuštění mapy narazíte na problém, postupujte podle pokynů v části [Problém s chybějícími sloupci tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) průvodce řešením problémů s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Fakturace a ceny | 2754422 | Odhady materiálu a nákladů neplynou do Finance, když jsou projekty zkopírovány do Dataverse. |
| Čas a výdaje | 2787409 | Neplatný schvalovatel může schválit neprojektovou časovou položku. |
| Správa příležitostí | 2788907 | Aktualizovaná chybová zpráva při ověřování jedinečnosti pro řádky objednávky, které obsahují příznaky. |
| Čas a výdaje | 2842253 | Zpracování výjimky null pro schválení času. |
| Fakturace a ceny | 2844181 | Nezískání ID korelace blokuje vytvoření faktury. |
| Fakturace a ceny | 2876628 | QLD, CLD – Rozlišení odhadovaného ceníku by mělo používat starší pole rozsahu dat ceníku. |
| Subdodávka | 2893222 | Pokud není pro řádek dílčí smlouvy zadána žádná role, mělo by být možné vybrat tento řádek u člena týmu pro jakoukoli roli. |

### <a name="project-management-and-accounting-in-finance"></a>Správa projektů a účetnictví ve Finance

Sháníte-li informace o opravách chyb zahrnutých v této aktualizaci, přihlaste se ke službám Microsoft Dynamics Lifecycle Services a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkce zapnuté ve výchozím nastavení v následující verzi

V následující tabulce je uveden seznam funkcí, které jsou ve verzi 10.0.30 ve výchozím nastavení zapnuté. Většinu funkcí, které byly automaticky zapnuty, lze vypnout v části [Správa funkcí](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). V budoucnu mohou být některé funkce, které byly automaticky zapnuty, odebrány ze správy funkcí a stát se povinnými. Tato změna zajišťuje, že zákazníci používají aktuální funkce, takže vylepšení mohou stavět na aktuálních funkcích, když jsou přidávána. Funkce nebudou automaticky aktivovány dříve než za jeden rok, pokud nebudou určeny jako nezbytné.

| Název funkce | Povolit datum | Funkce přidána | Stav funkce | Modul |
| --- | --- | --- |--- |--- |
| Zapnutí asynchronního provozu, když uživatel potřebuje přepínat mezi synchronizačními a asynchronními operacemi | 21. října 2022 | 9. dubna 2021 | Zapnuto ve výchozím nastavení | Řízení výdajů |
| Vyžaduje se vyhodnocení zásad výdajů pro účtenky | 21. října 2022 | 20. prosince 2021 | Zapnuto ve výchozím nastavení | Řízení výdajů |
| Seznam výkazů výdajů vytvořených delegujícími pracovníky | 21. října 2022 | 19. února 2020 | Zapnuto ve výchozím nastavení | Řízení výdajů |
| Výpočet celkových ujetých kilometrů podle fiskálního roku | 21. října 2022 | 10. května 2022 | Zapnuto ve výchozím nastavení | Řízení výdajů |
