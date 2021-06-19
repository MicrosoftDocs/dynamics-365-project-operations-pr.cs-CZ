---
title: Konfigurace účtovatelných součásti řádku smlouvy na základě projektu
description: Tento téma poskytuje informace o tom, jak přidat účtovatelné komponenty do řádků smlouvy v Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003713"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="fa344-103">Konfigurace účtovatelných součásti řádku smlouvy na základě projektu</span><span class="sxs-lookup"><span data-stu-id="fa344-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="fa344-104">_**Platí pro:** omezené nasazení – dohoda o pro forma fakturaci, Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="fa344-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fa344-105">Řádek smlouvy na základě projektu má *zahrnuté* komponenty a *účtovatelné* komponenty.</span><span class="sxs-lookup"><span data-stu-id="fa344-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="fa344-106">Zahrnuté komponenty jsou komponenty, které podléhají:</span><span class="sxs-lookup"><span data-stu-id="fa344-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="fa344-107">Způsob fakturace a rozdělení zákazníků</span><span class="sxs-lookup"><span data-stu-id="fa344-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="fa344-108">Nepřekročitelné limity</span><span class="sxs-lookup"><span data-stu-id="fa344-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="fa344-109">Nastavení frekvence faktur definované na řádku smlouvy na základě projektu</span><span class="sxs-lookup"><span data-stu-id="fa344-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="fa344-110">Podskupinu zahrnutých komponent lze označit jako účtovatelnou pomocí pole **Typ fakturace**.</span><span class="sxs-lookup"><span data-stu-id="fa344-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="fa344-111">Pole **Typ fakturace** je sada možností, která umožňuje následující hodnoty v kontextu řádku smlouvy:</span><span class="sxs-lookup"><span data-stu-id="fa344-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="fa344-112">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-112">Chargeable</span></span>
  - <span data-ttu-id="fa344-113">Neúčtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-113">Non-chargeable</span></span>

<span data-ttu-id="fa344-114">Účtovatelné komponenty lze definovat na úkolech, rolích a kategoriích transakcí.</span><span class="sxs-lookup"><span data-stu-id="fa344-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="fa344-115">Účtovatelnost je definována na úkolech pro řádek smlouvy projektu a platí pro všechny třídy transakcí zahrnutých na řádku.</span><span class="sxs-lookup"><span data-stu-id="fa344-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="fa344-116">Pokud je pole **Zahrnout úkoly** na řádku smlouvy prázdné nebo je nastaveno na **Celý projekt**, karta **Účtovatelné úlohy** nebude k dispozici.</span><span class="sxs-lookup"><span data-stu-id="fa344-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="fa344-117">Účtovatelnost definovaná pro role pro řádek smlouvy projektu se vztahuje pouze na třídu transakcí **Čas**.</span><span class="sxs-lookup"><span data-stu-id="fa344-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="fa344-118">Pokud je pole **Zahrnout čas** na řádku smlouvy nastaveno na **Ne**, karta **Účtovatelné role** nebude k dispozici.</span><span class="sxs-lookup"><span data-stu-id="fa344-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="fa344-119">Účtovatelnost definovaná na kategoriích transakcí pro řádek smlouvy projektu se vztahuje pouze na třídu transakcí **Výdaj**.</span><span class="sxs-lookup"><span data-stu-id="fa344-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="fa344-120">Pokud je pole **Zahrnout výdaje** na řádku smlouvy nastaveno na **Ne**, karta **Účtovatelné kategorie** nebude k dispozici.</span><span class="sxs-lookup"><span data-stu-id="fa344-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="fa344-121">Nastavení úkolu projektu jako účtovatelného nebo neúčtovatelného</span><span class="sxs-lookup"><span data-stu-id="fa344-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="fa344-122">Úkol projektu může být účtovatelný nebo neúčtovatelný na konkrétním řádku smlouvy, což umožňuje následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="fa344-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="fa344-123">Pokud řádek smlouvy na základě projektu zahrnuje **Čas** a určitý úkol, **T1** je k němu přidruženo jako účtovatelné.</span><span class="sxs-lookup"><span data-stu-id="fa344-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="fa344-124">Pokud existuje druhý řádek smlouvy, který zahrnuje **Výdaje**, můžete úkol T1 na řádku smlouvy asociovat jako neúčtovatelný.</span><span class="sxs-lookup"><span data-stu-id="fa344-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="fa344-125">Výsledkem je, že veškerý čas zaznamenaný na úkolu je účtovatelný a všechny náklady jsou neúčtovatelné.</span><span class="sxs-lookup"><span data-stu-id="fa344-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="fa344-126">Typ fakturace úkolu lze nakonfigurovat na kartě **Účtovatelné úkoly** řádku smlouvy aktualizací pole **Typ fakturace** v podmřížce Úkoly řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fa344-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="fa344-127">Alternativně můžete aktualizovat pole **Typ fakturace** v nastavení fakturace úkolu projektu, které zobrazuje řádky smluv přidružené k úkolu.</span><span class="sxs-lookup"><span data-stu-id="fa344-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="fa344-128">Nastavení role jako účtovatelné nebo neúčtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="fa344-129">Role může být účtovatelná nebo neúčtovatelná na konkrétním řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fa344-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="fa344-130">Typ fakturace role lze nakonfigurovat na kartě **Účtovatelné role** řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fa344-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="fa344-131">Chcete-li to provést, aktualizujte pole **Typ fakturace** v podmřížce **Účtovatelné role**.</span><span class="sxs-lookup"><span data-stu-id="fa344-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="fa344-132">Nastavení kategorie transakcí jako účtovatelné nebo neúčtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="fa344-133">Kategorie transakcí může být účtovatelná nebo neúčtovatelná na konkrétním řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fa344-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="fa344-134">Typ fakturace transakce lze nakonfigurovat na kartě **Účtovatelné kategorie** řádku smlouvy na základě projektu.</span><span class="sxs-lookup"><span data-stu-id="fa344-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="fa344-135">Chcete-li to provést, aktualizujte pole **Typ fakturace** v podmřížce **Účtovatelné kategorie**.</span><span class="sxs-lookup"><span data-stu-id="fa344-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="fa344-136">Vyřešení účtovatelnosti</span><span class="sxs-lookup"><span data-stu-id="fa344-136">Resolve chargeability</span></span>

<span data-ttu-id="fa344-137">Vytvořený odhad nebo skutečná hodnota pro čas bude považována za účtovatelnou, pouze pokud:</span><span class="sxs-lookup"><span data-stu-id="fa344-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="fa344-138">**Čas** je uveden v řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fa344-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="fa344-139">**Role** je nakonfigurována jako účtovatelná na řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fa344-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="fa344-140">**Zahrnuté úkoly** je nastaveno na **Vybrané úkoly** na řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fa344-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="fa344-141">Pokud jsou tyto tři věci pravdivé, úkol je také nakonfigurován jako účtovatelný.</span><span class="sxs-lookup"><span data-stu-id="fa344-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="fa344-142">Vytvořený odhad nebo skutečná hodnota pro výdaj bude považována za účtovatelnou, pouze pokud:</span><span class="sxs-lookup"><span data-stu-id="fa344-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="fa344-143">**Výdaj** je uveden v řádku smlouvy</span><span class="sxs-lookup"><span data-stu-id="fa344-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="fa344-144">**Kategorie transakce** je nakonfigurována jako účtovatelná na řádku smlouvy</span><span class="sxs-lookup"><span data-stu-id="fa344-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="fa344-145">**Zahrnuté úkoly** je nastaveno na **Vybraný úkol** na řádku smlouvy</span><span class="sxs-lookup"><span data-stu-id="fa344-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="fa344-146">Pokud jsou tyto tři věci pravdivé, **úkol** je také nakonfigurován jako účtovatelný.</span><span class="sxs-lookup"><span data-stu-id="fa344-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="fa344-147">Vytvořený odhad nebo skutečná hodnota pro materiál bude považována za účtovatelnou, pouze pokud:</span><span class="sxs-lookup"><span data-stu-id="fa344-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="fa344-148">**Materiály** je uvedeno v řádku smlouvy</span><span class="sxs-lookup"><span data-stu-id="fa344-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="fa344-149">**Zahrnuté úkoly** je nastaveno na **Vybrané úkoly** na řádku smlouvy</span><span class="sxs-lookup"><span data-stu-id="fa344-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="fa344-150">Pokud jsou tyto dvě věci pravdivé, **úkol** je také nakonfigurován jako účtovatelný.</span><span class="sxs-lookup"><span data-stu-id="fa344-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa344-151">
                    <strong>Zahrnuje čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="fa344-152">
                    <strong>Zahrnuje výdaj</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="fa344-153">
                    <strong>Zahrnuje materiály</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="fa344-154">
                    <strong>Zahrnuté úkoly</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa344-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa344-156">
                    <strong>Kategorie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa344-157">
                    <strong>Úkol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="fa344-158">
                    <strong>Dopad účtovatelnosti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-159">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa344-160">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa344-161">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa344-162">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="fa344-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-163">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-164">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-165">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="fa344-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa344-166">Skutečná fakturace na čas: <strong>Účtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-167">Typ fakturace při skutečných výdajích: <strong>Účtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-168">Typ fakturace na skutečnou hodnotu materiálu: <strong>účtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-169">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa344-170">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa344-171">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa344-172">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="fa344-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-173">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-174">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-175">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa344-176">Skutečná fakturace na čas: <strong>Účtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-177">Typ fakturace při skutečných výdajích: <strong>Účtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-178">Typ fakturace na skutečnou hodnotu materiálu: <strong>účtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-179">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa344-180">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa344-181">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa344-182">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="fa344-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa344-183">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-184">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-185">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa344-186">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-187">Typ fakturace při skutečných výdajích: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa344-188">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="fa344-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-189">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa344-190">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa344-191">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa344-192">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="fa344-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-193">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-194">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa344-195">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa344-196">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-197">Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-198">Typ fakturace při skutečném materiálu: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-199">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa344-200">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa344-201">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa344-202">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="fa344-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa344-203">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-204">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa344-205">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa344-206">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-207">Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-208">Typ fakturace při skutečném materiálu: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-209">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa344-210">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa344-211">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa344-212">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="fa344-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa344-213">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa344-214">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-215">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa344-216">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-217">Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-218">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="fa344-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa344-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa344-220">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa344-221">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa344-222">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="fa344-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-223">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="fa344-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa344-224">
                    <strong>Účtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-225">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="fa344-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa344-226">Skutečná fakturace na čas: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-227">Typ fakturace při skutečných výdajích: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa344-228">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="fa344-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa344-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa344-230">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa344-231">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa344-232">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="fa344-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-233">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="fa344-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa344-234">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-235">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="fa344-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa344-236">Skutečná fakturace na čas: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-237">Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-238">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="fa344-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-239">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="fa344-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa344-241">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa344-242">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="fa344-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-243">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-244">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="fa344-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-245">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="fa344-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa344-246">Skutečná fakturace na čas: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa344-247">Typ fakturace při skutečných výdajích: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-248">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="fa344-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-249">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="fa344-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa344-251">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa344-252">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="fa344-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa344-253">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-254">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="fa344-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-255">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="fa344-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa344-256">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-257">Typ fakturace při skutečných výdajích: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-258">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="fa344-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-259">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa344-260">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="fa344-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa344-262">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="fa344-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-263">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-264">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-265">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="fa344-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa344-266">Skutečná fakturace na čas: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa344-267">Typ fakturace při skutečných výdajích: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="fa344-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa344-268">Typ fakturace při skutečném materiálu: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa344-269">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa344-270">Ano</span><span class="sxs-lookup"><span data-stu-id="fa344-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="fa344-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa344-272">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="fa344-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa344-273">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa344-274">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa344-275">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="fa344-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa344-276">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-277">Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa344-278">Typ fakturace při skutečném materiálu: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa344-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
