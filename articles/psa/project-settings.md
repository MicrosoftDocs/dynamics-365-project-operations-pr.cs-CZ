---
title: Nastavení projektu
description: Toto téma obsahuje informace o nastavení řízení projektu.
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
ms.openlocfilehash: ca5fc63d56ddd84871949e38f421bcdfe38d478e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148140"
---
# <a name="project-settings"></a><span data-ttu-id="811d3-103">Nastavení projektu</span><span class="sxs-lookup"><span data-stu-id="811d3-103">Project settings</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="811d3-104">Pro přístup k funkcím plánování projektu použijte následující nastavení.</span><span class="sxs-lookup"><span data-stu-id="811d3-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="811d3-105">Šablona práce</span><span class="sxs-lookup"><span data-stu-id="811d3-105">Work template</span></span>

<span data-ttu-id="811d3-106">Chcete-li vytvořit plán projektu, vytvořte šablonu projektového kalendáře, který definuje počet pracovních hodin denně a všechny zavírací dny.</span><span class="sxs-lookup"><span data-stu-id="811d3-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="811d3-107">Chcete-li vytvořit šablonu kalendáře projektu, přidružte šablonu práce k poli **Šablona kalendáře** pro projekt.</span><span class="sxs-lookup"><span data-stu-id="811d3-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="811d3-108">Při vytváření šablony práce postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="811d3-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="811d3-109">V PSA klikněte v levém navigačním podokně na **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="811d3-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="811d3-110">Na stránce se seznamem **Zdroje** otevřete záznam uživatele a pak vyberte **Zobrazit pracovní dobu**.</span><span class="sxs-lookup"><span data-stu-id="811d3-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="811d3-111">Ujistěte se, že na stránce prohlížeče povolíte automaticky otevíraná okna.</span><span class="sxs-lookup"><span data-stu-id="811d3-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="811d3-112">To vám umožní zobrazit pracovní hodiny nastavené pro daný zdroj.</span><span class="sxs-lookup"><span data-stu-id="811d3-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="811d3-113">Na kartě **Měsíční zobrazení** klikněte na tlačítko **Nastavit**.</span><span class="sxs-lookup"><span data-stu-id="811d3-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="811d3-114">Zobrazí se seznam se třemi možnostmi:</span><span class="sxs-lookup"><span data-stu-id="811d3-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="811d3-115">Nový týdenní plán</span><span class="sxs-lookup"><span data-stu-id="811d3-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="811d3-116">Pracovní plán na jeden den</span><span class="sxs-lookup"><span data-stu-id="811d3-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="811d3-117">Volno</span><span class="sxs-lookup"><span data-stu-id="811d3-117">Time Off</span></span>

> ![Možnosti nastavení](media/project-13.png)

4. <span data-ttu-id="811d3-119">Vyberte **Nový týdenní plán** a pak nastavte možnosti pro tento plán zdrojů.</span><span class="sxs-lookup"><span data-stu-id="811d3-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="811d3-120">Můžete nastavit opakovaný týdenní plán, parametry denní hodiny, zavírací dny a další.</span><span class="sxs-lookup"><span data-stu-id="811d3-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="811d3-121">Nastavte rozsah kalendářních dat, vyberte **Uložit** a klikněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="811d3-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="811d3-122">Vraťte se zpět na se seznamem **Zdroje** a vyberte zdroj, pro který jste nastavili pracovní dobu.</span><span class="sxs-lookup"><span data-stu-id="811d3-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="811d3-123">Chcete-li nastavit šablonu práce vyberte **Nastavit kalendář jako**.</span><span class="sxs-lookup"><span data-stu-id="811d3-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="811d3-124">V dialogovém **Šablona práce** zadejte název šablony práce a pak vyberte **Použít**.</span><span class="sxs-lookup"><span data-stu-id="811d3-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="811d3-125">Nyní můžete šablonu práce přidružit k šabloně kalendáře projektu.</span><span class="sxs-lookup"><span data-stu-id="811d3-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="811d3-126">Role zdrojů</span><span class="sxs-lookup"><span data-stu-id="811d3-126">Resource roles</span></span>

<span data-ttu-id="811d3-127">Termín *Role zdroje* odkazuje na sadu dovedností, kompetencí a certifikací, které musí osoba mít k provedení specifické sady úkolů na projektu.</span><span class="sxs-lookup"><span data-stu-id="811d3-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="811d3-128">PSA vám umožní použít nákladovou a fakturační sazbu za čas zdroje na základě role, ke které je zdroj přidružen.</span><span class="sxs-lookup"><span data-stu-id="811d3-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="811d3-129">Každá organizace musí tyto role nastavit pomocí navigace vlevo v nabídce **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="811d3-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="811d3-130">Každá organizace musí tyto role nastavit na stránce **Aktivní kategorie zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="811d3-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="811d3-131">Chcete-li tuto stránku otevřít, vyberte v levém navigačním podokně **Role zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="811d3-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="811d3-132">Ceníky</span><span class="sxs-lookup"><span data-stu-id="811d3-132">Price lists</span></span>

<span data-ttu-id="811d3-133">Ceníky vám umožní nastavit nákladové a prodejní ceny pro role zdrojů, kategorie výdajů, produkty a další položky v organizaci.</span><span class="sxs-lookup"><span data-stu-id="811d3-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="811d3-134">Před nastavením finančních odhadů pro práci, která musí být dodána pro projekt, byste měli vytvořit pomocný nákladový a prodejní ceník.</span><span class="sxs-lookup"><span data-stu-id="811d3-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="811d3-135">V sekci parametry byste měli také nastavit výchozí nákladový a prodejní ceník, který se vztahuje na všechny projekty vytvořené v organizaci.</span><span class="sxs-lookup"><span data-stu-id="811d3-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="811d3-136">Na stránce **Aktivní projektové parametry** se ujistěte, že jste nastavili výchozí nákladový a prodejní ceník.</span><span class="sxs-lookup"><span data-stu-id="811d3-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
