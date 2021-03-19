---
title: Pracovní postup správy výdajů
description: Tento téma vysvětluje, jak můžete použít systém pracovního postupu v Microsoft Dynamics 365 Finance k nastavení procesu kontroly pro sestavy výdajů ve správě výdajů.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271660"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="e026a-103">Pracovní postup správy výdajů</span><span class="sxs-lookup"><span data-stu-id="e026a-103">Expense management workflow</span></span>

<span data-ttu-id="e026a-104">Systém pracovního postupu v Microsoft můžete použít k nastavení procesu kontroly pro sestavy výdajů ve správě výdajů.</span><span class="sxs-lookup"><span data-stu-id="e026a-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="e026a-105">Můžete nastavit pracovní postup, který k určení toho, kdo schvaluje sestavy výdajů, používá následující kritéria:</span><span class="sxs-lookup"><span data-stu-id="e026a-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="e026a-106">Hierarchie podřízenosti zaměstnanců a předdefinované limity schválení</span><span class="sxs-lookup"><span data-stu-id="e026a-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="e026a-107">Víceúrovňové schválení, které podporuje prozatímní schvalovatele a konečného schvalovatele</span><span class="sxs-lookup"><span data-stu-id="e026a-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="e026a-108">Finanční dimenze a odpovědnost za projekt</span><span class="sxs-lookup"><span data-stu-id="e026a-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="e026a-109">Přiřazení konkrétním uživatelům nebo skupinám uživatelů</span><span class="sxs-lookup"><span data-stu-id="e026a-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="e026a-110">Je možné vytvořit schválení pracovního postupu pro sestavy výdajů, cestovní požadavky, zálohy v hotovosti a vymáhání daně z přidané hodnoty (DPH).</span><span class="sxs-lookup"><span data-stu-id="e026a-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="e026a-111">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="e026a-111">**Example**</span></span>

<span data-ttu-id="e026a-112">Následující proces je příkladem pracovního postupu správy výdajů pro sestavu výdajů.</span><span class="sxs-lookup"><span data-stu-id="e026a-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="e026a-113">Zaměstnanec vytvoří a uloží sestavu výdajů.</span><span class="sxs-lookup"><span data-stu-id="e026a-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="e026a-114">Zaměstnance odešle sestavu výdajů ke schválení.</span><span class="sxs-lookup"><span data-stu-id="e026a-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="e026a-115">Schvalovatel je identifikován na základě pravidel, která byla definována při nastavení pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="e026a-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="e026a-116">Schvalovatel obdrží oznámení, že sestava výdajů je připraven ke schválení.</span><span class="sxs-lookup"><span data-stu-id="e026a-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="e026a-117">Schvalovatel zkontroluje sestava výdajů a ověří, zda jsou splněny následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e026a-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="e026a-118">Výdaje neporušují žádné zásady výdajů.</span><span class="sxs-lookup"><span data-stu-id="e026a-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="e026a-119">Pokud výdaj porušuje zásady, schvalovatel ověří, zda sestava výdajů obsahuje platné obchodní odůvodnění.</span><span class="sxs-lookup"><span data-stu-id="e026a-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="e026a-120">Elektronické účtenky jsou připojeny k sestavě výdajů.</span><span class="sxs-lookup"><span data-stu-id="e026a-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="e026a-121">Schvalovatel sestavu výdajů schválí.</span><span class="sxs-lookup"><span data-stu-id="e026a-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="e026a-122">Sestava výdajů je přiřazena koordinátorovi závazků k zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="e026a-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="e026a-123">Dojde k jednomu z následujících kroků v závislosti na tom, zda je nakonfigurováno automatické zaúčtování:</span><span class="sxs-lookup"><span data-stu-id="e026a-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="e026a-124">Pokud je nakonfigurováno automatické zaúčtování, je zpracována sestava výdajů k platbě a je aktualizován stav sestav výdajů.</span><span class="sxs-lookup"><span data-stu-id="e026a-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="e026a-125">Pokud automatické účtování není nakonfigurováno, koordinátor závazků ověří, zda byly odeslány všechny původní příjmy a zda jsou příjmy v souladu s výdaji v sestavě výdajů.</span><span class="sxs-lookup"><span data-stu-id="e026a-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="e026a-126">Všechny daňové zásady, které jsou zadány v sestavě výdajů, musí být také ověřeny jako správné.</span><span class="sxs-lookup"><span data-stu-id="e026a-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="e026a-127">Po ověření těchto požadavků se sestava výdajů zaúčtuje.</span><span class="sxs-lookup"><span data-stu-id="e026a-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="e026a-128">Po zaúčtování sestavy výdajů je platba pro sestavu výdajů autorizována a zaměstnanci jsou proplaceny peníze.</span><span class="sxs-lookup"><span data-stu-id="e026a-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]