---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 25, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 3aa10e1d4b23fbe6c2743d71497bdef840776008
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948863"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="27bc4-103">Novinky a změny v aplikaci Project Service Automation, aktualizace verze 25, V3</span><span class="sxs-lookup"><span data-stu-id="27bc4-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="27bc4-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="27bc4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="27bc4-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="27bc4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="27bc4-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="27bc4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="27bc4-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="27bc4-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="27bc4-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="27bc4-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="27bc4-109">Tohle téma uvádí funkce a opravy, které jsou nové nebo změněné pro Project Service Automation V3, vydání aktualizace 25. Tato verze má číslo sestavení V 3.10.43.76 a je obecně dostupná prostřednictvím ruční aktualizace v říjnu 2020.</span><span class="sxs-lookup"><span data-stu-id="27bc4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="27bc4-110">Aktualizace verze 25</span><span class="sxs-lookup"><span data-stu-id="27bc4-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="27bc4-111">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="27bc4-111">Bug fixes</span></span>

<span data-ttu-id="27bc4-112">**Čas a výdaje**</span><span class="sxs-lookup"><span data-stu-id="27bc4-112">**Time and Expense**</span></span>

<span data-ttu-id="27bc4-113">Následující problém byl opraven:</span><span class="sxs-lookup"><span data-stu-id="27bc4-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="27bc4-114">Graf časových záznamů zobrazující dodatečná data na základě příliš velkého načteného intervalu.</span><span class="sxs-lookup"><span data-stu-id="27bc4-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="27bc4-115">**Správa zdrojů**</span><span class="sxs-lookup"><span data-stu-id="27bc4-115">**Resource Management**</span></span>

<span data-ttu-id="27bc4-116">Následující problém byl opraven:</span><span class="sxs-lookup"><span data-stu-id="27bc4-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="27bc4-117">Přidán kód Package Deployer pro přeskočení importu opravy Universal Resource Scheduling, pokud již existuje vyšší verze opravy.</span><span class="sxs-lookup"><span data-stu-id="27bc4-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="27bc4-118">**Správa projektů**</span><span class="sxs-lookup"><span data-stu-id="27bc4-118">**Project Management**</span></span>

<span data-ttu-id="27bc4-119">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="27bc4-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="27bc4-120">Opravené nesrovnalosti zaokrouhlování a směnného kurzu vedoucí k nesprávným plánovaným nákladům v mřížce sledování projektu.</span><span class="sxs-lookup"><span data-stu-id="27bc4-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="27bc4-121">Podpora zobrazení dvou nebo více reakčních mřížek ve formuláři **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="27bc4-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="27bc4-122">Poskytnuto ověření, které řeší možnost přiřadzení úkolu po datu ukončení kalendáře, což má za následek neúspěšné přiřazení prostředků.</span><span class="sxs-lookup"><span data-stu-id="27bc4-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="27bc4-123">Vylepšené zpracování chyb pro řešení výjimky odkazu s hodnotou null generované z následujících:</span><span class="sxs-lookup"><span data-stu-id="27bc4-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="27bc4-124">Modul plugin **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="27bc4-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="27bc4-125">**PreValidateProjectTaskCreate**, když je projektový úkol vytvořen bez přidruženého projektu</span><span class="sxs-lookup"><span data-stu-id="27bc4-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="27bc4-126">Modul plugin **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="27bc4-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="27bc4-127">Modul plugin **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="27bc4-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="27bc4-128">Modul plugin **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="27bc4-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="27bc4-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="27bc4-129">**Sales**</span></span>

<span data-ttu-id="27bc4-130">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="27bc4-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="27bc4-131">Vylepšené zpracování chyb při řešení výjimek odkazu s hodnotou null generovaných z **Kopírování projektu: správa odhadů HelperResource**.</span><span class="sxs-lookup"><span data-stu-id="27bc4-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="27bc4-132">**Nepřipraveno k fakturaci** v **Nedokončená fakturace času a materiálu** nevymaže stav fakturace.</span><span class="sxs-lookup"><span data-stu-id="27bc4-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="27bc4-133">Opraveno nesprávně označená tlačítka **Ceny** na kartách **Cena role** a **Položky katalogu**.</span><span class="sxs-lookup"><span data-stu-id="27bc4-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]