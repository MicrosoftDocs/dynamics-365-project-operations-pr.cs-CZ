---
title: Výkon návrhů projektové faktury
description: Tento téma poskytuje informace o vylepšeních výkonu u návrhů projektových faktur.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269782"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="db9a4-103">Výkon návrhů projektové faktury</span><span class="sxs-lookup"><span data-stu-id="db9a4-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db9a4-104">Když vytvoříte nový návrh faktury, můžete narazit na problémy s výkonem, když výrazně naroste celkový počet projektů a dílčích projektů.</span><span class="sxs-lookup"><span data-stu-id="db9a4-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="db9a4-105">Ke zlepšení výkonu je k dispozici funkce, která zkracuje čas potřebný k vytvoření nového návrhu faktury za zaúčtované projektové transakce.</span><span class="sxs-lookup"><span data-stu-id="db9a4-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="db9a4-106">Povolení vylepšení výkonu návrhů projektových faktur</span><span class="sxs-lookup"><span data-stu-id="db9a4-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="db9a4-107">Chcete-li povolit funkci vylepšení výkonu návrhu projektové faktury, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="db9a4-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="db9a4-108">Přejděte do nabídky **Správa funkcí** > **Vše**.</span><span class="sxs-lookup"><span data-stu-id="db9a4-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="db9a4-109">V seznamu funkcí vyhledejte **Vylepšení výkonu návrhu projektové faktury**.</span><span class="sxs-lookup"><span data-stu-id="db9a4-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="db9a4-110">Vyberte **Povolit nyní**.</span><span class="sxs-lookup"><span data-stu-id="db9a4-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="db9a4-111">Obnovte stránku prohlížeče a vytvořte nový návrh faktury.</span><span class="sxs-lookup"><span data-stu-id="db9a4-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="db9a4-112">Vypnutí vylepšení výkonu návrhů projektových faktur</span><span class="sxs-lookup"><span data-stu-id="db9a4-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="db9a4-113">Chcete-li vypnout funkci vylepšení výkonu návrhu projektové faktury, dokončete následující kroky.</span><span class="sxs-lookup"><span data-stu-id="db9a4-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="db9a4-114">Přejděte do nabídky **Správa funkcí** > **Vše**.</span><span class="sxs-lookup"><span data-stu-id="db9a4-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="db9a4-115">V seznamu funkcí vyhledejte **Vylepšení výkonu návrhu projektové faktury**.</span><span class="sxs-lookup"><span data-stu-id="db9a4-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="db9a4-116">Vyberte **Zakázat**.</span><span class="sxs-lookup"><span data-stu-id="db9a4-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="db9a4-117">Aktualizujte okno prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="db9a4-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="db9a4-118">Jsou-li povolena pravidla fakturace, nelze použít výkon návrhu faktury.</span><span class="sxs-lookup"><span data-stu-id="db9a4-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="db9a4-119">Během dávkového procesu vytváření návrhů faktur počet dílčích úkolů rozdělí úkoly na maximální počet na základě počtu smluv s fakturovatelnými transakcemi, bez ohledu na to, co jste zadali.</span><span class="sxs-lookup"><span data-stu-id="db9a4-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="db9a4-120">Například pokud zadáte **3** pro počet dílčích úkolů pro hromadné vytvoření návrhu faktury a existují pouze dvě smlouvy s fakturovatelnými transakcemi, jsou vytvořeny pouze dva dílčí úkoly.</span><span class="sxs-lookup"><span data-stu-id="db9a4-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
