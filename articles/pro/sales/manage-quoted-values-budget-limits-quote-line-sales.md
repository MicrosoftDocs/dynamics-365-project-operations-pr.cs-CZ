---
title: Přehled řádků nabídky založené na projektu
description: Toto téma poskytuje informace o používání řádků nabídek založených na projektu pro práci na projektu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994848"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="36935-103">Přehled řádků nabídky založené na projektu</span><span class="sxs-lookup"><span data-stu-id="36935-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="36935-104">_**Platí pro:** omezené nasazení – dohoda o pro forma fakturaci, Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="36935-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="36935-105">Řádky nabídek založených na projektu jsou navrženy tak, aby pomohly odhadnout projektovou práci na zakázce.</span><span class="sxs-lookup"><span data-stu-id="36935-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="36935-106">Struktura řádku nabídky založené na projektu se rozšiřuje u odhadů projektu o následující koncepty:</span><span class="sxs-lookup"><span data-stu-id="36935-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="36935-107">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="36935-107">Billing Method</span></span>
- <span data-ttu-id="36935-108">Projekt a mapování úkolů</span><span class="sxs-lookup"><span data-stu-id="36935-108">Project and Task Mapping</span></span>
- <span data-ttu-id="36935-109">Zahrnuté třídy transakcí</span><span class="sxs-lookup"><span data-stu-id="36935-109">Included Transaction classes</span></span>
- <span data-ttu-id="36935-110">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="36935-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="36935-111">Nastavení účtovatelnosti</span><span class="sxs-lookup"><span data-stu-id="36935-111">Chargeability setup</span></span>
- <span data-ttu-id="36935-112">Odhad pomocí podrobností řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="36935-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="36935-113">Zákazníci řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="36935-113">Quote line Customers</span></span>

<span data-ttu-id="36935-114">Následující tabulka poskytuje informace o polích na karrtě **Všeobecné** řádku nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="36935-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="36935-115">Tato pole pomáhají připravit základ pro podrobný počáteční odhad projektové práce.</span><span class="sxs-lookup"><span data-stu-id="36935-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="36935-116">**Pole**</span><span class="sxs-lookup"><span data-stu-id="36935-116">**Field**</span></span> | <span data-ttu-id="36935-117">**Popis**</span><span class="sxs-lookup"><span data-stu-id="36935-117">**Description**</span></span> | <span data-ttu-id="36935-118">**Dopad na příjem dat**</span><span class="sxs-lookup"><span data-stu-id="36935-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="36935-119">Jméno</span><span class="sxs-lookup"><span data-stu-id="36935-119">Name</span></span> | <span data-ttu-id="36935-120">Název řádku nabídky, který vám pomůže identifikovat diskrétní složku nabídky, která se odhaduje.</span><span class="sxs-lookup"><span data-stu-id="36935-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="36935-121">Zkopírováno do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="36935-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="36935-122">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="36935-122">Billing Method</span></span> | <span data-ttu-id="36935-123">U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z příslušného pole na řádku příležitosti.</span><span class="sxs-lookup"><span data-stu-id="36935-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="36935-124">Toto pole zahrnuje dva hlavní smluvní modely podporované Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="36935-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="36935-125">- Pevná cena</span><span class="sxs-lookup"><span data-stu-id="36935-125">- Fixed price</span></span></br><span data-ttu-id="36935-126">- Čas a materiál.</span><span class="sxs-lookup"><span data-stu-id="36935-126">- Time and material.</span></span>| <span data-ttu-id="36935-127">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="36935-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="36935-128">Project</span><span class="sxs-lookup"><span data-stu-id="36935-128">Project</span></span> | <span data-ttu-id="36935-129">Pomocí tohoto volitelného pole můžete identifikovat projekt, který bude použit k provedení práce na této zakázce.</span><span class="sxs-lookup"><span data-stu-id="36935-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="36935-130">Když je projekt mapován na řádek nabídky, pomáhá to při nastavení zpoplatněných úkolů a také při stanovení odhadu založeného na projektu do řádku nabídky jako podrobnosti řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="36935-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="36935-131">Pokud projekt není mapován na řádek nabídky založené na projektu, odhad by měl být vytvořen ručně – vytvořením každé podrobnosti řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="36935-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="36935-132">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="36935-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="36935-133">Zahrnuté úkoly</span><span class="sxs-lookup"><span data-stu-id="36935-133">Included Tasks</span></span> | <span data-ttu-id="36935-134">Udává, zda je tento řádek nabídky použit pro všechny nebo jen některé úkoly vybraného projektu.</span><span class="sxs-lookup"><span data-stu-id="36935-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="36935-135">Toto pole může obsahovat následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="36935-135">This field has the following possible values:</span></span></br><span data-ttu-id="36935-136">- Všechny projektové úkoly</span><span class="sxs-lookup"><span data-stu-id="36935-136">- All project tasks</span></span></br><span data-ttu-id="36935-137">- Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="36935-137">- Selected project tasks only</span></span></br><span data-ttu-id="36935-138">Prázdná hodnota v tomto poli odpovídá možnosti **Všechny úkoly projektu**.</span><span class="sxs-lookup"><span data-stu-id="36935-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="36935-139">Když je na stránce projektu vybráno **Pouze vybrané úkoly projektu**, karta **Nastavení fakturace úkolu** umožňuje vybrat konkrétní úkoly a přidružit je k tomuto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="36935-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="36935-140">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="36935-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="36935-141">Zahrnout čas</span><span class="sxs-lookup"><span data-stu-id="36935-141">Include Time</span></span> | <span data-ttu-id="36935-142">Hodnota **Ano**/**Ne** označuje, zda budou do odhadu na tomto řádku nabídky zahrnuty časové transakce nebo náklady práce na vybraném projektu.</span><span class="sxs-lookup"><span data-stu-id="36935-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="36935-143">Hodnota **Ne** určuje, že časové transakce nebo náklady práce nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="36935-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="36935-144">Hodnota **Ano** určuje, že časové transakce nebo náklady práce budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="36935-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="36935-145">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="36935-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="36935-146">Zahrnout výdaj</span><span class="sxs-lookup"><span data-stu-id="36935-146">Include Expense</span></span> | <span data-ttu-id="36935-147">Hodnota **Ano**/**Ne** označuje, zda budou do odhadu na tomto řádku nabídky zahrnuty náklady výdajů na vybraném projektu.</span><span class="sxs-lookup"><span data-stu-id="36935-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="36935-148">Hodnota **Ne** určuje, že výdajové náklady nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="36935-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="36935-149">Hodnota **Ano** určuje, že výdajové náklady budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="36935-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="36935-150">Tato hodnota je překopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="36935-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="36935-151">Zahrnout materiál</span><span class="sxs-lookup"><span data-stu-id="36935-151">Include Material</span></span> | <span data-ttu-id="36935-152">Hodnota **Ano**/**Ne** označuje, zda budou do odhadu na tomto řádku nabídky zahrnuty náklady na materiál na vybraném projektu.</span><span class="sxs-lookup"><span data-stu-id="36935-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="36935-153">Hodnota **Ne** označuje, že nebudou do odhadu na tomto řádku nabídky zahrnuty náklady na materiál.</span><span class="sxs-lookup"><span data-stu-id="36935-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="36935-154">Hodnota **Ano** označuje, že budou do odhadu na tomto řádku nabídky zahrnuty náklady na materiál.</span><span class="sxs-lookup"><span data-stu-id="36935-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="36935-155">Tato hodnota je překopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="36935-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="36935-156">Zahrnout poplatek</span><span class="sxs-lookup"><span data-stu-id="36935-156">Include Fee</span></span> | <span data-ttu-id="36935-157">Hodnota **Ano**/**Ne** označuje, zda budou do odhadu na tomto řádku nabídky zahrnuty poplatky na vybraném projektu.</span><span class="sxs-lookup"><span data-stu-id="36935-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="36935-158">Hodnota **Ne** určuje, že poplatky nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="36935-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="36935-159">Hodnota **Ano** určuje, že poplatky budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="36935-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="36935-160">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="36935-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="36935-161">Nabízená částka</span><span class="sxs-lookup"><span data-stu-id="36935-161">Quoted Amount</span></span> | <span data-ttu-id="36935-162">Jedná se o částku, která bude zákazníkovi nabídnuta za veškerou práci předpovídanou v tomto řádku nabídky projektu.</span><span class="sxs-lookup"><span data-stu-id="36935-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="36935-163">U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z pole **Rozpočet zákazníka** na řádku příležitosti.</span><span class="sxs-lookup"><span data-stu-id="36935-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="36935-164">Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky na podrobnostech řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="36935-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="36935-165">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="36935-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="36935-166">Odhad daně</span><span class="sxs-lookup"><span data-stu-id="36935-166">Estimated Tax</span></span> | <span data-ttu-id="36935-167">Toto je upravitelné pole, kde může uživatel přidat odhadovanou částku daně do řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="36935-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="36935-168">Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky daně na podrobnostech řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="36935-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="36935-169">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="36935-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="36935-170">Nabízená částka včetně daně</span><span class="sxs-lookup"><span data-stu-id="36935-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="36935-171">Toto pole představuje částku nabídky po zdanění a je pouze ke čtení.</span><span class="sxs-lookup"><span data-stu-id="36935-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="36935-172">Částka v tomto poli se počítá jako *Nabízená částka + daň*.</span><span class="sxs-lookup"><span data-stu-id="36935-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="36935-173">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="36935-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="36935-174">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="36935-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="36935-175">Toto pole je upravitelné a je k dispozici pouze na řádcích nabídek založených na projektu, které mají nastaven způsob fakturace **Čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="36935-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="36935-176">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="36935-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="36935-177">Rozpočet zákazníka</span><span class="sxs-lookup"><span data-stu-id="36935-177">Customer Budget</span></span> | <span data-ttu-id="36935-178">Toto pole je upravitelné a jeho hodnota se zkopíruje z příslušného pole na řádku příležitosti, když je nabídka vytvořena z příležitosti.</span><span class="sxs-lookup"><span data-stu-id="36935-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="36935-179">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="36935-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="36935-180">Pravidla ověření pro pole na kartě Všeobecné řádků nabídek založených na projektu</span><span class="sxs-lookup"><span data-stu-id="36935-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="36935-181">**Pravidlo 1** : Pokud je pole **Zahrnuté úkoly** prázdné nebo je-li nastaveno na hodnotu **Všechny úkoly projektu**, je projekt zahrnut do řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="36935-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="36935-182">**Pravidlo 2** : Pokud je pole **Zahrnuté úkoly** prázdné nebo je-li nastaveno na hodnotu **Všechny úkoly projektu**, lze projekt a určitou třídu transakcí zahrnout pouze na jeden řádek nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="36935-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="36935-183">**Pravidlo 3**: Pokud je pole **Zahrnuté úkoly** prázdné nebo je-li nastaveno na hodnotu **Pouze vybrané úkoly projektu**, lze projekt a určitou třídu transakcí zahrnout do více řádků nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="36935-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="36935-184">**Pravidlo 4** : Pokud má příležitost více nabídek, mohou existovat řádky nabídky z různých nabídek, které všechny odkazují na stejný projekt a zahrnují stejnou třídu transakcí.</span><span class="sxs-lookup"><span data-stu-id="36935-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="36935-185">**Pravidlo 5** : Pokud nabídky nepatří ke stejné příležitosti, nemohou zahrnovat stejný projekt a třídu transakcí.</span><span class="sxs-lookup"><span data-stu-id="36935-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="36935-186">
                    <strong>Příležitost</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36935-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="36935-187">
                    <strong>Nabídka</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36935-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="36935-188">
                    <strong>Řádek nabídky</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36935-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="36935-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36935-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="36935-190">
                    <strong>Zahrnuté úkoly</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36935-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="36935-191">
                    <strong>Zahrnout čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36935-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="36935-192">
                    <strong>Zahrnout výdaj</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36935-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="36935-193">
                    <strong>Zahrnout materiál</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36935-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="36935-194">
                    <strong>Zahrnout</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36935-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="36935-195">
                    <strong>Poplatek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36935-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="36935-196">
                    <strong>Platné / Neplatné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36935-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="36935-197">
                    <strong>Důvod</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36935-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="36935-198">P1</span><span class="sxs-lookup"><span data-stu-id="36935-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="36935-199">Č1</span><span class="sxs-lookup"><span data-stu-id="36935-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="36935-200">ŘN1</span><span class="sxs-lookup"><span data-stu-id="36935-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-201">O1</span><span class="sxs-lookup"><span data-stu-id="36935-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="36935-202">prázdnou</span><span class="sxs-lookup"><span data-stu-id="36935-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="36935-203">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="36935-204">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="36935-205">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-206">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36935-207">Neplatný</span><span class="sxs-lookup"><span data-stu-id="36935-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36935-208">Porušení pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="36935-208">Violation of Rule #2.</span></span> <span data-ttu-id="36935-209">Čas, náklady a poplatky za projekt P1 jsou zahrnuty v řádcích nabídky ŘN1 a ŘN2</span><span class="sxs-lookup"><span data-stu-id="36935-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="36935-210">P1</span><span class="sxs-lookup"><span data-stu-id="36935-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="36935-211">Č1</span><span class="sxs-lookup"><span data-stu-id="36935-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="36935-212">ŘN2</span><span class="sxs-lookup"><span data-stu-id="36935-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-213">O1</span><span class="sxs-lookup"><span data-stu-id="36935-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="36935-214">prázdnou</span><span class="sxs-lookup"><span data-stu-id="36935-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="36935-215">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="36935-216">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="36935-217">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-218">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="36935-219">P1</span><span class="sxs-lookup"><span data-stu-id="36935-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="36935-220">Č1</span><span class="sxs-lookup"><span data-stu-id="36935-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="36935-221">ŘN1</span><span class="sxs-lookup"><span data-stu-id="36935-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-222">O1</span><span class="sxs-lookup"><span data-stu-id="36935-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="36935-223">prázdnou</span><span class="sxs-lookup"><span data-stu-id="36935-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="36935-224">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="36935-225">No</span><span class="sxs-lookup"><span data-stu-id="36935-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="36935-226">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-227">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36935-228">Neplatný</span><span class="sxs-lookup"><span data-stu-id="36935-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36935-229">Porušení pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="36935-229">Violation of Rule #2.</span></span> <span data-ttu-id="36935-230">Čas, materiál a poplatky za projekt P1 jsou zahrnuty v řádcích nabídky ŘN1 a ŘN2</span><span class="sxs-lookup"><span data-stu-id="36935-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="36935-231">P1</span><span class="sxs-lookup"><span data-stu-id="36935-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="36935-232">Č1</span><span class="sxs-lookup"><span data-stu-id="36935-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="36935-233">ŘN2</span><span class="sxs-lookup"><span data-stu-id="36935-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-234">O1</span><span class="sxs-lookup"><span data-stu-id="36935-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="36935-235">prázdnou</span><span class="sxs-lookup"><span data-stu-id="36935-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="36935-236">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="36935-237">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="36935-238">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-239">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="36935-240">P1</span><span class="sxs-lookup"><span data-stu-id="36935-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="36935-241">Č1</span><span class="sxs-lookup"><span data-stu-id="36935-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="36935-242">ŘN1</span><span class="sxs-lookup"><span data-stu-id="36935-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-243">O1</span><span class="sxs-lookup"><span data-stu-id="36935-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="36935-244">prázdnou</span><span class="sxs-lookup"><span data-stu-id="36935-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="36935-245">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="36935-246">No</span><span class="sxs-lookup"><span data-stu-id="36935-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="36935-247">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-248">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36935-249">Platné</span><span class="sxs-lookup"><span data-stu-id="36935-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36935-250">Čas, materiál a poplatky za projekt P1 jsou zahrnuty na ŘN1</span><span class="sxs-lookup"><span data-stu-id="36935-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="36935-251">Výdaje na projekt P1 jsou zahrnuty do ŘN2</span><span class="sxs-lookup"><span data-stu-id="36935-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="36935-252">Žádné překrývání toho, co je zahrnuto na každém řádku nabídky, a proto je zadání platné.</span><span class="sxs-lookup"><span data-stu-id="36935-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="36935-253">P1</span><span class="sxs-lookup"><span data-stu-id="36935-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="36935-254">Č1</span><span class="sxs-lookup"><span data-stu-id="36935-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="36935-255">ŘN2</span><span class="sxs-lookup"><span data-stu-id="36935-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-256">O1</span><span class="sxs-lookup"><span data-stu-id="36935-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="36935-257">prázdnou</span><span class="sxs-lookup"><span data-stu-id="36935-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="36935-258">No</span><span class="sxs-lookup"><span data-stu-id="36935-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="36935-259">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="36935-260">No</span><span class="sxs-lookup"><span data-stu-id="36935-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-261">No</span><span class="sxs-lookup"><span data-stu-id="36935-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="36935-262">P1</span><span class="sxs-lookup"><span data-stu-id="36935-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="36935-263">Č1</span><span class="sxs-lookup"><span data-stu-id="36935-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="36935-264">ŘN1</span><span class="sxs-lookup"><span data-stu-id="36935-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-265">O1</span><span class="sxs-lookup"><span data-stu-id="36935-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="36935-266">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="36935-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="36935-267">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="36935-268">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="36935-269">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-270">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36935-271">Neplatný</span><span class="sxs-lookup"><span data-stu-id="36935-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36935-272">Porušení pravidla č. 2</span><span class="sxs-lookup"><span data-stu-id="36935-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="36935-273">S1 zahrnuje čas, materiál, výdaje a poplatky za podmnožinu úkolů v projektu P1</span><span class="sxs-lookup"><span data-stu-id="36935-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="36935-274">ŘN2 zahrnuje čas, výdaje a poplatky za celý projekt P1, a proto se překrývá s tím, co je zahrnuto v S1.</span><span class="sxs-lookup"><span data-stu-id="36935-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="36935-275">P1</span><span class="sxs-lookup"><span data-stu-id="36935-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="36935-276">Č1</span><span class="sxs-lookup"><span data-stu-id="36935-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="36935-277">ŘN2</span><span class="sxs-lookup"><span data-stu-id="36935-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-278">O1</span><span class="sxs-lookup"><span data-stu-id="36935-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="36935-279">prázdnou</span><span class="sxs-lookup"><span data-stu-id="36935-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="36935-280">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="36935-281">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="36935-282">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-283">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="36935-284">P1</span><span class="sxs-lookup"><span data-stu-id="36935-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="36935-285">Č1</span><span class="sxs-lookup"><span data-stu-id="36935-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="36935-286">ŘN1</span><span class="sxs-lookup"><span data-stu-id="36935-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-287">O1</span><span class="sxs-lookup"><span data-stu-id="36935-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="36935-288">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="36935-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="36935-289">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="36935-290">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="36935-291">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-292">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36935-293">Platné</span><span class="sxs-lookup"><span data-stu-id="36935-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36935-294">Podle pravidla č. 3</span><span class="sxs-lookup"><span data-stu-id="36935-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="36935-295">Č1 zahrnuje čas, materiál, výdaje a poplatky za podmnožinu úkolů v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="36935-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="36935-296">ŘN2 zahrnuje čas, materiál, výdaje a poplatky za podmnožinu úkolů v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="36935-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="36935-297">Jediná další validace je kolem podmnožiny úkolů na ŘN1, která se liší od podmnožiny úkolů na ŘN2, aby se zajistilo, že nedojde k překrývání.</span><span class="sxs-lookup"><span data-stu-id="36935-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="36935-298">Toto provádí systém, když jsou přidruženy úkoly.</span><span class="sxs-lookup"><span data-stu-id="36935-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="36935-299">P1</span><span class="sxs-lookup"><span data-stu-id="36935-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="36935-300">Č1</span><span class="sxs-lookup"><span data-stu-id="36935-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="36935-301">ŘN2</span><span class="sxs-lookup"><span data-stu-id="36935-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-302">O1</span><span class="sxs-lookup"><span data-stu-id="36935-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="36935-303">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="36935-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="36935-304">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="36935-305">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="36935-306">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-307">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="36935-308">P1</span><span class="sxs-lookup"><span data-stu-id="36935-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="36935-309">Č1</span><span class="sxs-lookup"><span data-stu-id="36935-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="36935-310">ŘN1</span><span class="sxs-lookup"><span data-stu-id="36935-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-311">O1</span><span class="sxs-lookup"><span data-stu-id="36935-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="36935-312">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="36935-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="36935-313">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="36935-314">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="36935-315">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-316">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36935-317">Platné</span><span class="sxs-lookup"><span data-stu-id="36935-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36935-318">Podle pravidla č. 5 jsou Č1 a Č2 dvě nabídky u stejné příležitosti, takže mohou obě odhadovat na stejných komponentech projektu.</span><span class="sxs-lookup"><span data-stu-id="36935-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="36935-319">P1</span><span class="sxs-lookup"><span data-stu-id="36935-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="36935-320">Č2</span><span class="sxs-lookup"><span data-stu-id="36935-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="36935-321">ŘN1</span><span class="sxs-lookup"><span data-stu-id="36935-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-322">O1</span><span class="sxs-lookup"><span data-stu-id="36935-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="36935-323">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="36935-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="36935-324">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="36935-325">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="36935-326">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-327">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="36935-328">P1</span><span class="sxs-lookup"><span data-stu-id="36935-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="36935-329">Č1</span><span class="sxs-lookup"><span data-stu-id="36935-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="36935-330">ŘN1</span><span class="sxs-lookup"><span data-stu-id="36935-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-331">O1</span><span class="sxs-lookup"><span data-stu-id="36935-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="36935-332">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="36935-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="36935-333">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="36935-334">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="36935-335">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-336">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36935-337">Neplatný</span><span class="sxs-lookup"><span data-stu-id="36935-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36935-338">Podle pravidla č. 4 jsou Č1 a Č2 dvě nabídky na různé příležitosti, takže mohou obě odhadovat na stejných komponentech stejného projektu.</span><span class="sxs-lookup"><span data-stu-id="36935-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="36935-339">P2</span><span class="sxs-lookup"><span data-stu-id="36935-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="36935-340">Č1</span><span class="sxs-lookup"><span data-stu-id="36935-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="36935-341">ŘN1</span><span class="sxs-lookup"><span data-stu-id="36935-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-342">O1</span><span class="sxs-lookup"><span data-stu-id="36935-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="36935-343">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="36935-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="36935-344">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="36935-345">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="36935-346">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="36935-347">Ano</span><span class="sxs-lookup"><span data-stu-id="36935-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
