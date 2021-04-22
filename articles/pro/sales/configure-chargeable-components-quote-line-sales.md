---
title: Konfigurace účtovatelných součásti řádku nabídky
description: Tento téma poskytuje informace o nastavení účtovatelných a neúčtovatelných komponent na řádku nabídky založeného na projektu.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858285"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="de79a-103">Konfigurace účtovatelných součásti řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="de79a-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="de79a-104">_**Platí pro:** omezené nasazení – dohoda o pro forma fakturaci, Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="de79a-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="de79a-105">Řádek nabídky na základě projektu má koncept *zahrnutých* komponent a *účtovatelných* komponent.</span><span class="sxs-lookup"><span data-stu-id="de79a-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="de79a-106">Zahrnuté součásti podléhají:</span><span class="sxs-lookup"><span data-stu-id="de79a-106">Included components are subject to:</span></span>

  - <span data-ttu-id="de79a-107">Způsob fakturace a rozdělení zákazníků</span><span class="sxs-lookup"><span data-stu-id="de79a-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="de79a-108">Nepřekročitelné limity</span><span class="sxs-lookup"><span data-stu-id="de79a-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="de79a-109">Nastavení frekvence faktur definované na řádku nabídky na základě projektu</span><span class="sxs-lookup"><span data-stu-id="de79a-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="de79a-110">Podskupinu zahrnutých komponent lze označit jako účtovatelnou pomocí pole **Typ fakturace**.</span><span class="sxs-lookup"><span data-stu-id="de79a-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="de79a-111">Pole **Typ fakturace** je sada možností, která umožňuje následující hodnoty v kontextu řádku nabídky:</span><span class="sxs-lookup"><span data-stu-id="de79a-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="de79a-112">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-112">Chargeable</span></span>
  - <span data-ttu-id="de79a-113">Neúčtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-113">Non-chargeable</span></span>

<span data-ttu-id="de79a-114">Účtovatelné komponenty lze definovat na úkolech, rolích a kategoriích transakcí.</span><span class="sxs-lookup"><span data-stu-id="de79a-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="de79a-115">Účtovatelnost je definována na úkolech pro řádek nabídky a platí pro všechny třídy transakcí zahrnutých na řádku.</span><span class="sxs-lookup"><span data-stu-id="de79a-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="de79a-116">Pokud je pole **Zahrnout úkoly** nastaveno na **Celý projekt** nebo ponecháno prázdné, karta **Účtovatelné úlohy** není k dispozici.</span><span class="sxs-lookup"><span data-stu-id="de79a-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="de79a-117">Účtovatelnost definovaná pro role pro řádek nabídky se vztahuje pouze na třídu transakcí **Čas**.</span><span class="sxs-lookup"><span data-stu-id="de79a-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="de79a-118">Pokud je pole **Zahrnout čas** na řádku nabídky projektu nastaveno na **Ne**, karta **Účtovatelné role** není k dispozici.</span><span class="sxs-lookup"><span data-stu-id="de79a-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="de79a-119">Účtovatelnost definovaná na kategoriích transakcí pro řádek nabídky se vztahuje pouze na třídu transakcí **Výdaj**.</span><span class="sxs-lookup"><span data-stu-id="de79a-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="de79a-120">Pokud je pole **Zahrnout výdaje** na řádku nabídky projektu nastaveno na **Ne**, karta **Účtovatelné kategorie** není k dispozici.</span><span class="sxs-lookup"><span data-stu-id="de79a-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="de79a-121">Nastavení úkolu projektu jako účtovatelného nebo neúčtovatelného</span><span class="sxs-lookup"><span data-stu-id="de79a-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="de79a-122">Úkol projektu může být účtovatelný nebo neúčtovatelný v kontextu konkrétního řádku nabídky podle projektu, což umožňuje následující nastavení.</span><span class="sxs-lookup"><span data-stu-id="de79a-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="de79a-123">Pokud řádek nabídky na základě projektu zahrnuje **Čas** a úkol **T1**, úkol je přidružen k řádku nabídky jako účtovatelný.</span><span class="sxs-lookup"><span data-stu-id="de79a-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="de79a-124">Pokud existuje druhý řádek nabídky , který zahrnuje **Výdaje**, můžete úkol **T1** na řádku nabídky asociovat jako neúčtovatelný.</span><span class="sxs-lookup"><span data-stu-id="de79a-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="de79a-125">Výsledkem je, že veškerý čas zaznamenaný na úkolu je účtovatelný a všechny náklady zaznamenané na úkolu jsou neúčtovatelné.</span><span class="sxs-lookup"><span data-stu-id="de79a-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="de79a-126">Typ fakturace úkolu lze nakonfigurovat na kartě **Účtovatelné úkoly** řádku nabídky založeného na projektu aktualizací pole **Typ fakturace** v podmřížce **Úkoly řádku nabídky**.</span><span class="sxs-lookup"><span data-stu-id="de79a-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="de79a-127">Alternativně můžete aktualizovat typ fakturace pro projektový úkol v poli **Typ fakturace** v podmřížce v nastavení fakturace úkolu projektu, které zobrazuje řádky nabídek přidružené k úkolu.</span><span class="sxs-lookup"><span data-stu-id="de79a-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="de79a-128">Nastavení role jako účtovatelné nebo neúčtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="de79a-129">Role může být účtovatelná nebo neúčtovatelná v kontextu konkrétního řádku nabídky založeného na projektu.</span><span class="sxs-lookup"><span data-stu-id="de79a-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="de79a-130">Typ fakturace role lze nakonfigurovat na kartě **Účtovatelné role** řádku nabídky aktualizací pole **Typ fakturace** v podmřížce **Účtovatelné role**.</span><span class="sxs-lookup"><span data-stu-id="de79a-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="de79a-131">Nastavení kategorie transakcí jako účtovatelné nebo neúčtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="de79a-132">Kategorie transakcí může být účtovatelná nebo neúčtovatelná na konkrétním řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="de79a-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="de79a-133">Typ fakturace transakce lze nakonfigurovat na kartě **Účtovatelné kategorie** řádku nabídky aktualizací pole **Typ fakturace** v podmřížce **Účtovatelné kategorie**.</span><span class="sxs-lookup"><span data-stu-id="de79a-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="de79a-134">Vyřešení účtovatelnosti</span><span class="sxs-lookup"><span data-stu-id="de79a-134">Resolve chargeability</span></span>
<span data-ttu-id="de79a-135">Vytvořený odhad nebo skutečná hodnota pro čas bude považována za účtovatelnou, pouze pokud:</span><span class="sxs-lookup"><span data-stu-id="de79a-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="de79a-136">**Čas** je uveden v řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="de79a-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="de79a-137">**Role** je nakonfigurována jako účtovatelná na řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="de79a-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="de79a-138">**Zahrnuté úkoly** je nastaveno na **Vybrané úkoly** na řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="de79a-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="de79a-139">Pokud jsou tyto tři věci pravdivé, **Úkol** je také nakonfigurován jako účtovatelný.</span><span class="sxs-lookup"><span data-stu-id="de79a-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="de79a-140">Vytvořený odhad nebo skutečná hodnota pro výdaj bude považována za účtovatelnou, pouze pokud:</span><span class="sxs-lookup"><span data-stu-id="de79a-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="de79a-141">**Výdaj** je uveden v řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="de79a-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="de79a-142">**Kategorie transakce** je nakonfigurována jako účtovatelná na řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="de79a-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="de79a-143">**Zahrnuté úkoly** je nastaveno na **Vybrané úkoly** na řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="de79a-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="de79a-144">Pokud jsou tyto tři věci pravdivé, **Úkol** je také nakonfigurován jako účtovatelný.</span><span class="sxs-lookup"><span data-stu-id="de79a-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="de79a-145">Vytvořený odhad nebo skutečná hodnota pro materiál bude považována za účtovatelnou, pouze pokud:</span><span class="sxs-lookup"><span data-stu-id="de79a-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="de79a-146">**Materiály** je uvedeno v řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="de79a-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="de79a-147">**Zahrnuté úkoly** je nastaveno na **Vybrané úkoly** na řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="de79a-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="de79a-148">Pokud jsou tyto dvě věci pravdivé, **Úkol** je také nakonfigurován jako účtovatelný.</span><span class="sxs-lookup"><span data-stu-id="de79a-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="de79a-149">
                    <strong>Zahrnuje čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="de79a-150">
                    <strong>Zahrnuje výdaj</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="de79a-151">
                    <strong>Zahrnuje materiály</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="de79a-152">
                    <strong>Zahrnuté úkoly</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="de79a-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="de79a-154">
                    <strong>Kategorie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="de79a-155">
                    <strong>Úkol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="de79a-156">
                    <strong>Dopad účtovatelnosti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-157">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="de79a-158">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="de79a-159">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="de79a-160">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="de79a-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-161">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-162">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-163">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="de79a-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="de79a-164">Skutečná fakturace na čas: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="de79a-165">Typ fakturace při skutečných výdajích: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="de79a-166">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="de79a-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-167">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="de79a-168">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="de79a-169">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="de79a-170">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="de79a-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-171">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-172">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-173">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="de79a-174">Skutečná fakturace na čas: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="de79a-175">Typ fakturace při skutečných výdajích: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="de79a-176">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="de79a-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-177">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="de79a-178">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="de79a-179">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="de79a-180">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="de79a-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="de79a-181">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-182">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-183">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="de79a-184">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="de79a-185">Typ fakturace při skutečných výdajích: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="de79a-186">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="de79a-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-187">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="de79a-188">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="de79a-189">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="de79a-190">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="de79a-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-191">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-192">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="de79a-193">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="de79a-194">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="de79a-195">Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="de79a-196">Typ fakturace při skutečném materiálu: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-197">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="de79a-198">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="de79a-199">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="de79a-200">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="de79a-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="de79a-201">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-202">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="de79a-203">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="de79a-204">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="de79a-205">Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="de79a-206">Typ fakturace při skutečném materiálu: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-207">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="de79a-208">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="de79a-209">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="de79a-210">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="de79a-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="de79a-211">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="de79a-212">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-213">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="de79a-214">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="de79a-215">Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="de79a-216">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="de79a-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="de79a-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="de79a-218">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="de79a-219">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="de79a-220">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="de79a-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-221">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="de79a-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="de79a-222">
                    <strong>Účtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-223">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="de79a-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="de79a-224">Skutečná fakturace na čas: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="de79a-225">Typ fakturace při skutečných výdajích: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="de79a-226">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="de79a-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="de79a-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="de79a-228">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="de79a-229">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="de79a-230">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="de79a-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-231">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="de79a-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="de79a-232">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-233">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="de79a-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="de79a-234">Skutečná fakturace na čas: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="de79a-235">Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="de79a-236">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="de79a-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-237">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="de79a-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="de79a-239">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="de79a-240">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="de79a-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-241">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-242">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="de79a-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-243">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="de79a-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="de79a-244">Skutečná fakturace na čas: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="de79a-245">Typ fakturace při skutečných výdajích: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="de79a-246">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="de79a-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-247">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="de79a-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="de79a-249">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="de79a-250">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="de79a-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="de79a-251">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-252">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="de79a-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-253">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="de79a-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="de79a-254">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="de79a-255">Typ fakturace při skutečných výdajích: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="de79a-256">Typ fakturace na skutečnou hodnotu materiálu: účtovatelná</span><span class="sxs-lookup"><span data-stu-id="de79a-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-257">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="de79a-258">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="de79a-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="de79a-260">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="de79a-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-261">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-262">Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-263">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="de79a-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="de79a-264">Skutečná fakturace na čas: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="de79a-265">Typ fakturace při skutečných výdajích: Účtovatelné</span><span class="sxs-lookup"><span data-stu-id="de79a-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="de79a-266">Typ fakturace při skutečném materiálu: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="de79a-267">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="de79a-268">Ano</span><span class="sxs-lookup"><span data-stu-id="de79a-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="de79a-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="de79a-270">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="de79a-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="de79a-271">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="de79a-272">
                    <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="de79a-273">Nelze nastavit</span><span class="sxs-lookup"><span data-stu-id="de79a-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="de79a-274">Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="de79a-275">Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="de79a-276">Typ fakturace při skutečném materiálu: <strong>Není k dispozici</strong>
                </span><span class="sxs-lookup"><span data-stu-id="de79a-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
