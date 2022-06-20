---
title: Co je nového, únor 2021 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations z února 2021 pro scénáře založené na zdrojích / neskladových položkách.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 38fede1746bcb09700c9c9c5e20653e0c39fea2a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910624"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového, únor 2021 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Tento článek se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse 4.7.0.95
- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.16 

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| **Oblast funkcí** | **Referenční číslo** | **Aktualizace pro zvýšení kvality** |
| --- | --- | --- |
| **Fakturace a ceny** | 2053736 | Podrobnosti řádku faktury jsou nyní dostupné přechodem na **Faktura** > **Související informace**. |
| **Fakturace a ceny** | 2122613 | Akce **Aktivovat** a **Deaktivovat** akce byly odstraněny z entita asociace **Ceník**. |
| **Fakturace a ceny** | 2128606 | Vyřešen problém s **ullReferenceException** v modulu plug-in **GetEstimatesForProject**. |
| **Nasazení a konfigurace** | 2139346 | Vyřešen problém s importem nespravovaného řešení **Dynamics365ProjectOperationsDualWrite**. |
| **Nasazení a konfigurace** | 2140569 | V prostředí Dataverse Teams nesmí být instalováno řešení projektu. |
| **Nasazení a konfigurace** | 2086991 | Omezené přizpůsobení lokalizace webových zdrojů. |
| **Správa příležitostí** | 2136794 | Zobrazí se správná chybová zpráva, když proces **Potvrdit fakturu** nebo **Označit fakturu jako zaplacenou** selže. |
| **Správa příležitostí** | 2139330 | Změna projektového manažera na projektu nesmí resetovat vlastnickou společnost zpět na výchozí hodnotu. |
| **Správa příležitostí** | 2146376 | Opravená částka daně v nezúčtovatelné skutečné hodnotě je vytvořena z potvrzení faktury. |
| **Plánování a sledování projektu** | 2099879 | Nasazení prostředí Dataverse musí vytvořit výchozí kategorii transakcí se statickým ID, a ne náhodně generovat jednu pro každé prostředí. |
| **Plánování a sledování projektu** | 2128577 | Opravena oprávnění uživatele Project Service k aktualizaci kategorie transakcí při přiřazení prostředku. |
| **Plánování a sledování projektu** | 2164035 | Opravené problémy s funkcí **Kopírovat projekt**. |
| **Časový záznam** | 2129161 | Aplikují se přísnější omezení, aby uživatelé nemohli měnit a aktualizovat zadaný nebo schválený časový údaj. |
| **Časový záznam** | 2103572 | Schválení času pro neprojektové časové záznamy nesmí hledat roli schvalovatele projektu. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Řízení projektů a účetnictví v Dynamics 365 Finance 

Další informace o řízení projektů a účetnictví v Dynamics 365 Finance naleznete v [Co je nového Leden 2021 – Projektové operace pro scénáře založené na zdrojích/bez zásob](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Povinné aktualizace

Informace o regulačních aktualizacích pro finanční a provozní aplikace naleznete v části [Regulační aktualizace](/dynamics365/finance/localizations/regulatory-updates). Dalším způsobem, jak se dozvědět o aktualizacích předpisů, je přihlásit se do služby Lifecycle Services (LCS) a zobrazit plánované aktualizace předpisů pomocí nástroje pro vyhledávání problémů. Hledání problému vám umožňuje vyhledávat podle země, typu funkce a vydání.


[!INCLUDE[footer-include](../includes/footer-banner.md)]