---
title: Granty projektu
description: Toto téma vysvětluje, jak vytvořit nebo upravit grant.
author: RadhikaRS
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8e875ec086ee4c5e2ed3b16adcc6048ac8351ea7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999573"
---
# <a name="project-grants"></a><span data-ttu-id="de652-103">Granty projektu</span><span class="sxs-lookup"><span data-stu-id="de652-103">Project grants</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de652-104">Grant je dar peněz na konkrétní účel nebo projekt.</span><span class="sxs-lookup"><span data-stu-id="de652-104">A grant is a gift of money for a specific purpose or project.</span></span> <span data-ttu-id="de652-105">Obvykle existují omezení, jak lze grant použít.</span><span class="sxs-lookup"><span data-stu-id="de652-105">Usually, there are restrictions on how a grant can be spent.</span></span> <span data-ttu-id="de652-106">V části Řízení projektů a účetnictví můžete granty zadávat a sledovat, a definovat jejich vztahy k projektům a projektovým smlouvám.</span><span class="sxs-lookup"><span data-stu-id="de652-106">In Project management and accounting, you can enter and track grants, and define their relationships to projects and project contracts.</span></span> <span data-ttu-id="de652-107">Můžete například provádět následující úlohy.</span><span class="sxs-lookup"><span data-stu-id="de652-107">For example, you can perform the following tasks:</span></span>

- <span data-ttu-id="de652-108">Přidružte granty k projektům a zdrojům financování prostřednictvím odkazů na stránky **Projekt** a **Podrobnosti o projektové smlouvě**.</span><span class="sxs-lookup"><span data-stu-id="de652-108">Associate grants with projects and funding sources through links to the **Project** and **Project contract details** pages.</span></span>
- <span data-ttu-id="de652-109">Zadejte a sledujte změny grantu při jeho přechodu z jednoho stavu do druhého.</span><span class="sxs-lookup"><span data-stu-id="de652-109">Enter and track changes to a grant as it moves from one status to another.</span></span>
- <span data-ttu-id="de652-110">Zadejte a sledujte náklady, požadované částky a přidělené částky.</span><span class="sxs-lookup"><span data-stu-id="de652-110">Enter and track costs, requested amounts, and awarded amounts.</span></span>
- <span data-ttu-id="de652-111">Vytvořte hlavní granty a přidružte k nim dílčí granty.</span><span class="sxs-lookup"><span data-stu-id="de652-111">Create master grants, and associate subgrants with them.</span></span>

<span data-ttu-id="de652-112">Grant můžete vytvořit zadáním všech podrobností v novém záznamu, nebo můžete zkopírovat podrobnosti z existujícího grantu a poté je aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="de652-112">You can create a grant by entering all the details in a new record, or you can copy the details from an existing grant and then update them.</span></span>

## <a name="create-a-new-grant"></a><span data-ttu-id="de652-113">Vytvoření nového grantu</span><span class="sxs-lookup"><span data-stu-id="de652-113">Create a new grant</span></span>

1. <span data-ttu-id="de652-114">Přejděte do nabídky **Řízení projektů a účetnictví** \> **Granty** \> **Granty**.</span><span class="sxs-lookup"><span data-stu-id="de652-114">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="de652-115">Vyberte příkaz **Nový** \> **Grant**.</span><span class="sxs-lookup"><span data-stu-id="de652-115">Select **New** \> **Grant**.</span></span>
3. <span data-ttu-id="de652-116">Na stránce s podrobnostmi o grantu na pevné záložce **Všeobecné** zapište v poli **ID grantu** alfanumerický identifikátor grantu.</span><span class="sxs-lookup"><span data-stu-id="de652-116">On the grant details page, on the **General** FastTab, in the **Grant ID** field, enter an alphanumeric identifier for the grant.</span></span>
4. <span data-ttu-id="de652-117">V poli **Název grantu** zadejte název nového grantu.</span><span class="sxs-lookup"><span data-stu-id="de652-117">In the **Grant name** field, enter a name for the grant.</span></span>
5. <span data-ttu-id="de652-118">V poli **Popis** přidejte podrobnosti o novém grantu.</span><span class="sxs-lookup"><span data-stu-id="de652-118">In the **Description** field, add details about the new grant.</span></span>

    <span data-ttu-id="de652-119">Většina ostatních polí na stránce je volitelná a můžete v nich zadat tolik informací, kolik chcete.</span><span class="sxs-lookup"><span data-stu-id="de652-119">Most of the other fields on the page are optional, and you can enter as little or as much information as you want.</span></span>

    <span data-ttu-id="de652-120">Následující seznam popisuje informace, které jsou uvedeny na každé pevné záložce stránky s podrobnostmi o grantu:</span><span class="sxs-lookup"><span data-stu-id="de652-120">The following list describes the information that is specified on each FastTab of the grant details page:</span></span>

    - <span data-ttu-id="de652-121">**Všeobecné** – Zadejte název grantu, stav, popis, účel a částku.</span><span class="sxs-lookup"><span data-stu-id="de652-121">**General** – Enter the grant name, status, description, purpose, and amount.</span></span>
    - <span data-ttu-id="de652-122">**Kontaktní informace** – Zadejte podrobnosti o zaměstnancích, oddělení, které spravuje grant, a zdroji grantu (zákazníkovi nebo organizaci).</span><span class="sxs-lookup"><span data-stu-id="de652-122">**Contact information** – Enter details about staff members, the department that manages the grant, and the grant customer or organization source of the grant.</span></span> <span data-ttu-id="de652-123">Můžete také určit, že vaše organizace je předávací entitou, která obdrží grant, a poté jej předá jinému příjemci.</span><span class="sxs-lookup"><span data-stu-id="de652-123">You can also indicate whether your organization is a pass-through entity that receives the grant and then passes it on to another recipient.</span></span> <span data-ttu-id="de652-124">Vyberte **Přidat** a přidejte kontaktní informace, jako jsou telefonní čísla a e-mailové adresy organizace, která poskytuje grant.</span><span class="sxs-lookup"><span data-stu-id="de652-124">Select **Add** to add contact information such as telephone numbers and email addresses for the organization that provides the grant.</span></span>
    - <span data-ttu-id="de652-125">**Data a termíny** – Zadejte data, která se vztahují k grantu a žádosti o grant.</span><span class="sxs-lookup"><span data-stu-id="de652-125">**Dates and deadlines** – Enter dates that are related to the grant and the grant application.</span></span> <span data-ttu-id="de652-126">Mezi příklady patří koncové datum žádosti, datum podání a datum schválení nebo zamítnutí grantu.</span><span class="sxs-lookup"><span data-stu-id="de652-126">Examples include the application due date, the submission date, and the date when the grant is approved or rejected.</span></span>
    - <span data-ttu-id="de652-127">**Přidružené projekty a projektové smlouvy** – Na této pevné záložce můžete zadat informace, pouze pokud je pole **Stav udělení** na pevné záložce **Všeobecné** nastaveno na **Aktivní** nebo **Přidělený**.</span><span class="sxs-lookup"><span data-stu-id="de652-127">**Associated projects and project contracts** – You can enter information on this FastTab only if the **Grant status** field on the **General** FastTab is set to **Active** or **Awarded**.</span></span> <span data-ttu-id="de652-128">Vyberte jednu z následujících možností k dokončení související úlohy:</span><span class="sxs-lookup"><span data-stu-id="de652-128">Select among the following options to complete the related task:</span></span>

        - <span data-ttu-id="de652-129">**Přidat zdroj financování** – Přidejte nový zdroj financování grantu.</span><span class="sxs-lookup"><span data-stu-id="de652-129">**Add funding source** – Add a new funding source for the grant.</span></span> <span data-ttu-id="de652-130">Nyní můžete zadat všechny podrobnosti nebo můžete použít výchozí informace a později je aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="de652-130">You can enter all the details now, or you can use default information and then update it later.</span></span>
        - <span data-ttu-id="de652-131">**Přidat projektovou smlouvu** – Přidejte nebo aktualizujte informace o projektové smlouvě.</span><span class="sxs-lookup"><span data-stu-id="de652-131">**Add project contract** – Add or update project contract information.</span></span>
        - <span data-ttu-id="de652-132">**Přidat projekt** - Přidejte nebo aktualizujte podrobnosti projektu.</span><span class="sxs-lookup"><span data-stu-id="de652-132">**Add project** – Add or update project details.</span></span>

    - <span data-ttu-id="de652-133">**Nastavení** – Zadejte podrobnosti o odpovídajících fondech, pokud jsou tyto informace vyžadovány.</span><span class="sxs-lookup"><span data-stu-id="de652-133">**Setup** – Enter details about matching funds, if this information is required.</span></span> <span data-ttu-id="de652-134">Mnoho organizací, které udělují granty, vyžaduje, aby příjemci utratili konkrétní částku svých vlastních peněz nebo zdrojů, která má odpovídat částce udělené v grantu.</span><span class="sxs-lookup"><span data-stu-id="de652-134">Many organizations that award grants require that recipients spend a specific amount of their own money or resources, to match the amount that is awarded in the grant.</span></span> <span data-ttu-id="de652-135">V poli **Místní projekt nebo ID sledování** můžete zadat identifikátor, který se liší od identifikátoru projektu.</span><span class="sxs-lookup"><span data-stu-id="de652-135">In the **Local project or tracking ID** field, you can enter an identifier that differs from the project identifier.</span></span>

        > [!NOTE]
        > <span data-ttu-id="de652-136">Pokud bude část grantu udělena jiné organizaci, nastavte možnost **Další poskytovatel grantu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="de652-136">If part of the grant will be awarded to a different organization, set the **Subgrantor** option to **Yes**.</span></span> <span data-ttu-id="de652-137">U grantů, které se udělují ve Spojených státech, můžete určit, zda bude grant udělen na základě státního nebo federálního mandátu.</span><span class="sxs-lookup"><span data-stu-id="de652-137">For grants that are awarded in the United States, you can specify whether a grant will be awarded under a state mandate or a federal mandate.</span></span>

    - <span data-ttu-id="de652-138">**Podrobnosti o čerpání** – Přidejte nebo aktualizujte informace o tom, jak často lze prostředky z grantu vybírat, účtovat nebo utrácet.</span><span class="sxs-lookup"><span data-stu-id="de652-138">**Drawdown details** – Add or update information about how often grant funds can be withdrawn, billed for, or spent.</span></span>

## <a name="create-a-new-grant-from-a-copy"></a><span data-ttu-id="de652-139">Vytvoření nového grantu z kopie</span><span class="sxs-lookup"><span data-stu-id="de652-139">Create a new grant from a copy</span></span>

1. <span data-ttu-id="de652-140">Přejděte do nabídky **Řízení projektů a účetnictví** \> **Granty** \> **Granty**.</span><span class="sxs-lookup"><span data-stu-id="de652-140">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="de652-141">Vyberte příkaz **Nový** \> **Kopírovat z grantu**.</span><span class="sxs-lookup"><span data-stu-id="de652-141">Select **New** \> **Copy from grant**.</span></span>
3. <span data-ttu-id="de652-142">Zadejte alfanumerický identifikátor a název nového grantu a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="de652-142">Enter an alphanumeric identifier and a name for the new grant, and then select **OK**.</span></span>
4. <span data-ttu-id="de652-143">Na stránce s podrobnostmi o grantu zkontrolujte detaily zkopírovaného grantu a proveďte potřebné změny.</span><span class="sxs-lookup"><span data-stu-id="de652-143">On the grant details page, review the details of the copied grant, and make any changes that are required.</span></span> <span data-ttu-id="de652-144">Většina polí na stránce je volitelná.</span><span class="sxs-lookup"><span data-stu-id="de652-144">Most of the fields on the page are optional.</span></span>

## <a name="view-or-modify-grant-details"></a><span data-ttu-id="de652-145">Zobrazení nebo úprava podrobností grantu</span><span class="sxs-lookup"><span data-stu-id="de652-145">View or modify grant details</span></span>

1. <span data-ttu-id="de652-146">Přejděte do nabídky **Řízení projektů a účetnictví** \> **Granty** \> **Granty**.</span><span class="sxs-lookup"><span data-stu-id="de652-146">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="de652-147">Vyberte grant, který chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="de652-147">Select the grant to modify.</span></span>
3. <span data-ttu-id="de652-148">V podokně akcí na kartě **Grant** vyberte ve skupině **Udržovat** příkaz **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="de652-148">On the Action Pane, on the **Grant** tab, in the **Maintain** group, select **Edit**.</span></span>
4. <span data-ttu-id="de652-149">Zkontrolujte podrobnosti o grantu a proveďte potřebné změny.</span><span class="sxs-lookup"><span data-stu-id="de652-149">Review the grant details, and make any changes that are required.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]