---
title: Nastavení Project Operations a integrace dat konfigurace
description: Tento téma poskytuje informace o nastavení a konfiguraci map duálního zápisu Project Operations.
author: sigitac
manager: Annbe
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d5fe81dca30039f99d5d7b9bb459214e540db945
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938964"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Nastavení Project Operations a integrace dat konfigurace

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Tento téma poskytuje informace o integraci duálního zápisu Project Operations pro entity nastavení a konfigurace.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektové smlouvy, řádky smlouvy a projekty

Smlouvy o projektu, řádky smlouvy a projekty jsou vytvářeny v Dataverse a synchronizovány do aplikací Finance and Operations pro další účetnictví. Záznamy v těchto entitách lze vytvářet a mazat pouze v Dataverse. K těmto záznamům v účtu však lze v aplikacích Finance and Operations přidat účetní atributy, jako jsou výchozí hodnoty skupiny DPH a finanční dimenze.

  ![Koncepty integrace projektových smluv](./media/1ProjectContract.jpg)

Sledují se potenciální zákazníci, příležitosti a nabídky prodejní aktivity v Dataverse a nesynchronizují se do aplikací Finance and Operations, protože s touto aktivitou není spojeno žádné následné účetnictví.

Funkce smlouvy o projektu v Dataverse vytvoří záznam smlouvy o projektu v aplikacích Finance and Operations pomocí mapy tabulky **Záhlaví projektové smlouvy (salesorders)**. Uložení projektové smlouvy v Dataverse také zahájí vytváření záznamu zákaznické entity projektové smlouvy. Tento záznam je synchronizován s aplikacemi Finance and Operations pomocí mapy tabulky **Zdroj financování projektu (msdyn\_projectcontractssplitbillingrules)**. Tato mapa také synchronizuje přidání, aktualizace a odstranění zákazníků ze smlouvy o projektu. Rozdělení fakturačních procent mezi zákazníky smluvních projektů je prováděno pouze v Dataverse a není synchronizováno do aplikací Finance and Operations.

Po vytvoření smlouvy o projektu v Dataverse, účetní projektu může aktualizovat účetní atributy této smlouvy projektu v aplikacích Finance and Operations přechodem na **Řízení projektů a účetnictví** > **Projektové smlouvy** > **Nastavení** > **Zobrazit výchozí účetnictví**. Účetní může zkontrolovat provozní atributy projektové smlouvy, jako je požadované datum dodání a výše smlouvy, výběrem ID smlouvy projektu v aplikacích Finance and Operations, které otevírají související záznam smlouvy o projektu v Dataverse.

Entita projektu je synchronizována s aplikacemi Finance and Operations využívajícími mapu tabulky **Projekty V2 (msdyn\_projekty)**. Účetní projektu může:

  - Zkontrolovat projekty v aplikacích Finance and Operations přechodem na **Řízení projektů a účetnictví** > **Všechny projekty**. 
  - Aktualizovat účetní atributy projektu v aplikacích Finance and Operations přechodem na **Řízení projektů a účetnictví** > **Všechny projekty** > **Nastavení** > **Zobrazit výchozí účetnictví**.  
  - Kontrolovat provozní atributy projektu, například odhadované datum zahájení a ukončení, výběrem ID projektu v aplikacích Finance and Operations, které otevírají související záznam projektu v Dataverse.

Projekt je spojen se smlouvou o projektu prostřednictvím entity **Řádek smlouvy o projekt**.

Řádky smlouvy projektu v Dataverse vytvoří fakturační pravidlo smlouvy o projektu v aplikacích Finance and Operations pomocí mapy tabulky **Řádky smlouvy projektu (salesorderdetails)**. Metoda fakturace definuje typ pravidla fakturace kontraktu projektu v aplikacích Finance and Operations:

  - Řádky smlouvy projektu s metodou fakturace času a materiálu vytvářejí pravidlo fakturace času a typu materiálu.
  - Řádky kontraktu s metodou fakturace za pevnou cenu vytvářejí milníkové fakturační pravidlo.

Řádky smlouvy projektu může účetní projektu zkontrolovat v aplikacích Finance and Operations přechodem na **Řízení projektů a účetnictví** > **Smlouvy o projektu** > **Nastavení** > **Zobrazit výchozí účetnictví** a prohlédnutím údajů na kartě **Řádky smlouvy**. Účetní může také na této kartě nastavit výchozí finanční dimenze pro řádky smlouvy metody účtování za pevnou cenu.

## <a name="billing-milestones"></a>Fakturační milníky

Řádky smlouvy projektu využívající metodu fakturace s pevnou cenou jsou fakturovány prostřednictvím milníků fakturace. Milníky fakturace se synchronizují s projektem transakcí na účtu v aplikacích Finance and Operations pomocí mapy tabulky **Milníky řádku smlouvy integrace Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integrace fakturačních milníků](./media/2Milestones.jpg)

Účetní může zkontrolovat transakce na účtu a upravit účetní atributy těchto transakcí přechodem na **Řízení projektů a účetnictví** > **Projektové smlouvy** > **Údržba** > **Transakce na účet** nebo **Řízení projektů a účetnictví** > **Všechny projekty** > **Údržba** > **Transakce na účet**.

Když poprvé vytvoříte milník fakturace pro daný řádek smlouvy projektu, systém automaticky vytvoří projekt odhadu výnosů z pevné ceny pro projekt přidružený k tomuto řádku smlouvy. Projekty odhadu tržeb s pevnou cenou lze zkontrolovat na adrese **Řízení projektů a účetnictví** > **Projekty odhadů výnosů za pevnou cenu**.

### <a name="project-tasks"></a>Projektové úkoly

Úkoly projektu jsou synchronizovány do aplikací Finance and Operations prostřednictvím mapy tabulky **Projektové úkoly (msdyn\_projecttasks)** pouze pro referenční účely. Vytváření, aktualizace a mazání nejsou podporovány prostřednictvím aplikací Finance and Operations.

  ![Integrace úloh projektu](./media/3Tasks.jpg)

## <a name="project-resources"></a>Zdroje projektu

Entita **Role zdrojů projektu** je synchronizována s aplikacemi Finance and Operations pomocí mapy tabulky **Role projektových zdrojů pro všechny společnosti (bookableresourcecategories)** pouze pro referenční účely. Protože role zdrojů v Dataverse nejsou specifické pro společnost, systém automaticky vytvoří příslušné záznamy o rolích zdrojů specifické pro společnost v aplikacích Finance and Operations pro všechny právnické osoby zahrnuté do rozsahu integrace duálního zápisu.

![Integrace rolí zdrojů](./media/5Resources.jpg)

Zdroje projektu v Project Operations jsou udržovány v Dataverse a nejsou synchronizovány do aplikací Finance and Operations.

### <a name="transaction-categories"></a>Kategorie transakcí

Kategorie transakcí jsou udržovány v Dataverse a synchronizováno do aplikací Finance and Operations pomocí mapy tabulky **Kategorie transakcí projektu (msdyn\_transactioncategories)**. Po synchronizaci záznamu kategorie transakce systém automaticky vytvoří čtyři sdílené záznamy kategorie. Každý záznam odpovídá typu transakce v aplikacích Finance and Operations a propojí je se záznamem kategorie transakcí.

![Integrace kategorií transakcí](./media/4TransactionCategories.jpg)

Použití kategorií transakcí pro odhady a skutečné hodnoty vyžaduje, aby účetní projektu nebo správce systému vytvořil odpovídající kategorie projektu u každé právnické osoby. Další informace viz [Konfigurace kategorií projektu](../project-accounting/configure-project-categories.md).
