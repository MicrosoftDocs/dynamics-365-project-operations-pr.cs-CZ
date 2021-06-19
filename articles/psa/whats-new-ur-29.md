---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 29, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 29, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010463"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="df523-103">Novinky a změny v aplikaci Project Service Automation, aktualizace verze 29, V3</span><span class="sxs-lookup"><span data-stu-id="df523-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="df523-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="df523-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="df523-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="df523-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="df523-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="df523-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="df523-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="df523-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="df523-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="df523-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="df523-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 29 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="df523-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="df523-110">Tato verze má číslo sestavení V3.10.47.7 a je obecně dostupná prostřednictvím vlastní aktualizace v únoru 2021.</span><span class="sxs-lookup"><span data-stu-id="df523-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="df523-111">Aktualizace verze 29</span><span class="sxs-lookup"><span data-stu-id="df523-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="df523-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="df523-112">Bug fixes</span></span>

<span data-ttu-id="df523-113">**Čas a výdaje**</span><span class="sxs-lookup"><span data-stu-id="df523-113">**Time and Expense**</span></span>

<span data-ttu-id="df523-114">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="df523-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="df523-115">Uživatelé nemohou zobrazit pracovní dobu zaprotokolovanou v nepracovní dny v mřížce pro zadávání času.</span><span class="sxs-lookup"><span data-stu-id="df523-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="df523-116">Schválené položky výdajů lze upravovat v mřížce.</span><span class="sxs-lookup"><span data-stu-id="df523-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="df523-117">**Správa projektů**</span><span class="sxs-lookup"><span data-stu-id="df523-117">**Project Management**</span></span>

<span data-ttu-id="df523-118">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="df523-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="df523-119">Chybějící logika ověření, aby se zajistilo, že hodiny úsilí o přiřazení zdrojů nebudou záporné.</span><span class="sxs-lookup"><span data-stu-id="df523-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="df523-120">Vlastní akce, **AssignResourcesForTask** aktualizuje všechna pole namísto pouze změněných polí.</span><span class="sxs-lookup"><span data-stu-id="df523-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="df523-121">Při kopírování projektu v prostředí s doplňky nebo pracovními postupy , které jsou registrovány v události **CreateProject**, není atribut **msdyn_bulkgenerationstatus** aktualizován, pokud **CopyWBSToProject** selže.</span><span class="sxs-lookup"><span data-stu-id="df523-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="df523-122">Když rozbalíte kalendář projektu, pracovní dny nebudou seřazeny vzestupně, což způsobí selhání některých aktualizací úkolů projektu.</span><span class="sxs-lookup"><span data-stu-id="df523-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="df523-123">Změna manažera projektu v existujícím projektu aktivuje výchozí logiku organizační jednotky.</span><span class="sxs-lookup"><span data-stu-id="df523-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="df523-124">**Prodej**</span><span class="sxs-lookup"><span data-stu-id="df523-124">**Sales**</span></span>

<span data-ttu-id="df523-125">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="df523-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="df523-126">Karta **Plnění smlouvy** na stránce **Smlouva** během instalace bezobslužně selže, pokud nejsou k dispozici žádné řádky smlouvy.</span><span class="sxs-lookup"><span data-stu-id="df523-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>