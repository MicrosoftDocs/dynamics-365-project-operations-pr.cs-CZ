---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 16, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 16, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: f277d23e3fb0517f072e51f6f80f855479ab8189
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073739"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="79e65-103">Project Service Automation, vydání aktualizace 16, V3</span><span class="sxs-lookup"><span data-stu-id="79e65-103">Project Service Automation Update Release 16, V3</span></span>

<span data-ttu-id="79e65-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="79e65-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="79e65-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="79e65-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="79e65-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="79e65-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="79e65-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="79e65-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="79e65-108">Další informace viz [Instalace, aktualizace preferovaného řešení](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="79e65-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="79e65-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 16 pro aplikaci PSA V3.</span><span class="sxs-lookup"><span data-stu-id="79e65-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="79e65-110">Tato verze má číslo sestavení V3.10.6.34 a je obvykle k dispozici prostřednictvím automatické aktualizace v lednu 2020.</span><span class="sxs-lookup"><span data-stu-id="79e65-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="79e65-111">Aktualizace verze 16</span><span class="sxs-lookup"><span data-stu-id="79e65-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="79e65-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="79e65-112">Bug fixes</span></span>

-   <span data-ttu-id="79e65-113">Čas a výdaje</span><span class="sxs-lookup"><span data-stu-id="79e65-113">Time and Expense</span></span>

    -   <span data-ttu-id="79e65-114">Oprava: Uživatelé, kteří se pokusí odeslat odstraněné údaje o času a výdajích ke schválení, nyní obdrží příslušné chybové zprávy.</span><span class="sxs-lookup"><span data-stu-id="79e65-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="79e65-115">Správa projektů</span><span class="sxs-lookup"><span data-stu-id="79e65-115">Project Management</span></span>

    -   <span data-ttu-id="79e65-116">Oprava: Jednotky zdroje definované pro členy týmu v šablonách jsou respektovány se šablonami, které jsou použity na nový projekt.</span><span class="sxs-lookup"><span data-stu-id="79e65-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="79e65-117">Oprava: Vylepšené zpracování opětovného přiřazení vlastnictví záznamu.</span><span class="sxs-lookup"><span data-stu-id="79e65-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="79e65-118">Oprava: Projekty, které se právě kopírují, nebudou zkopírovány, dokud nebudou dokončeny všechny operace kopírování.</span><span class="sxs-lookup"><span data-stu-id="79e65-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="79e65-119">Správa zdrojů</span><span class="sxs-lookup"><span data-stu-id="79e65-119">Resource Management</span></span>

    -   <span data-ttu-id="79e65-120">Oprava: Rozšířené rezervace nyní zpracovávají krátké doby správně a již nevytvářejí nulové hodiny pro rozšířené rezervace.</span><span class="sxs-lookup"><span data-stu-id="79e65-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="79e65-121">Oprava: Zobrazení odsouhlasení se nyní vykreslí, když je časové pásmo projektu +5:30 GMT a čas uživatele je jiný.</span><span class="sxs-lookup"><span data-stu-id="79e65-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="79e65-122">Sales</span><span class="sxs-lookup"><span data-stu-id="79e65-122">Sales</span></span>

    -   <span data-ttu-id="79e65-123">Oprava: Když je odstraněn projekt mapovaný na řádek smlouvy a je namapován nový projekt, skutečné záznamy o novém projektu nebyly znovu vyhodnoceny na základě fakturačních a cenových pravidel definovaných na řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="79e65-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="79e65-124">To bylo v této verzi opraveno.</span><span class="sxs-lookup"><span data-stu-id="79e65-124">This has been fixed in this release.</span></span> <span data-ttu-id="79e65-125">Ceny a skutečné záznamy o nově mapovaném projektu budou stornovány a znovu vytvořeny správně na základě cenových a fakturačních pravidel řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="79e65-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="79e65-126">Skutečné záznamy nemapovaného projektu se v důsledku toho také přehodnotí a znovu vytvoří.</span><span class="sxs-lookup"><span data-stu-id="79e65-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="79e65-127">Oprava: K poli **Částka** řádku odhadu bylo přidáno další ověření, aby se zajistilo, že nezůstanou zachovány hodnoty null.</span><span class="sxs-lookup"><span data-stu-id="79e65-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="79e65-128">Oprava: Po aktualizaci skutečných hodnot projektu bylo do hlavního formuláře projektu přidáno tlačítko Obnovit, aby uživatelé mohli znovu synchronizovat skutečné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="79e65-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="79e65-129">Oprava: Když uživatelé upgradují z 2.X na 3.X, budou povoleny projekty s hodnotou NULL pro název projektu.</span><span class="sxs-lookup"><span data-stu-id="79e65-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

