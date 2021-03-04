---
title: Synchronizace skutečných hodnot projektu přímo z Project Service Automation do deníku integrace projektu k zaúčtování ve Finance and Operations
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci skutečných hodnot projektu přímo z Microsoft Dynamics 365 Project Service Automation do Finance and Operations.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: cff62e739e88dc45e7c3d1ea044875f0600f2bc1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073912"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synchronizace skutečných hodnot projektu přímo z Project Service Automation do deníku integrace projektu k zaúčtování ve Finance and Operations

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci skutečných hodnot projektu přímo z Dynamics 365 Project Service Automation do Dynamics 365 Finance.

Šablona synchronizuje transakce z Project Service Automation do pracovní tabulky v modulu Finance. Po dokončení synchronizace **musíte** importovat data z pracovní tabulky do integračního deníku.

> [!NOTE]
> - Integrace skutečných hodnot je k dispozici od verze 8.0.1.
> - Pokud používáte Enterprise Edition 7.3.0, po instalaci aktualizací KB 4132657 a KB 4132660 budete moci pomocí šablon integrovat projektové úkoly, kategorie transakcí výdajů, odhady hodin, odhady výdajů a skutečné hodnoty, a také konfigurovat blokování funkcí. Pokud musíte resetovat rozúčtování, doporučujeme vám také nainstalovat KB 4131710.
> - Pokud používáte verzi 7.3.0 a přenášíte transakce poplatků z Project Service Automation, musíte nainstalovat KB 4345320, abyste mohli zahrnout tyto poplatky do faktury projektu.
> - Pokud zadáváte částky daně z obratu v časových nebo výdajových transakcích v Project Service Automation, musíte nainstalovat aktualizaci Project Service Automation Update 7. V opačném případě nebudou skutečné hodnoty daně propojeny s přidruženými skutečnými časovými nebo výdajovými údaji a nebudou synchronizovány s modulem Finance. Další informace vám poskytne tým podpory.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Datový tok pro Project Service Automation do Finance

Řešení integrace aplikací Project Service Automation do Finance využívá funkci integrace dat k synchronizaci dat napříč instancemi aplikací Project Service Automation a Finance. Šablony integrace, které jsou k dispozici s funkcí Integrace dat, umožňují tok dat o skutečných hodnotách projektu z Project Service Automation do Finance.

Následující obrázek ukazuje, jak jsou data synchronizována mezi Project Service Automation a Finance.

[![Datový tok pro integraci Project Service Automation s Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Skutečné hodnoty projektu z Project Service Automation

### <a name="template-and-tasks"></a>Šablona a úkoly

Pro přístup k dostupným šablonám v centru pro správu Microsoft Power Apps vyberte **Projekty** a poté v pravém horním rohu vyberte **Nový projekt** , aby se vybraly veřejné šablony.

Následující šablona a základní úlohy se používají k synchronizaci skutečných hodnot projektu z Project Service Automation do Finance:

- **Název šablony v integraci dat** Skutečné hodnoty projektu (PSA do Fin and Ops)
- **Název úloh v projektu:**

    - Skutečnost
    - TransactionConnections

### <a name="entity-set"></a>Sada entit

| Project Service Automation | Finance                                   |
|----------------------------|----------------------------------------------------------|
| Skutečnost                    | Entita integrace pro skutečné hodnoty projektu                   |
| Propojení transakcí    | Entita integrace pro vztahy projektových transakcí |

### <a name="entity-flow"></a>Tok entity

Odhady skutečných hodnot projektu hodin jsou spravovány v aplikaci Project Service Automation a jsou synchronizovány s deníkem integrace projektu v modulu Finance. Účetnictví bude použito na základě výchozích finančních dimenzí a nastavení účtování.

### <a name="prerequisites"></a>Požadavky

Než může dojít k synchronizaci skutečných hodnot, musíte nakonfigurovat parametry integrace Project Service Automation a synchronizovat projekty, úkoly projektu a kategorie výdajových transakcí projektu.

### <a name="power-query"></a>Power Query

V šabloně skutečných hodnot projektu musíte použít Microsoft Power Query pro Excel k dokončení těchto úkolů:

- Transformujte typ transakce v Project Service Automation na správný typ transakce v Finance. Tato transformace je již definována v šabloně Skutečné hodnoty projektu (PSA do Fin and Ops).
- Transformujte typ fakturace v Project Service Automation na správný typ fakturace v Finance. Tato transformace je již definována v šabloně Skutečné hodnoty projektu (PSA do Fin and Ops). Typ fakturace je poté namapován na vlastnost řádku na základě konfigurace na stránce **Parametry integrace Project Service Automation**.
- Filtrujte na konkrétní organizační jednotky prostředků, které je třeba synchronizovat s touto šablonou.
- Pokud budou mezipodnikový čas nebo skutečné mezipodnikové výdaje synchronizovány s modulem Finance, musíte transformovat organizační jednotku smlouvy na správnou právnickou osobu v Finance. V šabloně Skutečné hodnoty projektu (PSA do Fin and Ops) je definován podmíněný sloupec založený na ukázkových datech. Poslední vložený podmíněný sloupec musíte aktualizovat na správné právnické osoby. V opačném případě může dojít k chybě integrace nebo k importu nesprávných skutečných transakcí do Finance.
- Pokud se mezipodnikový čas nebo skutečné mezipodnikové výdaje nesynchronizují s Finance, musíte odstranit poslední vložený podmíněný sloupec ze své šablony. V opačném případě může dojít k chybě integrace nebo k importu nesprávných skutečných transakcí do Finance.

#### <a name="contract-organizational-unit"></a>Smluvní organizační jednotka
Chcete-li aktualizovat vložený podmíněný sloupec v šabloně, otevřete kliknutím na ikonu **Mapovat** mapování. Kliknutím na odkaz **Pokročilý dotaz a filtrování** otevřete Power Query.

- Pokud používáte výchozí šablonu skutečných hodnot projektu (PSA do Fin and Ops), vyberte v Power Query podlední hodnotu **Vložená podmínka** v seznamu **Aplikované kroky**. V poli **Funkce** nahraďte **USSI** názvem právnické osoby, která by měla být použita s integrací. Do záznamu **Funkce** přidejte podle potřeby další podmínky a aktualizujte podmínku **else** z **USMF** na správnou právnickou osobu.
- Pokud vytváříte novou šablonu, musíte přidat sloupec, abyste podpořili mezipodnikový čas a výdaje. Vyberte **Přidat podmíněný sloupec** a zadejte název nového sloupce, například **LegalEntity**. Zadejte podmínku pro sloupec, kde pokud **název msdyn\_contractorganizationalunitid.msdyn\_** je \<organizational unit\>, pak \<enter the legal entity\> ; jinak null.

### <a name="template-mapping-in-data-integration"></a>Mapování šablon v integraci dat

Následující obrázky ukazují příklady mapování úlohy šablony v Integraci dat. Mapování zobrazuje informace pole, které budou synchronizovány z Project Service Automation do Finance.

[![Mapování šablon – Skutečnosti](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Mapování šablon – Propojení transakcí](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Import z pracovní tabulky po integraci z Project Service Automation

Periodický proces Import z pracovní tabulky musí být spuštěn po synchronizaci skutečných hodnot z Project Service Automation do Finance. Tento proces naimportuje transakce projektu z pracovní tabulky do integračního deníku Project Service Automation, kde se použije účetnictví a lze zaúčtovat importované transakce. Doporučujeme spustit tento proces v dávkovém režimu; lze jej volitelně nastavit tak, aby fungoval jako opakující se dávka.

## <a name="update-actuals-from-finance"></a>Aktualizace skutečných hodnot z modulu Finance

### <a name="template-and-tasks"></a>Šablona a úkoly

Následující šablona a podkladové úlohy se používají k synchronizaci čísla dokladu a daně z obratu za zaúčtované transakce projektu z Finance do Project Service Automation:

- **Název šablony v integraci dat** Aktualizace skutečných hodnot projektu (Fin Ops do PSA)
- **Název úloh v projektu:**

    - Skutečnost 
    - TransactionConnections

### <a name="entity-set"></a>Sada entit

| Finance                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Entita integrace pro skutečné hodnoty projektu                   | Skutečnost                    |
| Entita integrace pro vztahy projektových transakcí | Propojení transakcí    |

### <a name="entity-flow"></a>Tok entity

Odhady skutečných hodnot projektu hodin jsou spravovány v aplikaci Project Service Automation a jsou synchronizovány s deníkem integrace projektu v modulu Finance. Po zveřejnění skutečných hodnot v modulu Finance se aktualizují v Project Service Automation o číslo dokladu z Finance. Pokud byly ve Finance přidány daně z obratu, v Project Service Automation se vytvoří nové skutečné hodnoty daně.

### <a name="power-query"></a>Power Query

V šabloně skutečných hodnot projektu musíte použít Power Query k dokončení těchto úkolů:

- Transformujte typ transakce ve Finance na správný typ transakce v Project Service Automation. Tato transformace je již definována v aktualizaci šablony Skutečné hodnoty projektu (Fin Ops do PSA).
- Transformujte typ fakturace v modulu Finance na správný typ fakturace v Project Service Automation. Tato transformace je již definována v aktualizaci šablony Skutečné hodnoty projektu (Fin Ops do PSA).

### <a name="template-mapping-in-data-integration"></a>Mapování šablon v integraci dat

Následující obrázky ukazují příklady mapování úlohy šablony v Integraci dat. Mapování zobrazuje informace pole, které budou synchronizovány z Finance do Project Service Automation.

[![Mapování šablon – Aktualizace skutečností](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Mapování šablon – Aktualizace transakce](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]