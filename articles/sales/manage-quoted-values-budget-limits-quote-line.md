---
title: Přehled řádků nabídky založené na projektu
description: Toto téma poskytuje informace o používání řádků nabídek založených na projektu pro práci na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea54d83b1e26d1ee3520dbfab9ba56ffd1191dc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181849"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="073d9-103">Přehled řádků nabídky založené na projektu</span><span class="sxs-lookup"><span data-stu-id="073d9-103">Project-based quote lines overview</span></span>

<span data-ttu-id="073d9-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="073d9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="073d9-105">Řádky nabídek založených na projektu jsou navrženy tak, aby pomohly odhadnout projektovou práci na zakázce.</span><span class="sxs-lookup"><span data-stu-id="073d9-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="073d9-106">Struktura řádku nabídky založené na projektu se rozšiřuje u odhadů projektu o následující koncepty:</span><span class="sxs-lookup"><span data-stu-id="073d9-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="073d9-107">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="073d9-107">Billing Method</span></span>
- <span data-ttu-id="073d9-108">Mapování projektu</span><span class="sxs-lookup"><span data-stu-id="073d9-108">Project Mapping</span></span>
- <span data-ttu-id="073d9-109">Zahrnuté třídy transakcí</span><span class="sxs-lookup"><span data-stu-id="073d9-109">Included Transaction classes</span></span>
- <span data-ttu-id="073d9-110">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="073d9-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="073d9-111">Nastavení účtovatelnosti</span><span class="sxs-lookup"><span data-stu-id="073d9-111">Chargeability setup</span></span>
- <span data-ttu-id="073d9-112">Odhad pomocí podrobností řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="073d9-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="073d9-113">Zákazníci řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="073d9-113">Quote line Customers</span></span>

<span data-ttu-id="073d9-114">Následující tabulka poskytuje informace o polích na karrtě **Všeobecné** řádku nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="073d9-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="073d9-115">Tato pole pomáhají připravit základ pro podrobný počáteční odhad projektové práce.</span><span class="sxs-lookup"><span data-stu-id="073d9-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="073d9-116">**Pole**</span><span class="sxs-lookup"><span data-stu-id="073d9-116">**Field**</span></span> | <span data-ttu-id="073d9-117">**Popis**</span><span class="sxs-lookup"><span data-stu-id="073d9-117">**Description**</span></span> | <span data-ttu-id="073d9-118">**Dopad na příjem dat**</span><span class="sxs-lookup"><span data-stu-id="073d9-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="073d9-119">Jméno</span><span class="sxs-lookup"><span data-stu-id="073d9-119">Name</span></span> | <span data-ttu-id="073d9-120">Název řádku nabídky, který by vám měl pomoci identifikovat diskrétní součást nabídky, která se odhaduje.</span><span class="sxs-lookup"><span data-stu-id="073d9-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="073d9-121">Zkopírováno do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="073d9-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="073d9-122">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="073d9-122">Billing Method</span></span> | <span data-ttu-id="073d9-123">U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z příslušného pole na řádku příležitosti.</span><span class="sxs-lookup"><span data-stu-id="073d9-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="073d9-124">Toto pole zahrnuje dva hlavní smluvní modely podporované aplikací Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="073d9-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="073d9-125">- Pevná cena</span><span class="sxs-lookup"><span data-stu-id="073d9-125">- Fixed price</span></span></br><span data-ttu-id="073d9-126">- Čas a materiál.</span><span class="sxs-lookup"><span data-stu-id="073d9-126">- Time and material.</span></span>| <span data-ttu-id="073d9-127">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="073d9-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="073d9-128">Project</span><span class="sxs-lookup"><span data-stu-id="073d9-128">Project</span></span> | <span data-ttu-id="073d9-129">Pomocí tohoto volitelného pole můžete identifikovat projekt, který bude použit k provedení práce na této zakázce.</span><span class="sxs-lookup"><span data-stu-id="073d9-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="073d9-130">Když je projekt mapován na řádek nabídky, pomáhá to při nastavení zpoplatněných úkolů a také při stanovení odhadu založeného na projektu do řádku nabídky jako podrobnosti řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="073d9-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="073d9-131">Pokud projekt není mapován na řádek nabídky založené na projektu, odhad by měl být vytvořen ručně – vytvořením každé podrobnosti řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="073d9-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="073d9-132">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="073d9-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="073d9-133">Zahrnout čas</span><span class="sxs-lookup"><span data-stu-id="073d9-133">Include Time</span></span> | <span data-ttu-id="073d9-134">Příznak **Ano**/**Ne** určuje, zda budou časové transakce nebo náklady práce ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="073d9-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="073d9-135">Hodnota **Ne** určuje, že časové transakce nebo náklady práce nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="073d9-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="073d9-136">Hodnota **Ano** určuje, že časové transakce nebo náklady práce budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="073d9-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="073d9-137">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="073d9-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="073d9-138">Zahrnout výdaj</span><span class="sxs-lookup"><span data-stu-id="073d9-138">Include Expense</span></span> | <span data-ttu-id="073d9-139">Příznak **Ano**/**Ne** určuje, zda budou výdajové náklady ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="073d9-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="073d9-140">Hodnota **Ne** určuje, že výdajové náklady nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="073d9-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="073d9-141">Hodnota **Ano** určuje, že výdajové náklady budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="073d9-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="073d9-142">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="073d9-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="073d9-143">Zahrnout poplatek</span><span class="sxs-lookup"><span data-stu-id="073d9-143">Include Fee</span></span> | <span data-ttu-id="073d9-144">Příznak **Ano**/**Ne** určuje, zda budou poplatky ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="073d9-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="073d9-145">Hodnota **Ne** určuje, že poplatky nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="073d9-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="073d9-146">Hodnota **Ano** určuje, že poplatky budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="073d9-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="073d9-147">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="073d9-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="073d9-148">Nabízená částka</span><span class="sxs-lookup"><span data-stu-id="073d9-148">Quoted Amount</span></span> | <span data-ttu-id="073d9-149">Jedná se o částku, která bude zákazníkovi nabídnuta za veškerou práci předpovídanou v tomto řádku projektové nabídky.</span><span class="sxs-lookup"><span data-stu-id="073d9-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="073d9-150">U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z pole **Rozpočet zákazníka** na řádku příležitosti.</span><span class="sxs-lookup"><span data-stu-id="073d9-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="073d9-151">Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky na podrobnostech řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="073d9-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="073d9-152">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="073d9-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="073d9-153">Odhad daně</span><span class="sxs-lookup"><span data-stu-id="073d9-153">Estimated Tax</span></span> | <span data-ttu-id="073d9-154">Toto je upravitelné pole, kde může uživatel přidat odhadovanou částku daně do řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="073d9-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="073d9-155">Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky daně na podrobnostech řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="073d9-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="073d9-156">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="073d9-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="073d9-157">Nabízená částka včetně daně</span><span class="sxs-lookup"><span data-stu-id="073d9-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="073d9-158">Toto pole představuje částku nabídky po zdanění a je pouze ke čtení.</span><span class="sxs-lookup"><span data-stu-id="073d9-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="073d9-159">Částka v tomto poli se počítá jako *Nabízená částka + daň*.</span><span class="sxs-lookup"><span data-stu-id="073d9-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="073d9-160">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="073d9-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="073d9-161">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="073d9-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="073d9-162">Toto pole je upravitelné a je k dispozici pouze na řádcích nabídek založených na projektu, které mají nastaven způsob fakturace **Čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="073d9-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="073d9-163">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="073d9-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="073d9-164">Rozpočet zákazníka</span><span class="sxs-lookup"><span data-stu-id="073d9-164">Customer Budget</span></span> | <span data-ttu-id="073d9-165">Toto pole je upravitelné a jeho hodnota se zkopíruje z příslušného pole na řádku příležitosti, když je nabídka vytvořena z příležitosti.</span><span class="sxs-lookup"><span data-stu-id="073d9-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="073d9-166">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="073d9-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="073d9-167">Pravidla ověření pro pole na kartě Všeobecné řádků nabídek založených na projektu</span><span class="sxs-lookup"><span data-stu-id="073d9-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="073d9-168">**Pravidlo 1** : Určitou třídu transakcí ve vybraném projektu lze zahrnout pouze do jednoho řádku nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="073d9-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="073d9-169">**Pravidlo 2** : Pokud má příležitost více nabídek, mohou existovat řádky nabídky z různých nabídek, které všechny odkazují na stejný projekt a zahrnují stejnou třídu transakcí.</span><span class="sxs-lookup"><span data-stu-id="073d9-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="073d9-170">**Pravidlo 3** : Pokud nabídky nepatří ke stejné příležitosti, nemohou zahrnovat stejný projekt a třídu transakcí.</span><span class="sxs-lookup"><span data-stu-id="073d9-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="073d9-171">
                    <strong>Příležitost</strong>
                </span><span class="sxs-lookup"><span data-stu-id="073d9-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="073d9-172">
                    <strong>Nabídka</strong>
                </span><span class="sxs-lookup"><span data-stu-id="073d9-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="073d9-173">
                    <strong>Řádek nabídky</strong>
                </span><span class="sxs-lookup"><span data-stu-id="073d9-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="073d9-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="073d9-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="073d9-175">
                    <strong>Zahrnout čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="073d9-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="073d9-176">
                    <strong>Zahrnout výdaj</strong>
                </span><span class="sxs-lookup"><span data-stu-id="073d9-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="073d9-177">
                    <strong>Zahrnout</strong>
                </span><span class="sxs-lookup"><span data-stu-id="073d9-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="073d9-178">
                    <strong>poplatek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="073d9-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="073d9-179">
                    <strong>Platné / Neplatné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="073d9-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="073d9-180">
                    <strong>Důvod</strong>
                </span><span class="sxs-lookup"><span data-stu-id="073d9-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="073d9-181">P1</span><span class="sxs-lookup"><span data-stu-id="073d9-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="073d9-182">Č1</span><span class="sxs-lookup"><span data-stu-id="073d9-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-183">ŘN1</span><span class="sxs-lookup"><span data-stu-id="073d9-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-184">O1</span><span class="sxs-lookup"><span data-stu-id="073d9-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-185">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-186">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-187">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="073d9-188">Neplatný</span><span class="sxs-lookup"><span data-stu-id="073d9-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="073d9-189">Porušení pravidla č. 1.</span><span class="sxs-lookup"><span data-stu-id="073d9-189">Violation of Rule #1.</span></span> <span data-ttu-id="073d9-190">Čas, náklady a poplatky za projekt P1 jsou zahrnuty v obou řádcích nabídky ŘN1 a ŘN2.</span><span class="sxs-lookup"><span data-stu-id="073d9-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="073d9-191">P1</span><span class="sxs-lookup"><span data-stu-id="073d9-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="073d9-192">Č1</span><span class="sxs-lookup"><span data-stu-id="073d9-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-193">ŘN2</span><span class="sxs-lookup"><span data-stu-id="073d9-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-194">O1</span><span class="sxs-lookup"><span data-stu-id="073d9-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-195">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-196">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-197">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-197">Yes</span></span> </p>
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
<span data-ttu-id="073d9-198">P1</span><span class="sxs-lookup"><span data-stu-id="073d9-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="073d9-199">Č1</span><span class="sxs-lookup"><span data-stu-id="073d9-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-200">ŘN1</span><span class="sxs-lookup"><span data-stu-id="073d9-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-201">O1</span><span class="sxs-lookup"><span data-stu-id="073d9-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-202">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-203">No</span><span class="sxs-lookup"><span data-stu-id="073d9-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-204">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="073d9-205">Neplatný</span><span class="sxs-lookup"><span data-stu-id="073d9-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="073d9-206">Porušení pravidla č. 1.</span><span class="sxs-lookup"><span data-stu-id="073d9-206">Violation of Rule #1.</span></span> <span data-ttu-id="073d9-207">Čas a poplatky za projekt P1 jsou zahrnuty v obou řádcích nabídky ŘN1 a ŘN2.</span><span class="sxs-lookup"><span data-stu-id="073d9-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="073d9-208">P1</span><span class="sxs-lookup"><span data-stu-id="073d9-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="073d9-209">Č1</span><span class="sxs-lookup"><span data-stu-id="073d9-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-210">ŘN2</span><span class="sxs-lookup"><span data-stu-id="073d9-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-211">O1</span><span class="sxs-lookup"><span data-stu-id="073d9-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-212">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-213">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-214">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-214">Yes</span></span> </p>
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
<span data-ttu-id="073d9-215">P1</span><span class="sxs-lookup"><span data-stu-id="073d9-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="073d9-216">Č1</span><span class="sxs-lookup"><span data-stu-id="073d9-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-217">ŘN1</span><span class="sxs-lookup"><span data-stu-id="073d9-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-218">O1</span><span class="sxs-lookup"><span data-stu-id="073d9-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-219">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-220">No</span><span class="sxs-lookup"><span data-stu-id="073d9-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-221">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="073d9-222">Platná</span><span class="sxs-lookup"><span data-stu-id="073d9-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="073d9-223">Čas a poplatky za projekt P1 jsou zahrnuty v ŘN1.</span><span class="sxs-lookup"><span data-stu-id="073d9-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="073d9-224">Výdaje na projekt P1 jsou zahrnuty do ŘN2.</span><span class="sxs-lookup"><span data-stu-id="073d9-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="073d9-225">Neexistuje žádné překrývání položek zahrnutých v každém řádku nabídky, takže je platná.</span><span class="sxs-lookup"><span data-stu-id="073d9-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="073d9-226">P1</span><span class="sxs-lookup"><span data-stu-id="073d9-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="073d9-227">Č1</span><span class="sxs-lookup"><span data-stu-id="073d9-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-228">ŘN2</span><span class="sxs-lookup"><span data-stu-id="073d9-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-229">O1</span><span class="sxs-lookup"><span data-stu-id="073d9-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-230">No</span><span class="sxs-lookup"><span data-stu-id="073d9-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-231">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-232">No</span><span class="sxs-lookup"><span data-stu-id="073d9-232">No</span></span> </p>
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
<span data-ttu-id="073d9-233">P1</span><span class="sxs-lookup"><span data-stu-id="073d9-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="073d9-234">Č1</span><span class="sxs-lookup"><span data-stu-id="073d9-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-235">ŘN1</span><span class="sxs-lookup"><span data-stu-id="073d9-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-236">O1</span><span class="sxs-lookup"><span data-stu-id="073d9-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-237">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-238">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-239">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="073d9-240">Neplatný</span><span class="sxs-lookup"><span data-stu-id="073d9-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="073d9-241">Porušení výše uvedeného pravidla č. 1.</span><span class="sxs-lookup"><span data-stu-id="073d9-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="073d9-242">Nabídka N1 zahrnuje čas, výdaje a poplatky za celý projekt P1.</span><span class="sxs-lookup"><span data-stu-id="073d9-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="073d9-243">ŘN2 zahrnuje čas, výdaje a poplatky za celý projekt P1 a překrývá se s tím, co je zahrnuto v N1.</span><span class="sxs-lookup"><span data-stu-id="073d9-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="073d9-244">P1</span><span class="sxs-lookup"><span data-stu-id="073d9-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="073d9-245">Č1</span><span class="sxs-lookup"><span data-stu-id="073d9-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-246">ŘN2</span><span class="sxs-lookup"><span data-stu-id="073d9-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-247">O1</span><span class="sxs-lookup"><span data-stu-id="073d9-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-248">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-249">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-250">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-250">Yes</span></span> </p>
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
<span data-ttu-id="073d9-251">P1</span><span class="sxs-lookup"><span data-stu-id="073d9-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="073d9-252">Č1</span><span class="sxs-lookup"><span data-stu-id="073d9-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-253">ŘN1</span><span class="sxs-lookup"><span data-stu-id="073d9-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-254">O1</span><span class="sxs-lookup"><span data-stu-id="073d9-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-255">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-256">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-257">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="073d9-258">Platná</span><span class="sxs-lookup"><span data-stu-id="073d9-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="073d9-259">Na základě pravidla č. 2 jsou N1 a N2 dvě nabídky u stejné příležitosti, takže mohou obě odhadovat položky pro stejné součásti projektu.</span><span class="sxs-lookup"><span data-stu-id="073d9-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="073d9-260">P1</span><span class="sxs-lookup"><span data-stu-id="073d9-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="073d9-261">Č2</span><span class="sxs-lookup"><span data-stu-id="073d9-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-262">ŘN1 v N2</span><span class="sxs-lookup"><span data-stu-id="073d9-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-263">O1</span><span class="sxs-lookup"><span data-stu-id="073d9-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-264">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-265">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-266">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-266">Yes</span></span> </p>
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
<span data-ttu-id="073d9-267">P1</span><span class="sxs-lookup"><span data-stu-id="073d9-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="073d9-268">Č1</span><span class="sxs-lookup"><span data-stu-id="073d9-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-269">ŘN1</span><span class="sxs-lookup"><span data-stu-id="073d9-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-270">O1</span><span class="sxs-lookup"><span data-stu-id="073d9-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-271">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-272">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-273">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="073d9-274">Platná</span><span class="sxs-lookup"><span data-stu-id="073d9-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="073d9-275">Na základě pravidla č. 3 jsou N1 a N2 dvě nabídky u různých příležitostí, takže nemohou odhadovat položky pro stejné součásti stejného projektu.</span><span class="sxs-lookup"><span data-stu-id="073d9-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="073d9-276">P2</span><span class="sxs-lookup"><span data-stu-id="073d9-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="073d9-277">Č1</span><span class="sxs-lookup"><span data-stu-id="073d9-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-278">ŘN1</span><span class="sxs-lookup"><span data-stu-id="073d9-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-279">O1</span><span class="sxs-lookup"><span data-stu-id="073d9-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-280">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="073d9-281">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="073d9-282">Ano</span><span class="sxs-lookup"><span data-stu-id="073d9-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="073d9-283">Neplatný</span><span class="sxs-lookup"><span data-stu-id="073d9-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

