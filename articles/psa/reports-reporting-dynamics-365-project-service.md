---
title: Domovská stránka generování sestav
description: Toto téma poskytuje informace o generování sestav v Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 30411818bdc1b370a71148cf79f743413167dab2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074007"
---
# <a name="reporting-home-page"></a><span data-ttu-id="19186-103">Domovská stránka generování sestav</span><span class="sxs-lookup"><span data-stu-id="19186-103">Reporting home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="19186-104">Aplikace Dynamics 365 Project Service Automation od společnosti Microsoft umožňuje organizacím založeným na projektech efektivně řídit operace jejich podnikání.</span><span class="sxs-lookup"><span data-stu-id="19186-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="19186-105">V jakémkoli projektu musí členové týmu spravovat příležitost, nabídku a plánovat práci, zajišťovat pro projekty zdroje, spravovat práci podle plánu, fakturovat práci a poté práci za účelem dokončení projektu provést.</span><span class="sxs-lookup"><span data-stu-id="19186-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="19186-106">Možnost podávat zprávy o operacích je klíčem k určení stavu organizace a k přijetí potřebných nápravných opatření.</span><span class="sxs-lookup"><span data-stu-id="19186-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="19186-107">PSA používá pro veškeré své vykazování metody a technologie generování sestav Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="19186-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="19186-108">Další informace o možnostech vytváření sestav naleznete v části [Příručka pro psaní sestav pro aplikace Dynamics 365 Customer Engagement (on-premises) verze 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="19186-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="19186-109">Průvodce sestavou</span><span class="sxs-lookup"><span data-stu-id="19186-109">Report Wizard</span></span>

<span data-ttu-id="19186-110">Průvodce sestavou umožňuje vytvářet jednoduché sestavy také jiným pracovníkům než vývojářům.</span><span class="sxs-lookup"><span data-stu-id="19186-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="19186-111">Protože je aplikace sestavena na existující platformě, je toto prostředí stejné jako prostředí dokumentované v [Vytvoření nebo úprava sestavy pomocí Průvodce sestavou](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="19186-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="19186-112">Budete však používat entity specifické pro Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="19186-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="19186-113">Vlastní sestavy SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="19186-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="19186-114">Pokud váš podnik vyžaduje specifickou sestavu, kterou nelze vytvořit pomocí Průvodce sestavou, můžete vytvořit vlastní sestavu.</span><span class="sxs-lookup"><span data-stu-id="19186-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="19186-115">Je nutné mít nainstalovánu aplikaci Visual Studio od společnost Microsoft spolu s příslušnými rozšířeními Microsoft SQL Server Data Tools a Report Authoring Extensions.</span><span class="sxs-lookup"><span data-stu-id="19186-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="19186-116">Další informace o nástrojích a verzích viz [Prostředí pro psaní sestav pomocí SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="19186-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="19186-117">Informace o tom, jak vytvořit vlastní sestavu viz [Vytvoření nové sestavy pomocí SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="19186-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="19186-118">Aplikace pro přehledy Power BI</span><span class="sxs-lookup"><span data-stu-id="19186-118">Power BI insights apps</span></span>

<span data-ttu-id="19186-119">Aplikace Microsoft Power BI a Dynamics 365 vám společně poskytují výkonný způsob práce s daty ve formě aplikací pro přehledy.</span><span class="sxs-lookup"><span data-stu-id="19186-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="19186-120">Informace o dostupnosti aplikací pro přehledy viz [Stránka aplikací pro přehledy Power BI](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="19186-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="19186-121">Další materiály</span><span class="sxs-lookup"><span data-stu-id="19186-121">Additional resources</span></span>
<span data-ttu-id="19186-122">Další informace o generování sestav v PSA viz následující témata:</span><span class="sxs-lookup"><span data-stu-id="19186-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="19186-123">Práce s datovým modelem Project Service</span><span class="sxs-lookup"><span data-stu-id="19186-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="19186-124">Řídicí panely</span><span class="sxs-lookup"><span data-stu-id="19186-124">Dashboards</span></span>](reports-dashboards.md)

