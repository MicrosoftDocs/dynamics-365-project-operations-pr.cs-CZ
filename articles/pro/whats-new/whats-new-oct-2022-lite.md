---
title: Co je nového, říjen 2022 – omezené nasazení Project Operations
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Microsoft Dynamics 365 Project Operations z října 2022 pro omezené nasazení.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806614"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Co je nového, říjen 2022 – omezené nasazení Project Operations

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Tento článek se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.57.0.176

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

| Oblast funkcí | Název funkce | Více informací |
| --- | --- | --- |
| Plánování a sledování projektu | **Externí plánování Project Operations**<br>Režim externího plánování umožňuje zákazníkům nativně vytvářet, aktualizovat a odstraňovat entity, které souvisejí se strukturovaným rozpisem prací, pomocí nativních rozhraní API Dataverse bez aktuálních omezení, která jsou vynucována aplikací Microsoft Project for the Web. | [Externí plánování](/dynamics365/project-operations/project-management/external-scheduling) |
| Nasazení a konfigurace | <p>**Umožnit zákazníkům vybrat si typ nasazení**<br>Produktem řízené aktualizace (PDU) Project Operations se používají k automatické instalaci řešení duálního zápisu Project Operations, když jsou v prostředí nainstalována řešení jádra a orchestrace duálního zápisu.</p><p>Tato funkce zavádí nový parametr **Chování při upgradu řešení** v parametrech projektu. Když je tento parametr nastaven na **Pouze Lite**, PUD už nebudou automaticky instalovat řešení duálního zápisu Project Operations, i když jsou v prostředí nainstalována řešení jádra a orchestrace duálního zápisu. Toto chování bude přínosem pro zákazníky, kteří plánují používat řešení duálního zápisu k integraci prodejních objednávek do finančních a provozních aplikací, ale chtějí používat Project Operations ve zjednodušeném režimu (tj. bez integrace do finančních a provozních aplikací).</p> | |

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Fakturace a ceny | 2316317 | Systém umožňuje vytvářet faktury, které nemají žádné fakturovatelné transakce. |
| Fakturace a ceny | 2737300 | Před otevřením formuláře ověřte dostupnost pole Zákazník. |
| Fakturace a ceny | 2744948 | Přidejte kontrolu nuly pro způsob fakturace. |
| Fakturace a ceny | 2763515 | Popisovač chyby nulové reference, když chybí prodejní smlouva faktury. |
| Fakturace a ceny | 2844301 | Vytvoření dávkové faktury se nezdařilo kvůli chybě. |
| Fakturace a ceny | 2845869 | Nesprávné uložení organizační služby. |
| Fakturace a ceny | 2853729 | Údaje o roli a ceně se aktualizují při změně typu fakturace. |
| Fakturace a ceny | 2940350 | Při stanovení skutečných cen musí být automaticky zadány pouze aktivní ceníky. |
| Nasazení a konfigurace | 3001206 | Entita msdyn\_replaylogheader brání upgradům zákaznických organizací. |
| Správa příležitostí | 2755582 | Popisovač výjimek null v Pomocníkovi pravidla rozdělení fakturace. |
| Správa příležitostí | 2761477 | Při použití rozdělené fakturace po odstranění milníku (záhlaví) zůstanou osiřelé milníky. |
| Správa příležitostí | 2767595 | Když je záznam o využití materiálu otevřen v hlavním formuláři, rezervovatelný zdroj pro záznam se změní na aktuálně přihlášeného uživatele. |
| Plánování a sledování projektu | 2790384 | Časový limit čekající OperationSet je příliš krátký. |
| Správa zdrojů | 2751560 | Nekonzistentní preferované organizační jednotky v požadavku na zdroj. |
| Subdodávka | 2907231 | Fáze procesu dodavatelských faktur nemůže postoupit. |
| Čas a výdaje | 2867363 | Záznamy nevypadnou ze zobrazení Absence/Dovolená ke schválení, když jsou ve frontě ke schválení. |
| Čas a výdaje | 2894405 | TESA: Nepoužívaný adresář POC způsobuje problémy s dodržováním předpisů. |
