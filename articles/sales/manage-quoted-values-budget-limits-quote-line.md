---
title: Přehled řádků nabídky projektu
description: Tento téma poskytuje informace o tom, jak používat řádky nabídky projektu pro práci projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa48a90c275eae1b0c0dbce685ae718dd9674c88
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858015"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="1a64e-103">Přehled řádků nabídky projektu</span><span class="sxs-lookup"><span data-stu-id="1a64e-103">Project quote lines overview</span></span>

<span data-ttu-id="1a64e-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="1a64e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1a64e-105">Řádky nabídek založených na projektu jsou navrženy tak, aby pomohly odhadnout projektovou práci na zakázce.</span><span class="sxs-lookup"><span data-stu-id="1a64e-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="1a64e-106">Struktura řádku nabídky založené na projektu se rozšiřuje u odhadů projektu o následující koncepty:</span><span class="sxs-lookup"><span data-stu-id="1a64e-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="1a64e-107">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="1a64e-107">Billing Method</span></span>
- <span data-ttu-id="1a64e-108">Mapování projektu</span><span class="sxs-lookup"><span data-stu-id="1a64e-108">Project Mapping</span></span>
- <span data-ttu-id="1a64e-109">Zahrnuté třídy transakcí</span><span class="sxs-lookup"><span data-stu-id="1a64e-109">Included Transaction classes</span></span>
- <span data-ttu-id="1a64e-110">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="1a64e-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="1a64e-111">Nastavení účtovatelnosti</span><span class="sxs-lookup"><span data-stu-id="1a64e-111">Chargeability setup</span></span>
- <span data-ttu-id="1a64e-112">Odhad pomocí podrobností řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="1a64e-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="1a64e-113">Zákazníci řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="1a64e-113">Quote line Customers</span></span>

<span data-ttu-id="1a64e-114">Následující tabulka poskytuje informace o polích na karrtě **Všeobecné** řádku nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="1a64e-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="1a64e-115">Tato pole pomáhají připravit základ pro podrobný počáteční odhad projektové práce.</span><span class="sxs-lookup"><span data-stu-id="1a64e-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="1a64e-116">**Pole**</span><span class="sxs-lookup"><span data-stu-id="1a64e-116">**Field**</span></span> | <span data-ttu-id="1a64e-117">**Popis**</span><span class="sxs-lookup"><span data-stu-id="1a64e-117">**Description**</span></span> | <span data-ttu-id="1a64e-118">**Dopad na příjem dat**</span><span class="sxs-lookup"><span data-stu-id="1a64e-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1a64e-119">Jméno</span><span class="sxs-lookup"><span data-stu-id="1a64e-119">Name</span></span> | <span data-ttu-id="1a64e-120">Název řádku nabídky, který by vám měl pomoci identifikovat diskrétní součást nabídky, která se odhaduje.</span><span class="sxs-lookup"><span data-stu-id="1a64e-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="1a64e-121">Zkopírováno do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="1a64e-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a64e-122">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="1a64e-122">Billing Method</span></span> | <span data-ttu-id="1a64e-123">U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z příslušného pole na řádku příležitosti.</span><span class="sxs-lookup"><span data-stu-id="1a64e-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="1a64e-124">Toto pole zahrnuje dva hlavní smluvní modely podporované Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="1a64e-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="1a64e-125">- Pevná cena</span><span class="sxs-lookup"><span data-stu-id="1a64e-125">- Fixed price</span></span></br><span data-ttu-id="1a64e-126">- Čas a materiál.</span><span class="sxs-lookup"><span data-stu-id="1a64e-126">- Time and material.</span></span>| <span data-ttu-id="1a64e-127">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="1a64e-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a64e-128">Project</span><span class="sxs-lookup"><span data-stu-id="1a64e-128">Project</span></span> | <span data-ttu-id="1a64e-129">Pomocí tohoto volitelného pole můžete identifikovat projekt, který bude použit k provedení práce na této zakázce.</span><span class="sxs-lookup"><span data-stu-id="1a64e-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="1a64e-130">Když je projekt mapován na řádek nabídky, pomáhá to při nastavení zpoplatněných úkolů a také při stanovení odhadu založeného na projektu do řádku nabídky jako podrobnosti řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a64e-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="1a64e-131">Pokud projekt není mapován na řádek nabídky založené na projektu, odhad by měl být vytvořen ručně – vytvořením každé podrobnosti řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a64e-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="1a64e-132">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="1a64e-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a64e-133">Zahrnout čas</span><span class="sxs-lookup"><span data-stu-id="1a64e-133">Include Time</span></span> | <span data-ttu-id="1a64e-134">Příznak **Ano**/**Ne** určuje, zda budou časové transakce nebo náklady práce ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a64e-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a64e-135">Hodnota **Ne** určuje, že časové transakce nebo náklady práce nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a64e-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a64e-136">Hodnota **Ano** určuje, že časové transakce nebo náklady práce budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a64e-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1a64e-137">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="1a64e-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a64e-138">Zahrnout výdaj</span><span class="sxs-lookup"><span data-stu-id="1a64e-138">Include Expense</span></span> | <span data-ttu-id="1a64e-139">Příznak **Ano**/**Ne** určuje, zda budou výdajové náklady ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a64e-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a64e-140">Hodnota **Ne** určuje, že výdajové náklady nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a64e-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a64e-141">Hodnota **Ano** určuje, že výdajové náklady budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a64e-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1a64e-142">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="1a64e-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a64e-143">Zahrnout poplatek</span><span class="sxs-lookup"><span data-stu-id="1a64e-143">Include Fee</span></span> | <span data-ttu-id="1a64e-144">Příznak **Ano**/**Ne** určuje, zda budou poplatky ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a64e-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a64e-145">Hodnota **Ne** určuje, že poplatky nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a64e-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1a64e-146">Hodnota **Ano** určuje, že poplatky budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a64e-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1a64e-147">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="1a64e-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a64e-148">Nabízená částka</span><span class="sxs-lookup"><span data-stu-id="1a64e-148">Quoted Amount</span></span> | <span data-ttu-id="1a64e-149">Jedná se o částku, která bude zákazníkovi nabídnuta za veškerou práci předpovídanou v tomto řádku projektové nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a64e-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="1a64e-150">U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z pole **Rozpočet zákazníka** na řádku příležitosti.</span><span class="sxs-lookup"><span data-stu-id="1a64e-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="1a64e-151">Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky na podrobnostech řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a64e-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="1a64e-152">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="1a64e-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a64e-153">Odhad daně</span><span class="sxs-lookup"><span data-stu-id="1a64e-153">Estimated Tax</span></span> | <span data-ttu-id="1a64e-154">Toto je upravitelné pole, kde může uživatel přidat odhadovanou částku daně do řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a64e-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="1a64e-155">Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky daně na podrobnostech řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="1a64e-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="1a64e-156">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="1a64e-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a64e-157">Nabízená částka včetně daně</span><span class="sxs-lookup"><span data-stu-id="1a64e-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="1a64e-158">Toto pole představuje částku nabídky po zdanění a je pouze ke čtení.</span><span class="sxs-lookup"><span data-stu-id="1a64e-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="1a64e-159">Částka v tomto poli se počítá jako *Nabízená částka + daň*.</span><span class="sxs-lookup"><span data-stu-id="1a64e-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="1a64e-160">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="1a64e-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a64e-161">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="1a64e-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="1a64e-162">Toto pole je upravitelné a je k dispozici pouze na řádcích nabídek založených na projektu, které mají nastaven způsob fakturace **Čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="1a64e-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="1a64e-163">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="1a64e-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1a64e-164">Rozpočet zákazníka</span><span class="sxs-lookup"><span data-stu-id="1a64e-164">Customer Budget</span></span> | <span data-ttu-id="1a64e-165">Toto pole je upravitelné a jeho hodnota se zkopíruje z příslušného pole na řádku příležitosti, když je nabídka vytvořena z příležitosti.</span><span class="sxs-lookup"><span data-stu-id="1a64e-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="1a64e-166">Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="1a64e-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="1a64e-167">Pravidla ověření pro pole na kartě Všeobecné řádků nabídek založených na projektu</span><span class="sxs-lookup"><span data-stu-id="1a64e-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="1a64e-168">**Pravidlo 1** : Určitou třídu transakcí ve vybraném projektu lze zahrnout pouze do jednoho řádku nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="1a64e-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="1a64e-169">**Pravidlo 2** : Pokud má příležitost více nabídek, mohou existovat řádky nabídky z různých nabídek, které všechny odkazují na stejný projekt a zahrnují stejnou třídu transakcí.</span><span class="sxs-lookup"><span data-stu-id="1a64e-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="1a64e-170">**Pravidlo 3** : Pokud nabídky nepatří ke stejné příležitosti, nemohou zahrnovat stejný projekt a třídu transakcí.</span><span class="sxs-lookup"><span data-stu-id="1a64e-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="1a64e-171">
                    <strong>Příležitost</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a64e-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="1a64e-172">
                    <strong>Nabídka</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a64e-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1a64e-173">
                    <strong>Řádek nabídky</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a64e-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1a64e-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a64e-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="1a64e-175">
                    <strong>Zahrnout čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a64e-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="1a64e-176">
                    <strong>Zahrnout výdaj</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a64e-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1a64e-177">
                    <strong>Zahrnout</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a64e-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="1a64e-178">
                    <strong>poplatek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a64e-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="1a64e-179">
                    <strong>Platné / Neplatné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a64e-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="1a64e-180">
                    <strong>Důvod</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a64e-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a64e-181">P1</span><span class="sxs-lookup"><span data-stu-id="1a64e-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a64e-182">Č1</span><span class="sxs-lookup"><span data-stu-id="1a64e-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-183">ŘN1</span><span class="sxs-lookup"><span data-stu-id="1a64e-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-184">O1</span><span class="sxs-lookup"><span data-stu-id="1a64e-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-185">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-186">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-187">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a64e-188">Neplatný</span><span class="sxs-lookup"><span data-stu-id="1a64e-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a64e-189">Porušení pravidla č. 1.</span><span class="sxs-lookup"><span data-stu-id="1a64e-189">Violation of Rule #1.</span></span> <span data-ttu-id="1a64e-190">Čas, náklady a poplatky za projekt P1 jsou zahrnuty v obou řádcích nabídky ŘN1 a ŘN2.</span><span class="sxs-lookup"><span data-stu-id="1a64e-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a64e-191">P1</span><span class="sxs-lookup"><span data-stu-id="1a64e-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a64e-192">Č1</span><span class="sxs-lookup"><span data-stu-id="1a64e-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-193">ŘN2</span><span class="sxs-lookup"><span data-stu-id="1a64e-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-194">O1</span><span class="sxs-lookup"><span data-stu-id="1a64e-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-195">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-196">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-197">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-197">Yes</span></span> </p>
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
<span data-ttu-id="1a64e-198">P1</span><span class="sxs-lookup"><span data-stu-id="1a64e-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a64e-199">Č1</span><span class="sxs-lookup"><span data-stu-id="1a64e-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-200">ŘN1</span><span class="sxs-lookup"><span data-stu-id="1a64e-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-201">O1</span><span class="sxs-lookup"><span data-stu-id="1a64e-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-202">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-203">No</span><span class="sxs-lookup"><span data-stu-id="1a64e-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-204">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a64e-205">Neplatný</span><span class="sxs-lookup"><span data-stu-id="1a64e-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a64e-206">Porušení pravidla č. 1.</span><span class="sxs-lookup"><span data-stu-id="1a64e-206">Violation of Rule #1.</span></span> <span data-ttu-id="1a64e-207">Čas a poplatky za projekt P1 jsou zahrnuty v obou řádcích nabídky ŘN1 a ŘN2.</span><span class="sxs-lookup"><span data-stu-id="1a64e-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a64e-208">P1</span><span class="sxs-lookup"><span data-stu-id="1a64e-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a64e-209">Č1</span><span class="sxs-lookup"><span data-stu-id="1a64e-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-210">ŘN2</span><span class="sxs-lookup"><span data-stu-id="1a64e-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-211">O1</span><span class="sxs-lookup"><span data-stu-id="1a64e-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-212">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-213">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-214">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-214">Yes</span></span> </p>
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
<span data-ttu-id="1a64e-215">P1</span><span class="sxs-lookup"><span data-stu-id="1a64e-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a64e-216">Č1</span><span class="sxs-lookup"><span data-stu-id="1a64e-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-217">ŘN1</span><span class="sxs-lookup"><span data-stu-id="1a64e-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-218">O1</span><span class="sxs-lookup"><span data-stu-id="1a64e-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-219">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-220">No</span><span class="sxs-lookup"><span data-stu-id="1a64e-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-221">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a64e-222">Platná</span><span class="sxs-lookup"><span data-stu-id="1a64e-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="1a64e-223">Čas a poplatky za projekt P1 jsou zahrnuty v ŘN1.</span><span class="sxs-lookup"><span data-stu-id="1a64e-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="1a64e-224">Výdaje na projekt P1 jsou zahrnuty do ŘN2.</span><span class="sxs-lookup"><span data-stu-id="1a64e-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="1a64e-225">Neexistuje žádné překrývání položek zahrnutých v každém řádku nabídky, takže je platná.</span><span class="sxs-lookup"><span data-stu-id="1a64e-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a64e-226">P1</span><span class="sxs-lookup"><span data-stu-id="1a64e-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a64e-227">Č1</span><span class="sxs-lookup"><span data-stu-id="1a64e-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-228">ŘN2</span><span class="sxs-lookup"><span data-stu-id="1a64e-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-229">O1</span><span class="sxs-lookup"><span data-stu-id="1a64e-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-230">No</span><span class="sxs-lookup"><span data-stu-id="1a64e-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-231">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-232">No</span><span class="sxs-lookup"><span data-stu-id="1a64e-232">No</span></span> </p>
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
<span data-ttu-id="1a64e-233">P1</span><span class="sxs-lookup"><span data-stu-id="1a64e-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a64e-234">Č1</span><span class="sxs-lookup"><span data-stu-id="1a64e-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-235">ŘN1</span><span class="sxs-lookup"><span data-stu-id="1a64e-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-236">O1</span><span class="sxs-lookup"><span data-stu-id="1a64e-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-237">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-238">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-239">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a64e-240">Neplatný</span><span class="sxs-lookup"><span data-stu-id="1a64e-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a64e-241">Porušení výše uvedeného pravidla č. 1.</span><span class="sxs-lookup"><span data-stu-id="1a64e-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="1a64e-242">Nabídka N1 zahrnuje čas, výdaje a poplatky za celý projekt P1.</span><span class="sxs-lookup"><span data-stu-id="1a64e-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="1a64e-243">ŘN2 zahrnuje čas, výdaje a poplatky za celý projekt P1 a překrývá se s tím, co je zahrnuto v N1.</span><span class="sxs-lookup"><span data-stu-id="1a64e-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a64e-244">P1</span><span class="sxs-lookup"><span data-stu-id="1a64e-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a64e-245">Č1</span><span class="sxs-lookup"><span data-stu-id="1a64e-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-246">ŘN2</span><span class="sxs-lookup"><span data-stu-id="1a64e-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-247">O1</span><span class="sxs-lookup"><span data-stu-id="1a64e-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-248">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-249">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-250">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-250">Yes</span></span> </p>
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
<span data-ttu-id="1a64e-251">P1</span><span class="sxs-lookup"><span data-stu-id="1a64e-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a64e-252">Č1</span><span class="sxs-lookup"><span data-stu-id="1a64e-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-253">ŘN1</span><span class="sxs-lookup"><span data-stu-id="1a64e-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-254">O1</span><span class="sxs-lookup"><span data-stu-id="1a64e-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-255">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-256">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-257">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="1a64e-258">Platná</span><span class="sxs-lookup"><span data-stu-id="1a64e-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a64e-259">Na základě pravidla č. 2 jsou N1 a N2 dvě nabídky u stejné příležitosti, takže mohou obě odhadovat položky pro stejné součásti projektu.</span><span class="sxs-lookup"><span data-stu-id="1a64e-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a64e-260">P1</span><span class="sxs-lookup"><span data-stu-id="1a64e-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a64e-261">Č2</span><span class="sxs-lookup"><span data-stu-id="1a64e-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-262">ŘN1 v N2</span><span class="sxs-lookup"><span data-stu-id="1a64e-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-263">O1</span><span class="sxs-lookup"><span data-stu-id="1a64e-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-264">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-265">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-266">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-266">Yes</span></span> </p>
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
<span data-ttu-id="1a64e-267">P1</span><span class="sxs-lookup"><span data-stu-id="1a64e-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a64e-268">Č1</span><span class="sxs-lookup"><span data-stu-id="1a64e-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-269">ŘN1</span><span class="sxs-lookup"><span data-stu-id="1a64e-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-270">O1</span><span class="sxs-lookup"><span data-stu-id="1a64e-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-271">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-272">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-273">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="1a64e-274">Platná</span><span class="sxs-lookup"><span data-stu-id="1a64e-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1a64e-275">Na základě pravidla č. 3 jsou N1 a N2 dvě nabídky u různých příležitostí, takže nemohou odhadovat položky pro stejné součásti stejného projektu.</span><span class="sxs-lookup"><span data-stu-id="1a64e-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1a64e-276">P2</span><span class="sxs-lookup"><span data-stu-id="1a64e-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1a64e-277">Č1</span><span class="sxs-lookup"><span data-stu-id="1a64e-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-278">ŘN1</span><span class="sxs-lookup"><span data-stu-id="1a64e-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-279">O1</span><span class="sxs-lookup"><span data-stu-id="1a64e-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-280">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1a64e-281">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1a64e-282">Ano</span><span class="sxs-lookup"><span data-stu-id="1a64e-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="1a64e-283">Neplatný</span><span class="sxs-lookup"><span data-stu-id="1a64e-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
