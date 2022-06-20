---
title: Synchronizace odhadů projektu přímo z Project Service Automation do Finance and Operations
description: Tento článek popisuje šablony a základní úkoly, které se používají k synchronizaci odhadovaných hodin na projektu a náklady na projekt přímo z aplikace Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: fb39a377a51b09f04564b4fe8527e34f0ea12682
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920834"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronizace odhadů projektu přímo z Project Service Automation do Finance and Operations

[!include[banner](../includes/banner.md)]

Tento článek popisuje šablony a základní úkoly, které se používají k synchronizaci odhadovaných hodin na projektu a náklady na projekt přímo z aplikace Dynamics 365 Project Service Automation do Dynamics 365 Finance.

> [!NOTE]
> - Integrace projektových úkolů, kategorie transakcí výdajů, odhady hodin, odhady výdajů a zamykání funkcí je k dispozici ve verzi 8.0.
> - Integrace skutečných hodnot je k dispozici ve verzi 8.0.1 nebo novější.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Datový tok pro Project Service Automation do Finance

Řešení integrace aplikací Project Service Automation do Finance využívá funkci integrace dat k synchronizaci dat napříč instancemi aplikací Project Service Automation a Finance. Šablony integrace, které jsou k dispozici s funkcí Integrace dat, umožňují tok dat o odhadech projektových hodin a odhadech projektových výdajů z Project Service Automation do Finance.

Následující obrázek ukazuje, jak jsou data synchronizována mezi Project Service Automation a Finance.

[![Datový tok pro integraci Project Service Automation s Finance.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Odhady projektových hodin

### <a name="template-and-tasks"></a>Šablona a úkoly

Pro přístup k dostupným šablonám v centru pro správu Microsoft Power Apps vyberte **Projekty** a poté v pravém horním rohu vyberte **Nový projekt**, aby se vybraly veřejné šablony.

Následující šablona a základní úlohy se používají k synchronizaci odhadů projektových hodin z Project Service Automation do Finance:

- **Název šablony v integraci dat** Odhady projektových hodin (PSA do Fin and Ops)
- **Název úloh v projektu:**

    - Vztahy transakcí
    - Odhady výdajů

### <a name="entity-set"></a>Sada entit

| Project Service Automation | Finance                                       |
|----------------------------|-----------------------------------------------|
| Projektové úkoly              | Entita integrace pro odhady projektových hodin |

### <a name="entity-flow"></a>Tok entity

Odhady projektových hodin jsou spravovány v aplikaci Project Service Automation a jsou synchronizovány do Finance jako předpovědi projektových hodin.

### <a name="prerequisites"></a>Požadavky

Než může dojít k synchronizaci odhadů projektových hodin, musíte synchronizovat projekty, projektové úkoly a kategorie výdajových transakcí projektu.

### <a name="power-query"></a>Power Query

V šabloně odhadu hodin projektu je nutné použít Microsoft Power Query pro Excel za účelem dokončení těchto úkolů:

- Nastavte ID výchozího modelu předpovědi, který se použije, když integrace vytvoří nové předpovědi hodin.
- Odfiltrujte všechny záznamy specifické pro daný zdroj v úkolu, které selžou při integraci do předpovědí hodin.
- Odfiltrujte všechny prázdné řádky kategorie transakcí. Pokud tento úkol nedokončíte, může to mít za následek nesprávné předpovědi hodin.

#### <a name="set-the-default-forecast-model-id"></a>Nastavte ID výchozího modelu předpovědi

Chcete-li aktualizovat ID výchozího modelu předpovědi v šabloně, otevřete kliknutím na ikonu **Mapovat** mapování. Poté vyberte odkaz **Pokročilý dotaz a filtrování**.

- Pokud používáte výchozí šablonu odhadů projektových hodin (PSA do Fin a Ops), vyberte hodnotu **Vložená podmínka** v seznamu **Aplikované kroky**. V poli **Funkce** nahraďte **O\_předpověď** za název ID modelu předpovědi, který by měl být použit s integrací. Výchozí šablona obsahuje ID modelu předpovědi z ukázkových dat.
- Pokud vytváříte novou šablonu, musíte přidat tento sloupec. V Power Query zvolte **Přidat podmíněný sloupec** a zadejte název nového sloupce, jako například **ModelID**. Zadejte podmínku pro sloupec, kde pokud projektová úloha není null, pak \<enter the forecast model ID\>; jinak null.

#### <a name="filter-out-resource-specific-records"></a>Odfiltrování záznamů specifických pro určitý zdroj

Šablona Odhady projektových hodin (PSA do Fin a Ops) má výchozí filtr, který odstraní všechny záznamy specifické pro nějaký prostředek. Pokud vytvoříte vlastní šablonu, musíte přidat tento filtr. Vyberte odkaz **Pokročilý dotaz a filtrování** a filtrujte sloupec **msdyn\_islinetask** tak, aby byly zahrnuty pouze **Nepravdivé** záznamy.

#### <a name="filter-out-empty-transaction-category-rows"></a>Odfiltrování všech prázdných řádků kategorie transakcí

Chcete-li odstranit všechny řádky, které mají prázdné kategorie transakcí, musíte přidat filtr. Tato úloha je vyžadována bez ohledu na to, zda používáte výchozí šablonu nebo vytváříte vlastní šablonu. Tento filtr odebere všechny souhrnné řádky z Project Service Automation, které by mohly způsobit nesprávné hodinové předpovědi ve Finance. Vyberte odkaz **Pokročilý dotaz a filtrování** a odfiltrujte null záznamy ve sloupci **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Mapování šablon v integraci dat

Následující obrázek ukazuje příklad mapování úlohy šablony v Integraci dat. Mapování zobrazuje informace pole, které budou synchronizovány z Project Service Automation do Finance.

[![Mapování úlohy šablony v integraci dat.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Odhady projektových výdajů

### <a name="template-and-tasks"></a>Šablona a úkoly

Následující šablona a základní úlohy se používají k synchronizaci odhadů projektových výdajů z Project Service Automation do Finance:

- **Název šablony v Integraci dat** Odhady projektových výdajů (PSA do Fin and Ops)
- **Název úloh v projektu:**

    - Vztahy transakcí 
    - Odhady výdajů

### <a name="entity-set"></a>Sada entit

| Project Service Automation | Finance                                                  |
|----------------------------|----------------------------------------------------------|
| Propojení transakcí    | Entita integrace pro vztahy projektových transakcí |
| Řádky odhadu             | Entita integrace pro odhady projektových výdajů         |

### <a name="entity-flow"></a>Tok entity

Odhady projektových výdajů jsou spravovány v aplikaci Project Service Automation a jsou synchronizovány do Finance jako předpovědi projektových výdajů.

### <a name="prerequisites"></a>Požadavky

Než může dojít k synchronizaci odhadů projektových výdajů, musíte synchronizovat projekty, projektové úkoly a kategorie výdajových transakcí projektu.

### <a name="power-query"></a>Power Query

V šabloně odhadů výdajů projektu je nutné použít Power Query pro dokončení následujících úkolů:

- Filtr, který zahrne pouze záznamy řádků odhadu výdajů.
- Nastavte ID výchozího modelu předpovědi, který se použije, když integrace vytvoří nové předpovědi hodin.
- Transformujte typy fakturace.
- Transformujte typy transakcí.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtr, který zahrne pouze řádky odhadu výdajů.

Šablona Odhady projektových výdajů (PSA do Fin a Ops) má výchozí filtr, který do integrace zahrne pouze řádky výdajů. Pokud vytvoříte vlastní šablonu, musíte přidat tento filtr. Vyberte úlohu **Vztahy transakcí** a poté kliknutím na šipku **Mapovat** otevřete mapování. Vyberte odkaz **Pokročilý dotaz a filtrování**. Filtrujte sloupec **msdyn\_transactiontype1** tak, aby obsahoval pouze hodnoty **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Nastavte ID výchozího modelu předpovědi

Chcete-li aktualizovat ID výchozího modelu předpovědi v šabloně, vyberte úlohu **Odhady výdajů** a poté otevřete kliknutím na ikonu **Mapovat** mapování. Vyberte odkaz **Pokročilý dotaz a filtrování**.

- Pokud použijete výchozí šablonu odhadů projektových výdajů (PSA do Fin and Ops), vyberte v Power Query první **Vloženou podmínku** v sekci **Použité kroky**. V poli **Funkce** nahraďte **O\_předpověď** za název ID modelu předpovědi, který by měl být použit s integrací. Výchozí šablona obsahuje ID modelu předpovědi z ukázkových dat.
- Pokud vytváříte novou šablonu, musíte přidat tento sloupec. V Power Query zvolte **Přidat podmíněný sloupec** a zadejte název nového sloupce, jako například **ModelID**. Zadejte podmínku pro sloupec, kde pokud ID řádku odhadu není null, pak \<enter the forecast model ID\>; jinak null.

#### <a name="transform-the-billing-types"></a>Transformace typů fakturace

Šablona Odhady projektových výdajů (PSA do Fin a Ops) obsahuje podmíněný sloupec, který se používá k transformaci typů fakturace, které jsou přijímány z Project Service Automation během integrace. Pokud vytvoříte vlastní šablonu, musíte přidat tento podmíněný sloupec. Vyberte odkaz **Pokročilý dotaz a filtrování** a poté vyberte možnost **Přidat podmíněný sloupec**. Zadejte název nového sloupce, například **TypFakturace**. Poté zadejte následující podmínku:

Když **msdyn\_billingtype** = 192350000, Pak **NonChargeable**  
Jinak Když **msdyn\_billingtype** = 192350001, Pak **Chargeable**  
Jinak Když **msdyn\_billingtype** = 192350002, Pak **Complimentary**  
Jinak **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Transformace typů transakcí

Šablona Odhady projektových výdajů (PSA do Fin a Ops) obsahuje podmíněný sloupec, který se používá k transformaci typů transakcí, které jsou přijímány z Project Service Automation během integrace. Pokud vytvoříte vlastní šablonu, musíte přidat tento podmíněný sloupec. Vyberte odkaz **Pokročilý dotaz a filtrování** a poté vyberte možnost **Přidat podmíněný sloupec**. Zadejte název nového sloupce, například **TypTransakce**. Poté zadejte následující podmínku:

Když **msdyn\_transactiontypecode** = 192350000, Pak **Cost**  
Jinak Když **msdyn\_transactiontypecode** = 192350005, Pak **Sales**  
Jinak **null**

### <a name="template-mapping-in-data-integration"></a>Mapování šablon v integraci dat

Následující obrázky ukazují příklady mapování úlohy šablony v Integraci dat. Mapování zobrazuje informace pole, které budou synchronizovány z Project Service Automation do Finance.

[![Mapování šablon transakcí odhadu výdajů.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Mapování šablon odhadů výdajů.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]