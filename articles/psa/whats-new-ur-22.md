---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 22, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 22, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 5694aa27afe7618cfca6b27444393634a9686600
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006548"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="f51c7-103">Project Service Automation, vydání aktualizace 22, V3</span><span class="sxs-lookup"><span data-stu-id="f51c7-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f51c7-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f51c7-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f51c7-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="f51c7-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f51c7-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f51c7-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f51c7-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="f51c7-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f51c7-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f51c7-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f51c7-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 22 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="f51c7-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="f51c7-110">Tato verze má číslo sestaveníV 3.10.33.48 a je obvykle k dispozici prostřednictvím automatické aktualizace v červnu 2020.</span><span class="sxs-lookup"><span data-stu-id="f51c7-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="f51c7-111">Aktualizace verze 22</span><span class="sxs-lookup"><span data-stu-id="f51c7-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f51c7-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="f51c7-112">Bug fixes</span></span>



<span data-ttu-id="f51c7-113">**Čas a výdaje**</span><span class="sxs-lookup"><span data-stu-id="f51c7-113">**Time and Expense**</span></span>

<span data-ttu-id="f51c7-114">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="f51c7-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="f51c7-115">**Časové záznamy** se po importu automaticky nepřidávají do plánu zadání času.</span><span class="sxs-lookup"><span data-stu-id="f51c7-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="f51c7-116">Výběr data mřížky **Zadání času** nerozpozná místní nastavení uživatele.</span><span class="sxs-lookup"><span data-stu-id="f51c7-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="f51c7-117">**Správa zdrojů**</span><span class="sxs-lookup"><span data-stu-id="f51c7-117">**Resource Management**</span></span>

<span data-ttu-id="f51c7-118">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="f51c7-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="f51c7-119">V ručním režimu nejsou změny kontur **Přiřazení zdrojů** při generování **Požadavků na zdroje** rozpoznány.</span><span class="sxs-lookup"><span data-stu-id="f51c7-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="f51c7-120">**Požadavky na zdroje** nepodporují vlastní stavy požadavků.</span><span class="sxs-lookup"><span data-stu-id="f51c7-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="f51c7-121">**Správa projektů**</span><span class="sxs-lookup"><span data-stu-id="f51c7-121">**Project Management**</span></span>

<span data-ttu-id="f51c7-122">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="f51c7-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="f51c7-123">Dvojí kliknutí na EstimateGridControl nebude správně analyzovat čísla v holandském formátu.</span><span class="sxs-lookup"><span data-stu-id="f51c7-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="f51c7-124">Přiřazené hodiny se neaktualizují správně, když se přiřazení změní pomocí doplňku počítačového klienta Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="f51c7-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="f51c7-125">Mřížky sledování projektů a odhadů zobrazují nesprávný kód měny prodeje, pokud je měna smlouvy jiná než měna zákazníka a organizace je nakonfigurována tak, aby místo symbolů měny zobrazovala kódy měny.</span><span class="sxs-lookup"><span data-stu-id="f51c7-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="f51c7-126">Datum ukončení členství týmu přidá jeden den, pokud je plán pracovní doby 24 hodin denně.</span><span class="sxs-lookup"><span data-stu-id="f51c7-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="f51c7-127">V plánu projektu nespustí přidání kategorie transakce k úkolu automatické uložení.</span><span class="sxs-lookup"><span data-stu-id="f51c7-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="f51c7-128">Při přidávání člena týmu do šablony projektu se zobrazí následující chyba: "Požadavky na zdroje nelze přidružit k šablonám projektu".</span><span class="sxs-lookup"><span data-stu-id="f51c7-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="f51c7-129">Skript pravidla pásu karet "msdyn.Approval.CanApproveOrReject" zobrazuje chybu časového limitu.</span><span class="sxs-lookup"><span data-stu-id="f51c7-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="f51c7-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="f51c7-130">**Sales**</span></span>

<span data-ttu-id="f51c7-131">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="f51c7-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="f51c7-132">Chybová zpráva o ověření se nezobrazí, když je ve vyhledávání ceníku ve formuláři / entitě Ceník projektu nové nabídky vybraný Ceník nákladové ceny.</span><span class="sxs-lookup"><span data-stu-id="f51c7-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="f51c7-133">Uzavření nabídky tak, jak byla vyhrána, se nevztahuje na vytvořenou smlouvu, pokud je BPF připojená k nabídce v konečné fázi.</span><span class="sxs-lookup"><span data-stu-id="f51c7-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="f51c7-134">Stornování položky **Nevyfakturovaný prodej** je spojeno s původními náklady při vyvolání časového záznamu.</span><span class="sxs-lookup"><span data-stu-id="f51c7-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="f51c7-135">Po výběru tlačítka **Potvrdit** se stav faktury nezmění na **Potvrzeno**, pokud není faktura obnovena.</span><span class="sxs-lookup"><span data-stu-id="f51c7-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]