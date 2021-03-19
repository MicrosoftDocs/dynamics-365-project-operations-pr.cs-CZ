---
title: Přehled řádků nabídky založené na projektu – omezeno
description: Toto téma poskytuje informace o používání řádků nabídek založených na projektu pro práci na projektu. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4865c06691fba09eacf5fe6449adfaf542444520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272965"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="0ca88-104">Přehled řádků nabídky založené na projektu – omezeno</span><span class="sxs-lookup"><span data-stu-id="0ca88-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="0ca88-105">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="0ca88-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0ca88-106">Řádky nabídek založených na projektu jsou navrženy tak, aby pomohly odhadnout projektovou práci na zakázce.</span><span class="sxs-lookup"><span data-stu-id="0ca88-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="0ca88-107">Struktura řádku nabídky založené na projektu se rozšiřuje u odhadů projektu o následující koncepty:</span><span class="sxs-lookup"><span data-stu-id="0ca88-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="0ca88-108">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="0ca88-108">Billing Method</span></span>
- <span data-ttu-id="0ca88-109">Projekt a mapování úkolů</span><span class="sxs-lookup"><span data-stu-id="0ca88-109">Project and Task Mapping</span></span>
- <span data-ttu-id="0ca88-110">Zahrnuté třídy transakcí</span><span class="sxs-lookup"><span data-stu-id="0ca88-110">Included Transaction classes</span></span>
- <span data-ttu-id="0ca88-111">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="0ca88-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="0ca88-112">Nastavení účtovatelnosti</span><span class="sxs-lookup"><span data-stu-id="0ca88-112">Chargeability setup</span></span>
- <span data-ttu-id="0ca88-113">Odhad pomocí podrobností řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="0ca88-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="0ca88-114">Zákazníci řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="0ca88-114">Quote line Customers</span></span>

<span data-ttu-id="0ca88-115">Následující tabulka poskytuje informace o polích na karrtě **Všeobecné** řádku nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="0ca88-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="0ca88-116">Tato pole pomáhají připravit základ pro podrobný počáteční odhad projektové práce.</span><span class="sxs-lookup"><span data-stu-id="0ca88-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="0ca88-117">**Pole**</span><span class="sxs-lookup"><span data-stu-id="0ca88-117">**Field**</span></span> | <span data-ttu-id="0ca88-118">**Popis**</span><span class="sxs-lookup"><span data-stu-id="0ca88-118">**Description**</span></span> | <span data-ttu-id="0ca88-119">**Dopad na příjem dat**</span><span class="sxs-lookup"><span data-stu-id="0ca88-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0ca88-120">Jméno</span><span class="sxs-lookup"><span data-stu-id="0ca88-120">Name</span></span> | <span data-ttu-id="0ca88-121">Název řádku nabídky, který by vám měl pomoci identifikovat diskrétní součást nabídky, která se odhaduje.</span><span class="sxs-lookup"><span data-stu-id="0ca88-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="0ca88-122">Zkopírováno do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="0ca88-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0ca88-123">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="0ca88-123">Billing Method</span></span> | <span data-ttu-id="0ca88-124">U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z příslušného pole na řádku příležitosti.</span><span class="sxs-lookup"><span data-stu-id="0ca88-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="0ca88-125">Toto pole zahrnuje dva hlavní smluvní modely podporované Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="0ca88-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="0ca88-126">- Pevná cena</span><span class="sxs-lookup"><span data-stu-id="0ca88-126">- Fixed price</span></span></br><span data-ttu-id="0ca88-127">- Čas a materiál.</span><span class="sxs-lookup"><span data-stu-id="0ca88-127">- Time and material.</span></span>| <span data-ttu-id="0ca88-128">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="0ca88-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0ca88-129">Project</span><span class="sxs-lookup"><span data-stu-id="0ca88-129">Project</span></span> | <span data-ttu-id="0ca88-130">Pomocí tohoto volitelného pole můžete identifikovat projekt, který bude použit k provedení práce na této zakázce.</span><span class="sxs-lookup"><span data-stu-id="0ca88-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="0ca88-131">Když je projekt mapován na řádek nabídky, pomáhá to při nastavení zpoplatněných úkolů a také při stanovení odhadu založeného na projektu do řádku nabídky jako podrobnosti řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="0ca88-132">Pokud projekt není mapován na řádek nabídky založené na projektu, odhad by měl být vytvořen ručně – vytvořením každé podrobnosti řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="0ca88-133">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="0ca88-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="0ca88-134">Zahrnuté úkoly</span><span class="sxs-lookup"><span data-stu-id="0ca88-134">Included Tasks</span></span> | <span data-ttu-id="0ca88-135">Udává, zda je tento řádek nabídky použit pro všechny nebo jen některé úkoly vybraného projektu.</span><span class="sxs-lookup"><span data-stu-id="0ca88-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="0ca88-136">Toto pole může obsahovat následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="0ca88-136">This field has the following possible values:</span></span></br><span data-ttu-id="0ca88-137">- Všechny projektové úkoly</span><span class="sxs-lookup"><span data-stu-id="0ca88-137">- All project tasks</span></span></br><span data-ttu-id="0ca88-138">- Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="0ca88-138">- Selected project tasks only</span></span></br><span data-ttu-id="0ca88-139">Prázdná hodnota v tomto poli odpovídá možnosti **Všechny úkoly projektu**.</span><span class="sxs-lookup"><span data-stu-id="0ca88-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="0ca88-140">Když je vybrána hodnota **Pouze vybrané úkoly projektu**, poté je možné na stránce projektu v kartě **Nastavení fakturace úkolu** vybrat konkrétní úkoly a přidružit je k tomuto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="0ca88-141">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="0ca88-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0ca88-142">Zahrnout čas</span><span class="sxs-lookup"><span data-stu-id="0ca88-142">Include Time</span></span> | <span data-ttu-id="0ca88-143">Příznak **Ano**/**Ne** určuje, zda budou časové transakce nebo náklady práce ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0ca88-144">Hodnota **Ne** určuje, že časové transakce nebo náklady práce nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0ca88-145">Hodnota **Ano** určuje, že časové transakce nebo náklady práce budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0ca88-146">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="0ca88-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0ca88-147">Zahrnout výdaj</span><span class="sxs-lookup"><span data-stu-id="0ca88-147">Include Expense</span></span> | <span data-ttu-id="0ca88-148">Příznak **Ano**/**Ne** určuje, zda budou výdajové náklady ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0ca88-149">Hodnota **Ne** určuje, že výdajové náklady nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0ca88-150">Hodnota **Ano** určuje, že výdajové náklady budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0ca88-151">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="0ca88-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0ca88-152">Zahrnout poplatek</span><span class="sxs-lookup"><span data-stu-id="0ca88-152">Include Fee</span></span> | <span data-ttu-id="0ca88-153">Příznak **Ano**/**Ne** určuje, zda budou poplatky ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0ca88-154">Hodnota **Ne** určuje, že poplatky nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0ca88-155">Hodnota **Ano** určuje, že poplatky budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0ca88-156">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="0ca88-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0ca88-157">Nabízená částka</span><span class="sxs-lookup"><span data-stu-id="0ca88-157">Quoted Amount</span></span> | <span data-ttu-id="0ca88-158">Jedná se o částku, která bude zákazníkovi nabídnuta za veškerou práci předpovídanou v tomto řádku projektové nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="0ca88-159">U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z pole **Rozpočet zákazníka** na řádku příležitosti.</span><span class="sxs-lookup"><span data-stu-id="0ca88-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="0ca88-160">Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky na podrobnostech řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="0ca88-161">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="0ca88-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0ca88-162">Odhad daně</span><span class="sxs-lookup"><span data-stu-id="0ca88-162">Estimated Tax</span></span> | <span data-ttu-id="0ca88-163">Toto je upravitelné pole, kde může uživatel přidat odhadovanou částku daně do řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="0ca88-164">Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky daně na podrobnostech řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="0ca88-165">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="0ca88-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0ca88-166">Nabízená částka včetně daně</span><span class="sxs-lookup"><span data-stu-id="0ca88-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="0ca88-167">Toto pole představuje částku nabídky po zdanění a je pouze ke čtení.</span><span class="sxs-lookup"><span data-stu-id="0ca88-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="0ca88-168">Částka v tomto poli se počítá jako *Nabízená částka + daň*.</span><span class="sxs-lookup"><span data-stu-id="0ca88-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="0ca88-169">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="0ca88-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0ca88-170">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="0ca88-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="0ca88-171">Toto pole je upravitelné a je k dispozici pouze na řádcích nabídek založených na projektu, které mají nastaven způsob fakturace **Čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="0ca88-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="0ca88-172">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="0ca88-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0ca88-173">Rozpočet zákazníka</span><span class="sxs-lookup"><span data-stu-id="0ca88-173">Customer Budget</span></span> | <span data-ttu-id="0ca88-174">Toto pole je upravitelné a jeho hodnota se zkopíruje z příslušného pole na řádku příležitosti, když je nabídka vytvořena z příležitosti.</span><span class="sxs-lookup"><span data-stu-id="0ca88-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="0ca88-175">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="0ca88-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="0ca88-176">Pravidla ověření pro pole na kartě Všeobecné řádků nabídek založených na projektu</span><span class="sxs-lookup"><span data-stu-id="0ca88-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="0ca88-177">**Pravidlo 1** : Pokud je pole **Zahrnuté úkoly** prázdné nebo je-li nastaveno na hodnotu **Všechny úkoly projektu**, je projekt zahrnut do řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="0ca88-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="0ca88-178">**Pravidlo 2** : Pokud je pole **Zahrnuté úkoly** prázdné nebo je-li nastaveno na hodnotu **Všechny úkoly projektu**, lze projekt a určitou třídu transakcí zahrnout pouze na jeden řádek nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="0ca88-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="0ca88-179">**Pravidlo 3**: Pokud je pole **Zahrnuté úkoly** prázdné nebo je-li nastaveno na hodnotu **Pouze vybrané úkoly projektu**, lze projekt a určitou třídu transakcí zahrnout do více řádků nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="0ca88-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="0ca88-180">**Pravidlo 4** : Pokud má příležitost více nabídek, mohou existovat řádky nabídky z různých nabídek, které všechny odkazují na stejný projekt a zahrnují stejnou třídu transakcí.</span><span class="sxs-lookup"><span data-stu-id="0ca88-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="0ca88-181">**Pravidlo 5** : Pokud nabídky nepatří ke stejné příležitosti, nemohou zahrnovat stejný projekt a třídu transakcí.</span><span class="sxs-lookup"><span data-stu-id="0ca88-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="0ca88-182">
                    <strong>Příležitost</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0ca88-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="0ca88-183">
                    <strong>Nabídka</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0ca88-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0ca88-184">
                    <strong>Řádek nabídky</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0ca88-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0ca88-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0ca88-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="0ca88-186">
                    <strong>Zahrnuté úkoly</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0ca88-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="0ca88-187">
                    <strong>Zahrnout čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0ca88-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="0ca88-188">
                    <strong>Zahrnout výdaj</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0ca88-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0ca88-189">
                    <strong>Zahrnout</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0ca88-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="0ca88-190">
                    <strong>Poplatek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0ca88-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="0ca88-191">
                    <strong>Platné / Neplatné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0ca88-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="0ca88-192">
                    <strong>Důvod</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0ca88-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0ca88-193">P1</span><span class="sxs-lookup"><span data-stu-id="0ca88-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0ca88-194">Č1</span><span class="sxs-lookup"><span data-stu-id="0ca88-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-195">ŘN1</span><span class="sxs-lookup"><span data-stu-id="0ca88-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-196">O1</span><span class="sxs-lookup"><span data-stu-id="0ca88-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0ca88-197">Prázdný</span><span class="sxs-lookup"><span data-stu-id="0ca88-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-198">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-199">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-200">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0ca88-201">Neplatný</span><span class="sxs-lookup"><span data-stu-id="0ca88-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0ca88-202">Porušení pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="0ca88-202">Violation of Rule #2.</span></span> <span data-ttu-id="0ca88-203">Čas, náklady a poplatky za projekt P1 jsou zahrnuty v řádcích nabídky ŘN1 a ŘN2.</span><span class="sxs-lookup"><span data-stu-id="0ca88-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0ca88-204">P1</span><span class="sxs-lookup"><span data-stu-id="0ca88-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0ca88-205">Č1</span><span class="sxs-lookup"><span data-stu-id="0ca88-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-206">ŘN2</span><span class="sxs-lookup"><span data-stu-id="0ca88-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-207">O1</span><span class="sxs-lookup"><span data-stu-id="0ca88-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0ca88-208">Prázdný</span><span class="sxs-lookup"><span data-stu-id="0ca88-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-209">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-210">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-211">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-211">Yes</span></span> </p>
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
<span data-ttu-id="0ca88-212">P1</span><span class="sxs-lookup"><span data-stu-id="0ca88-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0ca88-213">Č1</span><span class="sxs-lookup"><span data-stu-id="0ca88-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-214">ŘN1</span><span class="sxs-lookup"><span data-stu-id="0ca88-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-215">O1</span><span class="sxs-lookup"><span data-stu-id="0ca88-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0ca88-216">Prázdný</span><span class="sxs-lookup"><span data-stu-id="0ca88-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-217">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-218">No</span><span class="sxs-lookup"><span data-stu-id="0ca88-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-219">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0ca88-220">Neplatný</span><span class="sxs-lookup"><span data-stu-id="0ca88-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0ca88-221">Porušení pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="0ca88-221">Violation of Rule #2.</span></span> <span data-ttu-id="0ca88-222">Čas a poplatky za projekt P1 jsou zahrnuty v řádcích nabídky ŘN1 a ŘN2.</span><span class="sxs-lookup"><span data-stu-id="0ca88-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0ca88-223">P1</span><span class="sxs-lookup"><span data-stu-id="0ca88-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0ca88-224">Č1</span><span class="sxs-lookup"><span data-stu-id="0ca88-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-225">ŘN2</span><span class="sxs-lookup"><span data-stu-id="0ca88-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-226">O1</span><span class="sxs-lookup"><span data-stu-id="0ca88-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0ca88-227">Prázdný</span><span class="sxs-lookup"><span data-stu-id="0ca88-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-228">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-229">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-230">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-230">Yes</span></span> </p>
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
<span data-ttu-id="0ca88-231">P1</span><span class="sxs-lookup"><span data-stu-id="0ca88-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0ca88-232">Č1</span><span class="sxs-lookup"><span data-stu-id="0ca88-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-233">ŘN1</span><span class="sxs-lookup"><span data-stu-id="0ca88-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-234">O1</span><span class="sxs-lookup"><span data-stu-id="0ca88-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0ca88-235">Prázdný</span><span class="sxs-lookup"><span data-stu-id="0ca88-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-236">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-237">No</span><span class="sxs-lookup"><span data-stu-id="0ca88-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-238">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0ca88-239">Platná</span><span class="sxs-lookup"><span data-stu-id="0ca88-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="0ca88-240">Čas a poplatky za projekt P1 jsou zahrnuty v ŘN1.</span><span class="sxs-lookup"><span data-stu-id="0ca88-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="0ca88-241">Výdaje na projekt P1 jsou zahrnuty do ŘN2.</span><span class="sxs-lookup"><span data-stu-id="0ca88-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="0ca88-242">Neexistuje žádné překrývání položek zahrnutých v každém řádku nabídky, která je platná.</span><span class="sxs-lookup"><span data-stu-id="0ca88-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0ca88-243">P1</span><span class="sxs-lookup"><span data-stu-id="0ca88-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0ca88-244">Č1</span><span class="sxs-lookup"><span data-stu-id="0ca88-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-245">ŘN2</span><span class="sxs-lookup"><span data-stu-id="0ca88-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-246">O1</span><span class="sxs-lookup"><span data-stu-id="0ca88-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0ca88-247">Prázdný</span><span class="sxs-lookup"><span data-stu-id="0ca88-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-248">No</span><span class="sxs-lookup"><span data-stu-id="0ca88-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-249">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-250">No</span><span class="sxs-lookup"><span data-stu-id="0ca88-250">No</span></span> </p>
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
<span data-ttu-id="0ca88-251">P1</span><span class="sxs-lookup"><span data-stu-id="0ca88-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0ca88-252">Č1</span><span class="sxs-lookup"><span data-stu-id="0ca88-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-253">ŘN1</span><span class="sxs-lookup"><span data-stu-id="0ca88-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-254">O1</span><span class="sxs-lookup"><span data-stu-id="0ca88-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0ca88-255">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="0ca88-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-256">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-257">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-258">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0ca88-259">Neplatný</span><span class="sxs-lookup"><span data-stu-id="0ca88-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0ca88-260">Porušení výše uvedeného pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="0ca88-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="0ca88-261">N1 zahrnuje čas, výdaje a poplatky za podmnožinu úkolů v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="0ca88-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0ca88-262">ŘN2 zahrnuje čas, výdaje a poplatky za celý projekt P1 a překrývá se s tím, co je zahrnuto v N1.</span><span class="sxs-lookup"><span data-stu-id="0ca88-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0ca88-263">P1</span><span class="sxs-lookup"><span data-stu-id="0ca88-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0ca88-264">Č1</span><span class="sxs-lookup"><span data-stu-id="0ca88-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-265">ŘN2</span><span class="sxs-lookup"><span data-stu-id="0ca88-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-266">O1</span><span class="sxs-lookup"><span data-stu-id="0ca88-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0ca88-267">Prázdný</span><span class="sxs-lookup"><span data-stu-id="0ca88-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-268">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-269">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-270">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-270">Yes</span></span> </p>
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
<span data-ttu-id="0ca88-271">P1</span><span class="sxs-lookup"><span data-stu-id="0ca88-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0ca88-272">Č1</span><span class="sxs-lookup"><span data-stu-id="0ca88-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-273">ŘN1</span><span class="sxs-lookup"><span data-stu-id="0ca88-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-274">O1</span><span class="sxs-lookup"><span data-stu-id="0ca88-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0ca88-275">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="0ca88-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-276">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-277">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-278">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0ca88-279">Platná</span><span class="sxs-lookup"><span data-stu-id="0ca88-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0ca88-280">Podle výše uvedeného pravidla č. 3,</span><span class="sxs-lookup"><span data-stu-id="0ca88-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="0ca88-281">N1 zahrnuje čas, výdaje a poplatky za podmnožinu úkolů v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="0ca88-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0ca88-282">ŘN2 zahrnuje čas, výdaje a poplatky za podmnožinu úkolů v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="0ca88-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0ca88-283">Jediné další ověření probíhá u podmnožiny úkolů na ŘN1, které se liší od podmnožiny úkolů na ŘN2.</span><span class="sxs-lookup"><span data-stu-id="0ca88-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="0ca88-284">Tím je zajištěno, že nedojde k žádnému překrytí.</span><span class="sxs-lookup"><span data-stu-id="0ca88-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="0ca88-285">Toto provádí systém, když jsou přidruženy úkoly.</span><span class="sxs-lookup"><span data-stu-id="0ca88-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0ca88-286">P1</span><span class="sxs-lookup"><span data-stu-id="0ca88-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0ca88-287">Č1</span><span class="sxs-lookup"><span data-stu-id="0ca88-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-288">ŘN2</span><span class="sxs-lookup"><span data-stu-id="0ca88-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-289">O1</span><span class="sxs-lookup"><span data-stu-id="0ca88-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0ca88-290">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="0ca88-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-291">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-292">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-293">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-293">Yes</span></span> </p>
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
<span data-ttu-id="0ca88-294">P1</span><span class="sxs-lookup"><span data-stu-id="0ca88-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0ca88-295">Č1</span><span class="sxs-lookup"><span data-stu-id="0ca88-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-296">ŘN1</span><span class="sxs-lookup"><span data-stu-id="0ca88-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-297">O1</span><span class="sxs-lookup"><span data-stu-id="0ca88-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0ca88-298">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="0ca88-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-299">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-300">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-301">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="0ca88-302">Platná</span><span class="sxs-lookup"><span data-stu-id="0ca88-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0ca88-303">Na základě pravidla č. 5 jsou N1 a N2 dvě nabídky u stejné příležitosti, takže mohou obě odhadovat položky pro stejné součásti projektu.</span><span class="sxs-lookup"><span data-stu-id="0ca88-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0ca88-304">P1</span><span class="sxs-lookup"><span data-stu-id="0ca88-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0ca88-305">Č2</span><span class="sxs-lookup"><span data-stu-id="0ca88-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-306">ŘN1</span><span class="sxs-lookup"><span data-stu-id="0ca88-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-307">O1</span><span class="sxs-lookup"><span data-stu-id="0ca88-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0ca88-308">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="0ca88-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-309">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-310">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-311">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-311">Yes</span></span> </p>
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
<span data-ttu-id="0ca88-312">P1</span><span class="sxs-lookup"><span data-stu-id="0ca88-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0ca88-313">Č1</span><span class="sxs-lookup"><span data-stu-id="0ca88-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-314">ŘN1</span><span class="sxs-lookup"><span data-stu-id="0ca88-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-315">O1</span><span class="sxs-lookup"><span data-stu-id="0ca88-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0ca88-316">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="0ca88-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-317">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-318">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-319">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="0ca88-320">Platná</span><span class="sxs-lookup"><span data-stu-id="0ca88-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0ca88-321">Na základě pravidla č. 4 jsou N1 a N2 dvě nabídky u různých příležitostí, takže nemohou odhadovat položky pro stejné součásti stejného projektu.</span><span class="sxs-lookup"><span data-stu-id="0ca88-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0ca88-322">P2</span><span class="sxs-lookup"><span data-stu-id="0ca88-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0ca88-323">Č1</span><span class="sxs-lookup"><span data-stu-id="0ca88-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-324">ŘN1</span><span class="sxs-lookup"><span data-stu-id="0ca88-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-325">O1</span><span class="sxs-lookup"><span data-stu-id="0ca88-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="0ca88-326">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="0ca88-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-327">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0ca88-328">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0ca88-329">Ano</span><span class="sxs-lookup"><span data-stu-id="0ca88-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="0ca88-330">Neplatný</span><span class="sxs-lookup"><span data-stu-id="0ca88-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]