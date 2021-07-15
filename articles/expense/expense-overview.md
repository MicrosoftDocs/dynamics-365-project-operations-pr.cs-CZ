---
title: Přehled výdajů
description: Tento téma poskytuje informace o funkci Výdaje ve službě Project Operations.
author: stsporen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 921df6fa8f1eb33bd01792c0b7c787fc74604adf
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368558"
---
# <a name="expense-home-page"></a><span data-ttu-id="434f2-103">Domovská stránka výdajů</span><span class="sxs-lookup"><span data-stu-id="434f2-103">Expense home page</span></span>

<span data-ttu-id="434f2-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="434f2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="434f2-105">Dynamics 365 Project Operations podporuje schopnost zpracovávat výdaje.</span><span class="sxs-lookup"><span data-stu-id="434f2-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="434f2-106">Ke zpracování výdajů dochází s projekty nebo bez projektů pomocí přizpůsobitelného pracovního postupu zásad, kategorií transakcí a schválení.</span><span class="sxs-lookup"><span data-stu-id="434f2-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="434f2-107">V Project Operations existují dva podporované modely nasazení pro výdaj:</span><span class="sxs-lookup"><span data-stu-id="434f2-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="434f2-108">**Plné**: Plné nasazení je k dispozici pro **Project Operations pro scénáře se zdroji bez skladových materiálů** nebo **Project Operations pro scénáře založené na výrobním příkazu**.</span><span class="sxs-lookup"><span data-stu-id="434f2-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="434f2-109">**Základní**: Základní nasazení je k dispozici pr **Project Operations pro scénáře se zdroji bez skladových materiálů** a **Omezené nasazení - od obchodu po pro forma fakturaci**.</span><span class="sxs-lookup"><span data-stu-id="434f2-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="434f2-110">Úplný</span><span class="sxs-lookup"><span data-stu-id="434f2-110">Full</span></span> 
<span data-ttu-id="434f2-111">Plné nasazení výdajů poskytuje úplné vynucování zásad, které zahrnuje schopnost vytvářet zásady, například:</span><span class="sxs-lookup"><span data-stu-id="434f2-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="434f2-112">Limity kategorií výdajů</span><span class="sxs-lookup"><span data-stu-id="434f2-112">Expense category limits</span></span>
  - <span data-ttu-id="434f2-113">Cesta</span><span class="sxs-lookup"><span data-stu-id="434f2-113">Travel</span></span>
  - <span data-ttu-id="434f2-114">Denní diety</span><span class="sxs-lookup"><span data-stu-id="434f2-114">Per diem</span></span>
  - <span data-ttu-id="434f2-115">Import platebních karet</span><span class="sxs-lookup"><span data-stu-id="434f2-115">Credit card imports</span></span>
  - <span data-ttu-id="434f2-116">Příjem optického rozpoznávání znaků</span><span class="sxs-lookup"><span data-stu-id="434f2-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="434f2-117">Základní</span><span class="sxs-lookup"><span data-stu-id="434f2-117">Basic</span></span> 
<span data-ttu-id="434f2-118">Scénář nasazení pro základní výdaje umožňuje pouze zaznamenat základní výdaje proti projektu.</span><span class="sxs-lookup"><span data-stu-id="434f2-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="434f2-119">Další informace viz [Výdajový záznam (omezený)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="434f2-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="434f2-120">Určení typu nasazení pro výdaje</span><span class="sxs-lookup"><span data-stu-id="434f2-120">Determine your Expense deployment</span></span>
<span data-ttu-id="434f2-121">Chcete-li zjistit, zda používáte nasazení pro správu základních výdajů, ověřte, zda adresa URL končí na **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="434f2-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]