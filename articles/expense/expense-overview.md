---
title: Přehled výdajů
description: Tento téma poskytuje informace o funkci Výdaje ve službě Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 0874b3d89e1dc0e65a51cedb82bf8f80831ca0bb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967358"
---
# <a name="expense-home-page"></a><span data-ttu-id="b83ba-103">Domovská stránka výdajů</span><span class="sxs-lookup"><span data-stu-id="b83ba-103">Expense home page</span></span>

<span data-ttu-id="b83ba-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="b83ba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b83ba-105">Dynamics 365 Project Operations podporuje schopnost zpracovávat výdaje.</span><span class="sxs-lookup"><span data-stu-id="b83ba-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="b83ba-106">Ke zpracování výdajů dochází s projekty nebo bez projektů pomocí přizpůsobitelného pracovního postupu zásad, kategorií transakcí a schválení.</span><span class="sxs-lookup"><span data-stu-id="b83ba-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="b83ba-107">V Project Operations existují dva podporované modely nasazení pro výdaj:</span><span class="sxs-lookup"><span data-stu-id="b83ba-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="b83ba-108">**Plné**: Plné nasazení je k dispozici pro **Project Operations pro scénáře se zdroji bez skladových materiálů** nebo **Project Operations pro scénáře založené na výrobním příkazu**.</span><span class="sxs-lookup"><span data-stu-id="b83ba-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="b83ba-109">**Základní**: Základní nasazení je k dispozici pr **Project Operations pro scénáře se zdroji bez skladových materiálů** a **Omezené nasazení - od obchodu po pro forma fakturaci**.</span><span class="sxs-lookup"><span data-stu-id="b83ba-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="b83ba-110">Úplný</span><span class="sxs-lookup"><span data-stu-id="b83ba-110">Full</span></span> 
<span data-ttu-id="b83ba-111">Nasazení pro plné výdaje poskytuje úplné vynucování zásad, které zahrnuje schopnost vytvářet zásady, například:</span><span class="sxs-lookup"><span data-stu-id="b83ba-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="b83ba-112">Limity kategorií výdajů</span><span class="sxs-lookup"><span data-stu-id="b83ba-112">Expense category limits</span></span>
  - <span data-ttu-id="b83ba-113">Cesta</span><span class="sxs-lookup"><span data-stu-id="b83ba-113">Travel</span></span>
  - <span data-ttu-id="b83ba-114">Denní diety</span><span class="sxs-lookup"><span data-stu-id="b83ba-114">Per diem</span></span>
  - <span data-ttu-id="b83ba-115">Import platebních karet</span><span class="sxs-lookup"><span data-stu-id="b83ba-115">Credit card imports</span></span>
  - <span data-ttu-id="b83ba-116">Příjem optického rozpoznávání znaků</span><span class="sxs-lookup"><span data-stu-id="b83ba-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="b83ba-117">Základní</span><span class="sxs-lookup"><span data-stu-id="b83ba-117">Basic</span></span> 
<span data-ttu-id="b83ba-118">Scénář nasazení pro základní výdaje umožňuje pouze zaznamenat základní výdaje proti projektu.</span><span class="sxs-lookup"><span data-stu-id="b83ba-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="b83ba-119">Další informace viz [Výdajový záznam (omezený)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="b83ba-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="b83ba-120">Určení typu nasazení pro výdaje</span><span class="sxs-lookup"><span data-stu-id="b83ba-120">Determine your Expense deployment</span></span>
<span data-ttu-id="b83ba-121">Chcete-li zjistit, zda používáte nasazení pro správu základních výdajů, ověřte, zda adresa URL končí na **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="b83ba-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
