---
title: Členové projektových týmů
description: Toto téma poskytuje informace o tom, jak pracovat s informacemi o členech projektového týmu, s jejich atributy a jak plánovat jejich činnost.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f4941803c657fab55ee2702d9f58d6e333592889
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907987"
---
# <a name="project-team-members"></a>Členové projektových týmů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Členy projektového týmu jsou účastníci projektu, kteří dokončují práci na projektu. Cílem mřížky členů týmu je poskytnout seznam pojmenovaných zdrojů, které jsou vyčleněny k zakázce, a obecných členů týmu, kteří jsou zástupnými zdroji a budou obsazeni později.

V mřížce členů týmu může vedoucí projektu a ostatní účastníci projektu zjistit, kdo je vyčleněn pro projekt. Mohou také zobrazit souhrn rezervací, plánovaného úsilí a přiřazení jednotlivých zdrojů. Mřížka členů týmu umožňuje projektovým manažerům definovat požadavky na zdroje pro obecné členy týmu a spravovat rezervace stávajících členů týmu.

V následující tabulce jsou uvedeny klíčové atributy člena projektového týmu.

| Název pole          | Popis                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Metoda přidělení        | Metoda alokace použitá k rezervaci zdrojů v projektu.                                                                         |
| Typ fakturace             | Vyberte, jestli je tento člen týmu klasifikován jako fakturovatelný.                                                                                                                                       |
| Rezervovatelný zdroj        | Rezervovatelný zdroj vybraný jako náhrada obecného zdroje.                                                                                                                   |
| Stav odstranění            | Stav odstranění člena týmu pro sledování, zda je do PSS odeslán požadavek na odstranění a zda PSS úspěšně odešle zpět odpověď v očekávaném časovém intervalu. |
| Celkové úsilí (hodiny)     | Souhrn úsilí člena týmu, které vynaložil na svá zadání.                                                                                                                         |
| Vynaložené úsilí (hodiny) | Sledování úsilí člena týmu, které vynaložil na svá přiřazení.                                                                                           |
| Zbývající úsilí (hodiny) | Sledování ještě nedokončeného úsilí člena týmu na svá přiřazení.                                                                                    |
| Dokončení                   | Datum ukončení členství v týmu zdrojů.                                                                                                                                            |
| Závazně rezervované hodiny        | Závazně rezervované hodiny člena týmu.                                                                                                                                                                |
| Název pozice            | Název sloužící k identifikaci obecného zdroje.                                                                                                                                   |
| Jednotka zdroje          | Organizační jednotka zdroje, který vykonává tuto práci                                                                                                                      |
| Schvalovatel projektu         | Vyberte, jestli tento člen týmu může schvalovat čas a výdaje.                                                                                                                     |
| Požadované hodiny           | Požadované hodiny člena týmu vycházející z požadavku na člena týmu.                                                                                                                       |
| Role                     | Role, kterou člen týmu plní v tomto týmu.                                                                                                                                |
| Popis pozice     | Zadejte popis role tohoto člena týmu.                                                                                                                             |
| Předběžně rezervované hodiny        | Předběžně rezervované hodiny člena týmu.                                                                                                                                                                 |
| Zahájení                    | Datum zahájení členství v týmu zdrojů.                                                                                                                                          |

V mřížce členů týmu lze provádět následující akce:

- **Rezervovat** : U organizací, které využívají metodiku hybridních rezervací, umožní akce knihy uživatelům rezervovat pojmenovaný zdroj na základě povinných požadavků generovaných obecným členem týmu
- **Generovat požadavek** : Tato akce generuje požadavek.
- **Určit vzor** : Umožňuje projektovým manažerům upravit průběhové křivky požadavků na zdroje na podrobné úrovni. Projektoví manažeři mohou přizpůsobit parametry konkrétním potřebám projektu v případech, kdy se jejich výchozí distribuce nehodí.
- **Odeslat žádost** : Určeno pro organizace využívající centrální metodiku rezervace.
- **Upravit** : Atributy členů týmu lze upravovat, včetně organizační jednotky, role a názvu pozice.
- **Zachovat rezervace** : Když je třeba aktualizovat rezervace zdrojů, zachování rezervací umožňuje manažerovi projektu upravit tyto údaje:

    - Zahájení
    - End
    - Celková alokace úsilí

- **Nový** : Kromě přidávání zdrojů přímo z plánu mohou projektoví manažeři přidávat nové pojmenované nebo obecné členy týmu z mřížky členů týmu.
- **Vymazat** : Po výběru jednoho nebo více členů týmu může projektový manažer odstranit prostředky, které se již na projektu nebudou podílet. Odstraněním člena týmu také odstraníte všechna přidružená přiřazení zdrojů a zrušíte všechny existující rezervace.
