---
title: Dotaz Plán výdajů z federálních grantů
description: Toto téma poskytuje informace o dotazu Plán výdajů z federálních grantů.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 70dff12c106723dda801668412cfd084c462db4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288956"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="39a99-103">Dotaz Plán výdajů z federálních grantů</span><span class="sxs-lookup"><span data-stu-id="39a99-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39a99-104">Podle oběžníku A-133 Úřadu pro správu a rozpočet (Office of Management and Budget) se na agentury, které dostávají federální fondy, vztahují požadavky na audit, které se označují také jako jednotné audity.</span><span class="sxs-lookup"><span data-stu-id="39a99-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="39a99-105">Proces auditu se používá k pravidelnému podávání zpráv o příjmech a výdajích plynoucích z federálních grantů.</span><span class="sxs-lookup"><span data-stu-id="39a99-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="39a99-106">Součástí zprávy o jednotném auditu je Plán výdajů z federálních grantů (Schedule of Expenditures of Federal Awards, SEFA).</span><span class="sxs-lookup"><span data-stu-id="39a99-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="39a99-107">Dotaz Plán výdajů z federálních grantů zahrnuje název a číslo katalogu federální domácí pomoci (CFDA), číslo grantu, rok poskytnutí grantu, název federální agentury, která poskytuje finanční prostředky, a název předávací entity.</span><span class="sxs-lookup"><span data-stu-id="39a99-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="39a99-108">Dotaz je určen pro konkrétní období.</span><span class="sxs-lookup"><span data-stu-id="39a99-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="39a99-109">Toto období je obvykle stejné jako období finančního výkazu, což je fiskální rok.</span><span class="sxs-lookup"><span data-stu-id="39a99-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="39a99-110">Dotaz zahrnuje granty, které mají projekční data ve vybraném časovém období.</span><span class="sxs-lookup"><span data-stu-id="39a99-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="39a99-111">Sloupec **Grantor agency** (Grantová agentura) v dotazu uvádí zákazníka grantu nebo – u předávacího grantu – agenturu poskytující granty.</span><span class="sxs-lookup"><span data-stu-id="39a99-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="39a99-112">U předávacího grantu je ve sloupci **Pass-through agency** (Předávací agentura) uveden zákazník grantu.</span><span class="sxs-lookup"><span data-stu-id="39a99-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="39a99-113">Jestliže grant není předávací, je sloupec **Pass-through agency** (Předávací agentura) ponechán prázdný.</span><span class="sxs-lookup"><span data-stu-id="39a99-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="39a99-114">Nastavení clusterů CFDA</span><span class="sxs-lookup"><span data-stu-id="39a99-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="39a99-115">Musíte nastavit clustery CFDA, které lze přidružit k číslům CFDA v dotazu Plán výdajů z federálních grantů.</span><span class="sxs-lookup"><span data-stu-id="39a99-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="39a99-116">Přejděte do nabídky **Řízení projektů a účetnictví \> Nastavení \> Granty \> Katalog clusterů federální domácí pomoci**.</span><span class="sxs-lookup"><span data-stu-id="39a99-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="39a99-117">Výběrem položky **Nový** vytvoříte cluster CFDA.</span><span class="sxs-lookup"><span data-stu-id="39a99-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="39a99-118">Zadejte název clusteru.</span><span class="sxs-lookup"><span data-stu-id="39a99-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="39a99-119">Výběrem možnosti **Uložit** uložte změny.</span><span class="sxs-lookup"><span data-stu-id="39a99-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="39a99-120">Nastavení čísel CFDA</span><span class="sxs-lookup"><span data-stu-id="39a99-120">Set up CFDA numbers</span></span>

<span data-ttu-id="39a99-121">Musíte nastavit čísla CFDA, které lze přidat ke grantům a zahrnout do dotazu Plán výdajů z federálních grantů.</span><span class="sxs-lookup"><span data-stu-id="39a99-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="39a99-122">Přejděte do nabídky **Řízení projektů a účetnictví \> Nastavení \> Granty \> Katalog čísel federální domácí pomoci**.</span><span class="sxs-lookup"><span data-stu-id="39a99-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="39a99-123">Výběrem položky **Nové** vytvoříte číslo CFDA.</span><span class="sxs-lookup"><span data-stu-id="39a99-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="39a99-124">Do sloupce **Číslo** zadejte číslo CFDA.</span><span class="sxs-lookup"><span data-stu-id="39a99-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="39a99-125">Stiskněte **tabulátor**.</span><span class="sxs-lookup"><span data-stu-id="39a99-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="39a99-126">Do sloupce **Popis** zadejte název CFDA.</span><span class="sxs-lookup"><span data-stu-id="39a99-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="39a99-127">Stiskněte **tabulátor**.</span><span class="sxs-lookup"><span data-stu-id="39a99-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="39a99-128">Volitelné: V poli **Programový cluster** přidejte příslušný cluster CFDA.</span><span class="sxs-lookup"><span data-stu-id="39a99-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="39a99-129">Výběrem možnosti **Uložit** uložte změny.</span><span class="sxs-lookup"><span data-stu-id="39a99-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="39a99-130">Nastavení grantů, které budou vykazovány v dotazu Plán výdajů z federálních grantů</span><span class="sxs-lookup"><span data-stu-id="39a99-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="39a99-131">Přejděte do nabídky **Řízení projektů a účetnictví \> Granty \> Granty** a vyberte existující grant.</span><span class="sxs-lookup"><span data-stu-id="39a99-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="39a99-132">Na pevné záložce **Nastavení** přiřaďte číslo CFDA v poli **Katalog federální domácí pomoci**.</span><span class="sxs-lookup"><span data-stu-id="39a99-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="39a99-133">Číslo CFDA na grantu určuje cluster CFDA pro podávání zpráv.</span><span class="sxs-lookup"><span data-stu-id="39a99-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="39a99-134">Na pevné záložce **Kontaktní informace** zadejte informace o poskytovateli grantů pomocí následujícího postupu:</span><span class="sxs-lookup"><span data-stu-id="39a99-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="39a99-135">V poli **Zákazník grantu** zadejte zákazníka, který je odpovědný za grant.</span><span class="sxs-lookup"><span data-stu-id="39a99-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="39a99-136">U stávajícího grantu mohou být tyto informace již zadány.</span><span class="sxs-lookup"><span data-stu-id="39a99-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="39a99-137">Uveďte, zda je zákazník grantu sám plátcem.</span><span class="sxs-lookup"><span data-stu-id="39a99-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="39a99-138">Pokud je zákazník grantu plátcem, nechte zaškrtávací políčko **Předávací** vypnuté.</span><span class="sxs-lookup"><span data-stu-id="39a99-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="39a99-139">Pokud je plátcem jiný zákazník a za utrácení a sledování peněz je odpovědný zákazník grantu, zapněte zaškrtávací políčko **Předávací**.</span><span class="sxs-lookup"><span data-stu-id="39a99-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="39a99-140">Pokud jste v předchozím kroku zapnuli zaškrtávací políčko **Předávací**, zadejte v poli **Grantová agentura** zákazníka, který poskytl grant.</span><span class="sxs-lookup"><span data-stu-id="39a99-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="39a99-141">Agentura poskytující granty a zákazník grantu nemohou být stejní zákazníci.</span><span class="sxs-lookup"><span data-stu-id="39a99-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="39a99-142">Zde je příklad předávacího grantu:</span><span class="sxs-lookup"><span data-stu-id="39a99-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="39a99-143">Federální vláda financovala projekt infrastruktury pro stát.</span><span class="sxs-lookup"><span data-stu-id="39a99-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="39a99-144">Federální vláda dala státu peníze na útratu.</span><span class="sxs-lookup"><span data-stu-id="39a99-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="39a99-145">V tomto případě je federální vláda agenturou poskytující granty a stát je zákazníkem grantu.</span><span class="sxs-lookup"><span data-stu-id="39a99-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="39a99-146">Při prvním zapnutí této funkce budou počáteční čísla CFDA zadána pomocí stávajících čísel v grantech.</span><span class="sxs-lookup"><span data-stu-id="39a99-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="39a99-147">Vyloučení grantů z vykazování SEFA na základě typu grantu</span><span class="sxs-lookup"><span data-stu-id="39a99-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="39a99-148">Přejděte do nabídky **Řízení projektů a účetnictví \> Nastavení \> Granty \> Typy grantů**.</span><span class="sxs-lookup"><span data-stu-id="39a99-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="39a99-149">Na pevné záložce **Výchozí informace** zaškrtněte políčko **Vyloučit z plánu výdajů z federálních grantů**.</span><span class="sxs-lookup"><span data-stu-id="39a99-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="39a99-150">Výběrem možnosti **Uložit** uložte změny.</span><span class="sxs-lookup"><span data-stu-id="39a99-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="39a99-151">Spuštění dotazu Plán výdajů z federálních grantů</span><span class="sxs-lookup"><span data-stu-id="39a99-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="39a99-152">Přejděte do nabídky **Řízení projektů a účetnictví \> Dotazy a sestavy \> Dotaz na grant \> Plán výdajů z federálních grantů**.</span><span class="sxs-lookup"><span data-stu-id="39a99-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="39a99-153">V části **Parametry** postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="39a99-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="39a99-154">V poli **Interval dat** vyberte kód pro časový interval.</span><span class="sxs-lookup"><span data-stu-id="39a99-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="39a99-155">Případně definujte časový interval v polích **Od data** a **Do data**.</span><span class="sxs-lookup"><span data-stu-id="39a99-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="39a99-156">Volitelné: Chcete-li do dotazu zahrnout jako výnos pouze fakturované transakce, nastavte možnost **Zahrnout pouze fakturované výnosy** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="39a99-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="39a99-157">Sloupce</span><span class="sxs-lookup"><span data-stu-id="39a99-157">Columns</span></span>

<span data-ttu-id="39a99-158">Dotaz Plán výdajů z federálních grantů zahrnuje následující sloupce:</span><span class="sxs-lookup"><span data-stu-id="39a99-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="39a99-159">Katalog názvů clusterů federální domácí pomoci</span><span class="sxs-lookup"><span data-stu-id="39a99-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="39a99-160">Grantová agentura</span><span class="sxs-lookup"><span data-stu-id="39a99-160">Grantor agency</span></span>
- <span data-ttu-id="39a99-161">Předávací agentura</span><span class="sxs-lookup"><span data-stu-id="39a99-161">Pass-through agency</span></span>
- <span data-ttu-id="39a99-162">Název grantu</span><span class="sxs-lookup"><span data-stu-id="39a99-162">Grant name</span></span>
- <span data-ttu-id="39a99-163">ID grantu</span><span class="sxs-lookup"><span data-stu-id="39a99-163">Grant ID</span></span>
- <span data-ttu-id="39a99-164">ID aplikace grantu</span><span class="sxs-lookup"><span data-stu-id="39a99-164">Grant application ID</span></span>
- <span data-ttu-id="39a99-165">Katalog federální domácí pomoci</span><span class="sxs-lookup"><span data-stu-id="39a99-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="39a99-166">Potvrzení</span><span class="sxs-lookup"><span data-stu-id="39a99-166">Receipts</span></span>
- <span data-ttu-id="39a99-167">Výdaje</span><span class="sxs-lookup"><span data-stu-id="39a99-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]