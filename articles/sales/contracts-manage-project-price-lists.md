---
title: Správa projektových ceníků ve smlouvách projektů
description: Tohle téma poskytuje informace o správě projektových ceníků u projektových smluv.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3313eef74b5e7a0624b32d2a336cd986dfdda839
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010373"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="da724-103">Správa projektových ceníků ve smlouvách projektů</span><span class="sxs-lookup"><span data-stu-id="da724-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="da724-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="da724-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="da724-105">Projektové smlouvy v Dynamics 365 Project Operations jsou navrženy tak, aby podporovaly vícedenní efektivní prodejní ceníky pro smlouvy.</span><span class="sxs-lookup"><span data-stu-id="da724-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="da724-106">V Project Operations existuje nová přidružená entita s názvem **Projektové ceníky**.</span><span class="sxs-lookup"><span data-stu-id="da724-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="da724-107">Tato entita má vztah 1:N k projektové smlouvě.</span><span class="sxs-lookup"><span data-stu-id="da724-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="da724-108">Ceníky projektu se používají k oceňování časových, materiálových a výdajových transakcí na projektu.</span><span class="sxs-lookup"><span data-stu-id="da724-108">Project price lists are used to price time, material, and expense transactions on a project.</span></span> <span data-ttu-id="da724-109">Pokud má smlouva jeden nebo více ceníků projektu, tyto ceníky se používají k ocenění ceny za čas, materiálu, odhadů výdajů a skutečné hodnoty u projektů, které jsou spojeny se smlouvou prostřednictvím řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="da724-109">When a contract has one or more project price lists, these price lists are used to price for time, material, expense estimates, and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="da724-110">Pokud ve smlouvě o projektu nejsou žádné ceníky projektu, zobrazí se varovná zpráva, že neexistují žádné ceníky projektu a vaše odhady, skutečná práce na projektu, materiál a zaznamenané náklady nebudou oceněny.</span><span class="sxs-lookup"><span data-stu-id="da724-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, material, and expenses logged will not be priced.</span></span> <span data-ttu-id="da724-111">Za prodejní hodnoty nebude žádná cena.</span><span class="sxs-lookup"><span data-stu-id="da724-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="da724-112">Přidružení nebo zrušení přidružení projektového ceníku k projektové smlouvě</span><span class="sxs-lookup"><span data-stu-id="da724-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a><span data-ttu-id="da724-113">Vytvořte nebo přiřaďte konkrétní ceník pro odhad projektové práce, materiálu a nákladů</span><span class="sxs-lookup"><span data-stu-id="da724-113">Create or associate a specific price list for estimating project-based work, material, and expenses</span></span>

1. <span data-ttu-id="da724-114">Na projektové smlouvě vyberte kartu **Projektové ceníky**.</span><span class="sxs-lookup"><span data-stu-id="da724-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="da724-115">V podmřížce vyberte **+ Přidat nový projektový ceník**.</span><span class="sxs-lookup"><span data-stu-id="da724-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="da724-116">Na posuvníku **Rychlé vytvoření** vyberte ceník.</span><span class="sxs-lookup"><span data-stu-id="da724-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="da724-117">Rozevírací seznam zobrazuje všechny ceníky, které mají nastaven kontext na **Prodej**, kde se měna ceníku shoduje s měnou smlouvy.</span><span class="sxs-lookup"><span data-stu-id="da724-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="da724-118">Zadejte popis přidružení projektového ceníku, vyberte **Uložit** a poté zavřete posuvník **Rychlé vytvoření**.</span><span class="sxs-lookup"><span data-stu-id="da724-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="da724-119">Vytvoří se přidružení projektového ceníku.</span><span class="sxs-lookup"><span data-stu-id="da724-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="da724-120">Opakováním kroků 1–4 přiřaďte k projektové smlouvě více než jeden projektový ceník.</span><span class="sxs-lookup"><span data-stu-id="da724-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="da724-121">Více projektových ceníků vytvářejte, pouze pokud máte u každého z přidružených projektových ceníků jiné datum platnosti.</span><span class="sxs-lookup"><span data-stu-id="da724-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="da724-122">Project Operations nepodporuje překrývající se data platnosti projektových ceníků.</span><span class="sxs-lookup"><span data-stu-id="da724-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="da724-123">Pokud existuje více projektových ceníků pro transakci s daným datem, cena této transakce bude implicitně nastavena na nulu.</span><span class="sxs-lookup"><span data-stu-id="da724-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="da724-124">Odebrání přidružení projektového ceníku</span><span class="sxs-lookup"><span data-stu-id="da724-124">Remove a project price list association</span></span>

- <span data-ttu-id="da724-125">Vyberte projektový ceník a poté vyberte **Odstranit projektový ceník smlouvy** v podmřížce.</span><span class="sxs-lookup"><span data-stu-id="da724-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="da724-126">Ceník je odstraněn z projektových ceníků smlouvy.</span><span class="sxs-lookup"><span data-stu-id="da724-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="da724-127">Samotný ceník nebude smazán.</span><span class="sxs-lookup"><span data-stu-id="da724-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="da724-128">Bude odstraněno pouze přidružení ke smlouvě.</span><span class="sxs-lookup"><span data-stu-id="da724-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="da724-129">Nastavení automatických výchozích projektových ceníků smlouvy</span><span class="sxs-lookup"><span data-stu-id="da724-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="da724-130">Ceník projektu lze nastavit jako výchozí ceník projektu.</span><span class="sxs-lookup"><span data-stu-id="da724-130">A project price list can be set up as the default project price list.</span></span> <span data-ttu-id="da724-131">Toto nastavení zajišťuje, že všechny smlouvy ve vaší organizaci vždy začínají standardním ceníkem projektu pro dané cenové období.</span><span class="sxs-lookup"><span data-stu-id="da724-131">This setup ensures that all contracts in your organization always start with a standard project price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="da724-132">Nastavení výchozí organizace pro projektové ceníky</span><span class="sxs-lookup"><span data-stu-id="da724-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="da724-133">Přejděte na **Nastavení** > **Obecné** a poté vyberte **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="da724-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="da724-134">V seznamu **Aktivní parametry** vyberte záznam a poklepáním jej otevřete.</span><span class="sxs-lookup"><span data-stu-id="da724-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="da724-135">Při poklepání se ujistěte, že neklikáte na hodnotu pole, které je hypertextovým odkazem.</span><span class="sxs-lookup"><span data-stu-id="da724-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="da724-136">Na stránce **Aktivní parametry** vyberte kartu **Ceník**. Podmřížka zobrazuje seznam výchozích ceníků.</span><span class="sxs-lookup"><span data-stu-id="da724-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="da724-137">Toto je seznam standardních nákladových a prodejních ceníků.</span><span class="sxs-lookup"><span data-stu-id="da724-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="da724-138">Pokud zde máte ceník **Prodej** přidružen ke každé měně, ve které prodáváte, máte zajištěno, že prodejní ceník je výchozí u jakékoli smlouvy, kterou vytvoříte pro zákazníky, kteří obchodují v této měně.</span><span class="sxs-lookup"><span data-stu-id="da724-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="da724-139">Nastavení projektového ceníku pro konkrétního zákazníka</span><span class="sxs-lookup"><span data-stu-id="da724-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="da724-140">Pokud jste se svými zákazníky sjednali hlavní cenovou smlouvu, můžete také nastavit projektové ceníky pro konkrétního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="da724-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="da724-141">Přejděte na **Prodej** > **Zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="da724-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="da724-142">Ze seznamu aktivních obchodních vztahů vyberte zákazníka, pro kterého máte speciální ceník.</span><span class="sxs-lookup"><span data-stu-id="da724-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="da724-143">Výběrem záznamu zákazníka jej otevřete a vyberte kartu **Projektové ceníky**. Podmřížka obsahuje seznam projektových ceníků pro tohoto konkrétního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="da724-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="da724-144">Vytvořte zde nové přidružení ceníku, abyste měli projektový ceník pro tohoto konkrétního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="da724-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="da724-145">Vlastní ceny v projektové smlouvě</span><span class="sxs-lookup"><span data-stu-id="da724-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="da724-146">Poté, co vytvoříte výchozí projektové ceníky pro konkrétního zákazníka, budou projektové smlouvy automaticky vytvořeny s těmito přidruženými projektovými ceníky.</span><span class="sxs-lookup"><span data-stu-id="da724-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="da724-147">Projektové ceníky se však vždy kopírují s připojeným datem a názvem smlouvy.</span><span class="sxs-lookup"><span data-stu-id="da724-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="da724-148">Manažeři obchodních vztahů a projektoví manažeři pak mohou na těchto kopiích začít provádět úpravy cen.</span><span class="sxs-lookup"><span data-stu-id="da724-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="da724-149">Tyto změněné ceny se budou vztahovat pouze na tuto projektovou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="da724-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
