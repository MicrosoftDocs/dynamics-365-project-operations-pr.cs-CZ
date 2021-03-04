---
title: Typy období
description: Toto téma poskytuje informace o tom, jak nastavit typy období pro odhad výnosů.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531389"
---
# <a name="period-types"></a><span data-ttu-id="8dc8f-103">Typy období</span><span class="sxs-lookup"><span data-stu-id="8dc8f-103">Period types</span></span>

<span data-ttu-id="8dc8f-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="8dc8f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8dc8f-105">Typ období definuje, jak často se odhadují výnosy z projektu.</span><span class="sxs-lookup"><span data-stu-id="8dc8f-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="8dc8f-106">Toto téma poskytuje informace o tom, jak nastavit typy období pro odhad výnosů.</span><span class="sxs-lookup"><span data-stu-id="8dc8f-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="8dc8f-107">Vytváření a práce s typy období</span><span class="sxs-lookup"><span data-stu-id="8dc8f-107">Create and work with period types</span></span>
<span data-ttu-id="8dc8f-108">Chcete-li vytvořit a pracovat s typy období, proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="8dc8f-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="8dc8f-109">Ve vašem prostředí Dynamics 365 Finance přejděte na **Řízení projektů a účetnictví** > **Založit** > **Odhady** > **Typy období**.</span><span class="sxs-lookup"><span data-stu-id="8dc8f-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="8dc8f-110">Výběrem možnosti **Nový** vytvořte nový typ období.</span><span class="sxs-lookup"><span data-stu-id="8dc8f-110">Select **New** to create new period type.</span></span> <span data-ttu-id="8dc8f-111">Zadejte jméno a popis.</span><span class="sxs-lookup"><span data-stu-id="8dc8f-111">Enter a name and description.</span></span>
3. <span data-ttu-id="8dc8f-112">Vyberte hodnotu poli **Frekvence**:</span><span class="sxs-lookup"><span data-stu-id="8dc8f-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="8dc8f-113">Pokud vyberete **Týden**, **Dvoutýdenní**, **Půlměsíční**, **Měsíc**, **Den**, **Čtvrtletí** nebo **Rok**, kalendář bude použit ke generování období.</span><span class="sxs-lookup"><span data-stu-id="8dc8f-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="8dc8f-114">Pokud vyberete **Období účetní knihy**, k vygenerování období se použijí období hlavní knihy z konfigurace hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="8dc8f-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="8dc8f-115">Pokud vyberete **Neomezený**, můžete zadat vlastní období.</span><span class="sxs-lookup"><span data-stu-id="8dc8f-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="8dc8f-116">Vyberte záznam typu období a poté vyberte **Generovat období** k vytvoření období pro typ období.</span><span class="sxs-lookup"><span data-stu-id="8dc8f-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="8dc8f-117">Na základě zvolené frekvence období můžete mít možnost určit datum zahájení nebo počet období, která se mají vygenerovat.</span><span class="sxs-lookup"><span data-stu-id="8dc8f-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="8dc8f-118">Vyberte **Období**, chcete-li zkontrolovat vygenerovaná období.</span><span class="sxs-lookup"><span data-stu-id="8dc8f-118">Select **Periods** to review generated periods.</span></span>
