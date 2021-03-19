---
title: Přenos projektových rozpočtů na konci fiskálního roku
description: Tento článek poskytuje informace o tom, jak převést zbývající částky rozpočtu do budoucích let a jak vytvořit podrobnosti registru rozpočtu.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 1f601be072e84fc04246cd55a260c8004f6fb3e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289721"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="9390f-103">Přenos projektových rozpočtů na konci fiskálního roku</span><span class="sxs-lookup"><span data-stu-id="9390f-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9390f-104">Při práci na víceletém projektu můžete mít na konci fiskálního roku zbývající rozpočet.</span><span class="sxs-lookup"><span data-stu-id="9390f-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="9390f-105">Můžete převést zbývající částky rozpočtu do budoucího roku a vytvořit podrobnosti registru rozpočtu pro částky v přidružených účtech hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="9390f-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="9390f-106">Než převedete zbývající částky, zkontrolujte a analyzujte zbývající částky rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="9390f-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="9390f-107">Kontrola a analýza zbývajících částek rozpočtu</span><span class="sxs-lookup"><span data-stu-id="9390f-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="9390f-108">Proveďte následující kroky, abyste zkontrolovali částky rozpočtu na konci roku u projektů, ale částky nepřenášejte.</span><span class="sxs-lookup"><span data-stu-id="9390f-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="9390f-109">Přejděte do **Řízení projektů a účetnictví** > **Periodické** > **Rozpočty** > **Převést rozpočty do dalšího období**.</span><span class="sxs-lookup"><span data-stu-id="9390f-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="9390f-110">Na stránce **Proces převedení projektového rozpočtu do dalšího období** na kartě **Možnosti na konci roku** ověřte, že není zapnuta možnost **Převést do dalšího období zbývající částky rozpočtu projektu**.</span><span class="sxs-lookup"><span data-stu-id="9390f-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="9390f-111">Na kartě **Parametry** v poli **Rozpočtový rok projektu** vyberte fiskální rok, u kterého chcete zobrazit zbývající částku rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="9390f-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="9390f-112">V poli **Počáteční fiskální rok** vyberte fiskální rok, u kterého chcete zobrazit zbývající částku rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="9390f-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="9390f-113">V poli **Z modelu prognózy** vyberte hodnotu **Zbývající rozpočet**.</span><span class="sxs-lookup"><span data-stu-id="9390f-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="9390f-114">Chcete-li zahrnout projekty, které splňují vámi vybraná kritéria a nemají zbývající rozpočet, vyberte **Zobrazit nulový zůstatek**.</span><span class="sxs-lookup"><span data-stu-id="9390f-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="9390f-115">Na kartě **Vyberte rozpočty** zvolte možnost **Načíst všechny rozpočty**, aby se načetly všechny rozpočty odpovídající vybraným kritériím, a poté vyberte **Zpracovat**.</span><span class="sxs-lookup"><span data-stu-id="9390f-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="9390f-116">Chcete-li navrhnout databázový dotaz, který do podokna načte konkrétní sadu rozpočtů, vyberte možnost **Načíst vybrané rozpočty**.</span><span class="sxs-lookup"><span data-stu-id="9390f-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="9390f-117">Chcete-li další informace o konkrétním řádku v podokně, vyberte řádek a poté vyberte příkaz **Zobrazit podrobnosti rozpočtu** nebo **Zobrazit účty**.</span><span class="sxs-lookup"><span data-stu-id="9390f-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="9390f-118">Převod zbývajících částek rozpočtu</span><span class="sxs-lookup"><span data-stu-id="9390f-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="9390f-119">Při zpracování zbývajících částek rozpočtu můžete v hlavní knize vytvořit transakce pro částky, které přenášíte.</span><span class="sxs-lookup"><span data-stu-id="9390f-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="9390f-120">Chcete-li vytvořit transakce hlavní knihy, proveďte kroky v části [Převod částek rozpočtu a vytvoření transakcí hlavní knihy](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="9390f-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="9390f-121">Částky rozpočtu, které jsou převedeny, jsou přeneseny do modelu prognózy, který je vybrán na stránce **Modely prognóz** jako model prognózy převodu.</span><span class="sxs-lookup"><span data-stu-id="9390f-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="9390f-122">Převod částek rozpočtu a vytvoření transakcí hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="9390f-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="9390f-123">Vyberte položku nabídky **Řízení projektů a účetnictví** > **Periodické** > **Rozpočty** > **Převést rozpočty do dalšího období**.</span><span class="sxs-lookup"><span data-stu-id="9390f-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="9390f-124">Na stránce **Proces převedení projektového rozpočtu do dalšího období** vyberte **Konec roku** a poté povolte možnosti **Převést zbývající částky rozpočtu projektu** a **Vytvořit položky registru rozpočtu v hlavní knize**.</span><span class="sxs-lookup"><span data-stu-id="9390f-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="9390f-125">Na kartě **Parametry** ve skupině polí **Parametry projektu** vyberte následující:</span><span class="sxs-lookup"><span data-stu-id="9390f-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="9390f-126">**Rozpočtový rok projektu**: Vyberte začátek fiskálního roku, u kterého chcete zobrazit zbývající částky rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="9390f-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="9390f-127">**Zisk a ztráta**: Vytvořte transakce zisků a ztrát v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="9390f-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="9390f-128">**NV**: Vytvořte transakce probíhajících prací (nedokončené výroby) v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="9390f-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="9390f-129">**Mzdy**: Vytvořte transakce přidělení mezd v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="9390f-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="9390f-130">Ve skupině polí **Hlavní kniha** zadejte následující informace:</span><span class="sxs-lookup"><span data-stu-id="9390f-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="9390f-131">V poli **Počáteční fiskální rok** vyberte fiskální rok, do kterého chcete přenést zbývající částky projektových rozpočtů.</span><span class="sxs-lookup"><span data-stu-id="9390f-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="9390f-132">Výchozí hodnota je jeden rok po hodnotě v poli **Rozpočtový rok projektu**.</span><span class="sxs-lookup"><span data-stu-id="9390f-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="9390f-133">V poli **Období převedení do dalšího období** vyberte období, pro které chcete vytvořit podrobnosti registru rozpočtu v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="9390f-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="9390f-134">Jedná se obvykle o první období v úvodním fiskálním roku.</span><span class="sxs-lookup"><span data-stu-id="9390f-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="9390f-135">Ve skupině polí **Kopírovat z/do** zadejte následující informace:</span><span class="sxs-lookup"><span data-stu-id="9390f-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="9390f-136">V poli **Z modelu prognózy** vyberte model prognózy projektového rozpočtu spojený se zbývajícími částkami rozpočtu, které chcete pro projekty převést.</span><span class="sxs-lookup"><span data-stu-id="9390f-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="9390f-137">V poli **Do rozpočtového modelu hlavní knihy** vyberte model rozpočtu hlavní knihy spojený s částkami rozpočtu, které chcete převést do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="9390f-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="9390f-138">Vyberte příkaz **Převést prodejní měnu**, chcete-li použít prodejní měnu projektu pro transakce hlavní knihy, které se vytvoří při přenosu částek rozpočtu pro projekty.</span><span class="sxs-lookup"><span data-stu-id="9390f-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="9390f-139">Pokud tato možnost není vybrána, transakce používají účetní měnu.</span><span class="sxs-lookup"><span data-stu-id="9390f-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="9390f-140">Vyberte možnost **Zobrazit nulový zůstatek**, chcete-li zahrnout projekty, které nemají žádné zbývající částky rozpočtu, ale splňují další kritéria, která vyberete v projektech zobrazených v dolním podokně.</span><span class="sxs-lookup"><span data-stu-id="9390f-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="9390f-141">Na kartě **Vyberte rozpočty** zvolte možnost **Načíst všechny rozpočty**, aby se načetly všechny rozpočty odpovídající vybraným kritériím.</span><span class="sxs-lookup"><span data-stu-id="9390f-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="9390f-142">Dáváte-li přednost návrhu databázového dotazu, který do podokna načte konkrétní sadu projektových rozpočtů, vyberte možnost **Načíst vybrané rozpočty**.</span><span class="sxs-lookup"><span data-stu-id="9390f-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="9390f-143">U každého projektu, který chcete zpracovat, vyberte možnost na začátku řádku pro projekt.</span><span class="sxs-lookup"><span data-stu-id="9390f-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="9390f-144">Chcete-li vybrat všechny nebo většinu projektů, zaškrtněte políčko v levém horním levém rohu.</span><span class="sxs-lookup"><span data-stu-id="9390f-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="9390f-145">Chcete-li vyloučit nějaký projekt ze zpracování, vypněte zaškrtávací políčko pro tento projekt.</span><span class="sxs-lookup"><span data-stu-id="9390f-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="9390f-146">Chcete-li přenést zbývající částky rozpočtu pro vybrané projekty do vybraného fiskálního roku a vytvořit podrobnosti registru rozpočtu v hlavní knize, vyberte příkaz **Zpracovat**.</span><span class="sxs-lookup"><span data-stu-id="9390f-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="9390f-147">Převod částek rozpočtu bez vytvoření transakcí hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="9390f-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="9390f-148">Přejděte do **Řízení projektů a účetnictví** > **Periodické** > **Rozpočty** > **Převést rozpočty do dalšího období**.</span><span class="sxs-lookup"><span data-stu-id="9390f-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="9390f-149">Na stránce **Proces převedení projektového rozpočtu do dalšího období** na kartě **Možnosti na konci roku** zapněte možnost **Převést do dalšího období zbývající částky rozpočtu projektu**.</span><span class="sxs-lookup"><span data-stu-id="9390f-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="9390f-150">Ve skupině **Parametry** v poli **Rozpočtový rok projektu** vyberte fiskální rok, u kterého chcete zobrazit zbývající částky rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="9390f-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="9390f-151">Ve skupině **Kopírovat z/do** zadejte následující informace:</span><span class="sxs-lookup"><span data-stu-id="9390f-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="9390f-152">V poli **Z modelu prognózy** vyberte model prognózy projektového rozpočtu, který je spojený se zbývajícími částkami rozpočtu, které chcete pro projekty převést.</span><span class="sxs-lookup"><span data-stu-id="9390f-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="9390f-153">Chcete-li zahrnout projekty, které nemají zbývající rozpočtové částky, ale splňují jiná vámi vybraná kritéria, vyberte možnost **Zobrazit nulový zůstatek**.</span><span class="sxs-lookup"><span data-stu-id="9390f-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="9390f-154">Ve skupině **Vyberte rozpočty** zvolte možnost **Načíst všechny rozpočty**, aby se načetly všechny rozpočty odpovídající vybraným kritériím.</span><span class="sxs-lookup"><span data-stu-id="9390f-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="9390f-155">Chcete-li navrhnout databázový dotaz, který do podokna načte konkrétní sadu projektových rozpočtů, vyberte možnost **Načíst vybrané rozpočty**.</span><span class="sxs-lookup"><span data-stu-id="9390f-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="9390f-156">U každého projektu, který chcete zpracovat, vyberte možnost na začátku řádku pro projekt.</span><span class="sxs-lookup"><span data-stu-id="9390f-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="9390f-157">Výběrem příkazu **Zpracovat** převeďte zbývající částky rozpočtu pro vybrané projekty do vybraného fiskálního roku.</span><span class="sxs-lookup"><span data-stu-id="9390f-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]