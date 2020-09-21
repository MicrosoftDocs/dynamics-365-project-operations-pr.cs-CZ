---
title: Novinky a změny v aplikaci Project Service Automation verze 3.x vlny 1 2020
description: Tohle téma poskytuje informace o novinkách a změnách v aplikaci Project Service Automation verze 3 vlny 1 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750330"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="141d9-103">Novinky a změny v aplikaci Project Service Automation verze 3 vlny 1 2020</span><span class="sxs-lookup"><span data-stu-id="141d9-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="141d9-104">Téma zdůrazňuje klíčové aspekty upgradu při přechodu na nejnovější vydání aplikace Project Service Automation (PSA) verze 3.x vlny 1 2020.</span><span class="sxs-lookup"><span data-stu-id="141d9-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="141d9-105">Časový záznam</span><span class="sxs-lookup"><span data-stu-id="141d9-105">Time entry</span></span>
<span data-ttu-id="141d9-106">Možnosti práce s časovým záznamem byly rozšířeny, takže umožňují rozšíření časového záznamu do více zákaznických scénářů.</span><span class="sxs-lookup"><span data-stu-id="141d9-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="141d9-107">To zahrnuje možnost přidat typy záznamů, které nyní řídí specifické chování na základě názvu schématu pole **Nastavení časového záznamu**, zobrazených jako **Časový zdroj**.</span><span class="sxs-lookup"><span data-stu-id="141d9-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="141d9-108">Důležité informace o upgradu</span><span class="sxs-lookup"><span data-stu-id="141d9-108">Upgrade consideration</span></span>
<span data-ttu-id="141d9-109">Pro podporu této funkce byly role v rámci PSA aktualizovány, aby zahrnovaly nová oprávnění.</span><span class="sxs-lookup"><span data-stu-id="141d9-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="141d9-110">Tato oprávnění udělují přístup pro čtení k nové entitě, **Nastavení časového záznamu**.</span><span class="sxs-lookup"><span data-stu-id="141d9-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="141d9-111">Uživatelům, kteří potřebují protokolovat čas, by měla být udělena role **Uživatel časového záznamu** navíc ke stávajícím rolím.</span><span class="sxs-lookup"><span data-stu-id="141d9-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="141d9-112">Tato role zahrnuje novou funkci a zajišťuje, že časový záznam bude nadále fungovat.</span><span class="sxs-lookup"><span data-stu-id="141d9-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="141d9-113">Aktuálně změny rozšířeného časového záznamu</span><span class="sxs-lookup"><span data-stu-id="141d9-113">Currently extended time entry changes</span></span>
<span data-ttu-id="141d9-114">Aby se minimalizoval dopad na současné uživatele časového záznamu, je tato změna role jediným základním požadavkem nezbytným pro pokračování ve časového záznamu.</span><span class="sxs-lookup"><span data-stu-id="141d9-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="141d9-115">Pokud jste vytvořili vlastní zobrazení nebo oddělené časové záznamy, musíte nastavit pole **Nastavení časového záznamu** na správnou hodnotu PSA.</span><span class="sxs-lookup"><span data-stu-id="141d9-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
