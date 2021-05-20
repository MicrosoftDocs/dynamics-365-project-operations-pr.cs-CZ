---
title: Používání rozhraní Schedule API k provádění operací s entitami plánování
description: Tento téma poskytuje informace a ukázky pro používání rozhraní Schedule API.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950796"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="f8879-103">Používání rozhraní Schedule API k provádění operací s entitami plánování</span><span class="sxs-lookup"><span data-stu-id="f8879-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="f8879-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="f8879-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="f8879-105">Některé nebo všechny funkce uvedené v tomto tématu jsou k dispozici jako součást vydání verze Preview.</span><span class="sxs-lookup"><span data-stu-id="f8879-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="f8879-106">Obsah a funkce se mohou změnit.</span><span class="sxs-lookup"><span data-stu-id="f8879-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="f8879-107">Entity plánování</span><span class="sxs-lookup"><span data-stu-id="f8879-107">Scheduling entities</span></span>

<span data-ttu-id="f8879-108">Rozhraní Schedule API poskytuje funkce k vytváření, aktualizaci a odstraňování **entit plánování**.</span><span class="sxs-lookup"><span data-stu-id="f8879-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="f8879-109">Tyto entity jsou spravovány prostřednictvím modulu Plánování v aplikaci Project for the Web.</span><span class="sxs-lookup"><span data-stu-id="f8879-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="f8879-110">Operace vytváření, aktualizace a odstraňování **entit plánování** byly ve starších verzích Dynamics 365 Project Operations omezeny.</span><span class="sxs-lookup"><span data-stu-id="f8879-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="f8879-111">Následující tabulka obsahuje úplný seznam **entit plánování**.</span><span class="sxs-lookup"><span data-stu-id="f8879-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="f8879-112">Název entity</span><span class="sxs-lookup"><span data-stu-id="f8879-112">Entity name</span></span>  | <span data-ttu-id="f8879-113">Logický název entity</span><span class="sxs-lookup"><span data-stu-id="f8879-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="f8879-114">Project</span><span class="sxs-lookup"><span data-stu-id="f8879-114">Project</span></span> | <span data-ttu-id="f8879-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="f8879-115">msdyn_project</span></span> |
| <span data-ttu-id="f8879-116">Projektový úkol</span><span class="sxs-lookup"><span data-stu-id="f8879-116">Project Task</span></span>  | <span data-ttu-id="f8879-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="f8879-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="f8879-118">Závislost projektového úkolu</span><span class="sxs-lookup"><span data-stu-id="f8879-118">Project Task Dependency</span></span>  | <span data-ttu-id="f8879-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="f8879-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="f8879-120">Přiřazení zdroje</span><span class="sxs-lookup"><span data-stu-id="f8879-120">Resource Assignment</span></span> | <span data-ttu-id="f8879-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="f8879-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="f8879-122">Kbelík projektu</span><span class="sxs-lookup"><span data-stu-id="f8879-122">Project Bucket</span></span>  | <span data-ttu-id="f8879-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="f8879-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="f8879-124">Člen projektového týmu</span><span class="sxs-lookup"><span data-stu-id="f8879-124">Project Team Member</span></span> | <span data-ttu-id="f8879-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="f8879-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="f8879-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="f8879-126">OperationSet</span></span>

<span data-ttu-id="f8879-127">OperationSet je vzor jednotky práce, který lze použít, když musí být v rámci transakce zpracováno několik požadavků ovlivňujících plány.</span><span class="sxs-lookup"><span data-stu-id="f8879-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="f8879-128">Rozhraní Schedule API</span><span class="sxs-lookup"><span data-stu-id="f8879-128">Schedule APIs</span></span>

<span data-ttu-id="f8879-129">Následuje seznam aktuálních rozhraní Schedule API.</span><span class="sxs-lookup"><span data-stu-id="f8879-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="f8879-130">**msdyn_CreateProjectV1** : Toto API lze použít k vytvoření projektu.</span><span class="sxs-lookup"><span data-stu-id="f8879-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="f8879-131">Projekt a výchozí projektový kbelík se vytvoří okamžitě.</span><span class="sxs-lookup"><span data-stu-id="f8879-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="f8879-132">**msdyn_CreateTeamMemberV1** : Toto API lze použít k vytvoření člena projektového týmu.</span><span class="sxs-lookup"><span data-stu-id="f8879-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="f8879-133">Záznam člena týmu je vytvořen okamžitě.</span><span class="sxs-lookup"><span data-stu-id="f8879-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="f8879-134">**msdyn_CreateOperationSetV1** : Toto API lze použít k naplánování několika požadavků, které je třeba provést v rámci transakce.</span><span class="sxs-lookup"><span data-stu-id="f8879-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="f8879-135">**msdyn_PSSCreateV1** : Toto API lze použít k vytvoření entity.</span><span class="sxs-lookup"><span data-stu-id="f8879-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="f8879-136">Entitou může být libovolná entita plánování, která podporuje operaci vytvoření.</span><span class="sxs-lookup"><span data-stu-id="f8879-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="f8879-137">**msdyn_PSSUpdateV1** : Toto API lze použít k aktualizaci entity.</span><span class="sxs-lookup"><span data-stu-id="f8879-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="f8879-138">Entitou může být libovolná entita plánování, která podporuje operaci aktualizace.</span><span class="sxs-lookup"><span data-stu-id="f8879-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="f8879-139">**msdyn_PSSDeleteV1** : Toto API lze použít k odstranění entity.</span><span class="sxs-lookup"><span data-stu-id="f8879-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="f8879-140">Entitou může být libovolná entita plánování, která podporuje operaci odstranění.</span><span class="sxs-lookup"><span data-stu-id="f8879-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="f8879-141">**msdyn_ExecuteOperationSetV1** : Toto API se používá k provedení všech operací v rámci dané sady operací.</span><span class="sxs-lookup"><span data-stu-id="f8879-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="f8879-142">Používání rozhraní Schedule API s OperationSet</span><span class="sxs-lookup"><span data-stu-id="f8879-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="f8879-143">Protože záznamy s oběma rozhraními **CreateProjectV1** a **CreateTeamMemberV1** jsou vytvořeny okamžitě, nelze tato API použít v sadě **OperationSet** přímo.</span><span class="sxs-lookup"><span data-stu-id="f8879-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="f8879-144">Můžete však použít API k vytvoření potřebných záznamů, vytvořit sadu **OperationSet** a poté použít tyto předem vytvořené záznamy v sadě **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="f8879-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="f8879-145">Podporované operace</span><span class="sxs-lookup"><span data-stu-id="f8879-145">Supported operations</span></span>

| <span data-ttu-id="f8879-146">Entita plánování</span><span class="sxs-lookup"><span data-stu-id="f8879-146">Scheduling entity</span></span> | <span data-ttu-id="f8879-147">Vytvoření</span><span class="sxs-lookup"><span data-stu-id="f8879-147">Create</span></span> | <span data-ttu-id="f8879-148">Aktualizace</span><span class="sxs-lookup"><span data-stu-id="f8879-148">Update</span></span> | <span data-ttu-id="f8879-149">Odstranění</span><span class="sxs-lookup"><span data-stu-id="f8879-149">Delete</span></span> | <span data-ttu-id="f8879-150">Důležitá poznámka</span><span class="sxs-lookup"><span data-stu-id="f8879-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="f8879-151">Projektový úkol</span><span class="sxs-lookup"><span data-stu-id="f8879-151">Project task</span></span> | <span data-ttu-id="f8879-152">Ano</span><span class="sxs-lookup"><span data-stu-id="f8879-152">Yes</span></span> | <span data-ttu-id="f8879-153">Ano</span><span class="sxs-lookup"><span data-stu-id="f8879-153">Yes</span></span> | <span data-ttu-id="f8879-154">Ano</span><span class="sxs-lookup"><span data-stu-id="f8879-154">Yes</span></span> | <span data-ttu-id="f8879-155">Nic</span><span class="sxs-lookup"><span data-stu-id="f8879-155">None</span></span> |
| <span data-ttu-id="f8879-156">Závislost projektového úkolu</span><span class="sxs-lookup"><span data-stu-id="f8879-156">Project task dependency</span></span> | <span data-ttu-id="f8879-157">Ano</span><span class="sxs-lookup"><span data-stu-id="f8879-157">Yes</span></span> | <span data-ttu-id="f8879-158">Ano</span><span class="sxs-lookup"><span data-stu-id="f8879-158">Yes</span></span> | | <span data-ttu-id="f8879-159">Záznamy závislostí projektových úkolů se neaktualizují.</span><span class="sxs-lookup"><span data-stu-id="f8879-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="f8879-160">Místo toho lze starý záznam odstranit a vytvořit nový záznam.</span><span class="sxs-lookup"><span data-stu-id="f8879-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="f8879-161">Přiřazení zdroje</span><span class="sxs-lookup"><span data-stu-id="f8879-161">Resource assignment</span></span> | <span data-ttu-id="f8879-162">Ano</span><span class="sxs-lookup"><span data-stu-id="f8879-162">Yes</span></span> | <span data-ttu-id="f8879-163">Ano</span><span class="sxs-lookup"><span data-stu-id="f8879-163">Yes</span></span> | | <span data-ttu-id="f8879-164">Operace s následujícími poli nejsou podporovány: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** a **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="f8879-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="f8879-165">Záznamy přiřazení zdrojů se neaktualizují.</span><span class="sxs-lookup"><span data-stu-id="f8879-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="f8879-166">Místo toho lze starý záznam odstranit a vytvořit nový záznam.</span><span class="sxs-lookup"><span data-stu-id="f8879-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="f8879-167">Kbelík projektu</span><span class="sxs-lookup"><span data-stu-id="f8879-167">Project bucket</span></span> | <span data-ttu-id="f8879-168">Není k dispozici</span><span class="sxs-lookup"><span data-stu-id="f8879-168">N/A</span></span> | <span data-ttu-id="f8879-169">Není k dispozici</span><span class="sxs-lookup"><span data-stu-id="f8879-169">N/A</span></span> | <span data-ttu-id="f8879-170">Není k dispozici</span><span class="sxs-lookup"><span data-stu-id="f8879-170">N/A</span></span> | <span data-ttu-id="f8879-171">Výchozí kbelík je vytvořen pomocí rozhraní API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="f8879-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="f8879-172">Člen projektového týmu</span><span class="sxs-lookup"><span data-stu-id="f8879-172">Project team member</span></span> | <span data-ttu-id="f8879-173">Ano</span><span class="sxs-lookup"><span data-stu-id="f8879-173">Yes</span></span> | <span data-ttu-id="f8879-174">Ano</span><span class="sxs-lookup"><span data-stu-id="f8879-174">Yes</span></span> | <span data-ttu-id="f8879-175">Ano</span><span class="sxs-lookup"><span data-stu-id="f8879-175">Yes</span></span> | <span data-ttu-id="f8879-176">Pro operaci vytvoření použijte API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="f8879-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="f8879-177">Project</span><span class="sxs-lookup"><span data-stu-id="f8879-177">Project</span></span> | <span data-ttu-id="f8879-178">Ano</span><span class="sxs-lookup"><span data-stu-id="f8879-178">Yes</span></span> | <span data-ttu-id="f8879-179">Ano</span><span class="sxs-lookup"><span data-stu-id="f8879-179">Yes</span></span> | <span data-ttu-id="f8879-180">Není k dispozici</span><span class="sxs-lookup"><span data-stu-id="f8879-180">N/A</span></span> | <span data-ttu-id="f8879-181">Operace s následujícími poli nejsou podporovány: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** a **Duration**.</span><span class="sxs-lookup"><span data-stu-id="f8879-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="f8879-182">Tato rozhraní API lze volat s objekty entit, které obsahují vlastní pole.</span><span class="sxs-lookup"><span data-stu-id="f8879-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="f8879-183">Vlastnost ID je volitelná.</span><span class="sxs-lookup"><span data-stu-id="f8879-183">The ID property is optional.</span></span> <span data-ttu-id="f8879-184">Pokud je k dispozici, systém se pokusí ji použít a vyvolá výjimku, pokud ji nelze použít.</span><span class="sxs-lookup"><span data-stu-id="f8879-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="f8879-185">Pokud není k dispozici, systém jej vygeneruje.</span><span class="sxs-lookup"><span data-stu-id="f8879-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="f8879-186">Omezená pole</span><span class="sxs-lookup"><span data-stu-id="f8879-186">Restricted fields</span></span>

<span data-ttu-id="f8879-187">Následující tabulky definují pole, která mají omezené funkce **Vytvořit** a **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="f8879-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="f8879-188">Projektový úkol</span><span class="sxs-lookup"><span data-stu-id="f8879-188">Project task</span></span>

| <span data-ttu-id="f8879-189">**Logický název**</span><span class="sxs-lookup"><span data-stu-id="f8879-189">**Logical name**</span></span>                       | <span data-ttu-id="f8879-190">**Je možné vytvořit**</span><span class="sxs-lookup"><span data-stu-id="f8879-190">**Can create**</span></span> | <span data-ttu-id="f8879-191">**Může upravit**</span><span class="sxs-lookup"><span data-stu-id="f8879-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="f8879-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="f8879-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="f8879-193">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-193">no</span></span>             | <span data-ttu-id="f8879-194">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-194">no</span></span>               |
| <span data-ttu-id="f8879-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="f8879-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="f8879-196">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-196">no</span></span>             | <span data-ttu-id="f8879-197">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-197">no</span></span>               |
| <span data-ttu-id="f8879-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="f8879-198">msdyn_actualend</span></span>                        | <span data-ttu-id="f8879-199">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-199">no</span></span>             | <span data-ttu-id="f8879-200">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-200">no</span></span>               |
| <span data-ttu-id="f8879-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="f8879-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="f8879-202">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-202">no</span></span>             | <span data-ttu-id="f8879-203">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-203">no</span></span>               |
| <span data-ttu-id="f8879-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="f8879-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="f8879-205">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-205">no</span></span>             | <span data-ttu-id="f8879-206">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-206">no</span></span>               |
| <span data-ttu-id="f8879-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="f8879-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="f8879-208">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-208">no</span></span>             | <span data-ttu-id="f8879-209">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-209">no</span></span>               |
| <span data-ttu-id="f8879-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="f8879-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="f8879-211">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-211">no</span></span>             | <span data-ttu-id="f8879-212">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-212">no</span></span>               |
| <span data-ttu-id="f8879-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="f8879-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="f8879-214">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-214">no</span></span>             | <span data-ttu-id="f8879-215">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-215">no</span></span>               |
| <span data-ttu-id="f8879-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="f8879-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="f8879-217">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-217">no</span></span>             | <span data-ttu-id="f8879-218">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-218">no</span></span>               |
| <span data-ttu-id="f8879-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f8879-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="f8879-220">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-220">no</span></span>             | <span data-ttu-id="f8879-221">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-221">no</span></span>               |
| <span data-ttu-id="f8879-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="f8879-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="f8879-223">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-223">no</span></span>             | <span data-ttu-id="f8879-224">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-224">no</span></span>               |
| <span data-ttu-id="f8879-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="f8879-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="f8879-226">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-226">no</span></span>             | <span data-ttu-id="f8879-227">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-227">no</span></span>               |
| <span data-ttu-id="f8879-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="f8879-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="f8879-229">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-229">no</span></span>             | <span data-ttu-id="f8879-230">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-230">no</span></span>               |
| <span data-ttu-id="f8879-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="f8879-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="f8879-232">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-232">no</span></span>             | <span data-ttu-id="f8879-233">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-233">no</span></span>               |
| <span data-ttu-id="f8879-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="f8879-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="f8879-235">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-235">no</span></span>             | <span data-ttu-id="f8879-236">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-236">no</span></span>               |
| <span data-ttu-id="f8879-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="f8879-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="f8879-238">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-238">no</span></span>             | <span data-ttu-id="f8879-239">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-239">no</span></span>               |
| <span data-ttu-id="f8879-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="f8879-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="f8879-241">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-241">no</span></span>             | <span data-ttu-id="f8879-242">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-242">no</span></span>               |
| <span data-ttu-id="f8879-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="f8879-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="f8879-244">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-244">no</span></span>             | <span data-ttu-id="f8879-245">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-245">no</span></span>               |
| <span data-ttu-id="f8879-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="f8879-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="f8879-247">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-247">no</span></span>             | <span data-ttu-id="f8879-248">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-248">no</span></span>               |
| <span data-ttu-id="f8879-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="f8879-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="f8879-250">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-250">no</span></span>             | <span data-ttu-id="f8879-251">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-251">no</span></span>               |
| <span data-ttu-id="f8879-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="f8879-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="f8879-253">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-253">no</span></span>             | <span data-ttu-id="f8879-254">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-254">no</span></span>               |
| <span data-ttu-id="f8879-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="f8879-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="f8879-256">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-256">no</span></span>             | <span data-ttu-id="f8879-257">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-257">no</span></span>               |
| <span data-ttu-id="f8879-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="f8879-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="f8879-259">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-259">no</span></span>             | <span data-ttu-id="f8879-260">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-260">no</span></span>               |
| <span data-ttu-id="f8879-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="f8879-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="f8879-262">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-262">no</span></span>             | <span data-ttu-id="f8879-263">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-263">no</span></span>               |
| <span data-ttu-id="f8879-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="f8879-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="f8879-265">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-265">no</span></span>             | <span data-ttu-id="f8879-266">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-266">no</span></span>               |
| <span data-ttu-id="f8879-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="f8879-267">msdyn_progress</span></span>                         | <span data-ttu-id="f8879-268">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-268">no</span></span>             | <span data-ttu-id="f8879-269">ne (ano pro P4W)</span><span class="sxs-lookup"><span data-stu-id="f8879-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="f8879-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="f8879-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="f8879-271">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-271">no</span></span>             | <span data-ttu-id="f8879-272">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-272">no</span></span>               |
| <span data-ttu-id="f8879-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="f8879-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="f8879-274">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-274">no</span></span>             | <span data-ttu-id="f8879-275">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-275">no</span></span>               |
| <span data-ttu-id="f8879-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="f8879-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="f8879-277">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-277">no</span></span>             | <span data-ttu-id="f8879-278">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-278">no</span></span>               |
| <span data-ttu-id="f8879-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="f8879-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="f8879-280">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-280">no</span></span>             | <span data-ttu-id="f8879-281">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-281">no</span></span>               |
| <span data-ttu-id="f8879-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="f8879-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="f8879-283">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-283">no</span></span>             | <span data-ttu-id="f8879-284">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-284">no</span></span>               |
| <span data-ttu-id="f8879-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="f8879-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="f8879-286">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-286">no</span></span>             | <span data-ttu-id="f8879-287">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-287">no</span></span>               |
| <span data-ttu-id="f8879-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="f8879-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="f8879-289">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-289">no</span></span>             | <span data-ttu-id="f8879-290">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-290">no</span></span>               |
| <span data-ttu-id="f8879-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="f8879-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="f8879-292">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-292">no</span></span>             | <span data-ttu-id="f8879-293">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-293">no</span></span>               |
| <span data-ttu-id="f8879-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="f8879-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="f8879-295">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-295">no</span></span>             | <span data-ttu-id="f8879-296">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-296">no</span></span>               |
| <span data-ttu-id="f8879-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="f8879-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="f8879-298">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-298">no</span></span>             | <span data-ttu-id="f8879-299">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-299">no</span></span>               |
| <span data-ttu-id="f8879-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="f8879-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="f8879-301">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-301">no</span></span>             | <span data-ttu-id="f8879-302">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-302">no</span></span>               |
| <span data-ttu-id="f8879-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="f8879-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="f8879-304">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-304">no</span></span>             | <span data-ttu-id="f8879-305">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-305">no</span></span>               |
| <span data-ttu-id="f8879-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="f8879-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="f8879-307">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-307">no</span></span>             | <span data-ttu-id="f8879-308">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-308">no</span></span>               |
| <span data-ttu-id="f8879-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="f8879-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="f8879-310">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-310">no</span></span>             | <span data-ttu-id="f8879-311">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-311">no</span></span>               |
| <span data-ttu-id="f8879-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="f8879-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="f8879-313">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-313">no</span></span>             | <span data-ttu-id="f8879-314">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-314">no</span></span>               |
| <span data-ttu-id="f8879-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="f8879-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="f8879-316">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-316">no</span></span>             | <span data-ttu-id="f8879-317">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-317">no</span></span>               |
| <span data-ttu-id="f8879-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="f8879-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="f8879-319">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-319">no</span></span>             | <span data-ttu-id="f8879-320">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-320">no</span></span>               |
| <span data-ttu-id="f8879-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="f8879-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="f8879-322">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-322">no</span></span>             | <span data-ttu-id="f8879-323">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-323">no</span></span>               |
| <span data-ttu-id="f8879-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="f8879-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="f8879-325">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-325">no</span></span>             | <span data-ttu-id="f8879-326">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-326">no</span></span>               |
| <span data-ttu-id="f8879-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="f8879-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="f8879-328">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-328">no</span></span>             | <span data-ttu-id="f8879-329">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-329">no</span></span>               |
| <span data-ttu-id="f8879-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="f8879-330">msdyn_summary</span></span>                          | <span data-ttu-id="f8879-331">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-331">no</span></span>             | <span data-ttu-id="f8879-332">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-332">no</span></span>               |
| <span data-ttu-id="f8879-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="f8879-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="f8879-334">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-334">no</span></span>             | <span data-ttu-id="f8879-335">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-335">no</span></span>               |
| <span data-ttu-id="f8879-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="f8879-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="f8879-337">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-337">no</span></span>             | <span data-ttu-id="f8879-338">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="f8879-339">Závislost projektového úkolu</span><span class="sxs-lookup"><span data-stu-id="f8879-339">Project task dependency</span></span>

| <span data-ttu-id="f8879-340">**Logický název**</span><span class="sxs-lookup"><span data-stu-id="f8879-340">**Logical name**</span></span>              | <span data-ttu-id="f8879-341">**Je možné vytvořit**</span><span class="sxs-lookup"><span data-stu-id="f8879-341">**Can create**</span></span> | <span data-ttu-id="f8879-342">**Může upravit**</span><span class="sxs-lookup"><span data-stu-id="f8879-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="f8879-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="f8879-343">msdyn_linktype</span></span>                | <span data-ttu-id="f8879-344">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-344">no</span></span>             | <span data-ttu-id="f8879-345">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-345">no</span></span>           |
| <span data-ttu-id="f8879-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="f8879-346">msdyn_linktypename</span></span>            | <span data-ttu-id="f8879-347">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-347">no</span></span>             | <span data-ttu-id="f8879-348">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-348">no</span></span>           |
| <span data-ttu-id="f8879-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="f8879-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="f8879-350">ano</span><span class="sxs-lookup"><span data-stu-id="f8879-350">yes</span></span>            | <span data-ttu-id="f8879-351">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-351">no</span></span>           |
| <span data-ttu-id="f8879-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="f8879-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="f8879-353">ano</span><span class="sxs-lookup"><span data-stu-id="f8879-353">yes</span></span>            | <span data-ttu-id="f8879-354">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-354">no</span></span>           |
| <span data-ttu-id="f8879-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="f8879-355">msdyn_project</span></span>                 | <span data-ttu-id="f8879-356">ano</span><span class="sxs-lookup"><span data-stu-id="f8879-356">yes</span></span>            | <span data-ttu-id="f8879-357">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-357">no</span></span>           |
| <span data-ttu-id="f8879-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="f8879-358">msdyn_projectname</span></span>             | <span data-ttu-id="f8879-359">ano</span><span class="sxs-lookup"><span data-stu-id="f8879-359">yes</span></span>            | <span data-ttu-id="f8879-360">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-360">no</span></span>           |
| <span data-ttu-id="f8879-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="f8879-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="f8879-362">ano</span><span class="sxs-lookup"><span data-stu-id="f8879-362">yes</span></span>            | <span data-ttu-id="f8879-363">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-363">no</span></span>           |
| <span data-ttu-id="f8879-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="f8879-364">msdyn_successortask</span></span>           | <span data-ttu-id="f8879-365">ano</span><span class="sxs-lookup"><span data-stu-id="f8879-365">yes</span></span>            | <span data-ttu-id="f8879-366">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-366">no</span></span>           |
| <span data-ttu-id="f8879-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="f8879-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="f8879-368">ano</span><span class="sxs-lookup"><span data-stu-id="f8879-368">yes</span></span>            | <span data-ttu-id="f8879-369">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="f8879-370">Přiřazení zdroje</span><span class="sxs-lookup"><span data-stu-id="f8879-370">Resource assignment</span></span>

| <span data-ttu-id="f8879-371">**Logický název**</span><span class="sxs-lookup"><span data-stu-id="f8879-371">**Logical name**</span></span>             | <span data-ttu-id="f8879-372">**Je možné vytvořit**</span><span class="sxs-lookup"><span data-stu-id="f8879-372">**Can create**</span></span> | <span data-ttu-id="f8879-373">**Může upravit**</span><span class="sxs-lookup"><span data-stu-id="f8879-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="f8879-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="f8879-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="f8879-375">ano</span><span class="sxs-lookup"><span data-stu-id="f8879-375">yes</span></span>            | <span data-ttu-id="f8879-376">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-376">no</span></span>           |
| <span data-ttu-id="f8879-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="f8879-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="f8879-378">ano</span><span class="sxs-lookup"><span data-stu-id="f8879-378">yes</span></span>            | <span data-ttu-id="f8879-379">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-379">no</span></span>           |
| <span data-ttu-id="f8879-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="f8879-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="f8879-381">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-381">no</span></span>             | <span data-ttu-id="f8879-382">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-382">no</span></span>           |
| <span data-ttu-id="f8879-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="f8879-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="f8879-384">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-384">no</span></span>             | <span data-ttu-id="f8879-385">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-385">no</span></span>           |
| <span data-ttu-id="f8879-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="f8879-386">msdyn_committype</span></span>             | <span data-ttu-id="f8879-387">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-387">no</span></span>             | <span data-ttu-id="f8879-388">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-388">no</span></span>           |
| <span data-ttu-id="f8879-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="f8879-389">msdyn_committypename</span></span>         | <span data-ttu-id="f8879-390">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-390">no</span></span>             | <span data-ttu-id="f8879-391">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-391">no</span></span>           |
| <span data-ttu-id="f8879-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="f8879-392">msdyn_effort</span></span>                 | <span data-ttu-id="f8879-393">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-393">no</span></span>             | <span data-ttu-id="f8879-394">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-394">no</span></span>           |
| <span data-ttu-id="f8879-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f8879-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="f8879-396">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-396">no</span></span>             | <span data-ttu-id="f8879-397">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-397">no</span></span>           |
| <span data-ttu-id="f8879-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="f8879-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="f8879-399">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-399">no</span></span>             | <span data-ttu-id="f8879-400">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-400">no</span></span>           |
| <span data-ttu-id="f8879-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="f8879-401">msdyn_finish</span></span>                 | <span data-ttu-id="f8879-402">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-402">no</span></span>             | <span data-ttu-id="f8879-403">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-403">no</span></span>           |
| <span data-ttu-id="f8879-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="f8879-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="f8879-405">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-405">no</span></span>             | <span data-ttu-id="f8879-406">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-406">no</span></span>           |
| <span data-ttu-id="f8879-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="f8879-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="f8879-408">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-408">no</span></span>             | <span data-ttu-id="f8879-409">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-409">no</span></span>           |
| <span data-ttu-id="f8879-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="f8879-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="f8879-411">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-411">no</span></span>             | <span data-ttu-id="f8879-412">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-412">no</span></span>           |
| <span data-ttu-id="f8879-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="f8879-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="f8879-414">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-414">no</span></span>             | <span data-ttu-id="f8879-415">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-415">no</span></span>           |
| <span data-ttu-id="f8879-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="f8879-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="f8879-417">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-417">no</span></span>             | <span data-ttu-id="f8879-418">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-418">no</span></span>           |
| <span data-ttu-id="f8879-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="f8879-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="f8879-420">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-420">no</span></span>             | <span data-ttu-id="f8879-421">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-421">no</span></span>           |
| <span data-ttu-id="f8879-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="f8879-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="f8879-423">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-423">no</span></span>             | <span data-ttu-id="f8879-424">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-424">no</span></span>           |
| <span data-ttu-id="f8879-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="f8879-425">msdyn_projectid</span></span>              | <span data-ttu-id="f8879-426">ano</span><span class="sxs-lookup"><span data-stu-id="f8879-426">yes</span></span>            | <span data-ttu-id="f8879-427">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-427">no</span></span>           |
| <span data-ttu-id="f8879-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="f8879-428">msdyn_projectidname</span></span>          | <span data-ttu-id="f8879-429">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-429">no</span></span>             | <span data-ttu-id="f8879-430">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-430">no</span></span>           |
| <span data-ttu-id="f8879-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="f8879-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="f8879-432">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-432">no</span></span>             | <span data-ttu-id="f8879-433">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-433">no</span></span>           |
| <span data-ttu-id="f8879-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="f8879-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="f8879-435">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-435">no</span></span>             | <span data-ttu-id="f8879-436">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-436">no</span></span>           |
| <span data-ttu-id="f8879-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="f8879-437">msdyn_start</span></span>                  | <span data-ttu-id="f8879-438">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-438">no</span></span>             | <span data-ttu-id="f8879-439">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-439">no</span></span>           |
| <span data-ttu-id="f8879-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="f8879-440">msdyn_taskid</span></span>                 | <span data-ttu-id="f8879-441">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-441">no</span></span>             | <span data-ttu-id="f8879-442">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-442">no</span></span>           |
| <span data-ttu-id="f8879-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="f8879-443">msdyn_taskidname</span></span>             | <span data-ttu-id="f8879-444">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-444">no</span></span>             | <span data-ttu-id="f8879-445">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-445">no</span></span>           |
| <span data-ttu-id="f8879-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="f8879-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="f8879-447">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-447">no</span></span>             | <span data-ttu-id="f8879-448">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="f8879-449">Člen projektového týmu</span><span class="sxs-lookup"><span data-stu-id="f8879-449">Project team member</span></span>

| <span data-ttu-id="f8879-450">**Logický název**</span><span class="sxs-lookup"><span data-stu-id="f8879-450">**Logical name**</span></span>                                 | <span data-ttu-id="f8879-451">**Je možné vytvořit**</span><span class="sxs-lookup"><span data-stu-id="f8879-451">**Can create**</span></span> | <span data-ttu-id="f8879-452">**Může upravit**</span><span class="sxs-lookup"><span data-stu-id="f8879-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="f8879-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="f8879-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="f8879-454">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-454">no</span></span>             | <span data-ttu-id="f8879-455">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-455">no</span></span>           |
| <span data-ttu-id="f8879-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="f8879-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="f8879-457">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-457">no</span></span>             | <span data-ttu-id="f8879-458">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-458">no</span></span>           |
| <span data-ttu-id="f8879-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="f8879-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="f8879-460">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-460">no</span></span>             | <span data-ttu-id="f8879-461">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-461">no</span></span>           |
| <span data-ttu-id="f8879-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="f8879-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="f8879-463">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-463">no</span></span>             | <span data-ttu-id="f8879-464">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-464">no</span></span>           |
| <span data-ttu-id="f8879-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="f8879-465">msdyn_effort</span></span>                                     | <span data-ttu-id="f8879-466">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-466">no</span></span>             | <span data-ttu-id="f8879-467">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-467">no</span></span>           |
| <span data-ttu-id="f8879-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f8879-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="f8879-469">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-469">no</span></span>             | <span data-ttu-id="f8879-470">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-470">no</span></span>           |
| <span data-ttu-id="f8879-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="f8879-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="f8879-472">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-472">no</span></span>             | <span data-ttu-id="f8879-473">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-473">no</span></span>           |
| <span data-ttu-id="f8879-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="f8879-474">msdyn_finish</span></span>                                     | <span data-ttu-id="f8879-475">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-475">no</span></span>             | <span data-ttu-id="f8879-476">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-476">no</span></span>           |
| <span data-ttu-id="f8879-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="f8879-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="f8879-478">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-478">no</span></span>             | <span data-ttu-id="f8879-479">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-479">no</span></span>           |
| <span data-ttu-id="f8879-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="f8879-480">msdyn_hours</span></span>                                      | <span data-ttu-id="f8879-481">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-481">no</span></span>             | <span data-ttu-id="f8879-482">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-482">no</span></span>           |
| <span data-ttu-id="f8879-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="f8879-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="f8879-484">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-484">no</span></span>             | <span data-ttu-id="f8879-485">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-485">no</span></span>           |
| <span data-ttu-id="f8879-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="f8879-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="f8879-487">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-487">no</span></span>             | <span data-ttu-id="f8879-488">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-488">no</span></span>           |
| <span data-ttu-id="f8879-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="f8879-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="f8879-490">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-490">no</span></span>             | <span data-ttu-id="f8879-491">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-491">no</span></span>           |
| <span data-ttu-id="f8879-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="f8879-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="f8879-493">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-493">no</span></span>             | <span data-ttu-id="f8879-494">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-494">no</span></span>           |
| <span data-ttu-id="f8879-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="f8879-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="f8879-496">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-496">no</span></span>             | <span data-ttu-id="f8879-497">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-497">no</span></span>           |
| <span data-ttu-id="f8879-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="f8879-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="f8879-499">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-499">no</span></span>             | <span data-ttu-id="f8879-500">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-500">no</span></span>           |
| <span data-ttu-id="f8879-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="f8879-501">msdyn_start</span></span>                                      | <span data-ttu-id="f8879-502">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-502">no</span></span>             | <span data-ttu-id="f8879-503">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="f8879-504">Project</span><span class="sxs-lookup"><span data-stu-id="f8879-504">Project</span></span>

| <span data-ttu-id="f8879-505">**Logický název**</span><span class="sxs-lookup"><span data-stu-id="f8879-505">**Logical name**</span></span>                       | <span data-ttu-id="f8879-506">**Je možné vytvořit**</span><span class="sxs-lookup"><span data-stu-id="f8879-506">**Can create**</span></span> | <span data-ttu-id="f8879-507">**Může upravit**</span><span class="sxs-lookup"><span data-stu-id="f8879-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="f8879-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="f8879-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="f8879-509">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-509">no</span></span>             | <span data-ttu-id="f8879-510">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-510">no</span></span>           |
| <span data-ttu-id="f8879-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="f8879-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="f8879-512">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-512">no</span></span>             | <span data-ttu-id="f8879-513">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-513">no</span></span>           |
| <span data-ttu-id="f8879-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="f8879-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="f8879-515">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-515">no</span></span>             | <span data-ttu-id="f8879-516">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-516">no</span></span>           |
| <span data-ttu-id="f8879-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="f8879-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="f8879-518">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-518">no</span></span>             | <span data-ttu-id="f8879-519">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-519">no</span></span>           |
| <span data-ttu-id="f8879-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="f8879-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="f8879-521">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-521">no</span></span>             | <span data-ttu-id="f8879-522">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-522">no</span></span>           |
| <span data-ttu-id="f8879-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="f8879-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="f8879-524">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-524">no</span></span>             | <span data-ttu-id="f8879-525">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-525">no</span></span>           |
| <span data-ttu-id="f8879-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="f8879-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="f8879-527">ano</span><span class="sxs-lookup"><span data-stu-id="f8879-527">yes</span></span>            | <span data-ttu-id="f8879-528">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-528">no</span></span>           |
| <span data-ttu-id="f8879-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="f8879-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="f8879-530">ano</span><span class="sxs-lookup"><span data-stu-id="f8879-530">yes</span></span>            | <span data-ttu-id="f8879-531">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-531">no</span></span>           |
| <span data-ttu-id="f8879-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="f8879-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="f8879-533">ano</span><span class="sxs-lookup"><span data-stu-id="f8879-533">yes</span></span>            | <span data-ttu-id="f8879-534">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-534">no</span></span>           |
| <span data-ttu-id="f8879-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="f8879-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="f8879-536">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-536">no</span></span>             | <span data-ttu-id="f8879-537">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-537">no</span></span>           |
| <span data-ttu-id="f8879-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="f8879-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="f8879-539">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-539">no</span></span>             | <span data-ttu-id="f8879-540">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-540">no</span></span>           |
| <span data-ttu-id="f8879-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="f8879-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="f8879-542">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-542">no</span></span>             | <span data-ttu-id="f8879-543">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-543">no</span></span>           |
| <span data-ttu-id="f8879-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="f8879-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="f8879-545">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-545">no</span></span>             | <span data-ttu-id="f8879-546">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-546">no</span></span>           |
| <span data-ttu-id="f8879-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="f8879-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="f8879-548">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-548">no</span></span>             | <span data-ttu-id="f8879-549">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-549">no</span></span>           |
| <span data-ttu-id="f8879-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="f8879-550">msdyn_duration</span></span>                         | <span data-ttu-id="f8879-551">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-551">no</span></span>             | <span data-ttu-id="f8879-552">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-552">no</span></span>           |
| <span data-ttu-id="f8879-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="f8879-553">msdyn_effort</span></span>                           | <span data-ttu-id="f8879-554">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-554">no</span></span>             | <span data-ttu-id="f8879-555">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-555">no</span></span>           |
| <span data-ttu-id="f8879-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f8879-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="f8879-557">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-557">no</span></span>             | <span data-ttu-id="f8879-558">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-558">no</span></span>           |
| <span data-ttu-id="f8879-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="f8879-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="f8879-560">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-560">no</span></span>             | <span data-ttu-id="f8879-561">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-561">no</span></span>           |
| <span data-ttu-id="f8879-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="f8879-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="f8879-563">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-563">no</span></span>             | <span data-ttu-id="f8879-564">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-564">no</span></span>           |
| <span data-ttu-id="f8879-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="f8879-565">msdyn_finish</span></span>                           | <span data-ttu-id="f8879-566">ano</span><span class="sxs-lookup"><span data-stu-id="f8879-566">yes</span></span>            | <span data-ttu-id="f8879-567">ano</span><span class="sxs-lookup"><span data-stu-id="f8879-567">yes</span></span>          |
| <span data-ttu-id="f8879-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="f8879-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="f8879-569">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-569">no</span></span>             | <span data-ttu-id="f8879-570">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-570">no</span></span>           |
| <span data-ttu-id="f8879-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="f8879-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="f8879-572">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-572">no</span></span>             | <span data-ttu-id="f8879-573">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-573">no</span></span>           |
| <span data-ttu-id="f8879-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="f8879-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="f8879-575">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-575">no</span></span>             | <span data-ttu-id="f8879-576">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-576">no</span></span>           |
| <span data-ttu-id="f8879-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="f8879-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="f8879-578">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-578">no</span></span>             | <span data-ttu-id="f8879-579">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-579">no</span></span>           |
| <span data-ttu-id="f8879-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="f8879-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="f8879-581">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-581">no</span></span>             | <span data-ttu-id="f8879-582">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-582">no</span></span>           |
| <span data-ttu-id="f8879-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="f8879-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="f8879-584">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-584">no</span></span>             | <span data-ttu-id="f8879-585">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-585">no</span></span>           |
| <span data-ttu-id="f8879-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="f8879-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="f8879-587">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-587">no</span></span>             | <span data-ttu-id="f8879-588">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-588">no</span></span>           |
| <span data-ttu-id="f8879-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="f8879-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="f8879-590">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-590">no</span></span>             | <span data-ttu-id="f8879-591">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-591">no</span></span>           |
| <span data-ttu-id="f8879-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="f8879-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="f8879-593">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-593">no</span></span>             | <span data-ttu-id="f8879-594">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-594">no</span></span>           |
| <span data-ttu-id="f8879-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="f8879-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="f8879-596">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-596">no</span></span>             | <span data-ttu-id="f8879-597">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-597">no</span></span>           |
| <span data-ttu-id="f8879-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="f8879-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="f8879-599">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-599">no</span></span>             | <span data-ttu-id="f8879-600">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-600">no</span></span>           |
| <span data-ttu-id="f8879-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="f8879-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="f8879-602">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-602">no</span></span>             | <span data-ttu-id="f8879-603">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-603">no</span></span>           |
| <span data-ttu-id="f8879-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="f8879-604">msdyn_progress</span></span>                         | <span data-ttu-id="f8879-605">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-605">no</span></span>             | <span data-ttu-id="f8879-606">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-606">no</span></span>           |
| <span data-ttu-id="f8879-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="f8879-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="f8879-608">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-608">no</span></span>             | <span data-ttu-id="f8879-609">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-609">no</span></span>           |
| <span data-ttu-id="f8879-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="f8879-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="f8879-611">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-611">no</span></span>             | <span data-ttu-id="f8879-612">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-612">no</span></span>           |
| <span data-ttu-id="f8879-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="f8879-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="f8879-614">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-614">no</span></span>             | <span data-ttu-id="f8879-615">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-615">no</span></span>           |
| <span data-ttu-id="f8879-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="f8879-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="f8879-617">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-617">no</span></span>             | <span data-ttu-id="f8879-618">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-618">no</span></span>           |
| <span data-ttu-id="f8879-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="f8879-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="f8879-620">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-620">no</span></span>             | <span data-ttu-id="f8879-621">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-621">no</span></span>           |
| <span data-ttu-id="f8879-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="f8879-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="f8879-623">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-623">no</span></span>             | <span data-ttu-id="f8879-624">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-624">no</span></span>           |
| <span data-ttu-id="f8879-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="f8879-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="f8879-626">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-626">no</span></span>             | <span data-ttu-id="f8879-627">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-627">no</span></span>           |
| <span data-ttu-id="f8879-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="f8879-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="f8879-629">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-629">no</span></span>             | <span data-ttu-id="f8879-630">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-630">no</span></span>           |
| <span data-ttu-id="f8879-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="f8879-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="f8879-632">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-632">no</span></span>             | <span data-ttu-id="f8879-633">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-633">no</span></span>           |
| <span data-ttu-id="f8879-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="f8879-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="f8879-635">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-635">no</span></span>             | <span data-ttu-id="f8879-636">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-636">no</span></span>           |
| <span data-ttu-id="f8879-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="f8879-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="f8879-638">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-638">no</span></span>             | <span data-ttu-id="f8879-639">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-639">no</span></span>           |
| <span data-ttu-id="f8879-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="f8879-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="f8879-641">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-641">no</span></span>             | <span data-ttu-id="f8879-642">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-642">no</span></span>           |
| <span data-ttu-id="f8879-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="f8879-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="f8879-644">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-644">no</span></span>             | <span data-ttu-id="f8879-645">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-645">no</span></span>           |
| <span data-ttu-id="f8879-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="f8879-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="f8879-647">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-647">no</span></span>             | <span data-ttu-id="f8879-648">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-648">no</span></span>           |
| <span data-ttu-id="f8879-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="f8879-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="f8879-650">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-650">no</span></span>             | <span data-ttu-id="f8879-651">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-651">no</span></span>           |
| <span data-ttu-id="f8879-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="f8879-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="f8879-653">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-653">no</span></span>             | <span data-ttu-id="f8879-654">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-654">no</span></span>           |
| <span data-ttu-id="f8879-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="f8879-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="f8879-656">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-656">no</span></span>             | <span data-ttu-id="f8879-657">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-657">no</span></span>           |
| <span data-ttu-id="f8879-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="f8879-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="f8879-659">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-659">no</span></span>             | <span data-ttu-id="f8879-660">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-660">no</span></span>           |
| <span data-ttu-id="f8879-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="f8879-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="f8879-662">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-662">no</span></span>             | <span data-ttu-id="f8879-663">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-663">no</span></span>           |
| <span data-ttu-id="f8879-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="f8879-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="f8879-665">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-665">no</span></span>             | <span data-ttu-id="f8879-666">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-666">no</span></span>           |
| <span data-ttu-id="f8879-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="f8879-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="f8879-668">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-668">no</span></span>             | <span data-ttu-id="f8879-669">ne</span><span class="sxs-lookup"><span data-stu-id="f8879-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="f8879-670">Omezení a známé problémy</span><span class="sxs-lookup"><span data-stu-id="f8879-670">Limitations and known issues</span></span>
<span data-ttu-id="f8879-671">Následuje seznam omezení a známých problémů:</span><span class="sxs-lookup"><span data-stu-id="f8879-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="f8879-672">Rozhraní Schedule API mohou používat pouze **uživatelé s licencí aplikace Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="f8879-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="f8879-673">Nemohou je používat:</span><span class="sxs-lookup"><span data-stu-id="f8879-673">They can't be used by:</span></span>
    - <span data-ttu-id="f8879-674">Uživatelé aplikace</span><span class="sxs-lookup"><span data-stu-id="f8879-674">Application users</span></span>
    - <span data-ttu-id="f8879-675">Systémoví uživatelé</span><span class="sxs-lookup"><span data-stu-id="f8879-675">System users</span></span>
    - <span data-ttu-id="f8879-676">Uživatelé integrace</span><span class="sxs-lookup"><span data-stu-id="f8879-676">Integration users</span></span>
    - <span data-ttu-id="f8879-677">Ostatní uživatelé, kteří nemají požadovanou licenci</span><span class="sxs-lookup"><span data-stu-id="f8879-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="f8879-678">Každá sada **OperationSet** může mít maximálně 100 operací.</span><span class="sxs-lookup"><span data-stu-id="f8879-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="f8879-679">Každý uživatel může mít maximálně 10 otevřených sad **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="f8879-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="f8879-680">Project Operations v současné době podporuje maximálně 500 úkolů v jednom projektu.</span><span class="sxs-lookup"><span data-stu-id="f8879-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="f8879-681">Stav selhání a protokoly selhání nejsou u sad **OperationSet** aktuálně k dispozici.</span><span class="sxs-lookup"><span data-stu-id="f8879-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="f8879-682">Rozhraní Schedule API jsou nyní ve fázi Public Preview.</span><span class="sxs-lookup"><span data-stu-id="f8879-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="f8879-683">Společnost Microsoft nepodporuje používání těchto API v produkčním prostředí.</span><span class="sxs-lookup"><span data-stu-id="f8879-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="f8879-684">Meze a hranice projektů a úkolů</span><span class="sxs-lookup"><span data-stu-id="f8879-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="f8879-685">Zpracování chyb</span><span class="sxs-lookup"><span data-stu-id="f8879-685">Error handling</span></span>

   - <span data-ttu-id="f8879-686">Chcete-li zkontrolovat chyby generované ze sad operací, přejděte na **Nastavení** \> **Naplánovat integraci** \> **Sady operací**.</span><span class="sxs-lookup"><span data-stu-id="f8879-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="f8879-687">Chcete-li zkontrolovat chyby generované službou plánování projektu, přejděte na **Nastavení** \> **Naplánovat integraci** \> **Protokoly chyb PSS**.</span><span class="sxs-lookup"><span data-stu-id="f8879-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="f8879-688">Ukázkový scénář</span><span class="sxs-lookup"><span data-stu-id="f8879-688">Sample scenario</span></span>

<span data-ttu-id="f8879-689">V tomto scénáři vytvoříte projekt, člena týmu, čtyři úkoly a dvě přiřazení prostředků.</span><span class="sxs-lookup"><span data-stu-id="f8879-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="f8879-690">Dále aktualizujete jeden úkol, aktualizujete projekt, odstraníte jeden úkol, odstraníte jedno přiřazení prostředku a vytvoříte závislost úkolu.</span><span class="sxs-lookup"><span data-stu-id="f8879-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="f8879-691">Další ukázky</span><span class="sxs-lookup"><span data-stu-id="f8879-691">Additional samples</span></span>

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
