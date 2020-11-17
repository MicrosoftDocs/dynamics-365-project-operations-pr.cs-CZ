---
title: Konfigurace rolí zdrojů
description: Postup konfigurace rolí zdrojů v Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 5f899d17980df16602c964bab4bbab1e976b3ebf
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073778"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="058bc-103">Konfigurace rolí zdrojů (Project Service)</span><span class="sxs-lookup"><span data-stu-id="058bc-103">Configure resource roles (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="058bc-104">Role hrají důležitou roli v plánování projektů, když stanovujete požadavky na zdroje nebo náklady projektu.</span><span class="sxs-lookup"><span data-stu-id="058bc-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="058bc-105">Pro každou roli, kterou projekty vyžadují, je nutné vytvořit roli zdroje a přiřadit k této roli dovednosti a odborné znalosti.</span><span class="sxs-lookup"><span data-stu-id="058bc-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="058bc-106">Můžete například vytvořit role pro vývojáře, vedoucího projektu nebo testera her.</span><span class="sxs-lookup"><span data-stu-id="058bc-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="058bc-107">Také nastavíte úrovně dovedností a odborné způsobilosti nezbytné pro roli.</span><span class="sxs-lookup"><span data-stu-id="058bc-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="058bc-108">Konfigurace rolí zdrojů vám pomůže zajistit účinný odhad projektu pro vaši organizaci.</span><span class="sxs-lookup"><span data-stu-id="058bc-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="058bc-109">Ujistěte se také, že přesně nastavíte typ účtování.</span><span class="sxs-lookup"><span data-stu-id="058bc-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="058bc-110">Položka nastavená s nefakturovatelným typem účtování se nezobrazí na řádcích smlouvy nebo nabídky.</span><span class="sxs-lookup"><span data-stu-id="058bc-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="058bc-111">Po nastavení rolí zdrojů můžete pomocí ceníku nastavit náklady a prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="058bc-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="058bc-112">Pro každou roli, kterou chcete přidat, proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="058bc-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="058bc-113">Přejděte do nabídky **Project Service > Role zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="058bc-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="058bc-114">Klikněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="058bc-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="058bc-115">V oblasti **Obecné** do pole Název zadejte roli do pole **Název** a potom podle potřeby vyplňte ostatní pole.</span><span class="sxs-lookup"><span data-stu-id="058bc-115">In the **General** area, enter a name for the role in **Name** , and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="058bc-116">Kliknutím na tlačítko **Uložit** vytvořte záznam, abyste mohli pokračovat v jeho úpravách.</span><span class="sxs-lookup"><span data-stu-id="058bc-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="058bc-117">V oblasti **Dovednosti** kliknutím na položku **+** přidejte dovednost.</span><span class="sxs-lookup"><span data-stu-id="058bc-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="058bc-118">V podokně **Požadavky na kompetence role** klikněte do pole **Dovednost** , poté na tlačítko **Hledat** a potom vyberte dovednost.</span><span class="sxs-lookup"><span data-stu-id="058bc-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="058bc-119">Vyberte odborné způsobilosti pro dovednost a poté klikněte na tlačítko **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="058bc-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="058bc-120">Pokračujte podle potřeby v přidávání dovedností.</span><span class="sxs-lookup"><span data-stu-id="058bc-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="058bc-121">Když jste hotovi, klikněte na tlačítko **Uložit** v pravém dolním rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="058bc-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="058bc-122">Chcete-li tuto roli zdroje zpřístupnit pro projekty, klikněte na tlačítko **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="058bc-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="058bc-123">Viz také</span><span class="sxs-lookup"><span data-stu-id="058bc-123">See Also</span></span>  
 [<span data-ttu-id="058bc-124">Nastavení zdrojů</span><span class="sxs-lookup"><span data-stu-id="058bc-124">Set up resources</span></span>](../psa/set-up-resources.md)