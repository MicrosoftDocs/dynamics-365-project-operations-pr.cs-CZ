---
title: Projektujte prodejní objednávky pro časové a materiální projekty
description: Toto téma vysvětluje, jak vytvořit prodejní objednávky založené na projektech času a materiálu.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750289"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="8f6f4-103">Projektujte prodejní objednávky pro časové a materiální projekty</span><span class="sxs-lookup"><span data-stu-id="8f6f4-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="8f6f4-104">Toto téma popisuje, jak vytvořit prodejní objednávku pro projekt.</span><span class="sxs-lookup"><span data-stu-id="8f6f4-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="8f6f4-105">Objednávky odběratele lze vytvořit pouze pro projekty typu **čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="8f6f4-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="8f6f4-106">Pokud má časový a věcný projekt na projektové smlouvě více zdrojů financování, musíte povolit **Povolit prodejní objednávky u projektů s více zdroji financování** parametr na stránce **Parametry řízení projektu a účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="8f6f4-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="8f6f4-107">Podpora prodejních objednávek projektů s více zdroji financování je k dispozici od vydání aplikace 10.0.2 a vyšší.</span><span class="sxs-lookup"><span data-stu-id="8f6f4-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="8f6f4-108">Parametr umožňující podporu objednávek projektu s více zdroji financování bude odstraněn ve vlně vydání z dubna 2020, po které bude funkce vždy povolena.</span><span class="sxs-lookup"><span data-stu-id="8f6f4-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="8f6f4-109">Zakázky prodeje založené na projektu můžete vytvořit dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="8f6f4-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="8f6f4-110">Přejděte na projekt.</span><span class="sxs-lookup"><span data-stu-id="8f6f4-110">Go to the project itself.</span></span> <span data-ttu-id="8f6f4-111">V podokně akcí vyberte **Spravovat > Úkoly položek > Prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="8f6f4-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="8f6f4-112">Informace o projektu budou výchozí pro prodejní objednávku z projektu.</span><span class="sxs-lookup"><span data-stu-id="8f6f4-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="8f6f4-113">Pokud má projektová smlouva více než jeden zdroj financování, budete muset vybrat zdroj financování a nastavit zákazníka pro prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="8f6f4-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="8f6f4-114">Pokud pro projekt existuje pouze jeden zdroj financování, zákazník se nastaví automaticky.</span><span class="sxs-lookup"><span data-stu-id="8f6f4-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="8f6f4-115">Přejděte na stránku seznamu **Všechny prodejní objednávky** a vytvořte novou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="8f6f4-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="8f6f4-116">Budete muset vybrat projekt pro prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="8f6f4-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="8f6f4-117">Po výběru projektu bude zákazník nastaven ze zdroje financování, nebo budete muset vybrat zdroj financování, pokud má projektová smlouva více zdrojů financování.</span><span class="sxs-lookup"><span data-stu-id="8f6f4-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

