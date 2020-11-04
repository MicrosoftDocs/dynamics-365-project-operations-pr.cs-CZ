---
title: Udržování členů týmu
description: Toto téma obsahuje informace o rezervaci pojmenovaných zdrojů pro projektové týmy a jejich přiřazování k úkolům.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073646"
---
# <a name="maintain-team-members"></a><span data-ttu-id="ad649-103">Udržování členů týmu</span><span class="sxs-lookup"><span data-stu-id="ad649-103">Maintain team members</span></span>

<span data-ttu-id="ad649-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="ad649-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ad649-105">Pojmenovaný zdroj můžete do vašeho projektového týmu přidat pomocí jejich přímé rezervace pro tým.</span><span class="sxs-lookup"><span data-stu-id="ad649-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="ad649-106">V aplikaci Dynamics 365 Project Operations přejděte na **Projekty** a vyberte otevření projektu, pro který provádíte rezervaci.</span><span class="sxs-lookup"><span data-stu-id="ad649-106">In Dynamics 365 Project Operations, go to **Projects** , and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="ad649-107">Na stránce **Projekt** vyberte na kartě **Tým** položku **Nový**.</span><span class="sxs-lookup"><span data-stu-id="ad649-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="ad649-108">V dialogovém okně **Vytvořit: Člen projektového týmu** vyberte rezervovatelný zdroj.</span><span class="sxs-lookup"><span data-stu-id="ad649-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="ad649-109">Pole **Role** se vyplní výchozí rolí zdroje, pokud je přiřazena.</span><span class="sxs-lookup"><span data-stu-id="ad649-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="ad649-110">Roli je možné změnit.</span><span class="sxs-lookup"><span data-stu-id="ad649-110">You can change the role.</span></span> 
4. <span data-ttu-id="ad649-111">Vyberte datumy začátku a konce období, kdy bude zdroj vyžadován, a vyberte metodu přidělení kapacity zdroje.</span><span class="sxs-lookup"><span data-stu-id="ad649-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="ad649-112">Pokud chcete, aby byl člen týmu schvalovatelem projektu, vyberte v poli **Schvalovatel projektu** hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ad649-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="ad649-113">Člen týmu může schválit odeslané časové a výdajové záznamy pro tento projekt.</span><span class="sxs-lookup"><span data-stu-id="ad649-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="ad649-114">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ad649-114">Select **Save**.</span></span>

<span data-ttu-id="ad649-115">Nyní můžete rezervovaný zdroj přiřadit k úkolům v projektu.</span><span class="sxs-lookup"><span data-stu-id="ad649-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="ad649-116">Na stránce **Projekt** na kartě **Plán** přiřaďte úkoly k novému zdroji,.</span><span class="sxs-lookup"><span data-stu-id="ad649-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="ad649-117">Výběr zdroje, který se spouští z pole **Zdroje** v mřížce úkolu, zobrazí členy týmu, které můžete vybrat.</span><span class="sxs-lookup"><span data-stu-id="ad649-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="ad649-118">V aplikaci Project Operations nejsou rezervace zdrojů a přiřazení úkolů pevně spojeny.</span><span class="sxs-lookup"><span data-stu-id="ad649-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="ad649-119">Když použijete výběr zdroje v plánu, můžete členům týmu přiřadit úkoly na více hodin, než jejich rezervace pokrývají projekt.</span><span class="sxs-lookup"><span data-stu-id="ad649-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="ad649-120">Rozdíly mezi rezervacemi a přiřazením člena týmu jsou uvedeny na kartách **Tým** a **Odsouhlasení zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="ad649-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="ad649-121">Můžete také odsouhlasit rozdíly mezi rezervacemi a přiřazeními zdrojů na podrobnější úrovni.</span><span class="sxs-lookup"><span data-stu-id="ad649-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="ad649-122">Pomocí výběru zdroje na kartě **Plán** vyhledejte a vyberte rezervovatelné zdroje, které ještě nejsou součástí projektového týmu.</span><span class="sxs-lookup"><span data-stu-id="ad649-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="ad649-123">Tyto zdroje jsou ve výběru zdroje zobrazeny jako **Další zdroje**.</span><span class="sxs-lookup"><span data-stu-id="ad649-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="ad649-124">Po provedení výběru bude zdroj přidán do projektového týmu a přiřazen k úkolu, ale nebudou generovány žádné rezervace.</span><span class="sxs-lookup"><span data-stu-id="ad649-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="ad649-125">K rezervaci kapacity zdroje pro projekt můžete použít funkci prodloužení rezervace na kartě **Vyrovnání** nebo **Plánovací vývěska**.</span><span class="sxs-lookup"><span data-stu-id="ad649-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="ad649-126">Po rezervaci člena týmu ve vašem projektu můžete přímo spravovat jejich rezervace pomocí funkcí **Správa rezervací** **Plánovací vývěska**.</span><span class="sxs-lookup"><span data-stu-id="ad649-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
