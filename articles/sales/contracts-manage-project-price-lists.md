---
title: Správa projektových ceníků ve smlouvách projektů
description: Tohle téma poskytuje informace o správě projektových ceníků u projektových smluv.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2cfac6eda64d1d8e578115bba07942a7d786328f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278590"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="cf75d-103">Správa projektových ceníků ve smlouvách projektů</span><span class="sxs-lookup"><span data-stu-id="cf75d-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="cf75d-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="cf75d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cf75d-105">Projektové smlouvy v Dynamics 365 Project Operations jsou navrženy tak, aby podporovaly vícedenní efektivní prodejní ceníky pro smlouvy.</span><span class="sxs-lookup"><span data-stu-id="cf75d-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="cf75d-106">V Project Operations existuje nová přidružená entita s názvem **Projektové ceníky**.</span><span class="sxs-lookup"><span data-stu-id="cf75d-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="cf75d-107">Tato entita má vztah 1:N k projektové smlouvě.</span><span class="sxs-lookup"><span data-stu-id="cf75d-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="cf75d-108">Projektové ceníky se používají k oceňování časových a výdajových transakcí na projektu.</span><span class="sxs-lookup"><span data-stu-id="cf75d-108">Project price lists are used to price time and expense transactions on a project.</span></span> <span data-ttu-id="cf75d-109">Pokud má smlouva jeden nebo více projektových ceníků, tyto ceníky se používají k ocenění odhadů času a výdajů a skutečných hodnot u projektů, které jsou přidruženy ke smlouvě prostřednictvím řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="cf75d-109">When a contract has one or more project price lists, these price lists are used to price for time and expense estimates and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="cf75d-110">Pokud v projektové smlouvě nejsou žádné projektové ceníky, zobrazí se varovná zpráva, že neexistují žádné projektové ceníky a vaše odhady, skutečná práce na projektu a výdaje nebudou oceněny.</span><span class="sxs-lookup"><span data-stu-id="cf75d-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, and expenses will not be priced.</span></span> <span data-ttu-id="cf75d-111">Za prodejní hodnoty nebude žádná cena.</span><span class="sxs-lookup"><span data-stu-id="cf75d-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="cf75d-112">Přidružení nebo zrušení přidružení projektového ceníku k projektové smlouvě</span><span class="sxs-lookup"><span data-stu-id="cf75d-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a><span data-ttu-id="cf75d-113">Vytvoření nebo přidružení konkrétního ceníku pro odhad projektové práce a výdajů</span><span class="sxs-lookup"><span data-stu-id="cf75d-113">Create or associate a specific price list for estimating project-based work and expenses</span></span>

1. <span data-ttu-id="cf75d-114">Na projektové smlouvě vyberte kartu **Projektové ceníky**.</span><span class="sxs-lookup"><span data-stu-id="cf75d-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="cf75d-115">V podmřížce vyberte **+ Přidat nový projektový ceník**.</span><span class="sxs-lookup"><span data-stu-id="cf75d-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="cf75d-116">Na posuvníku **Rychlé vytvoření** vyberte ceník.</span><span class="sxs-lookup"><span data-stu-id="cf75d-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="cf75d-117">Rozevírací seznam zobrazuje všechny ceníky, které mají nastaven kontext na **Prodej**, kde se měna ceníku shoduje s měnou smlouvy.</span><span class="sxs-lookup"><span data-stu-id="cf75d-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="cf75d-118">Zadejte popis přidružení projektového ceníku, vyberte **Uložit** a poté zavřete posuvník **Rychlé vytvoření**.</span><span class="sxs-lookup"><span data-stu-id="cf75d-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="cf75d-119">Vytvoří se přidružení projektového ceníku.</span><span class="sxs-lookup"><span data-stu-id="cf75d-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="cf75d-120">Opakováním kroků 1–4 přiřaďte k projektové smlouvě více než jeden projektový ceník.</span><span class="sxs-lookup"><span data-stu-id="cf75d-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="cf75d-121">Více projektových ceníků vytvářejte, pouze pokud máte u každého z přidružených projektových ceníků jiné datum platnosti.</span><span class="sxs-lookup"><span data-stu-id="cf75d-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="cf75d-122">Project Operations nepodporuje překrývající se data platnosti projektových ceníků.</span><span class="sxs-lookup"><span data-stu-id="cf75d-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="cf75d-123">Pokud existuje více projektových ceníků pro transakci s daným datem, cena této transakce bude implicitně nastavena na nulu.</span><span class="sxs-lookup"><span data-stu-id="cf75d-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="cf75d-124">Odebrání přidružení projektového ceníku</span><span class="sxs-lookup"><span data-stu-id="cf75d-124">Remove a project price list association</span></span>

- <span data-ttu-id="cf75d-125">Vyberte projektový ceník a poté vyberte **Odstranit projektový ceník smlouvy** v podmřížce.</span><span class="sxs-lookup"><span data-stu-id="cf75d-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="cf75d-126">Ceník je odstraněn z projektových ceníků smlouvy.</span><span class="sxs-lookup"><span data-stu-id="cf75d-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="cf75d-127">Samotný ceník nebude smazán.</span><span class="sxs-lookup"><span data-stu-id="cf75d-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="cf75d-128">Bude odstraněno pouze přidružení ke smlouvě.</span><span class="sxs-lookup"><span data-stu-id="cf75d-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="cf75d-129">Nastavení automatických výchozích projektových ceníků smlouvy</span><span class="sxs-lookup"><span data-stu-id="cf75d-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="cf75d-130">Projektový ceník lze nastavit jako výchozí seznam v projektové smlouvě.</span><span class="sxs-lookup"><span data-stu-id="cf75d-130">A project price list can be set up as the default list on a project contract.</span></span> <span data-ttu-id="cf75d-131">Toto nastavení může pomoci zajistit, aby všechny smlouvy ve vaší organizaci vždy začínaly standardním ceníkem pro dané cenové období.</span><span class="sxs-lookup"><span data-stu-id="cf75d-131">This setup can help ensure that all contracts in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="cf75d-132">Nastavení výchozí organizace pro projektové ceníky</span><span class="sxs-lookup"><span data-stu-id="cf75d-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="cf75d-133">Přejděte na **Nastavení** > **Obecné** a poté vyberte **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="cf75d-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="cf75d-134">V seznamu **Aktivní parametry** vyberte záznam a poklepáním jej otevřete.</span><span class="sxs-lookup"><span data-stu-id="cf75d-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="cf75d-135">Při poklepání se ujistěte, že neklikáte na hodnotu pole, které je hypertextovým odkazem.</span><span class="sxs-lookup"><span data-stu-id="cf75d-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="cf75d-136">Na stránce **Aktivní parametry** vyberte kartu **Ceník**. Podmřížka zobrazuje seznam výchozích ceníků.</span><span class="sxs-lookup"><span data-stu-id="cf75d-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="cf75d-137">Toto je seznam standardních nákladových a prodejních ceníků.</span><span class="sxs-lookup"><span data-stu-id="cf75d-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="cf75d-138">Pokud zde máte ceník **Prodej** přidružen ke každé měně, ve které prodáváte, máte zajištěno, že prodejní ceník je výchozí u jakékoli smlouvy, kterou vytvoříte pro zákazníky, kteří obchodují v této měně.</span><span class="sxs-lookup"><span data-stu-id="cf75d-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="cf75d-139">Nastavení projektového ceníku pro konkrétního zákazníka</span><span class="sxs-lookup"><span data-stu-id="cf75d-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="cf75d-140">Pokud jste se svými zákazníky sjednali hlavní cenovou smlouvu, můžete také nastavit projektové ceníky pro konkrétního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="cf75d-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="cf75d-141">Přejděte na **Prodej** > **Zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="cf75d-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="cf75d-142">Ze seznamu aktivních obchodních vztahů vyberte zákazníka, pro kterého máte speciální ceník.</span><span class="sxs-lookup"><span data-stu-id="cf75d-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="cf75d-143">Výběrem záznamu zákazníka jej otevřete a vyberte kartu **Projektové ceníky**. Podmřížka obsahuje seznam projektových ceníků pro tohoto konkrétního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="cf75d-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="cf75d-144">Vytvořte zde nové přidružení ceníku, abyste měli projektový ceník pro tohoto konkrétního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="cf75d-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="cf75d-145">Vlastní ceny v projektové smlouvě</span><span class="sxs-lookup"><span data-stu-id="cf75d-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="cf75d-146">Poté, co vytvoříte výchozí projektové ceníky pro konkrétního zákazníka, budou projektové smlouvy automaticky vytvořeny s těmito přidruženými projektovými ceníky.</span><span class="sxs-lookup"><span data-stu-id="cf75d-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="cf75d-147">Projektové ceníky se však vždy kopírují s připojeným datem a názvem smlouvy.</span><span class="sxs-lookup"><span data-stu-id="cf75d-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="cf75d-148">Manažeři obchodních vztahů a projektoví manažeři pak mohou na těchto kopiích začít provádět úpravy cen.</span><span class="sxs-lookup"><span data-stu-id="cf75d-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="cf75d-149">Tyto změněné ceny se budou vztahovat pouze na tuto projektovou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="cf75d-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]