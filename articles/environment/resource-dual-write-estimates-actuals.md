---
title: Integrace odhadů projektu a skutečností
description: Tento článek poskytuje informace o integraci duálního zápisu Project Operations pro odhady a skutečné hodnoty projektu.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 43c868b051bf141cfc3211669c0a44333b4b2c65
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914578"
---
# <a name="project-estimates-and-actuals-integration"></a>Integrace odhadů projektu a skutečností

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Tento článek poskytuje informace o integraci duálního zápisu Project Operations pro odhady a skutečné hodnoty projektu.

## <a name="project-estimates"></a>Odhady projektů

Odhady projektové práce, nákladů a materiálu jsou vytvářeny a udržovány v Microsoft Dataverse a synchronizovány s finančními a provozními aplikacemi pro účetní účely. Operace vytváření, aktualizace a odstraňování nejsou prostřednictvím finančních a provozních aplikací podporovány.

Vytváření odhadů vyžaduje platnou účetní konfiguraci projektu. Projekty, které jsou spojeny s řádky smlouvy, musí mít platný profil nákladů a výnosů projektu definovaný v pravidlech profilu nákladů a výnosů projektu. Další informace viz [Konfigurace účtování pro fakturovatelné projekty](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Odhady práce

Odhady pracovní síly jsou vytvářeny projektovým manažerem nebo Resource managerem, který projektovému úkolu také přiřadí obecný nebo pojmenovaný prostředek. Záznamy o přiřazení zdrojů lze zkontrolovat na kartě **Přiřazení zdrojů** na stránce **Detaily projektu** v Dataverse. Záznamy přiřazení zdrojů v Dataverse vytvářejí záznamy předpovědi hodin ve finančních a provozních aplikacích pomocí **Integrační entita Project Operations pro odhady hodin (msdyn\_resourceassignments)**.

   ![Integrace odhadů práce.](./Media/DW4LaborEstimates.png)

Duální zápis synchronizuje záznamy přiřazení prostředků do pracovní tabulky (**ProjCDSEstimateHoursImport**) a poté pomocí obchodní logiky vytváří a aktualizuje záznamy předpovědí hodin (**ProjForecastEmpl**).

Účetní projektu kontroluje záznamy předpokládaných hodin vytvořené ve finančních a provozních aplikacích tím, že přejde na **Projektové řízení a účetnictví** > **Všechny projekty** > **Plán** > **Hodinové předpovědi**.

## <a name="expense-estimates"></a>Odhady výdajů

Odhady výdajů vytváří projektový manažer na kartě **Odhady výdajů** na stránce **Detaily projektu** v Dataverse. Záznamy o odhadu výdajů jsou uloženy v entitě **Řádek odhadu** v Dataverse. Tyto záznamy odhadů mají třídu transakce **Výdaj** a jsou synchronizovány se záznamy prognózy výdajů ve finančních a provozních aplikacích, které používají **Integrační entitu Project Operations pro odhady výdajů (msdyn\_estimatelines)**.

   ![Integrace odhadů výdajů.](./Media/DW4ExpenseEstimates.png)

Duální zápis synchronizuje záznamy odhadů výdajů do pracovní tabulky **ProjCDSEstimateExpenseImport** a poté pomocí obchodní logiky vytváří a aktualizuje záznamy předpovědí výdajů (**ProjForecastCost**). Řádky odhadu ukládají odhady prodeje a odhady nákladů samostatně. Obchodní logika ve finančních a provozních aplikacích naplní jeden záznam prognózy výdajů pomocí tohoto detailu v pracovní tabulce.

Účetní projektu mohou kontrolovat záznamy předpokládaných výdajů vytvořené ve finančních a provozních aplikacích tím, že přejde na **Projektové řízení a účetnictví** > **Všechny projekty** > **Plán** > **Předpovědi výdajů**.

## <a name="material-estimates"></a>Odhady materiálu

Odhady materiálu vytváří projektový manažer na kartě **Odhady materiálu** na stránce **Detaily projektu** v Dataverse. Záznamy o odhadu materiálu jsou uloženy v entitě **Řádek odhadu** v Dataverse. Tyto záznamy odhadů mají třídu transakce **Materiál** a jsou synchronizovány se záznamy prognózy položek ve finančních a provozních aplikacích, které používají **Tabulku integrační entity pro odhady materiálu (msdyn\_estimatelines)**.

   ![Integrace odhadů materiálu.](./Media/DW4MaterialEstimates.png)

Duální zápis synchronizuje záznamy odhadů materiálu do pracovní tabulky **ProjForecastSalesImpor** a poté pomocí obchodní logiky vytváří a aktualizuje záznamy předpovědí položek (**ForecastSales**). Řádky odhadu ukládají odhady prodeje a odhady nákladů samostatně. Obchodní logika ve finančních a provozních aplikacích naplní jeden záznam prognózy položek pomocí tohoto detailu v pracovní tabulce.

Účetní projektu mohou kontrolovat záznamy předpokládaných položek vytvořené ve finančních a provozních aplikacích tím, že přejde na **Projektové řízení a účetnictví** > **Všechny projekty** > **Plán** > **Předpovědi položek**.

## <a name="project-actuals"></a>Skutečné hodnoty projektu

Skutečné hodnoty projektu jsou vytvořeny v Dataverse na základě času, výdajů, materiálu a fakturační činnosti. V této entitě Dataverse jsou zachyceny všechny provozní atributy těchto transakcí, včetně množství, nákladové ceny, prodejní ceny a projektu. Další informace najdete v části [Skutečné hodnoty](../actuals/actuals-overview.md). Skutečné záznamy jsou synchronizovány s finančními a provozními aplikacemi pomocí mapy tabulek s duálním zápisem **Skutečné hodnoty integrace Project Operations (msdyn\_actuals)** pro následné účetnictví.

   ![Integrace skutečných hodnot.](./Media/DW4Actuals.png)

Mapa tabulky **Skutečné hodnoty integrace Project Operations** synchronizuje všechny záznamy z entity **Skutečné hodnoty** v Dataverse s atributem **Přeskočit synchronizaci (pouze interní použití)** nastaveným na **False**. Tato hodnota atributu je nastavena v Dataverse automaticky při vytvoření záznamu. Příklady, kde je tento atribut nastaven na **True**, jsou:

  - Skutečné náklady projektu pro mezipodnikové transakce. Další informace viz [Vytváření mezipodnikových transakcí](../project-accounting/create-intercompany-transactions.md). Tyto záznamy jsou přeskočeny, protože systém znovu vytvoří skutečné náklady projektu ve finančních a provozních aplikacích, když je zaúčtována mezipodniková faktura dodavatele.
  - Negativní nevyfakturované záznamy o prodeji vytvořené při potvrzení proforma faktury. Tyto záznamy jsou přeskočeny, protože dílčí účetní kniha projektu ve finančních a provozních aplikacích nestornuje záznam o nevyfakturovaných tržbách při fakturaci, ale změní stav na plně fakturováno.

Mapa tabulky duálního zápisu synchronizuje záznamy skutečných hodnot s pracovní tabulkou **ProjCDSActualsImport**. Tyto záznamy jsou zpracovávány periodickým procesem **Import z pracovní tabulky** při vytváření řádků deníku integrace Project Operations a řádků návrhu faktury projektu. Další informace viz [Integrační deník v Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse také zachycuje vazby mezi skutečnými transakcemi projektu v entitě **Transakční připojení**. Další informace viz [Propojení skutečných hodnot s původními záznamy](../actuals/linkingactuals.md). Odkazy mezi skutečnými transakcemi jsou také synchronizovány s finančními a provozními aplikacemi pomocí mapy tabulek s duálním zápisem **Integrační entita pro vztahy transakcí projektu (msdyn\_transactionconnections)**. Tyto záznamy jsou používány periodickým procesem **Import z pracovní tabulky** při vytváření řádků deníku integrace Project Operations a řádků návrhu faktury projektu.

Zaúčtování deníku integrace Project Operations a návrhu faktury projektu spustí aktualizaci příslušných záznamů v pracovní tabulce **ProjCDSActualsImport**. Systém zachycuje a zaznamenává následující účetní atributy pro transakce skutečných hodnot:

- Částka ve zúčtovací měně
- Směnný kurz
- Číslo dokladu
- Částka prodejní daně

Mapa tabulky **Skutečné hodnoty integrace Project Operations** aktualizuje příslušné záznamy skutečných hodnot v Dataverse o tyto údaje.
