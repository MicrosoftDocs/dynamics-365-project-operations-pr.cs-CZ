---
title: Synchronizace projektových úkolů přímo z Project Service Automation do Finance and Operations
description: Toto téma popisuje šablonu a základní úkol, který se používají k synchronizaci projektových úkolů přímo z Microsoft Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 45846d7a6dd7b84fe28f0a78ccc103679236917ea506180c5b383fd2828624eb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992783"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronizace projektových úkolů přímo z Project Service Automation do Finance and Operations

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablonu a základní úkol, který se používají k synchronizaci projektových úkolů přímo z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.

> [!NOTE]
> - Integrace projektových úkolů, kategorie transakcí výdajů, odhady hodin, odhady výdajů a zamykání funkcí jsou k dispozici ve verzi 8.0.
> - Pokud používáte Enterprise Edition 7.3.0, po instalaci aktualizací KB 4132657 a KB 4132660 budete moci pomocí šablon integrovat projektové úkoly, kategorie transakcí výdajů, odhady hodin, odhady výdajů a skutečné hodnoty, a také konfigurovat blokování funkcí. Pokud musíte resetovat rozúčtování, doporučujeme vám také nainstalovat KB 4131710.
> - Integrace skutečných hodnot je k dispozici ve verzi 8.0.1 nebo novější.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Datový tok pro Project Service Automation do Finance

Řešení integrace aplikací Project Service Automation do Finance využívá funkci integrace dat k synchronizaci dat napříč instancemi aplikací Project Service Automation a Finance. Šablona integrace, která je k dispozici s funkcí Integrace dat, umožňuje tok dat o projektových úkolech z Project Service Automation do Finance.

Následující obrázek ukazuje, jak jsou data synchronizována mezi Project Service Automation a Finance.

[![Datový tok pro integraci Project Service Automation s Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Šablona a úkol

Pro přístup k šabloně v centru pro správu Microsoft Power Apps vyberte **Projekty** a poté v pravém horním rohu vyberte **Nový projekt**, aby se vybraly veřejné šablony.

Následující šablona a základní úloha se používají k synchronizaci projektových úkolů z Project Service Automation do Finance:

- **Název šablony v integraci dat** Projektové úkoly (PSA do Fin and Ops)
- **Název úlohy v projektu:** Projektové úkoly

Než může dojít k synchronizaci projektových úkolů, musíte synchronizovat účty projektové smlouvy a projekty.

## <a name="entity-set"></a>Sada entit

| Project Service Automation | Finance                             |
|----------------------------|-------------------------------------|
| Projektové úkoly              | Entita integrace pro projektový úkol |

## <a name="entity-flow"></a>Tok entity

Projektové úkoly jsou spravovány v aplikaci Project Service Automation a jsou synchronizovány do Finance jako projektové aktivity.

## <a name="prerequisites-and-mapping-setup"></a>Předpoklady a nastavení mapování

Než může dojít k synchronizaci projektových úkolů, musíte synchronizovat účty projektové smlouvy a projekty.

## <a name="power-query"></a>Power Query

K filtrování dat musíte použít Microsoft Power Query pro Excel, pokud je splněna následující podmínka:

- V úkolu projektu máte záznamy specifické pro daný prostředek.

Pokud musíte použít Power Query, postupujte podle těchto pokynů:

- Šablona Project tasks (PSA to Fin and Ops) má výchozí filtr, který vylučuje záznamy specifické pro prostředek z úkolu projektu nastavením filtru na **IsLineTask** na **Nepravdivé**. Pokud vytvoříte vlastní šablonu, musíte přidat tento filtr.

## <a name="template-mapping-in-data-integration"></a>Mapování šablon v integraci dat

Následující obrázek ukazuje příklad mapování úlohy šablony v Integraci dat. Mapování zobrazuje informace pole, které budou synchronizovány z Project Service Automation do Finance.

[![Mapování šablon.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]