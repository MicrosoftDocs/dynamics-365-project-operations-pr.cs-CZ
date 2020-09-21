---
title: Odeslání žádosti o zdroj
description: Toto téma obsahuje informace o odeslání žádosti o zdroj projektu.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750380"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="52bbe-103">Odeslání žádosti o zdroj</span><span class="sxs-lookup"><span data-stu-id="52bbe-103">Submit a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="52bbe-104">Vygenerovaný požadavek na zdroj můžete odeslat jako žádost o zdroj.</span><span class="sxs-lookup"><span data-stu-id="52bbe-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="52bbe-105">Žádost se pak odešle správci zdrojů ke splnění.</span><span class="sxs-lookup"><span data-stu-id="52bbe-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="52bbe-106">V Project Service Automation (PSA) klikněte na stránce **Projekty** na kartu **Tým** a zobrazte seznam rezervovatelných zdrojů.</span><span class="sxs-lookup"><span data-stu-id="52bbe-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="52bbe-107">Vyberte ze seznamu obecný zdroj, který obsahuje požadavek na zdroj, a pak klikněte na **Odeslat žádost**.</span><span class="sxs-lookup"><span data-stu-id="52bbe-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Odeslání žádosti o zdroj](media/RM-how-to-18.png)

<span data-ttu-id="52bbe-109">Stav žádosti obecného člena týmu se změní na **Odeslána**.</span><span class="sxs-lookup"><span data-stu-id="52bbe-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="52bbe-110">Po splnění žádosti správcem zdrojů bude obecný zdroj nahrazen pojmenovaným zdrojem, pokud správce zdrojů splní žádost rezervací pojmenovaného zdroje.</span><span class="sxs-lookup"><span data-stu-id="52bbe-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="52bbe-111">V opačném případě zůstane obecný zdroj v týmu a stav požadavku se změní na **Potřebuje kontrolu**, pokud správce prostředků navrhl pojmenovaný zdroj.</span><span class="sxs-lookup"><span data-stu-id="52bbe-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
