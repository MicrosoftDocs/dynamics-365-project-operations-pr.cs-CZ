---
title: Vytvoření šablony projektu
description: Postup vytvoření šablony projektu v Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 148bf1d42b640ff7b58b13bb0c30c7e583d803c8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997233"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="e53f8-103">Vytvoření šablony projektu (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e53f8-103">Create a project template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e53f8-104">Šablony projektů šetří váš čas, pokud se vaše společnost pravidelně uchází o podobné typy projektů.</span><span class="sxs-lookup"><span data-stu-id="e53f8-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="e53f8-105">Poskytují standardní sadu rolí a odhadované hodiny pro typ projektu.</span><span class="sxs-lookup"><span data-stu-id="e53f8-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="e53f8-106">Manažeři zákaznických účtů a vedoucí projektu mohou vytvořit projekty založené na šabloně projektu nebo mohou zkopírovat šablonu a vytvořit svou vlastní.</span><span class="sxs-lookup"><span data-stu-id="e53f8-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="e53f8-107">Součásti šablony projektu</span><span class="sxs-lookup"><span data-stu-id="e53f8-107">Components of project template</span></span>
 <span data-ttu-id="e53f8-108">Šablona projektu se skládá ze tří součástí:</span><span class="sxs-lookup"><span data-stu-id="e53f8-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="e53f8-109">**Strukturovaný rozpis prací**: Strukturovaný rozpis prací v šabloně projektu má stejnou sadu prvků jako v projektu.</span><span class="sxs-lookup"><span data-stu-id="e53f8-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="e53f8-110">Můžete vytvořit hierarchii úkolů, přiřadit role k úkolu, definovat atributy plánu, nastavit závislosti a zobrazit všechna data v Ganttově diagramu.</span><span class="sxs-lookup"><span data-stu-id="e53f8-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="e53f8-111">Strukturované rozpisy prací v šablonách projektů také podporují režimy úkolů pro každý úkol.</span><span class="sxs-lookup"><span data-stu-id="e53f8-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="e53f8-112">Při vytváření pracovního plánu není žádný rozdíl mezi šablonou projektu a projektem.</span><span class="sxs-lookup"><span data-stu-id="e53f8-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="e53f8-113">**Odhady projektu**: Odhady projektu v šablonách fungují stejným způsobem jako v projektech kromě toho, že nákladové a prodejní ceny jsou vždy výchozími nákladovými a prodejními ceníky definovanými v parametrech [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e53f8-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="e53f8-114">Zbývající funkce jsou stejné jako v projektu.</span><span class="sxs-lookup"><span data-stu-id="e53f8-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="e53f8-115">**Vytvoření projektového týmu**: Při vytváření projektového týmu pro šablonu projektu nelze rezervovat pojmenovaný zdroj v šabloně.</span><span class="sxs-lookup"><span data-stu-id="e53f8-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="e53f8-116">Můžete použít možnost **Vygenerovat projektový tým** ve strukturovaném rozpisu prací a vygenerovat sadu obecných zdrojů.</span><span class="sxs-lookup"><span data-stu-id="e53f8-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="e53f8-117">Můžete také určit požadované dovednosti a odborné znalosti pro obecné zdroje.</span><span class="sxs-lookup"><span data-stu-id="e53f8-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="e53f8-118">Nelze nahradit obecný zdroj rezervovatelným zdrojem v šablonách projektů.</span><span class="sxs-lookup"><span data-stu-id="e53f8-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="e53f8-119">Vytvoření projektu ze šablony</span><span class="sxs-lookup"><span data-stu-id="e53f8-119">Create a project from a template</span></span>  
 <span data-ttu-id="e53f8-120">Projekt lze ze šablony vytvořit následujícími způsoby:</span><span class="sxs-lookup"><span data-stu-id="e53f8-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="e53f8-121">Při vytváření projektu z nabídky můžete vybrat šablonu projektu ve formuláři pro rychlé vytvoření projektu.</span><span class="sxs-lookup"><span data-stu-id="e53f8-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="e53f8-122">Při vytváření projektu kliknutím na tlačítko **Nový projekt** se formulář projektu zobrazí před uložením záznamu.</span><span class="sxs-lookup"><span data-stu-id="e53f8-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="e53f8-123">Zde můžete kliknout na pole **Vybrat šablonu** a vybrat požadovanou šablonu ze seznamu předdefinovaných šablon projektů ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="e53f8-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="e53f8-124">Kliknutím na tlačítko **Vytvořit projekt ze šablony** na stránce **Šablona projektu** vytvořte projekt ze šablony.</span><span class="sxs-lookup"><span data-stu-id="e53f8-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="e53f8-125">Kopírování součástí šablony do projektu</span><span class="sxs-lookup"><span data-stu-id="e53f8-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="e53f8-126">Při kopírování součástí šablony do projektu je několik věcí, které byste měli mít na paměti.</span><span class="sxs-lookup"><span data-stu-id="e53f8-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="e53f8-127">**Kopírování strukturovaného rozpisu prací**: Pokud má projekt při kopírování strukturovaného rozpisu prací ze šablony projektu jiný kalendář projektu než šablona, bude v plánu úkolů použita pracovní doba z kalendáře projektu.</span><span class="sxs-lookup"><span data-stu-id="e53f8-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="e53f8-128">Tím se upraví plán pro pomocný kalendář projektu.</span><span class="sxs-lookup"><span data-stu-id="e53f8-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="e53f8-129">A podobně první úkol ve strukturovaném rozpisu prací bude mít datum zahájení projektu, takže zbytek plánu hierarchie úkolů bude aktualizován na základě doby trvání a závislostí, které jsou uvedeny ve strukturovaném rozpisu prací šablony.</span><span class="sxs-lookup"><span data-stu-id="e53f8-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="e53f8-130">**Kopírování odhadů projektu**: Při kopírování mezi řádky odhadů projektu budou ceníky aktualizovány na základě vlastnící jednotky projektu pro nákladový ceník a zákazníka pro prodejní ceník.</span><span class="sxs-lookup"><span data-stu-id="e53f8-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="e53f8-131">Nákladové a prodejní ceny na jednotku se stanovují z těchto ceníků u projektů, které jsou přidruženy k prodejní entitě.</span><span class="sxs-lookup"><span data-stu-id="e53f8-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="e53f8-132">**Kopírování projektového týmu**: Při kopírování projektového týmu z šablony do projektu jsou zkopírovány obecné zdroje spolu s dovednostmi a odbornými znalostmi definovanými v šabloně.</span><span class="sxs-lookup"><span data-stu-id="e53f8-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="e53f8-133">Přiřazení obecných zdrojů je rovněž zachováno jako v šabloně projektu.</span><span class="sxs-lookup"><span data-stu-id="e53f8-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e53f8-134">Viz také</span><span class="sxs-lookup"><span data-stu-id="e53f8-134">See Also</span></span>  
 [<span data-ttu-id="e53f8-135">Příručka pro projektového manažera</span><span class="sxs-lookup"><span data-stu-id="e53f8-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]