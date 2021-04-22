---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 29.5, oprava hotfix, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v aktualizaci verze 29.5, oprava hotfix, pro aplikaci Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/26/2021
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
ms.openlocfilehash: 99ba353236ad88b8bdff2c1b25e1247fa4bf3455
ms.sourcegitcommit: 9ebf7dd501898053bfa824f732adabf3f273613b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/26/2021
ms.locfileid: "5715653"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-295-v3"></a><span data-ttu-id="b549a-103">Novinky a změny v aplikaci Project Service Automation, aktualizace verze 29.5, V3</span><span class="sxs-lookup"><span data-stu-id="b549a-103">What's new or changed in Project Service Automation Update Release 29.5, V3</span></span>

<span data-ttu-id="b549a-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b549a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b549a-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="b549a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b549a-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b549a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b549a-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="b549a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b549a-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b549a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b549a-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 29.5 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="b549a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.5.</span></span> <span data-ttu-id="b549a-110">Tato verze má číslo sestavení V3.10.47.150 a je obvykle k dispozici prostřednictvím automatické aktualizace v lednu 2021.</span><span class="sxs-lookup"><span data-stu-id="b549a-110">This version has a build number of V3.10.47.150 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-295"></a><span data-ttu-id="b549a-111">Aktualizace verze 29.5</span><span class="sxs-lookup"><span data-stu-id="b549a-111">Update Release 29.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b549a-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="b549a-112">Bug fixes</span></span>


<span data-ttu-id="b549a-113">**Prodej**</span><span class="sxs-lookup"><span data-stu-id="b549a-113">**Sales**</span></span>

<span data-ttu-id="b549a-114">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="b549a-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b549a-115">Ve volání metody **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** dojde k výjimce null reference, když uzavřete nabídku jako vyhranou a nabídka nemá ceník.</span><span class="sxs-lookup"><span data-stu-id="b549a-115">A possible null reference exception occurs in **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** when you close a quote as won and the quote has no price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
