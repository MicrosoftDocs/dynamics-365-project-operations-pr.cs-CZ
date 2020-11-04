---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 17.5, oprava hotfix, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 17.5, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/13/2020
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
ms.openlocfilehash: 359eb8f8ca41d69d4f30dd44497a4deb6a6c4f8d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073735"
---
# <a name="project-service-automation-update-release-175-v3"></a><span data-ttu-id="0f585-103">Project Service Automation, vydání aktualizace 17.5, V3</span><span class="sxs-lookup"><span data-stu-id="0f585-103">Project Service Automation Update Release 17.5, V3</span></span>

<span data-ttu-id="0f585-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="0f585-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="0f585-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="0f585-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="0f585-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="0f585-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0f585-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="0f585-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="0f585-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="0f585-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0f585-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné pro V3, aktualizaci verze 17.5.</span><span class="sxs-lookup"><span data-stu-id="0f585-109">This topic lists the features and fixes that are new or changed for V3, Update Release 17.5.</span></span> <span data-ttu-id="0f585-110">Tato verze má číslo sestavení V3.10.7.32 a je obecně k dispozici prostřednictvím automatické aktualizace v březnu 2020.</span><span class="sxs-lookup"><span data-stu-id="0f585-110">This version has a build number of V3.10.7.32 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-175"></a><span data-ttu-id="0f585-111">Aktualizace verze 17.5</span><span class="sxs-lookup"><span data-stu-id="0f585-111">Update Release 17.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="0f585-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="0f585-112">Bug fixes</span></span>


<span data-ttu-id="0f585-113">**Správa projektů**</span><span class="sxs-lookup"><span data-stu-id="0f585-113">**Project Management**</span></span>

- <span data-ttu-id="0f585-114">Oprava: Řešení problémů se synchronizací na straně serveru, ke kterým dochází u úkolů s dlouhým trváním.</span><span class="sxs-lookup"><span data-stu-id="0f585-114">Fixed: Addressed server-side synchronization issues that occur with long duration tasks.</span></span>
- <span data-ttu-id="0f585-115">Oprava: Vyřešení šablon 24hodinové pracovní doby nepřesně přidávajících k úkolům další den.</span><span class="sxs-lookup"><span data-stu-id="0f585-115">Fixed: Addressed 24-hour work hour templates inaccurately adding an additional day to tasks.</span></span>
- <span data-ttu-id="0f585-116">Oprava: Vyřešení šablon pracovní doby +13 GMT nepřesně přesouvajících úkoly o den napřed.</span><span class="sxs-lookup"><span data-stu-id="0f585-116">Fixed: Addressed +13 GMT work hour templates inaccurately shifting tasks one day ahead.</span></span>

