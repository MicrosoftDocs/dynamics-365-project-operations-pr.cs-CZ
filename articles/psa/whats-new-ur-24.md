---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 24, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 24, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c95a9dcada4fbf6c462df29d450aaafab4e73aa5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000248"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="c35b4-103">Project Service Automation, vydání aktualizace 24, V3</span><span class="sxs-lookup"><span data-stu-id="c35b4-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c35b4-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c35b4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c35b4-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="c35b4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c35b4-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="c35b4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c35b4-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="c35b4-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c35b4-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c35b4-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c35b4-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 24 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="c35b4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="c35b4-110">Tato verze má číslo sestavení V 3.10.42.43 a je obvykle k dispozici prostřednictvím automatické aktualizace v říjnu 2020.</span><span class="sxs-lookup"><span data-stu-id="c35b4-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="c35b4-111">Aktualizace verze 24</span><span class="sxs-lookup"><span data-stu-id="c35b4-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c35b4-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="c35b4-112">Bug fixes</span></span>

<span data-ttu-id="c35b4-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="c35b4-113">**Sales**</span></span>

<span data-ttu-id="c35b4-114">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="c35b4-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="c35b4-115">Problém při nastavování výchozího ceníku produktů.</span><span class="sxs-lookup"><span data-stu-id="c35b4-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="c35b4-116">Výkon získávání nabídek je pomalý kvůli kopii záznamů ceníku a ceny role.</span><span class="sxs-lookup"><span data-stu-id="c35b4-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="c35b4-117">**Projektová smlouva / Centrum prodeje** > **Množství položky produktové řady / řádku objednávky** je automaticky zaokrouhleno na nejbližší celé číslo.</span><span class="sxs-lookup"><span data-stu-id="c35b4-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="c35b4-118">Při čtení ceníků zvýšit na systémová oprávnění.</span><span class="sxs-lookup"><span data-stu-id="c35b4-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="c35b4-119">Zkopírujte pole adresy zákazníka **address1_freighttermscode** a **address1_shippingmethodcode** do nabídky / objednávky.</span><span class="sxs-lookup"><span data-stu-id="c35b4-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="c35b4-120">**Čas a výdaje**</span><span class="sxs-lookup"><span data-stu-id="c35b4-120">**Time and Expense**</span></span>

<span data-ttu-id="c35b4-121">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="c35b4-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="c35b4-122">**Mřížka časových záznamů** nepodporuje chování času **Pouze datum**.</span><span class="sxs-lookup"><span data-stu-id="c35b4-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="c35b4-123">**Časový záznam** se automaticky neobnovuje.</span><span class="sxs-lookup"><span data-stu-id="c35b4-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="c35b4-124">Je vyžadována ruční aktualizace.</span><span class="sxs-lookup"><span data-stu-id="c35b4-124">A manual refresh is required.</span></span>
- <span data-ttu-id="c35b4-125">Nelze importovat časové záznamy z přiřazení, když je v přiřazení prostředku přestávka (0 hodin).</span><span class="sxs-lookup"><span data-stu-id="c35b4-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="c35b4-126">Při vytváření časového záznamu nastavte začátek na stejný jako **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="c35b4-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="c35b4-127">Znovu povolte hromadné úpravy pro časový záznam.</span><span class="sxs-lookup"><span data-stu-id="c35b4-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="c35b4-128">**Správa zdrojů**</span><span class="sxs-lookup"><span data-stu-id="c35b4-128">**Resource Management**</span></span>

<span data-ttu-id="c35b4-129">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="c35b4-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="c35b4-130">Pokus o aktualizaci stavu mezidenní rezervace bez požadavku vyvolá výjimku null-ref.</span><span class="sxs-lookup"><span data-stu-id="c35b4-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="c35b4-131">Chyba při načítání souboru **Zobrazení vyrovnání**.</span><span class="sxs-lookup"><span data-stu-id="c35b4-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="c35b4-132">**Správa projektů**</span><span class="sxs-lookup"><span data-stu-id="c35b4-132">**Project Management**</span></span>

<span data-ttu-id="c35b4-133">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="c35b4-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="c35b4-134">V **Časovém plánu projektu**, když přecházíte z **Manual** na **Auto**, automatické ukládání se nedokončí.</span><span class="sxs-lookup"><span data-stu-id="c35b4-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="c35b4-135">Náklady by se neměly počítat směrem k odchylce v **Mřížce pro sledování projektů**.</span><span class="sxs-lookup"><span data-stu-id="c35b4-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="c35b4-136">Nekonzistentní chování pro sloupce **Značka odhadů** během načítání versus změna typu **Časová fáze**.</span><span class="sxs-lookup"><span data-stu-id="c35b4-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="c35b4-137">Skutečné náklady na projekt nemusí odrážet součty ze **Skutečných hodnot**.</span><span class="sxs-lookup"><span data-stu-id="c35b4-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="c35b4-138">**Předpokládané datum dokončení** na kartě **Souhrn** neodpovídá **Plánu strukturovaného rozpisu prací**.</span><span class="sxs-lookup"><span data-stu-id="c35b4-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="c35b4-139">**Aktualizave skutečných hodin** při zmenšení odsazení nefunguje správně.</span><span class="sxs-lookup"><span data-stu-id="c35b4-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="c35b4-140">Projektový manažer mimo kořenovou **BU** nemůže vytvořit projekt.</span><span class="sxs-lookup"><span data-stu-id="c35b4-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="c35b4-141">Změny úkolu nebo kategorie v **Odhadech výdajů** nejsou zachovány.</span><span class="sxs-lookup"><span data-stu-id="c35b4-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="c35b4-142">**Kopie smlouvy** zkopíruje plány faktur a stav běhu.</span><span class="sxs-lookup"><span data-stu-id="c35b4-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="c35b4-143">Tlačítko **Obnovit skutečné údaje** nesprávně vypočítá souhrnné úkoly.</span><span class="sxs-lookup"><span data-stu-id="c35b4-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="c35b4-144">Doplněk Microsoft Project: Oprava chyby s nulovou referencí, pokud má kterýkoli člen týmu prázdnou zdrojovou jednotku.</span><span class="sxs-lookup"><span data-stu-id="c35b4-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]