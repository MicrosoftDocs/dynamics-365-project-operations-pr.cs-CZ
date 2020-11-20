---
title: Výchozí hodnoty finanční dimenze
description: Tohle téma poskytuje informace, jak nastavit výchozí finanční dimenze.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131875"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="332db-103">Výchozí hodnoty finanční dimenze</span><span class="sxs-lookup"><span data-stu-id="332db-103">Financial dimension defaults</span></span>

<span data-ttu-id="332db-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="332db-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="332db-105">Dynamics 365 Project Operations používá rámec [Finanční dimenze](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) v Dynamics 365 Finance, aby bylo možné poskytnout další informace o transakcích dílčí hlavní knihy a hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="332db-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="332db-106">Výchozí finanční dimenze lze nastavit pro zákazníka, zdroj financování projektu, milník, řádek smlouvy projektu nebo projekt.</span><span class="sxs-lookup"><span data-stu-id="332db-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="332db-107">Definování výchozích finančních dimenzí pro zákazníka</span><span class="sxs-lookup"><span data-stu-id="332db-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="332db-108">Výchozí dimenze zákazníka jsou specifikovány v řešení Finance.</span><span class="sxs-lookup"><span data-stu-id="332db-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="332db-109">Chcete-li nastavit výchozí hodnoty dimenze, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="332db-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="332db-110">Přejděte na **Pohledávky** > **Zákazníci** > **Všichni zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="332db-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="332db-111">Na kartě **Zákazníci** na kartě **Finanční dimenze** nastavte hodnoty finanční dimenze pro konkrétního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="332db-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="332db-112">Definování výchozích finančních dimenzí pro projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="332db-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="332db-113">Projektové smlouvy jsou vytvářeny a spravovány v Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="332db-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="332db-114">Atributy účetnictví pro projektové smlouvy jsou nastaveny v modulu **Řízení projektů a účetnictví** ve Finance.</span><span class="sxs-lookup"><span data-stu-id="332db-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="332db-115">Nastavení finančních dimenzí pro zdroj financování projektu</span><span class="sxs-lookup"><span data-stu-id="332db-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="332db-116">Přejděte do nabídky **Řízení projektů a účetnictví** > **Projekty** > **Projektové smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="332db-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="332db-117">Vyberte záznam, který chcete aktualizovat, a na kartě **Projektová smlouva** vyberte **Zobrazit výchozí účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="332db-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="332db-118">Rozbalte **Související informace** a vyberte kartu **Zdroje financování**.</span><span class="sxs-lookup"><span data-stu-id="332db-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="332db-119">Nastavte výchozí hodnoty finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="332db-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="332db-120">Všimněte si, že finanční dimenze vychází z účtu zákazníka.</span><span class="sxs-lookup"><span data-stu-id="332db-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="332db-121">Nastavení finančních dimenzí pro řádek projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="332db-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="332db-122">Přejděte do nabídky **Řízení projektů a účetnictví** > **Projekty** > **Projektové smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="332db-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="332db-123">Vyberte záznam, který chcete aktualizovat, a na kartě **Projektová smlouva** vyberte **Zobrazit výchozí účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="332db-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="332db-124">Rozbalte **Související informace** a vyberte kartu **Řádky smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="332db-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="332db-125">Nastavte výchozí hodnoty finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="332db-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="332db-126">Výchozí nastavení finanční dimenze jsou použitelná a lze je použít pouze u řádků smlouvy s pevnou cenou (milník).</span><span class="sxs-lookup"><span data-stu-id="332db-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="332db-127">Tyto výchozí hodnoty se používají u souvisejících projektových transakcí na účtu a na řádcích faktur.</span><span class="sxs-lookup"><span data-stu-id="332db-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="332db-128">Definování výchozích finančních dimenzí pro projekty</span><span class="sxs-lookup"><span data-stu-id="332db-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="332db-129">Projekty jsou vytvářeny a spravovány v CDS.</span><span class="sxs-lookup"><span data-stu-id="332db-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="332db-130">Atributy účetnictví pro projekty jsou nastaveny v modulu **Řízení projektů a účetnictví** ve Finance.</span><span class="sxs-lookup"><span data-stu-id="332db-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="332db-131">Přejděte do části **Správa projektů a účetnictví** > **Projekty** > **Všechny projekty**.</span><span class="sxs-lookup"><span data-stu-id="332db-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="332db-132">Vyberte záznam, který chcete aktualizovat, a na kartě **Projekt** vyberte **Zobrazit výchozí účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="332db-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="332db-133">Rozbalte **Související informace** a vyberte kartu **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="332db-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="332db-134">Nastavte výchozí hodnoty finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="332db-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="332db-135">Všimněte si, že finanční dimenze vychází z účtu zákazníka.</span><span class="sxs-lookup"><span data-stu-id="332db-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="332db-136">Pokud je projekt přidružen k řádku smlouvy s více zákazníky projektové smlouvy, primární zákazník se použije k nastavení výchozích finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="332db-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="332db-137">Výchozí finanční dimenze projektu se používají k nastavení výchozích hodnot řádků deníku pro transakce času, výdajů a poplatků v **Deníku integrace Project Operations** a na souvisejících řádcích faktury projektu.</span><span class="sxs-lookup"><span data-stu-id="332db-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
