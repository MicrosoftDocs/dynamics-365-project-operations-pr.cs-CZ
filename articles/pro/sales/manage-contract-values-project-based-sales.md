---
title: Přehled řádků smlouvy založené na projektu
description: Tohle téma poskytuje informace o práci s řádky smlouvy na základě projektu.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369908"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="fed40-103">Přehled řádků smlouvy založené na projektu</span><span class="sxs-lookup"><span data-stu-id="fed40-103">Project-based contract lines overview</span></span>

<span data-ttu-id="fed40-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="fed40-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fed40-105">Řádky smlouvy na základě projektu v Dynamics 365 Project Operations jsou navrženy tak, aby obsahovaly odhad a řešení fakturace pro konkrétní součásti projektové práce na aktivitě.</span><span class="sxs-lookup"><span data-stu-id="fed40-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="fed40-106">Struktura řádku smlouvy na základě projektu je rozšířena pro odhady projektu a scénáře fakturace o následující koncepty:</span><span class="sxs-lookup"><span data-stu-id="fed40-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="fed40-107">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="fed40-107">Billing method</span></span>
- <span data-ttu-id="fed40-108">Projekt a mapování úkolů</span><span class="sxs-lookup"><span data-stu-id="fed40-108">Project and task mapping</span></span>
- <span data-ttu-id="fed40-109">Zahrnuté třídy transakcí</span><span class="sxs-lookup"><span data-stu-id="fed40-109">Included transaction classes</span></span>
- <span data-ttu-id="fed40-110">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="fed40-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="fed40-111">Nastavení účtovatelnosti</span><span class="sxs-lookup"><span data-stu-id="fed40-111">Chargeability setup</span></span>
- <span data-ttu-id="fed40-112">Odhady pomocí podrobností řádku smlouvy</span><span class="sxs-lookup"><span data-stu-id="fed40-112">Estimates using contract line details</span></span>
- <span data-ttu-id="fed40-113">Zákazníci řádku smlouvy</span><span class="sxs-lookup"><span data-stu-id="fed40-113">Contract line customers</span></span>

<span data-ttu-id="fed40-114">Následující tabulka obsahuje pole na kartě **Obecné** pro řádky smlouvy založené na projektu, které pomáhají připravit základ pro podrobný odhad a řešení fakturace pro projektovou práci.</span><span class="sxs-lookup"><span data-stu-id="fed40-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="fed40-115">Pole</span><span class="sxs-lookup"><span data-stu-id="fed40-115">Field</span></span> | <span data-ttu-id="fed40-116">Popis</span><span class="sxs-lookup"><span data-stu-id="fed40-116">Description</span></span> | <span data-ttu-id="fed40-117">Dopad na následné složky</span><span class="sxs-lookup"><span data-stu-id="fed40-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fed40-118">**Jméno**</span><span class="sxs-lookup"><span data-stu-id="fed40-118">**Name**</span></span> | <span data-ttu-id="fed40-119">Název řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fed40-119">Name of the contract line.</span></span> <span data-ttu-id="fed40-120">Tento název označuje diskrétní složku smlouvy, která se odhaduje.</span><span class="sxs-lookup"><span data-stu-id="fed40-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="fed40-121">U smlouvy projektu vytvořené z nabídky je tato hodnota zkopírována z odpovídající hodnoty řádku nabídky na základě projektu.</span><span class="sxs-lookup"><span data-stu-id="fed40-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="fed40-122">Tento název je zkopírován do řádku faktury projektu, který je vytvořen z tohoto řádku smlouvy při vytváření faktury.</span><span class="sxs-lookup"><span data-stu-id="fed40-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="fed40-123">**Způsob fakturace**</span><span class="sxs-lookup"><span data-stu-id="fed40-123">**Billing Method**</span></span> | <span data-ttu-id="fed40-124">U smlouvy projektu vytvořené z nabídky je tato hodnota zkopírována z odpovídajícího pole na řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="fed40-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="fed40-125">Toto je sada možností, která představuje dva hlavní smluvní modely podporované v Project Operations:</span><span class="sxs-lookup"><span data-stu-id="fed40-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="fed40-126">- **Pevná cena**</span><span class="sxs-lookup"><span data-stu-id="fed40-126">- **Fixed Price**</span></span></br><span data-ttu-id="fed40-127">- **Čas a materiál**</span><span class="sxs-lookup"><span data-stu-id="fed40-127">- **Time and Material**</span></span> | <span data-ttu-id="fed40-128">Na základě způsobu fakturace odkazované řádky smlouvy bude zpracována samotná transakce.</span><span class="sxs-lookup"><span data-stu-id="fed40-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="fed40-129">Pokud má řádka smlouvy odkazovaná skutečnou hodnotou metodu fakturace času a materiálu, vytvoří se záznamy skutečných nákladů a nefakturovaného prodeje.</span><span class="sxs-lookup"><span data-stu-id="fed40-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="fed40-130">Pokud má řádek smlouvy, na který odkazuje skutečná hodnota, způsob fakturace s pevnou cenou, vytvoří se pouze skutečné náklady.</span><span class="sxs-lookup"><span data-stu-id="fed40-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="fed40-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="fed40-131">**Project**</span></span> | <span data-ttu-id="fed40-132">Toto pole použijte k identifikaci projektu, který bude použit k provedení práce na této aktivitě.</span><span class="sxs-lookup"><span data-stu-id="fed40-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="fed40-133">Tato hodnota bude použita ve spojení se **Zahrnutými úkoly** a **Zahrnutými třídami transakcí** k vyřešení odkazu na řádek smlouvy na záznamu řádku skutečné nebo odhadované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="fed40-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="fed40-134">**Zahrnuté úkoly**</span><span class="sxs-lookup"><span data-stu-id="fed40-134">**Included Tasks**</span></span> | <span data-ttu-id="fed40-135">Označuje, zda tento řádek smlouvy zahrnuje všechny projektové úkoly pro vybraný projekt nebo pouze podmnožinu úkolů.</span><span class="sxs-lookup"><span data-stu-id="fed40-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="fed40-136">Jedná se o sadu možností s následujícími možnými hodnotami:</span><span class="sxs-lookup"><span data-stu-id="fed40-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="fed40-137">- **Všechny projektové úkoly**</span><span class="sxs-lookup"><span data-stu-id="fed40-137">- **All Project Tasks**</span></span></br><span data-ttu-id="fed40-138">- **Pouze vybrané úkoly projektu**.</span><span class="sxs-lookup"><span data-stu-id="fed40-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="fed40-139">Prázdná hodnota v tomto poli se rovná výběru **Všechny projektové úkoly**.</span><span class="sxs-lookup"><span data-stu-id="fed40-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="fed40-140">Pokud je vybrána možnost **Pouze vybrané úkoly**, můžete vybrat konkrétní úkoly a přidružit je k tomuto řádku smlouvy na kartě **Nastavení účtování úkolů** na stránce **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="fed40-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="fed40-141">Tato hodnota se použije v souvislosti s poli **Projekt** a **Zahrnuté třídy transakcí** ke čtení odkazu na řádek smlouvy v záznamu skutečného nebo odhadovaného řádku.</span><span class="sxs-lookup"><span data-stu-id="fed40-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="fed40-142">**Zahrnout čas**</span><span class="sxs-lookup"><span data-stu-id="fed40-142">**Include Time**</span></span> | <span data-ttu-id="fed40-143">Hodnota **Ano**/**Ne** označuje, zda budou do na tomto řádku smlouvy zahrnuty časové transakce nebo náklady práce na vybraném projektu.</span><span class="sxs-lookup"><span data-stu-id="fed40-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="fed40-144">Hodnota **Ne** označuje, že časové transakce nebo mzdové náklady nebudou zahrnuty do tohoto řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fed40-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="fed40-145">Hodnota **Ano**, znamená že ano.</span><span class="sxs-lookup"><span data-stu-id="fed40-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="fed40-146">Tato hodnota se používá ve spojení s projektem k vyřešení odkazu na řádek smlouvy na záznamu řádku skutečné nebo odhadované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="fed40-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="fed40-147">**Zahrnout výdaj**</span><span class="sxs-lookup"><span data-stu-id="fed40-147">**Include Expense**</span></span> | <span data-ttu-id="fed40-148">Hodnota **Ano**/**Ne** označuje, zda budou do tohoto řádku smlouvy zahrnuty náklady výdajů na vybraném projektu.</span><span class="sxs-lookup"><span data-stu-id="fed40-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="fed40-149">Hodnota **Ne** označuje, že výdajové náklady nebudou zahrnuty do tohoto řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fed40-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="fed40-150">Hodnota **Ano**, znamená že ano.</span><span class="sxs-lookup"><span data-stu-id="fed40-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="fed40-151">Tato hodnota se používá ve spojení s projektem k vyřešení odkazu na řádek smlouvy na záznamu řádku skutečné nebo odhadované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="fed40-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="fed40-152">**Zahrnout materiály**</span><span class="sxs-lookup"><span data-stu-id="fed40-152">**Include Materials**</span></span> | <span data-ttu-id="fed40-153">Hodnota **Ano**/**Ne** označuje, zda budou do tohoto řádku smlouvy zahrnuty náklady materiálu na vybraném projektu.</span><span class="sxs-lookup"><span data-stu-id="fed40-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="fed40-154">Hodnota **Ne** označuje, že nebudou do řádku smlouvy zahrnuty náklady na materiál.</span><span class="sxs-lookup"><span data-stu-id="fed40-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="fed40-155">Hodnota **Ano**, znamená že ano.</span><span class="sxs-lookup"><span data-stu-id="fed40-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="fed40-156">Tato hodnota se používá ve spojení s projektem k vyřešení odkazu na řádek smlouvy na záznamu řádku skutečné nebo odhadované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="fed40-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="fed40-157">**Zahrnout poplatek**</span><span class="sxs-lookup"><span data-stu-id="fed40-157">**Include Fee**</span></span> | <span data-ttu-id="fed40-158">Hodnota **Ano**/**Ne** označuje, zda budou do tohoto řádku smlouvy zahrnuty poplatky na vybraném projektu.</span><span class="sxs-lookup"><span data-stu-id="fed40-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="fed40-159">Hodnota **Ne** označuje, že poplatky nebudou zahrnuty do tohoto řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fed40-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="fed40-160">Hodnota **Ano**, znamená že ano.</span><span class="sxs-lookup"><span data-stu-id="fed40-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="fed40-161">Tato hodnota se používá ve spojení s projektem k vyřešení odkazu na řádek smlouvy na záznamu řádku skutečné nebo odhadované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="fed40-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="fed40-162">**Nasmlouvaná částka**</span><span class="sxs-lookup"><span data-stu-id="fed40-162">**Contracted Amount**</span></span> | <span data-ttu-id="fed40-163">Na řádku smlouvy s pevnou cenou je tato částka dohodnutá hodnota, která bude zákazníkovi fakturována za všechny součásti práce přidružené k tomuto řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fed40-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="fed40-164">Na řádku smlouvy času a materiálu je tato částka odhadnutá hodnota, co bude zákazníkovi fakturováno za všechny součásti práce přidružené k tomuto řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fed40-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="fed40-165">U smlouvy projektu vytvořené z nabídky je tato hodnota zkopírována z odpovídajícího pole na řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="fed40-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="fed40-166">Pokud má řádek smlouvy na základě projektu podrobnosti, je toto pole uzamčeno pro úpravy a shrnuto z částky v podrobnostech řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fed40-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="fed40-167">Pokud řádek smlouvy obsahuje podrobnosti, lze tuto hodnotu upravit změnou částek v podrobnostech řádku.</span><span class="sxs-lookup"><span data-stu-id="fed40-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="fed40-168">Na řádku smlouvy s pevnou cenou se tato hodnota používá ke generování částky před daní z milníků periodické fakturace.</span><span class="sxs-lookup"><span data-stu-id="fed40-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="fed40-169">**Odhad daně**</span><span class="sxs-lookup"><span data-stu-id="fed40-169">**Estimated Tax**</span></span> | <span data-ttu-id="fed40-170">Uživatel může toto pole upravit a zadat odhadovanou částku daně na řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fed40-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="fed40-171">Pokud má řádek smlouvy na základě projektu podrobnosti, je toto pole uzamčeno pro úpravy a shrnuto z částky daně v podrobnostech řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fed40-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="fed40-172">Pokud řádek smlouvy obsahuje podrobnosti, lze tuto hodnotu upravit změnou částek daně v podrobnostech řádku.</span><span class="sxs-lookup"><span data-stu-id="fed40-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="fed40-173">Na řádku smlouvy s pevnou cenou se tato hodnota používá ke generování daně z milníků periodické fakturace.</span><span class="sxs-lookup"><span data-stu-id="fed40-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="fed40-174">**Nasmlouvaná částka včetně daně**</span><span class="sxs-lookup"><span data-stu-id="fed40-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="fed40-175">Řádka smlouvy s částkou včetně daně</span><span class="sxs-lookup"><span data-stu-id="fed40-175">The contract line amount after tax.</span></span> <span data-ttu-id="fed40-176">Toto pole je jen pro čtení a počítá se jako **Nasmlouvaná částka + daň**.</span><span class="sxs-lookup"><span data-stu-id="fed40-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="fed40-177">Na řádku smlouvy s pevnou cenou se tato hodnota používá ke generování milníků periodické fakturace.</span><span class="sxs-lookup"><span data-stu-id="fed40-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="fed40-178">**Nepřekročitelný limit**</span><span class="sxs-lookup"><span data-stu-id="fed40-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="fed40-179">Uživatel může toto pole upravit a je k dispozici pouze na řádcích smlouvy založené na projektu se způsobem fakturace nastaveným na čas a materiál.</span><span class="sxs-lookup"><span data-stu-id="fed40-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="fed40-180">Uživatel může toto pole upravit.</span><span class="sxs-lookup"><span data-stu-id="fed40-180">The user can edit this field.</span></span> <span data-ttu-id="fed40-181">Když skutečná hodnota času a materiálu odkazuje na tento řádek smlouvy pro čas a materiál, skutečná částka je vyhodnocena vůči nepřekročitelnému limitu na tomto řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fed40-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="fed40-182">Toto vyhodnocení je dokončeno po započítání již utracených a potvrzených částek.</span><span class="sxs-lookup"><span data-stu-id="fed40-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="fed40-183">**Rozpočet zákazníka**</span><span class="sxs-lookup"><span data-stu-id="fed40-183">**Customer Budget**</span></span> | <span data-ttu-id="fed40-184">Toto pole je upravitelné a je zkopírováno z odpovídajícího pole na řádku nabídky, pokud byla smlouva vytvořena z nabídky.</span><span class="sxs-lookup"><span data-stu-id="fed40-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="fed40-185">Toto pole slouží pouze pro informaci a nemá žádný následný význam.</span><span class="sxs-lookup"><span data-stu-id="fed40-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="fed40-186">Pravidla ověření pro možnosti na kartě Obecné pro řádky smlouvy založené na projektu</span><span class="sxs-lookup"><span data-stu-id="fed40-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="fed40-187">Pravidlo 1: Pokud je pole **Zahrnuté úkoly** prázdné nebo nastavené na **Všechny projektové úkoly**, všechny projektové úkoly jsou zahrnuty na řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="fed40-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="fed40-188">Pravidlo 2: Když je pole **Zahrnuté úkoly** prázdné nebo explicitně nastaveno na **Všechny projektové úkoly**, projekt a určitou třídu transakcí lze zahrnout pouze do jedné řádky smlouvy na základě projektu.</span><span class="sxs-lookup"><span data-stu-id="fed40-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="fed40-189">Pravidlo 3: Když je pole **Zahrnuté úkoly** nastaveno na **Pouze vybrané projektové úkoly**, projekt a určitou třídu transakcí lze zahrnout pouze do více řádek smlouvy na základě projektu.</span><span class="sxs-lookup"><span data-stu-id="fed40-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="fed40-190">
                    <strong>Smlouva</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fed40-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fed40-191">
                    <strong>Řádek smlouvy</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fed40-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fed40-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fed40-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="fed40-193">
                    <strong>Zahrnuté úkoly</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fed40-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="fed40-194">
                    <strong>Zahrnout čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fed40-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="fed40-195">
                    <strong>Zahrnout výdaj</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fed40-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fed40-196">
                    <strong>Zahrnout materiály</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fed40-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fed40-197">
                    <strong>Zahrnout</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fed40-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="fed40-198">
                    <strong>Poplatek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fed40-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="fed40-199">
                    <strong>Platné / Neplatné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fed40-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="fed40-200">
                    <strong>Důvod</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fed40-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fed40-201">S1</span><span class="sxs-lookup"><span data-stu-id="fed40-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fed40-202">ŘS1</span><span class="sxs-lookup"><span data-stu-id="fed40-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-203">O1</span><span class="sxs-lookup"><span data-stu-id="fed40-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fed40-204">prázdnou</span><span class="sxs-lookup"><span data-stu-id="fed40-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-205">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-206">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-207">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-208">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fed40-209">Neplatný</span><span class="sxs-lookup"><span data-stu-id="fed40-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fed40-210">Porušení pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="fed40-210">Violation of Rule #2.</span></span> <span data-ttu-id="fed40-211">Čas, náklady, materiály a poplatky za projekt P1 jsou zahrnuty v řádcích nabídky ŘN1 i ŘN2.</span><span class="sxs-lookup"><span data-stu-id="fed40-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fed40-212">S1</span><span class="sxs-lookup"><span data-stu-id="fed40-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fed40-213">ŘS2</span><span class="sxs-lookup"><span data-stu-id="fed40-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-214">O1</span><span class="sxs-lookup"><span data-stu-id="fed40-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fed40-215">prázdnou</span><span class="sxs-lookup"><span data-stu-id="fed40-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-216">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-217">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-218">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-219">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fed40-220">S1</span><span class="sxs-lookup"><span data-stu-id="fed40-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fed40-221">ŘS1</span><span class="sxs-lookup"><span data-stu-id="fed40-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-222">O1</span><span class="sxs-lookup"><span data-stu-id="fed40-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fed40-223">prázdnou</span><span class="sxs-lookup"><span data-stu-id="fed40-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-224">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-225">No</span><span class="sxs-lookup"><span data-stu-id="fed40-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-226">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-227">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fed40-228">Neplatný</span><span class="sxs-lookup"><span data-stu-id="fed40-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fed40-229">Porušení pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="fed40-229">Violation of Rule #2.</span></span> <span data-ttu-id="fed40-230">Čas, materiály a poplatky za projekt P1 jsou zahrnuty v řádcích nabídky ŘN1 i ŘN2.</span><span class="sxs-lookup"><span data-stu-id="fed40-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fed40-231">S1</span><span class="sxs-lookup"><span data-stu-id="fed40-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fed40-232">ŘS2</span><span class="sxs-lookup"><span data-stu-id="fed40-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-233">O1</span><span class="sxs-lookup"><span data-stu-id="fed40-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fed40-234">prázdnou</span><span class="sxs-lookup"><span data-stu-id="fed40-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-235">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-236">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-237">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-238">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fed40-239">S1</span><span class="sxs-lookup"><span data-stu-id="fed40-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fed40-240">ŘS1</span><span class="sxs-lookup"><span data-stu-id="fed40-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-241">O1</span><span class="sxs-lookup"><span data-stu-id="fed40-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fed40-242">prázdnou</span><span class="sxs-lookup"><span data-stu-id="fed40-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-243">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-244">No</span><span class="sxs-lookup"><span data-stu-id="fed40-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-245">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-246">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fed40-247">Platné</span><span class="sxs-lookup"><span data-stu-id="fed40-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fed40-248">Čas, materiály a poplatky za projekt P1 jsou zahrnuty na ŘN1.</span><span class="sxs-lookup"><span data-stu-id="fed40-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="fed40-249">Výdaje v projektu P1 jsou zahrnuty na řádku ŘS2.</span><span class="sxs-lookup"><span data-stu-id="fed40-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="fed40-250">Žádné překrývání toho, co je zahrnuto na každém řádku smlouvy, a proto je zadání platné.</span><span class="sxs-lookup"><span data-stu-id="fed40-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fed40-251">S1</span><span class="sxs-lookup"><span data-stu-id="fed40-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fed40-252">ŘS2</span><span class="sxs-lookup"><span data-stu-id="fed40-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-253">O1</span><span class="sxs-lookup"><span data-stu-id="fed40-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fed40-254">prázdnou</span><span class="sxs-lookup"><span data-stu-id="fed40-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-255">No</span><span class="sxs-lookup"><span data-stu-id="fed40-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-256">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-257">No</span><span class="sxs-lookup"><span data-stu-id="fed40-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-258">No</span><span class="sxs-lookup"><span data-stu-id="fed40-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fed40-259">S1</span><span class="sxs-lookup"><span data-stu-id="fed40-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fed40-260">ŘS1</span><span class="sxs-lookup"><span data-stu-id="fed40-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-261">O1</span><span class="sxs-lookup"><span data-stu-id="fed40-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fed40-262">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="fed40-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-263">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-264">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-265">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-266">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fed40-267">Neplatný</span><span class="sxs-lookup"><span data-stu-id="fed40-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fed40-268">Porušení pravidla č. 2</span><span class="sxs-lookup"><span data-stu-id="fed40-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="fed40-269">Č1 zahrnuje čas, materiály, výdaje a poplatky za podmnožinu úkolů v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="fed40-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fed40-270">ŘN2 zahrnuje čas, materiály, výdaje a poplatky za celý projekt P1, a proto se překrývá s tím, co je zahrnuto v S1.</span><span class="sxs-lookup"><span data-stu-id="fed40-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fed40-271">S1</span><span class="sxs-lookup"><span data-stu-id="fed40-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fed40-272">ŘS2</span><span class="sxs-lookup"><span data-stu-id="fed40-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-273">O1</span><span class="sxs-lookup"><span data-stu-id="fed40-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fed40-274">prázdnou</span><span class="sxs-lookup"><span data-stu-id="fed40-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-275">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-276">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-277">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-278">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fed40-279">S1</span><span class="sxs-lookup"><span data-stu-id="fed40-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fed40-280">ŘS1</span><span class="sxs-lookup"><span data-stu-id="fed40-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-281">O1</span><span class="sxs-lookup"><span data-stu-id="fed40-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fed40-282">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="fed40-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-283">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-284">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-285">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-286">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fed40-287">Platné</span><span class="sxs-lookup"><span data-stu-id="fed40-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fed40-288">Podle pravidla č. 3</span><span class="sxs-lookup"><span data-stu-id="fed40-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="fed40-289">Č1 zahrnuje čas, výdaje, materiály, výdaje a poplatky za podmnožinu úkolů v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="fed40-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fed40-290">ŘN2 zahrnuje čas, výdaje, materiály a poplatky za podmnožinu úkolů v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="fed40-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fed40-291">Jediná další validace je kolem podmnožiny úkolů na ŘN1, která se liší od podmnožiny úkolů na ŘN2, aby se zajistilo, že nedojde k překrývání.</span><span class="sxs-lookup"><span data-stu-id="fed40-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="fed40-292">Toto provádí systém, když jsou přidruženy úkoly.</span><span class="sxs-lookup"><span data-stu-id="fed40-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="fed40-293">S1</span><span class="sxs-lookup"><span data-stu-id="fed40-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fed40-294">ŘS2</span><span class="sxs-lookup"><span data-stu-id="fed40-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-295">O1</span><span class="sxs-lookup"><span data-stu-id="fed40-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="fed40-296">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="fed40-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-297">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fed40-298">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-299">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fed40-300">Ano</span><span class="sxs-lookup"><span data-stu-id="fed40-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
