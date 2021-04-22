---
title: Konfigurace účtovatelných součásti řádku smlouvy na základě projektu
description: Tento téma poskytuje informace o tom, jak přidat účtovatelné komponenty do řádků smlouvy v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858465"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="3967f-103">Konfigurace účtovatelných součásti řádku smlouvy na základě projektu</span><span class="sxs-lookup"><span data-stu-id="3967f-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="3967f-104">_**Platí pro:** omezené nasazení – dohoda o pro forma fakturaci, Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="3967f-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3967f-105">Řádek smlouvy na základě projektu má *zahrnuté* komponenty a *účtovatelné* komponenty.</span><span class="sxs-lookup"><span data-stu-id="3967f-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="3967f-106">Zahrnuté komponenty jsou komponenty, které podléhají:</span><span class="sxs-lookup"><span data-stu-id="3967f-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="3967f-107">Způsob fakturace a rozdělení zákazníků</span><span class="sxs-lookup"><span data-stu-id="3967f-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="3967f-108">Nepřekročitelné limity</span><span class="sxs-lookup"><span data-stu-id="3967f-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="3967f-109">Nastavení frekvence faktur definované na řádku smlouvy na základě projektu</span><span class="sxs-lookup"><span data-stu-id="3967f-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="3967f-110">Podskupinu zahrnutých komponent lze označit jako účtovatelnou pomocí pole **Typ fakturace**.</span><span class="sxs-lookup"><span data-stu-id="3967f-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="3967f-111">Pole **Typ fakturace** je sada možností, která umožňuje následující hodnoty v kontextu řádku smlouvy:</span><span class="sxs-lookup"><span data-stu-id="3967f-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="3967f-112">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-112">Chargeable</span></span>
  - <span data-ttu-id="3967f-113">Neúčtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-113">Non-chargeable</span></span>

<span data-ttu-id="3967f-114">Účtovatelné komponenty lze definovat na úkolech, rolích a kategoriích transakcí.</span><span class="sxs-lookup"><span data-stu-id="3967f-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="3967f-115">Účtovatelnost je definována na úkolech pro řádek smlouvy projektu a platí pro všechny třídy transakcí zahrnutých na řádku.</span><span class="sxs-lookup"><span data-stu-id="3967f-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="3967f-116">Pokud je pole **Zahrnout úkoly** na řádku smlouvy prázdné nebo je nastaveno na **Celý projekt**, karta **Účtovatelné úlohy** nebude k dispozici.</span><span class="sxs-lookup"><span data-stu-id="3967f-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="3967f-117">Účtovatelnost definovaná pro role pro řádek smlouvy projektu se vztahuje pouze na třídu transakcí **Čas**.</span><span class="sxs-lookup"><span data-stu-id="3967f-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="3967f-118">Pokud je pole **Zahrnout čas** na řádku smlouvy nastaveno na **Ne**, karta **Účtovatelné role** nebude k dispozici.</span><span class="sxs-lookup"><span data-stu-id="3967f-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="3967f-119">Účtovatelnost definovaná na kategoriích transakcí pro řádek smlouvy projektu se vztahuje pouze na třídu transakcí **Výdaj**.</span><span class="sxs-lookup"><span data-stu-id="3967f-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="3967f-120">Pokud je pole **Zahrnout výdaje** na řádku smlouvy nastaveno na **Ne**, karta **Účtovatelné kategorie** nebude k dispozici.</span><span class="sxs-lookup"><span data-stu-id="3967f-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="3967f-121">Nastavení úkolu projektu jako účtovatelného nebo neúčtovatelného</span><span class="sxs-lookup"><span data-stu-id="3967f-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="3967f-122">Úkol projektu může být účtovatelný nebo neúčtovatelný na konkrétním řádku smlouvy, což umožňuje následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="3967f-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="3967f-123">Pokud řádek smlouvy na základě projektu zahrnuje **Čas** a určitý úkol, **T1** je k němu přidruženo jako účtovatelné.</span><span class="sxs-lookup"><span data-stu-id="3967f-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="3967f-124">Pokud existuje druhý řádek smlouvy, který zahrnuje **Výdaje**, můžete úkol T1 na řádku smlouvy asociovat jako neúčtovatelný.</span><span class="sxs-lookup"><span data-stu-id="3967f-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="3967f-125">Výsledkem je, že veškerý čas zaznamenaný na úkolu je účtovatelný a všechny náklady jsou neúčtovatelné.</span><span class="sxs-lookup"><span data-stu-id="3967f-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="3967f-126">Typ fakturace úkolu lze nakonfigurovat na kartě **Účtovatelné úkoly** řádku smlouvy aktualizací pole **Typ fakturace** v podmřížce Úkoly řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="3967f-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="3967f-127">Alternativně můžete aktualizovat pole **Typ fakturace** v nastavení fakturace úkolu projektu, které zobrazuje řádky smluv přidružené k úkolu.</span><span class="sxs-lookup"><span data-stu-id="3967f-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="3967f-128">Nastavení role jako účtovatelné nebo neúčtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="3967f-129">Role může být účtovatelná nebo neúčtovatelná na konkrétním řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="3967f-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="3967f-130">Typ fakturace role lze nakonfigurovat na kartě **Účtovatelné role** řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="3967f-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="3967f-131">Chcete-li to provést, aktualizujte pole **Typ fakturace** v podmřížce **Účtovatelné role**.</span><span class="sxs-lookup"><span data-stu-id="3967f-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="3967f-132">Nastavení kategorie transakcí jako účtovatelné nebo neúčtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="3967f-133">Kategorie transakcí může být účtovatelná nebo neúčtovatelná na konkrétním řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="3967f-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="3967f-134">Typ fakturace transakce lze nakonfigurovat na kartě **Účtovatelné kategorie** řádku smlouvy na základě projektu.</span><span class="sxs-lookup"><span data-stu-id="3967f-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="3967f-135">Chcete-li to provést, aktualizujte pole **Typ fakturace** v podmřížce **Účtovatelné kategorie**.</span><span class="sxs-lookup"><span data-stu-id="3967f-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="3967f-136">Vyřešení účtovatelnosti</span><span class="sxs-lookup"><span data-stu-id="3967f-136">Resolve chargeability</span></span>

<span data-ttu-id="3967f-137">Vytvořený odhad nebo skutečná hodnota pro čas bude považována za účtovatelnou, pouze pokud:</span><span class="sxs-lookup"><span data-stu-id="3967f-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="3967f-138">**Čas** je uveden v řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="3967f-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="3967f-139">**Role** je nakonfigurována jako účtovatelná na řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="3967f-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="3967f-140">**Zahrnuté úkoly** je nastaveno na **Vybrané úkoly** na řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="3967f-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="3967f-141">Pokud jsou tyto tři věci pravdivé, úkol je také nakonfigurován jako účtovatelný.</span><span class="sxs-lookup"><span data-stu-id="3967f-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="3967f-142">Vytvořený odhad nebo skutečná hodnota pro výdaj bude považována za účtovatelnou, pouze pokud:</span><span class="sxs-lookup"><span data-stu-id="3967f-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="3967f-143">**Výdaj** je uveden v řádku smlouvy</span><span class="sxs-lookup"><span data-stu-id="3967f-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="3967f-144">**Kategorie transakce** je nakonfigurována jako účtovatelná na řádku smlouvy</span><span class="sxs-lookup"><span data-stu-id="3967f-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="3967f-145">**Zahrnuté úkoly** je nastaveno na **Vybraný úkol** na řádku smlouvy</span><span class="sxs-lookup"><span data-stu-id="3967f-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="3967f-146">Pokud jsou tyto tři věci pravdivé, **úkol** je také nakonfigurován jako účtovatelný.</span><span class="sxs-lookup"><span data-stu-id="3967f-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="3967f-147">Vytvořený odhad nebo skutečná hodnota pro materiál bude považována za účtovatelnou, pouze pokud:</span><span class="sxs-lookup"><span data-stu-id="3967f-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="3967f-148">**Materiály** je uvedeno v řádku smlouvy</span><span class="sxs-lookup"><span data-stu-id="3967f-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="3967f-149">**Zahrnuté úkoly** je nastaveno na **Vybrané úkoly** na řádku smlouvy</span><span class="sxs-lookup"><span data-stu-id="3967f-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="3967f-150">Pokud jsou tyto dvě věci pravdivé, **úkol** je také nakonfigurován jako účtovatelný.</span><span class="sxs-lookup"><span data-stu-id="3967f-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="3967f-151">
                    <strong>Zahrnuje čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="3967f-152">
                    <strong>Zahrnuje výdaj</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="3967f-153">
                    <strong>Zahrnuje materiály</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="3967f-154">
                    <strong>Zahrnuté úkoly</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3967f-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="3967f-156">
                    <strong>Kategorie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3967f-157">
                    <strong>Úkol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="3967f-158">
                    <strong>Dopad účtovatelnosti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-159">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3967f-160">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3967f-161">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3967f-162">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="3967f-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-163">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-164">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-165">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="3967f-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3967f-166">Skutečná fakturace na čas: <strong>Účtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-167">Typ fakturace při skutečných výdajích: <strong>Účtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-168">Typ fakturace na skutečnou hodnotu materiálu: <strong>účtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-169">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3967f-170">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3967f-171">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3967f-172">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="3967f-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-173">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-174">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-175">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3967f-176">Skutečná fakturace na čas: <strong>Účtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-177">Typ fakturace při skutečných výdajích: <strong>Účtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-178">Typ fakturace na skutečnou hodnotu materiálu: <strong>účtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-179">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3967f-180">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3967f-181">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3967f-182">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="3967f-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3967f-183">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-184">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-185">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3967f-186">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-187">Typ fakturace při skutečných výdajích: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3967f-188">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="3967f-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-189">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3967f-190">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3967f-191">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3967f-192">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="3967f-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-193">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-194">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3967f-195">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3967f-196">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-197">Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-198">Typ fakturace při skutečném materiálu: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-199">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3967f-200">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3967f-201">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3967f-202">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="3967f-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3967f-203">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-204">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3967f-205">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3967f-206">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-207">Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-208">Typ fakturace při skutečném materiálu: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-209">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3967f-210">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3967f-211">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3967f-212">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="3967f-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3967f-213">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="3967f-214">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-215">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3967f-216">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-217">Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-218">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="3967f-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="3967f-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3967f-220">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3967f-221">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3967f-222">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="3967f-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-223">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="3967f-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="3967f-224">
                    <strong>Účtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-225">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="3967f-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3967f-226">Skutečná fakturace na čas: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-227">Typ fakturace při skutečných výdajích: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3967f-228">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="3967f-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="3967f-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3967f-230">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3967f-231">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3967f-232">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="3967f-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-233">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="3967f-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="3967f-234">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-235">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="3967f-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3967f-236">Skutečná fakturace na čas: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-237">Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-238">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="3967f-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-239">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="3967f-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3967f-241">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3967f-242">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="3967f-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-243">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-244">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="3967f-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-245">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="3967f-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3967f-246">Skutečná fakturace na čas: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3967f-247">Typ fakturace při skutečných výdajích: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-248">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="3967f-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-249">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="3967f-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3967f-251">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3967f-252">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="3967f-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3967f-253">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-254">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="3967f-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-255">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="3967f-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3967f-256">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-257">Typ fakturace při skutečných výdajích: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-258">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="3967f-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-259">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3967f-260">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="3967f-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3967f-262">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="3967f-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-263">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-264">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-265">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="3967f-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3967f-266">Skutečná fakturace na čas: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3967f-267">Typ fakturace při skutečných výdajích: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="3967f-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3967f-268">Typ fakturace při skutečném materiálu: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3967f-269">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3967f-270">Ano</span><span class="sxs-lookup"><span data-stu-id="3967f-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="3967f-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3967f-272">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="3967f-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3967f-273">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="3967f-274">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3967f-275">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="3967f-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3967f-276">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-277">Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="3967f-278">Typ fakturace při skutečném materiálu: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3967f-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
