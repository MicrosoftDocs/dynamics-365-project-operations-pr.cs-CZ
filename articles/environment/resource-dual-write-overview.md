---
title: Integrace duálního zápisu Project Operations
description: Tento téma poskytuje přehled integrace projektu s duálním zápisem Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955650"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="121e3-103">Přehled integrace duálního zápisu Project Operations</span><span class="sxs-lookup"><span data-stu-id="121e3-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="121e3-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="121e3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="121e3-105">Project Operations používá [funkce duálního zápisu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) k synchronizaci dat napříč Microsoft Dataverse a Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="121e3-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="121e3-106">Následující obrázek ukazuje, jak jsou data synchronizována jako součást této integrace mezi Dataverse a Finance.</span><span class="sxs-lookup"><span data-stu-id="121e3-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Přehled toků dat Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="121e3-108">Project Operations na Dataverse poskytuje moderní uživatelské rozhraní (UI) a snadnou rozšiřitelnost bez kódování / s malým množstvím kódování pomocí funkcí Power Platform.</span><span class="sxs-lookup"><span data-stu-id="121e3-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="121e3-109">Projektoví manažeři, Resource manageři, členové projektového týmu a další personální pracovníci komunikující se zákazníky vykonávají své činnosti v Project Operations na Dataverse.</span><span class="sxs-lookup"><span data-stu-id="121e3-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="121e3-110">Project Operations ve Finance poskytuje podporu projektového účetnictví a rozpoznávání výnosů.</span><span class="sxs-lookup"><span data-stu-id="121e3-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="121e3-111">Project Operations se připojuje k finančnímu rámci ve Finance pro výpočet DPH, směnných kurzů, vykazování finančních dimenzí a další.</span><span class="sxs-lookup"><span data-stu-id="121e3-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="121e3-112">Účetní projektu pracuje většinou ve Finance.</span><span class="sxs-lookup"><span data-stu-id="121e3-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="121e3-113">Integrace Project Operations se skládá z následující integrace komponent:</span><span class="sxs-lookup"><span data-stu-id="121e3-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="121e3-114">Nastavení Project Operations a integrace dat konfigurace</span><span class="sxs-lookup"><span data-stu-id="121e3-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="121e3-115">Odhady a skutečné hodnoty projektu</span><span class="sxs-lookup"><span data-stu-id="121e3-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="121e3-116">Projektové faktury</span><span class="sxs-lookup"><span data-stu-id="121e3-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="121e3-117">Řízení výdajů</span><span class="sxs-lookup"><span data-stu-id="121e3-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="121e3-118">Faktura dodavatele</span><span class="sxs-lookup"><span data-stu-id="121e3-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
