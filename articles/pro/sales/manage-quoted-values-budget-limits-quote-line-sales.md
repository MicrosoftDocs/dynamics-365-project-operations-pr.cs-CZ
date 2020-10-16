---
title: Řádky nabídky založené na projektu (Pro)
description: Toto téma poskytuje informace o používání řádků nabídek založených na projektu pro práci na projektu. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907991"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="c3b4a-104">Řádky nabídky založené na projektu (Pro)</span><span class="sxs-lookup"><span data-stu-id="c3b4a-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="c3b4a-105">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="c3b4a-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c3b4a-106">Řádky nabídek založených na projektu jsou navrženy tak, aby pomohly odhadnout projektovou práci na zakázce.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="c3b4a-107">Struktura řádku nabídky založené na projektu se rozšiřuje u odhadů projektu o následující koncepty:</span><span class="sxs-lookup"><span data-stu-id="c3b4a-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="c3b4a-108">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="c3b4a-108">Billing Method</span></span>
- <span data-ttu-id="c3b4a-109">Projekt a mapování úkolů</span><span class="sxs-lookup"><span data-stu-id="c3b4a-109">Project and Task Mapping</span></span>
- <span data-ttu-id="c3b4a-110">Zahrnuté třídy transakcí</span><span class="sxs-lookup"><span data-stu-id="c3b4a-110">Included Transaction classes</span></span>
- <span data-ttu-id="c3b4a-111">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="c3b4a-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="c3b4a-112">Nastavení účtovatelnosti</span><span class="sxs-lookup"><span data-stu-id="c3b4a-112">Chargeability setup</span></span>
- <span data-ttu-id="c3b4a-113">Odhad pomocí podrobností řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="c3b4a-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="c3b4a-114">Zákazníci řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="c3b4a-114">Quote line Customers</span></span>

<span data-ttu-id="c3b4a-115">Následující tabulka poskytuje informace o polích na karrtě **Všeobecné** řádku nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="c3b4a-116">Tato pole pomáhají připravit základ pro podrobný počáteční odhad projektové práce.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="c3b4a-117">**Pole**</span><span class="sxs-lookup"><span data-stu-id="c3b4a-117">**Field**</span></span> | <span data-ttu-id="c3b4a-118">**Relevance, účel a vedení**</span><span class="sxs-lookup"><span data-stu-id="c3b4a-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="c3b4a-119">**Dopad na následné složky**</span><span class="sxs-lookup"><span data-stu-id="c3b4a-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c3b4a-120">Jméno</span><span class="sxs-lookup"><span data-stu-id="c3b4a-120">Name</span></span> | <span data-ttu-id="c3b4a-121">Název řádku nabídky, který by vám měl pomoci identifikovat diskrétní součást nabídky, která se odhaduje.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="c3b4a-122">Zkopírováno do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c3b4a-123">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="c3b4a-123">Billing Method</span></span> | <span data-ttu-id="c3b4a-124">U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z příslušného pole na řádku příležitosti.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="c3b4a-125">Toto pole zahrnuje dva hlavní smluvní modely podporované aplikací Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="c3b4a-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="c3b4a-126">- Pevná cena</span><span class="sxs-lookup"><span data-stu-id="c3b4a-126">- Fixed price</span></span></br><span data-ttu-id="c3b4a-127">- Čas a materiál.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-127">- Time and material.</span></span>| <span data-ttu-id="c3b4a-128">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c3b4a-129">Project</span><span class="sxs-lookup"><span data-stu-id="c3b4a-129">Project</span></span> | <span data-ttu-id="c3b4a-130">Pomocí tohoto volitelného pole můžete identifikovat projekt, který bude použit k provedení práce na této zakázce.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="c3b4a-131">Když je projekt mapován na řádek nabídky, pomáhá to při nastavení zpoplatněných úkolů a také při stanovení odhadu založeného na projektu do řádku nabídky jako podrobnosti řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="c3b4a-132">Pokud projekt není mapován na řádek nabídky založené na projektu, odhad by měl být vytvořen ručně – vytvořením každé podrobnosti řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="c3b4a-133">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="c3b4a-134">Zahrnuté úkoly</span><span class="sxs-lookup"><span data-stu-id="c3b4a-134">Included Tasks</span></span> | <span data-ttu-id="c3b4a-135">Udává, zda je tento řádek nabídky použit pro všechny nebo jen některé úkoly vybraného projektu.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="c3b4a-136">Toto pole může obsahovat následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="c3b4a-136">This field has the following possible values:</span></span></br><span data-ttu-id="c3b4a-137">- Všechny projektové úkoly</span><span class="sxs-lookup"><span data-stu-id="c3b4a-137">- All project tasks</span></span></br><span data-ttu-id="c3b4a-138">- Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="c3b4a-138">- Selected project tasks only</span></span></br><span data-ttu-id="c3b4a-139">Prázdná hodnota v tomto poli odpovídá možnosti **Všechny úkoly projektu**.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="c3b4a-140">Když je vybrána hodnota **Pouze vybrané úkoly projektu**, poté je možné na stránce projektu v kartě **Nastavení fakturace úkolu** vybrat konkrétní úkoly a přidružit je k tomuto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="c3b4a-141">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c3b4a-142">Zahrnout čas</span><span class="sxs-lookup"><span data-stu-id="c3b4a-142">Include Time</span></span> | <span data-ttu-id="c3b4a-143">Příznak **Ano**/**Ne** určuje, zda budou časové transakce nebo náklady práce ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c3b4a-144">Hodnota **Ne** určuje, že časové transakce nebo náklady práce nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c3b4a-145">Hodnota **Ano** určuje, že časové transakce nebo náklady práce budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c3b4a-146">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c3b4a-147">Zahrnout výdaj</span><span class="sxs-lookup"><span data-stu-id="c3b4a-147">Include Expense</span></span> | <span data-ttu-id="c3b4a-148">Příznak **Ano**/**Ne** určuje, zda budou výdajové náklady ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c3b4a-149">Hodnota **Ne** určuje, že výdajové náklady nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c3b4a-150">Hodnota **Ano** určuje, že výdajové náklady budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c3b4a-151">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c3b4a-152">Zahrnout poplatek</span><span class="sxs-lookup"><span data-stu-id="c3b4a-152">Include Fee</span></span> | <span data-ttu-id="c3b4a-153">Příznak **Ano**/**Ne** určuje, zda budou poplatky ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c3b4a-154">Hodnota **Ne** určuje, že poplatky nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c3b4a-155">Hodnota **Ano** určuje, že poplatky budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c3b4a-156">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c3b4a-157">Nabízená částka</span><span class="sxs-lookup"><span data-stu-id="c3b4a-157">Quoted Amount</span></span> | <span data-ttu-id="c3b4a-158">Jedná se o částku, která bude zákazníkovi nabídnuta za veškerou práci předpovídanou v tomto řádku projektové nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="c3b4a-159">U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z pole **Rozpočet zákazníka** na řádku příležitosti.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="c3b4a-160">Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky na podrobnostech řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="c3b4a-161">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c3b4a-162">Odhad daně</span><span class="sxs-lookup"><span data-stu-id="c3b4a-162">Estimated Tax</span></span> | <span data-ttu-id="c3b4a-163">Toto je upravitelné pole, kde může uživatel přidat odhadovanou částku daně do řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="c3b4a-164">Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky daně na podrobnostech řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="c3b4a-165">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c3b4a-166">Nabízená částka včetně daně</span><span class="sxs-lookup"><span data-stu-id="c3b4a-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="c3b4a-167">Toto pole představuje částku nabídky po zdanění a je pouze ke čtení.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="c3b4a-168">Částka v tomto poli se počítá jako *Nabízená částka + daň*.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="c3b4a-169">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c3b4a-170">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="c3b4a-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="c3b4a-171">Toto pole je upravitelné a je k dispozici pouze na řádcích nabídek založených na projektu, které mají nastaven způsob fakturace **Čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="c3b4a-172">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c3b4a-173">Rozpočet zákazníka</span><span class="sxs-lookup"><span data-stu-id="c3b4a-173">Customer Budget</span></span> | <span data-ttu-id="c3b4a-174">Toto pole je upravitelné a jeho hodnota se zkopíruje z příslušného pole na řádku příležitosti, když je nabídka vytvořena z příležitosti.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="c3b4a-175">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="c3b4a-176">Pravidla ověření pro pole na kartě Všeobecné řádků nabídek založených na projektu</span><span class="sxs-lookup"><span data-stu-id="c3b4a-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="c3b4a-177">**Pravidlo 1** : Pokud je pole **Zahrnuté úkoly** prázdné nebo je-li nastaveno na hodnotu **Všechny úkoly projektu**, je projekt zahrnut do řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="c3b4a-178">**Pravidlo 2** : Pokud je pole **Zahrnuté úkoly** prázdné nebo je-li nastaveno na hodnotu **Všechny úkoly projektu**, lze projekt a určitou třídu transakcí zahrnout pouze na jeden řádek nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="c3b4a-179">**Pravidlo 3**: Pokud je pole **Zahrnuté úkoly** prázdné nebo je-li nastaveno na hodnotu **Pouze vybrané úkoly projektu**, lze projekt a určitou třídu transakcí zahrnout do více řádků nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="c3b4a-180">**Pravidlo 4** : Pokud má příležitost více nabídek, mohou existovat řádky nabídky z různých nabídek, které všechny odkazují na stejný projekt a zahrnují stejnou třídu transakcí.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="c3b4a-181">**Pravidlo 5** : Pokud nabídky nepatří ke stejné příležitosti, nemohou zahrnovat stejný projekt a třídu transakcí.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="c3b4a-182">
                    <strong>Příležitost</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c3b4a-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="c3b4a-183">
                    <strong>Nabídka</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c3b4a-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="c3b4a-184">
                    <strong>Řádek nabídky</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c3b4a-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="c3b4a-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c3b4a-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="c3b4a-186">
                    <strong>Zahrnuté úkoly</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c3b4a-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="c3b4a-187">
                    <strong>Zahrnout čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c3b4a-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="c3b4a-188">
                    <strong>Zahrnout výdaj</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c3b4a-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="c3b4a-189">
                    <strong>Zahrnout</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c3b4a-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="c3b4a-190">
                    <strong>Poplatek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c3b4a-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="c3b4a-191">
                    <strong>Platné / Neplatné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c3b4a-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="c3b4a-192">
                    <strong>Důvod</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c3b4a-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c3b4a-193">P1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c3b4a-194">Č1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-195">ŘN1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-196">O1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c3b4a-197">Prázdný</span><span class="sxs-lookup"><span data-stu-id="c3b4a-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-198">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-199">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-200">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c3b4a-201">Neplatný</span><span class="sxs-lookup"><span data-stu-id="c3b4a-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c3b4a-202">Porušení pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-202">Violation of Rule #2.</span></span> <span data-ttu-id="c3b4a-203">Čas, náklady a poplatky za projekt P1 jsou zahrnuty v řádcích nabídky ŘN1 a ŘN2.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c3b4a-204">P1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c3b4a-205">Č1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-206">ŘN2</span><span class="sxs-lookup"><span data-stu-id="c3b4a-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-207">O1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c3b4a-208">Prázdný</span><span class="sxs-lookup"><span data-stu-id="c3b4a-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-209">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-210">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-211">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c3b4a-212">P1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c3b4a-213">Č1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-214">ŘN1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-215">O1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c3b4a-216">Prázdný</span><span class="sxs-lookup"><span data-stu-id="c3b4a-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-217">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-218">No</span><span class="sxs-lookup"><span data-stu-id="c3b4a-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-219">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c3b4a-220">Neplatný</span><span class="sxs-lookup"><span data-stu-id="c3b4a-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c3b4a-221">Porušení pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-221">Violation of Rule #2.</span></span> <span data-ttu-id="c3b4a-222">Čas a poplatky za projekt P1 jsou zahrnuty v řádcích nabídky ŘN1 a ŘN2.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c3b4a-223">P1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c3b4a-224">Č1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-225">ŘN2</span><span class="sxs-lookup"><span data-stu-id="c3b4a-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-226">O1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c3b4a-227">Prázdný</span><span class="sxs-lookup"><span data-stu-id="c3b4a-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-228">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-229">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-230">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c3b4a-231">P1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c3b4a-232">Č1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-233">ŘN1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-234">O1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c3b4a-235">Prázdný</span><span class="sxs-lookup"><span data-stu-id="c3b4a-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-236">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-237">No</span><span class="sxs-lookup"><span data-stu-id="c3b4a-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-238">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c3b4a-239">Platná</span><span class="sxs-lookup"><span data-stu-id="c3b4a-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="c3b4a-240">Čas a poplatky za projekt P1 jsou zahrnuty v ŘN1.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="c3b4a-241">Výdaje na projekt P1 jsou zahrnuty do ŘN2.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="c3b4a-242">Neexistuje žádné překrývání položek zahrnutých v každém řádku nabídky, která je platná.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c3b4a-243">P1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c3b4a-244">Č1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-245">ŘN2</span><span class="sxs-lookup"><span data-stu-id="c3b4a-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-246">O1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c3b4a-247">Prázdný</span><span class="sxs-lookup"><span data-stu-id="c3b4a-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-248">No</span><span class="sxs-lookup"><span data-stu-id="c3b4a-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-249">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-250">No</span><span class="sxs-lookup"><span data-stu-id="c3b4a-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c3b4a-251">P1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c3b4a-252">Č1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-253">ŘN1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-254">O1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c3b4a-255">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="c3b4a-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-256">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-257">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-258">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c3b4a-259">Neplatný</span><span class="sxs-lookup"><span data-stu-id="c3b4a-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c3b4a-260">Porušení výše uvedeného pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="c3b4a-261">N1 zahrnuje čas, výdaje a poplatky za podmnožinu úkolů v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c3b4a-262">ŘN2 zahrnuje čas, výdaje a poplatky za celý projekt P1 a překrývá se s tím, co je zahrnuto v N1.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c3b4a-263">P1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c3b4a-264">Č1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-265">ŘN2</span><span class="sxs-lookup"><span data-stu-id="c3b4a-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-266">O1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c3b4a-267">Prázdný</span><span class="sxs-lookup"><span data-stu-id="c3b4a-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-268">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-269">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-270">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c3b4a-271">P1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c3b4a-272">Č1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-273">ŘN1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-274">O1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c3b4a-275">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="c3b4a-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-276">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-277">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-278">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c3b4a-279">Platná</span><span class="sxs-lookup"><span data-stu-id="c3b4a-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c3b4a-280">Podle výše uvedeného pravidla č. 3,</span><span class="sxs-lookup"><span data-stu-id="c3b4a-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="c3b4a-281">N1 zahrnuje čas, výdaje a poplatky za podmnožinu úkolů v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c3b4a-282">ŘN2 zahrnuje čas, výdaje a poplatky za podmnožinu úkolů v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c3b4a-283">Jediné další ověření probíhá u podmnožiny úkolů na ŘN1, které se liší od podmnožiny úkolů na ŘN2.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="c3b4a-284">Tím je zajištěno, že nedojde k žádnému překrytí.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="c3b4a-285">Toto provádí systém, když jsou přidruženy úkoly.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c3b4a-286">P1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c3b4a-287">Č1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-288">ŘN2</span><span class="sxs-lookup"><span data-stu-id="c3b4a-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-289">O1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c3b4a-290">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="c3b4a-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-291">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-292">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-293">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c3b4a-294">P1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c3b4a-295">Č1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-296">ŘN1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-297">O1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c3b4a-298">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="c3b4a-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-299">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-300">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-301">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="c3b4a-302">Platná</span><span class="sxs-lookup"><span data-stu-id="c3b4a-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c3b4a-303">Na základě pravidla č. 5 jsou N1 a N2 dvě nabídky u stejné příležitosti, takže mohou obě odhadovat položky pro stejné součásti projektu.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c3b4a-304">P1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c3b4a-305">Č2</span><span class="sxs-lookup"><span data-stu-id="c3b4a-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-306">ŘN1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-307">O1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c3b4a-308">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="c3b4a-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-309">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-310">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-311">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c3b4a-312">P1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c3b4a-313">Č1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-314">ŘN1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-315">O1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c3b4a-316">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="c3b4a-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-317">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-318">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-319">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="c3b4a-320">Platná</span><span class="sxs-lookup"><span data-stu-id="c3b4a-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c3b4a-321">Na základě pravidla č. 4 jsou N1 a N2 dvě nabídky u různých příležitostí, takže nemohou odhadovat položky pro stejné součásti stejného projektu.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c3b4a-322">P2</span><span class="sxs-lookup"><span data-stu-id="c3b4a-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c3b4a-323">Č1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-324">ŘN1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-325">O1</span><span class="sxs-lookup"><span data-stu-id="c3b4a-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="c3b4a-326">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="c3b4a-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-327">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c3b4a-328">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c3b4a-329">Ano</span><span class="sxs-lookup"><span data-stu-id="c3b4a-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="c3b4a-330">Neplatný</span><span class="sxs-lookup"><span data-stu-id="c3b4a-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

