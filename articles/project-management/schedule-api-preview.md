---
title: K provádění operací s entitami plánování použijte rozhraní API pro plánování projektu
description: Tento téma poskytuje informace a ukázky pro použití rozhraní API plánu projektu.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293219"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="87fd8-103">K provádění operací s entitami plánování použijte rozhraní API pro plánování projektu</span><span class="sxs-lookup"><span data-stu-id="87fd8-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="87fd8-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="87fd8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="87fd8-105">Některé nebo všechny funkce uvedené v tomto tématu jsou k dispozici jako součást vydání verze Preview.</span><span class="sxs-lookup"><span data-stu-id="87fd8-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="87fd8-106">Obsah a funkce se mohou změnit.</span><span class="sxs-lookup"><span data-stu-id="87fd8-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="87fd8-107">Entity plánování</span><span class="sxs-lookup"><span data-stu-id="87fd8-107">Scheduling entities</span></span>

<span data-ttu-id="87fd8-108">Rozhraní API plánování projektu umožňují provádět operace vytváření, aktualizace a mazání pomocí **Plánovacích entit**.</span><span class="sxs-lookup"><span data-stu-id="87fd8-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="87fd8-109">Tyto entity jsou spravovány prostřednictvím modulu Plánování v aplikaci Project for the Web.</span><span class="sxs-lookup"><span data-stu-id="87fd8-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="87fd8-110">Operace vytváření, aktualizace a odstraňování **entit plánování** byly ve starších verzích Dynamics 365 Project Operations omezeny.</span><span class="sxs-lookup"><span data-stu-id="87fd8-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="87fd8-111">Následující tabulka poskytuje úplný seznam entit plánu projektu.</span><span class="sxs-lookup"><span data-stu-id="87fd8-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="87fd8-112">Název entity</span><span class="sxs-lookup"><span data-stu-id="87fd8-112">Entity name</span></span>  | <span data-ttu-id="87fd8-113">Logický název entity</span><span class="sxs-lookup"><span data-stu-id="87fd8-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="87fd8-114">Project</span><span class="sxs-lookup"><span data-stu-id="87fd8-114">Project</span></span> | <span data-ttu-id="87fd8-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="87fd8-115">msdyn_project</span></span> |
| <span data-ttu-id="87fd8-116">Projektový úkol</span><span class="sxs-lookup"><span data-stu-id="87fd8-116">Project Task</span></span>  | <span data-ttu-id="87fd8-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="87fd8-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="87fd8-118">Závislost projektového úkolu</span><span class="sxs-lookup"><span data-stu-id="87fd8-118">Project Task Dependency</span></span>  | <span data-ttu-id="87fd8-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="87fd8-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="87fd8-120">Přiřazení zdroje</span><span class="sxs-lookup"><span data-stu-id="87fd8-120">Resource Assignment</span></span> | <span data-ttu-id="87fd8-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="87fd8-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="87fd8-122">Kbelík projektu</span><span class="sxs-lookup"><span data-stu-id="87fd8-122">Project Bucket</span></span>  | <span data-ttu-id="87fd8-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="87fd8-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="87fd8-124">Člen projektového týmu</span><span class="sxs-lookup"><span data-stu-id="87fd8-124">Project Team Member</span></span> | <span data-ttu-id="87fd8-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="87fd8-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="87fd8-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="87fd8-126">OperationSet</span></span>

<span data-ttu-id="87fd8-127">OperationSet je vzor jednotky práce, který lze použít, když musí být v rámci transakce zpracováno několik požadavků ovlivňujících plány.</span><span class="sxs-lookup"><span data-stu-id="87fd8-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="87fd8-128">Rozhraní API plánu projektu</span><span class="sxs-lookup"><span data-stu-id="87fd8-128">Project schedule APIs</span></span>

<span data-ttu-id="87fd8-129">Následuje seznam aktuálních rozhraní API plánu projektu.</span><span class="sxs-lookup"><span data-stu-id="87fd8-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="87fd8-130">**msdyn_CreateProjectV1** : Toto API lze použít k vytvoření projektu.</span><span class="sxs-lookup"><span data-stu-id="87fd8-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="87fd8-131">Projekt a výchozí projektový kbelík se vytvoří okamžitě.</span><span class="sxs-lookup"><span data-stu-id="87fd8-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="87fd8-132">**msdyn_CreateTeamMemberV1** : Toto API lze použít k vytvoření člena projektového týmu.</span><span class="sxs-lookup"><span data-stu-id="87fd8-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="87fd8-133">Záznam člena týmu je vytvořen okamžitě.</span><span class="sxs-lookup"><span data-stu-id="87fd8-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="87fd8-134">**msdyn_CreateOperationSetV1** : Toto API lze použít k naplánování několika požadavků, které je třeba provést v rámci transakce.</span><span class="sxs-lookup"><span data-stu-id="87fd8-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="87fd8-135">**msdyn_PSSCreateV1** : Toto API lze použít k vytvoření entity.</span><span class="sxs-lookup"><span data-stu-id="87fd8-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="87fd8-136">Entitou může být jakákoli entita plánování projektu, která podporuje operaci vytvoření.</span><span class="sxs-lookup"><span data-stu-id="87fd8-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="87fd8-137">**msdyn_PSSUpdateV1** : Toto API lze použít k aktualizaci entity.</span><span class="sxs-lookup"><span data-stu-id="87fd8-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="87fd8-138">Entitou může být jakákoli entita plánování projektu, která podporuje operaci aktualizace.</span><span class="sxs-lookup"><span data-stu-id="87fd8-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="87fd8-139">**msdyn_PSSDeleteV1** : Toto API lze použít k odstranění entity.</span><span class="sxs-lookup"><span data-stu-id="87fd8-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="87fd8-140">Entitou může být jakákoli entita plánování projektu, která podporuje operaci odstranění.</span><span class="sxs-lookup"><span data-stu-id="87fd8-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="87fd8-141">**msdyn_ExecuteOperationSetV1** : Toto API se používá k provedení všech operací v rámci dané sady operací.</span><span class="sxs-lookup"><span data-stu-id="87fd8-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="87fd8-142">Používání API plánu projektu s OperationSet</span><span class="sxs-lookup"><span data-stu-id="87fd8-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="87fd8-143">Protože záznamy s oběma rozhraními **CreateProjectV1** a **CreateTeamMemberV1** jsou vytvořeny okamžitě, nelze tato API použít v sadě **OperationSet** přímo.</span><span class="sxs-lookup"><span data-stu-id="87fd8-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="87fd8-144">Můžete však použít API k vytvoření potřebných záznamů, vytvořit sadu **OperationSet** a poté použít tyto předem vytvořené záznamy v sadě **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="87fd8-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="87fd8-145">Podporované operace</span><span class="sxs-lookup"><span data-stu-id="87fd8-145">Supported operations</span></span>

| <span data-ttu-id="87fd8-146">Entita plánování</span><span class="sxs-lookup"><span data-stu-id="87fd8-146">Scheduling entity</span></span> | <span data-ttu-id="87fd8-147">Vytvoření</span><span class="sxs-lookup"><span data-stu-id="87fd8-147">Create</span></span> | <span data-ttu-id="87fd8-148">Aktualizace</span><span class="sxs-lookup"><span data-stu-id="87fd8-148">Update</span></span> | <span data-ttu-id="87fd8-149">Odstranění</span><span class="sxs-lookup"><span data-stu-id="87fd8-149">Delete</span></span> | <span data-ttu-id="87fd8-150">Důležitá poznámka</span><span class="sxs-lookup"><span data-stu-id="87fd8-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="87fd8-151">Projektový úkol</span><span class="sxs-lookup"><span data-stu-id="87fd8-151">Project task</span></span> | <span data-ttu-id="87fd8-152">Ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-152">Yes</span></span> | <span data-ttu-id="87fd8-153">Ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-153">Yes</span></span> | <span data-ttu-id="87fd8-154">Ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-154">Yes</span></span> | <span data-ttu-id="87fd8-155">Nic</span><span class="sxs-lookup"><span data-stu-id="87fd8-155">None</span></span> |
| <span data-ttu-id="87fd8-156">Závislost projektového úkolu</span><span class="sxs-lookup"><span data-stu-id="87fd8-156">Project task dependency</span></span> | <span data-ttu-id="87fd8-157">Ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-157">Yes</span></span> | <span data-ttu-id="87fd8-158">Ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-158">Yes</span></span> | | <span data-ttu-id="87fd8-159">Záznamy závislostí projektových úkolů se neaktualizují.</span><span class="sxs-lookup"><span data-stu-id="87fd8-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="87fd8-160">Místo toho lze starý záznam odstranit a vytvořit nový záznam.</span><span class="sxs-lookup"><span data-stu-id="87fd8-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="87fd8-161">Přiřazení zdroje</span><span class="sxs-lookup"><span data-stu-id="87fd8-161">Resource assignment</span></span> | <span data-ttu-id="87fd8-162">Ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-162">Yes</span></span> | <span data-ttu-id="87fd8-163">Ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-163">Yes</span></span> | | <span data-ttu-id="87fd8-164">Operace s následujícími poli nejsou podporovány: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** a **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="87fd8-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="87fd8-165">Záznamy přiřazení zdrojů se neaktualizují.</span><span class="sxs-lookup"><span data-stu-id="87fd8-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="87fd8-166">Místo toho lze starý záznam odstranit a vytvořit nový záznam.</span><span class="sxs-lookup"><span data-stu-id="87fd8-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="87fd8-167">Kbelík projektu</span><span class="sxs-lookup"><span data-stu-id="87fd8-167">Project bucket</span></span> | <span data-ttu-id="87fd8-168">Není k dispozici</span><span class="sxs-lookup"><span data-stu-id="87fd8-168">N/A</span></span> | <span data-ttu-id="87fd8-169">Není k dispozici</span><span class="sxs-lookup"><span data-stu-id="87fd8-169">N/A</span></span> | <span data-ttu-id="87fd8-170">Není k dispozici</span><span class="sxs-lookup"><span data-stu-id="87fd8-170">N/A</span></span> | <span data-ttu-id="87fd8-171">Výchozí kbelík je vytvořen pomocí rozhraní API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="87fd8-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="87fd8-172">Člen projektového týmu</span><span class="sxs-lookup"><span data-stu-id="87fd8-172">Project team member</span></span> | <span data-ttu-id="87fd8-173">Ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-173">Yes</span></span> | <span data-ttu-id="87fd8-174">Ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-174">Yes</span></span> | <span data-ttu-id="87fd8-175">Ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-175">Yes</span></span> | <span data-ttu-id="87fd8-176">Pro operaci vytvoření použijte API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="87fd8-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="87fd8-177">Project</span><span class="sxs-lookup"><span data-stu-id="87fd8-177">Project</span></span> | <span data-ttu-id="87fd8-178">Ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-178">Yes</span></span> | <span data-ttu-id="87fd8-179">Ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-179">Yes</span></span> | <span data-ttu-id="87fd8-180">Není k dispozici</span><span class="sxs-lookup"><span data-stu-id="87fd8-180">N/A</span></span> | <span data-ttu-id="87fd8-181">Operace s následujícími poli nejsou podporovány: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** a **Duration**.</span><span class="sxs-lookup"><span data-stu-id="87fd8-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="87fd8-182">Tato rozhraní API lze volat s objekty entit, které obsahují vlastní pole.</span><span class="sxs-lookup"><span data-stu-id="87fd8-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="87fd8-183">Vlastnost ID je volitelná.</span><span class="sxs-lookup"><span data-stu-id="87fd8-183">The ID property is optional.</span></span> <span data-ttu-id="87fd8-184">Pokud je k dispozici, systém se pokusí ji použít a vyvolá výjimku, pokud ji nelze použít.</span><span class="sxs-lookup"><span data-stu-id="87fd8-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="87fd8-185">Pokud není k dispozici, systém jej vygeneruje.</span><span class="sxs-lookup"><span data-stu-id="87fd8-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="87fd8-186">Omezená pole</span><span class="sxs-lookup"><span data-stu-id="87fd8-186">Restricted fields</span></span>

<span data-ttu-id="87fd8-187">Následující tabulky definují pole, která mají omezené funkce **Vytvořit** a **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="87fd8-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="87fd8-188">Projektový úkol</span><span class="sxs-lookup"><span data-stu-id="87fd8-188">Project task</span></span>

| <span data-ttu-id="87fd8-189">**Logický název**</span><span class="sxs-lookup"><span data-stu-id="87fd8-189">**Logical name**</span></span>                       | <span data-ttu-id="87fd8-190">**Je možné vytvořit**</span><span class="sxs-lookup"><span data-stu-id="87fd8-190">**Can create**</span></span> | <span data-ttu-id="87fd8-191">**Může upravit**</span><span class="sxs-lookup"><span data-stu-id="87fd8-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="87fd8-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="87fd8-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="87fd8-193">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-193">no</span></span>             | <span data-ttu-id="87fd8-194">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-194">no</span></span>               |
| <span data-ttu-id="87fd8-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="87fd8-196">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-196">no</span></span>             | <span data-ttu-id="87fd8-197">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-197">no</span></span>               |
| <span data-ttu-id="87fd8-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="87fd8-198">msdyn_actualend</span></span>                        | <span data-ttu-id="87fd8-199">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-199">no</span></span>             | <span data-ttu-id="87fd8-200">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-200">no</span></span>               |
| <span data-ttu-id="87fd8-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="87fd8-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="87fd8-202">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-202">no</span></span>             | <span data-ttu-id="87fd8-203">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-203">no</span></span>               |
| <span data-ttu-id="87fd8-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="87fd8-205">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-205">no</span></span>             | <span data-ttu-id="87fd8-206">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-206">no</span></span>               |
| <span data-ttu-id="87fd8-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="87fd8-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="87fd8-208">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-208">no</span></span>             | <span data-ttu-id="87fd8-209">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-209">no</span></span>               |
| <span data-ttu-id="87fd8-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="87fd8-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="87fd8-211">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-211">no</span></span>             | <span data-ttu-id="87fd8-212">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-212">no</span></span>               |
| <span data-ttu-id="87fd8-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="87fd8-214">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-214">no</span></span>             | <span data-ttu-id="87fd8-215">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-215">no</span></span>               |
| <span data-ttu-id="87fd8-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="87fd8-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="87fd8-217">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-217">no</span></span>             | <span data-ttu-id="87fd8-218">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-218">no</span></span>               |
| <span data-ttu-id="87fd8-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="87fd8-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="87fd8-220">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-220">no</span></span>             | <span data-ttu-id="87fd8-221">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-221">no</span></span>               |
| <span data-ttu-id="87fd8-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="87fd8-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="87fd8-223">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-223">no</span></span>             | <span data-ttu-id="87fd8-224">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-224">no</span></span>               |
| <span data-ttu-id="87fd8-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="87fd8-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="87fd8-226">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-226">no</span></span>             | <span data-ttu-id="87fd8-227">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-227">no</span></span>               |
| <span data-ttu-id="87fd8-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="87fd8-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="87fd8-229">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-229">no</span></span>             | <span data-ttu-id="87fd8-230">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-230">no</span></span>               |
| <span data-ttu-id="87fd8-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="87fd8-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="87fd8-232">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-232">no</span></span>             | <span data-ttu-id="87fd8-233">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-233">no</span></span>               |
| <span data-ttu-id="87fd8-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="87fd8-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="87fd8-235">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-235">no</span></span>             | <span data-ttu-id="87fd8-236">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-236">no</span></span>               |
| <span data-ttu-id="87fd8-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="87fd8-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="87fd8-238">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-238">no</span></span>             | <span data-ttu-id="87fd8-239">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-239">no</span></span>               |
| <span data-ttu-id="87fd8-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="87fd8-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="87fd8-241">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-241">no</span></span>             | <span data-ttu-id="87fd8-242">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-242">no</span></span>               |
| <span data-ttu-id="87fd8-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="87fd8-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="87fd8-244">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-244">no</span></span>             | <span data-ttu-id="87fd8-245">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-245">no</span></span>               |
| <span data-ttu-id="87fd8-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="87fd8-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="87fd8-247">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-247">no</span></span>             | <span data-ttu-id="87fd8-248">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-248">no</span></span>               |
| <span data-ttu-id="87fd8-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="87fd8-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="87fd8-250">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-250">no</span></span>             | <span data-ttu-id="87fd8-251">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-251">no</span></span>               |
| <span data-ttu-id="87fd8-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="87fd8-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="87fd8-253">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-253">no</span></span>             | <span data-ttu-id="87fd8-254">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-254">no</span></span>               |
| <span data-ttu-id="87fd8-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="87fd8-256">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-256">no</span></span>             | <span data-ttu-id="87fd8-257">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-257">no</span></span>               |
| <span data-ttu-id="87fd8-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="87fd8-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="87fd8-259">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-259">no</span></span>             | <span data-ttu-id="87fd8-260">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-260">no</span></span>               |
| <span data-ttu-id="87fd8-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="87fd8-262">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-262">no</span></span>             | <span data-ttu-id="87fd8-263">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-263">no</span></span>               |
| <span data-ttu-id="87fd8-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="87fd8-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="87fd8-265">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-265">no</span></span>             | <span data-ttu-id="87fd8-266">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-266">no</span></span>               |
| <span data-ttu-id="87fd8-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="87fd8-267">msdyn_progress</span></span>                         | <span data-ttu-id="87fd8-268">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-268">no</span></span>             | <span data-ttu-id="87fd8-269">ne (ano pro P4W)</span><span class="sxs-lookup"><span data-stu-id="87fd8-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="87fd8-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="87fd8-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="87fd8-271">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-271">no</span></span>             | <span data-ttu-id="87fd8-272">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-272">no</span></span>               |
| <span data-ttu-id="87fd8-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="87fd8-274">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-274">no</span></span>             | <span data-ttu-id="87fd8-275">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-275">no</span></span>               |
| <span data-ttu-id="87fd8-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="87fd8-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="87fd8-277">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-277">no</span></span>             | <span data-ttu-id="87fd8-278">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-278">no</span></span>               |
| <span data-ttu-id="87fd8-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="87fd8-280">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-280">no</span></span>             | <span data-ttu-id="87fd8-281">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-281">no</span></span>               |
| <span data-ttu-id="87fd8-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="87fd8-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="87fd8-283">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-283">no</span></span>             | <span data-ttu-id="87fd8-284">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-284">no</span></span>               |
| <span data-ttu-id="87fd8-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="87fd8-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="87fd8-286">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-286">no</span></span>             | <span data-ttu-id="87fd8-287">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-287">no</span></span>               |
| <span data-ttu-id="87fd8-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="87fd8-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="87fd8-289">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-289">no</span></span>             | <span data-ttu-id="87fd8-290">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-290">no</span></span>               |
| <span data-ttu-id="87fd8-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="87fd8-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="87fd8-292">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-292">no</span></span>             | <span data-ttu-id="87fd8-293">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-293">no</span></span>               |
| <span data-ttu-id="87fd8-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="87fd8-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="87fd8-295">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-295">no</span></span>             | <span data-ttu-id="87fd8-296">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-296">no</span></span>               |
| <span data-ttu-id="87fd8-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="87fd8-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="87fd8-298">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-298">no</span></span>             | <span data-ttu-id="87fd8-299">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-299">no</span></span>               |
| <span data-ttu-id="87fd8-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="87fd8-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="87fd8-301">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-301">no</span></span>             | <span data-ttu-id="87fd8-302">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-302">no</span></span>               |
| <span data-ttu-id="87fd8-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="87fd8-304">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-304">no</span></span>             | <span data-ttu-id="87fd8-305">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-305">no</span></span>               |
| <span data-ttu-id="87fd8-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="87fd8-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="87fd8-307">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-307">no</span></span>             | <span data-ttu-id="87fd8-308">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-308">no</span></span>               |
| <span data-ttu-id="87fd8-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="87fd8-310">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-310">no</span></span>             | <span data-ttu-id="87fd8-311">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-311">no</span></span>               |
| <span data-ttu-id="87fd8-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="87fd8-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="87fd8-313">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-313">no</span></span>             | <span data-ttu-id="87fd8-314">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-314">no</span></span>               |
| <span data-ttu-id="87fd8-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="87fd8-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="87fd8-316">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-316">no</span></span>             | <span data-ttu-id="87fd8-317">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-317">no</span></span>               |
| <span data-ttu-id="87fd8-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="87fd8-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="87fd8-319">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-319">no</span></span>             | <span data-ttu-id="87fd8-320">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-320">no</span></span>               |
| <span data-ttu-id="87fd8-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="87fd8-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="87fd8-322">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-322">no</span></span>             | <span data-ttu-id="87fd8-323">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-323">no</span></span>               |
| <span data-ttu-id="87fd8-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="87fd8-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="87fd8-325">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-325">no</span></span>             | <span data-ttu-id="87fd8-326">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-326">no</span></span>               |
| <span data-ttu-id="87fd8-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="87fd8-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="87fd8-328">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-328">no</span></span>             | <span data-ttu-id="87fd8-329">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-329">no</span></span>               |
| <span data-ttu-id="87fd8-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="87fd8-330">msdyn_summary</span></span>                          | <span data-ttu-id="87fd8-331">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-331">no</span></span>             | <span data-ttu-id="87fd8-332">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-332">no</span></span>               |
| <span data-ttu-id="87fd8-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="87fd8-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="87fd8-334">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-334">no</span></span>             | <span data-ttu-id="87fd8-335">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-335">no</span></span>               |
| <span data-ttu-id="87fd8-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="87fd8-337">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-337">no</span></span>             | <span data-ttu-id="87fd8-338">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="87fd8-339">Závislost projektového úkolu</span><span class="sxs-lookup"><span data-stu-id="87fd8-339">Project task dependency</span></span>

| <span data-ttu-id="87fd8-340">**Logický název**</span><span class="sxs-lookup"><span data-stu-id="87fd8-340">**Logical name**</span></span>              | <span data-ttu-id="87fd8-341">**Je možné vytvořit**</span><span class="sxs-lookup"><span data-stu-id="87fd8-341">**Can create**</span></span> | <span data-ttu-id="87fd8-342">**Může upravit**</span><span class="sxs-lookup"><span data-stu-id="87fd8-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="87fd8-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="87fd8-343">msdyn_linktype</span></span>                | <span data-ttu-id="87fd8-344">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-344">no</span></span>             | <span data-ttu-id="87fd8-345">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-345">no</span></span>           |
| <span data-ttu-id="87fd8-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="87fd8-346">msdyn_linktypename</span></span>            | <span data-ttu-id="87fd8-347">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-347">no</span></span>             | <span data-ttu-id="87fd8-348">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-348">no</span></span>           |
| <span data-ttu-id="87fd8-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="87fd8-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="87fd8-350">ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-350">yes</span></span>            | <span data-ttu-id="87fd8-351">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-351">no</span></span>           |
| <span data-ttu-id="87fd8-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="87fd8-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="87fd8-353">ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-353">yes</span></span>            | <span data-ttu-id="87fd8-354">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-354">no</span></span>           |
| <span data-ttu-id="87fd8-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="87fd8-355">msdyn_project</span></span>                 | <span data-ttu-id="87fd8-356">ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-356">yes</span></span>            | <span data-ttu-id="87fd8-357">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-357">no</span></span>           |
| <span data-ttu-id="87fd8-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="87fd8-358">msdyn_projectname</span></span>             | <span data-ttu-id="87fd8-359">ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-359">yes</span></span>            | <span data-ttu-id="87fd8-360">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-360">no</span></span>           |
| <span data-ttu-id="87fd8-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="87fd8-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="87fd8-362">ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-362">yes</span></span>            | <span data-ttu-id="87fd8-363">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-363">no</span></span>           |
| <span data-ttu-id="87fd8-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="87fd8-364">msdyn_successortask</span></span>           | <span data-ttu-id="87fd8-365">ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-365">yes</span></span>            | <span data-ttu-id="87fd8-366">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-366">no</span></span>           |
| <span data-ttu-id="87fd8-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="87fd8-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="87fd8-368">ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-368">yes</span></span>            | <span data-ttu-id="87fd8-369">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="87fd8-370">Přiřazení zdroje</span><span class="sxs-lookup"><span data-stu-id="87fd8-370">Resource assignment</span></span>

| <span data-ttu-id="87fd8-371">**Logický název**</span><span class="sxs-lookup"><span data-stu-id="87fd8-371">**Logical name**</span></span>             | <span data-ttu-id="87fd8-372">**Je možné vytvořit**</span><span class="sxs-lookup"><span data-stu-id="87fd8-372">**Can create**</span></span> | <span data-ttu-id="87fd8-373">**Může upravit**</span><span class="sxs-lookup"><span data-stu-id="87fd8-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="87fd8-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="87fd8-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="87fd8-375">ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-375">yes</span></span>            | <span data-ttu-id="87fd8-376">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-376">no</span></span>           |
| <span data-ttu-id="87fd8-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="87fd8-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="87fd8-378">ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-378">yes</span></span>            | <span data-ttu-id="87fd8-379">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-379">no</span></span>           |
| <span data-ttu-id="87fd8-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="87fd8-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="87fd8-381">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-381">no</span></span>             | <span data-ttu-id="87fd8-382">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-382">no</span></span>           |
| <span data-ttu-id="87fd8-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="87fd8-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="87fd8-384">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-384">no</span></span>             | <span data-ttu-id="87fd8-385">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-385">no</span></span>           |
| <span data-ttu-id="87fd8-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="87fd8-386">msdyn_committype</span></span>             | <span data-ttu-id="87fd8-387">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-387">no</span></span>             | <span data-ttu-id="87fd8-388">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-388">no</span></span>           |
| <span data-ttu-id="87fd8-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="87fd8-389">msdyn_committypename</span></span>         | <span data-ttu-id="87fd8-390">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-390">no</span></span>             | <span data-ttu-id="87fd8-391">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-391">no</span></span>           |
| <span data-ttu-id="87fd8-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="87fd8-392">msdyn_effort</span></span>                 | <span data-ttu-id="87fd8-393">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-393">no</span></span>             | <span data-ttu-id="87fd8-394">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-394">no</span></span>           |
| <span data-ttu-id="87fd8-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="87fd8-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="87fd8-396">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-396">no</span></span>             | <span data-ttu-id="87fd8-397">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-397">no</span></span>           |
| <span data-ttu-id="87fd8-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="87fd8-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="87fd8-399">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-399">no</span></span>             | <span data-ttu-id="87fd8-400">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-400">no</span></span>           |
| <span data-ttu-id="87fd8-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="87fd8-401">msdyn_finish</span></span>                 | <span data-ttu-id="87fd8-402">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-402">no</span></span>             | <span data-ttu-id="87fd8-403">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-403">no</span></span>           |
| <span data-ttu-id="87fd8-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="87fd8-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="87fd8-405">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-405">no</span></span>             | <span data-ttu-id="87fd8-406">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-406">no</span></span>           |
| <span data-ttu-id="87fd8-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="87fd8-408">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-408">no</span></span>             | <span data-ttu-id="87fd8-409">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-409">no</span></span>           |
| <span data-ttu-id="87fd8-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="87fd8-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="87fd8-411">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-411">no</span></span>             | <span data-ttu-id="87fd8-412">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-412">no</span></span>           |
| <span data-ttu-id="87fd8-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="87fd8-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="87fd8-414">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-414">no</span></span>             | <span data-ttu-id="87fd8-415">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-415">no</span></span>           |
| <span data-ttu-id="87fd8-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="87fd8-417">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-417">no</span></span>             | <span data-ttu-id="87fd8-418">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-418">no</span></span>           |
| <span data-ttu-id="87fd8-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="87fd8-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="87fd8-420">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-420">no</span></span>             | <span data-ttu-id="87fd8-421">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-421">no</span></span>           |
| <span data-ttu-id="87fd8-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="87fd8-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="87fd8-423">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-423">no</span></span>             | <span data-ttu-id="87fd8-424">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-424">no</span></span>           |
| <span data-ttu-id="87fd8-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="87fd8-425">msdyn_projectid</span></span>              | <span data-ttu-id="87fd8-426">ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-426">yes</span></span>            | <span data-ttu-id="87fd8-427">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-427">no</span></span>           |
| <span data-ttu-id="87fd8-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="87fd8-428">msdyn_projectidname</span></span>          | <span data-ttu-id="87fd8-429">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-429">no</span></span>             | <span data-ttu-id="87fd8-430">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-430">no</span></span>           |
| <span data-ttu-id="87fd8-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="87fd8-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="87fd8-432">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-432">no</span></span>             | <span data-ttu-id="87fd8-433">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-433">no</span></span>           |
| <span data-ttu-id="87fd8-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="87fd8-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="87fd8-435">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-435">no</span></span>             | <span data-ttu-id="87fd8-436">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-436">no</span></span>           |
| <span data-ttu-id="87fd8-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="87fd8-437">msdyn_start</span></span>                  | <span data-ttu-id="87fd8-438">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-438">no</span></span>             | <span data-ttu-id="87fd8-439">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-439">no</span></span>           |
| <span data-ttu-id="87fd8-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="87fd8-440">msdyn_taskid</span></span>                 | <span data-ttu-id="87fd8-441">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-441">no</span></span>             | <span data-ttu-id="87fd8-442">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-442">no</span></span>           |
| <span data-ttu-id="87fd8-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="87fd8-443">msdyn_taskidname</span></span>             | <span data-ttu-id="87fd8-444">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-444">no</span></span>             | <span data-ttu-id="87fd8-445">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-445">no</span></span>           |
| <span data-ttu-id="87fd8-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="87fd8-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="87fd8-447">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-447">no</span></span>             | <span data-ttu-id="87fd8-448">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="87fd8-449">Člen projektového týmu</span><span class="sxs-lookup"><span data-stu-id="87fd8-449">Project team member</span></span>

| <span data-ttu-id="87fd8-450">**Logický název**</span><span class="sxs-lookup"><span data-stu-id="87fd8-450">**Logical name**</span></span>                                 | <span data-ttu-id="87fd8-451">**Je možné vytvořit**</span><span class="sxs-lookup"><span data-stu-id="87fd8-451">**Can create**</span></span> | <span data-ttu-id="87fd8-452">**Může upravit**</span><span class="sxs-lookup"><span data-stu-id="87fd8-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="87fd8-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="87fd8-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="87fd8-454">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-454">no</span></span>             | <span data-ttu-id="87fd8-455">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-455">no</span></span>           |
| <span data-ttu-id="87fd8-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="87fd8-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="87fd8-457">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-457">no</span></span>             | <span data-ttu-id="87fd8-458">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-458">no</span></span>           |
| <span data-ttu-id="87fd8-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="87fd8-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="87fd8-460">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-460">no</span></span>             | <span data-ttu-id="87fd8-461">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-461">no</span></span>           |
| <span data-ttu-id="87fd8-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="87fd8-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="87fd8-463">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-463">no</span></span>             | <span data-ttu-id="87fd8-464">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-464">no</span></span>           |
| <span data-ttu-id="87fd8-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="87fd8-465">msdyn_effort</span></span>                                     | <span data-ttu-id="87fd8-466">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-466">no</span></span>             | <span data-ttu-id="87fd8-467">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-467">no</span></span>           |
| <span data-ttu-id="87fd8-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="87fd8-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="87fd8-469">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-469">no</span></span>             | <span data-ttu-id="87fd8-470">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-470">no</span></span>           |
| <span data-ttu-id="87fd8-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="87fd8-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="87fd8-472">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-472">no</span></span>             | <span data-ttu-id="87fd8-473">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-473">no</span></span>           |
| <span data-ttu-id="87fd8-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="87fd8-474">msdyn_finish</span></span>                                     | <span data-ttu-id="87fd8-475">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-475">no</span></span>             | <span data-ttu-id="87fd8-476">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-476">no</span></span>           |
| <span data-ttu-id="87fd8-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="87fd8-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="87fd8-478">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-478">no</span></span>             | <span data-ttu-id="87fd8-479">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-479">no</span></span>           |
| <span data-ttu-id="87fd8-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="87fd8-480">msdyn_hours</span></span>                                      | <span data-ttu-id="87fd8-481">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-481">no</span></span>             | <span data-ttu-id="87fd8-482">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-482">no</span></span>           |
| <span data-ttu-id="87fd8-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="87fd8-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="87fd8-484">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-484">no</span></span>             | <span data-ttu-id="87fd8-485">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-485">no</span></span>           |
| <span data-ttu-id="87fd8-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="87fd8-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="87fd8-487">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-487">no</span></span>             | <span data-ttu-id="87fd8-488">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-488">no</span></span>           |
| <span data-ttu-id="87fd8-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="87fd8-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="87fd8-490">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-490">no</span></span>             | <span data-ttu-id="87fd8-491">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-491">no</span></span>           |
| <span data-ttu-id="87fd8-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="87fd8-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="87fd8-493">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-493">no</span></span>             | <span data-ttu-id="87fd8-494">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-494">no</span></span>           |
| <span data-ttu-id="87fd8-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="87fd8-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="87fd8-496">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-496">no</span></span>             | <span data-ttu-id="87fd8-497">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-497">no</span></span>           |
| <span data-ttu-id="87fd8-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="87fd8-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="87fd8-499">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-499">no</span></span>             | <span data-ttu-id="87fd8-500">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-500">no</span></span>           |
| <span data-ttu-id="87fd8-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="87fd8-501">msdyn_start</span></span>                                      | <span data-ttu-id="87fd8-502">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-502">no</span></span>             | <span data-ttu-id="87fd8-503">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="87fd8-504">Project</span><span class="sxs-lookup"><span data-stu-id="87fd8-504">Project</span></span>

| <span data-ttu-id="87fd8-505">**Logický název**</span><span class="sxs-lookup"><span data-stu-id="87fd8-505">**Logical name**</span></span>                       | <span data-ttu-id="87fd8-506">**Je možné vytvořit**</span><span class="sxs-lookup"><span data-stu-id="87fd8-506">**Can create**</span></span> | <span data-ttu-id="87fd8-507">**Může upravit**</span><span class="sxs-lookup"><span data-stu-id="87fd8-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="87fd8-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="87fd8-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="87fd8-509">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-509">no</span></span>             | <span data-ttu-id="87fd8-510">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-510">no</span></span>           |
| <span data-ttu-id="87fd8-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="87fd8-512">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-512">no</span></span>             | <span data-ttu-id="87fd8-513">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-513">no</span></span>           |
| <span data-ttu-id="87fd8-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="87fd8-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="87fd8-515">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-515">no</span></span>             | <span data-ttu-id="87fd8-516">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-516">no</span></span>           |
| <span data-ttu-id="87fd8-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="87fd8-518">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-518">no</span></span>             | <span data-ttu-id="87fd8-519">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-519">no</span></span>           |
| <span data-ttu-id="87fd8-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="87fd8-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="87fd8-521">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-521">no</span></span>             | <span data-ttu-id="87fd8-522">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-522">no</span></span>           |
| <span data-ttu-id="87fd8-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="87fd8-524">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-524">no</span></span>             | <span data-ttu-id="87fd8-525">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-525">no</span></span>           |
| <span data-ttu-id="87fd8-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="87fd8-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="87fd8-527">ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-527">yes</span></span>            | <span data-ttu-id="87fd8-528">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-528">no</span></span>           |
| <span data-ttu-id="87fd8-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="87fd8-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="87fd8-530">ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-530">yes</span></span>            | <span data-ttu-id="87fd8-531">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-531">no</span></span>           |
| <span data-ttu-id="87fd8-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="87fd8-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="87fd8-533">ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-533">yes</span></span>            | <span data-ttu-id="87fd8-534">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-534">no</span></span>           |
| <span data-ttu-id="87fd8-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="87fd8-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="87fd8-536">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-536">no</span></span>             | <span data-ttu-id="87fd8-537">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-537">no</span></span>           |
| <span data-ttu-id="87fd8-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="87fd8-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="87fd8-539">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-539">no</span></span>             | <span data-ttu-id="87fd8-540">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-540">no</span></span>           |
| <span data-ttu-id="87fd8-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="87fd8-542">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-542">no</span></span>             | <span data-ttu-id="87fd8-543">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-543">no</span></span>           |
| <span data-ttu-id="87fd8-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="87fd8-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="87fd8-545">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-545">no</span></span>             | <span data-ttu-id="87fd8-546">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-546">no</span></span>           |
| <span data-ttu-id="87fd8-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="87fd8-548">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-548">no</span></span>             | <span data-ttu-id="87fd8-549">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-549">no</span></span>           |
| <span data-ttu-id="87fd8-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="87fd8-550">msdyn_duration</span></span>                         | <span data-ttu-id="87fd8-551">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-551">no</span></span>             | <span data-ttu-id="87fd8-552">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-552">no</span></span>           |
| <span data-ttu-id="87fd8-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="87fd8-553">msdyn_effort</span></span>                           | <span data-ttu-id="87fd8-554">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-554">no</span></span>             | <span data-ttu-id="87fd8-555">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-555">no</span></span>           |
| <span data-ttu-id="87fd8-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="87fd8-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="87fd8-557">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-557">no</span></span>             | <span data-ttu-id="87fd8-558">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-558">no</span></span>           |
| <span data-ttu-id="87fd8-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="87fd8-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="87fd8-560">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-560">no</span></span>             | <span data-ttu-id="87fd8-561">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-561">no</span></span>           |
| <span data-ttu-id="87fd8-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="87fd8-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="87fd8-563">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-563">no</span></span>             | <span data-ttu-id="87fd8-564">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-564">no</span></span>           |
| <span data-ttu-id="87fd8-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="87fd8-565">msdyn_finish</span></span>                           | <span data-ttu-id="87fd8-566">ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-566">yes</span></span>            | <span data-ttu-id="87fd8-567">ano</span><span class="sxs-lookup"><span data-stu-id="87fd8-567">yes</span></span>          |
| <span data-ttu-id="87fd8-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="87fd8-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="87fd8-569">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-569">no</span></span>             | <span data-ttu-id="87fd8-570">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-570">no</span></span>           |
| <span data-ttu-id="87fd8-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="87fd8-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="87fd8-572">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-572">no</span></span>             | <span data-ttu-id="87fd8-573">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-573">no</span></span>           |
| <span data-ttu-id="87fd8-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="87fd8-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="87fd8-575">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-575">no</span></span>             | <span data-ttu-id="87fd8-576">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-576">no</span></span>           |
| <span data-ttu-id="87fd8-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="87fd8-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="87fd8-578">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-578">no</span></span>             | <span data-ttu-id="87fd8-579">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-579">no</span></span>           |
| <span data-ttu-id="87fd8-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="87fd8-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="87fd8-581">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-581">no</span></span>             | <span data-ttu-id="87fd8-582">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-582">no</span></span>           |
| <span data-ttu-id="87fd8-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="87fd8-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="87fd8-584">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-584">no</span></span>             | <span data-ttu-id="87fd8-585">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-585">no</span></span>           |
| <span data-ttu-id="87fd8-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="87fd8-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="87fd8-587">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-587">no</span></span>             | <span data-ttu-id="87fd8-588">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-588">no</span></span>           |
| <span data-ttu-id="87fd8-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="87fd8-590">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-590">no</span></span>             | <span data-ttu-id="87fd8-591">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-591">no</span></span>           |
| <span data-ttu-id="87fd8-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="87fd8-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="87fd8-593">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-593">no</span></span>             | <span data-ttu-id="87fd8-594">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-594">no</span></span>           |
| <span data-ttu-id="87fd8-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="87fd8-596">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-596">no</span></span>             | <span data-ttu-id="87fd8-597">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-597">no</span></span>           |
| <span data-ttu-id="87fd8-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="87fd8-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="87fd8-599">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-599">no</span></span>             | <span data-ttu-id="87fd8-600">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-600">no</span></span>           |
| <span data-ttu-id="87fd8-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="87fd8-602">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-602">no</span></span>             | <span data-ttu-id="87fd8-603">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-603">no</span></span>           |
| <span data-ttu-id="87fd8-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="87fd8-604">msdyn_progress</span></span>                         | <span data-ttu-id="87fd8-605">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-605">no</span></span>             | <span data-ttu-id="87fd8-606">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-606">no</span></span>           |
| <span data-ttu-id="87fd8-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="87fd8-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="87fd8-608">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-608">no</span></span>             | <span data-ttu-id="87fd8-609">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-609">no</span></span>           |
| <span data-ttu-id="87fd8-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="87fd8-611">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-611">no</span></span>             | <span data-ttu-id="87fd8-612">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-612">no</span></span>           |
| <span data-ttu-id="87fd8-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="87fd8-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="87fd8-614">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-614">no</span></span>             | <span data-ttu-id="87fd8-615">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-615">no</span></span>           |
| <span data-ttu-id="87fd8-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="87fd8-617">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-617">no</span></span>             | <span data-ttu-id="87fd8-618">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-618">no</span></span>           |
| <span data-ttu-id="87fd8-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="87fd8-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="87fd8-620">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-620">no</span></span>             | <span data-ttu-id="87fd8-621">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-621">no</span></span>           |
| <span data-ttu-id="87fd8-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="87fd8-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="87fd8-623">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-623">no</span></span>             | <span data-ttu-id="87fd8-624">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-624">no</span></span>           |
| <span data-ttu-id="87fd8-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="87fd8-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="87fd8-626">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-626">no</span></span>             | <span data-ttu-id="87fd8-627">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-627">no</span></span>           |
| <span data-ttu-id="87fd8-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="87fd8-629">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-629">no</span></span>             | <span data-ttu-id="87fd8-630">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-630">no</span></span>           |
| <span data-ttu-id="87fd8-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="87fd8-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="87fd8-632">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-632">no</span></span>             | <span data-ttu-id="87fd8-633">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-633">no</span></span>           |
| <span data-ttu-id="87fd8-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="87fd8-635">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-635">no</span></span>             | <span data-ttu-id="87fd8-636">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-636">no</span></span>           |
| <span data-ttu-id="87fd8-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="87fd8-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="87fd8-638">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-638">no</span></span>             | <span data-ttu-id="87fd8-639">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-639">no</span></span>           |
| <span data-ttu-id="87fd8-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="87fd8-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="87fd8-641">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-641">no</span></span>             | <span data-ttu-id="87fd8-642">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-642">no</span></span>           |
| <span data-ttu-id="87fd8-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="87fd8-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="87fd8-644">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-644">no</span></span>             | <span data-ttu-id="87fd8-645">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-645">no</span></span>           |
| <span data-ttu-id="87fd8-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="87fd8-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="87fd8-647">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-647">no</span></span>             | <span data-ttu-id="87fd8-648">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-648">no</span></span>           |
| <span data-ttu-id="87fd8-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="87fd8-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="87fd8-650">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-650">no</span></span>             | <span data-ttu-id="87fd8-651">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-651">no</span></span>           |
| <span data-ttu-id="87fd8-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="87fd8-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="87fd8-653">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-653">no</span></span>             | <span data-ttu-id="87fd8-654">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-654">no</span></span>           |
| <span data-ttu-id="87fd8-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="87fd8-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="87fd8-656">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-656">no</span></span>             | <span data-ttu-id="87fd8-657">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-657">no</span></span>           |
| <span data-ttu-id="87fd8-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="87fd8-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="87fd8-659">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-659">no</span></span>             | <span data-ttu-id="87fd8-660">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-660">no</span></span>           |
| <span data-ttu-id="87fd8-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="87fd8-662">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-662">no</span></span>             | <span data-ttu-id="87fd8-663">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-663">no</span></span>           |
| <span data-ttu-id="87fd8-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="87fd8-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="87fd8-665">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-665">no</span></span>             | <span data-ttu-id="87fd8-666">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-666">no</span></span>           |
| <span data-ttu-id="87fd8-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="87fd8-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="87fd8-668">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-668">no</span></span>             | <span data-ttu-id="87fd8-669">ne</span><span class="sxs-lookup"><span data-stu-id="87fd8-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="87fd8-670">Omezení a známé problémy</span><span class="sxs-lookup"><span data-stu-id="87fd8-670">Limitations and known issues</span></span>
<span data-ttu-id="87fd8-671">Následuje seznam omezení a známých problémů:</span><span class="sxs-lookup"><span data-stu-id="87fd8-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="87fd8-672">Rozhraní API plánu projektu mohou používat pouze **Uživatelé s licencí Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="87fd8-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="87fd8-673">Nemohou je používat:</span><span class="sxs-lookup"><span data-stu-id="87fd8-673">They can't be used by:</span></span>
    - <span data-ttu-id="87fd8-674">Uživatelé aplikace</span><span class="sxs-lookup"><span data-stu-id="87fd8-674">Application users</span></span>
    - <span data-ttu-id="87fd8-675">Systémoví uživatelé</span><span class="sxs-lookup"><span data-stu-id="87fd8-675">System users</span></span>
    - <span data-ttu-id="87fd8-676">Uživatelé integrace</span><span class="sxs-lookup"><span data-stu-id="87fd8-676">Integration users</span></span>
    - <span data-ttu-id="87fd8-677">Ostatní uživatelé, kteří nemají požadovanou licenci</span><span class="sxs-lookup"><span data-stu-id="87fd8-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="87fd8-678">Každá sada **OperationSet** může mít maximálně 100 operací.</span><span class="sxs-lookup"><span data-stu-id="87fd8-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="87fd8-679">Každý uživatel může mít maximálně 10 otevřených sad **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="87fd8-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="87fd8-680">Project Operations v současné době podporuje maximálně 500 úkolů v jednom projektu.</span><span class="sxs-lookup"><span data-stu-id="87fd8-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="87fd8-681">Stav selhání a protokoly selhání nejsou u sad **OperationSet** aktuálně k dispozici.</span><span class="sxs-lookup"><span data-stu-id="87fd8-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="87fd8-682">Meze a hranice projektů a úkolů</span><span class="sxs-lookup"><span data-stu-id="87fd8-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="87fd8-683">Zpracování chyb</span><span class="sxs-lookup"><span data-stu-id="87fd8-683">Error handling</span></span>

   - <span data-ttu-id="87fd8-684">Chcete-li zkontrolovat chyby generované ze sad operací, přejděte na **Nastavení** \> **Naplánovat integraci** \> **Sady operací**.</span><span class="sxs-lookup"><span data-stu-id="87fd8-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="87fd8-685">Chcete-li zkontrolovat chyby generované službou plánování projektu, přejděte na **Nastavení** \> **Integrace plánu** \> **Protokoly chyb PSS**.</span><span class="sxs-lookup"><span data-stu-id="87fd8-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="87fd8-686">Ukázkový scénář</span><span class="sxs-lookup"><span data-stu-id="87fd8-686">Sample scenario</span></span>

<span data-ttu-id="87fd8-687">V tomto scénáři vytvoříte projekt, člena týmu, čtyři úkoly a dvě přiřazení prostředků.</span><span class="sxs-lookup"><span data-stu-id="87fd8-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="87fd8-688">Dále aktualizujete jeden úkol, aktualizujete projekt, odstraníte jeden úkol, odstraníte jedno přiřazení prostředku a vytvoříte závislost úkolu.</span><span class="sxs-lookup"><span data-stu-id="87fd8-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="87fd8-689">Další ukázky</span><span class="sxs-lookup"><span data-stu-id="87fd8-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
