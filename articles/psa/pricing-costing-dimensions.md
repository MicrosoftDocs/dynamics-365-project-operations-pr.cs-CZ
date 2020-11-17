---
title: Domovská stránka cenových a nákladových dimenzí
description: Toto téma obsahuje přehled cenových dimenzí.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 515a2e2e518614884b414ca43702e8bfea2c6919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073821"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="cc5f1-103">Domovská stránka cenových a nákladových dimenzí</span><span class="sxs-lookup"><span data-stu-id="cc5f1-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="cc5f1-104">Dimenze používané k nastavení cen práce a nákladů v projektových organizacích jsou ovlivněny následujícími atributy:</span><span class="sxs-lookup"><span data-stu-id="cc5f1-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="cc5f1-105">Lidé dělají práci dle svých zkušeností, rolí nebo geografie.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="cc5f1-106">Práce, která má být provedena dle složitosti nebo denní doby</span><span class="sxs-lookup"><span data-stu-id="cc5f1-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="cc5f1-107">Vzhledem k typické povaze těchto atributů práce a osob vyžadovaných k provedení práce jsou v Project Service Automation k dispozici dva typy hodnot dimenzí cen:</span><span class="sxs-lookup"><span data-stu-id="cc5f1-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="cc5f1-108">**Sady možností** : atributy, které jsou pevnými výčty pro sadu hodnot.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="cc5f1-109">**Hodnoty založené na entitách** - Atributy, které mohou mít různou sadu hodnot, které jsou konečné, ale mohou se časem měnit.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="cc5f1-110">Cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="cc5f1-110">Pricing dimensions</span></span>

<span data-ttu-id="cc5f1-111">PSA se dodává s výchozí sadou cenových dimenzí.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="cc5f1-112">Můžete je zobrazit pomocí **Project Service** > **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="cc5f1-113">V záznamu parametru na kartě **Cenové dimenze založené na částce** ověřte, že role **msdyn_resourcecategory** a organizační jednotka zdroje **msdyn_organizationalunit** mají pole **Použitelné pro prodej** a **Použitelné pro náklady** nastavená na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="cc5f1-114">To vám umožní nastavit cenu a náklady pro každou kombinaci role a organizační jednotky.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Snímek obrazovky parametrů Project Service se zvýrazněním „Použitelné na prodej”](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="cc5f1-116">Pokud jste před verzí 3 PSA jako cenové dimenze používali připravená pole role a organizační jednotky, nezaznamenáte žádné zjistitelné změny.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="cc5f1-117">Službu Project Service můžete nadále používat obvyklým způsobem.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="cc5f1-118">Potřebujete-li své zdroje ocenit nebo vyjádřit náklady na ně pomocí dalších atributů, můžete vytvořit přizpůsobená pole, entity a dimenze.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="cc5f1-119">Další informace naleznete v následujících tématech, ale mějte na vědomí, že je nutné dokončit postupy v uvedeném pořadí:</span><span class="sxs-lookup"><span data-stu-id="cc5f1-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="cc5f1-120">Vytvoření vlastních polí a entit</span><span class="sxs-lookup"><span data-stu-id="cc5f1-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="cc5f1-121">Přidání vlastních polí do nastavení ceny a transakčních entit</span><span class="sxs-lookup"><span data-stu-id="cc5f1-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="cc5f1-122">Nastavení vlastních polí jako cenových dimenzí </span><span class="sxs-lookup"><span data-stu-id="cc5f1-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="cc5f1-123">Aktualizace atributů modulů plug-in tak, aby zahrnovaly nové cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="cc5f1-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="cc5f1-124">Ocenění času lidského zdroje</span><span class="sxs-lookup"><span data-stu-id="cc5f1-124">Pricing human resource time</span></span>
<span data-ttu-id="cc5f1-125">Způsob, jakým organizace oceňuje čas lidského zdroje, je často důležitým strategickým aspektem, který přímo ovlivňuje ziskovost organizace.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="cc5f1-126">V případě, že vaše organizace je připravena určit, jakým způsobem chce vytvořit sazby fakturace a nákladové sazby pro čas lidského zdroje, pracujte s finančními týmy a vedoucími praxe.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="cc5f1-127">Další úvahy týkající se tvorby cen zahrnují to, zda se mají znovu použít pole nebo entity, které aktuálně nejsou cenovými dimenzemi, ale které se použijí jako cenové dimenze pro vaši organizaci.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="cc5f1-128">Pole jako **Kategorie transakce** ( **msdyn_transactioncategory** ) a **Rezervovatelný zdroj** ( **bookableresource** ) jsou příklady kandidátských dimenzí.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-128">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="cc5f1-129">Zvažte, zda by vaší cenovou dimenzí měla být tabulka nebo sada možností.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="cc5f1-130">Pokud předvídáte změny hodnot dimenze, které budou vyšší než 10 nebo 12, a potřebujete pro tyto hodnoty další atributy, vytvořte spíše entitu než sadu možností.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="cc5f1-131">Správa sada možností, jako např. přidání nebo odebrání hodnot, vyžaduje správce nebo vývojáře, zatímco přidání nových řádků do tabulky může provádět většina obchodních uživatelů.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="cc5f1-132">Následující příklad zobrazuje sazby fakturace, nastavené na základě role a organizační jednotce zdroje, ke které zdroj patří.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="cc5f1-133">Nákladové sazby jsou obvykle založeny na mzdovém pásmu zaměstnance a organizační jednotky, do které patří.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="cc5f1-134">V tomto příkladu budou tabulky fakturačnícch sazeb a nákladových sazeb vypadat následovně.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="cc5f1-135">**Ukázkové fakturační sazby**</span><span class="sxs-lookup"><span data-stu-id="cc5f1-135">**Sample bill rates**</span></span>

| <span data-ttu-id="cc5f1-136">Role</span><span class="sxs-lookup"><span data-stu-id="cc5f1-136">Role</span></span>        | <span data-ttu-id="cc5f1-137">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="cc5f1-137">Org Unit</span></span>    |<span data-ttu-id="cc5f1-138">Jednotka</span><span class="sxs-lookup"><span data-stu-id="cc5f1-138">Unit</span></span>      |<span data-ttu-id="cc5f1-139">Cena</span><span class="sxs-lookup"><span data-stu-id="cc5f1-139">Price</span></span>      |<span data-ttu-id="cc5f1-140">Měna</span><span class="sxs-lookup"><span data-stu-id="cc5f1-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="cc5f1-141">Vývojář</span><span class="sxs-lookup"><span data-stu-id="cc5f1-141">Developer</span></span>   | <span data-ttu-id="cc5f1-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="cc5f1-142">Contoso US</span></span>  |<span data-ttu-id="cc5f1-143">Hour</span><span class="sxs-lookup"><span data-stu-id="cc5f1-143">Hour</span></span> | <span data-ttu-id="cc5f1-144">200</span><span class="sxs-lookup"><span data-stu-id="cc5f1-144">200</span></span>|<span data-ttu-id="cc5f1-145">USD</span><span class="sxs-lookup"><span data-stu-id="cc5f1-145">USD</span></span>     |
| <span data-ttu-id="cc5f1-146">Vývojář</span><span class="sxs-lookup"><span data-stu-id="cc5f1-146">Developer</span></span>   | <span data-ttu-id="cc5f1-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="cc5f1-147">Contoso India</span></span> |<span data-ttu-id="cc5f1-148">Hour</span><span class="sxs-lookup"><span data-stu-id="cc5f1-148">Hour</span></span>|   <span data-ttu-id="cc5f1-149">112</span><span class="sxs-lookup"><span data-stu-id="cc5f1-149">112</span></span>|<span data-ttu-id="cc5f1-150">USD</span><span class="sxs-lookup"><span data-stu-id="cc5f1-150">USD</span></span>     |


<span data-ttu-id="cc5f1-151">**Příklad nákladových sazeb**</span><span class="sxs-lookup"><span data-stu-id="cc5f1-151">**Sample cost rates**</span></span>

| <span data-ttu-id="cc5f1-152">Mzdové pásmo</span><span class="sxs-lookup"><span data-stu-id="cc5f1-152">Salary Band</span></span>     | <span data-ttu-id="cc5f1-153">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="cc5f1-153">Org Unit</span></span>    |<span data-ttu-id="cc5f1-154">Jednotka</span><span class="sxs-lookup"><span data-stu-id="cc5f1-154">Unit</span></span>      |<span data-ttu-id="cc5f1-155">Cena</span><span class="sxs-lookup"><span data-stu-id="cc5f1-155">Price</span></span>      |<span data-ttu-id="cc5f1-156">Měna</span><span class="sxs-lookup"><span data-stu-id="cc5f1-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="cc5f1-157">Moje company_Band1</span><span class="sxs-lookup"><span data-stu-id="cc5f1-157">My company_Band1</span></span> | <span data-ttu-id="cc5f1-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="cc5f1-158">Contoso US</span></span>  |<span data-ttu-id="cc5f1-159">Hour</span><span class="sxs-lookup"><span data-stu-id="cc5f1-159">Hour</span></span> | <span data-ttu-id="cc5f1-160">145</span><span class="sxs-lookup"><span data-stu-id="cc5f1-160">145</span></span>|<span data-ttu-id="cc5f1-161">USD</span><span class="sxs-lookup"><span data-stu-id="cc5f1-161">USD</span></span>     |
| <span data-ttu-id="cc5f1-162">Moje company_Band2</span><span class="sxs-lookup"><span data-stu-id="cc5f1-162">My company_Band2</span></span> | <span data-ttu-id="cc5f1-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="cc5f1-163">Contoso India</span></span> |<span data-ttu-id="cc5f1-164">Hour</span><span class="sxs-lookup"><span data-stu-id="cc5f1-164">Hour</span></span>|   <span data-ttu-id="cc5f1-165">67</span><span class="sxs-lookup"><span data-stu-id="cc5f1-165">67</span></span>|<span data-ttu-id="cc5f1-166">USD</span><span class="sxs-lookup"><span data-stu-id="cc5f1-166">USD</span></span>     |