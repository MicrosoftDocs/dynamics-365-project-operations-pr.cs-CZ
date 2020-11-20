---
title: Nasazení Project Operations – omezené
description: Toto téma obsahuje informace o tom, jak nainstalovat omezené nasazení Project Operations - od obchodu po pro forma fakturaci.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0633585fcef91d9218d6140764addb7cf96ab31d
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175658"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="d79f7-103">Nasazení Project Operations – omezené</span><span class="sxs-lookup"><span data-stu-id="d79f7-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="d79f7-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="d79f7-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d79f7-105">Project Operations podporuje více modelů nasazení.</span><span class="sxs-lookup"><span data-stu-id="d79f7-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="d79f7-106">Chcete-li zjistit nejlepší model nasazení, podívejte se na [Typy nasazení](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="d79f7-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="d79f7-107">Toto nasazení, omezené nasazení - od obchodu po pro forma fakturaci, má za následek pouze nasazení **Common Data Service Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="d79f7-108">Instalace Project Operations do nového prostředí CDS</span><span class="sxs-lookup"><span data-stu-id="d79f7-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="d79f7-109">Instalace do existujícího prostředí CDS</span><span class="sxs-lookup"><span data-stu-id="d79f7-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="d79f7-110">Instalace Project Operations do nového prostředí CDS</span><span class="sxs-lookup"><span data-stu-id="d79f7-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="d79f7-111">Jako [Globální správce nebo správce Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) s licencí Project Operations vytvořte nové prostředí CDS v [Centru pro správu PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="d79f7-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="d79f7-112">Ujistěte se, že jsou povoleny **Databáze CDS** a **Aplikace Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="d79f7-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="d79f7-113">Další informace naleznete v [Vytvoření a správa prostředí v centru pro správu Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="d79f7-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="d79f7-114">Vyberte **Microsoft Dynamics 365 Project Operations** ze seznamu nasazení aplikací Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d79f7-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="d79f7-115">Instalace Project Operations do stávajícího prostředí CDS</span><span class="sxs-lookup"><span data-stu-id="d79f7-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="d79f7-116">Jako [Globální správce nebo správce Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) s licencí Project Operations vyhledejte prostředí v [Centru pro správu PowerPlatform](https://admin.powerplatform.com), kam chcete nainstalovat Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d79f7-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="d79f7-117">Nainstalujte **Microsoft Dynamics 365 Project Operations** ze seznamu nasazení aplikací Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d79f7-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="d79f7-118">Další informace najdete v části [Správa aplikací Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="d79f7-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


