---
title: Proč je výchozí cena skutečných časových nákladů nastavena na nulu?
description: Odstranění problému, kdy je výchozí cena skutečných časových nákladů nastavena na nulu.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 635fe6dfb547e8b9f96ca1786912309a770e24c2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146250"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="38f2e-103">Proč je výchozí cena skutečných časových nákladů nastavena na nulu?</span><span class="sxs-lookup"><span data-stu-id="38f2e-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="38f2e-104">Tyto často kladené dotazy se týkají skutečných položek, kdy je třída transakce nastavena na Čas a typ transakce na Náklady.</span><span class="sxs-lookup"><span data-stu-id="38f2e-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="38f2e-105">Následující tři kontroly vám pomohou vyřešit, proč je cena skutečných časových nákladů nastavena na nulu.</span><span class="sxs-lookup"><span data-stu-id="38f2e-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="38f2e-106">Kontrola 1: Určete nákladový ceník pro daný projekt</span><span class="sxs-lookup"><span data-stu-id="38f2e-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="38f2e-107">Najděte projekt z oblasti aktuálních nákladu a následně přejděte na stránku projektu.</span><span class="sxs-lookup"><span data-stu-id="38f2e-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="38f2e-108">Klepněte na odkaz smluvní jednotky v poli.</span><span class="sxs-lookup"><span data-stu-id="38f2e-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="38f2e-109">Na stránce Smluvní jednotka zkontrolujte, zda smluvní jednotka má ceník v mřížce Nákladové ceníky.</span><span class="sxs-lookup"><span data-stu-id="38f2e-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="38f2e-110">Pokud existuje více než jeden ceník, odhalili jste problém</span><span class="sxs-lookup"><span data-stu-id="38f2e-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="38f2e-111">Projektové služby podporují pouze jeden ceník na organizační jednotku.</span><span class="sxs-lookup"><span data-stu-id="38f2e-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="38f2e-112">Odstraňte všechny seznamy cen z této entity, dokud nebude v mřížce Nákladové ceníky Organizační jednotky připojen pouze jeden ceník.</span><span class="sxs-lookup"><span data-stu-id="38f2e-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="38f2e-113">Pokud neexistují žádné ceníky připojené k organizační jednotce, poznamenejte si měnu organizační jednotky.</span><span class="sxs-lookup"><span data-stu-id="38f2e-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="38f2e-114">Přejděte na Projektové služby, následně na Parametry a otevřete kartu Ceníky. Zkontrolujte, zda existují ceníky s kontextem nastaveným na Náklady a měnou, která se shoduje s měnou Organizační jednotky.</span><span class="sxs-lookup"><span data-stu-id="38f2e-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="38f2e-115">Pokud neexistují žádné ceníky, které splňují tato kritéria, odhalili jste problém.</span><span class="sxs-lookup"><span data-stu-id="38f2e-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="38f2e-116">Přesvědčte se, zda máte alespoň jeden ceník, jehož kontext je nastaven na Náklady a jehož měna odpovídá měně Organizační jednotky.</span><span class="sxs-lookup"><span data-stu-id="38f2e-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="38f2e-117">Pokud existuje více ceníků, které splňují tato kritéria, pokračujte ve čtení tohoto dokumentu a proveďte další kontroly.</span><span class="sxs-lookup"><span data-stu-id="38f2e-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="38f2e-118">Kontrola 2: Jsou všechny ceníky určené výše platné pro konkrétní datum skutečného časového nákladu?</span><span class="sxs-lookup"><span data-stu-id="38f2e-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="38f2e-119">Aby bylo možné považovat daný ceník projektových služeb za ceník definující výchozí cenu, ceník by měl být platný pro datum aktuálních časových nákladů.</span><span class="sxs-lookup"><span data-stu-id="38f2e-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="38f2e-120">Zkontrolujte následující položky, pokud si přejete zjistit, zda jsou výše uvedené ceníky platné:</span><span class="sxs-lookup"><span data-stu-id="38f2e-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="38f2e-121">Zkontrolujte, zda není počáteční a koncové datum na kartě Obecné pro přiložené ceníky prázdné.</span><span class="sxs-lookup"><span data-stu-id="38f2e-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="38f2e-122">Pokud je počáteční a koncové datum ve výše uvedených cenících prázdné, odhalili jste problém.</span><span class="sxs-lookup"><span data-stu-id="38f2e-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="38f2e-123">Poznamenejte si pole Počáteční datum vašich skutečných časových nákladů a zkontrolujte, zda jsou všechny uvedené ceníky pro toto datum platné.</span><span class="sxs-lookup"><span data-stu-id="38f2e-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="38f2e-124">Například datum skutečných časových nákladů by měl spadat mezi počáteční datum a koncové datum v ceníku.</span><span class="sxs-lookup"><span data-stu-id="38f2e-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="38f2e-125">Pokud pro datum skutečných časových nákladů neexistuje žádný ceník, odhalili jste problém.</span><span class="sxs-lookup"><span data-stu-id="38f2e-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="38f2e-126">Upravte počáteční a koncové datum ceníku pro zajištění, že ceník zahrnuje datum skutečných časových nákladů.</span><span class="sxs-lookup"><span data-stu-id="38f2e-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="38f2e-127">Pokud pro datum skutečných časových nákladů existuje více ceníků, odhalili jste problém.</span><span class="sxs-lookup"><span data-stu-id="38f2e-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="38f2e-128">Můžete to vyřešit úpravou počátečních a koncových dat ceníků tak, aby pouze jeden ceník pokrýval datum skutečných časových nákladů.</span><span class="sxs-lookup"><span data-stu-id="38f2e-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="38f2e-129">Pokud existuje pouze jeden ceník, který je platný pro tyto skutečné časové náklady, přesuňte se na další kontrolu v dokumentu.</span><span class="sxs-lookup"><span data-stu-id="38f2e-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="38f2e-130">Po provedení požadovaných oprav znovu vytvořte položku času, schvalte ji a ověřte, že skutečné časové náklady ukazují platnou cenu.</span><span class="sxs-lookup"><span data-stu-id="38f2e-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="38f2e-131">Kontrola 3: Je v ceníku cena pro ocenění skutečných časových nákladů?</span><span class="sxs-lookup"><span data-stu-id="38f2e-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="38f2e-132">Pokud jste úspěšně dokončili kontrolu 1 a 2, nyní byste měli mít pouze jeden ceník, který platí pro datum skutečných časových nákladů.</span><span class="sxs-lookup"><span data-stu-id="38f2e-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="38f2e-133">Otevřete tento ceník a přejděte na kartu Ceny rolí. Ujistěte se, že je pro konkrétní cenové dimenze u skutečných časových nákladů řádek v mřížce.</span><span class="sxs-lookup"><span data-stu-id="38f2e-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="38f2e-134">Pokud pro konkrétní cenové dimenze u skutečných časových nákladů řádek v mřížce chybí, odhalili jste problém.</span><span class="sxs-lookup"><span data-stu-id="38f2e-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="38f2e-135">Vytvořte řádek v mřížce Ceny rolí pro konkrétní cenové dimenze vašich skutečných časových nákladů.</span><span class="sxs-lookup"><span data-stu-id="38f2e-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="38f2e-136">Jakmile to provedete, znovu vytvořte položku času, schvalte ji a ověřte, že skutečné časové náklady ukazují platnou cenu.</span><span class="sxs-lookup"><span data-stu-id="38f2e-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="38f2e-137">Pokud i přesto nevidíte platnou cenu vašich skutečných časových nákladů po provedení tří výše uvedených kontrol, odešlete prosím lístek podpory.</span><span class="sxs-lookup"><span data-stu-id="38f2e-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



