---
title: Více schvalovatelů na sestavě výdajů
description: Toto téma poskytuje informace o výkazech výdajů, které vyžadují schválení více osobami.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073936"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="5e836-103">Více schvalovatelů na sestavě výdajů</span><span class="sxs-lookup"><span data-stu-id="5e836-103">Multiple approvers on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e836-104">V závislosti na zásadách schvalování výdajů vaší organizace bude muset schválit sestavu výdajů odeslanou zaměstnancem více než jedna osoba.</span><span class="sxs-lookup"><span data-stu-id="5e836-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="5e836-105">Když nastavíte proces pracovního postupu pro schválení výkazu výdajů, můžete přidat prvky pracovního postupu, které zahrnují úkoly nebo kroky pro jednoho nebo více schvalovatelů výkazu výdajů.</span><span class="sxs-lookup"><span data-stu-id="5e836-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="5e836-106">Můžete například požadovat, aby všechny výkazy výdajů byly schváleny nejprve manažerem zaměstnance, který výdaj odeslal, a poté koordinátorem závazků.</span><span class="sxs-lookup"><span data-stu-id="5e836-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="5e836-107">Pokud se rozhodnete vyžadovat více schvalovatelů výkazů výdajů, můžete přidat prvky pracovního toku některým z následujících způsobů:</span><span class="sxs-lookup"><span data-stu-id="5e836-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="5e836-108">Přidejte jeden prvek schvalování, který má jeden krok.</span><span class="sxs-lookup"><span data-stu-id="5e836-108">Add one approval element that has one step.</span></span> <span data-ttu-id="5e836-109">Krok může například vyžadovat, aby byl výkaz výdajů přiřazen skupině uživatelů a aby byl schválen 50 procenty členů skupiny uživatelů.</span><span class="sxs-lookup"><span data-stu-id="5e836-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="5e836-110">Přidejte jeden prvek schvalování, který má více kroků.</span><span class="sxs-lookup"><span data-stu-id="5e836-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="5e836-111">Například prvek schvalování může mít následující kroky:</span><span class="sxs-lookup"><span data-stu-id="5e836-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="5e836-112">Manažer zaměstnance, který odeslal výkaz výdajů, ho schválí.</span><span class="sxs-lookup"><span data-stu-id="5e836-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="5e836-113">Úředník závazků ověří účtenky a položky výkazu výdajů.</span><span class="sxs-lookup"><span data-stu-id="5e836-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="5e836-114">Vlastník rozpočtu schválí výkaz výdajů.</span><span class="sxs-lookup"><span data-stu-id="5e836-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="5e836-115">Přidejte několik prvků schvalování, z nichž každý má jeden krok.</span><span class="sxs-lookup"><span data-stu-id="5e836-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="5e836-116">Můžete například přidat samostatný prvek schválení pro každý z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="5e836-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="5e836-117">Manažer zaměstnance schválí výkaz výdajů.</span><span class="sxs-lookup"><span data-stu-id="5e836-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="5e836-118">Vlastník rozpočtu schválí výkaz výdajů.</span><span class="sxs-lookup"><span data-stu-id="5e836-118">The budget owner approves the expense report.</span></span>
