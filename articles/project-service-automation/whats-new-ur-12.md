---
title: Co je nového v aktualizaci verze 12 pro aplikaci Project Service Automation V3
description: Tohle téma poskytuje informace o tom, co je nového v aktualizaci verze 12 pro aplikaci Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750335"
---
# <a name="project-service-automation-v3-update-release-12"></a><span data-ttu-id="1af21-103">Project Service Automation V3, aktualizace verze 12</span><span class="sxs-lookup"><span data-stu-id="1af21-103">Project Service Automation V3, Update Release 12</span></span>
<span data-ttu-id="1af21-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="1af21-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="1af21-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="1af21-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1af21-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1af21-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1af21-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 a na stránce řešení nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="1af21-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="1af21-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1af21-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1af21-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 12 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="1af21-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="1af21-110">Tato verze má číslo sestavení V3.10.2.34 a je obvykle k dispozici prostřednictvím automatické aktualizace v říjnu 2019.</span><span class="sxs-lookup"><span data-stu-id="1af21-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="1af21-111">Aktualizace verze 12</span><span class="sxs-lookup"><span data-stu-id="1af21-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1af21-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="1af21-112">Bug fixes</span></span>

- <span data-ttu-id="1af21-113">Čas a výdaje</span><span class="sxs-lookup"><span data-stu-id="1af21-113">Time and Expense</span></span>

    - <span data-ttu-id="1af21-114">Opraveno: Zprávy o chybách časového záznamu byly aktualizovány o relevantnější kontext.</span><span class="sxs-lookup"><span data-stu-id="1af21-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="1af21-115">Opraveno: Mřížka časového záznamu a plán správně zobrazují svislý posuvník v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="1af21-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="1af21-116">Opraveno: Odeslané výdaje nebo časové záznamy lze schválit.</span><span class="sxs-lookup"><span data-stu-id="1af21-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="1af21-117">Opraveno: Zpráva potvrzovacího dialogového okna pro schválení zrušení byla opravena, aby reflektovala stav schválení, když je změněn ze **Schváleno** na **Odesláno**.</span><span class="sxs-lookup"><span data-stu-id="1af21-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="1af21-118">Opraveno: Pole **Cena**, **Jednotka** a **Množství** jsou nyní po schválení uzamčena v záznamu Výdaje.</span><span class="sxs-lookup"><span data-stu-id="1af21-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="1af21-119">Správa projektů</span><span class="sxs-lookup"><span data-stu-id="1af21-119">Project Management</span></span>

    - <span data-ttu-id="1af21-120">Opraveno: Akce **Nový** na hlavním formuláři **Člen týmu** byla odstraněna.</span><span class="sxs-lookup"><span data-stu-id="1af21-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="1af21-121">Opraveno: Přiřazení zdrojů bylo aktualizováno, aby zohledňovalo chyby nepřesného zaokrouhlování, které vedou k posunu koncového data úlohy.</span><span class="sxs-lookup"><span data-stu-id="1af21-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="1af21-122">Opraveno: V mřížce úloh se uživateli zobrazí příslušné chyby na straně serveru.</span><span class="sxs-lookup"><span data-stu-id="1af21-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="1af21-123">Opraveno: Jméno člena týmu se nyní v názvu úlohy vykreslí místo názvu pozice.</span><span class="sxs-lookup"><span data-stu-id="1af21-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="1af21-124">Správa zdrojů</span><span class="sxs-lookup"><span data-stu-id="1af21-124">Resource Management</span></span>

    - <span data-ttu-id="1af21-125">Opraveno: Podrobnosti o požadavcích na zdroje pro projekty vytvořené ze šablony nyní používají kalendář projektu.</span><span class="sxs-lookup"><span data-stu-id="1af21-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="1af21-126">Opraveno: Dovednosti a kompetence jsou standardně nastaveny od hlavních dat role po požadavek na zdroj vytvořené pro tuto roli.</span><span class="sxs-lookup"><span data-stu-id="1af21-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="1af21-127">Sales</span><span class="sxs-lookup"><span data-stu-id="1af21-127">Sales</span></span>

    - <span data-ttu-id="1af21-128">Opraveno: Duplicitní ID objektů nalezená na formuláři **Hlavní smlouva**.</span><span class="sxs-lookup"><span data-stu-id="1af21-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="1af21-129">Opraveno: Logika byla aktualizována, aby karta **Analýza nabídky** byla viditelná, takže zobrazuje nastavení metadat karty.</span><span class="sxs-lookup"><span data-stu-id="1af21-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="1af21-130">Opraveno: Datum účtování ve skutečném záznamu nyní pochází od data záznamu času/výdajů a nikoli od data schválení.</span><span class="sxs-lookup"><span data-stu-id="1af21-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
