---
title: Novinky a změny v aplikaci Project Service Automation verze 3.x vlny 1 2020
description: Tohle téma poskytuje informace o novinkách a změnách v aplikaci Project Service Automation verze 3 vlny 1 2020.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 5110679038ae7ed1e21a3e7dc80a4657e0752b49
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150930"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="979ed-103">Novinky a změny v aplikaci Project Service Automation verze 3 vlny 1 2020</span><span class="sxs-lookup"><span data-stu-id="979ed-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="979ed-104">Téma zdůrazňuje klíčové aspekty upgradu při přechodu na nejnovější vydání aplikace Project Service Automation (PSA) verze 3.x vlny 1 2020.</span><span class="sxs-lookup"><span data-stu-id="979ed-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="979ed-105">Časový záznam</span><span class="sxs-lookup"><span data-stu-id="979ed-105">Time entry</span></span>
<span data-ttu-id="979ed-106">Možnosti práce s časovým záznamem byly rozšířeny, takže umožňují rozšíření časového záznamu do více zákaznických scénářů.</span><span class="sxs-lookup"><span data-stu-id="979ed-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="979ed-107">To zahrnuje možnost přidat typy záznamů, které nyní řídí specifické chování na základě názvu schématu pole **Nastavení časového záznamu**, zobrazených jako **Časový zdroj**.</span><span class="sxs-lookup"><span data-stu-id="979ed-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="979ed-108">Na podporu této funkce bylo přidáno nové řešení Time, Expense, Statusing, and Approvals (TESA).</span><span class="sxs-lookup"><span data-stu-id="979ed-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="979ed-109">Důležité informace o upgradu</span><span class="sxs-lookup"><span data-stu-id="979ed-109">Upgrade consideration</span></span>
<span data-ttu-id="979ed-110">Pro podporu této funkce byly role v rámci PSA aktualizovány, aby zahrnovaly nová oprávnění.</span><span class="sxs-lookup"><span data-stu-id="979ed-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="979ed-111">Tato oprávnění udělují přístup pro čtení k nové entitě, **Nastavení časového záznamu**.</span><span class="sxs-lookup"><span data-stu-id="979ed-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="979ed-112">Uživatelům, kteří potřebují protokolovat čas, by měla být udělena role **Uživatel časového záznamu** navíc ke stávajícím rolím.</span><span class="sxs-lookup"><span data-stu-id="979ed-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="979ed-113">Tato role zahrnuje novou funkci a zajišťuje, že časový záznam bude nadále fungovat.</span><span class="sxs-lookup"><span data-stu-id="979ed-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="979ed-114">Pokud navíc máte jakékoli vlastní moduly aplikace, které zahrnují všechny formuláře pro entitu časového zadání, budete muset odebrat **formulář pro rychlé vytvoření zadání času TESA** z modulu.</span><span class="sxs-lookup"><span data-stu-id="979ed-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="979ed-115">Aktuálně změny rozšířeného časového záznamu</span><span class="sxs-lookup"><span data-stu-id="979ed-115">Currently extended time entry changes</span></span>
<span data-ttu-id="979ed-116">Aby se minimalizoval dopad na současné uživatele časového záznamu, je tato změna role jediným základním požadavkem nezbytným pro pokračování ve časového záznamu.</span><span class="sxs-lookup"><span data-stu-id="979ed-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="979ed-117">Pokud jste vytvořili vlastní zobrazení nebo oddělené časové záznamy, musíte nastavit pole **Nastavení časového záznamu** na správnou hodnotu PSA.</span><span class="sxs-lookup"><span data-stu-id="979ed-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
