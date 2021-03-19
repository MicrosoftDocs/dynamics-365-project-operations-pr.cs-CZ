---
title: Vytvoření projektového týmu
description: Toto téma obsahuje informace o způsobu vytváření a správy projektových týmů.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 121a007d91c2da4f3b9951901781757b8bcca8fe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270850"
---
# <a name="create-a-project-team"></a><span data-ttu-id="b3546-103">Vytvoření projektového týmu</span><span class="sxs-lookup"><span data-stu-id="b3546-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3546-104">Chce-li použít role, které byly předtím nastaveny v projektu, musí projektový manažer přidružit role k projektu.</span><span class="sxs-lookup"><span data-stu-id="b3546-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="b3546-105">Projektu lze přiřadit více rolí.</span><span class="sxs-lookup"><span data-stu-id="b3546-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="b3546-106">Aby nedocházelo k nejasnostem, jsou tyto role během rezervace automaticky označeny.</span><span class="sxs-lookup"><span data-stu-id="b3546-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="b3546-107">Například pokud projektový manažer vyžaduje tři softwarové inženýry, jsou automaticky generovány tři role softwarového inženýra, které jsou označeny štítky **softwarový inženýr 1**, **softwarový inženýr 2** a **softwarový inženýr 3**.</span><span class="sxs-lookup"><span data-stu-id="b3546-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="b3546-108">Pokud již byly charakteristiky rolí nastaveny pro roli, použijí se jako filtr během hledání zdrojů.</span><span class="sxs-lookup"><span data-stu-id="b3546-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="b3546-109">Podle potřeby lze přidat další charakteristiky k dalšímu upřesnění vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b3546-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="b3546-110">Nastavení zobrazení lze také přizpůsobit tak, aby poskytovalo lepší přehled o dostupnosti zdrojů.</span><span class="sxs-lookup"><span data-stu-id="b3546-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="b3546-111">K dispozici jsou možnosti zobrazení hodinové, denní, týdenní, měsíční, čtvrtletní a roční dostupnosti.</span><span class="sxs-lookup"><span data-stu-id="b3546-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="b3546-112">K dispozici je také možnost zobrazit dostupnou a zbývající kapacitu zdrojů.</span><span class="sxs-lookup"><span data-stu-id="b3546-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="b3546-113">Tato možnost je užitečná pro správu času, když odhadujete dostupný čas pro aktivity nebo dostupnost zdrojů.</span><span class="sxs-lookup"><span data-stu-id="b3546-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="b3546-114">Projektový manažer může vybrat roli na stránce a poté, pokud existuje dostupný zdroj vyhovující požadavku, vybere rezervaci prostředku, aby naplnil roli.</span><span class="sxs-lookup"><span data-stu-id="b3546-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="b3546-115">Všimněte si, že zdroje nemusí být rezervovány v tomto okamžiku ve fázi plánování.</span><span class="sxs-lookup"><span data-stu-id="b3546-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="b3546-116">Když vytvoříte strukturovaný rozpis prací, můžete role nahradit personálními zdroji pro projekt.</span><span class="sxs-lookup"><span data-stu-id="b3546-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="b3546-117">Pokud jsou role nahrazeny personálními zdroji ve strukturovaném rozpisu prací, nastavení prostředků automaticky aktualizuje seznam a plánování projektového týmu.</span><span class="sxs-lookup"><span data-stu-id="b3546-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="b3546-118">[![Seznam projektového týmu, který zahrnuje role i skutečné zdroje](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="b3546-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="b3546-119">Projektový manažer má různé možnosti rezervace zdroje pro projekt, například **Zbývající kapacita**, **Plná kapacita**, **Procento kapacity** a **Zadat hodiny**.</span><span class="sxs-lookup"><span data-stu-id="b3546-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="b3546-120">Tyto možnosti rezervace lze kdykoli zrušit, pokud se změní přiřazení zdrojů.</span><span class="sxs-lookup"><span data-stu-id="b3546-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="b3546-121">Podporovány jsou dva typy rezervací:</span><span class="sxs-lookup"><span data-stu-id="b3546-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="b3546-122">**Závazná rezervace** – Rezervace zdroje byla schválena a potvrzena pro práci na zakázce po stanovenou dobu.</span><span class="sxs-lookup"><span data-stu-id="b3546-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="b3546-123">**Předběžná rezervace** – Rezervace zdrojů byly pro práci na zakázce po stanovenou dobu nastaveny předběžně.</span><span class="sxs-lookup"><span data-stu-id="b3546-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="b3546-124">Následující procedura vysvětluje, jak vytvořit projektový tým:</span><span class="sxs-lookup"><span data-stu-id="b3546-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="b3546-125">Vytvoření projektového týmu</span><span class="sxs-lookup"><span data-stu-id="b3546-125">Create a project team</span></span>

1. <span data-ttu-id="b3546-126">Na stránce se seznamem **Všechny projekty** vyberte projekt a poté vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="b3546-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="b3546-127">Na kartě **Projektový tým a plánování** zadejte v poli **Naplánovat koncové datum** datum zahájení plánu plus jeden měsíc.</span><span class="sxs-lookup"><span data-stu-id="b3546-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="b3546-128">Pokud je například datum zahájení plánu 24. června 2017 (24. 6. 2017), zadejte **24. 7. 2017**.</span><span class="sxs-lookup"><span data-stu-id="b3546-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="b3546-129">Vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="b3546-129">Select **Add**.</span></span>
4. <span data-ttu-id="b3546-130">V podokně **Přidat role do projektu** vyberte v poli **Role** hodnotu **Vyšší projektový manažer**.</span><span class="sxs-lookup"><span data-stu-id="b3546-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="b3546-131">Vyberte **Požadované kompetence**.</span><span class="sxs-lookup"><span data-stu-id="b3546-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="b3546-132">Na stránce **Vyberte charakteristiky** jsou ve výchozím nastavení vybrány charakteristiky, které jste předtím nastavili pro roli Vyšší projektový manažer.</span><span class="sxs-lookup"><span data-stu-id="b3546-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="b3546-133">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3546-133">Select **OK**.</span></span>
7. <span data-ttu-id="b3546-134">Na stránce **Přidat role do projektu** zadejte v poli **Počet zdrojů** číslo **1**.</span><span class="sxs-lookup"><span data-stu-id="b3546-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="b3546-135">V poli **Zdroj** vyhledávání zobrazí všechny zdroje, které mají požadované kompetence.</span><span class="sxs-lookup"><span data-stu-id="b3546-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="b3546-136">Vyberte položku **Daniel Goldschmidt** a potom vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="b3546-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="b3546-137">Na stránce **Projekt** vyberte příkaz **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="b3546-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="b3546-138">V podokně **Přidat role do projektu** vyberte v poli **Role** hodnotu **Člen týmu**.</span><span class="sxs-lookup"><span data-stu-id="b3546-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="b3546-139">V poli **Počet zdrojů** zadejte **5**.</span><span class="sxs-lookup"><span data-stu-id="b3546-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="b3546-140">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="b3546-140">Select **Create**.</span></span>
12. <span data-ttu-id="b3546-141">Na stránce **Projekty** vyberte **Splnit prostředek**.</span><span class="sxs-lookup"><span data-stu-id="b3546-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="b3546-142">Monitorování projektových týmů</span><span class="sxs-lookup"><span data-stu-id="b3546-142">Monitor project teams</span></span>
1. <span data-ttu-id="b3546-143">Na stránce **Všechny projekty** vyberte odkaz **ID projektu** pro projekt **Fáze 2 upgradu XYZ**.</span><span class="sxs-lookup"><span data-stu-id="b3546-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="b3546-144">Na kartě **Projektový tým a plánování** ověřte, zda jsou projektové zdroje v seznamu správné.</span><span class="sxs-lookup"><span data-stu-id="b3546-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]