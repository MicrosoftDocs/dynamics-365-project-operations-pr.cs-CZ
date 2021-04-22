---
title: Deaktivace ceníků
description: Tento téma vysvětluje, jak deaktivovat nebo odstranit nepoužívané nebo staré ceníky.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701918"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="95e8b-103">Deaktivace ceníků</span><span class="sxs-lookup"><span data-stu-id="95e8b-103">Deactivate price lists</span></span> 

<span data-ttu-id="95e8b-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="95e8b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="95e8b-105">K odebráních starých nebo nepoužívaných ceníků z Dynamics 365 Project Operations musíte provést dva kroky.</span><span class="sxs-lookup"><span data-stu-id="95e8b-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="95e8b-106">Odeberte nebo odstraňte ceník z konkrétních stránek.</span><span class="sxs-lookup"><span data-stu-id="95e8b-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="95e8b-107">Deaktivujte nebo odstraňte ceník z aktivních ceníků na stránce **Ceníky**.</span><span class="sxs-lookup"><span data-stu-id="95e8b-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="95e8b-108">K úplnému odstranění ceníku musíte provést oba kroky.</span><span class="sxs-lookup"><span data-stu-id="95e8b-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="95e8b-109">Nestačí pouze provedení kroku 2, kterým je přímé odstranění nebo deaktivace ceníku z pohledu Aktivní ceníky.</span><span class="sxs-lookup"><span data-stu-id="95e8b-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="95e8b-110">Také musíte odstranit přidružení tohoto ceníku ze všech míst uvedených v kroku 1.</span><span class="sxs-lookup"><span data-stu-id="95e8b-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="95e8b-111">Odstranění ceníku z konkrétních stránek</span><span class="sxs-lookup"><span data-stu-id="95e8b-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="95e8b-112">Chcete-li odstranit ceník z Project Operations, přejděte na následující stránky:</span><span class="sxs-lookup"><span data-stu-id="95e8b-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="95e8b-113">Karta **Parametry projektu** > karta **Ceníky**</span><span class="sxs-lookup"><span data-stu-id="95e8b-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="95e8b-114">Stránka **Organizační jednotka** > mřížka **Ceníky**</span><span class="sxs-lookup"><span data-stu-id="95e8b-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="95e8b-115">Stránka **Účet** > mřížka **Ceníky projektu**</span><span class="sxs-lookup"><span data-stu-id="95e8b-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="95e8b-116">Stránka **Cenové nabídky projektu** > mřížka **Ceníky projektu**: To platí pro všechny aktivní nabídky projektu.</span><span class="sxs-lookup"><span data-stu-id="95e8b-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="95e8b-117">Stránka **Smlouvy projektu** > mřížka **Ceníky projektu**: To platí pro všechny aktivní smlouvy projektu.</span><span class="sxs-lookup"><span data-stu-id="95e8b-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="95e8b-118">U každé stránky musíte vybrat ceník, který chcete odstranit, a poté vybrat **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="95e8b-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="95e8b-119">Odstranění nebo deaktivace ceníku z aktivních ceníků na stránce Ceníky</span><span class="sxs-lookup"><span data-stu-id="95e8b-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="95e8b-120">Chcete-li odstranit ceník z aktivních ceníků, přejděte na **Prodej** > **Zákazníci** > **Ceníky**.</span><span class="sxs-lookup"><span data-stu-id="95e8b-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="95e8b-121">Vyberte ceník, který chcete odstranit, a vyberte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="95e8b-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="95e8b-122">Pokud se na ceník odkazuje na jakékoli existující transakce, nebudete jej moci odstranit.</span><span class="sxs-lookup"><span data-stu-id="95e8b-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="95e8b-123">Pokud k tomu dojde, můžete deaktivovat ceník, aby se nezobrazil v žádném zobrazení.</span><span class="sxs-lookup"><span data-stu-id="95e8b-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="95e8b-124">Chcete-li deaktivovat ceník, vyberte znovu ceník a poté vyberte **Deaktivovat**.</span><span class="sxs-lookup"><span data-stu-id="95e8b-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
