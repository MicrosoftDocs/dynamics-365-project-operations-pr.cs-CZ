---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 26, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 14fcccf5804e5da0926dbc69bdfa040229a7f068
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143550"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="80406-103">Project Service Automation, vydání aktualizace 26, V3</span><span class="sxs-lookup"><span data-stu-id="80406-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="80406-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="80406-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="80406-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="80406-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="80406-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="80406-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="80406-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="80406-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="80406-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="80406-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="80406-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 26 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="80406-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="80406-110">Tato verze má číslo sestavení V3.10.44.59 a je obecně dostupná prostřednictvím vlastní aktualizace v prosinci 2020.</span><span class="sxs-lookup"><span data-stu-id="80406-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="80406-111">Aktualizace verze 26</span><span class="sxs-lookup"><span data-stu-id="80406-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="80406-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="80406-112">Bug fixes</span></span>

<span data-ttu-id="80406-113">**Čas a výdaje**</span><span class="sxs-lookup"><span data-stu-id="80406-113">**Time and Expense**</span></span>

<span data-ttu-id="80406-114">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="80406-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="80406-115">Uživatelé jsou schopni změnit úkol u časového záznamu, který byl schválen / odeslán.</span><span class="sxs-lookup"><span data-stu-id="80406-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="80406-116">Chyba „Odkaz na objekt není nastaven“ při ukládání časového záznamu.</span><span class="sxs-lookup"><span data-stu-id="80406-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="80406-117">Import časového záznamu z přiřazení prostředků vytváří časové záznamy s nesprávnými hodnotami DateTime.</span><span class="sxs-lookup"><span data-stu-id="80406-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="80406-118">Když jsou nainstalovány aplikace Project Service Automation i Field Service, tlačítko **Nový** se zobrazuje dvakrát na panelu příkazů pro časové údaje v aplikaci Field Service.</span><span class="sxs-lookup"><span data-stu-id="80406-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="80406-119">Aktualizace buněk **Povolit jednotku** a **Skupina jednotek** nyní funguje v mřížce **Odhady výdajů**.</span><span class="sxs-lookup"><span data-stu-id="80406-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="80406-120">Formulář **Aktualizovat úpravu časového údaje** obsahuje **Časovou osu**.</span><span class="sxs-lookup"><span data-stu-id="80406-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="80406-121">Schválení času pro neprojektové časové údaje blokuje systém při hledání role schvalovatele projektu.</span><span class="sxs-lookup"><span data-stu-id="80406-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="80406-122">**Správa zdrojů**</span><span class="sxs-lookup"><span data-stu-id="80406-122">**Resource Management**</span></span>

<span data-ttu-id="80406-123">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="80406-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="80406-124">Přidáno ověření v modulu plug-in **PostProjectCreate**, který před vytvořením zkontroluje primární požadavek.</span><span class="sxs-lookup"><span data-stu-id="80406-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="80406-125">Rychlé vytvoření formuláře **Člen projektového týmu** vyvolá výjimku s nulovým odkazem, pokud jsou pole z formuláře odstraněna.</span><span class="sxs-lookup"><span data-stu-id="80406-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="80406-126">Generování požadavků na 12 hodin po dobu 1 roku nefunguje.</span><span class="sxs-lookup"><span data-stu-id="80406-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="80406-127">Vylepšená chybová zpráva výjimky s bulovým odkazem během vytváření požadavku na zdroj.</span><span class="sxs-lookup"><span data-stu-id="80406-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="80406-128">**Správa projektů**</span><span class="sxs-lookup"><span data-stu-id="80406-128">**Project Management**</span></span>

<span data-ttu-id="80406-129">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="80406-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="80406-130">Vylepšené ověřování pro řešení výjimky s nulovým odkazem generované v modulu plug-in **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="80406-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="80406-131">Projekty publikované doplňkem Microsoft Project pro stolní počítače odstraňují nepřiřazená přiřazení.</span><span class="sxs-lookup"><span data-stu-id="80406-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="80406-132">Přidáno nové ověření, když je odkaz na projekt úkolu neplatný kvůli výjimce nulového odkazu v modulu plug-in **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="80406-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="80406-133">Mřížka členů týmu nezobrazuje odlišná přiřazení v záznamu člena týmu.</span><span class="sxs-lookup"><span data-stu-id="80406-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="80406-134">Přidáno nové ověření a chybové zprávy kvůli výjimce nulové reference v modulu plug-in **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="80406-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="80406-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="80406-135">**Sales**</span></span>

<span data-ttu-id="80406-136">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="80406-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="80406-137">Při výběru řádku založeného na projektu v nabídce nebo smlouvě by tlačítko **Návrh** mělo být viditelné pouze při výběru řádku založeného na projektu spojené s existujícím produktem.</span><span class="sxs-lookup"><span data-stu-id="80406-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="80406-138">Rozdělit oprávnění **Create_Product** z oprávnění **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="80406-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="80406-139">Odstranění řádku faktury způsobí selhání nulové reference v **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="80406-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
