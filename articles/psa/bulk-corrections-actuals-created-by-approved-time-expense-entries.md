---
title: Hromadné opravy skutečných hodnot vytvořených schválenými položkami času a výdajů
description: Toto téma vysvětluje, jak může správce provést jednorázové nebo hromadné opravy dříve schválených položek času nebo výdajů, pokud není fakturace dokončena.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 063c4d017f5904f09c3c239bfa432a128872e4d7
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144945"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="7a61a-103">Hromadné opravy skutečných hodnot vytvořených schválenými položkami času a výdajů</span><span class="sxs-lookup"><span data-stu-id="7a61a-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7a61a-104">Někdy může být nesprávně zadán údaj o čase nebo výdaji.</span><span class="sxs-lookup"><span data-stu-id="7a61a-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="7a61a-105">Poradce může například při vytváření časového záznamu vybrat nesprávné datum nebo při zadávání výdaje může transponovat čísla.</span><span class="sxs-lookup"><span data-stu-id="7a61a-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="7a61a-106">Pokud konzultant nemůže provést aktualizace odeslaných zadání, může správce přímo opravit záznam pro projekt.</span><span class="sxs-lookup"><span data-stu-id="7a61a-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="7a61a-107">K dokončení postupů v tomto tématu budete potřebovat oprávnění správce.</span><span class="sxs-lookup"><span data-stu-id="7a61a-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="7a61a-108">Oprava schválených časových údajů</span><span class="sxs-lookup"><span data-stu-id="7a61a-108">Correct approved time entries</span></span>     

<span data-ttu-id="7a61a-109">Chcete-li opravit jeden nebo více časových záznamů pro projekt, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="7a61a-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="7a61a-110">V oblasti **Prodej** vyberte **Transakce** a poté vyberte **Schválený čas**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="7a61a-111">V seznamu **Schválený čas** vyhledejte a vyberte jeden nebo více schválených časových záznamů, které chcete opravit.</span><span class="sxs-lookup"><span data-stu-id="7a61a-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="7a61a-112">Pomocí filtru můžete vyhledat související položky.</span><span class="sxs-lookup"><span data-stu-id="7a61a-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="7a61a-113">Můžete například filtrovat ID projektu a vybrat všechny schválené časové záznamy s tímto ID projektu.</span><span class="sxs-lookup"><span data-stu-id="7a61a-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="7a61a-114">Zvolte **Opravit položky**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-114">Select **Correct entries**.</span></span> <span data-ttu-id="7a61a-115">Automaticky se vytvoří nový deník oprav s přiřazeným typem **Oprava času**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="7a61a-116">Vybrané položky se přidají do deníku.</span><span class="sxs-lookup"><span data-stu-id="7a61a-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="7a61a-117">Na stránce **Nový deník** zadejte **Popis** pro svůj deník oprav a poté vyberte kartu **Opravy časových záznamů**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="7a61a-118">V části **Nové hodnoty pro časové záznamy** aktualizujte pole správnými informacemi podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="7a61a-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="7a61a-119">Například můžete změnit přiřazený projekt nebo rezervovatelný zdroj.</span><span class="sxs-lookup"><span data-stu-id="7a61a-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="7a61a-120">Vyberte **Náhled**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-120">Select **Preview**.</span></span> <span data-ttu-id="7a61a-121">V dialogovém okně vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="7a61a-122">Na kartě **Řádky deníku** můžete zobrazit seznam původních skutečných hodnot, které se vztahují k vybraným časovým záznamům, které byly stornovány, a opraveným odpovídajícím řádkům, které byly vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="7a61a-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="7a61a-123">Pokud je třeba provést další opravy, opakujte kroky 5 a 6.</span><span class="sxs-lookup"><span data-stu-id="7a61a-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="7a61a-124">Všechny opravené skutečné hodnoty budou mít stejné hodnoty, jaké jste vybrali v části **Nové hodnoty pro časové záznamy**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="7a61a-125">Pokud se opravy objeví podle očekávání, vyberte **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="7a61a-126">V dialogovém okně vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="7a61a-127">Vraťte se do části **Prodej**, vyberte **Projekty** a poté otevřete projekt, pro který jste právě aktualizovali časové záznamy.</span><span class="sxs-lookup"><span data-stu-id="7a61a-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="7a61a-128">Na stránce **Projekty** na kartě **Skutečné hodnoty** zobrazte provedené změny.</span><span class="sxs-lookup"><span data-stu-id="7a61a-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="7a61a-129">Pokud není karta **Skutečné hodnoty** viditelná, vyberte **Související** > **Skutečné hodnoty**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="7a61a-130">V seznamu **Přidružené zobrazení skutečností** můžete vidět, že původní časové záznamy, které byly stornovány, jsou stále uvedeny, stejně jako odpovídající opravené časové záznamy.</span><span class="sxs-lookup"><span data-stu-id="7a61a-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="7a61a-131">Například v následující grafice jsou dvě položky řádku s množstvím 8,00, jejichž debety jsou uvedeny ve sloupci Částka.</span><span class="sxs-lookup"><span data-stu-id="7a61a-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="7a61a-132">Navíc jsou ve sloupci Částka dvě položky řádku s množstvím -8,00, které zobrazují připsané částky.</span><span class="sxs-lookup"><span data-stu-id="7a61a-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="7a61a-133">Tyto korekce uvádějí množství na nulu.</span><span class="sxs-lookup"><span data-stu-id="7a61a-133">These corrections bring the quantity to zero.</span></span>

![Seznam přidružených zobrazení skutečností](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="7a61a-135">Oprava schválených záznamů výdajů</span><span class="sxs-lookup"><span data-stu-id="7a61a-135">Correct approved expense entries</span></span>

<span data-ttu-id="7a61a-136">Chcete-li opravit jeden nebo více záznamů výdajů, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="7a61a-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="7a61a-137">V části **Prodej** v levém navigačním podokně pod možností **Transakce** vyberte **Schválené výdaje**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="7a61a-138">V seznamu **Schválené výdaje** vyberte projekt, který chcete opravit, a poté vyberte **Opravit položky**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="7a61a-139">Automaticky se vytvoří nový deník oprav s přiřazeným typem **Oprava výdajů**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="7a61a-140">Na stránce **Nový deník** zadejte **Popis** pro opravu a na kartě **Oprava výdajů** v části **Nové hodnoty nákladů** vyberte datová pole, která chcete opravit pro vybrané řádky výdajů.</span><span class="sxs-lookup"><span data-stu-id="7a61a-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="7a61a-141">Například můžete přiřadit výdaje jinému **projektu**, nebo opravit **Kategorie výdajů**, **Datum výdaje**, nebo **Rezervovatelný zdroj**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="7a61a-142">Vyberte **Náhled**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-142">Select **Preview**.</span></span> <span data-ttu-id="7a61a-143">V dialogovém okně vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="7a61a-144">Na kartě **Řádky deníku** ověřte opravy. Můžete zobrazit seznam původních skutečných hodnot, které se vztahují k vybraným záznamům výdajů, které byly stornovány, a opraveným odpovídajícím řádkům, které byly vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="7a61a-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="7a61a-145">Pokud opravené hodnoty odpovídají očekávání, vyberte **Potvrdit**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="7a61a-146">V dialogovém okně vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="7a61a-147">Pokud se hodnoty nezobrazují podle očekávání, vyberte **Zrušit** a vraťte se do seznamu **Schválené výdaje**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="7a61a-148">Opakujte kroky 2 až 5.</span><span class="sxs-lookup"><span data-stu-id="7a61a-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="7a61a-149">Opravené skutečné hodnoty budou mít stejné hodnoty, jaké jste vybrali v části **Nové hodnoty pro výdaje**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="7a61a-150">Po potvrzení deníku oprav přejděte zpět k projektu nebo projektům, které jste aktualizovali, a zobrazte své změny.</span><span class="sxs-lookup"><span data-stu-id="7a61a-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="7a61a-151">Na stránce projektu na kartě **Skutečné hodnoty** zkontrolujte **Přidružené zobrazení skutečností**.</span><span class="sxs-lookup"><span data-stu-id="7a61a-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="7a61a-152">Jsou uvedeny původní záznamy a opravené záznamy.</span><span class="sxs-lookup"><span data-stu-id="7a61a-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="7a61a-153">Následující obrázek ukazuje původní částky záznamu výdajů a odpovídající opravené položky částek zadaných výdajů.</span><span class="sxs-lookup"><span data-stu-id="7a61a-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Skutečné hodnoty nákladů](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
