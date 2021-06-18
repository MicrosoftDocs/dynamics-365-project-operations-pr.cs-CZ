---
title: Výkon návrhů projektové faktury
description: Tento téma poskytuje informace o vylepšeních výkonu u návrhů projektových faktur.
author: Yowelle
ms.date: 04/20/2021
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
ms.openlocfilehash: 0e7a9eedc80a88e80b7788be4fe4b2f969be8ba1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999483"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="b1333-103">Výkon návrhů projektové faktury</span><span class="sxs-lookup"><span data-stu-id="b1333-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1333-104">Když vytvoříte nový návrh faktury, můžete narazit na problémy s výkonem, když výrazně naroste celkový počet projektů a dílčích projektů.</span><span class="sxs-lookup"><span data-stu-id="b1333-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="b1333-105">Ke zlepšení výkonu je k dispozici funkce, která zkracuje čas potřebný k vytvoření nového návrhu faktury za zaúčtované projektové transakce.</span><span class="sxs-lookup"><span data-stu-id="b1333-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="b1333-106">Povolení vylepšení výkonu návrhů projektových faktur</span><span class="sxs-lookup"><span data-stu-id="b1333-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="b1333-107">Chcete-li povolit funkci vylepšení výkonu návrhu projektové faktury, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="b1333-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="b1333-108">Přejděte do nabídky **Správa funkcí** > **Vše**.</span><span class="sxs-lookup"><span data-stu-id="b1333-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="b1333-109">V seznamu funkcí vyhledejte **Vylepšení výkonu návrhu projektové faktury**.</span><span class="sxs-lookup"><span data-stu-id="b1333-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="b1333-110">Vyberte **Povolit nyní**.</span><span class="sxs-lookup"><span data-stu-id="b1333-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="b1333-111">Obnovte stránku prohlížeče a vytvořte nový návrh faktury.</span><span class="sxs-lookup"><span data-stu-id="b1333-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="b1333-112">Vypnutí vylepšení výkonu návrhů projektových faktur</span><span class="sxs-lookup"><span data-stu-id="b1333-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="b1333-113">Chcete-li vypnout funkci vylepšení výkonu návrhu projektové faktury, dokončete následující kroky.</span><span class="sxs-lookup"><span data-stu-id="b1333-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="b1333-114">Přejděte do nabídky **Správa funkcí** > **Vše**.</span><span class="sxs-lookup"><span data-stu-id="b1333-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="b1333-115">V seznamu funkcí vyhledejte **Vylepšení výkonu návrhu projektové faktury**.</span><span class="sxs-lookup"><span data-stu-id="b1333-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="b1333-116">Vyberte **Zakázat**.</span><span class="sxs-lookup"><span data-stu-id="b1333-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="b1333-117">Aktualizujte okno prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="b1333-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="b1333-118">Výkon návrhu faktury nelze použít, když jsou povolena pravidla fakturace nebo jsou spuštěny dávkové procesy.</span><span class="sxs-lookup"><span data-stu-id="b1333-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
