---
title: Konfigurace dalšího nastavení parametrů
description: Postup konfigurace nastavení dalších parametrů v Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 73264845808e12950a48eea2b79e54c393d9c024
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151560"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="38beb-103">Konfigurace nastavení dalších parametrů (Project Service)</span><span class="sxs-lookup"><span data-stu-id="38beb-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="38beb-104">Po konfiguraci položek uvedených v předchozích tématech je nutné nastavit další parametry projektu pro vaše projekty.</span><span class="sxs-lookup"><span data-stu-id="38beb-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="38beb-105">Při první instalaci [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] jste vytvořili nastavení parametrů, aby mohly být nejprve vytvořeny všechny záznamy požadované pro fungování [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="38beb-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="38beb-106">Nyní je čas vrátit se zpět a nakonfigurovat další pole pro tato nastavení.</span><span class="sxs-lookup"><span data-stu-id="38beb-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="38beb-107">Je třeba, aby byla nakonfigurována následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="38beb-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="38beb-108">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="38beb-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="38beb-109">Četnost faktur</span><span class="sxs-lookup"><span data-stu-id="38beb-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="38beb-110">Šablona pracovní doby</span><span class="sxs-lookup"><span data-stu-id="38beb-110">Work hours template</span></span>  
  
-   <span data-ttu-id="38beb-111">Ceník</span><span class="sxs-lookup"><span data-stu-id="38beb-111">Price list</span></span>  
 
<span data-ttu-id="38beb-112">V tomto kroku také určíte, jaký typ přidělování zdrojů požadujete:</span><span class="sxs-lookup"><span data-stu-id="38beb-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="38beb-113">**Centrální**.</span><span class="sxs-lookup"><span data-stu-id="38beb-113">**Central**.</span></span> <span data-ttu-id="38beb-114">Pouze správci zdrojů mohou přidělovat zdroje k projektům.</span><span class="sxs-lookup"><span data-stu-id="38beb-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="38beb-115">**Hybridní**.</span><span class="sxs-lookup"><span data-stu-id="38beb-115">**Hybrid**.</span></span> <span data-ttu-id="38beb-116">Správci zdrojů, vedoucí projektů a manažeři zákaznických účtů mohou přidělovat zdroje k projektům.</span><span class="sxs-lookup"><span data-stu-id="38beb-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="38beb-117">Nastavení parametrů projektu:</span><span class="sxs-lookup"><span data-stu-id="38beb-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="38beb-118">Přejděte do nabídky **Project Service > Parametry**.</span><span class="sxs-lookup"><span data-stu-id="38beb-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="38beb-119">Klikněte na nastavení parametrů, které chcete konfigurovat (nastavení, které jste vytvořili při první instalaci [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), nebo kliknutím na tlačítko **Nové** vytvořte nové nastavení.</span><span class="sxs-lookup"><span data-stu-id="38beb-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="38beb-120">V oblasti **Obecné** nastavte všechny možnosti parametrů vašeho projektu.</span><span class="sxs-lookup"><span data-stu-id="38beb-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="38beb-121">V oblasti **Ceník** přidejte ceník kliknutím na tlačítko **+**, vyberte ceník v rozevíracím seznamu **Ceník projektových parametrů** a klikněte na tlačítko **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="38beb-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="38beb-122">Klikněte na tlačítko **Uložit** v pravém dolním rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="38beb-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="38beb-123">Aby aplikace Project Service fungovala správně, musí být zachován záznam parametrů projektu.</span><span class="sxs-lookup"><span data-stu-id="38beb-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="38beb-124">Tento záznam by neměl být vymazán.</span><span class="sxs-lookup"><span data-stu-id="38beb-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="38beb-125">Viz také</span><span class="sxs-lookup"><span data-stu-id="38beb-125">See Also</span></span>  
 [<span data-ttu-id="38beb-126">Nastavení zdrojů</span><span class="sxs-lookup"><span data-stu-id="38beb-126">Set up resources</span></span>](../psa/set-up-resources.md)
