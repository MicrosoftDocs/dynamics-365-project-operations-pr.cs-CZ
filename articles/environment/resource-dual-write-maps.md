---
title: Verze mapování duálního zápisu Project Operations
description: Tento téma poskytuje seznam map duálního zápisu požadovaných pro Dynamics 365 Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa0342985f2c860cd3cb3f686f0dcaa59d8cfd41
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938962"
---
# <a name="project-operations-dual-write-map-versions"></a>Verze mapování duálního zápisu Project Operations

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Použití Dynamics 365 Project Operations pro scénáře zdrojů / položek, které nejsou na skladě, vyžaduje, aby byla v prostředí spuštěna sada map duálního zápisu. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Potřebné mapy: Řešení orchestrace duálního zápisu

Následující mapy jsou požadovanými předpoklady pro řešení Project Operations. Nezapomeňte spustit mapy uvedené v následující tabulce a všechny související mapové tabulky ve vašem prostředí.

| Mapování tabulky | Počáteční synchronizace |
| --- | --- |
| Registr (msdyn_ledgers) | Vyžaduje počáteční synchronizaci pro mapu tabulky a všechny předpoklady. Předloha pro počáteční synchronizaci v aplikacích Finance and Operations. |
| Právnické osoby (cdm_companies) | Nepovinné. Systém automaticky naplní tuto entitu, když jsou prostředí propojena pomocí duálního zápisu. |
| Zákazníci V3 (účty) | Není nutné pro zřizování. |
| Dodavatelé V2 (msdyn_vendors) | Není nutné pro zřizování. |

1. Ze seznamu map vyberte mapu Hlavní kniha **(msdyn\_ledgers)** se všemi předpoklady a zaškrtněte **Počáteční synchronizace**. V poli **Předloha pro počáteční synchronizaci** vyberte **Aplikace Finance and Operations** pro mapu hlavní knihy i všechny nezbytné mapy. Vyberte **Spustit**.

![Synchronizace mapy registru](media/DW6.png)

1. Stejným způsobem postupujte u všech zbývajících map tabulek uvedených v tabulce výše. Nevybírejte políčko **Počáteční synchronizace** při spuštění těchto map.

## <a name="project-operations-dual-write-maps"></a>Mapy duálního zápisu Project Operations

Následující mapy jsou požadované pro řešení Project Operations.

| **Mapování entity** | **Nejnovější verze** | **Počáteční synchronizace** |
| --- | --- | --- |
| Entita integrace pro vztahy projektových transakcí (msdyn\_transactionconnections) | 1.0.0.0 | Není nutné pro zřizování. |
| Záhlaví kontraktu projektu (prodejní objednávky) | 1.0.0.1 | Není nutné pro zřizování. |
| Řádky smlouvy založené na projektu (salesorderdetails) | 1.0.0.0 | Není nutné pro zřizování. |
| Zdroj financování projektu (msdyn_projectcontractsplitbillingrules) | 1.0.0.1 | Není nutné pro zřizování. |
| Tabulka integrace Project Operations pro odhady materiálu (msdyn\_estimatelines) | 1.0.0.0 | Není nutné pro zřizování. |
| Návrhy faktury projektu V2 (faktury) | 1.0.0.2 | Není nutné pro zřizování. |
| Skutečné hodnoty integrace Project Operations (msdyn_actuals) | 1.0.0.14 | Není nutné pro zřizování. |
| Milníky řádku smlouvy integrace Project Operations (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | Není nutné pro zřizování. |
| Entita integrace Project Operations pro odhady výdajů (msdyn_estimateslines) | 1.0.0.2 | Není nutné pro zřizování. |
| Entita integrace Project Operations pro odhady hodin (msdyn_resourceassignments) | 1.0.0.5 | Není nutné pro zřizování. |
| Entita exportu kategorie výdajů projektu integrace Project Operations (msdyn_expensecategories) | 1.0.0.2 | Není nutné pro zřizování. |
| Entita exportu výdajů projektu integrace Project Operations (msdyn_expenses) | 1.0.0.2 | Není nutné pro zřizování. |
| Entita exportu faktury dodavatele projektu integrace Project Operations (msdyn_projectvendorinvoices) | 1.0.0.0 | Není nutné pro zřizování. |
| Entita exportu řádku faktury dodavatele projektu integrace Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.0 | Není nutné pro zřizování. |
| Role zdrojů projektu pro všechny společnosti (bookableresourcecategories) | 1.0.0.1 | Vyžaduje počáteční synchronizaci pro mapu tabulky k synchronizaci rolí prostředků Projektový manažer a Člen týmu, které jsou naplněny v prostředí Dynamics 365 Dataverse během zřizování. Dataverse je hlavním zdrojem pro počáteční synchronizaci. |
| Projektové úkoly (msdyn_projecttasks) | 1.0.0.4 | Není nutné pro zřizování. |
| Kategorie transakcí projektu (msdyn_transactioncategories) | 1.0.0.0 | Není nutné pro zřizování. |
| Projekty V2 (msdyn_projects) | 1.0.0.1 | Není nutné pro zřizování. |

Chcete-li spustit uvedené mapy, proveďte následující kroky.

1. Aktivujte role prostředků projektu pro mapu tabulky **všechny společnosti (bookableresourcecategories)**, protože tato mapa vyžaduje počáteční synchronizaci. V poli **Předloha pro počáteční synchronizaci** vyberte **Common data service**. 

 ![Synchronizace mapy tabulek rolí zdrojů](media/6ResourceInitialSync.jpg)

 Počkejte, až bude stav mapy **Spuštěná**, než přejdete k dalšímu kroku.

2. Vyberte všechny zbývající požadované mapy. Můžete je filtrovat v seznamu map duálního zápisu pomocí klíčového slova **Projekt** při vyhledávání v pravém horním rohu. Můžete vybrat všechny mapy a poté je spustit. Další informace viz [Správa více map tabulek](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Nezapomeňte také povolit a spustit související mapy entit.

### <a name="project-operations-dual-write-map-versions"></a>Verze mapování duálního zápisu Project Operations

Vždy spusťte nejnovější verzi mapy ve vašem prostředí. Určité funkce a možnosti nemusí fungovat správně, pokud existuje některá z následujících podmínek:

- Mapa není aktivována.
- Nejnovější verze mapy není aktivována. 
- Související mapové tabulky nejsou aktivovány.

Aktivní verzi mapy můžete zobrazit ve sloupci **Verze** na stránce **Duální zápis**. Novou verzi mapy můžete aktivovat výběrem **Verze mapy tabulky** výběrem nejnovější verze a poté uložením vybrané verze. Pokud jste přizpůsobili připravenou mapu tabulky, budete muset změny znovu použít. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).