---
title: Poskytnutí odhadů práce pro projekt během prodejního procesu
description: Postup poskytnutí odhadů práce pro projekt během prodejního procesu v Project Service
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
ms.openlocfilehash: d1daff101f9f0342bb691253fee1290d2335318c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998223"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="d586c-103">Poskytnutí odhadů práce pro projekt během prodejního procesu (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d586c-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d586c-104">Během prodejního procesu můžete vypracovat prodejní odhady od začátku s řádky nabídky.</span><span class="sxs-lookup"><span data-stu-id="d586c-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="d586c-105">Funkce [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v aplikaci [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] přinášejí více vědecký a deterministický způsob vypracování prodejních odhadů prostřednictvím analýzy položek práce a přiřazení příslušných atributů, které přispívají k odhadům pro projekt ve strukturovaném rozpisu prací.</span><span class="sxs-lookup"><span data-stu-id="d586c-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="d586c-106">Jakmile prodej uzavřete, můžete použít přiřazený strukturovaný rozpis prací v plánu projektu a upřesnit jej tak, jak je nutné pro úspěšné dokončení projektu.</span><span class="sxs-lookup"><span data-stu-id="d586c-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="d586c-107">Propojení projektu k řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="d586c-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="d586c-108">Při vytváření řádku nabídky založené na projektu můžete vytvořit nový projekt z řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="d586c-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="d586c-109">Potom můžete použít šablony projektu, což jsou předem nakonfigurované standardní projektové plány a finanční odhady společné ve vaší organizaci nebo kopie plánu projektu a odhady z posledního projektu.</span><span class="sxs-lookup"><span data-stu-id="d586c-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="d586c-110">Když vytvoříte projekt, výběr šablony projektu poskytuje základ pro upřesnění požadavků na plán projektu, odhady a roli.</span><span class="sxs-lookup"><span data-stu-id="d586c-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="d586c-111">Vytvořením projektu z nabídky bude projekt automaticky přidružen k řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="d586c-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="d586c-112">Součásti odhadu projektu</span><span class="sxs-lookup"><span data-stu-id="d586c-112">Project estimate components</span></span>  
 <span data-ttu-id="d586c-113">Strukturovaný rozpis prací v projektu umožňuje rozdělit práci na úkoly, udržovat hierarchii úkolů a přiřadit odhad úsilí potřebného k dokončení jednotlivých úkolů.</span><span class="sxs-lookup"><span data-stu-id="d586c-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="d586c-114">Můžete také přiřadit role k úkolu, čímž označíte odhad typu zdroje potřebného k dokončení úkolu a plánu.</span><span class="sxs-lookup"><span data-stu-id="d586c-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="d586c-115">Strukturovaný rozpis prací vám pomůže určit pracovní úsilí a odhady plánu.</span><span class="sxs-lookup"><span data-stu-id="d586c-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="d586c-116">Ve výchozím nastavení používá projekt výchozí ceníky, které jste definovali dříve.</span><span class="sxs-lookup"><span data-stu-id="d586c-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="d586c-117">Nákladové a prodejní ceny uvedené v seznamech pomáhají určit finanční odhady pro rozpis prací projektu.</span><span class="sxs-lookup"><span data-stu-id="d586c-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="d586c-118">Pokud je projekt přidružen k nabídce a nabídka má jiný než výchozí ceník, je pro finanční odhady použit ceník nabídky.</span><span class="sxs-lookup"><span data-stu-id="d586c-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="d586c-119">Import odhadů z projektu do nabídky</span><span class="sxs-lookup"><span data-stu-id="d586c-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="d586c-120">Jakmile máte odhady projektu v projektu, můžete tyto odhady importovat do řádku nabídky:</span><span class="sxs-lookup"><span data-stu-id="d586c-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="d586c-121">V nabídce **Podrobnosti řádku nabídky** klikněte na tlačítko **Import z odhadů**.</span><span class="sxs-lookup"><span data-stu-id="d586c-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="d586c-122">Vyberte, zda chcete importovat odhady projekt sumarizované podle typu transakce, role nebo úrovně uzlu strukturovaného rozpisu prací.</span><span class="sxs-lookup"><span data-stu-id="d586c-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d586c-123">Viz také</span><span class="sxs-lookup"><span data-stu-id="d586c-123">See Also</span></span>  
 [<span data-ttu-id="d586c-124">Příručka pro projektového manažera</span><span class="sxs-lookup"><span data-stu-id="d586c-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]