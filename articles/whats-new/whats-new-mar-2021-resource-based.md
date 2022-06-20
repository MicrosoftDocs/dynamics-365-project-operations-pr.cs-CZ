---
title: Co je nového, březen 2021 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations z března 2021 pro scénáře založené na zdrojích / neskladových položkách.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fbdcb01117c39f879f80319b01d278c91a56e8f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932932"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového, březen 2021 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Tento článek se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.8.0.91 
- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.16 

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse


| **Oblast funkcí** | **Referenční číslo** | **Aktualizace pro zvýšení kvality** |
| --- | --- | --- |
| Fakturace a ceny | 2133873 | Bylo opraveno zobrazení symbolu měny **Jednotková prodejní cena** v mřížce **Odhady výdajů**. |
| Fakturace a ceny | 2174616 | Když získáte nabídku, na vlastní ceník smlouvy se odkazuje v podrobnostech řádku smlouvy, které jsou z nabídky zkopírovány. |
| Správa příležitostí | 2167475 | Opravená částka daně v opravné faktuře, která vznikla nevyfakturovanou skutečnou položkou. |
| Správa příležitostí | 2176285 | Částku daně nelze kopírovat z podrobností kupní smlouvy / řádku nabídky do podrobností smlouvy o nákladech / řádku nabídky. |
| Správa příležitostí | 2188079 | Pravidlo rozdělené fakturace nesmí být vytvořeno pro smlouvy, které nejsou založené na práci. |
| Plánování a sledování | 2125274 | Atribut **Mapa zápisu duálního projektu** pro **mapování počátečního data projektu** byl aktualizován z **msdyn\_taskearlieststart** na **msdyn\_actualstart**. |
| Plánování a sledování | 2138853 | Funkce kopírování projektu byla aktualizována, aby se zajistilo, že se řádky odhadu výdajů, které odkazují na úkoly, zkopírují do cílového projektu. |
| Plánování a sledování | 2154306 | Byly opraveny problémy s odstraněním odhadů výdajů v Project Operations pro scénáře založené na zdrojích. |
| Plánování a sledování | 2173259 | Funkce kopírování projektu byla aktualizována, aby se zajistilo, že se v některých scénářích nezobrazí chybová zpráva **Kopírování WBS**. |
| Čas a výdaje | 2148910 | Byl opraven problém se zobrazením stránky **Upravit záznam** v mřížce **Zadání času**. |
| Čas a výdaje | 2159798 | Zpřísněné ovládací prvky zajišťující, že schválené položky výdajů nelze upravovat. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Řízení projektů a účetnictví v Dynamics 365 Finance

Více informací najdete v tématu [Co je nového, leden 2021 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Povinné aktualizace

Informace o regulačních aktualizacích pro finanční a provozní aplikace naleznete v části [Regulační aktualizace](/dynamics365/finance/localizations/regulatory-updates). Dalším způsobem, jak se dozvědět o aktualizacích předpisů, je přihlásit se do služby LCS a zobrazit plánované aktualizace předpisů pomocí nástroje pro vyhledávání problémů. Hledání problému vám umožňuje vyhledávat podle země, typu funkce a vydání.


[!INCLUDE[footer-include](../includes/footer-banner.md)]