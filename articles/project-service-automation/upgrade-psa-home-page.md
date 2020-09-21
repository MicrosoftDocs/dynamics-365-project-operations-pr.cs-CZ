---
title: Upgrade domovské stránky
description: Toto téma ukazuje, kde naleznete důležité informace o nových a změněných funkcích aplikace Dynamics 365 Project Service Automation a o procesu upgradu na nejnovější verzi.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750370"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="6c81d-103">Upgrade domovské stránky</span><span class="sxs-lookup"><span data-stu-id="6c81d-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="6c81d-104">Upgrade PSA z verze 2.x nebo 1.x na verzi 3.x</span><span class="sxs-lookup"><span data-stu-id="6c81d-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="6c81d-105">Nové instance</span><span class="sxs-lookup"><span data-stu-id="6c81d-105">New instances</span></span>

<span data-ttu-id="6c81d-106">Od 17. května 2019 platí, že pokud je při zřizování nové instance vybrána služba Project Service Automation, bude ve výchozím nastavení nainstalována verze 3.x.</span><span class="sxs-lookup"><span data-stu-id="6c81d-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="6c81d-107">Existují instance</span><span class="sxs-lookup"><span data-stu-id="6c81d-107">Existing instances</span></span>

<span data-ttu-id="6c81d-108">Dříve museli zákazníci, kteří měli instanci PSA verze 2.x a potřebovali upgradovat na verzi 3.x, což je verze PSA založená na sjednoceném rozhraní klienta (UCI), kontaktovat podporu Microsoft a poskytnout podrobnosti o jejich instanci, aby podpora mohla povolit instanci pro upgrade na verzi 3.x.</span><span class="sxs-lookup"><span data-stu-id="6c81d-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="6c81d-109">Od 1. března 2020 budou zákazníci, kteří mají instanci PSA verze 2.x a potřebují upgradovat na verzi 3.x, moci upgradovat své instance přímo z portálu pro správu, aniž by museli kontaktovat podporu společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6c81d-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="6c81d-110">PSA verze 3.x zahrnuje významné změny.</span><span class="sxs-lookup"><span data-stu-id="6c81d-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="6c81d-111">Byla postavena na architektuře Sjednoceného rozhraní, aby pomohla zajistit lepší uživatelské prostředí.</span><span class="sxs-lookup"><span data-stu-id="6c81d-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="6c81d-112">Nově přepracovaná aplikace poskytuje konzistentní, jednotné uživatelské rozhraní (UI) a řídí se zásadami přizpůsobivého návrhu pro optimální zobrazení libovolné velikosti obrazovky nebo zařízení.</span><span class="sxs-lookup"><span data-stu-id="6c81d-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="6c81d-113">V aplikaci byly provedeny další změny.</span><span class="sxs-lookup"><span data-stu-id="6c81d-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="6c81d-114">Mezi oblasti, které byly změněny, patří tvorba cen, rezervace a přiřazování zdrojů, čas, výdaje a schválení.</span><span class="sxs-lookup"><span data-stu-id="6c81d-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="6c81d-115">Před spuštěním upgradu doporučujeme dokončit následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="6c81d-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="6c81d-116">Ověřte, zda jsou v identifikované instanci nainstalovány aplikace Dynamics 365 Field Service a Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6c81d-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="6c81d-117">Pokud jsou nainstalována obě řešení, měli byste naplánovat upgrade obou před obnovením běžného používání dané instance.</span><span class="sxs-lookup"><span data-stu-id="6c81d-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="6c81d-118">Pečlivě si prostudujte následující témata.</span><span class="sxs-lookup"><span data-stu-id="6c81d-118">Carefully review the following topics.</span></span> <span data-ttu-id="6c81d-119">Znalost a pochopení změn mezi verzemi vám pomůže při procesu upgradu.</span><span class="sxs-lookup"><span data-stu-id="6c81d-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="6c81d-120">Tato témata obsahují informace o hlavních změnách v programu PSA, včetně důležitých informací a doporučení pro plánování upgradu na verzi 3.x.</span><span class="sxs-lookup"><span data-stu-id="6c81d-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="6c81d-121">Novinky a změny v aplikaci Project Service Automation verze 3</span><span class="sxs-lookup"><span data-stu-id="6c81d-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="6c81d-122">Důležité informace o upgradu – Project Service Automation verze 2.x nebo 1.x na verzi 3</span><span class="sxs-lookup"><span data-stu-id="6c81d-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="6c81d-123">Upgradujte sandboxovou instanci, chcete-li zhodnotit změny v implementaci před upgradem produkční instance.</span><span class="sxs-lookup"><span data-stu-id="6c81d-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="6c81d-124">Po zkontrolování dříve zmíněných témat a jakmile budete připraveni na upgrade na verzi PSA 3.x nebo na verzi založenou na UCI, odešlete požadavek oddělení podpory Microsoftu, aby byl upgrade k dispozici z centra pro správu.</span><span class="sxs-lookup"><span data-stu-id="6c81d-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="6c81d-125">V požadavku zadejte podrobnosti o vaší instanci.</span><span class="sxs-lookup"><span data-stu-id="6c81d-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="6c81d-126">Starší verze programu PSA (PSA verze 2.x) v nově vytvořené instanci</span><span class="sxs-lookup"><span data-stu-id="6c81d-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="6c81d-127">Od 17. května 2019 budou mít všechny nové instance UCI jako výchozího klienta.</span><span class="sxs-lookup"><span data-stu-id="6c81d-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="6c81d-128">Pro zajištění souladu s touto změnou bude ve výchozím nastavení zřízena verze PSA 3.x a Field Service 8.x, protože tyto verze jsou navrženy tak, aby fungovaly s klientem UCI.</span><span class="sxs-lookup"><span data-stu-id="6c81d-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="6c81d-129">Od 1. března 2020 již zákazníci Dynamics PSA nebudou moci vytvářet nová prostředí se staršími verzemi PSA, například PSA verze 2.x nebo nižší.</span><span class="sxs-lookup"><span data-stu-id="6c81d-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="6c81d-130">Jakékoli nové prostředí bude pouze verze 3.x aplikace PSA.</span><span class="sxs-lookup"><span data-stu-id="6c81d-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="6c81d-131">Chcete-li dosáhnout nejlepších výsledků, pokud používáte starší verze aplikací Field Service a PSA, přejděte na stránku **Nastavení systému** a pro pole **Používat jen nové Sjednocené rozhraní (doporučeno)** vyberte možnost **Ne**, protože tyto verze nejsou navrženy tak, aby byly v UCI správně načteny.</span><span class="sxs-lookup"><span data-stu-id="6c81d-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="6c81d-132">Po vypnutí UCI můžete tyto verze aplikací Field Service a PSA otevřít a spustit pomocí starého webového klienta.</span><span class="sxs-lookup"><span data-stu-id="6c81d-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> <span data-ttu-id="6c81d-133">Pokyny k vypnutí klienta UCI naleznete v části [Povolení pouze Sjednoceného rozhraní](../admin/enable-unified-interface-only.md).</span><span class="sxs-lookup"><span data-stu-id="6c81d-133">For instructions about how to turn off the UCI client, see [Enable unified interface only](../admin/enable-unified-interface-only.md).</span></span>
