---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 32, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129658"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="52eac-103">Novinky a změny v aplikaci Project Service Automation, aktualizace verze 32, V3</span><span class="sxs-lookup"><span data-stu-id="52eac-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="52eac-104">S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="52eac-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="52eac-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="52eac-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="52eac-106">Je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="52eac-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="52eac-107">Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="52eac-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="52eac-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="52eac-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="52eac-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 32 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="52eac-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="52eac-110">Tato verze má číslo sestavení V3.10.53.108 a je obecně dostupná prostřednictvím samostatné aktualizace v červnu 2021.</span><span class="sxs-lookup"><span data-stu-id="52eac-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="52eac-111">Aktualizace verze 32</span><span class="sxs-lookup"><span data-stu-id="52eac-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="52eac-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="52eac-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="52eac-113">Obecná</span><span class="sxs-lookup"><span data-stu-id="52eac-113">General</span></span>

- <span data-ttu-id="52eac-114">Když hlavní upgrade selže, je třeba zablokovat pouze hlavní vstupní body aplikace, aby bylo zajištěno, že sdílené entity jsou stále přístupné.</span><span class="sxs-lookup"><span data-stu-id="52eac-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="52eac-115">Čas a výdaje</span><span class="sxs-lookup"><span data-stu-id="52eac-115">Time and Expense</span></span>

<span data-ttu-id="52eac-116">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="52eac-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="52eac-117">**TimeEntriesImportFromResourceAssignment** neudržuje počáteční a koncový čas obrysového řezu přiřazení prostředků.</span><span class="sxs-lookup"><span data-stu-id="52eac-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="52eac-118">Když vyberete **Otevřít vstup** na mřížce **Zadání času** mřížce, může vám to bránit ve výběru jiných formulářů.</span><span class="sxs-lookup"><span data-stu-id="52eac-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="52eac-119">Při importu přiřazení k časovým položkám může dotaz na kód klienta vygenerovat dlouhou adresu URL, ve které se dotaz nezdaří.</span><span class="sxs-lookup"><span data-stu-id="52eac-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="52eac-120">V mřížce **Zadání času** poté, co je hodnota odstraněna z buňky, zaměření nezůstane v mřížce.</span><span class="sxs-lookup"><span data-stu-id="52eac-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="52eac-121">Tlačítko **Odmítnout** bylo odstraněno z pohledu **Zpracování schválení** u moderního schvalování.</span><span class="sxs-lookup"><span data-stu-id="52eac-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="52eac-122">Stabilita a výkon hromadného schválení časového vstupu jsou ovlivněny zablokováním a selháním vhodného zpracování přizpůsobení, které souvisí s entitou **Zadání času**.</span><span class="sxs-lookup"><span data-stu-id="52eac-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="52eac-123">Plánování projektu</span><span class="sxs-lookup"><span data-stu-id="52eac-123">Project Planning</span></span>

- <span data-ttu-id="52eac-124">Při aktualizaci projektu, který má v poli **Smluvní jednotka** hodnotu null, se vygeneruje výjimka nulového odkazu.</span><span class="sxs-lookup"><span data-stu-id="52eac-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="52eac-125">**Obnovit součty projektu** nesprávně vypočítá zbývající náklady a zbývající prodeje projektu.</span><span class="sxs-lookup"><span data-stu-id="52eac-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="52eac-126">Výpočty redundantních cen ovlivňují výkon, který souvisí s aktualizacemi kontur přiřazení prostředků.</span><span class="sxs-lookup"><span data-stu-id="52eac-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="52eac-127">Správa zdrojů</span><span class="sxs-lookup"><span data-stu-id="52eac-127">Resource Management</span></span>

<span data-ttu-id="52eac-128">Následující problém byl opraven:</span><span class="sxs-lookup"><span data-stu-id="52eac-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="52eac-129">Když je kapacita kalendáře rezervovatelného zdroje větší než 1, Project Service Automation nesprávně rozpozná kapacitu jako 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="52eac-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="52eac-130">Proto v zobrazení plánu dojde k nekonečné smyčce.</span><span class="sxs-lookup"><span data-stu-id="52eac-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="52eac-131">Prodej</span><span class="sxs-lookup"><span data-stu-id="52eac-131">Sales</span></span>

<span data-ttu-id="52eac-132">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="52eac-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="52eac-133">Když je vytvořen řádek deníku, který má vlastní typ transakce, dojde k následující výjimce nulového odkazu: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="52eac-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="52eac-134">Role a kategorie, které jsou deaktivovány před zkopírováním nabídky, nesmíte do fakturovatelných rolí a kategorií nově zkopírované nabídky.</span><span class="sxs-lookup"><span data-stu-id="52eac-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="52eac-135">Datum dokumentu a datum účetnictví nejsou v souladu s počátečním datem uvedeným v detailu řádku faktury, který je vytvořen přímo v konceptu faktury.</span><span class="sxs-lookup"><span data-stu-id="52eac-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="52eac-136">Výjimky s nulovým odkazem se generují ve scénářích, které souvisejí s inaktivací rolí a kategorií před zkopírováním nabídky.</span><span class="sxs-lookup"><span data-stu-id="52eac-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="52eac-137">Akce **Aktualizovat ceny** na stránce **Projekty** neaktualizuje odhady výdajů a odhady materiálu.</span><span class="sxs-lookup"><span data-stu-id="52eac-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
