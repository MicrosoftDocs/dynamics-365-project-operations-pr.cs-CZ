---
title: Odhady výdajů
description: Tento téma poskytuje informace o definování nebo odhadu nákladů na projekt.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3f0429366c69346113003355679c055cd2c74ca3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287050"
---
# <a name="expense-estimates"></a><span data-ttu-id="5bc39-103">Odhady výdajů</span><span class="sxs-lookup"><span data-stu-id="5bc39-103">Expense estimates</span></span>
<span data-ttu-id="5bc39-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="5bc39-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5bc39-105">Spolu s definováním odhadů založených na zdrojích Dynamics 365 Project Operations umožňuje projektovým manažerům definovat projektové výdaje pro každý projekt.</span><span class="sxs-lookup"><span data-stu-id="5bc39-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="5bc39-106">Každá výdajová položka může být spojena s konkrétním úkolem projektu nebo kategorií výdajů.</span><span class="sxs-lookup"><span data-stu-id="5bc39-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="5bc39-107">Kategorie výdajů jsou obvykle definovány na úrovni organizace.</span><span class="sxs-lookup"><span data-stu-id="5bc39-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="5bc39-108">Cena pro každou kategorii výdajů je obvykle definována v následující hierarchii:</span><span class="sxs-lookup"><span data-stu-id="5bc39-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="5bc39-109">Organizace</span><span class="sxs-lookup"><span data-stu-id="5bc39-109">Organization</span></span>
- <span data-ttu-id="5bc39-110">Zákazník</span><span class="sxs-lookup"><span data-stu-id="5bc39-110">Customer</span></span>
- <span data-ttu-id="5bc39-111">Nabídka / smlouva</span><span class="sxs-lookup"><span data-stu-id="5bc39-111">Quote/contract</span></span>

<span data-ttu-id="5bc39-112">Chcete-li zobrazit, přidat nebo odstranit náklady na projekt, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="5bc39-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="5bc39-113">Přejděte na **Projekty** a vyberte projekt, na kterém chcete pracovat.</span><span class="sxs-lookup"><span data-stu-id="5bc39-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="5bc39-114">Vyberte kartu **Odhady projektu** a zobrazte seznam výdajů projektu.</span><span class="sxs-lookup"><span data-stu-id="5bc39-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="5bc39-115">Vyberte **Nový výdaj**, chcete-li přidat výdaj.</span><span class="sxs-lookup"><span data-stu-id="5bc39-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="5bc39-116">Nebo vyberte výdaj, který chcete odstranit, a poté vyberte **Smazat výdaj**.</span><span class="sxs-lookup"><span data-stu-id="5bc39-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="5bc39-117">Pro každou položku řádku výdajů jsou definovány následující atributy:</span><span class="sxs-lookup"><span data-stu-id="5bc39-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="5bc39-118">**Kategorie**: Společná seskupení používaná k popisu všech nákladů vynaložených na projekt.</span><span class="sxs-lookup"><span data-stu-id="5bc39-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="5bc39-119">**Počáteční datum**: Datum, kdy se předpokládá vznik výdajů.</span><span class="sxs-lookup"><span data-stu-id="5bc39-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="5bc39-120">**Množství**: Odhadovaný počet výdajových položek pro konkrétní kategorii.</span><span class="sxs-lookup"><span data-stu-id="5bc39-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="5bc39-121">**Nákladová cena jednotky**: Jednotková cena použitá k výpočtu nákladů.</span><span class="sxs-lookup"><span data-stu-id="5bc39-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="5bc39-122">**Prodejní cena jednotky**: Jednotková cena použitá k výpočtu prodejní ceny výdaje.</span><span class="sxs-lookup"><span data-stu-id="5bc39-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]