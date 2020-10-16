---
title: Řádky nabídky založené na projektu
description: Toto téma poskytuje informace o používání řádků nabídek založených na projektu pro práci na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906115"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="4ac97-103">Řádky nabídky založené na projektu</span><span class="sxs-lookup"><span data-stu-id="4ac97-103">Project-based quote lines</span></span>

<span data-ttu-id="4ac97-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="4ac97-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4ac97-105">Řádky nabídek založených na projektu jsou navrženy tak, aby pomohly odhadnout projektovou práci na zakázce.</span><span class="sxs-lookup"><span data-stu-id="4ac97-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="4ac97-106">Struktura řádku nabídky založené na projektu se rozšiřuje u odhadů projektu o následující koncepty:</span><span class="sxs-lookup"><span data-stu-id="4ac97-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="4ac97-107">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="4ac97-107">Billing Method</span></span>
- <span data-ttu-id="4ac97-108">Mapování projektu</span><span class="sxs-lookup"><span data-stu-id="4ac97-108">Project Mapping</span></span>
- <span data-ttu-id="4ac97-109">Zahrnuté třídy transakcí</span><span class="sxs-lookup"><span data-stu-id="4ac97-109">Included Transaction classes</span></span>
- <span data-ttu-id="4ac97-110">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="4ac97-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="4ac97-111">Nastavení účtovatelnosti</span><span class="sxs-lookup"><span data-stu-id="4ac97-111">Chargeability setup</span></span>
- <span data-ttu-id="4ac97-112">Odhad pomocí podrobností řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="4ac97-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="4ac97-113">Zákazníci řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="4ac97-113">Quote line Customers</span></span>

<span data-ttu-id="4ac97-114">Následující tabulka poskytuje informace o polích na karrtě **Všeobecné** řádku nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="4ac97-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="4ac97-115">Tato pole pomáhají připravit základ pro podrobný počáteční odhad projektové práce.</span><span class="sxs-lookup"><span data-stu-id="4ac97-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="4ac97-116">**Pole**</span><span class="sxs-lookup"><span data-stu-id="4ac97-116">**Field**</span></span> | <span data-ttu-id="4ac97-117">**Relevance, účel a vedení**</span><span class="sxs-lookup"><span data-stu-id="4ac97-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="4ac97-118">**Dopad na následné složky**</span><span class="sxs-lookup"><span data-stu-id="4ac97-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4ac97-119">Jméno</span><span class="sxs-lookup"><span data-stu-id="4ac97-119">Name</span></span> | <span data-ttu-id="4ac97-120">Název řádku nabídky, který by vám měl pomoci identifikovat diskrétní součást nabídky, která se odhaduje.</span><span class="sxs-lookup"><span data-stu-id="4ac97-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="4ac97-121">Zkopírováno do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="4ac97-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ac97-122">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="4ac97-122">Billing Method</span></span> | <span data-ttu-id="4ac97-123">U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z příslušného pole na řádku příležitosti.</span><span class="sxs-lookup"><span data-stu-id="4ac97-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="4ac97-124">Toto pole zahrnuje dva hlavní smluvní modely podporované aplikací Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="4ac97-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="4ac97-125">- Pevná cena</span><span class="sxs-lookup"><span data-stu-id="4ac97-125">- Fixed price</span></span></br><span data-ttu-id="4ac97-126">- Čas a materiál.</span><span class="sxs-lookup"><span data-stu-id="4ac97-126">- Time and material.</span></span>| <span data-ttu-id="4ac97-127">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="4ac97-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ac97-128">Project</span><span class="sxs-lookup"><span data-stu-id="4ac97-128">Project</span></span> | <span data-ttu-id="4ac97-129">Pomocí tohoto volitelného pole můžete identifikovat projekt, který bude použit k provedení práce na této zakázce.</span><span class="sxs-lookup"><span data-stu-id="4ac97-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="4ac97-130">Když je projekt mapován na řádek nabídky, pomáhá to při nastavení zpoplatněných úkolů a také při stanovení odhadu založeného na projektu do řádku nabídky jako podrobnosti řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="4ac97-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="4ac97-131">Pokud projekt není mapován na řádek nabídky založené na projektu, odhad by měl být vytvořen ručně – vytvořením každé podrobnosti řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="4ac97-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="4ac97-132">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="4ac97-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ac97-133">Zahrnout čas</span><span class="sxs-lookup"><span data-stu-id="4ac97-133">Include Time</span></span> | <span data-ttu-id="4ac97-134">Příznak **Ano**/**Ne** určuje, zda budou časové transakce nebo náklady práce ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="4ac97-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4ac97-135">Hodnota **Ne** určuje, že časové transakce nebo náklady práce nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="4ac97-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4ac97-136">Hodnota **Ano** určuje, že časové transakce nebo náklady práce budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="4ac97-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4ac97-137">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="4ac97-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ac97-138">Zahrnout výdaj</span><span class="sxs-lookup"><span data-stu-id="4ac97-138">Include Expense</span></span> | <span data-ttu-id="4ac97-139">Příznak **Ano**/**Ne** určuje, zda budou výdajové náklady ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="4ac97-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4ac97-140">Hodnota **Ne** určuje, že výdajové náklady nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="4ac97-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4ac97-141">Hodnota **Ano** určuje, že výdajové náklady budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="4ac97-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4ac97-142">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="4ac97-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ac97-143">Zahrnout poplatek</span><span class="sxs-lookup"><span data-stu-id="4ac97-143">Include Fee</span></span> | <span data-ttu-id="4ac97-144">Příznak **Ano**/**Ne** určuje, zda budou poplatky ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="4ac97-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4ac97-145">Hodnota **Ne** určuje, že poplatky nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="4ac97-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4ac97-146">Hodnota **Ano** určuje, že poplatky budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="4ac97-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4ac97-147">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="4ac97-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ac97-148">Nabízená částka</span><span class="sxs-lookup"><span data-stu-id="4ac97-148">Quoted Amount</span></span> | <span data-ttu-id="4ac97-149">Jedná se o částku, která bude zákazníkovi nabídnuta za veškerou práci předpovídanou v tomto řádku projektové nabídky.</span><span class="sxs-lookup"><span data-stu-id="4ac97-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="4ac97-150">U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z pole **Rozpočet zákazníka** na řádku příležitosti.</span><span class="sxs-lookup"><span data-stu-id="4ac97-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="4ac97-151">Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky na podrobnostech řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="4ac97-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="4ac97-152">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="4ac97-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ac97-153">Odhad daně</span><span class="sxs-lookup"><span data-stu-id="4ac97-153">Estimated Tax</span></span> | <span data-ttu-id="4ac97-154">Toto je upravitelné pole, kde může uživatel přidat odhadovanou částku daně do řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="4ac97-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="4ac97-155">Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky daně na podrobnostech řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="4ac97-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="4ac97-156">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="4ac97-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ac97-157">Nabízená částka včetně daně</span><span class="sxs-lookup"><span data-stu-id="4ac97-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="4ac97-158">Toto pole představuje částku nabídky po zdanění a je pouze ke čtení.</span><span class="sxs-lookup"><span data-stu-id="4ac97-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="4ac97-159">Částka v tomto poli se počítá jako *Nabízená částka + daň*.</span><span class="sxs-lookup"><span data-stu-id="4ac97-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="4ac97-160">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="4ac97-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ac97-161">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="4ac97-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="4ac97-162">Toto pole je upravitelné a je k dispozici pouze na řádcích nabídek založených na projektu, které mají nastaven způsob fakturace **Čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="4ac97-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="4ac97-163">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="4ac97-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ac97-164">Rozpočet zákazníka</span><span class="sxs-lookup"><span data-stu-id="4ac97-164">Customer Budget</span></span> | <span data-ttu-id="4ac97-165">Toto pole je upravitelné a jeho hodnota se zkopíruje z příslušného pole na řádku příležitosti, když je nabídka vytvořena z příležitosti.</span><span class="sxs-lookup"><span data-stu-id="4ac97-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="4ac97-166">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="4ac97-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="4ac97-167">Pravidla ověření pro pole na kartě Všeobecné řádků nabídek založených na projektu</span><span class="sxs-lookup"><span data-stu-id="4ac97-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="4ac97-168">**Pravidlo 1** : Určitou třídu transakcí ve vybraném projektu lze zahrnout pouze do jednoho řádku nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="4ac97-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="4ac97-169">**Pravidlo 2** : Pokud má příležitost více nabídek, mohou existovat řádky nabídky z různých nabídek, které všechny odkazují na stejný projekt a zahrnují stejnou třídu transakcí.</span><span class="sxs-lookup"><span data-stu-id="4ac97-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="4ac97-170">**Pravidlo 3** : Pokud nabídky nepatří ke stejné příležitosti, nemohou zahrnovat stejný projekt a třídu transakcí.</span><span class="sxs-lookup"><span data-stu-id="4ac97-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="4ac97-171">
                    <strong>Příležitost</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ac97-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="4ac97-172">
                    <strong>Nabídka</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ac97-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="4ac97-173">
                    <strong>Řádek nabídky</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ac97-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="4ac97-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ac97-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="4ac97-175">
                    <strong>Zahrnout čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ac97-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="4ac97-176">
                    <strong>Zahrnout výdaj</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ac97-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="4ac97-177">
                    <strong>Zahrnout</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ac97-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="4ac97-178">
                    <strong>poplatek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ac97-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="4ac97-179">
                    <strong>Platné / Neplatné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ac97-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="4ac97-180">
                    <strong>Důvod</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ac97-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ac97-181">P1</span><span class="sxs-lookup"><span data-stu-id="4ac97-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ac97-182">Č1</span><span class="sxs-lookup"><span data-stu-id="4ac97-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-183">ŘN1</span><span class="sxs-lookup"><span data-stu-id="4ac97-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-184">O1</span><span class="sxs-lookup"><span data-stu-id="4ac97-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-185">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-186">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-187">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ac97-188">Neplatný</span><span class="sxs-lookup"><span data-stu-id="4ac97-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ac97-189">Porušení pravidla č. 1.</span><span class="sxs-lookup"><span data-stu-id="4ac97-189">Violation of Rule #1.</span></span> <span data-ttu-id="4ac97-190">Čas, náklady a poplatky za projekt P1 jsou zahrnuty v obou řádcích nabídky ŘN1 a ŘN2.</span><span class="sxs-lookup"><span data-stu-id="4ac97-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ac97-191">P1</span><span class="sxs-lookup"><span data-stu-id="4ac97-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ac97-192">Č1</span><span class="sxs-lookup"><span data-stu-id="4ac97-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-193">ŘN2</span><span class="sxs-lookup"><span data-stu-id="4ac97-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-194">O1</span><span class="sxs-lookup"><span data-stu-id="4ac97-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-195">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-196">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-197">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-197">Yes</span></span> </p>
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
<span data-ttu-id="4ac97-198">P1</span><span class="sxs-lookup"><span data-stu-id="4ac97-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ac97-199">Č1</span><span class="sxs-lookup"><span data-stu-id="4ac97-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-200">ŘN1</span><span class="sxs-lookup"><span data-stu-id="4ac97-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-201">O1</span><span class="sxs-lookup"><span data-stu-id="4ac97-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-202">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-203">No</span><span class="sxs-lookup"><span data-stu-id="4ac97-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-204">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ac97-205">Neplatný</span><span class="sxs-lookup"><span data-stu-id="4ac97-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ac97-206">Porušení pravidla č. 1.</span><span class="sxs-lookup"><span data-stu-id="4ac97-206">Violation of Rule #1.</span></span> <span data-ttu-id="4ac97-207">Čas a poplatky za projekt P1 jsou zahrnuty v obou řádcích nabídky ŘN1 a ŘN2.</span><span class="sxs-lookup"><span data-stu-id="4ac97-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ac97-208">P1</span><span class="sxs-lookup"><span data-stu-id="4ac97-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ac97-209">Č1</span><span class="sxs-lookup"><span data-stu-id="4ac97-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-210">ŘN2</span><span class="sxs-lookup"><span data-stu-id="4ac97-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-211">O1</span><span class="sxs-lookup"><span data-stu-id="4ac97-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-212">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-213">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-214">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-214">Yes</span></span> </p>
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
<span data-ttu-id="4ac97-215">P1</span><span class="sxs-lookup"><span data-stu-id="4ac97-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ac97-216">Č1</span><span class="sxs-lookup"><span data-stu-id="4ac97-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-217">ŘN1</span><span class="sxs-lookup"><span data-stu-id="4ac97-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-218">O1</span><span class="sxs-lookup"><span data-stu-id="4ac97-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-219">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-220">No</span><span class="sxs-lookup"><span data-stu-id="4ac97-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-221">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ac97-222">Platná</span><span class="sxs-lookup"><span data-stu-id="4ac97-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="4ac97-223">Čas a poplatky za projekt P1 jsou zahrnuty v ŘN1.</span><span class="sxs-lookup"><span data-stu-id="4ac97-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="4ac97-224">Výdaje na projekt P1 jsou zahrnuty do ŘN2.</span><span class="sxs-lookup"><span data-stu-id="4ac97-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="4ac97-225">Neexistuje žádné překrývání položek zahrnutých v každém řádku nabídky, takže je platná.</span><span class="sxs-lookup"><span data-stu-id="4ac97-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ac97-226">P1</span><span class="sxs-lookup"><span data-stu-id="4ac97-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ac97-227">Č1</span><span class="sxs-lookup"><span data-stu-id="4ac97-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-228">ŘN2</span><span class="sxs-lookup"><span data-stu-id="4ac97-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-229">O1</span><span class="sxs-lookup"><span data-stu-id="4ac97-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-230">No</span><span class="sxs-lookup"><span data-stu-id="4ac97-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-231">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-232">No</span><span class="sxs-lookup"><span data-stu-id="4ac97-232">No</span></span> </p>
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
<span data-ttu-id="4ac97-233">P1</span><span class="sxs-lookup"><span data-stu-id="4ac97-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ac97-234">Č1</span><span class="sxs-lookup"><span data-stu-id="4ac97-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-235">ŘN1</span><span class="sxs-lookup"><span data-stu-id="4ac97-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-236">O1</span><span class="sxs-lookup"><span data-stu-id="4ac97-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-237">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-238">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-239">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ac97-240">Neplatný</span><span class="sxs-lookup"><span data-stu-id="4ac97-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ac97-241">Porušení výše uvedeného pravidla č. 1.</span><span class="sxs-lookup"><span data-stu-id="4ac97-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="4ac97-242">Nabídka N1 zahrnuje čas, výdaje a poplatky za celý projekt P1.</span><span class="sxs-lookup"><span data-stu-id="4ac97-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="4ac97-243">ŘN2 zahrnuje čas, výdaje a poplatky za celý projekt P1 a překrývá se s tím, co je zahrnuto v N1.</span><span class="sxs-lookup"><span data-stu-id="4ac97-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ac97-244">P1</span><span class="sxs-lookup"><span data-stu-id="4ac97-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ac97-245">Č1</span><span class="sxs-lookup"><span data-stu-id="4ac97-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-246">ŘN2</span><span class="sxs-lookup"><span data-stu-id="4ac97-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-247">O1</span><span class="sxs-lookup"><span data-stu-id="4ac97-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-248">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-249">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-250">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-250">Yes</span></span> </p>
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
<span data-ttu-id="4ac97-251">P1</span><span class="sxs-lookup"><span data-stu-id="4ac97-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ac97-252">Č1</span><span class="sxs-lookup"><span data-stu-id="4ac97-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-253">ŘN1</span><span class="sxs-lookup"><span data-stu-id="4ac97-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-254">O1</span><span class="sxs-lookup"><span data-stu-id="4ac97-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-255">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-256">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-257">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="4ac97-258">Platná</span><span class="sxs-lookup"><span data-stu-id="4ac97-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ac97-259">Na základě pravidla č. 2 jsou N1 a N2 dvě nabídky u stejné příležitosti, takže mohou obě odhadovat položky pro stejné součásti projektu.</span><span class="sxs-lookup"><span data-stu-id="4ac97-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ac97-260">P1</span><span class="sxs-lookup"><span data-stu-id="4ac97-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ac97-261">Č2</span><span class="sxs-lookup"><span data-stu-id="4ac97-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-262">ŘN1 v N2</span><span class="sxs-lookup"><span data-stu-id="4ac97-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-263">O1</span><span class="sxs-lookup"><span data-stu-id="4ac97-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-264">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-265">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-266">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-266">Yes</span></span> </p>
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
<span data-ttu-id="4ac97-267">P1</span><span class="sxs-lookup"><span data-stu-id="4ac97-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ac97-268">Č1</span><span class="sxs-lookup"><span data-stu-id="4ac97-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-269">ŘN1</span><span class="sxs-lookup"><span data-stu-id="4ac97-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-270">O1</span><span class="sxs-lookup"><span data-stu-id="4ac97-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-271">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-272">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-273">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="4ac97-274">Platná</span><span class="sxs-lookup"><span data-stu-id="4ac97-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ac97-275">Na základě pravidla č. 3 jsou N1 a N2 dvě nabídky u různých příležitostí, takže nemohou odhadovat položky pro stejné součásti stejného projektu.</span><span class="sxs-lookup"><span data-stu-id="4ac97-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ac97-276">P2</span><span class="sxs-lookup"><span data-stu-id="4ac97-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ac97-277">Č1</span><span class="sxs-lookup"><span data-stu-id="4ac97-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-278">ŘN1</span><span class="sxs-lookup"><span data-stu-id="4ac97-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-279">O1</span><span class="sxs-lookup"><span data-stu-id="4ac97-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-280">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ac97-281">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ac97-282">Ano</span><span class="sxs-lookup"><span data-stu-id="4ac97-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="4ac97-283">Neplatný</span><span class="sxs-lookup"><span data-stu-id="4ac97-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

