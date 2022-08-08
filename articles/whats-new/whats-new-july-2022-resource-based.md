---
title: Co je nového, červenec 2022 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Microsoft Dynamics 365 Project Operations z července 2022 pro scénáře založené na zdrojích / neskladových položkách.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183882"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového, červenec 2022 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Tento článek se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.44.0.22
- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

V této verzi nejsou k dispozici žádné aktualizace map duálního zápisu Project Operations. Aktuální seznam a verze map duálního zápisu Project Operations najdete v části [Verze map duálního zápisu Project Operations](../environment/resource-dual-write-maps.md).

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a řešení Finance. Některé funkce a možnosti nemusí fungovat správně, pokud není aktivována nejnovější verze mapy. Aktivní verzi mapy můžete zobrazit ve sloupci **Verze** na stránce **Duální zápis**. Novou verzi mapy můžete aktivovat výběrem **Verze mapy tabulky** výběrem nejnovější verze a poté uložením vybrané verze. Pokud jste upravili integrovanou mapu tabulky, použijte změny znovu. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud při spuštění mapy narazíte na problém, postupujte podle pokynů v části [Problém s chybějícími sloupci tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) průvodce řešením problémů s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Nasazení a konfigurace | 2761472 | Chyba instalace Project Operations je zpracována. |
| Fakturace a ceny | 2746940 | Název řádku subdodávky by měl mít maximální délku 100 znaků. |
| Fakturace a ceny | 2739162 | Zákazníci musí mít možnost vidět tlačítka pásu v zobrazení skutečné mřížky. |
| Plánování a sledování projektu | 2730318 | Aktualizováno ověření pro nepodporované znaky v předmětu projektu. |
| Fakturace a ceny | 2705361 | Do polí sledování projektu musí být zahrnuty skutečné fakturované tržby za milníky. |
| Fakturace a ceny | 2675880 | Zabraňte propojení projektu s řádkem slouvy, který není založen na práci. |
| Fakturace a ceny | 2664396 | Pokud je ceník nabídky uložen bez nabídky, musí se vyskytnout chyba, která říká, že nabídka nemůže být prázdná. |
| Fakturace a ceny | 2184019 | Karta **Fakturace na základě úkolů** by se neměla zobrazovat u projektů, které nemají žádnou podpůrnou smlouvu nebo nabídku. |

### <a name="project-management-and-accounting-in-finance"></a>Správa projektů a účetnictví ve Finance

Sháníte-li informace o opravách chyb zahrnutých v této aktualizaci, přihlaste se ke službám Microsoft Dynamics Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkce zapnuté ve výchozím nastavení v následující verzi

V následující tabulce je uveden seznam funkcí, které jsou ve verzi 10.0.29 ve výchozím nastavení zapnuté. Většinu funkcí, které byly automaticky zapnuty, lze vypnout v části [Správa funkcí](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). V budoucnu mohou být některé funkce, které byly automaticky zapnuty, odebrány ze správy funkcí a stát se povinnými. Tato změna zajišťuje, že zákazníci používají aktuální funkce, takže vylepšení mohou stavět na aktuálních funkcích, když jsou přidávána. Funkce nebudou automaticky aktivovány dříve než za jeden rok, pokud nebudou určeny jako nezbytné.

| Název funkce | Povolit datum | Funkce přidána | Stav funkce | Modul |
| --- | --- | --- |--- |--- |
| Povolit úpravu hodinové transakce na základě změny alokace pravidel financování | 16. září 2022 | 7. října 2020 | Zapnuto ve výchozím nastavení | Přehled řízení projektů a účetnictví |
| Funkce storna zálohové faktury projektové objednávky | 16. září 2022 | 6. října 2021 | Zapnuto ve výchozím nastavení | Přehled řízení projektů a účetnictví |
| Odstraňte řádky návrhu faktury, když používáte Project Operations pro scénáře založené na zdrojích / bez skladových materiálů | 16. září 2022 | 6. října 2021 | Zapnuto ve výchozím nastavení | Přehled řízení projektů a účetnictví |
| Upravte účetnictví na zaúčtované transakci projektu | 16. září 2022 | 10. května 2020 | Zapnuto ve výchozím nastavení | Přehled řízení projektů a účetnictví |
| Povolit výchozí nastavení účetnictví pro projekt | 16. září 2022 | 19. února 2020 | Zapnuto ve výchozím nastavení | Přehled řízení projektů a účetnictví |
| Povolit více řádků smlouvy pro projekt | 16. září 2022 | 29. června 2020 | Zapnuto ve výchozím nastavení | Přehled řízení projektů a účetnictví |
| Pokud aktuální stav schválení neumožňuje úpravy, nastavte hodinové deníky projektu pouze pro čtení | 16. září 2022 | 6. října 2021 | Zapnuto ve výchozím nastavení | Přehled řízení projektů a účetnictví |
| Povolit synchronizaci prodejních řádků z nákupních řádků, když jsou nákupní řádky aktualizovány a je zapnut parametr správy změny nákupní objednávky | 16. září 2022 | 7. října 2020 | Zapnuto ve výchozím nastavení | Přehled řízení projektů a účetnictví |
| Povolte Project Operations v Dynamics 365 Customer Engagement | 16. září 2022 | 29. června 2020 | Zapnuto ve výchozím nastavení | Přehled řízení projektů a účetnictví |
| Funkce opravy zrušení transakce projektu | 16. září 2022 | 13. července 2020 | Zapnuto ve výchozím nastavení | Přehled řízení projektů a účetnictví |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funkce, které se v nadcházející verzi stanou povinnými

V následující tabulce je uveden seznam funkcí, které jsou povinné od verze 10.0.29.

| Název funkce | Povolit datum | Funkce přidána | Stav funkce | Modul |
| --- | --- | --- | --- | --- |
| Vypočítejte přislíbenou hodnotu zdroje financování bez zaokrouhlení směnného kurzu | 16. září 2022 | 14. června 2020 | Povinný | Přehled řízení projektů a účetnictví |
| Povolit účtování úprav projektu se stejným účtem hlavní knihy jako původní transakce | 16. září 2022 | 14. června 2020 | Povinný | Přehled řízení projektů a účetnictví |
| Podrobnosti o potvrzené částce projektové smlouvy | 16. září 2022 | 31. srpna 2019 | Povinný | Přehled řízení projektů a účetnictví |
| Povolit řazení podle zdroje při vytváření návrhu projektové faktury | 16. září 2022 | 31. srpna 2019 | Povinný | Přehled řízení projektů a účetnictví |
