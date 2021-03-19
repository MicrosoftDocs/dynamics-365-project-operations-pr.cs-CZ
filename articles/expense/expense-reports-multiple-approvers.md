---
title: Vyúčtování výdajů a více schvalovatelů
description: Toto téma poskytuje informace o výkazech výdajů, které vyžadují schválení více než jednou osobou.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9b9826c89e9deb870adb053f82bd049906f56052
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276520"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="0650c-103">Vyúčtování výdajů a více schvalovatelů</span><span class="sxs-lookup"><span data-stu-id="0650c-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="0650c-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="0650c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0650c-105">V závislosti na zásadách schvalování výdajů vaší organizace bude muset schválit odeslaný výkaz více než jedna osoba.</span><span class="sxs-lookup"><span data-stu-id="0650c-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="0650c-106">Když nastavíte proces pracovního postupu pro schválení výkazu výdajů, můžete přidat prvky pracovního postupu, které zahrnují úkoly nebo kroky pro jednoho nebo více schvalovatelů výkazu výdajů.</span><span class="sxs-lookup"><span data-stu-id="0650c-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="0650c-107">Můžete například požadovat, aby všechny výkazy výdajů byly schváleny dvěma samostatnými osobami, manažerem zaměstnance, který výdaj odeslal, a koordinátorem závazků.</span><span class="sxs-lookup"><span data-stu-id="0650c-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="0650c-108">Pokud se rozhodnete vyžadovat více schvalovatelů výkazů výdajů, můžete přidat prvky pracovního toku některým z následujících způsobů:</span><span class="sxs-lookup"><span data-stu-id="0650c-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="0650c-109">Přidejte jeden prvek schvalování, který má jeden krok.</span><span class="sxs-lookup"><span data-stu-id="0650c-109">Add one approval element that has one step.</span></span> <span data-ttu-id="0650c-110">Krok může například vyžadovat, aby byl výkaz výdajů přiřazen skupině uživatelů a aby byl schválen 50 procenty členů skupiny uživatelů.</span><span class="sxs-lookup"><span data-stu-id="0650c-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="0650c-111">Přidejte jeden prvek schvalování, který má více kroků.</span><span class="sxs-lookup"><span data-stu-id="0650c-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="0650c-112">Například prvek schvalování může mít následující kroky:</span><span class="sxs-lookup"><span data-stu-id="0650c-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="0650c-113">Manažer zaměstnance, který odeslal výkaz výdajů, ho schválí.</span><span class="sxs-lookup"><span data-stu-id="0650c-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="0650c-114">Úředník závazků ověří účtenky a položky výkazu výdajů.</span><span class="sxs-lookup"><span data-stu-id="0650c-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="0650c-115">Vlastník rozpočtu schválí výkaz výdajů.</span><span class="sxs-lookup"><span data-stu-id="0650c-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="0650c-116">Přidejte několik prvků schvalování, z nichž každý má jeden krok.</span><span class="sxs-lookup"><span data-stu-id="0650c-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="0650c-117">Můžete například přidat samostatný prvek schválení pro každý z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="0650c-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="0650c-118">Manažer zaměstnance schválí výkaz výdajů.</span><span class="sxs-lookup"><span data-stu-id="0650c-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="0650c-119">Vlastník rozpočtu schválí výkaz výdajů.</span><span class="sxs-lookup"><span data-stu-id="0650c-119">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]