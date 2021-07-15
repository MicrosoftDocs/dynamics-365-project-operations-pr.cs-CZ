---
title: Přehled uznání výnosů
description: Toto téma obsahuje informace o uznání výnosů v Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368018"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="69f7b-103">Přehled uznání výnosů</span><span class="sxs-lookup"><span data-stu-id="69f7b-103">Revenue recognition overview</span></span>

<span data-ttu-id="69f7b-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="69f7b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="69f7b-105">v Dynamics 365 Project Operations se zásady uznání výnosů liší podle vybrané metody fakturace pro projekt nebo část projektu.</span><span class="sxs-lookup"><span data-stu-id="69f7b-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="69f7b-106">Toto téma obsahuje informace o uznání výnosů v Project Operations.</span><span class="sxs-lookup"><span data-stu-id="69f7b-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="69f7b-107">Zaúčtování transakcí pomocí způsobu fakturace času a materiálu</span><span class="sxs-lookup"><span data-stu-id="69f7b-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="69f7b-108">Uznávání nákladů a výnosů je propojeno.</span><span class="sxs-lookup"><span data-stu-id="69f7b-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="69f7b-109">Transakční náklady a nevyfakturované prodeje se zaúčtují pomocí [Deníku integrace Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="69f7b-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="69f7b-110">Profil nákladů a výnosů projektu určuje, zda se nevyfakturované prodejní transakce zaúčtují do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="69f7b-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="69f7b-111">Je-li vybráno **Časově rozlišené výnosy**, systém během účtování použije účty **Hodnota prodeje probíhající práce (WIP)** a **Časově rozlišené výnosy – hodnota prodeje**.</span><span class="sxs-lookup"><span data-stu-id="69f7b-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="69f7b-112">Následuje příklad této metody.</span><span class="sxs-lookup"><span data-stu-id="69f7b-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="69f7b-113">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="69f7b-113">Transaction type</span></span> | <span data-ttu-id="69f7b-114">Debet / kredit</span><span class="sxs-lookup"><span data-stu-id="69f7b-114">Debit/Credit</span></span> | <span data-ttu-id="69f7b-115">Množství</span><span class="sxs-lookup"><span data-stu-id="69f7b-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="69f7b-116">Hodnota prodeje probíhající práce</span><span class="sxs-lookup"><span data-stu-id="69f7b-116">WIP Sales value</span></span> | <span data-ttu-id="69f7b-117">Debet</span><span class="sxs-lookup"><span data-stu-id="69f7b-117">Debit</span></span> | <span data-ttu-id="69f7b-118">100</span><span class="sxs-lookup"><span data-stu-id="69f7b-118">100</span></span> |
  | <span data-ttu-id="69f7b-119">Časově rozlišené výnosy – hodnota prodeje</span><span class="sxs-lookup"><span data-stu-id="69f7b-119">Accrued revenue sales value</span></span> | <span data-ttu-id="69f7b-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="69f7b-120">Credit</span></span> | <span data-ttu-id="69f7b-121">100</span><span class="sxs-lookup"><span data-stu-id="69f7b-121">100</span></span> |

- <span data-ttu-id="69f7b-122">Výnosy jsou uznané při fakturaci.</span><span class="sxs-lookup"><span data-stu-id="69f7b-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="69f7b-123">Systém používá úšet **Fakturované výnosy** během účtování.</span><span class="sxs-lookup"><span data-stu-id="69f7b-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="69f7b-124">Následuje příklad této metody.</span><span class="sxs-lookup"><span data-stu-id="69f7b-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="69f7b-125">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="69f7b-125">Transaction type</span></span> | <span data-ttu-id="69f7b-126">Debet / kredit</span><span class="sxs-lookup"><span data-stu-id="69f7b-126">Debit/Credit</span></span> | <span data-ttu-id="69f7b-127">Množství</span><span class="sxs-lookup"><span data-stu-id="69f7b-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="69f7b-128">Zůstatek zákazníka</span><span class="sxs-lookup"><span data-stu-id="69f7b-128">Customer balance</span></span> | <span data-ttu-id="69f7b-129">Debet</span><span class="sxs-lookup"><span data-stu-id="69f7b-129">Debit</span></span> | <span data-ttu-id="69f7b-130">120</span><span class="sxs-lookup"><span data-stu-id="69f7b-130">120</span></span> |
  | <span data-ttu-id="69f7b-131">Splatná DPH</span><span class="sxs-lookup"><span data-stu-id="69f7b-131">Sales tax payable</span></span> | <span data-ttu-id="69f7b-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="69f7b-132">Credit</span></span> | <span data-ttu-id="69f7b-133">20</span><span class="sxs-lookup"><span data-stu-id="69f7b-133">20</span></span> |
  | <span data-ttu-id="69f7b-134">Fakturované výnosy</span><span class="sxs-lookup"><span data-stu-id="69f7b-134">Invoiced Revenue</span></span> | <span data-ttu-id="69f7b-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="69f7b-135">Credit</span></span> | <span data-ttu-id="69f7b-136">100</span><span class="sxs-lookup"><span data-stu-id="69f7b-136">100</span></span> |

- <span data-ttu-id="69f7b-137">Pokud byly výnosy časově rozlišeny při zaúčtování nevyfakturovaných prodejů, systém tyto nashromážděné výnosy při fakturaci stornuje.</span><span class="sxs-lookup"><span data-stu-id="69f7b-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="69f7b-138">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="69f7b-138">Transaction type</span></span> | <span data-ttu-id="69f7b-139">Debet / kredit</span><span class="sxs-lookup"><span data-stu-id="69f7b-139">Debit/Credit</span></span> | <span data-ttu-id="69f7b-140">Množství</span><span class="sxs-lookup"><span data-stu-id="69f7b-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="69f7b-141">Hodnota prodeje probíhající práce</span><span class="sxs-lookup"><span data-stu-id="69f7b-141">WIP Sales value</span></span> | <span data-ttu-id="69f7b-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="69f7b-142">Credit</span></span> | <span data-ttu-id="69f7b-143">100</span><span class="sxs-lookup"><span data-stu-id="69f7b-143">100</span></span> |
  | <span data-ttu-id="69f7b-144">Časově rozlišené výnosy – hodnota prodeje</span><span class="sxs-lookup"><span data-stu-id="69f7b-144">Accrued revenue sales value</span></span> | <span data-ttu-id="69f7b-145">Debet</span><span class="sxs-lookup"><span data-stu-id="69f7b-145">Debit</span></span> | <span data-ttu-id="69f7b-146">100</span><span class="sxs-lookup"><span data-stu-id="69f7b-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="69f7b-147">Zaúčtování transakcí pomocí způsobu fakturace fixní ceny</span><span class="sxs-lookup"><span data-stu-id="69f7b-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="69f7b-148">Uznávání nákladů a výnosů je samostatné.</span><span class="sxs-lookup"><span data-stu-id="69f7b-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="69f7b-149">Transakční náklady se zaúčtují pomocí [Deníku integrace Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="69f7b-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="69f7b-150">Nevyfakturované prodejní transakce se nevytvářejí.</span><span class="sxs-lookup"><span data-stu-id="69f7b-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="69f7b-151">Výnosy lze uznat během fakturace, pokud má profil nákladů a výnosy projektu vobu **Zásada použitá pro výpočty dokončení projektu** nastavenou na **Žádné probíhající práce**.</span><span class="sxs-lookup"><span data-stu-id="69f7b-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="69f7b-152">Tuto metodu používejte pouze pro krátkodobé jednoduché projekty.</span><span class="sxs-lookup"><span data-stu-id="69f7b-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="69f7b-153">Výnosy lze uznat pomocí odhadů výnosů s fixní cenou, a to buď metodou **Dokončená smlouva** nebo **Uznání výnosů z procentuálního dokončení**.</span><span class="sxs-lookup"><span data-stu-id="69f7b-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69f7b-154">Další materiály</span><span class="sxs-lookup"><span data-stu-id="69f7b-154">Additional resources</span></span>
[<span data-ttu-id="69f7b-155">Článek Konfigurace účetnictví pro fakturovatelné projekty</span><span class="sxs-lookup"><span data-stu-id="69f7b-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="69f7b-156">Projekty odhadu výnosů pevné ceny</span><span class="sxs-lookup"><span data-stu-id="69f7b-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="69f7b-157">Správa odhadů výnosů</span><span class="sxs-lookup"><span data-stu-id="69f7b-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="69f7b-158">Náklady na dokončení metod</span><span class="sxs-lookup"><span data-stu-id="69f7b-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]