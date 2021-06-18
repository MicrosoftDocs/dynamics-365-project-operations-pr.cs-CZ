---
title: Integrace správy výdajů
description: Toto téma poskytuje informace o integraci sestav výdajů Project Operations s použitím duálního zápisu.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7fff69f062bf09fe7ceca61d951b535d2e010bfd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999978"
---
# <a name="expense-management-integration"></a>Integrace správy výdajů

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Toto téma poskytuje informace o integraci sestav výdajů [v nasazení s plnými výdaji](../expense/expense-overview.md) Project Operations s použitím duálního zápisu.

## <a name="expense-categories"></a>Kategorie výdajů

Při plném nasazení výdajů se vytvářejí a udržují kategorie výdajů v aplikacích Finance and Operations. Chcete-li vytvořit novou kategorii výdajů, proveďte následující kroky:

1. V Microsoft Dataverse vytvořte kategorii **Transakce**. Integrace duálního zápisu synchronizuje tuto kategorii transakcí s aplikacemi Finance and Operations. Další informace viz [Konfigurace kategorií projektů](/dynamics365/project-operations/project-accounting/configure-project-categories) a [Integrace dat konfigurace a nastavení Project Operations](resource-dual-write-setup-integration.md). V důsledku této integrace systém vytvoří čtyři záznamy sdílené kategorie v aplikacích Finance and Operations.
2. Ve Finance přejděte na **Správa výdajů** > **Nastavení** > **Sdílené kategorie** a vyberte sdílenou kategorii s třídou transakcí **Výdaje**. Nastavte parametr **Lze použít ve výdajích** na **True** a definujte typ výdajů, který se má použít.
3. Pomocí tohoto záznamu sdílené kategorie vytvořte novou kategorii výdajů přechodem na **Správa výdajů** > **Nastavení** > **Kategorie výdajů** a výběrem **Nový**. Když je záznam uložen, dvojitý zápis používá mapu tabulky **Entita exportu kategorií výdajů projektu integrace Project Operations (msdyn\_expensecategories)** k synchronizaci tohoto záznamu do Dataverse.

  ![Integrace kategorií výdajů](./media/DW6ExpenseCategories.png)

Kategorie výdajů v aplikacích Finance and Operations jsou specifické pro společnost nebo právnickou osobu. Existují samostatné odpovídající záznamy týkající se konkrétních právnických osob Dataverse. Když projektový manažer odhaduje výdaje, nemůže vybrat kategorie výdajů, které byly vytvořeny pro projekt, který vlastní jiná společnost, než společnost, která vlastní projekt, na kterém pracuje. 

## <a name="expense-reports"></a>Sestavy výdajů

Sestavy výdajů jsou vytvářeny a schvalovány v aplikacích Finance and Operations. Další informace viz [Vytváření a zpracování sestav výdajů v Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Po schválení sestavy výdajů projektovým manažerem se zaúčtuje do hlavní knihy. V Project Operations se řádky sestavy výdajů související s projektem zaúčtují pomocí zvláštních pravidel účtování:

  - Náklady související s projektem (včetně nevratné daně) se neúčtují okamžitě na účet nákladů projektu v hlavní knize, ale místo toho se zaúčtují na účet integrace výdajů. Tento účet se konfiguruje na kartě **Řízení projektů a účetnictví** > **Nastavit** > **Parametry řízení projektu a účetnictví**, **Project Operations na Dynamics 365 Customer engagement**.
  - Duální zápis se synchronizuje do Dataverse pomocí mapy tabulky **Entita exportu výdajů projektu integrace Project Operations (msdyn\_expenses)**.
  - Daňová podřízená kniha, podřízená kniha dodavatele a další finanční zaúčtování se zaznamenávají podle potřeby v době zaúčtování sestavy výdajů.

  ![Integrace sestav výdajů](./media/DW6ExpenseReports.png)

Když je záznam zapsán do entity **Výdaje** v Dataverse, systém spustí automatizovaný proces schválení záznamu. V případě potřeby lze stav automatizovaného schvalovacího procesu zkontrolovat v Dataverse tím, že půjdete do **Pokročilé nastavení** > **Systém** > **Systémové úlohy**. Po dokončení schválení se v systému vytvoří záznamy třídy výdajových transakcí v entitě **Skutečné hodnoty**.

Skutečné hodnoty související s výdaji jsou poté zpracovány pomocí mapy tabulky s duálním zápisem **Skutečné hodnoty integrace Project Operations(msdyn\_actuals)**. Další informace viz [Odhady a skutečné hodnoty projektu](resource-dual-write-estimates-actuals.md).

Periodický proces **Import z předvádění** vytvoří v deníku integrace Project Operations řádky deníku související se sestavou výdajů. Výchozí účet offsetu je účet integrace výdajů. Integrační deník účtování vymaže zůstatek účtu pro výdajovou transakci a přesune částku výdajů na účet nákladů projektu. Systém také vytváří transakce podřízené knihy projektu pro účely následné fakturace a uznání výnosů.
