---
title: Nastavení Project Operations a integrace dat konfigurace
description: Tento článek poskytuje informace o tom, jak nastavit a konfigurovat mapy duálního zápisu Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 173ff01e938af48d2d6488d5e59cf4e74b3af8e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914532"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Nastavení Project Operations a integrace dat konfigurace

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Tento článek poskytuje informace o integraci duálního zápisu Project Operations pro entity nastavení a konfigurace.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektové smlouvy, řádky smlouvy a projekty

Projektové smlouvy, řádky smlouvy a projekty se vytvářejí v Dataverse a synchronizují s finančními a provozními aplikacemi pro další účetnictví. Záznamy v těchto entitách lze vytvářet a mazat pouze v Dataverse. K těmto záznamům ve finančních a provozních aplikacích však lze přidat účetní atributy, jako jsou výchozí hodnoty skupiny daně z prodeje a finanční dimenze.

  ![Koncepty integrace projektových smluv.](./media/1ProjectContract.jpg)

Potenciální zákazníci, příležitosti a nabídky prodejních aktivit se sledují v Dataverse a nesynchronizují se s finančními a provozními aplikacemi, protože s touto aktivitou není spojeno žádné následné účetnictví.

Funkčnost projektové smlouvy v Dataverse vytvoří záznam projektové smlouvy ve finančních a provozních aplikacích pomocí mapy tabulky **Záhlaví projektových smluv (salesorders)**. Uložení projektové smlouvy v Dataverse také zahájí vytváření záznamu zákaznické entity projektové smlouvy. Tento záznam je synchronizován s finančními a provozními aplikacemi pomocí mapy tabulky **Zdroj financování projektu (msdyn\_projectcontractssplitbillingrules)**. Tato mapa také synchronizuje přidání, aktualizace a odstranění zákazníků ze smlouvy o projektu. Procenta rozdělení fakturace mezi zákazníky se smlouvou o projektu se ovládají pouze v Dataverse a nejsou synchronizovány s finančními a provozními aplikacemi.

Po vytvoření projektové smlouvy v Dataverse může účetní projektu aktualizovat účetní atributy pro tuto projektovou smlouvu ve finančních a provozních aplikacích tím, že přejde na **Projektové řízení a účetnictví** > **Projektové smlouvy** > **Založit** > **Zobrazit výchozí účetnictví**. Účetní může zkontrolovat atributy smlouvy o provozním projektu, jako je požadované datum dodání a částka smlouvy, výběrem ID smlouvy o projektu ve finančních a provozních aplikacích, které otevře související záznam smlouvy o projektu v Dataverse.

Entita projektu je synchronizována s finančními a provozními aplikacemi pomocí mapy tabulky **Projekty V2 (msdyn\_projects)**. Účetní projektu může:

  - Prohlédněte si projekty ve finančních a provozních aplikacích na **Projektové řízení a účetnictví** > **Všechny projekty**. 
  - Aktualizujte účetní atributy pro projekt ve finančních a provozních aplikacích tím, že přejdete na **Projektové řízení a účetnictví** > **Všechny projekty** > **Založit** > **Zobrazit výchozí účetnictví**.  
  - Zkontrolujte atributy provozního projektu, jako je odhadované datum zahájení a ukončení, výběrem ID projektu ve finančních a provozních aplikacích, které otevře související záznam projektu v Dataverse.

Projekt je spojen se smlouvou o projektu prostřednictvím entity **Řádek smlouvy o projekt**.

Řádky projektové smlouvy v Dataverse vytvoří fakturační pravidlo projektové smlouvy ve finančních a provozních aplikacích pomocí mapy tabulky **Řádky projektových smluv (salesorderdetails)**. Metoda fakturace definuje typ pravidla fakturace projektové smlouvy ve finančních a provozních aplikacích:

  - Řádky smlouvy projektu s metodou fakturace času a materiálu vytvářejí pravidlo fakturace času a typu materiálu.
  - Řádky kontraktu s metodou fakturace za pevnou cenu vytvářejí milníkové fakturační pravidlo.

Řádky projektových smluv může zkontrolovat projektový účetní ve finančních a provozních aplikacích v **Projektové řízení a účetnictví** > **Projektové smlouvy** > **Založit** > **Zobrazit výchozí účetnictví** a kontrolou podrobností na kartě **Řádky smlouvy**. Účetní může na této záložce také nastavit výchozí finanční dimenze pro smluvní řádky způsobu účtování s pevnou cenou.

## <a name="billing-milestones"></a>Fakturační milníky

Řádky smlouvy projektu využívající metodu fakturace s pevnou cenou jsou fakturovány prostřednictvím milníků fakturace. Fakturační milníky jsou synchronizovány s projektem transakcí na účtu ve finančních a provozních aplikacích pomocí mapy tabulky **Milníky řádků smlouvy o integraci Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integrace fakturačních milníků.](./media/2Milestones.jpg)

Účetní může zkontrolovat transakce na účtu a upravit účetní atributy těchto transakcí přechodem na **Řízení projektů a účetnictví** > **Projektové smlouvy** > **Údržba** > **Transakce na účet** nebo **Řízení projektů a účetnictví** > **Všechny projekty** > **Údržba** > **Transakce na účet**.

Když poprvé vytvoříte milník fakturace pro daný řádek smlouvy projektu, systém automaticky vytvoří projekt odhadu výnosů z pevné ceny pro projekt přidružený k tomuto řádku smlouvy. Projekty odhadu tržeb s pevnou cenou lze zkontrolovat na adrese **Řízení projektů a účetnictví** > **Projekty odhadů výnosů za pevnou cenu**.

### <a name="project-tasks"></a>Projektové úkoly

Projektové úlohy jsou synchronizovány s finančními a provozními aplikacemi prostřednictvím mapy tabulky **Projektové úkoly (msdyn\_projecttasks)** pouze pro referenční účely. Operace vytváření, aktualizace a odstraňování nejsou prostřednictvím finančních a provozních aplikací podporovány.

  ![Integrace úloh projektu.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Zdroje projektu

Entita **Role projektových zdrojů** je synchronizována s finančními a provozními aplikacemi pomocí mapy tabulky **Role projektových zdrojů pro všechny společnosti (bookableresourcecategories)** pouze pro referenční účely. Protože role zdrojů v Dataverse nejsou specifické pro společnost, systém automaticky vytváří příslušné záznamy rolí zdrojů specifických pro společnost ve finančních a provozních aplikacích automaticky pro všechny právnické osoby zahrnuté do rozsahu integrace s duálním zápisem.

![Integrace rolí zdrojů.](./media/5Resources.jpg)

Projektové zdroje v Project Operations jsou udržovány v Dataverse a nejsou synchronizovány s finančními a provozními aplikacemi.

### <a name="transaction-categories"></a>Kategorie transakcí

Kategorie transakcí jsou udržovány v Dataverse a synchronizovány s finančními a provozními aplikacemi pomocí mapy tabulky **Kategorie transakcí projektu (msdyn\_transactioncategories)**. Po synchronizaci záznamu kategorie transakce systém automaticky vytvoří čtyři sdílené záznamy kategorie. Každý záznam odpovídá typu transakce ve finančních a provozních aplikacích a propojuje je se záznamem kategorie transakce.

![Integrace kategorií transakcí.](./media/4TransactionCategories.jpg)

Použití kategorií transakcí pro odhady a skutečné hodnoty vyžaduje, aby účetní projektu nebo správce systému vytvořil odpovídající kategorie projektu u každé právnické osoby. Další informace viz [Konfigurace kategorií projektu](../project-accounting/configure-project-categories.md).
