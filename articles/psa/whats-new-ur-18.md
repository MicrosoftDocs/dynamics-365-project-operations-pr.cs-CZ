---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 18, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 18, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: f7def50e77a83fd790b81b1b4fd36008ce293b0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006638"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="ba752-103">Project Service Automation, vydání aktualizace 18, V3</span><span class="sxs-lookup"><span data-stu-id="ba752-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ba752-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ba752-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ba752-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="ba752-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ba752-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ba752-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ba752-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="ba752-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="ba752-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ba752-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ba752-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 18 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="ba752-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="ba752-110">Tato verze má číslo sestavení V3.10.8.12 a je obvykle k dispozici prostřednictvím automatické aktualizace v dubnu 2020.</span><span class="sxs-lookup"><span data-stu-id="ba752-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="ba752-111">Aktualizace verze 18</span><span class="sxs-lookup"><span data-stu-id="ba752-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ba752-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="ba752-112">Bug fixes</span></span>

<span data-ttu-id="ba752-113">**Čas a výdaje**</span><span class="sxs-lookup"><span data-stu-id="ba752-113">**Time and Expense**</span></span>

- <span data-ttu-id="ba752-114">Opraveno: Toky **Odvolat**, **Požádat** a **Zrušit schválení** vyvolávají výjimky s nejasnými chybovými zprávami.</span><span class="sxs-lookup"><span data-stu-id="ba752-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="ba752-115">Opraveno: Když možnost **Zrušit schválení** selže u nákladů, není vyvolána relevantní výjimka.</span><span class="sxs-lookup"><span data-stu-id="ba752-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="ba752-116">Opraveno: Mřížka časového záznamu nesprávně zpracovává nepracovní dny v Austrálii po přepnutí letního času (DST) v říjnu.</span><span class="sxs-lookup"><span data-stu-id="ba752-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="ba752-117">Opraveno: Nesprávná výchozí logika zabraňuje odesílání výdajů.</span><span class="sxs-lookup"><span data-stu-id="ba752-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="ba752-118">Opraveno: Pokud selže schválení časového záznamu, zůstává schválení ve stavu **Čekající**.</span><span class="sxs-lookup"><span data-stu-id="ba752-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="ba752-119">Opraveno: Chyby SQL při hromadném schvalování (zablokování / časový limit).</span><span class="sxs-lookup"><span data-stu-id="ba752-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="ba752-120">Opraveno: Významné problémy s výkonem v uživatelském rozhraní způsobené aktualizací členů týmu při schvalování časových záznamů.</span><span class="sxs-lookup"><span data-stu-id="ba752-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="ba752-121">**Správa projektů**</span><span class="sxs-lookup"><span data-stu-id="ba752-121">**Project Management**</span></span>

- <span data-ttu-id="ba752-122">Opraveno: Oznámení o časovém pásmu bylo přesunuto ze zobrazení **Vyrovnání** do hlavního formuláře **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="ba752-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="ba752-123">Opraveno: Šablona kalendáře není správně nastavena, když se otevře nový formulář projektu.</span><span class="sxs-lookup"><span data-stu-id="ba752-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="ba752-124">Oprava: V prohlížečích založených na Chromiu nemohou uživatelé snadno vybrat předchozí úkoly, které mají být odstraněny.</span><span class="sxs-lookup"><span data-stu-id="ba752-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="ba752-125">Opraveno: Vytvoření nebo kopírování **Projektu z prázdné šablony** načítá nesouvisející úkoly.</span><span class="sxs-lookup"><span data-stu-id="ba752-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="ba752-126">Opraveno: V konkrétních mezních případech má vytvoření nového přiřazení z mřížky úkolu za následek vytvoření duplicitních záznamů.</span><span class="sxs-lookup"><span data-stu-id="ba752-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="ba752-127">Opraveno: V ručním režimu nemohou uživatelé aktualizovat počáteční data úlohy na pozdější než aktuální uložené datum.</span><span class="sxs-lookup"><span data-stu-id="ba752-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="ba752-128">**Správa zdrojů**</span><span class="sxs-lookup"><span data-stu-id="ba752-128">**Resource Management**</span></span>

- <span data-ttu-id="ba752-129">Opraveno: Řádek mezisoučtu zobrazení **Vyrovnání** nesprávně vypočítá variantu rezervací po prodloužení rezervace.</span><span class="sxs-lookup"><span data-stu-id="ba752-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="ba752-130">Opraveno: Zobrazení **Vyrovnání** nesprávně zobrazuje přiřazení zdrojů, pokud rezervovatelný zdroj obsahuje kalendář, který neodpovídá kalendáři projektu.</span><span class="sxs-lookup"><span data-stu-id="ba752-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="ba752-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="ba752-131">**Sales**</span></span>

- <span data-ttu-id="ba752-132">Opraveno: Při opětovném schválení časových záznamů (**Schválit > Zrušit>** a znovu schválit), se vytvoří duplicitní neúčtovatelná skutečná hodnota.</span><span class="sxs-lookup"><span data-stu-id="ba752-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]