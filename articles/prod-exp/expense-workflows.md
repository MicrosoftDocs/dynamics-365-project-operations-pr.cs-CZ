---
title: Nastavení pracovních postupů správy výdajů
description: Můžete nastavit proces pracovního postupu ke kontrole a schvalování cestovních a výdajových dokladů.
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
ms.openlocfilehash: 36ab1edc4769013684fa9248e6c5eac025637bbd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271615"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="7b086-103">Nastavení pracovních postupů správy výdajů</span><span class="sxs-lookup"><span data-stu-id="7b086-103">Set up Expense management workflows</span></span>

<span data-ttu-id="7b086-104">Můžete nastavit proces pracovního postupu, který se používá ke kontrole a schvalování cestovních a výdajových dokladů.</span><span class="sxs-lookup"><span data-stu-id="7b086-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="7b086-105">Mezi dokumenty, pro které je možné definovat pracovní postupy, patří sestavy výdajů, cestovní žádanky a žádosti o hotovostní zálohy.</span><span class="sxs-lookup"><span data-stu-id="7b086-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="7b086-106">Pracovní postup představuje obchodní proces.</span><span class="sxs-lookup"><span data-stu-id="7b086-106">A workflow represents a business process.</span></span> <span data-ttu-id="7b086-107">Definuje, jak dokument prochází systémem, a určuje, kdo musí provést úkol nebo schválit dokument.</span><span class="sxs-lookup"><span data-stu-id="7b086-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="7b086-108">Existuje několik výhod používání systému pracovního postupu ve vaší organizaci:</span><span class="sxs-lookup"><span data-stu-id="7b086-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="7b086-109">**Konzistentní procesy** – Můžete definovat proces schvalování pro konkrétní doklady, jako jsou nákupní žádanky a sestavy výdajů.</span><span class="sxs-lookup"><span data-stu-id="7b086-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="7b086-110">Používání systému pracovního postupu pomáhá zajistit, aby dokumenty byly zpracovávány a schvalovány konzistentním a efektivním způsobem.</span><span class="sxs-lookup"><span data-stu-id="7b086-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="7b086-111">Viditelnost procesu – Můžete sledovat stav, historii a metriky výkonu konkrétní instance pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="7b086-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="7b086-112">To vám pomůže určit, zda je třeba provést změny v pracovním postupu, aby se zlepšila účinnost.</span><span class="sxs-lookup"><span data-stu-id="7b086-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="7b086-113">Centralizovaný pracovní seznam – Uživatelé si mohou prohlížet centralizovaný pracovní seznam a zobrazit úkoly pracovního toku a schválení, která jim byla přidělena.</span><span class="sxs-lookup"><span data-stu-id="7b086-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="7b086-114">**Typy pracovních postupů, které můžete vytvořit**</span><span class="sxs-lookup"><span data-stu-id="7b086-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="7b086-115">Následující tabulka obsahuje typy pracovních postupů, které můžete vytvářet ve **Výdajích**.</span><span class="sxs-lookup"><span data-stu-id="7b086-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="7b086-116"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="7b086-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="7b086-117"><strong>Použít tento typ k</strong></span><span class="sxs-lookup"><span data-stu-id="7b086-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="7b086-118"><strong>Sestava výdajů</strong></span><span class="sxs-lookup"><span data-stu-id="7b086-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="7b086-119">Vytvořte pracovní postupy schválení pro výkazy výdajů.</span><span class="sxs-lookup"><span data-stu-id="7b086-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="7b086-120"><strong>Automatické zaúčtování výkazů výdajů</strong></span><span class="sxs-lookup"><span data-stu-id="7b086-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="7b086-121">Vytvořte pracovní postupy automatického zaúčtování pro výkazy výdajů.</span><span class="sxs-lookup"><span data-stu-id="7b086-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="7b086-122"><strong>Položka řádku výdajů</strong></span><span class="sxs-lookup"><span data-stu-id="7b086-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="7b086-123">Vytvořte pracovní postupy schválení pro položky řádků na výkazech výdajů.</span><span class="sxs-lookup"><span data-stu-id="7b086-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="7b086-124"><strong>Automatické zaúčtování položek řádku výdajů</strong></span><span class="sxs-lookup"><span data-stu-id="7b086-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="7b086-125">Vytvořte pracovní postupy automatického zaúčtování pro položky řádků na výkazech výdajů.</span><span class="sxs-lookup"><span data-stu-id="7b086-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="7b086-126"><strong>Cestovní žádanka</strong></span><span class="sxs-lookup"><span data-stu-id="7b086-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="7b086-127">Vytvořte pracovní postupy schválení pro cestovní žádanky.</span><span class="sxs-lookup"><span data-stu-id="7b086-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="7b086-128"><strong>Požadavek na hotovostní zálohu</strong></span><span class="sxs-lookup"><span data-stu-id="7b086-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="7b086-129">Vytvořte pracovní postupy schvalování požadavků na hotovostní zálohu.</span><span class="sxs-lookup"><span data-stu-id="7b086-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="7b086-130"><strong>Vratka DPH</strong></span><span class="sxs-lookup"><span data-stu-id="7b086-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="7b086-131">Vytvořte pracovní postupy schválení pro vratku daně z přidané hodnoty (DPH).</span><span class="sxs-lookup"><span data-stu-id="7b086-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]