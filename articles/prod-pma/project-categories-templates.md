---
title: Synchronizace kategorií projektových výdajů mezi Finance and Operations a Project Service Automation
description: Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci kategorií výdajů mezi aplikací Microsoft Dynamics 365 Finance a Dynamics 365 Project Service Automation.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c5513285c8beb96e2aa8b9c67ebde38b3c938edd
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685462"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synchronizace kategorií projektových výdajů mezi Finance and Operations a Project Service Automation

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablony a základní úkoly, které se používají k synchronizaci kategorií výdajů mezi aplikací Dynamics 365 Finance a Dynamics 365 Project Service Automation.

> [!NOTE]
> - Integrace projektových úkolů, kategorie transakcí výdajů, odhady hodin, odhady výdajů a zamykání funkcí jsou k dispozici ve verzi 8.0.
> - Integrace skutečných hodnot je k dispozici ve verzi 8.0.1 nebo novější.
> - Pokud používáte Enterprise Edition 7.3.0, po instalaci aktualizací KB 4132657 a KB 4132660 budete moci pomocí šablon integrovat projektové úkoly, kategorie transakcí výdajů, odhady hodin, odhady výdajů a skutečné hodnoty, a také konfigurovat blokování funkcí. Pokud musíte resetovat rozúčtování, doporučujeme vám také nainstalovat KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Datový tok pro aplikace Project Service Automation a Finance

Řešení integrace aplikací Project Service Automation a Finance využívá funkci integrace dat k synchronizaci dat napříč instancemi aplikací Project Service Automation a Finance. Šablony integrace, které jsou k dispozici s funkcí Integrace dat, umožňují tok dat o kategoriích transakcí výdajů projektu mezi aplikacemi Finance a Project Service Automation.

Pokud jsou kategorie výdajů na projekt řízeny v aplikaci Finance, jde integrační tok nejprve z aplikace Finance do Project Service Automation. Identifikátory integrace kategorií výdajů na projekt se poté aktualizují prostřednictvím synchronizace z Project Service Automation do Finance.

Pokud jsou kategorie výdajů na projekt řízeny v aplikaci Project Service Automation, jde integrační tok nejprve z aplikace Project Service Automation do Finance. Před synchronizací z Project Service Automation musí být kategorie projektů již konfigurovány v aplikaci Finance. Poté proveďte synchronizaci z Finance zpět do Project Service Automation a následně znovu z Project Service Automation do Finance. Tímto způsobem zaručíte propojení kategorií a zabráníte vzniku duplikátů.

> [!NOTE]
> Obvykle jsou kategorie výdajů na projekty řízeny v aplikaci Finance. Pokud však nejsou, nebo pokud již byly v Project Service Automation vytvořeny kategorie výdajů, musíte nejprve synchronizovat pomocí šablony Kategorie transakcí výdajů projektu (PSA do Fin a Ops). Potom proveďte synchronizaci pomocí šablony Kategorie transakcí výdajů projektu (Fin a Ops do PSA). Potom byste měli synchronizaci z Project Service Automation do Finance spustit ještě jednou.
>
> Pokud synchronizujete nejprve z Project Service Automation, musí být před spuštěním synchronizace v aplikaci Finance splněny následující požadavky:
>
> - Sdílená kategorie, která odpovídá kategorii projektu nastavené v Project Service Automation, musí existovat a musí být povolena pro možnosti **Projekt** a **Výdaje**.
> - Pro každý právní subjekt Finance, který musí být integrován, musí existovat následující kategorie projektu:
>
>     - **Kategorie projektu** existuje. 
>     - **Použít ve výdajích** je povoleno.
>     - **Aktivní v deníku** je povoleno.
>     - **Typ transakce** je nastaven na **Výdaje**.

Následující obrázek ukazuje, jak jsou data synchronizována mezi Project Service Automation a Finance.

[![Datový tok pro integraci Project Service Automation s Finance.](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Synchronizace kategorií výdajů projektu z Finance do Project Service Automation

### <a name="template-and-task"></a>Šablona a úkol

Pro přístup k šabloně v centru pro správu Microsoft Power Apps vyberte **Projekty** a poté v pravém horním rohu vyberte **Nový projekt**, aby se vybraly veřejné šablony.

Následující šablona a základní úloha se používají k synchronizaci kategorií výdajů projektu z Finance do Project Service Automation:

- **Název šablony v integraci dat** Kategorie transakcí výdajů na projekt (Fin and Ops do PSA)
- **Název úkolu v projektu:** Synchronizace kategorií do PSA

### <a name="entity-set"></a>Sada entit

| Finance                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Integrační entita pro kategorie | Kategorie transakcí     |

### <a name="entity-flow"></a>Tok entity

Kategorie výdajů na projekt jsou spravovány ve Finance a jsou synchronizovány do Project Service Automation jako kategorie transakcí.

### <a name="power-query"></a>Power Query

Musíte použít Microsoft Power Query pro Excel pro nastavení typu účtování na kategorii transakce při synchronizaci do Project Service Automation. Šablona kategorií transakcí výdajů projektu (Fin a Ops do PSA) poskytuje výchozí sloupec a mapování. Pokud vytvoříte vlastní šablony, je nutné přidat podmíněný sloupec v Power Query. Postupujte takto.

1. Kliknutím na šipku otevřete mapování úkolu kategorie výdajů projektu v šabloně Kategorie transakcí výdajů projektu (Fin a Ops do PSA).
2. Klikněte na odkaz **Pokročilé dotazy a filtrování** a otevřete tak Power Query.
2. Vyberte **Přidat podmíněný sloupec**.
3. Zadejte název nového sloupce, například **TypFakturace**.
4. Zadejte následující podmínku: **Pokud CATEGORYID není rovno null, Pak 19235001, Jinak null**.
5. Klikněte na možnost **OK** na sloupci.
6. Nezapomeňte namapovat tento nový sloupec na stránce mapování.

Následující obrázek ukazuje příklad mapování úlohy šablony v Integraci dat. Mapování zobrazuje informace pole, které budou synchronizovány z Finance do Project Service Automation.

[![Mapování šablon kategorií výdajů projektu na šablony Project Service Automation.](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Synchronizace kategorií výdajů projektu z Project Service Automation do Finance

### <a name="template-and-task"></a>Šablona a úkol

Následující šablona a základní úloha se používají k synchronizaci kategorií výdajů projektu z Project Service Automation do Finance:

- **Název šablony v integraci dat** Kategorie transakcí výdajů na projekt (PSA do Fin and Ops)
- **Název úkolu v projektu:** Synchronizace kategorií do Fin Ops

### <a name="entity-set"></a>Sada entit

| Project Service Automation | Finance                           |
|----------------------------|-----------------------------------|
| Kategorie transakcí     | Integrační entita pro kategorie |

### <a name="entity-flow"></a>Tok entity

Kategorie výdajů na projekt jsou spravovány ve Finance a jsou synchronizovány do Project Service Automation jako kategorie transakcí. Synchronizace zpět do Finance aktualizuje kategorii projektu ve Finance s ID integrace z Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Mapování šablon v integraci dat

Následující obrázek ukazuje příklad mapování úlohy šablony v Integraci dat.

> [!NOTE]
> Mapování zobrazuje informace pole, které budou synchronizovány z Project Service Automation do Finance.

[![Mapování šablon Project Service Automation na šablony Finance.](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]