---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 23, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 23, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 87f89828aeff22d9b473539e294d5cf04d46a203
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150030"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="cc47d-103">Project Service Automation, vydání aktualizace 23, V3</span><span class="sxs-lookup"><span data-stu-id="cc47d-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cc47d-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cc47d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cc47d-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="cc47d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cc47d-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cc47d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cc47d-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="cc47d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cc47d-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cc47d-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cc47d-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 23 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="cc47d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="cc47d-110">Tato verze má číslo sestavení V 3.10.34.30 a je obvykle k dispozici prostřednictvím automatické aktualizace v srpnu 2020.</span><span class="sxs-lookup"><span data-stu-id="cc47d-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="cc47d-111">Aktualizace verze 23</span><span class="sxs-lookup"><span data-stu-id="cc47d-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cc47d-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="cc47d-112">Bug fixes</span></span>

<span data-ttu-id="cc47d-113">**Čas a výdaje**</span><span class="sxs-lookup"><span data-stu-id="cc47d-113">**Time and Expense**</span></span>

<span data-ttu-id="cc47d-114">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="cc47d-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="cc47d-115">Zpracovnání případu hrany v možnosti **Smazat člena projektového týmu** pro poskytnutí smysluplné výjimky.</span><span class="sxs-lookup"><span data-stu-id="cc47d-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="cc47d-116">Výsledky importu přiřazení na prázdné obrazovce pro odebrání.</span><span class="sxs-lookup"><span data-stu-id="cc47d-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="cc47d-117">**Správa zdrojů**</span><span class="sxs-lookup"><span data-stu-id="cc47d-117">**Resource Management**</span></span>

<span data-ttu-id="cc47d-118">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="cc47d-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc47d-119">**Karta zdrojů mřížky využití zrdojů** zobrazuje nesprávná data, pokud je časová stupnice delší než pět dní.</span><span class="sxs-lookup"><span data-stu-id="cc47d-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="cc47d-120">Když zákazníci vytvoří rezervovatelný zdroj, modul plug-in občas selže při automatickém přidání zdroje do skupiny Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="cc47d-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="cc47d-121">Zobrazení **Vyrovnání** ukazuje manuální křivky v zobrazení **Týden** nebo **Měsíc** nesprávně.</span><span class="sxs-lookup"><span data-stu-id="cc47d-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="cc47d-122">**Správa projektů**</span><span class="sxs-lookup"><span data-stu-id="cc47d-122">**Project Management**</span></span>

<span data-ttu-id="cc47d-123">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="cc47d-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc47d-124">Nadměrný počet entit **RetrieveMultiple for usersettings** způsobuje snížený výkon při schvalování projektů a dalších operacích.</span><span class="sxs-lookup"><span data-stu-id="cc47d-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="cc47d-125">Vyhledávání zdrojů v mřížce **Plánování úkolů** je omezeno pouze na zobrazení až pěti členů týmu z projektového týmu.</span><span class="sxs-lookup"><span data-stu-id="cc47d-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="cc47d-126">Vyhledávání zdrojů v mřížce **Plánování úkolů** nefiltruje neaktivní zdroje.</span><span class="sxs-lookup"><span data-stu-id="cc47d-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="cc47d-127">Manuální režim nefunguje podle očekávání ve strukturovaném rozpisu prací při plánování projektu.</span><span class="sxs-lookup"><span data-stu-id="cc47d-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="cc47d-128">Mřížka **Plánování úkolů** ukazuje **Neaktivní kategorie transakcí**.</span><span class="sxs-lookup"><span data-stu-id="cc47d-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="cc47d-129">Mřížka **Přiřazení zdrojů** se zaokrouhlí nesprávně, když má úkol více přiřazení.</span><span class="sxs-lookup"><span data-stu-id="cc47d-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="cc47d-130">Hodnoty zaokrouhlení se liší mezi plánovanými náklady a skutečnými náklady na jeden úkol.</span><span class="sxs-lookup"><span data-stu-id="cc47d-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="cc47d-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cc47d-131">**Sales**</span></span>

<span data-ttu-id="cc47d-132">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="cc47d-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc47d-133">**Načíst všechny kategorie transakcí** při dvojitém kliknutí vytvoří více řádků.</span><span class="sxs-lookup"><span data-stu-id="cc47d-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
