---
title: Přehled cenových dimenzí
description: Toto téma obsahuje informace o cenových dimenzích v Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128455"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="585cd-103">Přehled cenových dimenzí</span><span class="sxs-lookup"><span data-stu-id="585cd-103">Pricing dimensions overview</span></span>

<span data-ttu-id="585cd-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="585cd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="585cd-105">Dimenze používané v lidských zdrojích k nastavení cen a nákladů spadají do dvou kategorií:</span><span class="sxs-lookup"><span data-stu-id="585cd-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="585cd-106">Lidé</span><span class="sxs-lookup"><span data-stu-id="585cd-106">People</span></span>
- <span data-ttu-id="585cd-107">Naplánovaná práce</span><span class="sxs-lookup"><span data-stu-id="585cd-107">Planned work</span></span>

<span data-ttu-id="585cd-108">Z tohoto důvodu jsou k dispozici dva typy hodnot cenové dimenze:</span><span class="sxs-lookup"><span data-stu-id="585cd-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="585cd-109">**Sady možností**: Dimenze, které jsou pevnými výčty pro sadu hodnot.</span><span class="sxs-lookup"><span data-stu-id="585cd-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="585cd-110">**Hodnoty založené na entitě**: Dimenze, které mohou být různé sady hodnot.</span><span class="sxs-lookup"><span data-stu-id="585cd-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="585cd-111">Cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="585cd-111">Pricing dimensions</span></span>

<span data-ttu-id="585cd-112">Dynamics 365 Project Operations se dodává s výchozí sadou cenových dimenzí.</span><span class="sxs-lookup"><span data-stu-id="585cd-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="585cd-113">Tyto cenové dimenze můžete zobrazit přechodem na **Project Operations** > **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="585cd-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="585cd-114">V záznamu parametru na kartě **Cenové dimenze založené na částce** ověřte, že role **msdyn_resourcecategory** a organizační jednotka zdroje **msdyn_organizationalunit** mají pole **Použitelné pro prodej** a **Použitelné pro náklady** nastavená na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="585cd-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="585cd-115">Když jsou tato pole povolena, můžete nastavit cenu a náklady pro každou kombinaci role a organizační jednotky.</span><span class="sxs-lookup"><span data-stu-id="585cd-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="585cd-116">Potřebujete-li své zdroje ocenit nebo vyjádřit náklady na ně pomocí dalších atributů, můžete vytvořit přizpůsobená pole, entity a dimenze.</span><span class="sxs-lookup"><span data-stu-id="585cd-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="585cd-117">Ocenění času lidského zdroje</span><span class="sxs-lookup"><span data-stu-id="585cd-117">Pricing human resource time</span></span>
<span data-ttu-id="585cd-118">Způsob, jakým organizace oceňuje čas lidského zdroje, je často důležitým strategickým aspektem, který přímo ovlivňuje ziskovost organizace.</span><span class="sxs-lookup"><span data-stu-id="585cd-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="585cd-119">V případě, že vaše organizace je připravena určit, jakým způsobem chce vytvořit sazby fakturace a nákladové sazby pro čas lidského zdroje, pracujte s finančními týmy a vedoucími praxe.</span><span class="sxs-lookup"><span data-stu-id="585cd-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="585cd-120">Další úvahy týkající se tvorby cen zahrnují to, zda se mají znovu použít pole nebo entity, které aktuálně nejsou cenovými dimenzemi, ale které se použijí jako cenové dimenze pro vaši organizaci.</span><span class="sxs-lookup"><span data-stu-id="585cd-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="585cd-121">Pole jako **Kategorie transakce** (**msdyn_transactioncategory**) a **Rezervovatelný zdroj** (**bookableresource**) jsou příklady kandidátských dimenzí.</span><span class="sxs-lookup"><span data-stu-id="585cd-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="585cd-122">Zvažte, zda by vaší cenovou dimenzí měla být tabulka nebo sada možností.</span><span class="sxs-lookup"><span data-stu-id="585cd-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="585cd-123">Pokud předvídáte změny hodnot dimenze, které budou vyšší než 10 nebo 12, a potřebujete pro tyto hodnoty další atributy, mohli byste vytvořit spíše entitu než sadu možností.</span><span class="sxs-lookup"><span data-stu-id="585cd-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="585cd-124">Správa sada možností, jako např. přidání nebo odebrání hodnot, vyžaduje správce nebo vývojáře, zatímco přidání nových řádků do tabulky může provádět většina uživatelů.</span><span class="sxs-lookup"><span data-stu-id="585cd-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="585cd-125">Následující příklad zobrazuje sazby fakturace, nastavené na základě role a organizační jednotce zdroje, ke které zdroj patří.</span><span class="sxs-lookup"><span data-stu-id="585cd-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="585cd-126">Nákladové sazby jsou obvykle založeny na mzdovém pásmu zaměstnance a organizační jednotky, do které patří.</span><span class="sxs-lookup"><span data-stu-id="585cd-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="585cd-127">V tomto příkladu budou tabulky fakturačnícch sazeb a nákladových sazeb vypadat následovně.</span><span class="sxs-lookup"><span data-stu-id="585cd-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="585cd-128">**Ukázkové fakturační sazby**</span><span class="sxs-lookup"><span data-stu-id="585cd-128">**Sample bill rates**</span></span>

| <span data-ttu-id="585cd-129">Role</span><span class="sxs-lookup"><span data-stu-id="585cd-129">Role</span></span>        | <span data-ttu-id="585cd-130">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="585cd-130">Org Unit</span></span>    |<span data-ttu-id="585cd-131">Jednotka</span><span class="sxs-lookup"><span data-stu-id="585cd-131">Unit</span></span>      |<span data-ttu-id="585cd-132">Cena</span><span class="sxs-lookup"><span data-stu-id="585cd-132">Price</span></span>      |<span data-ttu-id="585cd-133">Měna</span><span class="sxs-lookup"><span data-stu-id="585cd-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="585cd-134">Vývojář</span><span class="sxs-lookup"><span data-stu-id="585cd-134">Developer</span></span>   | <span data-ttu-id="585cd-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="585cd-135">Contoso US</span></span>  |<span data-ttu-id="585cd-136">Hour</span><span class="sxs-lookup"><span data-stu-id="585cd-136">Hour</span></span> | <span data-ttu-id="585cd-137">200</span><span class="sxs-lookup"><span data-stu-id="585cd-137">200</span></span>|<span data-ttu-id="585cd-138">USD</span><span class="sxs-lookup"><span data-stu-id="585cd-138">USD</span></span>     |
| <span data-ttu-id="585cd-139">Vývojář</span><span class="sxs-lookup"><span data-stu-id="585cd-139">Developer</span></span>   | <span data-ttu-id="585cd-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="585cd-140">Contoso India</span></span> |<span data-ttu-id="585cd-141">Hour</span><span class="sxs-lookup"><span data-stu-id="585cd-141">Hour</span></span>|   <span data-ttu-id="585cd-142">112</span><span class="sxs-lookup"><span data-stu-id="585cd-142">112</span></span>|<span data-ttu-id="585cd-143">USD</span><span class="sxs-lookup"><span data-stu-id="585cd-143">USD</span></span>     |


<span data-ttu-id="585cd-144">**Příklad nákladových sazeb**</span><span class="sxs-lookup"><span data-stu-id="585cd-144">**Sample cost rates**</span></span>

| <span data-ttu-id="585cd-145">Mzdové pásmo</span><span class="sxs-lookup"><span data-stu-id="585cd-145">Salary Band</span></span>     | <span data-ttu-id="585cd-146">Organizační jednotka</span><span class="sxs-lookup"><span data-stu-id="585cd-146">Org Unit</span></span>    |<span data-ttu-id="585cd-147">Jednotka</span><span class="sxs-lookup"><span data-stu-id="585cd-147">Unit</span></span>      |<span data-ttu-id="585cd-148">Cena</span><span class="sxs-lookup"><span data-stu-id="585cd-148">Price</span></span>      |<span data-ttu-id="585cd-149">Měna</span><span class="sxs-lookup"><span data-stu-id="585cd-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="585cd-150">Moje company_Band1</span><span class="sxs-lookup"><span data-stu-id="585cd-150">My company_Band1</span></span> | <span data-ttu-id="585cd-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="585cd-151">Contoso US</span></span>  |<span data-ttu-id="585cd-152">Hour</span><span class="sxs-lookup"><span data-stu-id="585cd-152">Hour</span></span> | <span data-ttu-id="585cd-153">145</span><span class="sxs-lookup"><span data-stu-id="585cd-153">145</span></span>|<span data-ttu-id="585cd-154">USD</span><span class="sxs-lookup"><span data-stu-id="585cd-154">USD</span></span>     |
| <span data-ttu-id="585cd-155">Moje company_Band2</span><span class="sxs-lookup"><span data-stu-id="585cd-155">My company_Band2</span></span> | <span data-ttu-id="585cd-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="585cd-156">Contoso India</span></span> |<span data-ttu-id="585cd-157">Hour</span><span class="sxs-lookup"><span data-stu-id="585cd-157">Hour</span></span>|   <span data-ttu-id="585cd-158">67</span><span class="sxs-lookup"><span data-stu-id="585cd-158">67</span></span>|<span data-ttu-id="585cd-159">USD</span><span class="sxs-lookup"><span data-stu-id="585cd-159">USD</span></span>     |
