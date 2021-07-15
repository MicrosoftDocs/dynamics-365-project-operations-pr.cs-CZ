---
title: Přehled aplikace Project Service Automation
description: Toto téma poskytuje informace o Dynamics 365 Project Service Automation na Dynamics 365 Finance integrační řešení.
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c756caec6cd7eda8f891446d3e8309aca3b2482
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369611"
---
# <a name="project-service-automation-overview"></a>Přehled aplikace Project Service Automation

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Řešení integrace aplikací Project Service Automation do Finance využívá funkci integrace dat k synchronizaci dat napříč instancemi aplikací Dynamics 365 Finance a Dynamics 365 Project Service Automation přes Common Data Service. Šablony integrace, která jsou k dispozici s funkcí integrace dat, umožňují tok dat o projektových smlouvách, projektech, řádcích projektových smluv, milníků řádků, projektových úkolů, kategorií transakcí výdajů, odhadů hodinových cen a výdajů z Project Service Automation do Finance.

> [!NOTE]
> - Pokud používáte verzi 7.3.0, musíte si nainstalovat aktualizaci KB 4074835. Poté budete moci integrovat projekty s pevnou cenou.
> - Pokud používáte verzi 7.3.0 a přenášíte transakce poplatků z Project Service Automation, musíte nainstalovat KB 4345320, abyste mohli zahrnout tyto poplatky do faktury projektu.
> - Pokud používáte verzi 8.0, budete moci používat projektové úkoly, kategorie transakcí výdajů, odhady hodin, odhady výdajů a zamykání funkcí.
> - Pokud používáte verzi 8.0.1 nebo novější, budete moci synchronizovat skutečné údaje.

Než budete moci integrovat Project Service Automation Finance, musíte nakonfigurovat integrační parametry Project Service Automation. Pro další informace viz [Integrační paramenty Project Service Automation](PSA-parameters.md)

Toto integrační řešení umožňuje přímou synchronizaci v následujících scénářích:

- Udržujte projektové smlouvy v Project Service Automation a synchronizujte je přímo z Project Service Automation do Finance.
- Vytvořte projekty v Project Service Automation a synchronizujte je přímo z Project Service Automation do Finance.
- Udržujte řádky projektových smluv v Project Service Automation a synchronizujte je přímo z Project Service Automation do Finance.
- Udržujte milníky řádků projektových smluv v Project Service Automation a synchronizujte je přímo z Project Service Automation do Finance.
- Udržujte úkoly projektů v Project Service Automation a synchronizujte je přímo z Project Service Automation do Finance.
- Udržujte kategorie transakcí výdajů ve Finance a synchronizujte je přímo z Finance do Project Service Automation.
- Vytvořte odhady projektových hodin v Project Service Automation a synchronizujte je přímo z Project Service Automation do Finance.
- Vytvořte odhady projektových výdajů v Project Service Automation a synchronizujte je přímo z Project Service Automation do Finance.
- Vytvořte v projektu Project Service Automation skutečné údaje o čase, výdajích a poplatcích za projekt a vytvořte transakce projektu v deníku integrace Project Service Automation, aby je bylo možné zaúčtovat ve Finance.

## <a name="data-synchronization"></a>Synchronizace dat

Následující obrázek ukazuje, jak jsou data synchronizována jako součást integrace mezi Project Service Automation a Finance.

> [!NOTE]
> V současné době nejsou k dispozici všechny šablony. Šablony budou vydány, jakmile budou dokončeny.

[![Integrace Project Service Automation s Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Systémové požadavky na Finance

Chcete-li použít integrační řešení Project Service Automation to Finance, musíte nainstalovat Enterprise edition 7.3 s aktualizací platformy 12 nebo novější.

## <a name="system-requirements-for-project-service-automation"></a>Systémové pozadavky pro Project Service Automation

Chcete-li použít integrační řešení Project Service Automation to Finance, musíte nainstalovat následující součásti:

- Dynamics 365 Project Service Automation verze 9.0.0.0 nebo vyšší
- Řešení vyhlídky na hotovost pro Dynamics 365 Sales, verze 1.14.0.0 (v14) nebo novější
- Řešení Project Service Automation to Finance pro Dynamics 365 Project Service Automation verzi 1.0.0.0 nebo novější

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Nainstalujte řešení integrace Project Service Automation to Finance do instance Project Service Automation

Stáhněte si řešení integrace řešení Project Service Automation to Finance z [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) a postupujte podle pokynů, které jsou součástí řešení.


[!INCLUDE[footer-include](../includes/footer-banner.md)]