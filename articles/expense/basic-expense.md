---
title: Položka výdajů (omezené)
description: Tento téma poskytuje informace o tom, jak pracovat se zadáním výdajů v omezeném nasazení.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073664"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="8f11e-103">Položka výdajů (omezené)</span><span class="sxs-lookup"><span data-stu-id="8f11e-103">Expense entry (lite)</span></span>

<span data-ttu-id="8f11e-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="8f11e-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8f11e-105">Základní nebo omezená správa nákladů je schopnost zaznamenávat jednoduché výdaje.</span><span class="sxs-lookup"><span data-stu-id="8f11e-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="8f11e-106">Můžete zaznamenat výdaje proti projektu a poté je schvalovatel projektu zkontroluje a schválí.</span><span class="sxs-lookup"><span data-stu-id="8f11e-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="8f11e-107">Další informace o možnostech výdajů v Dynamics 365 Project Operations najdete v [Přehledu výdajů](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8f11e-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="8f11e-108">Zachyťte základní výdaje</span><span class="sxs-lookup"><span data-stu-id="8f11e-108">Capture a basic expense</span></span>

<span data-ttu-id="8f11e-109">Můžete zachytit své výdaje, abyste je mohli předat schvalovateli.</span><span class="sxs-lookup"><span data-stu-id="8f11e-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="8f11e-110">přejděte na **Výdaje** a vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="8f11e-110">Go to **Expenses** , and select **New**.</span></span>
2. <span data-ttu-id="8f11e-111">Na stránce **Nový výdaj** zadejte požadované informace o výdajích a poté vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8f11e-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="8f11e-112">Odešlete základní výdaje</span><span class="sxs-lookup"><span data-stu-id="8f11e-112">Submit a basic expense</span></span>

<span data-ttu-id="8f11e-113">Jakmile dokončíte získávání všech svých výdajů a jste připraveni je schválit, musíte je odeslat.</span><span class="sxs-lookup"><span data-stu-id="8f11e-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="8f11e-114">přejděte na **Výdaje** a vyberte výdaj.</span><span class="sxs-lookup"><span data-stu-id="8f11e-114">Go to **Expenses** , and select an expense.</span></span> <span data-ttu-id="8f11e-115">Nebo vyberte všechny výdaje pomocí zaškrtávacího políčka v záhlaví.</span><span class="sxs-lookup"><span data-stu-id="8f11e-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="8f11e-116">Vyberte položku **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="8f11e-116">Select **Submit**.</span></span> <span data-ttu-id="8f11e-117">Systém zpracuje vybrané položky a poté vytvoří žádosti o schválení výdajů.</span><span class="sxs-lookup"><span data-stu-id="8f11e-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="8f11e-118">Odvolání základního výdaje</span><span class="sxs-lookup"><span data-stu-id="8f11e-118">Recall a basic expense</span></span>

<span data-ttu-id="8f11e-119">Pokud omylem zadáte výdaj, můžete jej odvolat.</span><span class="sxs-lookup"><span data-stu-id="8f11e-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="8f11e-120">Čas potřebný k vyvolání položky výdajů závisí na fázi jejího schválení.</span><span class="sxs-lookup"><span data-stu-id="8f11e-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="8f11e-121">Pokud schvalovatel dosud neschválil záznam, může k odvolání dojít okamžitě.</span><span class="sxs-lookup"><span data-stu-id="8f11e-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="8f11e-122">Pokud však již byl záznam schválen, je schvalovatel požádán o schválení odvolání a zrušení transakcí.</span><span class="sxs-lookup"><span data-stu-id="8f11e-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="8f11e-123">Přejděte na **Výdaje** a poté v seznamu výdajů vyberte výdaj, který chcete odvolat.</span><span class="sxs-lookup"><span data-stu-id="8f11e-123">Go to **Expenses** , and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="8f11e-124">Vyberte **Odvolat**.</span><span class="sxs-lookup"><span data-stu-id="8f11e-124">Select **Recall**.</span></span> <span data-ttu-id="8f11e-125">Pokud položka výdajů ještě nebyla schválena, systém ji okamžitě vyvolá.</span><span class="sxs-lookup"><span data-stu-id="8f11e-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="8f11e-126">Pokud položka výdajů již byla schválena, je vytvořen požadavek na odvolání, který informuje schvalovatele, že chcete výdaj zrušit.</span><span class="sxs-lookup"><span data-stu-id="8f11e-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="8f11e-127">Schvalovatel poté potvrdí, že lze provést zrušení, a záznam bude vrácen.</span><span class="sxs-lookup"><span data-stu-id="8f11e-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="8f11e-128">Odstranit základní výdaje</span><span class="sxs-lookup"><span data-stu-id="8f11e-128">Delete a basic expense</span></span>

<span data-ttu-id="8f11e-129">Výdaje, které dosud nebyly odeslány, lze smazat.</span><span class="sxs-lookup"><span data-stu-id="8f11e-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="8f11e-130">Chcete-li odstranit již odeslaný výdaj, musíte jej nejprve odvolat.</span><span class="sxs-lookup"><span data-stu-id="8f11e-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f11e-131">Viz také</span><span class="sxs-lookup"><span data-stu-id="8f11e-131">See also</span></span>

- [<span data-ttu-id="8f11e-132">Přehled schválení</span><span class="sxs-lookup"><span data-stu-id="8f11e-132">Approvals overview</span></span>](../approvals/approvals-overview.md)