---
title: Definování kalendářů zdrojů
description: Toto téma poskytuje informace o tom, jak definovat kalendáře pracovní doby pro zdroje v Project Operations.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5ac834e16afc2f559bee6e10434f7015e8a8e51f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012173"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="79818-103">Definování kalendářů zdrojů</span><span class="sxs-lookup"><span data-stu-id="79818-103">Define resource calendars</span></span>

<span data-ttu-id="79818-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="79818-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="79818-105">Každý rezervovatelný zdroj pracující na projektu musí mít kalendář pracovní doby, aby definoval jejich dostupnost.</span><span class="sxs-lookup"><span data-stu-id="79818-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="79818-106">Pracovní dobu zdroje lze definovat dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="79818-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="79818-107">Definujte jednotlivá pravidla kalendáře pro zdroj</span><span class="sxs-lookup"><span data-stu-id="79818-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="79818-108">Použít pro prostředek existující šablonu kalendáře</span><span class="sxs-lookup"><span data-stu-id="79818-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="79818-109">Definujte pracovní dobu zdroje</span><span class="sxs-lookup"><span data-stu-id="79818-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="79818-110">V nabídce **Zdroje** vyberte **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="79818-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="79818-111">V zobrazení mřížky vyberte příslušný **Rezervovatelný zdroj**.</span><span class="sxs-lookup"><span data-stu-id="79818-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="79818-112">Na stránce **Podrobnosti o zdroji** vyberte kartu **Pracovní doba**. Ve výchozím nastavení je v kalendáři rezervovatelných zdrojů výchozí pracovní doba výchozí šablony pracovní hodiny, která je definována pro organizaci.</span><span class="sxs-lookup"><span data-stu-id="79818-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="79818-113">Chcete-li aktualizovat pracovní dobu, klikněte pravým tlačítkem na datum zahájení navrhovaného pravidla kalendáře, které chcete definovat.</span><span class="sxs-lookup"><span data-stu-id="79818-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="79818-114">Pomocí nabídky pravidel kalendáře můžete definovat pravidlo kalendáře pro konkrétní den, zbytek série nebo celý kalendář.</span><span class="sxs-lookup"><span data-stu-id="79818-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="79818-115">Po výběru možnosti můžete definovat:</span><span class="sxs-lookup"><span data-stu-id="79818-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="79818-116">Den v týdnu, kdy bude platit pracovní doba.</span><span class="sxs-lookup"><span data-stu-id="79818-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="79818-117">Pracovní doba v každém dni.</span><span class="sxs-lookup"><span data-stu-id="79818-117">The working times within each day.</span></span>
    - <span data-ttu-id="79818-118">Časové pásmo kalendářního pravidla.</span><span class="sxs-lookup"><span data-stu-id="79818-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="79818-119">Je-li to relevantní, lze pro pravidlo určit také dobu mimo pracovní dobu.</span><span class="sxs-lookup"><span data-stu-id="79818-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="79818-120">Použití šablony kalendáře na zdroj</span><span class="sxs-lookup"><span data-stu-id="79818-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="79818-121">V nabídce **Zdroje** vyberte **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="79818-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="79818-122">V zobrazení mřížky vyberte až 25 **Rezervovatelných zdrojů** k aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="79818-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="79818-123">Vyberte **Nastavit kalendář** a zobrazí se dialogové okno se seznamem dostupných šablon pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="79818-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="79818-124">Vyberte šablonu, kterou chcete použít, a vyberte **Použít**.</span><span class="sxs-lookup"><span data-stu-id="79818-124">Select the template you want to use, and then select **Apply**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]