---
title: Domovská stránka generování sestav
description: Toto téma poskytuje informace o generování sestav v Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 25486b0c153842cab4331f27eea4872f848bea50
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147690"
---
# <a name="reporting-home-page"></a>Domovská stránka generování sestav

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Aplikace Dynamics 365 Project Service Automation od společnosti Microsoft umožňuje organizacím založeným na projektech efektivně řídit operace jejich podnikání. V jakémkoli projektu musí členové týmu spravovat příležitost, nabídku a plánovat práci, zajišťovat pro projekty zdroje, spravovat práci podle plánu, fakturovat práci a poté práci za účelem dokončení projektu provést. Možnost podávat zprávy o operacích je klíčem k určení stavu organizace a k přijetí potřebných nápravných opatření. PSA používá pro veškeré své vykazování metody a technologie generování sestav Microsoft Dynamics 365. Další informace o možnostech vytváření sestav naleznete v části [Příručka pro psaní sestav pro aplikace Dynamics 365 Customer Engagement (on-premises) verze 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).

## <a name="report-wizard"></a>Průvodce sestavou

Průvodce sestavou umožňuje vytvářet jednoduché sestavy také jiným pracovníkům než vývojářům. Protože je aplikace sestavena na existující platformě, je toto prostředí stejné jako prostředí dokumentované v [Vytvoření nebo úprava sestavy pomocí Průvodce sestavou](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard). Budete však používat entity specifické pro Project Service Automation.

## <a name="custom-sql-server-reporting-services-reports"></a>Vlastní sestavy SQL Server Reporting Services

Pokud váš podnik vyžaduje specifickou sestavu, kterou nelze vytvořit pomocí Průvodce sestavou, můžete vytvořit vlastní sestavu. Je nutné mít nainstalovánu aplikaci Visual Studio od společnost Microsoft spolu s příslušnými rozšířeními Microsoft SQL Server Data Tools a Report Authoring Extensions. Další informace o nástrojích a verzích viz [Prostředí pro psaní sestav pomocí SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools). Informace o tom, jak vytvořit vlastní sestavu viz [Vytvoření nové sestavy pomocí SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).

## <a name="power-bi-insights-apps"></a>Aplikace pro přehledy Power BI

Aplikace Microsoft Power BI a Dynamics 365 vám společně poskytují výkonný způsob práce s daty ve formě aplikací pro přehledy. Informace o dostupnosti aplikací pro přehledy viz [Stránka aplikací pro přehledy Power BI](https://powerbi.microsoft.com/power-bi-insights-apps/).


## <a name="additional-resources"></a>Další materiály
Další informace o generování sestav v PSA viz následující témata:

- [Práce s datovým modelem Project Service](reports-working-project-service-data-model.md)
- [Řídicí panely](reports-dashboards.md)

