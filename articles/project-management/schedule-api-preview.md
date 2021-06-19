---
title: Používání rozhraní Schedule API k provádění operací s entitami plánování
description: Tento téma poskytuje informace a ukázky pro používání rozhraní Schedule API.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116789"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="f5c90-103">Používání rozhraní Schedule API k provádění operací s entitami plánování</span><span class="sxs-lookup"><span data-stu-id="f5c90-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="f5c90-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="f5c90-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="f5c90-105">Některé nebo všechny funkce uvedené v tomto tématu jsou k dispozici jako součást vydání verze Preview.</span><span class="sxs-lookup"><span data-stu-id="f5c90-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="f5c90-106">Obsah a funkce se mohou změnit.</span><span class="sxs-lookup"><span data-stu-id="f5c90-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="f5c90-107">Entity plánování</span><span class="sxs-lookup"><span data-stu-id="f5c90-107">Scheduling entities</span></span>

<span data-ttu-id="f5c90-108">Rozhraní Schedule API poskytuje funkce k vytváření, aktualizaci a odstraňování **entit plánování**.</span><span class="sxs-lookup"><span data-stu-id="f5c90-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="f5c90-109">Tyto entity jsou spravovány prostřednictvím modulu Plánování v aplikaci Project for the Web.</span><span class="sxs-lookup"><span data-stu-id="f5c90-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="f5c90-110">Operace vytváření, aktualizace a odstraňování **entit plánování** byly ve starších verzích Dynamics 365 Project Operations omezeny.</span><span class="sxs-lookup"><span data-stu-id="f5c90-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="f5c90-111">Následující tabulka obsahuje úplný seznam **entit plánování**.</span><span class="sxs-lookup"><span data-stu-id="f5c90-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="f5c90-112">Název entity</span><span class="sxs-lookup"><span data-stu-id="f5c90-112">Entity name</span></span>  | <span data-ttu-id="f5c90-113">Logický název entity</span><span class="sxs-lookup"><span data-stu-id="f5c90-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="f5c90-114">Project</span><span class="sxs-lookup"><span data-stu-id="f5c90-114">Project</span></span> | <span data-ttu-id="f5c90-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="f5c90-115">msdyn_project</span></span> |
| <span data-ttu-id="f5c90-116">Projektový úkol</span><span class="sxs-lookup"><span data-stu-id="f5c90-116">Project Task</span></span>  | <span data-ttu-id="f5c90-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="f5c90-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="f5c90-118">Závislost projektového úkolu</span><span class="sxs-lookup"><span data-stu-id="f5c90-118">Project Task Dependency</span></span>  | <span data-ttu-id="f5c90-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="f5c90-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="f5c90-120">Přiřazení zdroje</span><span class="sxs-lookup"><span data-stu-id="f5c90-120">Resource Assignment</span></span> | <span data-ttu-id="f5c90-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="f5c90-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="f5c90-122">Kbelík projektu</span><span class="sxs-lookup"><span data-stu-id="f5c90-122">Project Bucket</span></span>  | <span data-ttu-id="f5c90-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="f5c90-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="f5c90-124">Člen projektového týmu</span><span class="sxs-lookup"><span data-stu-id="f5c90-124">Project Team Member</span></span> | <span data-ttu-id="f5c90-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="f5c90-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="f5c90-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="f5c90-126">OperationSet</span></span>

<span data-ttu-id="f5c90-127">OperationSet je vzor jednotky práce, který lze použít, když musí být v rámci transakce zpracováno několik požadavků ovlivňujících plány.</span><span class="sxs-lookup"><span data-stu-id="f5c90-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="f5c90-128">Rozhraní Schedule API</span><span class="sxs-lookup"><span data-stu-id="f5c90-128">Schedule APIs</span></span>

<span data-ttu-id="f5c90-129">Následuje seznam aktuálních rozhraní Schedule API.</span><span class="sxs-lookup"><span data-stu-id="f5c90-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="f5c90-130">**msdyn_CreateProjectV1** : Toto API lze použít k vytvoření projektu.</span><span class="sxs-lookup"><span data-stu-id="f5c90-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="f5c90-131">Projekt a výchozí projektový kbelík se vytvoří okamžitě.</span><span class="sxs-lookup"><span data-stu-id="f5c90-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="f5c90-132">**msdyn_CreateTeamMemberV1** : Toto API lze použít k vytvoření člena projektového týmu.</span><span class="sxs-lookup"><span data-stu-id="f5c90-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="f5c90-133">Záznam člena týmu je vytvořen okamžitě.</span><span class="sxs-lookup"><span data-stu-id="f5c90-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="f5c90-134">**msdyn_CreateOperationSetV1** : Toto API lze použít k naplánování několika požadavků, které je třeba provést v rámci transakce.</span><span class="sxs-lookup"><span data-stu-id="f5c90-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="f5c90-135">**msdyn_PSSCreateV1** : Toto API lze použít k vytvoření entity.</span><span class="sxs-lookup"><span data-stu-id="f5c90-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="f5c90-136">Entitou může být libovolná entita plánování, která podporuje operaci vytvoření.</span><span class="sxs-lookup"><span data-stu-id="f5c90-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="f5c90-137">**msdyn_PSSUpdateV1** : Toto API lze použít k aktualizaci entity.</span><span class="sxs-lookup"><span data-stu-id="f5c90-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="f5c90-138">Entitou může být libovolná entita plánování, která podporuje operaci aktualizace.</span><span class="sxs-lookup"><span data-stu-id="f5c90-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="f5c90-139">**msdyn_PSSDeleteV1** : Toto API lze použít k odstranění entity.</span><span class="sxs-lookup"><span data-stu-id="f5c90-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="f5c90-140">Entitou může být libovolná entita plánování, která podporuje operaci odstranění.</span><span class="sxs-lookup"><span data-stu-id="f5c90-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="f5c90-141">**msdyn_ExecuteOperationSetV1** : Toto API se používá k provedení všech operací v rámci dané sady operací.</span><span class="sxs-lookup"><span data-stu-id="f5c90-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="f5c90-142">Používání rozhraní Schedule API s OperationSet</span><span class="sxs-lookup"><span data-stu-id="f5c90-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="f5c90-143">Protože záznamy s oběma rozhraními **CreateProjectV1** a **CreateTeamMemberV1** jsou vytvořeny okamžitě, nelze tato API použít v sadě **OperationSet** přímo.</span><span class="sxs-lookup"><span data-stu-id="f5c90-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="f5c90-144">Můžete však použít API k vytvoření potřebných záznamů, vytvořit sadu **OperationSet** a poté použít tyto předem vytvořené záznamy v sadě **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="f5c90-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="f5c90-145">Podporované operace</span><span class="sxs-lookup"><span data-stu-id="f5c90-145">Supported operations</span></span>

| <span data-ttu-id="f5c90-146">Entita plánování</span><span class="sxs-lookup"><span data-stu-id="f5c90-146">Scheduling entity</span></span> | <span data-ttu-id="f5c90-147">Vytvoření</span><span class="sxs-lookup"><span data-stu-id="f5c90-147">Create</span></span> | <span data-ttu-id="f5c90-148">Aktualizace</span><span class="sxs-lookup"><span data-stu-id="f5c90-148">Update</span></span> | <span data-ttu-id="f5c90-149">Odstranění</span><span class="sxs-lookup"><span data-stu-id="f5c90-149">Delete</span></span> | <span data-ttu-id="f5c90-150">Důležitá poznámka</span><span class="sxs-lookup"><span data-stu-id="f5c90-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="f5c90-151">Projektový úkol</span><span class="sxs-lookup"><span data-stu-id="f5c90-151">Project task</span></span> | <span data-ttu-id="f5c90-152">Ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-152">Yes</span></span> | <span data-ttu-id="f5c90-153">Ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-153">Yes</span></span> | <span data-ttu-id="f5c90-154">Ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-154">Yes</span></span> | <span data-ttu-id="f5c90-155">Nic</span><span class="sxs-lookup"><span data-stu-id="f5c90-155">None</span></span> |
| <span data-ttu-id="f5c90-156">Závislost projektového úkolu</span><span class="sxs-lookup"><span data-stu-id="f5c90-156">Project task dependency</span></span> | <span data-ttu-id="f5c90-157">Ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-157">Yes</span></span> | <span data-ttu-id="f5c90-158">Ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-158">Yes</span></span> | | <span data-ttu-id="f5c90-159">Záznamy závislostí projektových úkolů se neaktualizují.</span><span class="sxs-lookup"><span data-stu-id="f5c90-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="f5c90-160">Místo toho lze starý záznam odstranit a vytvořit nový záznam.</span><span class="sxs-lookup"><span data-stu-id="f5c90-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="f5c90-161">Přiřazení zdroje</span><span class="sxs-lookup"><span data-stu-id="f5c90-161">Resource assignment</span></span> | <span data-ttu-id="f5c90-162">Ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-162">Yes</span></span> | <span data-ttu-id="f5c90-163">Ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-163">Yes</span></span> | | <span data-ttu-id="f5c90-164">Operace s následujícími poli nejsou podporovány: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** a **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="f5c90-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="f5c90-165">Záznamy přiřazení zdrojů se neaktualizují.</span><span class="sxs-lookup"><span data-stu-id="f5c90-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="f5c90-166">Místo toho lze starý záznam odstranit a vytvořit nový záznam.</span><span class="sxs-lookup"><span data-stu-id="f5c90-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="f5c90-167">Kbelík projektu</span><span class="sxs-lookup"><span data-stu-id="f5c90-167">Project bucket</span></span> | <span data-ttu-id="f5c90-168">Není k dispozici</span><span class="sxs-lookup"><span data-stu-id="f5c90-168">N/A</span></span> | <span data-ttu-id="f5c90-169">Není k dispozici</span><span class="sxs-lookup"><span data-stu-id="f5c90-169">N/A</span></span> | <span data-ttu-id="f5c90-170">Není k dispozici</span><span class="sxs-lookup"><span data-stu-id="f5c90-170">N/A</span></span> | <span data-ttu-id="f5c90-171">Výchozí kbelík je vytvořen pomocí rozhraní API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="f5c90-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="f5c90-172">Člen projektového týmu</span><span class="sxs-lookup"><span data-stu-id="f5c90-172">Project team member</span></span> | <span data-ttu-id="f5c90-173">Ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-173">Yes</span></span> | <span data-ttu-id="f5c90-174">Ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-174">Yes</span></span> | <span data-ttu-id="f5c90-175">Ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-175">Yes</span></span> | <span data-ttu-id="f5c90-176">Pro operaci vytvoření použijte API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="f5c90-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="f5c90-177">Project</span><span class="sxs-lookup"><span data-stu-id="f5c90-177">Project</span></span> | <span data-ttu-id="f5c90-178">Ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-178">Yes</span></span> | <span data-ttu-id="f5c90-179">Ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-179">Yes</span></span> | <span data-ttu-id="f5c90-180">Není k dispozici</span><span class="sxs-lookup"><span data-stu-id="f5c90-180">N/A</span></span> | <span data-ttu-id="f5c90-181">Operace s následujícími poli nejsou podporovány: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** a **Duration**.</span><span class="sxs-lookup"><span data-stu-id="f5c90-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="f5c90-182">Tato rozhraní API lze volat s objekty entit, které obsahují vlastní pole.</span><span class="sxs-lookup"><span data-stu-id="f5c90-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="f5c90-183">Vlastnost ID je volitelná.</span><span class="sxs-lookup"><span data-stu-id="f5c90-183">The ID property is optional.</span></span> <span data-ttu-id="f5c90-184">Pokud je k dispozici, systém se pokusí ji použít a vyvolá výjimku, pokud ji nelze použít.</span><span class="sxs-lookup"><span data-stu-id="f5c90-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="f5c90-185">Pokud není k dispozici, systém jej vygeneruje.</span><span class="sxs-lookup"><span data-stu-id="f5c90-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="f5c90-186">Omezená pole</span><span class="sxs-lookup"><span data-stu-id="f5c90-186">Restricted fields</span></span>

<span data-ttu-id="f5c90-187">Následující tabulky definují pole, která mají omezené funkce **Vytvořit** a **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="f5c90-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="f5c90-188">Projektový úkol</span><span class="sxs-lookup"><span data-stu-id="f5c90-188">Project task</span></span>

| <span data-ttu-id="f5c90-189">**Logický název**</span><span class="sxs-lookup"><span data-stu-id="f5c90-189">**Logical name**</span></span>                       | <span data-ttu-id="f5c90-190">**Je možné vytvořit**</span><span class="sxs-lookup"><span data-stu-id="f5c90-190">**Can create**</span></span> | <span data-ttu-id="f5c90-191">**Může upravit**</span><span class="sxs-lookup"><span data-stu-id="f5c90-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="f5c90-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="f5c90-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="f5c90-193">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-193">no</span></span>             | <span data-ttu-id="f5c90-194">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-194">no</span></span>               |
| <span data-ttu-id="f5c90-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="f5c90-196">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-196">no</span></span>             | <span data-ttu-id="f5c90-197">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-197">no</span></span>               |
| <span data-ttu-id="f5c90-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="f5c90-198">msdyn_actualend</span></span>                        | <span data-ttu-id="f5c90-199">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-199">no</span></span>             | <span data-ttu-id="f5c90-200">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-200">no</span></span>               |
| <span data-ttu-id="f5c90-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="f5c90-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="f5c90-202">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-202">no</span></span>             | <span data-ttu-id="f5c90-203">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-203">no</span></span>               |
| <span data-ttu-id="f5c90-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="f5c90-205">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-205">no</span></span>             | <span data-ttu-id="f5c90-206">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-206">no</span></span>               |
| <span data-ttu-id="f5c90-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="f5c90-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="f5c90-208">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-208">no</span></span>             | <span data-ttu-id="f5c90-209">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-209">no</span></span>               |
| <span data-ttu-id="f5c90-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="f5c90-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="f5c90-211">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-211">no</span></span>             | <span data-ttu-id="f5c90-212">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-212">no</span></span>               |
| <span data-ttu-id="f5c90-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="f5c90-214">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-214">no</span></span>             | <span data-ttu-id="f5c90-215">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-215">no</span></span>               |
| <span data-ttu-id="f5c90-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="f5c90-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="f5c90-217">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-217">no</span></span>             | <span data-ttu-id="f5c90-218">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-218">no</span></span>               |
| <span data-ttu-id="f5c90-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f5c90-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="f5c90-220">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-220">no</span></span>             | <span data-ttu-id="f5c90-221">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-221">no</span></span>               |
| <span data-ttu-id="f5c90-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="f5c90-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="f5c90-223">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-223">no</span></span>             | <span data-ttu-id="f5c90-224">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-224">no</span></span>               |
| <span data-ttu-id="f5c90-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="f5c90-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="f5c90-226">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-226">no</span></span>             | <span data-ttu-id="f5c90-227">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-227">no</span></span>               |
| <span data-ttu-id="f5c90-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="f5c90-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="f5c90-229">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-229">no</span></span>             | <span data-ttu-id="f5c90-230">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-230">no</span></span>               |
| <span data-ttu-id="f5c90-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="f5c90-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="f5c90-232">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-232">no</span></span>             | <span data-ttu-id="f5c90-233">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-233">no</span></span>               |
| <span data-ttu-id="f5c90-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="f5c90-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="f5c90-235">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-235">no</span></span>             | <span data-ttu-id="f5c90-236">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-236">no</span></span>               |
| <span data-ttu-id="f5c90-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="f5c90-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="f5c90-238">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-238">no</span></span>             | <span data-ttu-id="f5c90-239">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-239">no</span></span>               |
| <span data-ttu-id="f5c90-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="f5c90-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="f5c90-241">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-241">no</span></span>             | <span data-ttu-id="f5c90-242">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-242">no</span></span>               |
| <span data-ttu-id="f5c90-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="f5c90-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="f5c90-244">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-244">no</span></span>             | <span data-ttu-id="f5c90-245">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-245">no</span></span>               |
| <span data-ttu-id="f5c90-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="f5c90-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="f5c90-247">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-247">no</span></span>             | <span data-ttu-id="f5c90-248">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-248">no</span></span>               |
| <span data-ttu-id="f5c90-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="f5c90-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="f5c90-250">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-250">no</span></span>             | <span data-ttu-id="f5c90-251">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-251">no</span></span>               |
| <span data-ttu-id="f5c90-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="f5c90-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="f5c90-253">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-253">no</span></span>             | <span data-ttu-id="f5c90-254">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-254">no</span></span>               |
| <span data-ttu-id="f5c90-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="f5c90-256">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-256">no</span></span>             | <span data-ttu-id="f5c90-257">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-257">no</span></span>               |
| <span data-ttu-id="f5c90-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="f5c90-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="f5c90-259">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-259">no</span></span>             | <span data-ttu-id="f5c90-260">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-260">no</span></span>               |
| <span data-ttu-id="f5c90-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="f5c90-262">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-262">no</span></span>             | <span data-ttu-id="f5c90-263">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-263">no</span></span>               |
| <span data-ttu-id="f5c90-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="f5c90-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="f5c90-265">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-265">no</span></span>             | <span data-ttu-id="f5c90-266">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-266">no</span></span>               |
| <span data-ttu-id="f5c90-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="f5c90-267">msdyn_progress</span></span>                         | <span data-ttu-id="f5c90-268">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-268">no</span></span>             | <span data-ttu-id="f5c90-269">ne (ano pro P4W)</span><span class="sxs-lookup"><span data-stu-id="f5c90-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="f5c90-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="f5c90-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="f5c90-271">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-271">no</span></span>             | <span data-ttu-id="f5c90-272">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-272">no</span></span>               |
| <span data-ttu-id="f5c90-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="f5c90-274">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-274">no</span></span>             | <span data-ttu-id="f5c90-275">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-275">no</span></span>               |
| <span data-ttu-id="f5c90-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="f5c90-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="f5c90-277">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-277">no</span></span>             | <span data-ttu-id="f5c90-278">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-278">no</span></span>               |
| <span data-ttu-id="f5c90-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="f5c90-280">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-280">no</span></span>             | <span data-ttu-id="f5c90-281">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-281">no</span></span>               |
| <span data-ttu-id="f5c90-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="f5c90-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="f5c90-283">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-283">no</span></span>             | <span data-ttu-id="f5c90-284">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-284">no</span></span>               |
| <span data-ttu-id="f5c90-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="f5c90-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="f5c90-286">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-286">no</span></span>             | <span data-ttu-id="f5c90-287">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-287">no</span></span>               |
| <span data-ttu-id="f5c90-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="f5c90-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="f5c90-289">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-289">no</span></span>             | <span data-ttu-id="f5c90-290">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-290">no</span></span>               |
| <span data-ttu-id="f5c90-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="f5c90-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="f5c90-292">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-292">no</span></span>             | <span data-ttu-id="f5c90-293">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-293">no</span></span>               |
| <span data-ttu-id="f5c90-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="f5c90-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="f5c90-295">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-295">no</span></span>             | <span data-ttu-id="f5c90-296">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-296">no</span></span>               |
| <span data-ttu-id="f5c90-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="f5c90-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="f5c90-298">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-298">no</span></span>             | <span data-ttu-id="f5c90-299">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-299">no</span></span>               |
| <span data-ttu-id="f5c90-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="f5c90-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="f5c90-301">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-301">no</span></span>             | <span data-ttu-id="f5c90-302">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-302">no</span></span>               |
| <span data-ttu-id="f5c90-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="f5c90-304">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-304">no</span></span>             | <span data-ttu-id="f5c90-305">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-305">no</span></span>               |
| <span data-ttu-id="f5c90-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="f5c90-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="f5c90-307">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-307">no</span></span>             | <span data-ttu-id="f5c90-308">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-308">no</span></span>               |
| <span data-ttu-id="f5c90-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="f5c90-310">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-310">no</span></span>             | <span data-ttu-id="f5c90-311">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-311">no</span></span>               |
| <span data-ttu-id="f5c90-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="f5c90-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="f5c90-313">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-313">no</span></span>             | <span data-ttu-id="f5c90-314">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-314">no</span></span>               |
| <span data-ttu-id="f5c90-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="f5c90-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="f5c90-316">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-316">no</span></span>             | <span data-ttu-id="f5c90-317">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-317">no</span></span>               |
| <span data-ttu-id="f5c90-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="f5c90-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="f5c90-319">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-319">no</span></span>             | <span data-ttu-id="f5c90-320">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-320">no</span></span>               |
| <span data-ttu-id="f5c90-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="f5c90-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="f5c90-322">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-322">no</span></span>             | <span data-ttu-id="f5c90-323">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-323">no</span></span>               |
| <span data-ttu-id="f5c90-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="f5c90-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="f5c90-325">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-325">no</span></span>             | <span data-ttu-id="f5c90-326">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-326">no</span></span>               |
| <span data-ttu-id="f5c90-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="f5c90-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="f5c90-328">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-328">no</span></span>             | <span data-ttu-id="f5c90-329">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-329">no</span></span>               |
| <span data-ttu-id="f5c90-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="f5c90-330">msdyn_summary</span></span>                          | <span data-ttu-id="f5c90-331">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-331">no</span></span>             | <span data-ttu-id="f5c90-332">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-332">no</span></span>               |
| <span data-ttu-id="f5c90-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="f5c90-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="f5c90-334">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-334">no</span></span>             | <span data-ttu-id="f5c90-335">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-335">no</span></span>               |
| <span data-ttu-id="f5c90-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="f5c90-337">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-337">no</span></span>             | <span data-ttu-id="f5c90-338">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="f5c90-339">Závislost projektového úkolu</span><span class="sxs-lookup"><span data-stu-id="f5c90-339">Project task dependency</span></span>

| <span data-ttu-id="f5c90-340">**Logický název**</span><span class="sxs-lookup"><span data-stu-id="f5c90-340">**Logical name**</span></span>              | <span data-ttu-id="f5c90-341">**Je možné vytvořit**</span><span class="sxs-lookup"><span data-stu-id="f5c90-341">**Can create**</span></span> | <span data-ttu-id="f5c90-342">**Může upravit**</span><span class="sxs-lookup"><span data-stu-id="f5c90-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="f5c90-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="f5c90-343">msdyn_linktype</span></span>                | <span data-ttu-id="f5c90-344">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-344">no</span></span>             | <span data-ttu-id="f5c90-345">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-345">no</span></span>           |
| <span data-ttu-id="f5c90-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="f5c90-346">msdyn_linktypename</span></span>            | <span data-ttu-id="f5c90-347">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-347">no</span></span>             | <span data-ttu-id="f5c90-348">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-348">no</span></span>           |
| <span data-ttu-id="f5c90-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="f5c90-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="f5c90-350">ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-350">yes</span></span>            | <span data-ttu-id="f5c90-351">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-351">no</span></span>           |
| <span data-ttu-id="f5c90-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="f5c90-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="f5c90-353">ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-353">yes</span></span>            | <span data-ttu-id="f5c90-354">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-354">no</span></span>           |
| <span data-ttu-id="f5c90-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="f5c90-355">msdyn_project</span></span>                 | <span data-ttu-id="f5c90-356">ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-356">yes</span></span>            | <span data-ttu-id="f5c90-357">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-357">no</span></span>           |
| <span data-ttu-id="f5c90-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="f5c90-358">msdyn_projectname</span></span>             | <span data-ttu-id="f5c90-359">ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-359">yes</span></span>            | <span data-ttu-id="f5c90-360">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-360">no</span></span>           |
| <span data-ttu-id="f5c90-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="f5c90-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="f5c90-362">ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-362">yes</span></span>            | <span data-ttu-id="f5c90-363">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-363">no</span></span>           |
| <span data-ttu-id="f5c90-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="f5c90-364">msdyn_successortask</span></span>           | <span data-ttu-id="f5c90-365">ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-365">yes</span></span>            | <span data-ttu-id="f5c90-366">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-366">no</span></span>           |
| <span data-ttu-id="f5c90-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="f5c90-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="f5c90-368">ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-368">yes</span></span>            | <span data-ttu-id="f5c90-369">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="f5c90-370">Přiřazení zdroje</span><span class="sxs-lookup"><span data-stu-id="f5c90-370">Resource assignment</span></span>

| <span data-ttu-id="f5c90-371">**Logický název**</span><span class="sxs-lookup"><span data-stu-id="f5c90-371">**Logical name**</span></span>             | <span data-ttu-id="f5c90-372">**Je možné vytvořit**</span><span class="sxs-lookup"><span data-stu-id="f5c90-372">**Can create**</span></span> | <span data-ttu-id="f5c90-373">**Může upravit**</span><span class="sxs-lookup"><span data-stu-id="f5c90-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="f5c90-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="f5c90-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="f5c90-375">ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-375">yes</span></span>            | <span data-ttu-id="f5c90-376">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-376">no</span></span>           |
| <span data-ttu-id="f5c90-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="f5c90-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="f5c90-378">ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-378">yes</span></span>            | <span data-ttu-id="f5c90-379">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-379">no</span></span>           |
| <span data-ttu-id="f5c90-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="f5c90-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="f5c90-381">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-381">no</span></span>             | <span data-ttu-id="f5c90-382">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-382">no</span></span>           |
| <span data-ttu-id="f5c90-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="f5c90-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="f5c90-384">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-384">no</span></span>             | <span data-ttu-id="f5c90-385">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-385">no</span></span>           |
| <span data-ttu-id="f5c90-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="f5c90-386">msdyn_committype</span></span>             | <span data-ttu-id="f5c90-387">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-387">no</span></span>             | <span data-ttu-id="f5c90-388">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-388">no</span></span>           |
| <span data-ttu-id="f5c90-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="f5c90-389">msdyn_committypename</span></span>         | <span data-ttu-id="f5c90-390">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-390">no</span></span>             | <span data-ttu-id="f5c90-391">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-391">no</span></span>           |
| <span data-ttu-id="f5c90-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="f5c90-392">msdyn_effort</span></span>                 | <span data-ttu-id="f5c90-393">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-393">no</span></span>             | <span data-ttu-id="f5c90-394">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-394">no</span></span>           |
| <span data-ttu-id="f5c90-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f5c90-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="f5c90-396">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-396">no</span></span>             | <span data-ttu-id="f5c90-397">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-397">no</span></span>           |
| <span data-ttu-id="f5c90-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="f5c90-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="f5c90-399">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-399">no</span></span>             | <span data-ttu-id="f5c90-400">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-400">no</span></span>           |
| <span data-ttu-id="f5c90-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="f5c90-401">msdyn_finish</span></span>                 | <span data-ttu-id="f5c90-402">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-402">no</span></span>             | <span data-ttu-id="f5c90-403">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-403">no</span></span>           |
| <span data-ttu-id="f5c90-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="f5c90-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="f5c90-405">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-405">no</span></span>             | <span data-ttu-id="f5c90-406">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-406">no</span></span>           |
| <span data-ttu-id="f5c90-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="f5c90-408">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-408">no</span></span>             | <span data-ttu-id="f5c90-409">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-409">no</span></span>           |
| <span data-ttu-id="f5c90-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="f5c90-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="f5c90-411">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-411">no</span></span>             | <span data-ttu-id="f5c90-412">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-412">no</span></span>           |
| <span data-ttu-id="f5c90-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="f5c90-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="f5c90-414">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-414">no</span></span>             | <span data-ttu-id="f5c90-415">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-415">no</span></span>           |
| <span data-ttu-id="f5c90-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="f5c90-417">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-417">no</span></span>             | <span data-ttu-id="f5c90-418">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-418">no</span></span>           |
| <span data-ttu-id="f5c90-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="f5c90-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="f5c90-420">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-420">no</span></span>             | <span data-ttu-id="f5c90-421">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-421">no</span></span>           |
| <span data-ttu-id="f5c90-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="f5c90-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="f5c90-423">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-423">no</span></span>             | <span data-ttu-id="f5c90-424">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-424">no</span></span>           |
| <span data-ttu-id="f5c90-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="f5c90-425">msdyn_projectid</span></span>              | <span data-ttu-id="f5c90-426">ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-426">yes</span></span>            | <span data-ttu-id="f5c90-427">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-427">no</span></span>           |
| <span data-ttu-id="f5c90-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="f5c90-428">msdyn_projectidname</span></span>          | <span data-ttu-id="f5c90-429">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-429">no</span></span>             | <span data-ttu-id="f5c90-430">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-430">no</span></span>           |
| <span data-ttu-id="f5c90-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="f5c90-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="f5c90-432">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-432">no</span></span>             | <span data-ttu-id="f5c90-433">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-433">no</span></span>           |
| <span data-ttu-id="f5c90-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="f5c90-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="f5c90-435">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-435">no</span></span>             | <span data-ttu-id="f5c90-436">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-436">no</span></span>           |
| <span data-ttu-id="f5c90-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="f5c90-437">msdyn_start</span></span>                  | <span data-ttu-id="f5c90-438">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-438">no</span></span>             | <span data-ttu-id="f5c90-439">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-439">no</span></span>           |
| <span data-ttu-id="f5c90-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="f5c90-440">msdyn_taskid</span></span>                 | <span data-ttu-id="f5c90-441">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-441">no</span></span>             | <span data-ttu-id="f5c90-442">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-442">no</span></span>           |
| <span data-ttu-id="f5c90-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="f5c90-443">msdyn_taskidname</span></span>             | <span data-ttu-id="f5c90-444">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-444">no</span></span>             | <span data-ttu-id="f5c90-445">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-445">no</span></span>           |
| <span data-ttu-id="f5c90-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="f5c90-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="f5c90-447">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-447">no</span></span>             | <span data-ttu-id="f5c90-448">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="f5c90-449">Člen projektového týmu</span><span class="sxs-lookup"><span data-stu-id="f5c90-449">Project team member</span></span>

| <span data-ttu-id="f5c90-450">**Logický název**</span><span class="sxs-lookup"><span data-stu-id="f5c90-450">**Logical name**</span></span>                                 | <span data-ttu-id="f5c90-451">**Je možné vytvořit**</span><span class="sxs-lookup"><span data-stu-id="f5c90-451">**Can create**</span></span> | <span data-ttu-id="f5c90-452">**Může upravit**</span><span class="sxs-lookup"><span data-stu-id="f5c90-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="f5c90-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="f5c90-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="f5c90-454">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-454">no</span></span>             | <span data-ttu-id="f5c90-455">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-455">no</span></span>           |
| <span data-ttu-id="f5c90-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="f5c90-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="f5c90-457">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-457">no</span></span>             | <span data-ttu-id="f5c90-458">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-458">no</span></span>           |
| <span data-ttu-id="f5c90-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="f5c90-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="f5c90-460">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-460">no</span></span>             | <span data-ttu-id="f5c90-461">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-461">no</span></span>           |
| <span data-ttu-id="f5c90-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="f5c90-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="f5c90-463">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-463">no</span></span>             | <span data-ttu-id="f5c90-464">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-464">no</span></span>           |
| <span data-ttu-id="f5c90-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="f5c90-465">msdyn_effort</span></span>                                     | <span data-ttu-id="f5c90-466">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-466">no</span></span>             | <span data-ttu-id="f5c90-467">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-467">no</span></span>           |
| <span data-ttu-id="f5c90-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f5c90-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="f5c90-469">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-469">no</span></span>             | <span data-ttu-id="f5c90-470">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-470">no</span></span>           |
| <span data-ttu-id="f5c90-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="f5c90-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="f5c90-472">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-472">no</span></span>             | <span data-ttu-id="f5c90-473">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-473">no</span></span>           |
| <span data-ttu-id="f5c90-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="f5c90-474">msdyn_finish</span></span>                                     | <span data-ttu-id="f5c90-475">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-475">no</span></span>             | <span data-ttu-id="f5c90-476">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-476">no</span></span>           |
| <span data-ttu-id="f5c90-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="f5c90-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="f5c90-478">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-478">no</span></span>             | <span data-ttu-id="f5c90-479">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-479">no</span></span>           |
| <span data-ttu-id="f5c90-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="f5c90-480">msdyn_hours</span></span>                                      | <span data-ttu-id="f5c90-481">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-481">no</span></span>             | <span data-ttu-id="f5c90-482">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-482">no</span></span>           |
| <span data-ttu-id="f5c90-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="f5c90-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="f5c90-484">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-484">no</span></span>             | <span data-ttu-id="f5c90-485">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-485">no</span></span>           |
| <span data-ttu-id="f5c90-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="f5c90-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="f5c90-487">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-487">no</span></span>             | <span data-ttu-id="f5c90-488">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-488">no</span></span>           |
| <span data-ttu-id="f5c90-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="f5c90-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="f5c90-490">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-490">no</span></span>             | <span data-ttu-id="f5c90-491">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-491">no</span></span>           |
| <span data-ttu-id="f5c90-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="f5c90-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="f5c90-493">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-493">no</span></span>             | <span data-ttu-id="f5c90-494">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-494">no</span></span>           |
| <span data-ttu-id="f5c90-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="f5c90-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="f5c90-496">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-496">no</span></span>             | <span data-ttu-id="f5c90-497">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-497">no</span></span>           |
| <span data-ttu-id="f5c90-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="f5c90-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="f5c90-499">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-499">no</span></span>             | <span data-ttu-id="f5c90-500">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-500">no</span></span>           |
| <span data-ttu-id="f5c90-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="f5c90-501">msdyn_start</span></span>                                      | <span data-ttu-id="f5c90-502">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-502">no</span></span>             | <span data-ttu-id="f5c90-503">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="f5c90-504">Project</span><span class="sxs-lookup"><span data-stu-id="f5c90-504">Project</span></span>

| <span data-ttu-id="f5c90-505">**Logický název**</span><span class="sxs-lookup"><span data-stu-id="f5c90-505">**Logical name**</span></span>                       | <span data-ttu-id="f5c90-506">**Je možné vytvořit**</span><span class="sxs-lookup"><span data-stu-id="f5c90-506">**Can create**</span></span> | <span data-ttu-id="f5c90-507">**Může upravit**</span><span class="sxs-lookup"><span data-stu-id="f5c90-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="f5c90-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="f5c90-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="f5c90-509">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-509">no</span></span>             | <span data-ttu-id="f5c90-510">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-510">no</span></span>           |
| <span data-ttu-id="f5c90-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="f5c90-512">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-512">no</span></span>             | <span data-ttu-id="f5c90-513">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-513">no</span></span>           |
| <span data-ttu-id="f5c90-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="f5c90-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="f5c90-515">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-515">no</span></span>             | <span data-ttu-id="f5c90-516">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-516">no</span></span>           |
| <span data-ttu-id="f5c90-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="f5c90-518">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-518">no</span></span>             | <span data-ttu-id="f5c90-519">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-519">no</span></span>           |
| <span data-ttu-id="f5c90-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="f5c90-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="f5c90-521">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-521">no</span></span>             | <span data-ttu-id="f5c90-522">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-522">no</span></span>           |
| <span data-ttu-id="f5c90-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="f5c90-524">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-524">no</span></span>             | <span data-ttu-id="f5c90-525">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-525">no</span></span>           |
| <span data-ttu-id="f5c90-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="f5c90-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="f5c90-527">ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-527">yes</span></span>            | <span data-ttu-id="f5c90-528">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-528">no</span></span>           |
| <span data-ttu-id="f5c90-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="f5c90-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="f5c90-530">ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-530">yes</span></span>            | <span data-ttu-id="f5c90-531">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-531">no</span></span>           |
| <span data-ttu-id="f5c90-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="f5c90-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="f5c90-533">ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-533">yes</span></span>            | <span data-ttu-id="f5c90-534">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-534">no</span></span>           |
| <span data-ttu-id="f5c90-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="f5c90-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="f5c90-536">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-536">no</span></span>             | <span data-ttu-id="f5c90-537">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-537">no</span></span>           |
| <span data-ttu-id="f5c90-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="f5c90-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="f5c90-539">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-539">no</span></span>             | <span data-ttu-id="f5c90-540">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-540">no</span></span>           |
| <span data-ttu-id="f5c90-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="f5c90-542">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-542">no</span></span>             | <span data-ttu-id="f5c90-543">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-543">no</span></span>           |
| <span data-ttu-id="f5c90-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="f5c90-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="f5c90-545">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-545">no</span></span>             | <span data-ttu-id="f5c90-546">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-546">no</span></span>           |
| <span data-ttu-id="f5c90-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="f5c90-548">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-548">no</span></span>             | <span data-ttu-id="f5c90-549">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-549">no</span></span>           |
| <span data-ttu-id="f5c90-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="f5c90-550">msdyn_duration</span></span>                         | <span data-ttu-id="f5c90-551">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-551">no</span></span>             | <span data-ttu-id="f5c90-552">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-552">no</span></span>           |
| <span data-ttu-id="f5c90-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="f5c90-553">msdyn_effort</span></span>                           | <span data-ttu-id="f5c90-554">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-554">no</span></span>             | <span data-ttu-id="f5c90-555">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-555">no</span></span>           |
| <span data-ttu-id="f5c90-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="f5c90-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="f5c90-557">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-557">no</span></span>             | <span data-ttu-id="f5c90-558">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-558">no</span></span>           |
| <span data-ttu-id="f5c90-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="f5c90-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="f5c90-560">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-560">no</span></span>             | <span data-ttu-id="f5c90-561">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-561">no</span></span>           |
| <span data-ttu-id="f5c90-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="f5c90-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="f5c90-563">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-563">no</span></span>             | <span data-ttu-id="f5c90-564">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-564">no</span></span>           |
| <span data-ttu-id="f5c90-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="f5c90-565">msdyn_finish</span></span>                           | <span data-ttu-id="f5c90-566">ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-566">yes</span></span>            | <span data-ttu-id="f5c90-567">ano</span><span class="sxs-lookup"><span data-stu-id="f5c90-567">yes</span></span>          |
| <span data-ttu-id="f5c90-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="f5c90-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="f5c90-569">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-569">no</span></span>             | <span data-ttu-id="f5c90-570">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-570">no</span></span>           |
| <span data-ttu-id="f5c90-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="f5c90-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="f5c90-572">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-572">no</span></span>             | <span data-ttu-id="f5c90-573">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-573">no</span></span>           |
| <span data-ttu-id="f5c90-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="f5c90-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="f5c90-575">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-575">no</span></span>             | <span data-ttu-id="f5c90-576">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-576">no</span></span>           |
| <span data-ttu-id="f5c90-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="f5c90-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="f5c90-578">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-578">no</span></span>             | <span data-ttu-id="f5c90-579">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-579">no</span></span>           |
| <span data-ttu-id="f5c90-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="f5c90-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="f5c90-581">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-581">no</span></span>             | <span data-ttu-id="f5c90-582">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-582">no</span></span>           |
| <span data-ttu-id="f5c90-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="f5c90-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="f5c90-584">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-584">no</span></span>             | <span data-ttu-id="f5c90-585">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-585">no</span></span>           |
| <span data-ttu-id="f5c90-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="f5c90-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="f5c90-587">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-587">no</span></span>             | <span data-ttu-id="f5c90-588">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-588">no</span></span>           |
| <span data-ttu-id="f5c90-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="f5c90-590">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-590">no</span></span>             | <span data-ttu-id="f5c90-591">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-591">no</span></span>           |
| <span data-ttu-id="f5c90-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="f5c90-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="f5c90-593">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-593">no</span></span>             | <span data-ttu-id="f5c90-594">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-594">no</span></span>           |
| <span data-ttu-id="f5c90-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="f5c90-596">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-596">no</span></span>             | <span data-ttu-id="f5c90-597">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-597">no</span></span>           |
| <span data-ttu-id="f5c90-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="f5c90-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="f5c90-599">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-599">no</span></span>             | <span data-ttu-id="f5c90-600">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-600">no</span></span>           |
| <span data-ttu-id="f5c90-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="f5c90-602">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-602">no</span></span>             | <span data-ttu-id="f5c90-603">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-603">no</span></span>           |
| <span data-ttu-id="f5c90-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="f5c90-604">msdyn_progress</span></span>                         | <span data-ttu-id="f5c90-605">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-605">no</span></span>             | <span data-ttu-id="f5c90-606">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-606">no</span></span>           |
| <span data-ttu-id="f5c90-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="f5c90-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="f5c90-608">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-608">no</span></span>             | <span data-ttu-id="f5c90-609">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-609">no</span></span>           |
| <span data-ttu-id="f5c90-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="f5c90-611">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-611">no</span></span>             | <span data-ttu-id="f5c90-612">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-612">no</span></span>           |
| <span data-ttu-id="f5c90-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="f5c90-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="f5c90-614">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-614">no</span></span>             | <span data-ttu-id="f5c90-615">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-615">no</span></span>           |
| <span data-ttu-id="f5c90-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="f5c90-617">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-617">no</span></span>             | <span data-ttu-id="f5c90-618">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-618">no</span></span>           |
| <span data-ttu-id="f5c90-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="f5c90-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="f5c90-620">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-620">no</span></span>             | <span data-ttu-id="f5c90-621">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-621">no</span></span>           |
| <span data-ttu-id="f5c90-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="f5c90-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="f5c90-623">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-623">no</span></span>             | <span data-ttu-id="f5c90-624">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-624">no</span></span>           |
| <span data-ttu-id="f5c90-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="f5c90-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="f5c90-626">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-626">no</span></span>             | <span data-ttu-id="f5c90-627">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-627">no</span></span>           |
| <span data-ttu-id="f5c90-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="f5c90-629">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-629">no</span></span>             | <span data-ttu-id="f5c90-630">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-630">no</span></span>           |
| <span data-ttu-id="f5c90-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="f5c90-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="f5c90-632">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-632">no</span></span>             | <span data-ttu-id="f5c90-633">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-633">no</span></span>           |
| <span data-ttu-id="f5c90-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="f5c90-635">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-635">no</span></span>             | <span data-ttu-id="f5c90-636">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-636">no</span></span>           |
| <span data-ttu-id="f5c90-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="f5c90-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="f5c90-638">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-638">no</span></span>             | <span data-ttu-id="f5c90-639">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-639">no</span></span>           |
| <span data-ttu-id="f5c90-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="f5c90-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="f5c90-641">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-641">no</span></span>             | <span data-ttu-id="f5c90-642">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-642">no</span></span>           |
| <span data-ttu-id="f5c90-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="f5c90-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="f5c90-644">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-644">no</span></span>             | <span data-ttu-id="f5c90-645">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-645">no</span></span>           |
| <span data-ttu-id="f5c90-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="f5c90-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="f5c90-647">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-647">no</span></span>             | <span data-ttu-id="f5c90-648">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-648">no</span></span>           |
| <span data-ttu-id="f5c90-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="f5c90-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="f5c90-650">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-650">no</span></span>             | <span data-ttu-id="f5c90-651">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-651">no</span></span>           |
| <span data-ttu-id="f5c90-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="f5c90-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="f5c90-653">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-653">no</span></span>             | <span data-ttu-id="f5c90-654">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-654">no</span></span>           |
| <span data-ttu-id="f5c90-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="f5c90-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="f5c90-656">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-656">no</span></span>             | <span data-ttu-id="f5c90-657">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-657">no</span></span>           |
| <span data-ttu-id="f5c90-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="f5c90-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="f5c90-659">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-659">no</span></span>             | <span data-ttu-id="f5c90-660">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-660">no</span></span>           |
| <span data-ttu-id="f5c90-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="f5c90-662">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-662">no</span></span>             | <span data-ttu-id="f5c90-663">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-663">no</span></span>           |
| <span data-ttu-id="f5c90-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="f5c90-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="f5c90-665">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-665">no</span></span>             | <span data-ttu-id="f5c90-666">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-666">no</span></span>           |
| <span data-ttu-id="f5c90-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="f5c90-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="f5c90-668">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-668">no</span></span>             | <span data-ttu-id="f5c90-669">ne</span><span class="sxs-lookup"><span data-stu-id="f5c90-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="f5c90-670">Omezení a známé problémy</span><span class="sxs-lookup"><span data-stu-id="f5c90-670">Limitations and known issues</span></span>
<span data-ttu-id="f5c90-671">Následuje seznam omezení a známých problémů:</span><span class="sxs-lookup"><span data-stu-id="f5c90-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="f5c90-672">Rozhraní Schedule API mohou používat pouze **uživatelé s licencí aplikace Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="f5c90-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="f5c90-673">Nemohou je používat:</span><span class="sxs-lookup"><span data-stu-id="f5c90-673">They can't be used by:</span></span>
    - <span data-ttu-id="f5c90-674">Uživatelé aplikace</span><span class="sxs-lookup"><span data-stu-id="f5c90-674">Application users</span></span>
    - <span data-ttu-id="f5c90-675">Systémoví uživatelé</span><span class="sxs-lookup"><span data-stu-id="f5c90-675">System users</span></span>
    - <span data-ttu-id="f5c90-676">Uživatelé integrace</span><span class="sxs-lookup"><span data-stu-id="f5c90-676">Integration users</span></span>
    - <span data-ttu-id="f5c90-677">Ostatní uživatelé, kteří nemají požadovanou licenci</span><span class="sxs-lookup"><span data-stu-id="f5c90-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="f5c90-678">Každá sada **OperationSet** může mít maximálně 100 operací.</span><span class="sxs-lookup"><span data-stu-id="f5c90-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="f5c90-679">Každý uživatel může mít maximálně 10 otevřených sad **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="f5c90-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="f5c90-680">Project Operations v současné době podporuje maximálně 500 úkolů v jednom projektu.</span><span class="sxs-lookup"><span data-stu-id="f5c90-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="f5c90-681">Stav selhání a protokoly selhání nejsou u sad **OperationSet** aktuálně k dispozici.</span><span class="sxs-lookup"><span data-stu-id="f5c90-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="f5c90-682">Meze a hranice projektů a úkolů</span><span class="sxs-lookup"><span data-stu-id="f5c90-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="f5c90-683">Zpracování chyb</span><span class="sxs-lookup"><span data-stu-id="f5c90-683">Error handling</span></span>

   - <span data-ttu-id="f5c90-684">Chcete-li zkontrolovat chyby generované ze sad operací, přejděte na **Nastavení** \> **Naplánovat integraci** \> **Sady operací**.</span><span class="sxs-lookup"><span data-stu-id="f5c90-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="f5c90-685">Chcete-li zkontrolovat chyby generované službou plánování projektu, přejděte na **Nastavení** \> **Naplánovat integraci** \> **Protokoly chyb PSS**.</span><span class="sxs-lookup"><span data-stu-id="f5c90-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="f5c90-686">Ukázkový scénář</span><span class="sxs-lookup"><span data-stu-id="f5c90-686">Sample scenario</span></span>

<span data-ttu-id="f5c90-687">V tomto scénáři vytvoříte projekt, člena týmu, čtyři úkoly a dvě přiřazení prostředků.</span><span class="sxs-lookup"><span data-stu-id="f5c90-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="f5c90-688">Dále aktualizujete jeden úkol, aktualizujete projekt, odstraníte jeden úkol, odstraníte jedno přiřazení prostředku a vytvoříte závislost úkolu.</span><span class="sxs-lookup"><span data-stu-id="f5c90-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="f5c90-689">Další ukázky</span><span class="sxs-lookup"><span data-stu-id="f5c90-689">Additional samples</span></span>

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
