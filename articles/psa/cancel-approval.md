---
title: Zrušit dříve schválené časové a výdajové záznamy
description: Toto téma obsahuje informace o tom, jak zrušit schválený čas projektu a výdajovou transakci.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150570"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="e9dda-103">Zrušit dříve schválené časové nebo výdajové záznamy</span><span class="sxs-lookup"><span data-stu-id="e9dda-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e9dda-104">V nejnovější verzi Dynamics 365 Project Service Automation mohou schvalující zrušit časové nebo výdajové záznamy, které dříve schválili.</span><span class="sxs-lookup"><span data-stu-id="e9dda-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="e9dda-105">Zrušit dříve schválený časový nebo výdajový záznam</span><span class="sxs-lookup"><span data-stu-id="e9dda-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="e9dda-106">Chcete-li zrušit dříve schválený časový nebo výdajový záznam, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="e9dda-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="e9dda-107">Přejděte do **Projekty** \> **Úkoly** \> **Schválení**.</span><span class="sxs-lookup"><span data-stu-id="e9dda-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="e9dda-108">Na stránce se seznamem **Schválení** změňte zobrazení na **Moje předchozí schválení**.</span><span class="sxs-lookup"><span data-stu-id="e9dda-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="e9dda-109">Zobrazí se seznam časových a výdajových záznamů, které jste dříve schválili.</span><span class="sxs-lookup"><span data-stu-id="e9dda-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="e9dda-110">Vyberte jeden nebo více záznamů a pak vyberte **Zrušit schválení**.</span><span class="sxs-lookup"><span data-stu-id="e9dda-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="e9dda-111">Zobrazí se varovná zpráva.</span><span class="sxs-lookup"><span data-stu-id="e9dda-111">You receive a warning message.</span></span>
4. <span data-ttu-id="e9dda-112">Pokud chcete schválení zrušit, vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9dda-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="e9dda-113">Porozumění vlivu zrušení schválení časového nebo výdajového záznamu</span><span class="sxs-lookup"><span data-stu-id="e9dda-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="e9dda-114">Pokud je schválení zrušeno, existuje jak provozní dopad, tak i finanční dopad.</span><span class="sxs-lookup"><span data-stu-id="e9dda-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="e9dda-115">Provozní dopad</span><span class="sxs-lookup"><span data-stu-id="e9dda-115">Operational impact</span></span>

<span data-ttu-id="e9dda-116">Z provozního pohledu se stav záznamu při zrušení schválení obnoví na **Koncept** a schválení se již nezobrazuje v zobrazení **Moje předchozí schválení**.</span><span class="sxs-lookup"><span data-stu-id="e9dda-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="e9dda-117">Zrušené schválení se místo toho zobrazí buď v zobrazení **Časové záznamy ke schválení** nebo v zobrazení **Výdajové záznamy ke schválení**, v závislosti na tom, zda se jednalo o časový záznam nebo výdajový záznam.</span><span class="sxs-lookup"><span data-stu-id="e9dda-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="e9dda-118">Dále se stav souvisejícího časového nebo výdajového záznamu změní na **Odesláno**, takže související záznam je konzistentní se schváleními, která mají stav **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="e9dda-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="e9dda-119">Jako schvalující můžete upravit některá pole schválení, která mají stav **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="e9dda-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="e9dda-120">Tato pole zahrnují **Typ fakturace** a **Fakturovatelné hodiny pro časové záznamy**.</span><span class="sxs-lookup"><span data-stu-id="e9dda-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="e9dda-121">Po provedení změn můžete záznam znovu schválit.</span><span class="sxs-lookup"><span data-stu-id="e9dda-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="e9dda-122">Záznam můžete také zamítnout.</span><span class="sxs-lookup"><span data-stu-id="e9dda-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="e9dda-123">Pokud zamítnete schválení časového záznamu, změní se stav záznamu na **Vráceno**.</span><span class="sxs-lookup"><span data-stu-id="e9dda-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="e9dda-124">Pokud zamítnete schválení výdajového záznamu, změní se stav záznamu na **Zamítnuto**.</span><span class="sxs-lookup"><span data-stu-id="e9dda-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="e9dda-125">Funkčně se oba vrácené a zamítnuté záznamy chovají stejně jako záznam se stavem **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="e9dda-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="e9dda-126">Člen projektového týmu může buď provést požadované změny záznamu, a pak jej znovu odeslat ke schválení, nebo záznam zcela odstranit.</span><span class="sxs-lookup"><span data-stu-id="e9dda-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="e9dda-127">Finanční dopad</span><span class="sxs-lookup"><span data-stu-id="e9dda-127">Financial impact</span></span>

<span data-ttu-id="e9dda-128">Projekt je při zrušení schválení ovlivněn také finančně.</span><span class="sxs-lookup"><span data-stu-id="e9dda-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="e9dda-129">Odpovídající skutečné hodnoty nákladů a prodeje se nejprve aktualizují následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="e9dda-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="e9dda-130">Stav úpravy je nastaven na **Upraveno**.</span><span class="sxs-lookup"><span data-stu-id="e9dda-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="e9dda-131">Stav fakturace je nastaven na **Zrušeno**.</span><span class="sxs-lookup"><span data-stu-id="e9dda-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="e9dda-132">Dále se v tabulce Skutečné hodnoty vytvoří záznamy storna.</span><span class="sxs-lookup"><span data-stu-id="e9dda-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="e9dda-133">Chcete-li vytvořit záznamy storna, systém zkopíruje hodnoty tohoto pole z původních skutečných hodnot.</span><span class="sxs-lookup"><span data-stu-id="e9dda-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="e9dda-134">Jedinými hodnotami, které nejsou kopírovány, jsou hodnoty množství.</span><span class="sxs-lookup"><span data-stu-id="e9dda-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="e9dda-135">Tyto hodnoty jsou naopak stornovány.</span><span class="sxs-lookup"><span data-stu-id="e9dda-135">These values are reversed instead.</span></span> <span data-ttu-id="e9dda-136">Stornované skutečné hodnoty se vytvoří pro skutečné hodnoty **Nákladů** a **Nefakturovaného prodeje**.</span><span class="sxs-lookup"><span data-stu-id="e9dda-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="e9dda-137">Pole **Stav úpravy** je u stornovaných skutečných hodnot nastaveno na **Neupravitelné** a stav fakturace je nastaven na **Zrušeno**.</span><span class="sxs-lookup"><span data-stu-id="e9dda-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="e9dda-138">Po provedení těchto změn bude částka zaznamenaná jako utracená v projektu a nedokončené výnosy v projektu dále odpovídat částkám, které tyto skutečné hodnoty představují.</span><span class="sxs-lookup"><span data-stu-id="e9dda-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
