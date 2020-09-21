---
title: Co je nového v aktualizaci verze 14 pro aplikaci Project Service Automation V3
description: Tohle téma poskytuje informace o tom, co je nového v aktualizaci verze 14 pro aplikaci Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750333"
---
# <a name="project-service-automation-v3-update-release-14"></a><span data-ttu-id="b34de-103">Project Service Automation V3, aktualizace verze 14</span><span class="sxs-lookup"><span data-stu-id="b34de-103">Project Service Automation V3, Update Release 14</span></span>
<span data-ttu-id="b34de-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="b34de-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="b34de-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="b34de-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b34de-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b34de-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b34de-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 a na stránce řešení nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="b34de-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="b34de-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b34de-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b34de-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 14 pro aplikaci PSA V3.</span><span class="sxs-lookup"><span data-stu-id="b34de-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="b34de-110">Tato verze má číslo sestavení V3.10.4.21 a je k dispozici v následujícím plánu:</span><span class="sxs-lookup"><span data-stu-id="b34de-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="b34de-111">**Obecná dostupnost (automatická aktualizace):** Leden 2020</span><span class="sxs-lookup"><span data-stu-id="b34de-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="b34de-112">**Automatická aktualizace:** Únor 2020</span><span class="sxs-lookup"><span data-stu-id="b34de-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="b34de-113">Aktualizace verze 14</span><span class="sxs-lookup"><span data-stu-id="b34de-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="b34de-114">Vylepšení</span><span class="sxs-lookup"><span data-stu-id="b34de-114">Enhancements</span></span>

- <span data-ttu-id="b34de-115">Sales</span><span class="sxs-lookup"><span data-stu-id="b34de-115">Sales</span></span>

     - <span data-ttu-id="b34de-116">Vlastní hodnoty pole **Podrobnosti řádku nabídky** jsou zkopírovány do pole **Podrobnosti řádků projektových smluv** při aktualizaci nabídky na **Uzavřeno jako získané**.</span><span class="sxs-lookup"><span data-stu-id="b34de-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="b34de-117">Potvrzené projekty mohou být ve stavu **Uzavřeno jako ztracené**.</span><span class="sxs-lookup"><span data-stu-id="b34de-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="b34de-118">Správa zdrojů</span><span class="sxs-lookup"><span data-stu-id="b34de-118">Resource Management</span></span>

     - <span data-ttu-id="b34de-119">Při rozšiřování rezervace budou se uživatelům zobrazí potvrzovací dialogové okno obsahující shrnutí výsledků rezervace a odkaz Zachovat rezervace.</span><span class="sxs-lookup"><span data-stu-id="b34de-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="b34de-120">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="b34de-120">Bug fixes</span></span>

- <span data-ttu-id="b34de-121">Čas a výdaje</span><span class="sxs-lookup"><span data-stu-id="b34de-121">Time and Expense</span></span>

     - <span data-ttu-id="b34de-122">Opraveno: Vylepšeno uživatelské prostředí, když uživatel nevybral žádné položky, které mají být opraveny.</span><span class="sxs-lookup"><span data-stu-id="b34de-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="b34de-123">Správa zdrojů</span><span class="sxs-lookup"><span data-stu-id="b34de-123">Resource Management</span></span>

     - <span data-ttu-id="b34de-124">Opraveno: Vícenásobná rezervace zdroje přeteče název rezervovatelného zdroje.</span><span class="sxs-lookup"><span data-stu-id="b34de-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="b34de-125">Sales</span><span class="sxs-lookup"><span data-stu-id="b34de-125">Sales</span></span>

     - <span data-ttu-id="b34de-126">Opraveno: Celková prodejní cena se nevypočítává, dokud uživatel také nevloží nákladovou cenu pro odhad nákladů na projekt.</span><span class="sxs-lookup"><span data-stu-id="b34de-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="b34de-127">Opraveno: Uzavření nabídky jako **Získáno** selže, pokud přidružená projektová smlouva není ve stavu **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="b34de-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

