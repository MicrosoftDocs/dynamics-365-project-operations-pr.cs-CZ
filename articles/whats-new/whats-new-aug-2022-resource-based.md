---
title: Co je nového v srpnu 2022 - Project Operations pro scénáře založené na zdrojích/položkách, které nejsou na skladě
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Microsoft Dynamics 365 Project Operations ze srpna 2022 pro scénáře založené na zdrojích / neskladových položkách.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 112dbb98de09ef342c03d122a29cb8025058e47f
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348000"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového v srpnu 2022 - Project Operations pro scénáře založené na zdrojích/položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Tento článek se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.45.0.53
- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

V této verzi nejsou k dispozici žádné aktualizace map duálního zápisu Project Operations. Aktuální seznam a verze map duálního zápisu Project Operations najdete v části [Verze map duálního zápisu Project Operations](../environment/resource-dual-write-maps.md).

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a řešení Finance. Některé funkce a možnosti nemusí fungovat správně, pokud není aktivována nejnovější verze mapy. Aktivní verzi mapy můžete zobrazit ve sloupci **Verze** na stránce **Duální zápis**. Novou verzi mapy můžete aktivovat výběrem **Verze mapy tabulky** výběrem nejnovější verze a poté uložením vybrané verze. Pokud jste upravili integrovanou mapu tabulky, použijte změny znovu. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud při spuštění mapy narazíte na problém, postupujte podle pokynů v části [Problém s chybějícími sloupci tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) průvodce řešením problémů s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Správa příležitostí | 2762089 | Ošetření chyb při uzavírání smlouvy jako ztracené, pokud je v organizaci zakázáno automatické ukládání.|

### <a name="project-management-and-accounting-in-finance"></a>Správa projektů a účetnictví ve Finance

Sháníte-li informace o opravách chyb zahrnutých v této aktualizaci, přihlaste se ke službám Microsoft Dynamics Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
