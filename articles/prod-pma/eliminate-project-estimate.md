---
title: Eliminace odhadu projektu
description: Tento téma poskytuje informace o eliminaci odhadu projektu po jeho dokončení.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a4ad06bef7ed66a626c6d2ad7ef01ba5b99d1c0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006908"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="32665-103">Eliminace odhadu projektu</span><span class="sxs-lookup"><span data-stu-id="32665-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32665-104">Projektové odhady poskytují finanční přehled odhadované a plánované práce na projektu.</span><span class="sxs-lookup"><span data-stu-id="32665-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="32665-105">Chcete-li pracovat s odhady projektu, musíte projekt připojit k projektu odhadu.</span><span class="sxs-lookup"><span data-stu-id="32665-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="32665-106">Projekt odhadu je vždy založen na existujícím projektu, na jeden projekt odhadu však může odkazovat více projektů.</span><span class="sxs-lookup"><span data-stu-id="32665-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="32665-107">K projektům odhadu lze připojit pouze investiční projekty s pevnou cenou a tyto projekty musí patřit do stejné skupiny projektů jako projekt odhadu.</span><span class="sxs-lookup"><span data-stu-id="32665-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="32665-108">Chcete-li eliminovat projekt odhadu, musí být hotový.</span><span class="sxs-lookup"><span data-stu-id="32665-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="32665-109">Následující kroky vysvětlují, jak eliminovat odhad.</span><span class="sxs-lookup"><span data-stu-id="32665-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="32665-110">Přejděte do části **Řízení projektů a účetnictví** > **Všechny projekty** a otevřete projekt.</span><span class="sxs-lookup"><span data-stu-id="32665-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="32665-111">Na kartě **Spravovat** vyberte **Odhady** a na stránce **Odhad** vyberte **Eliminovat**.</span><span class="sxs-lookup"><span data-stu-id="32665-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="32665-112">Na stránce **Eliminovat odhad** stránka na kartě **Obecné** nastavte následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="32665-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="32665-113">**Kód období**: Vyberte kód období a vyberte příslušné projekty odhadu.</span><span class="sxs-lookup"><span data-stu-id="32665-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="32665-114">**Datum odhadu**: Vyberte příslušné datum odhadu pro eliminaci.</span><span class="sxs-lookup"><span data-stu-id="32665-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="32665-115">**Eliminovat s varováními WIP**: Tuto možnost povolte, chcete-li uvádět oznámení, když bude eliminován odhad, který je spojen s nedokončenou prací (WIP).</span><span class="sxs-lookup"><span data-stu-id="32665-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="32665-116">Pokud tato možnost není povolena, eliminace nemůže pokračovat, pokud existují neodhadnuté transakce.</span><span class="sxs-lookup"><span data-stu-id="32665-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="32665-117">Tato možnost je k dispozici pouze v případě, že je na projekt odhadu použita eliminace.</span><span class="sxs-lookup"><span data-stu-id="32665-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="32665-118">Není k dispozici, pokud používáte pravidelné zveřejňování účtování.</span><span class="sxs-lookup"><span data-stu-id="32665-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="32665-119">Toto nastavení funguje s nastavením na kartě **Odhad** na stránce **Parametry projektu** ve skupině polí **Povolit eliminaci, když existují neodhadnuté transakce**.</span><span class="sxs-lookup"><span data-stu-id="32665-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="32665-120">**Nastavit fázi na Dokončeno**: Povolením této možnosti nastavíte fázi odhadu projektu na **Hotovo** po spuštění eliminace.</span><span class="sxs-lookup"><span data-stu-id="32665-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="32665-121">**Vytisknout seznam odhadů**: Vyberte informace, které mají být zahrnuty při tisku seznamu odhadů.</span><span class="sxs-lookup"><span data-stu-id="32665-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="32665-122">**Zobrazit Infolog**: Povolením této možnosti zobrazíte Infolog.</span><span class="sxs-lookup"><span data-stu-id="32665-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="32665-123">**Datum zaúčtování**: Vyberte datum zaúčtování odhadu do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="32665-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="32665-124">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="32665-124">Select **OK**.</span></span>
5. <span data-ttu-id="32665-125">Po dokončení procesu eliminace se zobrazí eliminovaný projekt odhadu se zápornou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="32665-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="32665-126">Pokud jste neměli v úmyslu odhad eliminovat, můžete vybrat eliminovat odhad a vybrat **Vrátit eliminaci**.</span><span class="sxs-lookup"><span data-stu-id="32665-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]