---
title: Co je nového v listopadu 2022 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Microsoft Dynamics 365 Project Operations z listopadu 2022 pro scénáře založené na zdrojích / neskladových položkách.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831074"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového v listopadu 2022 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Tento článek se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.58.0.119
- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

V této verzi nejsou k dispozici žádné aktualizace map duálního zápisu Project Operations. Aktuální seznam a verze map duálního zápisu Project Operations najdete v části [Verze map duálního zápisu Project Operations](../environment/resource-dual-write-maps.md).

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a řešení Finance. Některé funkce a možnosti nemusí fungovat správně, pokud není aktivována nejnovější verze mapy. Aktivní verzi mapy můžete zobrazit ve sloupci **Verze** na stránce **Duální zápis**. Novou verzi mapy můžete aktivovat výběrem **Verze mapy tabulky** výběrem nejnovější verze a poté uložením vybrané verze. Pokud jste upravili integrovanou mapu tabulky, použijte změny znovu. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud při spuštění mapy narazíte na problém, postupujte podle pokynů v části [Problém s chybějícími sloupci tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) průvodce řešením problémů s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Fakturace a ceny | 2781818 | Chyba klíče nenalezena při výchozí ceně pro protokol použití materiálu. |
| Fakturace a ceny | 2922373 | Nelze propojit řádek nabídky s projektem, který byl uzavřen jako ztracená nabídka. |
| Fakturace a ceny | 2943206 | Pole **Řádek smlouvy** v entitě projektu by mělo být volitelné. |
| Fakturace a ceny | 2953182 | Vylepšete chybovou zprávu pro opravné faktury.|
| Fakturace a ceny | 2959500 | Řádek nabídky nelze propojit s projektovým úkolem, který je již spojen se ztracenou nabídkou.|
| Fakturace a ceny | 2959560 | Zpráva „Tento zákazník již má smlouvu na projekt“ přijatá při uzavírání nabídky jako vyhraná v určitých lokalitách. |
| Fakturace a ceny | 3031727 | Přiřazení prostředků se nezdaří, v poli Povinné pole „msdyn_Company“ chybí chyba. |
| Fakturace a ceny | 3036905 | Vlastnící společnost není nikdy inicializována na ProjectTeamMember. |
| Správa příležitostí | 2763519 | Chyba nulové reference v EnsureProjectContractAllowsUpdates. |
| Správa příležitostí | 2783798 | Při importu odhadů projektu na řádku nabídky chybí popisy úkolů pro odhady nákladů a materiálu.|
| Správa příležitostí | 2988635 | Vylepšení popisu chybové zprávy při odstraňování zákazníka z nabídky. |
| Správa příležitostí | 3001191 | Nelze vytvořit cenovou nabídku z příležitosti, kde je způsob fakturace zadán jako null. |
| Upgrade | 3012324 | Konverze projektu se nezdařila u projektu s řídicími znaky jako tabulátor v názvu. || Plánování a sledování projektu | 2790384 | Časový limit čekající OperationSet je příliš krátký. |
| Plánování a sledování projektu | 3044275 | Chybějící lokalizace pro: missingProjectSchedulerErrorMessage. |
| Plánování a sledování projektu | 3044277 | Mřížka Uznání projektu se nenačte, když není plánovač nastaven.|
| Správa zdrojů | 2943153 | Aktualizace karty Sledování, aby se pro Trvání zobrazovala dvě desetinná místa.|
| Subdodávka | 2932774 | Řádek faktury dodavatele pouze pro čtení chybně vyvolá chybu. |
| Subdodávka | 2939556 | Stav záhlaví faktury dodavatele by neměl být nastaven na Odstranit koncept online, pokud není aktivní. |
| Čas a výdaje | 2939998 | Využití nové verze TESA v ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Správa projektů a účetnictví ve Finance

Sháníte-li informace o opravách chyb zahrnutých v této aktualizaci, přihlaste se ke službám Microsoft Dynamics Lifecycle Services a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
