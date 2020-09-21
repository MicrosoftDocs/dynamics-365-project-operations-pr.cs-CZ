---
title: Co je nového v aktualizaci verze 15 pro aplikaci Project Service Automation V3
description: Tohle téma poskytuje informace o tom, co je nového v aktualizaci verze 15 pro aplikaci Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750332"
---
# <a name="project-service-automation-v3-update-release-15"></a><span data-ttu-id="922c7-103">Project Service Automation V3, aktualizace verze 15</span><span class="sxs-lookup"><span data-stu-id="922c7-103">Project Service Automation V3, Update Release 15</span></span>

<span data-ttu-id="922c7-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="922c7-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="922c7-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="922c7-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="922c7-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="922c7-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="922c7-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 a na stránce řešení nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="922c7-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="922c7-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="922c7-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="922c7-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 15 pro aplikaci PSA V3.</span><span class="sxs-lookup"><span data-stu-id="922c7-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="922c7-110">Tato verze má číslo sestavení V3.10.5.28 a je obvykle k dispozici prostřednictvím automatické aktualizace v lednu 2020.</span><span class="sxs-lookup"><span data-stu-id="922c7-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="922c7-111">Aktualizace verze 15</span><span class="sxs-lookup"><span data-stu-id="922c7-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="922c7-112">Vylepšení</span><span class="sxs-lookup"><span data-stu-id="922c7-112">Enhancements</span></span>

- <span data-ttu-id="922c7-113">Správa projektů</span><span class="sxs-lookup"><span data-stu-id="922c7-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="922c7-114">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="922c7-114">Bug fixes</span></span>

- <span data-ttu-id="922c7-115">Čas a výdaje</span><span class="sxs-lookup"><span data-stu-id="922c7-115">Time and Expense</span></span>

  - <span data-ttu-id="922c7-116">Opraveno: Přidáno zpracování chyb při načítání v zobrazení odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="922c7-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="922c7-117">Opraveno: Centrum projektových zdrojů: Přejmenováno **Množství** pro omezení nejednoznačnosti.</span><span class="sxs-lookup"><span data-stu-id="922c7-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="922c7-118">Opraveno: Upraveno zobrazení **Zkopírovat sloupce časového záznamu**, aby zahrnovalo typ.</span><span class="sxs-lookup"><span data-stu-id="922c7-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="922c7-119">Opraveno: Úprava doby trvání časového záznamu v zobrazení mřížky pomocí desetinných čísel způsobila u některých čísel neznámou chybu.</span><span class="sxs-lookup"><span data-stu-id="922c7-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="922c7-120">Správa projektů</span><span class="sxs-lookup"><span data-stu-id="922c7-120">Project Management</span></span>

  - <span data-ttu-id="922c7-121">Opraveno: Rozevírací nabídka pro **Použít v zobrazení sledování** se nyní rozevírá podle šířky možností.</span><span class="sxs-lookup"><span data-stu-id="922c7-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="922c7-122">Opraveno: Při správě projektů v časovém pásmu +13 mohou výpočty úkolů zobrazovat nepřesné výsledky.</span><span class="sxs-lookup"><span data-stu-id="922c7-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="922c7-123">Opraveno: **Čas ukončení člena týmu** byl opraven při použití 24hodinového kalendáře.</span><span class="sxs-lookup"><span data-stu-id="922c7-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="922c7-124">Opraveno: Znovu aktivován **BPF** v hlavním formuláři **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="922c7-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="922c7-125">Opraveno: Výpočet přiřazení již neignoruje jeden den.</span><span class="sxs-lookup"><span data-stu-id="922c7-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="922c7-126">Opraveno: Do formuláře projektu byl přidán nový oznamovací pruh, když se časové pásmo liší mezi uživatelem a projektem.</span><span class="sxs-lookup"><span data-stu-id="922c7-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="922c7-127">Sales</span><span class="sxs-lookup"><span data-stu-id="922c7-127">Sales</span></span>

  - <span data-ttu-id="922c7-128">Opraveno: Vyhledávání kategorie odhadu nákladů lze použít k filtrování duplikátů.</span><span class="sxs-lookup"><span data-stu-id="922c7-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="922c7-129">Opraveno: Kód v **PluginDomain.ExecuteIn tryCatchBlock(..)** již neskrývá původ výjimky.</span><span class="sxs-lookup"><span data-stu-id="922c7-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="922c7-130">Opraveno: Již se nezobrazí chybová zpráva ve **Vyhledávání projektu** ve formuláři **Řádek nabídky**, pokud existuje více než 1000 projektů.</span><span class="sxs-lookup"><span data-stu-id="922c7-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="922c7-131">Opraveno: Mřížka **Odhady** pro odhady práce a nákladů nyní zobrazuje správný symbol měny.</span><span class="sxs-lookup"><span data-stu-id="922c7-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="922c7-132">Opraveno: Poté, co organizace aktualizuje PSA z aktualizace verze 14 na verzi 15, karta **Plán** se již na formuláři **Projekt** nezobrazuje jako prázdná.</span><span class="sxs-lookup"><span data-stu-id="922c7-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
