---
title: Vytváření rozšířených smluv pro fakturaci na základě pokroku
description: Toto téma vysvětluje, jak vytvořit projektové smlouvy, abyste mohli generovat faktury pro zákazníky na základě procenta z dokončené práce.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3b445488100e0a8335a05505405953b173ff836c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999663"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="4b82c-103">Vytváření rozšířených smluv pro fakturaci na základě pokroku</span><span class="sxs-lookup"><span data-stu-id="4b82c-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b82c-104">Toto téma vysvětluje, jak vytvořit projektové smlouvy, abyste mohli vytvářet faktury pro zákazníky na základě procenta z dokončené práce.</span><span class="sxs-lookup"><span data-stu-id="4b82c-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="4b82c-105">Částky faktury se automaticky počítají pro rozpočtové kategorie práce, které jste pro projekt nastavili.</span><span class="sxs-lookup"><span data-stu-id="4b82c-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="4b82c-106">Časování faktur je nastaveno při sjednávání projektové smlouvy se zákazníkem.</span><span class="sxs-lookup"><span data-stu-id="4b82c-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="4b82c-107">Pomocí postupů v tomto tématu můžete nastavit smlouvu, přidružený projekt a pravidla fakturace, která počítají částky faktur pro rozpočtové kategorie práce, které jste pro projekt nastavili.</span><span class="sxs-lookup"><span data-stu-id="4b82c-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="4b82c-108">Poté, co vytvoříte smlouvu a projekt, můžete nastavit podrobnosti projektu.</span><span class="sxs-lookup"><span data-stu-id="4b82c-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="4b82c-109">Můžete například definovat aktivity a přiřadit pracovníky k projektu.</span><span class="sxs-lookup"><span data-stu-id="4b82c-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="4b82c-110">Příklad</span><span class="sxs-lookup"><span data-stu-id="4b82c-110">Example</span></span>

<span data-ttu-id="4b82c-111">Vaše organizace je firma zabývající se vývojem softwaru.</span><span class="sxs-lookup"><span data-stu-id="4b82c-111">Your organization is a software development firm.</span></span> <span data-ttu-id="4b82c-112">Souhlasíte s vytvořením balíčku mzdového účetnictví pro zákazníka s celkovou částkou 20 000 amerických dolarů (USD).</span><span class="sxs-lookup"><span data-stu-id="4b82c-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="4b82c-113">Vaše organizace se zavazuje fakturovat zákazníkovi, jakmile dokončíte konkrétní procento projektu.</span><span class="sxs-lookup"><span data-stu-id="4b82c-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="4b82c-114">Pro práci nastavíte následující projektové kategorie, abyste je mohli použít v procesu fakturace:</span><span class="sxs-lookup"><span data-stu-id="4b82c-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="4b82c-115">Poradenství</span><span class="sxs-lookup"><span data-stu-id="4b82c-115">Consulting</span></span>
- <span data-ttu-id="4b82c-116">Návrh</span><span class="sxs-lookup"><span data-stu-id="4b82c-116">Design</span></span>
- <span data-ttu-id="4b82c-117">Instalace</span><span class="sxs-lookup"><span data-stu-id="4b82c-117">Installation</span></span>

<span data-ttu-id="4b82c-118">Nastavíte také pravidla fakturace, která automaticky vypočítají částky faktury pro procento projektové práce dokončené v každé kategorii.</span><span class="sxs-lookup"><span data-stu-id="4b82c-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="4b82c-119">Manažer rozpočtu vytvoří rozpočet pro kategorie projektů.</span><span class="sxs-lookup"><span data-stu-id="4b82c-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="4b82c-120">Množství dokončené práce se automaticky vypočítá jako procento skutečné práce ve srovnání s částkami rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="4b82c-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4b82c-121">Požadavky</span><span class="sxs-lookup"><span data-stu-id="4b82c-121">Prerequisites</span></span>

<span data-ttu-id="4b82c-122">Před vytvořením projektu, který používá pravidla fakturace, musíte nastavit číselné řady pro pravidla fakturace a deník poplatků, který se používá k zaúčtování fakturace průběhu.</span><span class="sxs-lookup"><span data-stu-id="4b82c-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="4b82c-123">Přejděte do nabídky **Řízení projektů a účetnictví** \> **Nastavení** \> **Parametry modulu Řízení a účetnictví projektu**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="4b82c-124">Na stránce **Parametry modulu Řízení a účetnictví projektu** na kartě **Číselné řady** nastavte číselnou posloupnost, kterou chcete použít při vytváření pravidel fakturace.</span><span class="sxs-lookup"><span data-stu-id="4b82c-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="4b82c-125">Přejděte do nabídky **Řízení projektů a účetnictví** \> **Deníky** \> **Poplatek**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="4b82c-126">Na stránce **Deník poplatků** vyberte **Nový** a zadejte název deníku.</span><span class="sxs-lookup"><span data-stu-id="4b82c-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="4b82c-127">Vytvoření smlouvy pro fakturaci průběhu</span><span class="sxs-lookup"><span data-stu-id="4b82c-127">Create a contract for progress billings</span></span>

<span data-ttu-id="4b82c-128">Tento postup využijte k vytvoření projektové smlouvy pro projekt s pevnou cenou.</span><span class="sxs-lookup"><span data-stu-id="4b82c-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="4b82c-129">Projektovou fakturu vytvoříte, když práce dokončená na projektu dosáhne stanoveného procenta.</span><span class="sxs-lookup"><span data-stu-id="4b82c-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="4b82c-130">Přejděte do nabídky **Řízení projektů a účetnictví** \> **Projekty** \> **Projektové smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="4b82c-131">Na stránce **Projektové smlouvy** vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="4b82c-132">V dialogovém okně **Nová projektová smlouva** nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="4b82c-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="4b82c-133">**Jméno**</span><span class="sxs-lookup"><span data-stu-id="4b82c-133">**Name**</span></span>
    - <span data-ttu-id="4b82c-134">**Typ financování**</span><span class="sxs-lookup"><span data-stu-id="4b82c-134">**Funding type**</span></span>
    - <span data-ttu-id="4b82c-135">**Zdroj financování**</span><span class="sxs-lookup"><span data-stu-id="4b82c-135">**Funding source**</span></span>
    - <span data-ttu-id="4b82c-136">**Prodejní měna** – Ve výchozím nastavení se tato měna používá ve fakturách zákazníků spojených s projektovou smlouvou.</span><span class="sxs-lookup"><span data-stu-id="4b82c-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="4b82c-137">Prodejní měnu však můžete na konkrétní faktuře zákazníka změnit.</span><span class="sxs-lookup"><span data-stu-id="4b82c-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="4b82c-138">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-138">Select **OK**.</span></span> <span data-ttu-id="4b82c-139">Informace se zkopírují do záhlaví stránky **Projektové smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="4b82c-140">Na stránce **Projektové smlouvy** vyplňte zbývající požadované informace o projektu.</span><span class="sxs-lookup"><span data-stu-id="4b82c-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="4b82c-141">Vytvoření projektu pro fakturaci průběhu</span><span class="sxs-lookup"><span data-stu-id="4b82c-141">Create a project for progress billings</span></span>

<span data-ttu-id="4b82c-142">Tento postup využijte k vytvoření projektu a všech dílčích projektů, které jsou spojeny s projektovou smlouvou.</span><span class="sxs-lookup"><span data-stu-id="4b82c-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="4b82c-143">Přejděte do části **Řízení projektů a účetnictví** \> **Projekty** \> **Všechny projekty**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="4b82c-144">Na stránce **Všechny projekty** vyberte příkaz **Nový**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="4b82c-145">V dialogovém okně **Nový projekt** vyberte v poli **Typ projektu** hodnotu **Čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="4b82c-146">Vyberte skupinu projektu.</span><span class="sxs-lookup"><span data-stu-id="4b82c-146">Select a project group.</span></span> <span data-ttu-id="4b82c-147">Skupina projektu definuje informace o účtování pro projekty, které jsou skupině přiřazeny.</span><span class="sxs-lookup"><span data-stu-id="4b82c-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="4b82c-148">Vyberte příkaz **Vytvořit projekt**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-148">Select **Create project**.</span></span>
6. <span data-ttu-id="4b82c-149">Po vytvoření projektu nastavte fázi projektu na **Probíhá**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="4b82c-150">Vytvoření rozpočtu pro projekt</span><span class="sxs-lookup"><span data-stu-id="4b82c-150">Create a budget for a project</span></span>

<span data-ttu-id="4b82c-151">Rozpočtové kategorie se používají k automatickému výpočtu částek faktury pro procento práce dokončené v každé kategorii.</span><span class="sxs-lookup"><span data-stu-id="4b82c-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="4b82c-152">Pomocí následujícího postupu vytvořte rozpočtové kategorie pro odhadované náklady.</span><span class="sxs-lookup"><span data-stu-id="4b82c-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="4b82c-153">Přejděte do části **Řízení projektů a účetnictví** \> **Projekty** \> **Všechny projekty**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="4b82c-154">Na stránce **Všechny projekty** vyberte a otevřete požadovaný projekt.</span><span class="sxs-lookup"><span data-stu-id="4b82c-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="4b82c-155">Na stránce **Projekty** v podokně akcí na kartě **Plán** vyberte ve skupině **Rozpočet** hodnotu **Rozpočet projektu**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="4b82c-156">Na stránce **Rozpočet projektu** zadejte odhadované náklady pro každou kategorii v projektu.</span><span class="sxs-lookup"><span data-stu-id="4b82c-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="4b82c-157">Vytvořte pravidla fakturace pro fakturaci průběhu</span><span class="sxs-lookup"><span data-stu-id="4b82c-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="4b82c-158">Přejděte do nabídky **Řízení projektů a účetnictví** \> **Projekty** \> **Projektové smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="4b82c-159">Na stránce **Projektové smlouvy** vyberte a otevřete projektovou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="4b82c-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="4b82c-160">Na stránce projektové smlouvy vyberte na pevné záložce **Pravidla fakturace** příkaz **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="4b82c-161">Na stránce **Pravidlo fakturace** vyberte v poli **Typ řádku** hodnotu **Průběh**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="4b82c-162">Na pevné záložce **Podrobnosti řádku pravidla účtování** v poli **Hodnota smlouvy** zadejte celkovou hodnotu smlouvy.</span><span class="sxs-lookup"><span data-stu-id="4b82c-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="4b82c-163">V poli **Kategorie** vyberte kategorii, do které chcete zaúčtovat transakci poplatku.</span><span class="sxs-lookup"><span data-stu-id="4b82c-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="4b82c-164">V poli **Projekt** vyberte projekt, který používá toto fakturační pravidlo.</span><span class="sxs-lookup"><span data-stu-id="4b82c-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="4b82c-165">Volitelné: Přiřaďte pravidlo fakturace k dalším projektům.</span><span class="sxs-lookup"><span data-stu-id="4b82c-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="4b82c-166">Na pevné záložce **Projekt** v části **Dostupné projekty** vyberte projekt a poté kliknutím na tlačítko se šipkou doprava přidejte projekt do části **Vybrané projekty**.</span><span class="sxs-lookup"><span data-stu-id="4b82c-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="4b82c-167">Volitelné: Vypočítejte procentní částku, kterou zákazník zadrží z plateb na faktuře.</span><span class="sxs-lookup"><span data-stu-id="4b82c-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="4b82c-168">Na pevné záložce **Podmínky zadržení platby** vyberte zdroj financování a poté v poli **Procento zádržného** zadejte procento zádržného.</span><span class="sxs-lookup"><span data-stu-id="4b82c-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="4b82c-169">Opakováním těchto kroků vytvoříte další fakturační pravidla pro projektovou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="4b82c-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]