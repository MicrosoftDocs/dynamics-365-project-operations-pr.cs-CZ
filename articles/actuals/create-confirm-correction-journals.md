---
title: Vytváření a potvrzení deníků oprav
description: Toto téma obsahuje informace o způsobu vytvoření a potvrzení deníku oprav..
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 855593df1ea14827f06961dda5b4becd2fa75c18
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073777"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="4b35c-103">Vytváření a potvrzení deníků oprav</span><span class="sxs-lookup"><span data-stu-id="4b35c-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="4b35c-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="4b35c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4b35c-105">Někdy může být nesprávně zadán údaj o čase nebo výdaji.</span><span class="sxs-lookup"><span data-stu-id="4b35c-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="4b35c-106">Poradce může například při vytváření časového záznamu vybrat nesprávné datum nebo při zadávání výdaje může transponovat čísla.</span><span class="sxs-lookup"><span data-stu-id="4b35c-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="4b35c-107">Pokud konzultant nemůže provést aktualizace odeslaných zadání, může správce přímo opravit záznam pro projekt.</span><span class="sxs-lookup"><span data-stu-id="4b35c-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="4b35c-108">K dokončení postupů v tomto tématu budete potřebovat oprávnění správce.</span><span class="sxs-lookup"><span data-stu-id="4b35c-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="4b35c-109">Oprava schválených časových údajů</span><span class="sxs-lookup"><span data-stu-id="4b35c-109">Correct approved time entries</span></span>     

<span data-ttu-id="4b35c-110">Chcete-li opravit jeden nebo více časových záznamů pro projekt, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="4b35c-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="4b35c-111">V oblasti **Prodej** vyberte **Transakce** a poté vyberte **Schválený čas**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-111">In the **Sales** area, select **Transactions** , and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="4b35c-112">V seznamu **Schválený čas** vyhledejte a vyberte jeden nebo více schválených časových záznamů, které chcete opravit.</span><span class="sxs-lookup"><span data-stu-id="4b35c-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="4b35c-113">Pomocí filtru můžete vyhledat související položky.</span><span class="sxs-lookup"><span data-stu-id="4b35c-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="4b35c-114">Můžete například filtrovat ID projektu a vybrat všechny schválené časové záznamy s tímto ID projektu.</span><span class="sxs-lookup"><span data-stu-id="4b35c-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="4b35c-115">Zvolte **Opravit položky**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-115">Select **Correct entries**.</span></span> <span data-ttu-id="4b35c-116">Automaticky se vytvoří nový deník oprav s přiřazeným typem **Oprava času**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="4b35c-117">Vybrané položky se přidají do deníku.</span><span class="sxs-lookup"><span data-stu-id="4b35c-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="4b35c-118">Na stránce **Nový deník** zadejte **Popis** pro svůj deník oprav a poté vyberte kartu **Opravy časových záznamů**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="4b35c-119">V části **Nové hodnoty pro časové záznamy** aktualizujte pole správnými informacemi podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="4b35c-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="4b35c-120">Například můžete změnit přiřazený projekt nebo rezervovatelný zdroj.</span><span class="sxs-lookup"><span data-stu-id="4b35c-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="4b35c-121">Vyberte **Náhled**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-121">Select **Preview**.</span></span> <span data-ttu-id="4b35c-122">V dialogovém okně vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="4b35c-123">Na kartě **Řádky deníku** můžete zobrazit seznam původních skutečných hodnot, které se vztahují k vybraným časovým záznamům, které byly stornovány, a opraveným odpovídajícím řádkům, které byly vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="4b35c-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="4b35c-124">Pokud je třeba provést další opravy, opakujte kroky 5 a 6.</span><span class="sxs-lookup"><span data-stu-id="4b35c-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="4b35c-125">Všechny opravené skutečné hodnoty budou mít stejné hodnoty, jaké jste vybrali v části **Nové hodnoty pro časové záznamy**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="4b35c-126">Pokud se opravy objeví podle očekávání, vyberte **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="4b35c-127">V dialogovém okně vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="4b35c-128">Vraťte se do části **Prodej** , vyberte **Projekty** a poté otevřete projekt, pro který jste právě aktualizovali časové záznamy.</span><span class="sxs-lookup"><span data-stu-id="4b35c-128">Return to the **Sales** area, select **Projects** , and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="4b35c-129">Na stránce **Projekty** na kartě **Skutečné hodnoty** zobrazte provedené změny.</span><span class="sxs-lookup"><span data-stu-id="4b35c-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="4b35c-130">Pokud není karta **Skutečné hodnoty** viditelná, vyberte **Související** > **Skutečné hodnoty**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="4b35c-131">V seznamu **Přidružené zobrazení skutečností** můžete vidět, že původní časové záznamy, které byly stornovány, jsou stále uvedeny, stejně jako odpovídající opravené časové záznamy.</span><span class="sxs-lookup"><span data-stu-id="4b35c-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="4b35c-132">Například v následující grafice jsou dvě položky řádku s množstvím 8,00, jejichž debety jsou uvedeny ve sloupci Částka.</span><span class="sxs-lookup"><span data-stu-id="4b35c-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="4b35c-133">Navíc jsou ve sloupci Částka dvě položky řádku s množstvím -8,00, které zobrazují připsané částky.</span><span class="sxs-lookup"><span data-stu-id="4b35c-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="4b35c-134">Tyto korekce uvádějí množství na nulu.</span><span class="sxs-lookup"><span data-stu-id="4b35c-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="4b35c-135">Oprava schválených záznamů výdajů</span><span class="sxs-lookup"><span data-stu-id="4b35c-135">Correct approved expense entries</span></span>

<span data-ttu-id="4b35c-136">Chcete-li opravit jeden nebo více záznamů výdajů, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="4b35c-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="4b35c-137">V části **Prodej** v levém navigačním podokně pod možností **Transakce** vyberte **Schválené výdaje**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-137">In the **Sales** area, in the left navigation pane, under **Transactions** , select **Approved Expenses**.</span></span>

2. <span data-ttu-id="4b35c-138">V seznamu **Schválené výdaje** vyberte projekt, který chcete opravit, a poté vyberte **Opravit položky**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="4b35c-139">Automaticky se vytvoří nový deník oprav s přiřazeným typem **Oprava výdajů**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="4b35c-140">Na stránce **Nový deník** zadejte **Popis** pro opravu a na kartě **Oprava výdajů** v části **Nové hodnoty nákladů** vyberte datová pole, která chcete opravit pro vybrané řádky výdajů.</span><span class="sxs-lookup"><span data-stu-id="4b35c-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="4b35c-141">Například můžete přiřadit výdaje jinému **projektu** , nebo opravit **Kategorie výdajů** , **Datum výdaje** , nebo **Rezervovatelný zdroj**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-141">For example, you can assign the expense to another **Project** , or correct the **Expense Category** , **Expense Date** , or **Bookable Resource**.</span></span>

4. <span data-ttu-id="4b35c-142">Vyberte **Náhled**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-142">Select **Preview**.</span></span> <span data-ttu-id="4b35c-143">V dialogovém okně vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="4b35c-144">Na kartě **Řádky deníku** ověřte opravy. Můžete zobrazit seznam původních skutečných hodnot, které se vztahují k vybraným záznamům výdajů, které byly stornovány, a opraveným odpovídajícím řádkům, které byly vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="4b35c-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="4b35c-145">Pokud opravené hodnoty odpovídají očekávání, vyberte **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="4b35c-146">V dialogovém okně vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="4b35c-147">Pokud se hodnoty nezobrazují podle očekávání, vyberte **Zrušit** a vraťte se do seznamu **Schválené výdaje**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="4b35c-148">Opakujte kroky 2 až 5.</span><span class="sxs-lookup"><span data-stu-id="4b35c-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="4b35c-149">Opravené skutečné hodnoty budou mít stejné hodnoty, jaké jste vybrali v části **Nové hodnoty pro výdaje**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="4b35c-150">Po potvrzení deníku oprav přejděte zpět k projektu nebo projektům, které jste aktualizovali, a zobrazte své změny.</span><span class="sxs-lookup"><span data-stu-id="4b35c-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="4b35c-151">Na stránce projektu na kartě **Skutečné hodnoty** zkontrolujte **Přidružené zobrazení skutečností**.</span><span class="sxs-lookup"><span data-stu-id="4b35c-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="4b35c-152">Jsou uvedeny původní záznamy a opravené záznamy.</span><span class="sxs-lookup"><span data-stu-id="4b35c-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="4b35c-153">Následující obrázek ukazuje původní částky záznamu výdajů a odpovídající opravené položky částek zadaných výdajů.</span><span class="sxs-lookup"><span data-stu-id="4b35c-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

