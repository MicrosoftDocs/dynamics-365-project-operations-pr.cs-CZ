---
title: Přehled uznání výnosů
description: Toto téma obsahuje informace o uznání výnosů v Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013748"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="51763-103">Přehled uznání výnosů</span><span class="sxs-lookup"><span data-stu-id="51763-103">Revenue recognition overview</span></span>

<span data-ttu-id="51763-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="51763-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="51763-105">v Dynamics 365 Project Operations se zásady uznání výnosů liší podle vybrané metody fakturace pro projekt nebo část projektu.</span><span class="sxs-lookup"><span data-stu-id="51763-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="51763-106">Toto téma obsahuje informace o uznání výnosů v Project Operations.</span><span class="sxs-lookup"><span data-stu-id="51763-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="51763-107">Zaúčtování transakcí pomocí způsobu fakturace času a materiálu</span><span class="sxs-lookup"><span data-stu-id="51763-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="51763-108">Uznávání nákladů a výnosů je propojeno.</span><span class="sxs-lookup"><span data-stu-id="51763-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="51763-109">Transakční náklady a nevyfakturované prodeje se zaúčtují pomocí [Deníku integrace Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="51763-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="51763-110">Profil nákladů a výnosů projektu určuje, zda se nevyfakturované prodejní transakce zaúčtují do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="51763-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="51763-111">Je-li vybráno **Časově rozlišené výnosy**, systém během účtování použije účty **Hodnota prodeje probíhající práce (WIP)** a **Časově rozlišené výnosy – hodnota prodeje**.</span><span class="sxs-lookup"><span data-stu-id="51763-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="51763-112">Následuje příklad této metody.</span><span class="sxs-lookup"><span data-stu-id="51763-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="51763-113">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="51763-113">Transaction type</span></span> | <span data-ttu-id="51763-114">Debet / kredit</span><span class="sxs-lookup"><span data-stu-id="51763-114">Debit/Credit</span></span> | <span data-ttu-id="51763-115">Množství</span><span class="sxs-lookup"><span data-stu-id="51763-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="51763-116">Hodnota prodeje probíhající práce</span><span class="sxs-lookup"><span data-stu-id="51763-116">WIP Sales value</span></span> | <span data-ttu-id="51763-117">Debet</span><span class="sxs-lookup"><span data-stu-id="51763-117">Debit</span></span> | <span data-ttu-id="51763-118">100</span><span class="sxs-lookup"><span data-stu-id="51763-118">100</span></span> |
  | <span data-ttu-id="51763-119">Časově rozlišené výnosy – hodnota prodeje</span><span class="sxs-lookup"><span data-stu-id="51763-119">Accrued revenue sales value</span></span> | <span data-ttu-id="51763-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="51763-120">Credit</span></span> | <span data-ttu-id="51763-121">100</span><span class="sxs-lookup"><span data-stu-id="51763-121">100</span></span> |

- <span data-ttu-id="51763-122">Výnosy jsou uznané při fakturaci.</span><span class="sxs-lookup"><span data-stu-id="51763-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="51763-123">Systém používá úšet **Fakturované výnosy** během účtování.</span><span class="sxs-lookup"><span data-stu-id="51763-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="51763-124">Následuje příklad této metody.</span><span class="sxs-lookup"><span data-stu-id="51763-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="51763-125">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="51763-125">Transaction type</span></span> | <span data-ttu-id="51763-126">Debet / kredit</span><span class="sxs-lookup"><span data-stu-id="51763-126">Debit/Credit</span></span> | <span data-ttu-id="51763-127">Množství</span><span class="sxs-lookup"><span data-stu-id="51763-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="51763-128">Zůstatek zákazníka</span><span class="sxs-lookup"><span data-stu-id="51763-128">Customer balance</span></span> | <span data-ttu-id="51763-129">Debet</span><span class="sxs-lookup"><span data-stu-id="51763-129">Debit</span></span> | <span data-ttu-id="51763-130">120</span><span class="sxs-lookup"><span data-stu-id="51763-130">120</span></span> |
  | <span data-ttu-id="51763-131">Splatná DPH</span><span class="sxs-lookup"><span data-stu-id="51763-131">Sales tax payable</span></span> | <span data-ttu-id="51763-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="51763-132">Credit</span></span> | <span data-ttu-id="51763-133">20</span><span class="sxs-lookup"><span data-stu-id="51763-133">20</span></span> |
  | <span data-ttu-id="51763-134">Fakturované výnosy</span><span class="sxs-lookup"><span data-stu-id="51763-134">Invoiced Revenue</span></span> | <span data-ttu-id="51763-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="51763-135">Credit</span></span> | <span data-ttu-id="51763-136">100</span><span class="sxs-lookup"><span data-stu-id="51763-136">100</span></span> |

- <span data-ttu-id="51763-137">Pokud byly výnosy časově rozlišeny při zaúčtování nevyfakturovaných prodejů, systém tyto nashromážděné výnosy při fakturaci stornuje.</span><span class="sxs-lookup"><span data-stu-id="51763-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="51763-138">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="51763-138">Transaction type</span></span> | <span data-ttu-id="51763-139">Debet / kredit</span><span class="sxs-lookup"><span data-stu-id="51763-139">Debit/Credit</span></span> | <span data-ttu-id="51763-140">Množství</span><span class="sxs-lookup"><span data-stu-id="51763-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="51763-141">Hodnota prodeje probíhající práce</span><span class="sxs-lookup"><span data-stu-id="51763-141">WIP Sales value</span></span> | <span data-ttu-id="51763-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="51763-142">Credit</span></span> | <span data-ttu-id="51763-143">100</span><span class="sxs-lookup"><span data-stu-id="51763-143">100</span></span> |
  | <span data-ttu-id="51763-144">Časově rozlišené výnosy – hodnota prodeje</span><span class="sxs-lookup"><span data-stu-id="51763-144">Accrued revenue sales value</span></span> | <span data-ttu-id="51763-145">Debet</span><span class="sxs-lookup"><span data-stu-id="51763-145">Debit</span></span> | <span data-ttu-id="51763-146">100</span><span class="sxs-lookup"><span data-stu-id="51763-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="51763-147">Zaúčtování transakcí pomocí způsobu fakturace fixní ceny</span><span class="sxs-lookup"><span data-stu-id="51763-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="51763-148">Uznávání nákladů a výnosů je samostatné.</span><span class="sxs-lookup"><span data-stu-id="51763-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="51763-149">Transakční náklady se zaúčtují pomocí [Deníku integrace Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="51763-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="51763-150">Nevyfakturované prodejní transakce se nevytvářejí.</span><span class="sxs-lookup"><span data-stu-id="51763-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="51763-151">Výnosy lze uznat během fakturace, pokud má profil nákladů a výnosy projektu vobu **Zásada použitá pro výpočty dokončení projektu** nastavenou na **Žádné probíhající práce**.</span><span class="sxs-lookup"><span data-stu-id="51763-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="51763-152">Tuto metodu používejte pouze pro krátkodobé jednoduché projekty.</span><span class="sxs-lookup"><span data-stu-id="51763-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="51763-153">Výnosy lze uznat pomocí odhadů výnosů s fixní cenou, a to buď metodou **Dokončená smlouva** nebo **Uznání výnosů z procentuálního dokončení**.</span><span class="sxs-lookup"><span data-stu-id="51763-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51763-154">Další materiály</span><span class="sxs-lookup"><span data-stu-id="51763-154">Additional resources</span></span>
[<span data-ttu-id="51763-155">Článek Konfigurace účetnictví pro fakturovatelné projekty</span><span class="sxs-lookup"><span data-stu-id="51763-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="51763-156">Projekty odhadu výnosů pevné ceny</span><span class="sxs-lookup"><span data-stu-id="51763-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="51763-157">Správa odhadů výnosů</span><span class="sxs-lookup"><span data-stu-id="51763-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="51763-158">Náklady na dokončení metod</span><span class="sxs-lookup"><span data-stu-id="51763-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]