---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 31, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 31, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999123"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="9e1b4-103">Novinky a změny v aplikaci Project Service Automation, aktualizace verze 31, V3</span><span class="sxs-lookup"><span data-stu-id="9e1b4-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9e1b4-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9e1b4-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9e1b4-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9e1b4-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9e1b4-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9e1b4-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9e1b4-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 31 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="9e1b4-110">Tato verze má číslo sestavení V3.10.52.77 a je obvykle k dispozici prostřednictvím automatické aktualizace v květnu 2021.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="9e1b4-111">Aktualizace verze 31</span><span class="sxs-lookup"><span data-stu-id="9e1b4-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9e1b4-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="9e1b4-112">Bug fixes</span></span>

<span data-ttu-id="9e1b4-113">**Čas a výdaje**</span><span class="sxs-lookup"><span data-stu-id="9e1b4-113">**Time and Expense**</span></span>

<span data-ttu-id="9e1b4-114">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="9e1b4-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9e1b4-115">Ovládací tlačítka pro zadávání času na stránce **Rezervovatelný zdroj** byla matoucí.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="9e1b4-116">Byla vygenerována výjimka nulové reference v **Project.SetTrackingFields** při schvalování zadání času.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="9e1b4-117">**Správa zdrojů**</span><span class="sxs-lookup"><span data-stu-id="9e1b4-117">**Resource Management**</span></span>

<span data-ttu-id="9e1b4-118">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="9e1b4-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="9e1b4-119">**Vytvořit člena týmu** správně nezobrazuje nastavení metadat nastavení rezervace pro **Výchozí stav potvrzení rezervace**.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="9e1b4-120">Při upgradu z PSA 1.X na 3.X proces upgradu selže při **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="9e1b4-121">**Prodej**</span><span class="sxs-lookup"><span data-stu-id="9e1b4-121">**Sales**</span></span>

<span data-ttu-id="9e1b4-122">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="9e1b4-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="9e1b4-123">Skutečný příjem převádí částky na měnu projektu v mřížce sledování.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="9e1b4-124">Výchozí měna je nejasná při vytváření řádků deníku, řádků nabídek a řádků kontraktů ve scénářích, kde se základní měna organizace liší od měny projektu.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="9e1b4-125">Dotaz **Ověření deníku čekajících na opravu** nefiltruje podle projektu.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="9e1b4-126">Zbývající tržby se u projektu počítají nesprávně.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="9e1b4-127">Nabídky založené na kontaktu selžou, když jsou vytvořeny bez ceníku.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="9e1b4-128">Po výběru **Potvrdit fakturu** se nezobrazí žádné kolečko zpracování.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="9e1b4-129">Po výběru **Vytvořit fakturu** se nezobrazí žádné kolečko zpracování.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="9e1b4-130">Uzavření nabídky jako ztracené nezruší rezervace.</span><span class="sxs-lookup"><span data-stu-id="9e1b4-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







