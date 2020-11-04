---
title: Kalendář časových záznamů
description: Toto téma obsahuje informace o způsobu použití kalendáře časových záznamů.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: afc31609c51f48db61ce359c18707b5a92211082
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073870"
---
# <a name="time-entry-calendar"></a><span data-ttu-id="e07c3-103">Kalendář časových záznamů</span><span class="sxs-lookup"><span data-stu-id="e07c3-103">Time entry calendar</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e07c3-104">Na stránce **Časové záznamy** můžete zobrazit časové záznamy v kalendáři výběrem možnosti **Zobrazit jako** \> **Ovládací prvek kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="e07c3-104">On the **Time Entries** page, you can view the time entries on the calendar by selecting **Show as** \> **Calendar Control**.</span></span>

## <a name="updated-calendar-control"></a><span data-ttu-id="e07c3-105">Aktualizovaný ovládací prvek kalendáře</span><span class="sxs-lookup"><span data-stu-id="e07c3-105">Updated calendar control</span></span>

<span data-ttu-id="e07c3-106">Dynamics 365 Project Service Automation nabízí nové a rozšiřitelné možnosti zadávání času.</span><span class="sxs-lookup"><span data-stu-id="e07c3-106">Dynamics 365 Project Service Automation offers a new and extensible time entry experience.</span></span> <span data-ttu-id="e07c3-107">Tato nová funkce nahrazuje vlastní ovládací prvek kalendáře, který byl použit v dřívějších verzích.</span><span class="sxs-lookup"><span data-stu-id="e07c3-107">This new experience replaces the Custom Calendar Control that was used in earlier versions.</span></span> <span data-ttu-id="e07c3-108">Časové záznamy však můžete stále zobrazit prostřednictvím ovládacího prvku kalendáře jen pro čtení, který poskytuje architektura Sjednocené rozhraní pro denní, týdenní nebo měsíční zobrazení.</span><span class="sxs-lookup"><span data-stu-id="e07c3-108">However, you can still view time entries through a read-only calendar control that the Unified Interface Framework provides for daily, weekly, or monthly views.</span></span>

<span data-ttu-id="e07c3-109">Kalendář nepodporuje akce jednotlivých položek kalendáře a nelze vybrat jednu nebo více položek kalendáře pro odeslání nebo odstranění.</span><span class="sxs-lookup"><span data-stu-id="e07c3-109">The calendar doesn't support actions on individual calendar items, and you can't select one or more calendar items for submission or deletion.</span></span> <span data-ttu-id="e07c3-110">Místo toho vyberte položku kalendáře pro otevření stránky entity **Časový záznam** , kde můžete provést požadované akce.</span><span class="sxs-lookup"><span data-stu-id="e07c3-110">Instead, select a calendar item to open the **Time Entry** entity page, where you can complete the required actions.</span></span>

## <a name="extensibility"></a><span data-ttu-id="e07c3-111">Rozšiřitelnost</span><span class="sxs-lookup"><span data-stu-id="e07c3-111">Extensibility</span></span>

<span data-ttu-id="e07c3-112">Na stránce **Časové záznamy** s mřížkou zadávání času můžete přidávat vlastní pole, nastavovat vyhledávací pole a vytvářet vlastní zobrazení.</span><span class="sxs-lookup"><span data-stu-id="e07c3-112">On the **Time Entries** page that has the time entry grid, you can add custom fields, set up lookup fields, and create custom views.</span></span> <span data-ttu-id="e07c3-113">Můžete také nastavit vlastní obchodní logiku, která je založena na hodnotách vybraných nebo zadaných do vlastních polí.</span><span class="sxs-lookup"><span data-stu-id="e07c3-113">You can also set up custom business logic that is based on the values that are selected or entered in custom fields.</span></span>
