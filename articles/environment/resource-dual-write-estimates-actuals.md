---
title: Integrace odhadů projektu a skutečností
description: Tento téma poskytuje informace o integraci duálního zápisu Project Operations pro odhady projektu a skutečné hodnoty.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c558ab1eb5070f6d1a2db06b630e8807cc67819f9bdd57c15ec346f484e04fe9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006283"
---
# <a name="project-estimates-and-actuals-integration"></a>Integrace odhadů projektu a skutečností

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Tento téma poskytuje informace o integraci duálního zápisu Project Operations pro odhady projektu a skutečné hodnoty.

## <a name="project-estimates"></a>Odhady projektů

Odhady pracovní síly, výdajů a materiálu jsou vytvářeny a udržovány v aplikaci Microsoft Dataverse a synchronizovány do aplikace Finance and Operations pro účetní účely. Operace vytváření, aktualizace a mazání nejsou podporovány prostřednictvím aplikací Finance and Operations.

Vytváření odhadů vyžaduje platnou účetní konfiguraci projektu. Projekty, které jsou spojeny s řádky smlouvy, musí mít platný profil nákladů a výnosů projektu definovaný v pravidlech profilu nákladů a výnosů projektu. Další informace viz [Konfigurace účtování pro fakturovatelné projekty](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Odhady práce

Odhady pracovní síly jsou vytvářeny projektovým manažerem nebo Resource managerem, který projektovému úkolu také přiřadí obecný nebo pojmenovaný prostředek. Záznamy o přiřazení zdrojů lze zkontrolovat na kartě **Přiřazení zdrojů** na stránce **Detaily projektu** v Dataverse. Záznamy přiřazení zdrojů v Dataverse vytvářejí záznamy předpovědi hodin v aplikacích Finance and Operations využívající pomocí **entity integrace Project Operations pro hodinové odhady (msdyn\_resourceassignments)**.

   ![Integrace odhadů práce.](./Media/DW4LaborEstimates.png)

Duální zápis synchronizuje záznamy přiřazení prostředků do pracovní tabulky (**ProjCDSEstimateHoursImport**) a poté pomocí obchodní logiky vytváří a aktualizuje záznamy předpovědí hodin (**ProjForecastEmpl**).

Účetní projektu kontroluje záznamy předpovědi hodin vytvořené v aplikacích Finance and Operations přechodem na **Řízení projektů a účetnictví** > **Všechny projekty** > **Plán** > **Předpovědi hodin**.

## <a name="expense-estimates"></a>Odhady výdajů

Odhady výdajů vytváří projektový manažer na kartě **Odhady výdajů** na stránce **Detaily projektu** v Dataverse. Záznamy o odhadu výdajů jsou uloženy v entitě **Řádek odhadu** v Dataverse. Tyto záznamy odhadů mají transakční třídu **Výdaje** a jsou synchronizovány se záznamy prognózy výdajů v aplikacích Finance and Operations pomocí **entity integrace Project Operations pro odhady výdajů (msdyn\_estimatelines)**.

   ![Integrace odhadů výdajů.](./Media/DW4ExpenseEstimates.png)

Duální zápis synchronizuje záznamy odhadů výdajů do pracovní tabulky **ProjCDSEstimateExpenseImport** a poté pomocí obchodní logiky vytváří a aktualizuje záznamy předpovědí výdajů (**ProjForecastCost**). Řádky odhadu ukládají odhady prodeje a odhady nákladů samostatně. Obchodní logika v aplikacích Finance and Operations naplní jeden záznam prognózy výdajů pomocí tohoto detailu v pracovní tabulce.

Účetní projektu může zkontrolovat záznamy předpovědi výdajů vytvořené v aplikacích Finance and Operations přechodem na **Řízení projektů a účetnictví** > **Všechny projekty** > **Plán** > **Předpovědi výdajů**.

## <a name="material-estimates"></a>Odhady materiálu

Odhady materiálu vytváří projektový manažer na kartě **Odhady materiálu** na stránce **Detaily projektu** v Dataverse. Záznamy o odhadu materiálu jsou uloženy v entitě **Řádek odhadu** v Dataverse. Tyto záznamy odhadů mají transakční třídu **Materiál** a jsou synchronizovány se záznamy prognózy položek v aplikacích Finance and Operations pomocí **tabulky integrace projektu pro odhady výdajů (msdyn\_estimatelines)**.

   ![Integrace odhadů materiálu.](./Media/DW4MaterialEstimates.png)

Duální zápis synchronizuje záznamy odhadů materiálu do pracovní tabulky **ProjForecastSalesImpor** a poté pomocí obchodní logiky vytváří a aktualizuje záznamy předpovědí položek (**ForecastSales**). Řádky odhadu ukládají odhady prodeje a odhady nákladů samostatně. Obchodní logika v aplikacích Finance and Operations naplní jeden záznam prognózy položek pomocí tohoto detailu v pracovní tabulce.

Účetní projektu může zkontrolovat záznamy předpovědi položek vytvořené v aplikacích Finance and Operations přechodem na **Řízení projektů a účetnictví** > **Všechny projekty** > **Plán** > **Předpovědi položek**.

## <a name="project-actuals"></a>Skutečné hodnoty projektu

Skutečné hodnoty projektu jsou vytvořeny v Dataverse na základě času, výdajů, materiálu a fakturační činnosti. V této entitě Dataverse jsou zachyceny všechny provozní atributy těchto transakcí, včetně množství, nákladové ceny, prodejní ceny a projektu. Další informace najdete v části [Skutečné hodnoty](../actuals/actuals-overview.md). Záznamy skutečných hodnot jsou synchronizovány do aplikací Finance and Operations pomocí mapy tabulky s duálním zápisem **Skutečné hodnoty integrace Project Operations (msdyn\_actuals)** pro následné účetnictví.

   ![Integrace skutečných hodnot.](./Media/DW4Actuals.png)

Mapa tabulky **Skutečné hodnoty integrace Project Operations** synchronizuje všechny záznamy z entity **Skutečné hodnoty** v Dataverse s atributem **Přeskočit synchronizaci (pouze interní použití)** nastaveným na **False**. Tato hodnota atributu je nastavena v Dataverse automaticky při vytvoření záznamu. Příklady, kde je tento atribut nastaven na **True**, jsou:

  - Skutečné náklady projektu pro mezipodnikové transakce. Další informace viz [Vytváření mezipodnikových transakcí](../project-accounting/create-intercompany-transactions.md). Tyto záznamy jsou přeskočeny, protože systém znovu vytvoří skutečné náklady projektu v aplikacích Finance and Operations při zaúčtování faktury mezipodnikového dodavatele.
  - Negativní nevyfakturované záznamy o prodeji vytvořené při potvrzení proforma faktury. Tyto záznamy jsou přeskočeny, protože podřízená kniha projektu v aplikacích Finance and Operations nezruší nevyfakturovaný záznam prodeje při fakturaci, ale změní stav na plně fakturovaný.

Mapa tabulky duálního zápisu synchronizuje záznamy skutečných hodnot s pracovní tabulkou **ProjCDSActualsImport**. Tyto záznamy jsou zpracovávány periodickým procesem **Import z pracovní tabulky** při vytváření řádků deníku integrace Project Operations a řádků návrhu faktury projektu. Další informace viz [Integrační deník v Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse také zachycuje vazby mezi skutečnými transakcemi projektu v entitě **Transakční připojení**. Další informace viz [Propojení skutečných hodnot s původními záznamy](../actuals/linkingactuals.md). S aplikacemi Finance and Operations se synchronizují také odkazy mezi skutečnými transakcemi pomocí mapu tabulky s duálním zápisem **Entita integrace pro vztahy projektové transakce (msdyn\_transactionconnections)**. Tyto záznamy jsou používány periodickým procesem **Import z pracovní tabulky** při vytváření řádků deníku integrace Project Operations a řádků návrhu faktury projektu.

Zaúčtování deníku integrace Project Operations a návrhu faktury projektu spustí aktualizaci příslušných záznamů v pracovní tabulce **ProjCDSActualsImport**. Systém zachycuje a zaznamenává následující účetní atributy pro transakce skutečných hodnot:

- Částka ve zúčtovací měně
- Směnný kurz
- Číslo dokladu
- Částka prodejní daně

Mapa tabulky **Skutečné hodnoty integrace Project Operations** aktualizuje příslušné záznamy skutečných hodnot v Dataverse o tyto údaje.
