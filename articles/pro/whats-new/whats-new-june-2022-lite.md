---
title: Co je nového - červen 2022 - Project Operations omezené nasazení
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Microsoft Dynamics 365 Project Operations z června 2022 pro omezené nasazení.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959391"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Co je nového - červen 2022 - Project Operations omezené nasazení

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Tento článek se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.43.0.77

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Subdodávka | 2708885 | Opravena chybová zpráva, která se zobrazuje, když uživatel vytvoří záznam záhlaví rezervace rezervovatelného zdroje, kde není vyplněn žádný rezervovatelný zdroj. |
| Plánování a sledování projektu | 2629441 | Opravena logika spouštění pracovního postupu, aby se zabránilo nekonečné smyčce při aktualizaci projektových úkolů. |
| Čas a výdaje | 2641209 | Import časových záznamů z úkolů/rezervací musí uchovávat odkaz na rezervovatelné zdroje. |
| Plánování a sledování projektu | 2651148 | Záhlaví projektového dokumentu musí být chráněno.|
| Plánování a sledování projektu | 2653145 | Přidána ověření, aby bylo zajištěno, že nelze vytvořit záznam projektu, který má v názvu neplatné znaky. |
| Čas a výdaje | 2654710 | Opraveno filtrování na stránce **Schválení**. |
| Fakturace a ceny | 2667805 | Byla přidána ověření, která pomáhají zabránit vytvoření skutečných fakturovaných prodejů, pokud neexistují podpůrné nevyúčtované skutečné prodeje. |
| Fakturace a ceny | 2668378 | Přidána ověření, která pomáhají zabránit přidání vlastní dimenze cen, pokud není vyplněn logický název a název pole. |
| Čas a výdaje | 2700428 | Vylepšená logika schvalování, aby bylo zajištěno, že další sady schválení pro projekt lze zpracovat, i když jedna ze sad schválení uvízne v systémových úlohách. |
