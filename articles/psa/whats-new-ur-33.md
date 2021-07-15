---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 33, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334518"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="47aa2-103">Novinky a změny v aplikaci Project Service Automation, aktualizace verze 33, V3</span><span class="sxs-lookup"><span data-stu-id="47aa2-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="47aa2-104">S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="47aa2-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="47aa2-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="47aa2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="47aa2-106">Je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="47aa2-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="47aa2-107">Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="47aa2-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="47aa2-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="47aa2-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="47aa2-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 33 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="47aa2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="47aa2-110">Tato verze má číslo sestavení V3.10.54.98 a je obecně dostupná prostřednictvím vlastní aktualizace v červenci 2021.</span><span class="sxs-lookup"><span data-stu-id="47aa2-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="47aa2-111">Aktualizace verze 33</span><span class="sxs-lookup"><span data-stu-id="47aa2-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="47aa2-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="47aa2-112">Bug fixes</span></span>

<span data-ttu-id="47aa2-113">**Čas a výdaje**</span><span class="sxs-lookup"><span data-stu-id="47aa2-113">**Time and Expense**</span></span>

<span data-ttu-id="47aa2-114">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="47aa2-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="47aa2-115">Dvě zamčená pole, **msdyn_description** a **msdyn_externaldescription** jsou upravitelné po odeslání.</span><span class="sxs-lookup"><span data-stu-id="47aa2-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="47aa2-116">Chybová zpráva se objeví, pokud je vytvořen výdaj, který nesouvisí s projektem.</span><span class="sxs-lookup"><span data-stu-id="47aa2-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="47aa2-117">Když je vytvořen časový záznam, výchozí role zdroje je neaktivní role.</span><span class="sxs-lookup"><span data-stu-id="47aa2-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="47aa2-118">Řádky deníku spojené s odvolaným a odstraněným výdajem nebudou odstraněny.</span><span class="sxs-lookup"><span data-stu-id="47aa2-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="47aa2-119">Ve **Formuláři pro rychlé vytvoření časového záznamu** aktualizujte zobrazení **Seznam úkolů projektu** pro změnu data zobrazeného vy výchozím nastavení na datum zahájení úkolu.</span><span class="sxs-lookup"><span data-stu-id="47aa2-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="47aa2-120">Když vytvoříte časový záznam z karty **Související** rezervovatelného zdroje, pro přihlášeného uživatele je nesprávně vytvořen časový údaj místo nadřazeného rezervovatelného prostředku.</span><span class="sxs-lookup"><span data-stu-id="47aa2-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="47aa2-121">Do dialogového okna **Hromadné schválení MDD** jsou přidána nová pole.</span><span class="sxs-lookup"><span data-stu-id="47aa2-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="47aa2-122">**Plánování projektu**</span><span class="sxs-lookup"><span data-stu-id="47aa2-122">**Project planning**</span></span>

<span data-ttu-id="47aa2-123">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="47aa2-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="47aa2-124">Pomalý výkon při vytváření projektu, když jsou šablony pracovních hodin projektu použity s komplexními kalendáři.</span><span class="sxs-lookup"><span data-stu-id="47aa2-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="47aa2-125">Když je počáteční datum větší než koncové datum, zobrazí se na šabloně projektu kopírování chyba z důvodu rozdílů v časové složce každého pole.</span><span class="sxs-lookup"><span data-stu-id="47aa2-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="47aa2-126">**Řízení zdrojů**</span><span class="sxs-lookup"><span data-stu-id="47aa2-126">**Resource management**</span></span>

<span data-ttu-id="47aa2-127">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="47aa2-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="47aa2-128">V dotazu na využití prostředků se používá nesprávný parametr a XML vede k nesprávným výsledkům filtrů v mřížce **Využití zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="47aa2-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="47aa2-129">Potvrzení **Rozšířit rezervace** zobrazí nesprávné datum ukončení rezervace.</span><span class="sxs-lookup"><span data-stu-id="47aa2-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="47aa2-130">**Prodej**</span><span class="sxs-lookup"><span data-stu-id="47aa2-130">**Sales**</span></span>

<span data-ttu-id="47aa2-131">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="47aa2-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="47aa2-132">Pokud je cena kategorie vytvořena s chybějícími hodnotami, objeví se chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="47aa2-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="47aa2-133">Objeví se chybová zpráva, pokud je milník řádku smlouvy vytvořen bez řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="47aa2-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
