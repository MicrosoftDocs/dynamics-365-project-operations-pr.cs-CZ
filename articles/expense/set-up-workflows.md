---
title: Nastavení pracovních postupů pro správu výdajů
description: Můžete nastavit proces pracovního postupu, který se používá ke kontrole a schvalování cestovních a výdajových dokladů.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: db1bda71e18369550cd2d38fee1d0ac40e07555d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073807"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="37fbf-103">Nastavení pracovních postupů pro správu výdajů</span><span class="sxs-lookup"><span data-stu-id="37fbf-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="37fbf-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="37fbf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="37fbf-105">Můžete nastavit proces pracovního postupu ke kontrole a schvalování cestovních a výdajových dokladů.</span><span class="sxs-lookup"><span data-stu-id="37fbf-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="37fbf-106">Můžete definovat pracovní postupy pro výkazy výdajů, cestovní žádanky a žádosti o hotovostní zálohy.</span><span class="sxs-lookup"><span data-stu-id="37fbf-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="37fbf-107">Pracovní postup představuje obchodní proces a definuje, jak doklad protéká systémem.</span><span class="sxs-lookup"><span data-stu-id="37fbf-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="37fbf-108">Pracovní postup také označuje, kdo musí dokončit úkol nebo schválit dokument.</span><span class="sxs-lookup"><span data-stu-id="37fbf-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="37fbf-109">Existuje několik výhod používání systému pracovního postupu ve vaší organizaci:</span><span class="sxs-lookup"><span data-stu-id="37fbf-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="37fbf-110">**Konzistentní procesy** : Můžete definovat proces schvalování pro konkrétní doklady, jako jsou nákupní žádanky a výkazy výdajů.</span><span class="sxs-lookup"><span data-stu-id="37fbf-110">**Consistent processes** : You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="37fbf-111">Používání systému pracovního postupu pomáhá zajistit, aby dokumenty byly zpracovávány a schvalovány konzistentním a efektivním způsobem.</span><span class="sxs-lookup"><span data-stu-id="37fbf-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="37fbf-112">**Viditelnost procesu** : Můžete sledovat stav, historii a metriky výkonu konkrétní instance pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="37fbf-112">**Process visibility** : You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="37fbf-113">To vám pomůže určit, zda je třeba provést změny v pracovním postupu, aby se zlepšila účinnost.</span><span class="sxs-lookup"><span data-stu-id="37fbf-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="37fbf-114">**Centralizovaný pracovní seznam** : Uživatelé si mohou prohlížet centralizovaný pracovní seznam a zobrazit úkoly pracovního toku a schválení, která jim byla přidělena.</span><span class="sxs-lookup"><span data-stu-id="37fbf-114">**Centralized work list** : Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="37fbf-115">Typy pracovního postupu</span><span class="sxs-lookup"><span data-stu-id="37fbf-115">Workflow types</span></span>

<span data-ttu-id="37fbf-116">Následující tabulka obsahuje typy pracovních postupů, které můžete vytvářet ve **správě výdajů**.</span><span class="sxs-lookup"><span data-stu-id="37fbf-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="37fbf-117"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="37fbf-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="37fbf-118"><strong>Použít tento typ k</strong></span><span class="sxs-lookup"><span data-stu-id="37fbf-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="37fbf-119"><strong>Automatické schválení výkazů výdajů</strong></span><span class="sxs-lookup"><span data-stu-id="37fbf-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="37fbf-120">Vytvořte pracovní postupy schválení pro výkazy výdajů.</span><span class="sxs-lookup"><span data-stu-id="37fbf-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="37fbf-121"><strong>Automatické zaúčtování výkazů výdajů</strong></span><span class="sxs-lookup"><span data-stu-id="37fbf-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="37fbf-122">Vytvořte pracovní postupy automatického zaúčtování pro výkazy výdajů.</span><span class="sxs-lookup"><span data-stu-id="37fbf-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="37fbf-123"><strong>Položka řádku výdajů</strong></span><span class="sxs-lookup"><span data-stu-id="37fbf-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="37fbf-124">Vytvořte pracovní postupy schválení pro položky řádků na výkazech výdajů.</span><span class="sxs-lookup"><span data-stu-id="37fbf-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="37fbf-125"><strong>Automatické zaúčtování položek řádku výdajů</strong></span><span class="sxs-lookup"><span data-stu-id="37fbf-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="37fbf-126">Vytvořte pracovní postupy automatického zaúčtování pro položky řádků na výkazech výdajů.</span><span class="sxs-lookup"><span data-stu-id="37fbf-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="37fbf-127"><strong>Cestovní žádanka</strong></span><span class="sxs-lookup"><span data-stu-id="37fbf-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="37fbf-128">Vytvořte pracovní postupy schválení pro cestovní žádanky.</span><span class="sxs-lookup"><span data-stu-id="37fbf-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="37fbf-129"><strong>Požadavek na hotovostní zálohu</strong></span><span class="sxs-lookup"><span data-stu-id="37fbf-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="37fbf-130">Vytvořte pracovní postupy schvalování požadavků na hotovostní zálohu.</span><span class="sxs-lookup"><span data-stu-id="37fbf-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="37fbf-131"><strong>Vratka DPH</strong></span><span class="sxs-lookup"><span data-stu-id="37fbf-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="37fbf-132">Vytvořte pracovní postupy schválení pro vratku daně z přidané hodnoty (DPH).</span><span class="sxs-lookup"><span data-stu-id="37fbf-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
