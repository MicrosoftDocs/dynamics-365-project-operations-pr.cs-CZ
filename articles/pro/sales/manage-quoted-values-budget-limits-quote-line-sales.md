---
title: Přehled řádků nabídky založené na projektu
description: Toto téma poskytuje informace o používání řádků nabídek založených na projektu pro práci na projektu.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cfe98fc89130c93dd0a36af8583881fdcb4550c0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858690"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="9b154-103">Přehled řádků nabídky založené na projektu</span><span class="sxs-lookup"><span data-stu-id="9b154-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="9b154-104">_**Platí pro:** omezené nasazení – dohoda o pro forma fakturaci, Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="9b154-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9b154-105">Řádky nabídek založených na projektu jsou navrženy tak, aby pomohly odhadnout projektovou práci na zakázce.</span><span class="sxs-lookup"><span data-stu-id="9b154-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="9b154-106">Struktura řádku nabídky založené na projektu se rozšiřuje u odhadů projektu o následující koncepty:</span><span class="sxs-lookup"><span data-stu-id="9b154-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="9b154-107">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="9b154-107">Billing Method</span></span>
- <span data-ttu-id="9b154-108">Projekt a mapování úkolů</span><span class="sxs-lookup"><span data-stu-id="9b154-108">Project and Task Mapping</span></span>
- <span data-ttu-id="9b154-109">Zahrnuté třídy transakcí</span><span class="sxs-lookup"><span data-stu-id="9b154-109">Included Transaction classes</span></span>
- <span data-ttu-id="9b154-110">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="9b154-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="9b154-111">Nastavení účtovatelnosti</span><span class="sxs-lookup"><span data-stu-id="9b154-111">Chargeability setup</span></span>
- <span data-ttu-id="9b154-112">Odhad pomocí podrobností řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="9b154-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="9b154-113">Zákazníci řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="9b154-113">Quote line Customers</span></span>

<span data-ttu-id="9b154-114">Následující tabulka poskytuje informace o polích na karrtě **Všeobecné** řádku nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="9b154-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="9b154-115">Tato pole pomáhají připravit základ pro podrobný počáteční odhad projektové práce.</span><span class="sxs-lookup"><span data-stu-id="9b154-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="9b154-116">**Pole**</span><span class="sxs-lookup"><span data-stu-id="9b154-116">**Field**</span></span> | <span data-ttu-id="9b154-117">**Popis**</span><span class="sxs-lookup"><span data-stu-id="9b154-117">**Description**</span></span> | <span data-ttu-id="9b154-118">**Dopad na příjem dat**</span><span class="sxs-lookup"><span data-stu-id="9b154-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9b154-119">Jméno</span><span class="sxs-lookup"><span data-stu-id="9b154-119">Name</span></span> | <span data-ttu-id="9b154-120">Název řádku nabídky, který vám pomůže identifikovat diskrétní složku nabídky, která se odhaduje.</span><span class="sxs-lookup"><span data-stu-id="9b154-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="9b154-121">Zkopírováno do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána.</span><span class="sxs-lookup"><span data-stu-id="9b154-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="9b154-122">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="9b154-122">Billing Method</span></span> | <span data-ttu-id="9b154-123">U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z příslušného pole na řádku příležitosti.</span><span class="sxs-lookup"><span data-stu-id="9b154-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="9b154-124">Toto pole zahrnuje dva hlavní smluvní modely podporované Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="9b154-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="9b154-125">- Pevná cena</span><span class="sxs-lookup"><span data-stu-id="9b154-125">- Fixed price</span></span></br><span data-ttu-id="9b154-126">- Čas a materiál.</span><span class="sxs-lookup"><span data-stu-id="9b154-126">- Time and material.</span></span>| <span data-ttu-id="9b154-127">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="9b154-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="9b154-128">Project</span><span class="sxs-lookup"><span data-stu-id="9b154-128">Project</span></span> | <span data-ttu-id="9b154-129">Pomocí tohoto volitelného pole můžete identifikovat projekt, který bude použit k provedení práce na této zakázce.</span><span class="sxs-lookup"><span data-stu-id="9b154-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="9b154-130">Když je projekt mapován na řádek nabídky, pomáhá to při nastavení zpoplatněných úkolů a také při stanovení odhadu založeného na projektu do řádku nabídky jako podrobnosti řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="9b154-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="9b154-131">Pokud projekt není mapován na řádek nabídky založené na projektu, odhad by měl být vytvořen ručně – vytvořením každé podrobnosti řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="9b154-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="9b154-132">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="9b154-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="9b154-133">Zahrnuté úkoly</span><span class="sxs-lookup"><span data-stu-id="9b154-133">Included Tasks</span></span> | <span data-ttu-id="9b154-134">Udává, zda je tento řádek nabídky použit pro všechny nebo jen některé úkoly vybraného projektu.</span><span class="sxs-lookup"><span data-stu-id="9b154-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="9b154-135">Toto pole může obsahovat následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="9b154-135">This field has the following possible values:</span></span></br><span data-ttu-id="9b154-136">- Všechny projektové úkoly</span><span class="sxs-lookup"><span data-stu-id="9b154-136">- All project tasks</span></span></br><span data-ttu-id="9b154-137">- Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="9b154-137">- Selected project tasks only</span></span></br><span data-ttu-id="9b154-138">Prázdná hodnota v tomto poli odpovídá možnosti **Všechny úkoly projektu**.</span><span class="sxs-lookup"><span data-stu-id="9b154-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="9b154-139">Když je na stránce projektu vybráno **Pouze vybrané úkoly projektu**, karta **Nastavení fakturace úkolu** umožňuje vybrat konkrétní úkoly a přidružit je k tomuto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="9b154-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="9b154-140">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="9b154-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="9b154-141">Zahrnout čas</span><span class="sxs-lookup"><span data-stu-id="9b154-141">Include Time</span></span> | <span data-ttu-id="9b154-142">Hodnota **Ano**/**Ne** označuje, zda budou do odhadu na tomto řádku nabídky zahrnuty časové transakce nebo náklady práce na vybraném projektu.</span><span class="sxs-lookup"><span data-stu-id="9b154-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="9b154-143">Hodnota **Ne** určuje, že časové transakce nebo náklady práce nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="9b154-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="9b154-144">Hodnota **Ano** určuje, že časové transakce nebo náklady práce budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="9b154-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="9b154-145">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="9b154-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="9b154-146">Zahrnout výdaj</span><span class="sxs-lookup"><span data-stu-id="9b154-146">Include Expense</span></span> | <span data-ttu-id="9b154-147">Hodnota **Ano**/**Ne** označuje, zda budou do odhadu na tomto řádku nabídky zahrnuty náklady výdajů na vybraném projektu.</span><span class="sxs-lookup"><span data-stu-id="9b154-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="9b154-148">Hodnota **Ne** určuje, že výdajové náklady nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="9b154-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="9b154-149">Hodnota **Ano** určuje, že výdajové náklady budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="9b154-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="9b154-150">Tato hodnota je překopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="9b154-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="9b154-151">Zahrnout materiál</span><span class="sxs-lookup"><span data-stu-id="9b154-151">Include Material</span></span> | <span data-ttu-id="9b154-152">Hodnota **Ano**/**Ne** označuje, zda budou do odhadu na tomto řádku nabídky zahrnuty náklady na materiál na vybraném projektu.</span><span class="sxs-lookup"><span data-stu-id="9b154-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="9b154-153">Hodnota **Ne** označuje, že nebudou do odhadu na tomto řádku nabídky zahrnuty náklady na materiál.</span><span class="sxs-lookup"><span data-stu-id="9b154-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="9b154-154">Hodnota **Ano** označuje, že budou do odhadu na tomto řádku nabídky zahrnuty náklady na materiál.</span><span class="sxs-lookup"><span data-stu-id="9b154-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="9b154-155">Tato hodnota je překopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="9b154-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="9b154-156">Zahrnout poplatek</span><span class="sxs-lookup"><span data-stu-id="9b154-156">Include Fee</span></span> | <span data-ttu-id="9b154-157">Hodnota **Ano**/**Ne** označuje, zda budou do odhadu na tomto řádku nabídky zahrnuty poplatky na vybraném projektu.</span><span class="sxs-lookup"><span data-stu-id="9b154-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="9b154-158">Hodnota **Ne** určuje, že poplatky nebudou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="9b154-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="9b154-159">Hodnota **Ano** určuje, že poplatky budou zahrnuty do odhadu na tomto řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="9b154-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="9b154-160">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="9b154-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="9b154-161">Nabízená částka</span><span class="sxs-lookup"><span data-stu-id="9b154-161">Quoted Amount</span></span> | <span data-ttu-id="9b154-162">Jedná se o částku, která bude zákazníkovi nabídnuta za veškerou práci předpovídanou v tomto řádku nabídky projektu.</span><span class="sxs-lookup"><span data-stu-id="9b154-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="9b154-163">U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z pole **Rozpočet zákazníka** na řádku příležitosti.</span><span class="sxs-lookup"><span data-stu-id="9b154-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="9b154-164">Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky na podrobnostech řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="9b154-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="9b154-165">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="9b154-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="9b154-166">Odhad daně</span><span class="sxs-lookup"><span data-stu-id="9b154-166">Estimated Tax</span></span> | <span data-ttu-id="9b154-167">Toto je upravitelné pole, kde může uživatel přidat odhadovanou částku daně do řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="9b154-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="9b154-168">Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky daně na podrobnostech řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="9b154-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="9b154-169">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="9b154-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="9b154-170">Nabízená částka včetně daně</span><span class="sxs-lookup"><span data-stu-id="9b154-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="9b154-171">Toto pole představuje částku nabídky po zdanění a je pouze ke čtení.</span><span class="sxs-lookup"><span data-stu-id="9b154-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="9b154-172">Částka v tomto poli se počítá jako *Nabízená částka + daň*.</span><span class="sxs-lookup"><span data-stu-id="9b154-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="9b154-173">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="9b154-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="9b154-174">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="9b154-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="9b154-175">Toto pole je upravitelné a je k dispozici pouze na řádcích nabídek založených na projektu, které mají nastaven způsob fakturace **Čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="9b154-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="9b154-176">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="9b154-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="9b154-177">Rozpočet zákazníka</span><span class="sxs-lookup"><span data-stu-id="9b154-177">Customer Budget</span></span> | <span data-ttu-id="9b154-178">Toto pole je upravitelné a jeho hodnota se zkopíruje z příslušného pole na řádku příležitosti, když je nabídka vytvořena z příležitosti.</span><span class="sxs-lookup"><span data-stu-id="9b154-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="9b154-179">Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.</span><span class="sxs-lookup"><span data-stu-id="9b154-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="9b154-180">Pravidla ověření pro pole na kartě Všeobecné řádků nabídek založených na projektu</span><span class="sxs-lookup"><span data-stu-id="9b154-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="9b154-181">**Pravidlo 1** : Pokud je pole **Zahrnuté úkoly** prázdné nebo je-li nastaveno na hodnotu **Všechny úkoly projektu**, je projekt zahrnut do řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="9b154-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="9b154-182">**Pravidlo 2** : Pokud je pole **Zahrnuté úkoly** prázdné nebo je-li nastaveno na hodnotu **Všechny úkoly projektu**, lze projekt a určitou třídu transakcí zahrnout pouze na jeden řádek nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="9b154-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="9b154-183">**Pravidlo 3**: Pokud je pole **Zahrnuté úkoly** prázdné nebo je-li nastaveno na hodnotu **Pouze vybrané úkoly projektu**, lze projekt a určitou třídu transakcí zahrnout do více řádků nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="9b154-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="9b154-184">**Pravidlo 4** : Pokud má příležitost více nabídek, mohou existovat řádky nabídky z různých nabídek, které všechny odkazují na stejný projekt a zahrnují stejnou třídu transakcí.</span><span class="sxs-lookup"><span data-stu-id="9b154-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="9b154-185">**Pravidlo 5** : Pokud nabídky nepatří ke stejné příležitosti, nemohou zahrnovat stejný projekt a třídu transakcí.</span><span class="sxs-lookup"><span data-stu-id="9b154-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="9b154-186">
                    <strong>Příležitost</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b154-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="9b154-187">
                    <strong>Nabídka</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b154-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="9b154-188">
                    <strong>Řádek nabídky</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b154-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="9b154-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b154-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="9b154-190">
                    <strong>Zahrnuté úkoly</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b154-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="9b154-191">
                    <strong>Zahrnout čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b154-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="9b154-192">
                    <strong>Zahrnout výdaj</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b154-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="9b154-193">
                    <strong>Zahrnout materiál</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b154-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="9b154-194">
                    <strong>Zahrnout</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b154-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="9b154-195">
                    <strong>Poplatek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b154-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="9b154-196">
                    <strong>Platné / Neplatné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b154-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="9b154-197">
                    <strong>Důvod</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9b154-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="9b154-198">P1</span><span class="sxs-lookup"><span data-stu-id="9b154-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="9b154-199">Č1</span><span class="sxs-lookup"><span data-stu-id="9b154-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="9b154-200">ŘN1</span><span class="sxs-lookup"><span data-stu-id="9b154-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-201">O1</span><span class="sxs-lookup"><span data-stu-id="9b154-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="9b154-202">prázdnou</span><span class="sxs-lookup"><span data-stu-id="9b154-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="9b154-203">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="9b154-204">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9b154-205">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-206">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b154-207">Neplatný</span><span class="sxs-lookup"><span data-stu-id="9b154-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b154-208">Porušení pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="9b154-208">Violation of Rule #2.</span></span> <span data-ttu-id="9b154-209">Čas, náklady a poplatky za projekt P1 jsou zahrnuty v řádcích nabídky ŘN1 a ŘN2</span><span class="sxs-lookup"><span data-stu-id="9b154-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="9b154-210">P1</span><span class="sxs-lookup"><span data-stu-id="9b154-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="9b154-211">Č1</span><span class="sxs-lookup"><span data-stu-id="9b154-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="9b154-212">ŘN2</span><span class="sxs-lookup"><span data-stu-id="9b154-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-213">O1</span><span class="sxs-lookup"><span data-stu-id="9b154-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="9b154-214">prázdnou</span><span class="sxs-lookup"><span data-stu-id="9b154-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="9b154-215">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="9b154-216">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9b154-217">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-218">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-218">Yes</span></span> </p>
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
<span data-ttu-id="9b154-219">P1</span><span class="sxs-lookup"><span data-stu-id="9b154-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="9b154-220">Č1</span><span class="sxs-lookup"><span data-stu-id="9b154-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="9b154-221">ŘN1</span><span class="sxs-lookup"><span data-stu-id="9b154-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-222">O1</span><span class="sxs-lookup"><span data-stu-id="9b154-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="9b154-223">prázdnou</span><span class="sxs-lookup"><span data-stu-id="9b154-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="9b154-224">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="9b154-225">No</span><span class="sxs-lookup"><span data-stu-id="9b154-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9b154-226">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-227">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b154-228">Neplatný</span><span class="sxs-lookup"><span data-stu-id="9b154-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b154-229">Porušení pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="9b154-229">Violation of Rule #2.</span></span> <span data-ttu-id="9b154-230">Čas, materiál a poplatky za projekt P1 jsou zahrnuty v řádcích nabídky ŘN1 a ŘN2</span><span class="sxs-lookup"><span data-stu-id="9b154-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="9b154-231">P1</span><span class="sxs-lookup"><span data-stu-id="9b154-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="9b154-232">Č1</span><span class="sxs-lookup"><span data-stu-id="9b154-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="9b154-233">ŘN2</span><span class="sxs-lookup"><span data-stu-id="9b154-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-234">O1</span><span class="sxs-lookup"><span data-stu-id="9b154-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="9b154-235">prázdnou</span><span class="sxs-lookup"><span data-stu-id="9b154-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="9b154-236">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="9b154-237">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9b154-238">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-239">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-239">Yes</span></span> </p>
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
<span data-ttu-id="9b154-240">P1</span><span class="sxs-lookup"><span data-stu-id="9b154-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="9b154-241">Č1</span><span class="sxs-lookup"><span data-stu-id="9b154-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="9b154-242">ŘN1</span><span class="sxs-lookup"><span data-stu-id="9b154-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-243">O1</span><span class="sxs-lookup"><span data-stu-id="9b154-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="9b154-244">prázdnou</span><span class="sxs-lookup"><span data-stu-id="9b154-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="9b154-245">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="9b154-246">No</span><span class="sxs-lookup"><span data-stu-id="9b154-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9b154-247">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-248">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b154-249">Platné</span><span class="sxs-lookup"><span data-stu-id="9b154-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b154-250">Čas, materiál a poplatky za projekt P1 jsou zahrnuty na ŘN1</span><span class="sxs-lookup"><span data-stu-id="9b154-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="9b154-251">Výdaje na projekt P1 jsou zahrnuty do ŘN2</span><span class="sxs-lookup"><span data-stu-id="9b154-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="9b154-252">Žádné překrývání toho, co je zahrnuto na každém řádku nabídky, a proto je zadání platné.</span><span class="sxs-lookup"><span data-stu-id="9b154-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="9b154-253">P1</span><span class="sxs-lookup"><span data-stu-id="9b154-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="9b154-254">Č1</span><span class="sxs-lookup"><span data-stu-id="9b154-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="9b154-255">ŘN2</span><span class="sxs-lookup"><span data-stu-id="9b154-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-256">O1</span><span class="sxs-lookup"><span data-stu-id="9b154-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="9b154-257">prázdnou</span><span class="sxs-lookup"><span data-stu-id="9b154-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="9b154-258">No</span><span class="sxs-lookup"><span data-stu-id="9b154-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="9b154-259">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9b154-260">No</span><span class="sxs-lookup"><span data-stu-id="9b154-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-261">No</span><span class="sxs-lookup"><span data-stu-id="9b154-261">No</span></span> </p>
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
<span data-ttu-id="9b154-262">P1</span><span class="sxs-lookup"><span data-stu-id="9b154-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="9b154-263">Č1</span><span class="sxs-lookup"><span data-stu-id="9b154-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="9b154-264">ŘN1</span><span class="sxs-lookup"><span data-stu-id="9b154-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-265">O1</span><span class="sxs-lookup"><span data-stu-id="9b154-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="9b154-266">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="9b154-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="9b154-267">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="9b154-268">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9b154-269">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-270">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b154-271">Neplatný</span><span class="sxs-lookup"><span data-stu-id="9b154-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b154-272">Porušení pravidla č. 2</span><span class="sxs-lookup"><span data-stu-id="9b154-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="9b154-273">S1 zahrnuje čas, materiál, výdaje a poplatky za podmnožinu úkolů v projektu P1</span><span class="sxs-lookup"><span data-stu-id="9b154-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="9b154-274">ŘN2 zahrnuje čas, výdaje a poplatky za celý projekt P1, a proto se překrývá s tím, co je zahrnuto v S1.</span><span class="sxs-lookup"><span data-stu-id="9b154-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="9b154-275">P1</span><span class="sxs-lookup"><span data-stu-id="9b154-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="9b154-276">Č1</span><span class="sxs-lookup"><span data-stu-id="9b154-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="9b154-277">ŘN2</span><span class="sxs-lookup"><span data-stu-id="9b154-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-278">O1</span><span class="sxs-lookup"><span data-stu-id="9b154-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="9b154-279">prázdnou</span><span class="sxs-lookup"><span data-stu-id="9b154-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="9b154-280">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="9b154-281">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9b154-282">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-283">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-283">Yes</span></span> </p>
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
<span data-ttu-id="9b154-284">P1</span><span class="sxs-lookup"><span data-stu-id="9b154-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="9b154-285">Č1</span><span class="sxs-lookup"><span data-stu-id="9b154-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="9b154-286">ŘN1</span><span class="sxs-lookup"><span data-stu-id="9b154-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-287">O1</span><span class="sxs-lookup"><span data-stu-id="9b154-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="9b154-288">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="9b154-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="9b154-289">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="9b154-290">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9b154-291">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-292">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b154-293">Platné</span><span class="sxs-lookup"><span data-stu-id="9b154-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b154-294">Podle pravidla č. 3</span><span class="sxs-lookup"><span data-stu-id="9b154-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="9b154-295">Č1 zahrnuje čas, materiál, výdaje a poplatky za podmnožinu úkolů v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="9b154-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="9b154-296">ŘN2 zahrnuje čas, materiál, výdaje a poplatky za podmnožinu úkolů v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="9b154-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="9b154-297">Jediná další validace je kolem podmnožiny úkolů na ŘN1, která se liší od podmnožiny úkolů na ŘN2, aby se zajistilo, že nedojde k překrývání.</span><span class="sxs-lookup"><span data-stu-id="9b154-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="9b154-298">Toto provádí systém, když jsou přidruženy úkoly.</span><span class="sxs-lookup"><span data-stu-id="9b154-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="9b154-299">P1</span><span class="sxs-lookup"><span data-stu-id="9b154-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="9b154-300">Č1</span><span class="sxs-lookup"><span data-stu-id="9b154-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="9b154-301">ŘN2</span><span class="sxs-lookup"><span data-stu-id="9b154-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-302">O1</span><span class="sxs-lookup"><span data-stu-id="9b154-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="9b154-303">Pouze vybrané úkoly projektu</span><span class="sxs-lookup"><span data-stu-id="9b154-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="9b154-304">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="9b154-305">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9b154-306">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-307">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-307">Yes</span></span> </p>
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
<span data-ttu-id="9b154-308">P1</span><span class="sxs-lookup"><span data-stu-id="9b154-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="9b154-309">Č1</span><span class="sxs-lookup"><span data-stu-id="9b154-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="9b154-310">ŘN1</span><span class="sxs-lookup"><span data-stu-id="9b154-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-311">O1</span><span class="sxs-lookup"><span data-stu-id="9b154-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="9b154-312">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="9b154-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="9b154-313">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="9b154-314">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9b154-315">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-316">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b154-317">Platné</span><span class="sxs-lookup"><span data-stu-id="9b154-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b154-318">Podle pravidla č. 5 jsou Č1 a Č2 dvě nabídky u stejné příležitosti, takže mohou obě odhadovat na stejných komponentech projektu.</span><span class="sxs-lookup"><span data-stu-id="9b154-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="9b154-319">P1</span><span class="sxs-lookup"><span data-stu-id="9b154-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="9b154-320">Č2</span><span class="sxs-lookup"><span data-stu-id="9b154-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="9b154-321">ŘN1</span><span class="sxs-lookup"><span data-stu-id="9b154-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-322">O1</span><span class="sxs-lookup"><span data-stu-id="9b154-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="9b154-323">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="9b154-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="9b154-324">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="9b154-325">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9b154-326">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-327">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-327">Yes</span></span> </p>
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
<span data-ttu-id="9b154-328">P1</span><span class="sxs-lookup"><span data-stu-id="9b154-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="9b154-329">Č1</span><span class="sxs-lookup"><span data-stu-id="9b154-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="9b154-330">ŘN1</span><span class="sxs-lookup"><span data-stu-id="9b154-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-331">O1</span><span class="sxs-lookup"><span data-stu-id="9b154-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="9b154-332">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="9b154-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="9b154-333">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="9b154-334">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9b154-335">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-336">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b154-337">Neplatný</span><span class="sxs-lookup"><span data-stu-id="9b154-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9b154-338">Podle pravidla č. 4 jsou Č1 a Č2 dvě nabídky na různé příležitosti, takže mohou obě odhadovat na stejných komponentech stejného projektu.</span><span class="sxs-lookup"><span data-stu-id="9b154-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="9b154-339">P2</span><span class="sxs-lookup"><span data-stu-id="9b154-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="9b154-340">Č1</span><span class="sxs-lookup"><span data-stu-id="9b154-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="9b154-341">ŘN1</span><span class="sxs-lookup"><span data-stu-id="9b154-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-342">O1</span><span class="sxs-lookup"><span data-stu-id="9b154-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="9b154-343">Všechny úkoly projektu nebo prázdné</span><span class="sxs-lookup"><span data-stu-id="9b154-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="9b154-344">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="9b154-345">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="9b154-346">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="9b154-347">Ano</span><span class="sxs-lookup"><span data-stu-id="9b154-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
