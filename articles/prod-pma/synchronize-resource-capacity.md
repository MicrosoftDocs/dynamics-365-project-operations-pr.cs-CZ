---
title: Synchronizace kapacity zdroje
description: Toto téma poskytuje informace o tom, jak synchronizovat kapacitu zdroje napříč kalendáři a projekty.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997503"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="ce046-103">Synchronizace kapacity zdroje</span><span class="sxs-lookup"><span data-stu-id="ce046-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce046-104">Procesy pro synchronizaci zdrojů pomáhají zaručit, že informace kalendáře a základního kalendáře se postupně dostávají do plánování zdrojů projektu.</span><span class="sxs-lookup"><span data-stu-id="ce046-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="ce046-105">Pokud se kalendář změní, procesy provedou požadované aktualizace plánování projektových zdrojů.</span><span class="sxs-lookup"><span data-stu-id="ce046-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="ce046-106">Procesy také pomáhají zlepšit výkon, protože informace o zdrojích kalendáře jsou synchronizovány předem.</span><span class="sxs-lookup"><span data-stu-id="ce046-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="ce046-107">Aktualizace informací o plánování prostředků proto probíhají rychleji.</span><span class="sxs-lookup"><span data-stu-id="ce046-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="ce046-108">Doporučujeme naplánovat spouštění procesů v dávce namísto po jednom.</span><span class="sxs-lookup"><span data-stu-id="ce046-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="ce046-109">V opačném případě existuje riziko, že někdo zapomene hraniční datumy období, kdy byly informace naposledy synchronizovány.</span><span class="sxs-lookup"><span data-stu-id="ce046-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="ce046-110">Pokud se nepoužívají správné hraniční datumy, mohou se během synchronizace datumů objevit mezery.</span><span class="sxs-lookup"><span data-stu-id="ce046-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Synchronizace kalendáře](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="ce046-112">Synchronizace souhrnů kapacity zdrojů</span><span class="sxs-lookup"><span data-stu-id="ce046-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="ce046-113">Proces synchronizace je navržen tak, aby synchronizoval všechny informace kalendáře zdrojů.</span><span class="sxs-lookup"><span data-stu-id="ce046-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="ce046-114">Tyto informace zahrnují informace základního kalendáře o všech změnách v tabulce kapacity kalendáře zdrojů projektu.</span><span class="sxs-lookup"><span data-stu-id="ce046-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="ce046-115">Pokud jsou do projektu přidány nové zdroje, synchronizace pomáhá zaručit, že jsou k dispozici aktualizované informace kalendáře.</span><span class="sxs-lookup"><span data-stu-id="ce046-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="ce046-116">Tuto synchronizaci lze provést kdykoli.</span><span class="sxs-lookup"><span data-stu-id="ce046-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="ce046-117">Doporučujeme vám použít dávkovou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="ce046-117">We recommend that you use a batch.</span></span> <span data-ttu-id="ce046-118">Možnosti jsou k dispozici během synchronizace rezervací kapacity.</span><span class="sxs-lookup"><span data-stu-id="ce046-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="ce046-119">Vyberte **Správa projektů a účetnictví** &gt; **Periodické** &gt; **Synchronizace kapacity** &gt; **Synchronizace souhrnů kapacity zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="ce046-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="ce046-120">Nastavte možnosti v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="ce046-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="ce046-121">Možnost</span><span class="sxs-lookup"><span data-stu-id="ce046-121">Option</span></span>      | <span data-ttu-id="ce046-122">Popis</span><span class="sxs-lookup"><span data-stu-id="ce046-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="ce046-123">Kód období</span><span class="sxs-lookup"><span data-stu-id="ce046-123">Period code</span></span> | <span data-ttu-id="ce046-124">Volitelně vyberte kód intervalu datumů hlavní knihy a nastavte tak počáteční a konečné datum procesu synchronizace souhrnů kapacity zdrojů.</span><span class="sxs-lookup"><span data-stu-id="ce046-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="ce046-125">Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="ce046-125">Start date</span></span>  | <span data-ttu-id="ce046-126">Zadejte počáteční datum procesu synchronizace souhrnů kapacity zdrojů.</span><span class="sxs-lookup"><span data-stu-id="ce046-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="ce046-127">Koncové datum</span><span class="sxs-lookup"><span data-stu-id="ce046-127">End date</span></span>    | <span data-ttu-id="ce046-128">Zadejte koncové datum procesu synchronizace souhrnů kapacity zdrojů.</span><span class="sxs-lookup"><span data-stu-id="ce046-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="ce046-129">[![Proces synchronizace](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="ce046-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]