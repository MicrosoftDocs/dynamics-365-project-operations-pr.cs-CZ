---
title: Deaktivace ceníků
description: Tento téma vysvětluje, jak deaktivovat nebo odstranit nepoužívané nebo staré ceníky.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001328"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="4dc99-103">Deaktivace ceníků</span><span class="sxs-lookup"><span data-stu-id="4dc99-103">Deactivate price lists</span></span> 

<span data-ttu-id="4dc99-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="4dc99-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4dc99-105">K odebráních starých nebo nepoužívaných ceníků z Dynamics 365 Project Operations musíte provést dva kroky.</span><span class="sxs-lookup"><span data-stu-id="4dc99-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="4dc99-106">Odeberte nebo odstraňte ceník z konkrétních stránek.</span><span class="sxs-lookup"><span data-stu-id="4dc99-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="4dc99-107">Deaktivujte nebo odstraňte ceník z aktivních ceníků na stránce **Ceníky**.</span><span class="sxs-lookup"><span data-stu-id="4dc99-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="4dc99-108">K úplnému odstranění ceníku musíte provést oba kroky.</span><span class="sxs-lookup"><span data-stu-id="4dc99-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="4dc99-109">Nestačí pouze provedení kroku 2, kterým je přímé odstranění nebo deaktivace ceníku z pohledu Aktivní ceníky.</span><span class="sxs-lookup"><span data-stu-id="4dc99-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="4dc99-110">Také musíte odstranit přidružení tohoto ceníku ze všech míst uvedených v kroku 1.</span><span class="sxs-lookup"><span data-stu-id="4dc99-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="4dc99-111">Odstranění ceníku z konkrétních stránek</span><span class="sxs-lookup"><span data-stu-id="4dc99-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="4dc99-112">Chcete-li odstranit ceník z Project Operations, přejděte na následující stránky:</span><span class="sxs-lookup"><span data-stu-id="4dc99-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="4dc99-113">Karta **Parametry projektu** > karta **Ceníky**</span><span class="sxs-lookup"><span data-stu-id="4dc99-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="4dc99-114">Stránka **Organizační jednotka** > mřížka **Ceníky**</span><span class="sxs-lookup"><span data-stu-id="4dc99-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="4dc99-115">Stránka **Účet** > mřížka **Ceníky projektu**</span><span class="sxs-lookup"><span data-stu-id="4dc99-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="4dc99-116">Stránka **Cenové nabídky projektu** > mřížka **Ceníky projektu**: To platí pro všechny aktivní nabídky projektu.</span><span class="sxs-lookup"><span data-stu-id="4dc99-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="4dc99-117">Stránka **Smlouvy projektu** > mřížka **Ceníky projektu**: To platí pro všechny aktivní smlouvy projektu.</span><span class="sxs-lookup"><span data-stu-id="4dc99-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="4dc99-118">U každé stránky musíte vybrat ceník, který chcete odstranit, a poté vybrat **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="4dc99-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="4dc99-119">Odstranění nebo deaktivace ceníku z aktivních ceníků na stránce Ceníky</span><span class="sxs-lookup"><span data-stu-id="4dc99-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="4dc99-120">Chcete-li odstranit ceník z aktivních ceníků, přejděte na **Prodej** > **Zákazníci** > **Ceníky**.</span><span class="sxs-lookup"><span data-stu-id="4dc99-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="4dc99-121">Vyberte ceník, který chcete odstranit, a vyberte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="4dc99-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="4dc99-122">Pokud se na ceník odkazuje na jakékoli existující transakce, nebudete jej moci odstranit.</span><span class="sxs-lookup"><span data-stu-id="4dc99-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="4dc99-123">Pokud k tomu dojde, můžete deaktivovat ceník, aby se nezobrazil v žádném zobrazení.</span><span class="sxs-lookup"><span data-stu-id="4dc99-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="4dc99-124">Chcete-li deaktivovat ceník, vyberte znovu ceník a poté vyberte **Deaktivovat**.</span><span class="sxs-lookup"><span data-stu-id="4dc99-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
