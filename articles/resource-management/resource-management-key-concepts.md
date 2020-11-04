---
title: Klíčové koncepty správy zdrojů
description: Toto téma poskytuje informace o funkcích pro správu zdrojů v aplikaci Microsoft Dynamics Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 124d9bad5cc0c16955417a8213db047a2d8bae1d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073627"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="32145-103">Klíčové koncepty správy zdrojů</span><span class="sxs-lookup"><span data-stu-id="32145-103">Resource management key concepts</span></span>

<span data-ttu-id="32145-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="32145-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="32145-105">Zdroje jsou nejdůležitějším majetkem organizace založené na službách.</span><span class="sxs-lookup"><span data-stu-id="32145-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="32145-106">Schopnost najít správné zdroje ve správný čas, rezervovat tyto zdroje pro projekty a udržovat je využité pomáhá organizaci plnit výnosové cíle a cíle spokojenosti zákazníků.</span><span class="sxs-lookup"><span data-stu-id="32145-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="32145-107">Funkci zajišťování zdrojů pro projekt v Dynamics 365 Project Operations můžete použít k provedení těchto úkolů:</span><span class="sxs-lookup"><span data-stu-id="32145-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="32145-108">Vytvoření projektových týmů pomocí rezervace dostupných a kvalifikovaných zdrojů.</span><span class="sxs-lookup"><span data-stu-id="32145-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="32145-109">Vytvoření záznamů obecných členů týmu a definování jejich rolí a organizační jednotky zdroje.</span><span class="sxs-lookup"><span data-stu-id="32145-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="32145-110">Generování požadavků na zdroje pro obecné členy týmu z jejich přiřazení úkolů.</span><span class="sxs-lookup"><span data-stu-id="32145-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="32145-111">Párování dovedností určením dovedností definovaných na poptávce po zdroji vůči dostupným dovednostem zdrojů.</span><span class="sxs-lookup"><span data-stu-id="32145-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="32145-112">Nahrazení zdrojů.</span><span class="sxs-lookup"><span data-stu-id="32145-112">Substitute resources.</span></span>
- <span data-ttu-id="32145-113">Vyrovnání přiřazení plánu projektu a rezervací zdrojů.</span><span class="sxs-lookup"><span data-stu-id="32145-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="32145-114">Vyrovnání rozdílů v rezervacích a přiřazeních.</span><span class="sxs-lookup"><span data-stu-id="32145-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="32145-115">Změna rezervací zdrojů v odezvě na stav mimo kancelář.</span><span class="sxs-lookup"><span data-stu-id="32145-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="32145-116">Spolupráce mezi projektovými manažery a správci zdrojů.</span><span class="sxs-lookup"><span data-stu-id="32145-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="32145-117">Zobrazení historie využití zdrojů oproti cíli, včetně rozpisu způsobu využívání času zdroje.</span><span class="sxs-lookup"><span data-stu-id="32145-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="32145-118">Údržba úložiště dovedností a odbornosti.</span><span class="sxs-lookup"><span data-stu-id="32145-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="32145-119">Projekt můžete v Project Operations personálně obsadit týmem obecných nebo pojmenovaných zdrojů.</span><span class="sxs-lookup"><span data-stu-id="32145-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="32145-120">Pro přidání a přiřazení členů týmu a ke správě jejich rezervací a přiřazení můžete použít různé metody.</span><span class="sxs-lookup"><span data-stu-id="32145-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 
