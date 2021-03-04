---
title: Požadavky na předběžnou rezervaci
description: Toto téma obsahuje informace o požadavcích na předběžnou rezervaci.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 09f7acb95be014034cc03d7eed9d37363d430601
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147375"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="e34d2-103">Požadavky na předběžnou rezervaci</span><span class="sxs-lookup"><span data-stu-id="e34d2-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e34d2-104">Požadavek na zdroj může být rezervovaný závazně.</span><span class="sxs-lookup"><span data-stu-id="e34d2-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="e34d2-105">Závazná rezervace vytvoří návrh, který spotřebovává kapacitu zdroje.</span><span class="sxs-lookup"><span data-stu-id="e34d2-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="e34d2-106">Návrh je poté odeslán zpět žadateli ke schválení.</span><span class="sxs-lookup"><span data-stu-id="e34d2-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="e34d2-107">Předběžná rezervace předběžně přidá zdroj do projektového týmu a má jiný stav v Plánovací vývěsce, ale nespotřebovává kapacitu zdroje.</span><span class="sxs-lookup"><span data-stu-id="e34d2-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="e34d2-108">Chcete-li předběžně rezervovat zdroj z Plánovací vývěsky, nastavte pole **Stav rezervace** na **Předběžná**.</span><span class="sxs-lookup"><span data-stu-id="e34d2-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Stav rezervace nastavený na Předběžná](media/Resource-Management-image77.png)

<span data-ttu-id="e34d2-110">Pokud je karta **Tým** v zobrazení **Pojmenovaní členové týmu**, zdroj se zde zobrazí.</span><span class="sxs-lookup"><span data-stu-id="e34d2-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="e34d2-111">Předběžně rezervované hodiny jsou hlášeny ve sloupci **Předběžně rezervované hodiny**.</span><span class="sxs-lookup"><span data-stu-id="e34d2-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Předběžně rezervované hodiny v zobrazení Pojmenovaní členové týmu](media/Resource-Management-image78.png)

<span data-ttu-id="e34d2-113">Předběžně rezervované členy týmu lze přiřadit k úkolům.</span><span class="sxs-lookup"><span data-stu-id="e34d2-113">Soft-booked team members can be assigned to tasks.</span></span>

![Předběžně rezervovaný člen týmu přiřazený k úkolu](media/Resource-Management-image79.png)

<span data-ttu-id="e34d2-115">Na kartě **Vyrovnání** se u předběžně rezervovaného zdroje nezobrazují žádné rezervace, protože karta **Vyrovnání** zohledňuje pouze závazné rezervace.</span><span class="sxs-lookup"><span data-stu-id="e34d2-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Předběžně rezervovaný zdroj bez rezervací na kartě Vyrovnání](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="e34d2-117">Z požadavku, který vygeneroval obecný člen týmu, nelze provést předběžnou rezervaci zdroje.</span><span class="sxs-lookup"><span data-stu-id="e34d2-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="e34d2-118">V Plánovací vývěsce se pro předběžné rezervace zdrojů používá odlišné zbarvení.</span><span class="sxs-lookup"><span data-stu-id="e34d2-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Předběžné rezervace v Plánovací vývěsce](media/Resource-Management-image81.png)

<span data-ttu-id="e34d2-120">Chcete-li změnit předběžnou rezervaci na závaznou rezervaci, klikněte v Plánovací vývěsce na předběžnou rezervaci pravým tlačítkem myši a pak vyberte **Změnit stav** \> **Závazně rezervovat** \> **Závazná**.</span><span class="sxs-lookup"><span data-stu-id="e34d2-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Změna stavu rezervace na Závazná](media/Resource-Management-image82.png)

<span data-ttu-id="e34d2-122">Rezervace se změní a změní se stav v Plánovací vývěsce.</span><span class="sxs-lookup"><span data-stu-id="e34d2-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="e34d2-123">Vzhledem k tomu, že stav je nyní **Závazná**, zdroj je zobrazen jako rezervovaný a je upravena jeho kapacita a dostupnost.</span><span class="sxs-lookup"><span data-stu-id="e34d2-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="e34d2-124">Stejný postup můžete použít ke zrušení závazné rezervace nebo předběžné rezervace z Plánovací vývěsky.</span><span class="sxs-lookup"><span data-stu-id="e34d2-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="e34d2-125">Chcete-li změnit zdroj, který je na kartě **Tým** předběžně rezervovaný na závazně rezervovaný, vyberte zdroj a pak vyberte **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="e34d2-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Příkaz Potvrdit](media/Resource-Management-image83.png)
