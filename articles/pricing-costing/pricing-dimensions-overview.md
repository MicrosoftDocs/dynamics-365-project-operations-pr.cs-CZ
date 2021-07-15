---
title: Přehled cenových dimenzí
description: Toto téma obsahuje informace o nastavení cenových dimenzí v Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: e8d62dcf9975e5427926210a881dec2c256f1b8b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368468"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="f3fbb-103">Přehled cenových dimenzí</span><span class="sxs-lookup"><span data-stu-id="f3fbb-103">Pricing dimensions overview</span></span>

<span data-ttu-id="f3fbb-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="f3fbb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f3fbb-105">Dimenze používané v lidských zdrojích k nastavení cen a nákladů spadají do dvou kategorií:</span><span class="sxs-lookup"><span data-stu-id="f3fbb-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="f3fbb-106">Lidé</span><span class="sxs-lookup"><span data-stu-id="f3fbb-106">People</span></span>
- <span data-ttu-id="f3fbb-107">Naplánovaná práce</span><span class="sxs-lookup"><span data-stu-id="f3fbb-107">Planned work</span></span>

<span data-ttu-id="f3fbb-108">Z tohoto důvodu jsou k dispozici dva typy hodnot cenové dimenze:</span><span class="sxs-lookup"><span data-stu-id="f3fbb-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="f3fbb-109">**Sady možností**: Dimenze, které jsou pevnými výčty pro sadu hodnot.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="f3fbb-110">**Hodnoty založené na entitě**: Dimenze, které mohou být různé sady hodnot.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="f3fbb-111">Cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="f3fbb-111">Pricing dimensions</span></span>

<span data-ttu-id="f3fbb-112">Dynamics 365 Project Operations se dodává s výchozí sadou cenových dimenzí.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="f3fbb-113">Tyto cenové dimenze můžete zobrazit přechodem na **Project Operations** > **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="f3fbb-114">V záznamu parametru na kartě **Cenové dimenze založené na částce** ověřte, že role **msdyn_resourcecategory** a organizační jednotka zdroje **msdyn_organizationalunit** mají pole **Použitelné pro prodej** a **Použitelné pro náklady** nastavená na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="f3fbb-115">Když jsou tato pole povolena, můžete nastavit cenu a náklady pro každou kombinaci role a organizační jednotky.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

![Snímek obrazovky parametrů Project Service se zvýrazněním „Použitelné na prodej”](media/PS-OOB-parameters.png)

<span data-ttu-id="f3fbb-117">Potřebujete-li své zdroje ocenit nebo vyjádřit náklady na ně pomocí dalších atributů, můžete vytvořit přizpůsobená pole, entity a dimenze.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-117">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="f3fbb-118">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="f3fbb-118">For more information, see the following topics.</span></span> 
  
  > [!NOTE]
  > <span data-ttu-id="f3fbb-119">Postupy musí být dokončeny v pořadí, v jakém jsou uvedeny.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-119">The procedures must be completed in the order they are listed.</span></span>

1. [<span data-ttu-id="f3fbb-120">Vytvoření řešení pro vlastní cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="f3fbb-120">Create a solution for custom pricing dimensions</span></span>](../sales/create-solution-custompd.md)
2. [<span data-ttu-id="f3fbb-121">Vytvoření vlastních polí a entit</span><span class="sxs-lookup"><span data-stu-id="f3fbb-121">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md)
3. [<span data-ttu-id="f3fbb-122">Přidání vlastních polí do nastavení ceny a transakčních entit </span><span class="sxs-lookup"><span data-stu-id="f3fbb-122">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
4. [<span data-ttu-id="f3fbb-123">Nastavení vlastních polí jako cenových dimenzí </span><span class="sxs-lookup"><span data-stu-id="f3fbb-123">Set up custom fields as pricing dimensions</span></span>](set-up-custom-fields-pricing-dimensions.md)
5. [<span data-ttu-id="f3fbb-124">Aktualizace atributů modulů plug-in tak, aby zahrnovaly nové cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="f3fbb-124">Update plug-in attributes to include new pricing dimensions</span></span>](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a><span data-ttu-id="f3fbb-125">Ocenění času lidského zdroje</span><span class="sxs-lookup"><span data-stu-id="f3fbb-125">Pricing human resource time</span></span>
<span data-ttu-id="f3fbb-126">Způsob, jakým organizace oceňuje čas lidského zdroje, je často důležitým strategickým aspektem, který přímo ovlivňuje ziskovost organizace.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-126">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="f3fbb-127">V případě, že vaše organizace je připravena určit, jakým způsobem chce vytvořit sazby fakturace a nákladové sazby pro čas lidského zdroje, pracujte s finančními týmy a vedoucími praxe.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-127">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="f3fbb-128">Další úvahy týkající se tvorby cen zahrnují to, zda se mají znovu použít pole nebo entity, které aktuálně nejsou cenovými dimenzemi, ale které se použijí jako cenové dimenze pro vaši organizaci.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-128">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="f3fbb-129">Pole jako **Kategorie transakce** (**msdyn_transactioncategory**) a **Rezervovatelný zdroj** (**bookableresource**) jsou příklady kandidátských dimenzí.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-129">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="f3fbb-130">Zvažte, zda by vaší cenovou dimenzí měla být tabulka nebo sada možností.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-130">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="f3fbb-131">Pokud předvídáte změny hodnot dimenze, které budou vyšší než 10 nebo 12, a potřebujete pro tyto hodnoty další atributy, mohli byste vytvořit spíše entitu než sadu možností.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-131">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="f3fbb-132">Správa sada možností, jako např. přidání nebo odebrání hodnot, vyžaduje správce nebo vývojáře, zatímco přidání nových řádků do tabulky může provádět většina uživatelů.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-132">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="f3fbb-133">Následující příklad zobrazuje sazby fakturace, nastavené na základě role a organizační jednotce zdroje, ke které zdroj patří.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-133">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="f3fbb-134">Nákladové sazby jsou obvykle založeny na mzdovém pásmu zaměstnance a organizační jednotky, do které patří.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-134">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="f3fbb-135">V tomto příkladu budou tabulky fakturačnícch sazeb a nákladových sazeb vypadat následovně.</span><span class="sxs-lookup"><span data-stu-id="f3fbb-135">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="f3fbb-136">**Ukázkové fakturační sazby**</span><span class="sxs-lookup"><span data-stu-id="f3fbb-136">**Sample bill rates**</span></span>

| <span data-ttu-id="f3fbb-137">Role</span><span class="sxs-lookup"><span data-stu-id="f3fbb-137">Role</span></span>        | <span data-ttu-id="f3fbb-138">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="f3fbb-138">Org Unit</span></span>    |<span data-ttu-id="f3fbb-139">Jednotka</span><span class="sxs-lookup"><span data-stu-id="f3fbb-139">Unit</span></span>      |<span data-ttu-id="f3fbb-140">Cena</span><span class="sxs-lookup"><span data-stu-id="f3fbb-140">Price</span></span>      |<span data-ttu-id="f3fbb-141">Měna</span><span class="sxs-lookup"><span data-stu-id="f3fbb-141">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f3fbb-142">Vývojář</span><span class="sxs-lookup"><span data-stu-id="f3fbb-142">Developer</span></span>   | <span data-ttu-id="f3fbb-143">Contoso (USA)</span><span class="sxs-lookup"><span data-stu-id="f3fbb-143">Contoso US</span></span>  |<span data-ttu-id="f3fbb-144">hod</span><span class="sxs-lookup"><span data-stu-id="f3fbb-144">Hour</span></span> | <span data-ttu-id="f3fbb-145">200</span><span class="sxs-lookup"><span data-stu-id="f3fbb-145">200</span></span>|<span data-ttu-id="f3fbb-146">USD</span><span class="sxs-lookup"><span data-stu-id="f3fbb-146">USD</span></span>     |
| <span data-ttu-id="f3fbb-147">Vývojář</span><span class="sxs-lookup"><span data-stu-id="f3fbb-147">Developer</span></span>   | <span data-ttu-id="f3fbb-148">Contoso India</span><span class="sxs-lookup"><span data-stu-id="f3fbb-148">Contoso India</span></span> |<span data-ttu-id="f3fbb-149">hod</span><span class="sxs-lookup"><span data-stu-id="f3fbb-149">Hour</span></span>|   <span data-ttu-id="f3fbb-150">112</span><span class="sxs-lookup"><span data-stu-id="f3fbb-150">112</span></span>|<span data-ttu-id="f3fbb-151">USD</span><span class="sxs-lookup"><span data-stu-id="f3fbb-151">USD</span></span>     |


<span data-ttu-id="f3fbb-152">**Příklad nákladových sazeb**</span><span class="sxs-lookup"><span data-stu-id="f3fbb-152">**Sample cost rates**</span></span>

| <span data-ttu-id="f3fbb-153">Mzdové pásmo</span><span class="sxs-lookup"><span data-stu-id="f3fbb-153">Salary Band</span></span>     | <span data-ttu-id="f3fbb-154">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="f3fbb-154">Org Unit</span></span>    |<span data-ttu-id="f3fbb-155">Jednotka</span><span class="sxs-lookup"><span data-stu-id="f3fbb-155">Unit</span></span>      |<span data-ttu-id="f3fbb-156">Cena</span><span class="sxs-lookup"><span data-stu-id="f3fbb-156">Price</span></span>      |<span data-ttu-id="f3fbb-157">Měna</span><span class="sxs-lookup"><span data-stu-id="f3fbb-157">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f3fbb-158">Moje company_Band1</span><span class="sxs-lookup"><span data-stu-id="f3fbb-158">My company_Band1</span></span> | <span data-ttu-id="f3fbb-159">Contoso (USA)</span><span class="sxs-lookup"><span data-stu-id="f3fbb-159">Contoso US</span></span>  |<span data-ttu-id="f3fbb-160">hod</span><span class="sxs-lookup"><span data-stu-id="f3fbb-160">Hour</span></span> | <span data-ttu-id="f3fbb-161">145</span><span class="sxs-lookup"><span data-stu-id="f3fbb-161">145</span></span>|<span data-ttu-id="f3fbb-162">USD</span><span class="sxs-lookup"><span data-stu-id="f3fbb-162">USD</span></span>     |
| <span data-ttu-id="f3fbb-163">Moje company_Band2</span><span class="sxs-lookup"><span data-stu-id="f3fbb-163">My company_Band2</span></span> | <span data-ttu-id="f3fbb-164">Contoso India</span><span class="sxs-lookup"><span data-stu-id="f3fbb-164">Contoso India</span></span> |<span data-ttu-id="f3fbb-165">hod</span><span class="sxs-lookup"><span data-stu-id="f3fbb-165">Hour</span></span>|   <span data-ttu-id="f3fbb-166">67</span><span class="sxs-lookup"><span data-stu-id="f3fbb-166">67</span></span>|<span data-ttu-id="f3fbb-167">USD</span><span class="sxs-lookup"><span data-stu-id="f3fbb-167">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]