---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 17, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 17, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: f9fb941a95b0610dc546b1c12a87aa7faef4d676
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143695"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="af501-103">Project Service Automation, vydání aktualizace 17, V3</span><span class="sxs-lookup"><span data-stu-id="af501-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="af501-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="af501-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="af501-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="af501-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="af501-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="af501-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="af501-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="af501-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="af501-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="af501-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="af501-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 17 pro aplikaci PSA V3.</span><span class="sxs-lookup"><span data-stu-id="af501-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="af501-110">Tato verze má číslo sestavení V3.10.6.34 a je obecně k dispozici prostřednictvím automatické aktualizace v březnu 2020.</span><span class="sxs-lookup"><span data-stu-id="af501-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="af501-111">Aktualizace verze 17</span><span class="sxs-lookup"><span data-stu-id="af501-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="af501-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="af501-112">Bug fixes</span></span>

<span data-ttu-id="af501-113">**Obecné**</span><span class="sxs-lookup"><span data-stu-id="af501-113">**General**</span></span>

- <span data-ttu-id="af501-114">Oprava: Aktualizace Project Service Automation za účelem vynucení licencí Team Member (Centrum projektových zdrojů bude zahrnovat metadata servisního plánu pro členy týmu 3.x)</span><span class="sxs-lookup"><span data-stu-id="af501-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="af501-115">**Čas a výdaje**</span><span class="sxs-lookup"><span data-stu-id="af501-115">**Time and Expense**</span></span>

- <span data-ttu-id="af501-116">Oprava: Není možné změnit odhad výdajů z nenulové ceny na nulu (0).</span><span class="sxs-lookup"><span data-stu-id="af501-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="af501-117">Změna je ignorována.</span><span class="sxs-lookup"><span data-stu-id="af501-117">The change is ignored.</span></span>

<span data-ttu-id="af501-118">**Správa projektů**</span><span class="sxs-lookup"><span data-stu-id="af501-118">**Project Management**</span></span>

- <span data-ttu-id="af501-119">Oprava: Do názvu pozice člena týmu byla přidána kontrola nulových hodnot.</span><span class="sxs-lookup"><span data-stu-id="af501-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="af501-120">Oprava: Pole **msdyn_userresourceid** v entitě **msdyn_resourceassignment** je zastaralé.</span><span class="sxs-lookup"><span data-stu-id="af501-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="af501-121">Oprava: Upgrade z 2.x na 3.x nyní zpracovává prázdné křivky úsilí při přiřazování úkolů.</span><span class="sxs-lookup"><span data-stu-id="af501-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="af501-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="af501-122">**Sales**</span></span>

- <span data-ttu-id="af501-123">Oprava: **Invoice.PreValidateInvoiceUpdate** nyní zpracovává scénář správného opětovného přiřazení vlastníků záznamů.</span><span class="sxs-lookup"><span data-stu-id="af501-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="af501-124">Oprava: Když je třída transakce **Čas**, **UnitGroup** nelze upravovat pro všechny entity, včetně **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, a **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="af501-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="af501-125">Nicméně **Jednotka** je needitovatelná pouze pro **JournalLine** a **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="af501-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


