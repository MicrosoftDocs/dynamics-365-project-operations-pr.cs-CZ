---
title: Odvolání schválených časových nebo výdajových záznamů
description: Toto téma obsahuje informace o tom, jak odvolat dříve schválený čas nebo výdajovou transakci.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1a199985099745b2e62b844ef748ea2031054458
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283450"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="d3312-103">Odvolání schválených časových nebo výdajových záznamů</span><span class="sxs-lookup"><span data-stu-id="d3312-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d3312-104">Člen projektového týmu nebo jiná osoba, která odesílá časový nebo výdajový záznam, může tento časový nebo výdajový záznam po schválení odvolat.</span><span class="sxs-lookup"><span data-stu-id="d3312-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="d3312-105">Proces odvolání časového nebo výdajového záznamu má dva kroky:</span><span class="sxs-lookup"><span data-stu-id="d3312-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="d3312-106">Odesílatel požádá o odvolání.</span><span class="sxs-lookup"><span data-stu-id="d3312-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="d3312-107">Schvalovatel schválí odvolání.</span><span class="sxs-lookup"><span data-stu-id="d3312-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="d3312-108">Žádost o odvolání</span><span class="sxs-lookup"><span data-stu-id="d3312-108">Request a recall</span></span>

<span data-ttu-id="d3312-109">Chcete-li odvolat dříve schválený časový nebo výdajový záznam, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="d3312-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="d3312-110">V případě časových záznamů přejděte do **Projekty** \> **Úkoly** \> **Časový záznam**.</span><span class="sxs-lookup"><span data-stu-id="d3312-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="d3312-111">–nebo–</span><span class="sxs-lookup"><span data-stu-id="d3312-111">–or–</span></span>

    <span data-ttu-id="d3312-112">V případě výdajových záznamů přejděte do **Projekty** \> **Úkoly** \> **Výdaje**.</span><span class="sxs-lookup"><span data-stu-id="d3312-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="d3312-113">U časových záznamů vyberte všechny časové záznamy pro konkrétní kombinaci projektu a úkolu.</span><span class="sxs-lookup"><span data-stu-id="d3312-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="d3312-114">Alternativně vyberte v mřížce jednotlivé buňky pro čas u určitého data pro konkrétní projekt.</span><span class="sxs-lookup"><span data-stu-id="d3312-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="d3312-115">–nebo–</span><span class="sxs-lookup"><span data-stu-id="d3312-115">–or–</span></span>

    <span data-ttu-id="d3312-116">U výdajových záznamů vyberte řádek výdajového záznamu, který chcete odvolat.</span><span class="sxs-lookup"><span data-stu-id="d3312-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="d3312-117">Vyberte **Odvolat**.</span><span class="sxs-lookup"><span data-stu-id="d3312-117">Select **Recall**.</span></span> <span data-ttu-id="d3312-118">Zobrazí se dialogové okno s potvrzením</span><span class="sxs-lookup"><span data-stu-id="d3312-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="d3312-119">Pokud byly vybrané časové a výdajové záznamy již schváleny, budete vyzváni k zadání důvodu odvolání.</span><span class="sxs-lookup"><span data-stu-id="d3312-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="d3312-120">Zadejte důvod odvolání a výběrem **OK** operaci potvrďte.</span><span class="sxs-lookup"><span data-stu-id="d3312-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="d3312-121">Systém zašle osobě, která položky schválila, žádost o schválení odvolání.</span><span class="sxs-lookup"><span data-stu-id="d3312-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="d3312-122">Přestože lze schválené časové a výdajové záznamy odvolat, pokud již byl zákazníkovi schválený časový nebo výdajový záznam fakturován, nelze žádost o odvolání vytvořit.</span><span class="sxs-lookup"><span data-stu-id="d3312-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="d3312-123">Uživatel, který se pokusí vytvořit žádost o odvolání, obdrží zprávu, že časový nebo výdajový záznam nelze odvolat, protože už byl fakturován.</span><span class="sxs-lookup"><span data-stu-id="d3312-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="d3312-124">Schválení nebo zamítnutí žádosti o odvolání</span><span class="sxs-lookup"><span data-stu-id="d3312-124">Approve or reject a recall request</span></span>

<span data-ttu-id="d3312-125">Chcete-li žádost o odvolání schválit nebo zamítnout, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="d3312-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="d3312-126">Přejděte do **Projekty** \> **Úkoly** \> **Schválení**.</span><span class="sxs-lookup"><span data-stu-id="d3312-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="d3312-127">Na stránce se seznamem **Schválení** změňte zobrazení na **Odvolat žádosti o schválení**.</span><span class="sxs-lookup"><span data-stu-id="d3312-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="d3312-128">Zobrazí se seznam odeslaných žádostí o odvolání.</span><span class="sxs-lookup"><span data-stu-id="d3312-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="d3312-129">Vyberte jeden nebo více záznamů a pak vyberte buď **Schválit** nebo **Zamítnout**.</span><span class="sxs-lookup"><span data-stu-id="d3312-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="d3312-130">Pokud jste zvolili **Schválit**, obdržíte varovnou zprávu s vysvětlením dopadu schválení.</span><span class="sxs-lookup"><span data-stu-id="d3312-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="d3312-131">Výběrem **OK** operaci potvrďte.</span><span class="sxs-lookup"><span data-stu-id="d3312-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="d3312-132">Žádost o odvolání je schválena.</span><span class="sxs-lookup"><span data-stu-id="d3312-132">The recall request is approved.</span></span>

    <span data-ttu-id="d3312-133">–nebo–</span><span class="sxs-lookup"><span data-stu-id="d3312-133">–or–</span></span>

    <span data-ttu-id="d3312-134">Pokud jste vybrali **Zamítnout**, je žádost o odvolání zamítnuta.</span><span class="sxs-lookup"><span data-stu-id="d3312-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="d3312-135">Stejně jako při žádosti o odvolání systém při schválení odvolání u časových nebo výdajových záznamů kontroluje jakoukoli fakturační činnost.</span><span class="sxs-lookup"><span data-stu-id="d3312-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="d3312-136">Pokud byl záznam již fakturován nebo pokud je na konceptu faktury, zobrazí se schvalovateli chybová zpráva, že odvolání časového nebo výdajového záznamu nelze schválit, protože již byl fakturován.</span><span class="sxs-lookup"><span data-stu-id="d3312-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="d3312-137">Dopad žádosti o odvolání</span><span class="sxs-lookup"><span data-stu-id="d3312-137">Impact of a recall request</span></span>

<span data-ttu-id="d3312-138">Pokud je schválení odvoláno, existuje jak provozní dopad, tak i finanční dopad.</span><span class="sxs-lookup"><span data-stu-id="d3312-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="d3312-139">Provozní dopad</span><span class="sxs-lookup"><span data-stu-id="d3312-139">Operational impact</span></span>

<span data-ttu-id="d3312-140">Je-li žádost o odvolání schválena, označí se záznam o schválení jako **Zamítnutý**.</span><span class="sxs-lookup"><span data-stu-id="d3312-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="d3312-141">Stav záznamu se změní buď na **Vráceno**, nebo **Zamítnuto**, v závislosti na tom, zda se jedná o časový nebo výdajový záznam.</span><span class="sxs-lookup"><span data-stu-id="d3312-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="d3312-142">Člen projektového týmu může záznamy zobrazit, upravit a poté je znovu odeslat nebo zcela odstranit.</span><span class="sxs-lookup"><span data-stu-id="d3312-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="d3312-143">Pokud je žádost o odvolání zamítnuta, stav záznamu zůstane **Schváleno** a člen týmu nebo schvalovatel projektu ho nemůže upravit.</span><span class="sxs-lookup"><span data-stu-id="d3312-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="d3312-144">Finanční dopad</span><span class="sxs-lookup"><span data-stu-id="d3312-144">Financial impact</span></span>

<span data-ttu-id="d3312-145">Pokud je žádost o odvolání schválena, tak se skutečné hodnoty nákladů a prodeje nejprve aktualizují následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="d3312-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="d3312-146">Pole **Stav úpravy** se aktualizuje na **Upraveno**.</span><span class="sxs-lookup"><span data-stu-id="d3312-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="d3312-147">Pole **Stav fakturace** se aktualizuje na **Zrušeno**.</span><span class="sxs-lookup"><span data-stu-id="d3312-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="d3312-148">Dále se v tabulce Skutečné hodnoty vytvoří záznamy storna.</span><span class="sxs-lookup"><span data-stu-id="d3312-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="d3312-149">Chcete-li vytvořit záznamy storna, systém zkopíruje hodnoty tohoto pole z původních skutečných hodnot.</span><span class="sxs-lookup"><span data-stu-id="d3312-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="d3312-150">Jedinými hodnotami, které nejsou kopírovány, jsou hodnoty množství.</span><span class="sxs-lookup"><span data-stu-id="d3312-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="d3312-151">Tyto hodnoty jsou naopak stornovány.</span><span class="sxs-lookup"><span data-stu-id="d3312-151">These values are reversed instead.</span></span> <span data-ttu-id="d3312-152">Stornované skutečné hodnoty se vytvoří pro skutečné hodnoty **Nákladů** a **Nefakturovaného prodeje**.</span><span class="sxs-lookup"><span data-stu-id="d3312-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="d3312-153">Pole **Stav úpravy** je u stornovaných skutečných hodnot nastaveno na **Neupravitelné** a pole **Stav fakturace** je nastaveno na **Zrušeno**.</span><span class="sxs-lookup"><span data-stu-id="d3312-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="d3312-154">Kvůli těmto změnám už nebudou zaznamenané výdaje a nedokončené výnosy v projektu dále odpovídat částkám, které tyto skutečné hodnoty představují.</span><span class="sxs-lookup"><span data-stu-id="d3312-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="d3312-155">Je-li žádost o odvolání zamítnuta, tak to na projekt nemá žádný finanční dopad.</span><span class="sxs-lookup"><span data-stu-id="d3312-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="d3312-156">Změny časových záznamů</span><span class="sxs-lookup"><span data-stu-id="d3312-156">Changes to time entry records</span></span>

<span data-ttu-id="d3312-157">Následující obrázek zobrazuje změny, ke kterým dojde u schválených časových záznamů při jejich odvolání.</span><span class="sxs-lookup"><span data-stu-id="d3312-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Stavové přechody časových záznamů](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="d3312-159">Změny výdajových záznamů</span><span class="sxs-lookup"><span data-stu-id="d3312-159">Changes to expense entry records</span></span>

<span data-ttu-id="d3312-160">Následující obrázek zobrazuje změny, ke kterým dojde u schválených výdajových záznamů při jejich odvolání.</span><span class="sxs-lookup"><span data-stu-id="d3312-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Stavové přechody výdajových záznamů](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]