---
title: Odhady prodeje a projekty
description: Toto téma obsahuje informace o způsobu využití plánu a odhadů v prodejním procesu.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d8bb380519759659dc1b4151b62228a626ee7a26
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120670"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="fdebd-103">Odhady prodeje a projekty</span><span class="sxs-lookup"><span data-stu-id="fdebd-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fdebd-104">Během prodejního procesu můžete vytvořit odhady prodeje propojením projektu s prodejní nabídkou.</span><span class="sxs-lookup"><span data-stu-id="fdebd-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="fdebd-105">Tímto způsobem může během prodejního procesu proběhnout deterministický odhad, aby bylo možné využít funkce plánování a odhadů projektů.</span><span class="sxs-lookup"><span data-stu-id="fdebd-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="fdebd-106">Pokud prodej projde, lze jako základ pro další upřesnění plánu projektu použít plán, který byl použit pro účely odhadu prodeje.</span><span class="sxs-lookup"><span data-stu-id="fdebd-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="fdebd-107">Propojení projektu k řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="fdebd-107">Linking a project to a quote line</span></span>

<span data-ttu-id="fdebd-108">Při vytváření řádku nabídky založeného na projektu můžete vytvořit nový projekt nebo přidružit existující projekt na stránce **Řádek nabídky**.</span><span class="sxs-lookup"><span data-stu-id="fdebd-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Formulář Řádek nabídky](media/project-8.png)
 
<span data-ttu-id="fdebd-110">Při vytváření nového projektu z podrobností řádku nabídky můžete využít šablony projektů.</span><span class="sxs-lookup"><span data-stu-id="fdebd-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="fdebd-111">Šablony projektů jsou modelové projekty, které představují standardní plány projektů a finanční odhady, které jsou v organizaci typické.</span><span class="sxs-lookup"><span data-stu-id="fdebd-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="fdebd-112">Mohou také představovat kopie projektových plánů a odhadů z minulých projektů.</span><span class="sxs-lookup"><span data-stu-id="fdebd-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Podrobnosti řádku nabídky](media/project-9.png)
  
<span data-ttu-id="fdebd-114">Při vytváření projektu z nabídky bude projekt automaticky přidružen k řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="fdebd-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="fdebd-115">Komponenty odhadů v projektu</span><span class="sxs-lookup"><span data-stu-id="fdebd-115">Components of estimates in a project</span></span>

<span data-ttu-id="fdebd-116">Plán vám umožňuje rozdělit práci na úkoly, udržovat hierarchii úkolů, zjistit, jaké zdroje jsou požadovány k dokončení úkolu, a přiřadit odhad úsilí, které je nutné k dokončení úkolu.</span><span class="sxs-lookup"><span data-stu-id="fdebd-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="fdebd-117">Odhady pracovního úsilí a plánování můžete definovat pomocí polí na kartě **Plán** na stránce **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="fdebd-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="fdebd-118">Vzhledem k tomu, že je k projektu přidružen ceník, jsou finanční odhady vypočteny pomocí nákladových a prodejních cen, které jsou definovány v ceníku.</span><span class="sxs-lookup"><span data-stu-id="fdebd-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="fdebd-119">Import odhadů z projektu do nabídky</span><span class="sxs-lookup"><span data-stu-id="fdebd-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="fdebd-120">Po definování odhadů projektu je můžete importovat do řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="fdebd-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="fdebd-121">Chcete-li odhady projektu shrnout podle typu transakce, role nebo úrovně úkolu, vyberte na stránce **Podrobnosti řádku nabídky** na pásu karet **Import z odhadů**.</span><span class="sxs-lookup"><span data-stu-id="fdebd-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
