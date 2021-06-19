---
title: Odeslání žádosti o zdroj
description: Vygenerovaný požadavek na zdroj můžete odeslat jako žádost o zdroj. Žádost se pak odešle správci zdrojů ke splnění.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6ac0044a27d1e506c9c62c477014017fd0ca06cb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014018"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="7bf37-104">Odeslání žádosti o zdroj</span><span class="sxs-lookup"><span data-stu-id="7bf37-104">Submit a resource request</span></span>

<span data-ttu-id="7bf37-105">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="7bf37-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7bf37-106">Vygenerovaný požadavek na zdroj můžete odeslat jako žádost o zdroj.</span><span class="sxs-lookup"><span data-stu-id="7bf37-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="7bf37-107">Žádost se pak odešle správci zdrojů ke splnění.</span><span class="sxs-lookup"><span data-stu-id="7bf37-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="7bf37-108">V Dynamics 365 Project Operations klikněte na stránce **Projekty** na kartu **Tým** a zobrazte seznam rezervovatelných zdrojů.</span><span class="sxs-lookup"><span data-stu-id="7bf37-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="7bf37-109">Vyberte ze seznamu obecný zdroj, který obsahuje požadavek na zdroj, a pak klikněte na **Odeslat žádost**.</span><span class="sxs-lookup"><span data-stu-id="7bf37-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="7bf37-110">Stav žádosti obecného člena týmu se změní na **Odeslána**.</span><span class="sxs-lookup"><span data-stu-id="7bf37-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="7bf37-111">Po splnění žádosti bude obecný zdroj nahrazen pojmenovaným zdrojem, pokud správce zdrojů splní žádost rezervací pojmenovaného zdroje.</span><span class="sxs-lookup"><span data-stu-id="7bf37-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="7bf37-112">Jinak, pokud správce zdrojů navrhne pojmenovaný zdroj, zůstane obecný zdroj v týmu a stav požadavku se změní na **Potřebuje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="7bf37-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]