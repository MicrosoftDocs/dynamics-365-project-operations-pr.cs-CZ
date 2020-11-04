---
title: Eliminace odhadu projektu
description: Tento téma poskytuje informace o eliminaci odhadu projektu po jeho dokončení.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073833"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="118ac-103">Eliminace odhadu projektu</span><span class="sxs-lookup"><span data-stu-id="118ac-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="118ac-104">Projektové odhady poskytují finanční přehled odhadované a plánované práce na projektu.</span><span class="sxs-lookup"><span data-stu-id="118ac-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="118ac-105">Chcete-li pracovat s odhady projektu, musíte projekt připojit k projektu odhadu.</span><span class="sxs-lookup"><span data-stu-id="118ac-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="118ac-106">Projekt odhadu je vždy založen na existujícím projektu, na jeden projekt odhadu však může odkazovat více projektů.</span><span class="sxs-lookup"><span data-stu-id="118ac-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="118ac-107">K projektům odhadu lze připojit pouze investiční projekty s pevnou cenou a tyto projekty musí patřit do stejné skupiny projektů jako projekt odhadu.</span><span class="sxs-lookup"><span data-stu-id="118ac-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="118ac-108">Chcete-li eliminovat projekt odhadu, musí být hotový.</span><span class="sxs-lookup"><span data-stu-id="118ac-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="118ac-109">Následující kroky vysvětlují, jak eliminovat odhad.</span><span class="sxs-lookup"><span data-stu-id="118ac-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="118ac-110">Přejděte do části **Řízení projektů a účetnictví** > **Všechny projekty** a otevřete projekt.</span><span class="sxs-lookup"><span data-stu-id="118ac-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="118ac-111">Na kartě **Spravovat** vyberte **Odhady** a na stránce **Odhad** vyberte **Eliminovat**.</span><span class="sxs-lookup"><span data-stu-id="118ac-111">On the **Manage** tab, select **Estimates** , and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="118ac-112">Na stránce **Eliminovat odhad** stránka na kartě **Obecné** nastavte následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="118ac-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="118ac-113">**Kód období** : Vyberte kód období a vyberte příslušné projekty odhadu.</span><span class="sxs-lookup"><span data-stu-id="118ac-113">**Period code** : Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="118ac-114">**Datum odhadu** : Vyberte příslušné datum odhadu pro eliminaci.</span><span class="sxs-lookup"><span data-stu-id="118ac-114">**Estimate date** : Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="118ac-115">**Eliminovat s varováními WIP** : Tuto možnost povolte, chcete-li uvádět oznámení, když bude eliminován odhad, který je spojen s nedokončenou prací (WIP).</span><span class="sxs-lookup"><span data-stu-id="118ac-115">**Eliminate with WIP warnings** : Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="118ac-116">Pokud tato možnost není povolena, eliminace nemůže pokračovat, pokud existují neodhadnuté transakce.</span><span class="sxs-lookup"><span data-stu-id="118ac-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="118ac-117">Tato možnost je k dispozici pouze v případě, že je na projekt odhadu použita eliminace.</span><span class="sxs-lookup"><span data-stu-id="118ac-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="118ac-118">Není k dispozici, pokud používáte pravidelné zveřejňování účtování.</span><span class="sxs-lookup"><span data-stu-id="118ac-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="118ac-119">Toto nastavení funguje s nastavením na kartě **Odhad** na stránce **Parametry projektu** ve skupině polí **Povolit eliminaci, když existují neodhadnuté transakce**.</span><span class="sxs-lookup"><span data-stu-id="118ac-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="118ac-120">**Nastavit fázi na Dokončeno** : Povolením této možnosti nastavíte fázi odhadu projektu na **Hotovo** po spuštění eliminace.</span><span class="sxs-lookup"><span data-stu-id="118ac-120">**Set stage to Finished** : Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="118ac-121">**Vytisknout seznam odhadů** : Vyberte informace, které mají být zahrnuty při tisku seznamu odhadů.</span><span class="sxs-lookup"><span data-stu-id="118ac-121">**Print estimate list** : Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="118ac-122">**Zobrazit Infolog** : Povolením této možnosti zobrazíte Infolog.</span><span class="sxs-lookup"><span data-stu-id="118ac-122">**Show Infolog** : Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="118ac-123">**Datum zaúčtování** : Vyberte datum zaúčtování odhadu do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="118ac-123">**Posting date** : Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="118ac-124">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="118ac-124">Select **OK**.</span></span>
5. <span data-ttu-id="118ac-125">Po dokončení procesu eliminace se zobrazí eliminovaný projekt odhadu se zápornou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="118ac-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="118ac-126">Pokud jste neměli v úmyslu odhad eliminovat, můžete vybrat eliminovat odhad a vybrat **Vrátit eliminaci**.</span><span class="sxs-lookup"><span data-stu-id="118ac-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
