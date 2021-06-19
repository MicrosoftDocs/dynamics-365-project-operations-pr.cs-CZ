---
title: Sady schválení
description: Tento téma poskytuje informace o sadě schválení, požadavcích a podmnožinách těchto operací.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116863"
---
# <a name="approval-sets"></a><span data-ttu-id="8fa25-103">Sady schválení</span><span class="sxs-lookup"><span data-stu-id="8fa25-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8fa25-104">Sady schválení seskupují požadavky na schválení společně do menších podmnožin operací.</span><span class="sxs-lookup"><span data-stu-id="8fa25-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="8fa25-105">Toto seskupení umožňuje zpracování schválení v pořadí podle projektu a umožňuje opakování a řazení.</span><span class="sxs-lookup"><span data-stu-id="8fa25-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="8fa25-106">Seskupení zlepšuje spolehlivost a sledovatelnost zpracování schválení pro velké objemy schválení.</span><span class="sxs-lookup"><span data-stu-id="8fa25-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="8fa25-107">Sady schválení označují celkový stav zpracování souvisejících záznamů.</span><span class="sxs-lookup"><span data-stu-id="8fa25-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="8fa25-108">Když je záznam o schválení zpracován pomocí sady schválení, záznam se přesune z **Odesláno** na **Schváleno** a je odpojen od sady schválení.</span><span class="sxs-lookup"><span data-stu-id="8fa25-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="8fa25-109">Pokud záznam selže při odeslání ke schválení, zůstane ve stavu **Odesláno** a sada schválení je označena jako neúspěšná.</span><span class="sxs-lookup"><span data-stu-id="8fa25-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="8fa25-110">Sada schválení zaznamená chybovou zprávu o selhání.</span><span class="sxs-lookup"><span data-stu-id="8fa25-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="8fa25-111">Zpracování schválení a sad schválení</span><span class="sxs-lookup"><span data-stu-id="8fa25-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="8fa25-112">Schválení, která jsou zařazena do fronty ke zpracování, jsou viditelná v pohledu **Zpracování schválení**.</span><span class="sxs-lookup"><span data-stu-id="8fa25-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="8fa25-113">Systém se pokusí zpracovat všechny položky několikrát asynchronně, včetně opakování pokusu o schválení, pokud předchozí pokusy selhaly.</span><span class="sxs-lookup"><span data-stu-id="8fa25-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="8fa25-114">Pole **Životnost sady schválení** zaznamenává počet pokusů zbývajících ke zpracování sady, než bude označena jako neúspěšná.</span><span class="sxs-lookup"><span data-stu-id="8fa25-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="8fa25-115">Neúspěšná schválení a sady schválení</span><span class="sxs-lookup"><span data-stu-id="8fa25-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="8fa25-116">Zobrazení **Neúspěšná schválení** obsahuje seznam všech schválení, která vyžadují zásah uživatele.</span><span class="sxs-lookup"><span data-stu-id="8fa25-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="8fa25-117">Otevřete související protokoly sady schválení a zjistěte příčinu selhání.</span><span class="sxs-lookup"><span data-stu-id="8fa25-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="8fa25-118">Výběr možnosti **Opakovat** zvýší celkový počet sady schválení, přesune sadu schválení zpět do stavu **Zpracovává se** a pokusí se zpracovat zbývající záznamy.</span><span class="sxs-lookup"><span data-stu-id="8fa25-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="8fa25-119">Konfigurace sad schválení</span><span class="sxs-lookup"><span data-stu-id="8fa25-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="8fa25-120">Aktivace funkce sad schválení</span><span class="sxs-lookup"><span data-stu-id="8fa25-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="8fa25-121">Než aktivujete funkci sad schválení, ověřte, zda v současné době nejsou zpracovávána žádná schválení.</span><span class="sxs-lookup"><span data-stu-id="8fa25-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="8fa25-122">Přejděte na stránku **Parametry projektu** stránku a vyberte **Ovládání funkcí** > **Aktivovat moderní schválení**.</span><span class="sxs-lookup"><span data-stu-id="8fa25-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="8fa25-123">Vypnutí funkce sad schválení</span><span class="sxs-lookup"><span data-stu-id="8fa25-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="8fa25-124">Než vypnete funkci sad schválení, ověřte, zda v současné době nejsou zpracovávána žádná schválení.</span><span class="sxs-lookup"><span data-stu-id="8fa25-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="8fa25-125">Přejděte na stránku **Parametry projektu** stránku a vyberte **Ovládání funkcí** > **Deaktivovat moderní schválení**.</span><span class="sxs-lookup"><span data-stu-id="8fa25-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="8fa25-126">Konfigurace asynchronního prahu</span><span class="sxs-lookup"><span data-stu-id="8fa25-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="8fa25-127">Když jsou vytvořeny sady schválení, zpracování se přesune na pozadí, když vybraný počet záznamů ke schválení překročí uvedenou prahovou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8fa25-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="8fa25-128">Použijte pole **Asynchronní prahová hodnota** pro konfiguraci, kdy má být zpracování schválení spuštěno synchronně nebo asynchronně.</span><span class="sxs-lookup"><span data-stu-id="8fa25-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="8fa25-129">Platné hodnoty jsou:</span><span class="sxs-lookup"><span data-stu-id="8fa25-129">Valid values are:</span></span>

  - <span data-ttu-id="8fa25-130">Nula: Všechny požadavky by měly být zpracovávány asynchronně.</span><span class="sxs-lookup"><span data-stu-id="8fa25-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="8fa25-131">Čísla větší než nula: Schválení se zpracovávají asynchronně, pouze pokud zadaný počet schválení překročí tuto hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8fa25-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
