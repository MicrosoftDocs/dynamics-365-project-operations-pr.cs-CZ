---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 30, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 30, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010418"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="d5a97-103">Novinky a změny v aplikaci Project Service Automation, aktualizace verze 30, V3</span><span class="sxs-lookup"><span data-stu-id="d5a97-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d5a97-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d5a97-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d5a97-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="d5a97-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d5a97-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d5a97-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d5a97-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="d5a97-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d5a97-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="d5a97-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="d5a97-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 30 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="d5a97-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="d5a97-110">Tato verze má číslo sestavení V3.10.51.61 a je obvykle k dispozici prostřednictvím automatické aktualizace v dubnu 2021.</span><span class="sxs-lookup"><span data-stu-id="d5a97-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="d5a97-111">Aktualizace verze 30</span><span class="sxs-lookup"><span data-stu-id="d5a97-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d5a97-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="d5a97-112">Bug fixes</span></span>

<span data-ttu-id="d5a97-113">**Čas a výdaje**</span><span class="sxs-lookup"><span data-stu-id="d5a97-113">**Time and Expense**</span></span>

<span data-ttu-id="d5a97-114">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="d5a97-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="d5a97-115">Při vytváření a ukládání časového záznamu dojde k chybě na stránce **Rychlé vytvoření**, pokud je odstraněno pole **Role**.</span><span class="sxs-lookup"><span data-stu-id="d5a97-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="d5a97-116">Filtr Časový vstup použije nesprávný operátor filtru.</span><span class="sxs-lookup"><span data-stu-id="d5a97-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="d5a97-117">Zkopírované časové rozvrhy se po výběru možnosti **Kopírovat týden** na ovládacím prvku zadávání času automaticky nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="d5a97-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="d5a97-118">**Správa zdrojů**</span><span class="sxs-lookup"><span data-stu-id="d5a97-118">**Resource Management**</span></span>

<span data-ttu-id="d5a97-119">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="d5a97-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="d5a97-120">Při prodloužení rezervace je stav rezervace přiřazený závazné rezervaci nesprávný.</span><span class="sxs-lookup"><span data-stu-id="d5a97-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="d5a97-121">Prodloužení rezervace respektuje stav rezervace definovaný jako **Potvrzený** v metadatech nastavení rezervace.</span><span class="sxs-lookup"><span data-stu-id="d5a97-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="d5a97-122">Pokud není zadán platný stav rezervace, chybová zpráva není správně lokalizována.</span><span class="sxs-lookup"><span data-stu-id="d5a97-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="d5a97-123">**Správa projektů**</span><span class="sxs-lookup"><span data-stu-id="d5a97-123">**Project Management**</span></span>

<span data-ttu-id="d5a97-124">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="d5a97-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="d5a97-125">Projekty nelze vytvořit v jedné měně, když zahrnují související úkoly v jiné měně.</span><span class="sxs-lookup"><span data-stu-id="d5a97-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="d5a97-126">**Prodej**</span><span class="sxs-lookup"><span data-stu-id="d5a97-126">**Sales**</span></span>

<span data-ttu-id="d5a97-127">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="d5a97-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="d5a97-128">Při kopírování ceníku se ceny neaktualizují.</span><span class="sxs-lookup"><span data-stu-id="d5a97-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="d5a97-129">Uzavření nabídky jako vyhrané selže, když má detail nákladů hodnotu původu.</span><span class="sxs-lookup"><span data-stu-id="d5a97-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="d5a97-130">U entity **Projektový úkol** byly **Odhadované náklady** přejmenovány **Plánované náklady (základ)**.</span><span class="sxs-lookup"><span data-stu-id="d5a97-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="d5a97-131">Při vytváření nebo odstraňování faktur se generuje výjimka null reference.</span><span class="sxs-lookup"><span data-stu-id="d5a97-131">A null reference exception is generated when invoices are created or deleted.</span></span>
