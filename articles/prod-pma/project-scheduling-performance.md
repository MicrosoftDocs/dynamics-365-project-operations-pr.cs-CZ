---
title: Výkon plánování zdrojů projektu
description: Toto téma poskytuje informace o tom, jak zlepšit výkon plánování zdrojů u velkého počtu projektů.
author: Yowelle
ms.date: 08/31/2020
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
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 113023909f88cb4dd498190ef21b6955482b25dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010013"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="a7842-103">Výkon plánování zdrojů projektu</span><span class="sxs-lookup"><span data-stu-id="a7842-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="a7842-104">Problémy s výkonem u plánování zdrojů mohou nastat, když počet projektů dosáhne tisíců.</span><span class="sxs-lookup"><span data-stu-id="a7842-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="a7842-105">Chcete-li zlepšit výkon plánování zdrojů, je k dispozici funkce, která uživatelům umožňuje zkrátit čas potřebný ke spuštění formuláře dostupnosti zdrojů.</span><span class="sxs-lookup"><span data-stu-id="a7842-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="a7842-106">Konkrétně dojde k odebrání procesu synchronizace shrnutí kapacity zdrojů a použije se tabulka **ResProjectResource** k urychlení vyhledávání zdrojů.</span><span class="sxs-lookup"><span data-stu-id="a7842-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="a7842-107">Poznámka: tabulka **ResRollup** již nebude použita.</span><span class="sxs-lookup"><span data-stu-id="a7842-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7842-108">Pokud existuje závislost buď na procesu synchronizace shrnutí kapacity zdrojů, nebo na tabulce **ResProjectResource**, nepoužívejte tuto funkci.</span><span class="sxs-lookup"><span data-stu-id="a7842-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="a7842-109">Jak povolit vylepšení výkonu plánování zdrojů</span><span class="sxs-lookup"><span data-stu-id="a7842-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="a7842-110">Chcete-li povolit vylepšený výkon při plánování zdrojů, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="a7842-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="a7842-111">Přejděte do nabídky **Správa funkcí** > **Vše** a v seznamu funkcí vyhledejte položku **Povolit funkci vylepšení výkonu plánování zdrojů projektu**.</span><span class="sxs-lookup"><span data-stu-id="a7842-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="a7842-112">Vyberte **Povolit nyní**.</span><span class="sxs-lookup"><span data-stu-id="a7842-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="a7842-113">Pokud nemůžete najít funkci v seznamu, aktualizujte seznam výběrem položky **Kontrola aktualizací**.</span><span class="sxs-lookup"><span data-stu-id="a7842-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="a7842-114">Aktualizujte okno prohlížeče a přejděte na **Řízení projektů a účetnictví** > **Periodické** > **Zdroje projektu** > **Synchronizovat kapacitu kalendářů zdrojů ve všech společnostech**.</span><span class="sxs-lookup"><span data-stu-id="a7842-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="a7842-115">Nastavením položky **Odebrat existující záznamy o kapacitě** na **Ano** odstraníte předchozí data.</span><span class="sxs-lookup"><span data-stu-id="a7842-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="a7842-116">Pokud chcete generovat přírůstková data, nastavte tuto položku na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="a7842-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="a7842-117">V poli **Kód období** vyberte období, ve kterém mají být data generována.</span><span class="sxs-lookup"><span data-stu-id="a7842-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="a7842-118">Když vyberete kód období, není nutné definovat počáteční a koncové datum.</span><span class="sxs-lookup"><span data-stu-id="a7842-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="a7842-119">Když necháte pole **Kód období** prázdné, vyberte konkrétní data zahájení a ukončení pro generování dat.</span><span class="sxs-lookup"><span data-stu-id="a7842-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="a7842-120">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7842-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="a7842-121">Tato akce bude distribuovat obecná data do tabulky **ResCalendarCapacity** napříč všemi společnostmi ve vašem prostředí, takže dávkovou úlohu je třeba spustit pouze v jedné právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="a7842-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="a7842-122">Data v této dávkové úloze jsou potřebná k výpočtu kapacity zdrojů prostřednictvím přidruženého kalendáře.</span><span class="sxs-lookup"><span data-stu-id="a7842-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="a7842-123">Přejděte do nabídky **Řízení projektů a účetnictví** > **Periodické** > **Zdroje projektu** > **Naplnit zdroje projektu napříč všemi společnostmi** a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7842-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="a7842-124">Toto je skript pro aktualizaci obecných dat v tabulkách **ResProjectResource**, **ResCalendarDateTimeRange** a **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="a7842-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="a7842-125">Hodnoty pro pole **PSAPRojSchedRole.RootActivity** se také aktualizují.</span><span class="sxs-lookup"><span data-stu-id="a7842-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="a7842-126">Pokud tato akce není spuštěna, obdržíte varování, když se pokusíte provést operace plánování zdrojů.</span><span class="sxs-lookup"><span data-stu-id="a7842-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="a7842-127">Jak vypnout vylepšení výkonu plánování zdrojů</span><span class="sxs-lookup"><span data-stu-id="a7842-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="a7842-128">Přejděte do nabídky **Správa funkcí** > **Vše** a vyhledejte položku **Povolit funkci vylepšení výkonu plánování zdrojů projektu**.</span><span class="sxs-lookup"><span data-stu-id="a7842-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="a7842-129">Vyberte funkci a poté klikněte na tlačítko **Zakázat**.</span><span class="sxs-lookup"><span data-stu-id="a7842-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="a7842-130">Aktualizujte okno prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="a7842-130">Refresh your browser.</span></span>
4. <span data-ttu-id="a7842-131">Přejděte do nabídky **Řízení projektů a účetnictví** > **Periodické** > **Synchronizace kapacity** > **Synchronizace shrnutí kapacity pro prostředek**.</span><span class="sxs-lookup"><span data-stu-id="a7842-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="a7842-132">Na stránce **Synchronizace shrnutí kapacity** nastavením položky **Odebrat existující záznamy o kapacitě** na **Ano** odstraníte předchozí data.</span><span class="sxs-lookup"><span data-stu-id="a7842-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="a7842-133">Pokud chcete generovat přírůstková data, nastavte tuto položku na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="a7842-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="a7842-134">V poli **Kód období** vyberte období, ve kterém mají být data generována.</span><span class="sxs-lookup"><span data-stu-id="a7842-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="a7842-135">Když vyberete kód období, není nutné definovat počáteční a koncové datum.</span><span class="sxs-lookup"><span data-stu-id="a7842-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="a7842-136">Když necháte pole **Kód období** prázdné, vyberte konkrétní data zahájení a ukončení pro generování dat.</span><span class="sxs-lookup"><span data-stu-id="a7842-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="a7842-137">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7842-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="a7842-138">Tato akce bude distribuovat obecná data do tabulky **ResRollup** napříč všemi společnostmi ve vašem prostředí, takže dávkovou úlohu je třeba spustit pouze v jedné právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="a7842-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="a7842-139">Tato dávková úloha je nutná pro všechny pohledy **Dostupnost zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="a7842-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="a7842-140">Pokud tato dávková úloha není spuštěna, data tabulky **ResRollup** budou generována za chodu, což může chvíli trvat.</span><span class="sxs-lookup"><span data-stu-id="a7842-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]