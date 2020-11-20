---
title: Správa projektových nabídek
description: Toto téma poskytuje informace o projektových nabídkách.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c33adabbd03cca19ae5e7f401f08a716e9242b2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177818"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="fa77e-103">Správa projektových nabídek</span><span class="sxs-lookup"><span data-stu-id="fa77e-103">Manage project quotes</span></span>

<span data-ttu-id="fa77e-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="fa77e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fa77e-105">V Dynamics 365 Project Operations jsou projektové nabídky navrženy tak, aby pomohly vytvářet návrhy pro práci na projektu.</span><span class="sxs-lookup"><span data-stu-id="fa77e-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="fa77e-106">Struktura projektové nabídky v Project Operations je strukturována pro návrhy projektu s následujícími součástmi:</span><span class="sxs-lookup"><span data-stu-id="fa77e-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="fa77e-107">Řádky nabídky, které identifikují jednotlivé součásti práce, které budou představovat součásti na vysoké úrovni.</span><span class="sxs-lookup"><span data-stu-id="fa77e-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="fa77e-108">Podrobnosti řádku nabídky, které identifikují a odhadují práci pro každou součást nebo řádek nabídky na vysoké úrovni.</span><span class="sxs-lookup"><span data-stu-id="fa77e-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="fa77e-109">Plán nebo odhady dat a finanční aspekty práce jsou vázány na daný řádek nabídky.</span><span class="sxs-lookup"><span data-stu-id="fa77e-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="fa77e-110">Smluvní modely a zpoplatněné součásti jsou nastaveny pro každý řádek nabídky.</span><span class="sxs-lookup"><span data-stu-id="fa77e-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="fa77e-111">Toto nastavení pomáhá odhadnout rozložení příjmů, výdajů a ziskovosti pro každý řádek nabídky a celkovou nabídku.</span><span class="sxs-lookup"><span data-stu-id="fa77e-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="fa77e-112">Zobrazení všech nabídek založených na projektu</span><span class="sxs-lookup"><span data-stu-id="fa77e-112">View all project-based quotes</span></span>

<span data-ttu-id="fa77e-113">Seznam nabídek projektu se nachází na stránce se seznamem **Nabídky**.</span><span class="sxs-lookup"><span data-stu-id="fa77e-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="fa77e-114">Přejděte na **Prodej** > **Nabídky**.</span><span class="sxs-lookup"><span data-stu-id="fa77e-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="fa77e-115">Zobrazí se seznam všech vašich projektových nabídek v systému.</span><span class="sxs-lookup"><span data-stu-id="fa77e-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="fa77e-116">Pomocí **přepínače zobrazení** vyberte další filtrovaná zobrazení nabídek.</span><span class="sxs-lookup"><span data-stu-id="fa77e-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="fa77e-117">Pomocí vlastních kritérií filtru můžete nakonfigurovat vlastní zobrazení a možnosti navigace.</span><span class="sxs-lookup"><span data-stu-id="fa77e-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="fa77e-118">Nabídky lze vytvářet nebo mazat z této stránky seznamu nebo stránek podrobností.</span><span class="sxs-lookup"><span data-stu-id="fa77e-118">Quotes can be created or deleted from this list page or detail pages.</span></span>
