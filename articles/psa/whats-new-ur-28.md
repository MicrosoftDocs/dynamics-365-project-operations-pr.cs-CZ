---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 28, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 28, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010508"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="cd31f-103">Novinky a změny v aplikaci Project Service Automation, aktualizace verze 28, V3</span><span class="sxs-lookup"><span data-stu-id="cd31f-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cd31f-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cd31f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cd31f-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="cd31f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cd31f-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cd31f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cd31f-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="cd31f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cd31f-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cd31f-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cd31f-109">Tohle téma uvádí funkce a opravy, které jsou nové nebo změněné pro Project Service Automation V3, vydání aktualizace 28. Tato verze má číslo sestavení V 3.10.46.32 a je obecně dostupná prostřednictvím ruční aktualizace v lednu 2021.</span><span class="sxs-lookup"><span data-stu-id="cd31f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="cd31f-110">Aktualizace verze 28</span><span class="sxs-lookup"><span data-stu-id="cd31f-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cd31f-111">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="cd31f-111">Bug fixes</span></span>

<span data-ttu-id="cd31f-112">**Čas a výdaje**</span><span class="sxs-lookup"><span data-stu-id="cd31f-112">**Time and Expense**</span></span>

<span data-ttu-id="cd31f-113">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="cd31f-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd31f-114">Uživatelé mohou použít **Hromadné úpravy** k aktualizaci položek času, které byly schváleny a odeslány.</span><span class="sxs-lookup"><span data-stu-id="cd31f-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="cd31f-115">**Správa projektů**</span><span class="sxs-lookup"><span data-stu-id="cd31f-115">**Project Management**</span></span>

<span data-ttu-id="cd31f-116">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="cd31f-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd31f-117">V případech, kdy je identifikátor GUID úlohy interpretován jako číslo, nelze úkoly otevřít pro úpravy pomocí **Upravit úkol** ve pásu nástrojů na stránce **Strukturovaný rozpis prací**.</span><span class="sxs-lookup"><span data-stu-id="cd31f-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="cd31f-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cd31f-118">**Sales**</span></span>

<span data-ttu-id="cd31f-119">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="cd31f-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd31f-120">Výjimka nulové reference je generována, když je vyvolán modul plug-in **GetEstimatesForProject**.</span><span class="sxs-lookup"><span data-stu-id="cd31f-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="cd31f-121">**Označit jako připraveno k fakturaci** na mřížce milníku aktualizuje atributy pouze částečně, s výjimkou atributu **Stav faktury**, který je aktualizován.</span><span class="sxs-lookup"><span data-stu-id="cd31f-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]