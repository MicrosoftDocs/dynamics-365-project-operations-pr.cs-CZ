---
title: Definování kalendářů projektů
description: Toto téma poskytuje informace o používání kalendáře projektu ke sledování plánu projektu.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 442a901af8754fa0335bbf43f4ac8c73b11f9499
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131650"
---
# <a name="define-project-calendars"></a><span data-ttu-id="24a0e-103">Definování kalendářů projektů</span><span class="sxs-lookup"><span data-stu-id="24a0e-103">Define project calendars</span></span>

<span data-ttu-id="24a0e-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="24a0e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="24a0e-105">Chcete-li vytvořit plán projektu, vytvořte šablonu projektového kalendáře, který definuje počet pracovních hodin denně a všechny zavírací dny.</span><span class="sxs-lookup"><span data-stu-id="24a0e-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="24a0e-106">Chcete-li vytvořit šablonu kalendáře projektu, přidružte šablonu práce k poli **Šablona kalendáře** pro projekt.</span><span class="sxs-lookup"><span data-stu-id="24a0e-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="24a0e-107">Při vytváření šablony práce postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="24a0e-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="24a0e-108">V levém navigačním podokně vyberte **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="24a0e-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="24a0e-109">Na stránce se seznamem **Zdroje** otevřete záznam uživatele a pak vyberte **Zobrazit pracovní dobu**.</span><span class="sxs-lookup"><span data-stu-id="24a0e-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="24a0e-110">Ujistěte se, že na stránce prohlížeče povolíte automaticky otevíraná okna.</span><span class="sxs-lookup"><span data-stu-id="24a0e-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="24a0e-111">To vám umožní zobrazit pracovní hodiny nastavené pro daný zdroj.</span><span class="sxs-lookup"><span data-stu-id="24a0e-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="24a0e-112">Na kartě **Měsíční zobrazení** vyberte **Nastavit**.</span><span class="sxs-lookup"><span data-stu-id="24a0e-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="24a0e-113">Zobrazí se seznam se třemi možnostmi:</span><span class="sxs-lookup"><span data-stu-id="24a0e-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="24a0e-114">Nový týdenní plán</span><span class="sxs-lookup"><span data-stu-id="24a0e-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="24a0e-115">Pracovní plán na jeden den</span><span class="sxs-lookup"><span data-stu-id="24a0e-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="24a0e-116">Volno</span><span class="sxs-lookup"><span data-stu-id="24a0e-116">Time Off</span></span>

4. <span data-ttu-id="24a0e-117">Vyberte **Nový týdenní plán** a pak nastavte možnosti pro tento plán zdrojů.</span><span class="sxs-lookup"><span data-stu-id="24a0e-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="24a0e-118">Můžete nastavit opakovaný týdenní plán, parametry denní hodiny, zavírací dny a další.</span><span class="sxs-lookup"><span data-stu-id="24a0e-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="24a0e-119">Nastavte rozsah kalendářních dat, vyberte **Uložit** a vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="24a0e-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="24a0e-120">Vraťte se zpět na se seznamem **Zdroje** a vyberte zdroj, pro který jste nastavili pracovní dobu.</span><span class="sxs-lookup"><span data-stu-id="24a0e-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="24a0e-121">Chcete-li nastavit šablonu práce vyberte **Nastavit kalendář jako**.</span><span class="sxs-lookup"><span data-stu-id="24a0e-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="24a0e-122">V dialogovém **Šablona práce** zadejte název šablony práce a pak vyberte **Použít**.</span><span class="sxs-lookup"><span data-stu-id="24a0e-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="24a0e-123">Nyní můžete šablonu práce přidružit k šabloně kalendáře projektu.</span><span class="sxs-lookup"><span data-stu-id="24a0e-123">You can now associate the work template with a project calendar template.</span></span>
