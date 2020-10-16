---
title: Mapování projektů a úkolů na řádky nabídky založené na projektu
description: Toto téma poskytuje informace o mapování projektů a úkolů na řádku nabídky založené na projektu.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 6b396ccf5e76230a42a2f933a3aaa5b8149790bb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/06/2020
ms.locfileid: "3964899"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="8a867-103">Mapování projektů a úkolů na řádky nabídky založené na projektu</span><span class="sxs-lookup"><span data-stu-id="8a867-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="8a867-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="8a867-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8a867-105">Na řádcích nabídek založených na projektu můžete mapovat konkrétní úkoly projektu, který je již přidružen k řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="8a867-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="8a867-106">Když mapujete úkoly na řádek nabídky, následující položky, které jste definovali na řádku nabídky, se vztahují pouze na tyto úkoly:</span><span class="sxs-lookup"><span data-stu-id="8a867-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="8a867-107">Způsob fakturace</span><span class="sxs-lookup"><span data-stu-id="8a867-107">Billing method</span></span>
- <span data-ttu-id="8a867-108">Možnosti účtovatelnosti</span><span class="sxs-lookup"><span data-stu-id="8a867-108">Chargeability options</span></span>
- <span data-ttu-id="8a867-109">Nepřekročitelné limity</span><span class="sxs-lookup"><span data-stu-id="8a867-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="8a867-110">Zákazníci</span><span class="sxs-lookup"><span data-stu-id="8a867-110">Customers</span></span>

<span data-ttu-id="8a867-111">Například můžete mít projekt, kde jedna fáze je pevná cena a všechny ostatní fáze jsou čas a materiály.</span><span class="sxs-lookup"><span data-stu-id="8a867-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="8a867-112">V tomto případě můžete první fázi a všechny její podřízené úkoly přidružit k řádku nabídky pro tuto fázi s metodou fakturace za pevnou cenu.</span><span class="sxs-lookup"><span data-stu-id="8a867-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="8a867-113">Poté můžete všechny ostatní fáze přidružit k řádku nabídky založeném na čase a materiálů.</span><span class="sxs-lookup"><span data-stu-id="8a867-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="8a867-114">Přidružení úkolů k řádkům nabídky založené na projektu</span><span class="sxs-lookup"><span data-stu-id="8a867-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="8a867-115">Úkoly můžete přidružit k řádkům nabídek z následujících umístění:</span><span class="sxs-lookup"><span data-stu-id="8a867-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="8a867-116">Stránka **Projekt** > karta **Účtování úkolů** (optimální)</span><span class="sxs-lookup"><span data-stu-id="8a867-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="8a867-117">Stránka **Řádek nabídky** > karta **Účtovatelné úkoly**</span><span class="sxs-lookup"><span data-stu-id="8a867-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="8a867-118">Ze stránky Projekt</span><span class="sxs-lookup"><span data-stu-id="8a867-118">From the Project page</span></span>

<span data-ttu-id="8a867-119">Stránka **Projekt** poskytuje optimální prostředí pro přidružení úkolů k řádkům nabídky.</span><span class="sxs-lookup"><span data-stu-id="8a867-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="8a867-120">Na této stránce můžete vybrat více úkolů a všechny z nich – včetně jejich podřízených úkolů – přiřadit k vybranému řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="8a867-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="8a867-121">Na kartě **Všeobecné** řádku nabídky založené na projektu si ověřte, že je vyplněno pole **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="8a867-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="8a867-122">V poli **Zahrnuté úkoly** vyberte možnost **Pouze vybrané úkoly**.</span><span class="sxs-lookup"><span data-stu-id="8a867-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="8a867-123">Uložte řádek nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="8a867-123">Save the project-based quote line.</span></span> <span data-ttu-id="8a867-124">Když se formulář aktualizuje, zobrazí se karta **Účtovatelné úkoly**.</span><span class="sxs-lookup"><span data-stu-id="8a867-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="8a867-125">Na kartě **Všeobecné** vyberte odkaz na projekt v poli **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="8a867-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="8a867-126">Na stránce **Projekt** vyberte kartu **Účtování úkolů**.</span><span class="sxs-lookup"><span data-stu-id="8a867-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="8a867-127">Ve druhé mřížce, která se vztahuje na nastavení fakturace pro konkrétní úkol, vyberte jeden nebo více úkolů a poté vyberte možnost **Přidružit řádky nabídek**.</span><span class="sxs-lookup"><span data-stu-id="8a867-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="8a867-128">V zobrazené stránce dialogu vyberte řádek nabídky, který v nabídce zobrazí řádky nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="8a867-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="8a867-129">V poli **Typ fakturace** uveďte, zda jsou tyto úkoly účtovatelné nebo neúčtovatelné.</span><span class="sxs-lookup"><span data-stu-id="8a867-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="8a867-130">Zaškrtnutím políčka určíte, zda má přidružení zahrnovat podřízené úkoly vybraných úkolů.</span><span class="sxs-lookup"><span data-stu-id="8a867-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="8a867-131">Zaškrtnutí políčka přidruží podřízené úkoly vybraných úkolů k řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="8a867-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="8a867-132">Výběrem možnosti **OK** zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="8a867-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="8a867-133">Ze stránky řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="8a867-133">From the Quote line page</span></span>

<span data-ttu-id="8a867-134">K řádkům nabídky můžete přidružit projektové úkoly na kartě **Účtovatelné úkoly** umístěné ve stránce **Řádek nabídky**.</span><span class="sxs-lookup"><span data-stu-id="8a867-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="8a867-135">Optimálním místem pro přidružení projektových úkolů k řádkům nabídky je karta **Účtování úkolů** na stránce **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="8a867-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="8a867-136">Pokud přidružení úkolů provádíte na kartě **Účtovatelné úkoly** umístěné na stránce **Řádek nabídky**, musíte ručně přidružit každý projekt.</span><span class="sxs-lookup"><span data-stu-id="8a867-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="8a867-137">Na kartě **Všeobecné** řádku nabídky založené na projektu si ověřte, že je v poli **Projekt** vybrán projekt.</span><span class="sxs-lookup"><span data-stu-id="8a867-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="8a867-138">V poli **Zahrnuté úkoly** vyberte možnost **Pouze vybrané úkoly**.</span><span class="sxs-lookup"><span data-stu-id="8a867-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="8a867-139">Uložte řádek nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="8a867-139">Save the project-based quote line.</span></span> <span data-ttu-id="8a867-140">Když se formulář aktualizuje, zobrazí se karta **Účtovatelné úkoly**.</span><span class="sxs-lookup"><span data-stu-id="8a867-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="8a867-141">Na kartě **Účtovatelné úkoly** vyberte možnost **Přidat úkol řádku nabídky**.</span><span class="sxs-lookup"><span data-stu-id="8a867-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="8a867-142">Na stránce **Úkol řádku nabídky** vyberte úkol v poli **Úkoly** a v poli **Typ fakturace** vyberte příkaz **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8a867-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="8a867-143">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8a867-143">Close the page.</span></span> <span data-ttu-id="8a867-144">Vybraný úkol je nyní přidružen k řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="8a867-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="8a867-145">Zrušení přidružení úkolů k řádkům nabídky založené na projektu</span><span class="sxs-lookup"><span data-stu-id="8a867-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="8a867-146">Ze stránky Projekt</span><span class="sxs-lookup"><span data-stu-id="8a867-146">From the Project page</span></span>

<span data-ttu-id="8a867-147">Tato metoda poskytuje optimální prostředí pro zrušení přidružení úkolů k řádkům nabídky.</span><span class="sxs-lookup"><span data-stu-id="8a867-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="8a867-148">Na této stránce můžete vybrat více úkolů a zrušit jejich přiřazení – včetně jejich podřízených úkolů – k vybranému řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="8a867-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="8a867-149">Na kartě **Všeobecné** řádku nabídky založené na projektu vyberte v poli **Projekt** odkaz na projekt.</span><span class="sxs-lookup"><span data-stu-id="8a867-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="8a867-150">Na stránce **Projekt** vyberte kartu **Účtování úkolů**.</span><span class="sxs-lookup"><span data-stu-id="8a867-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="8a867-151">Ve druhé mřížce, která se vztahuje na nastavení fakturace pro konkrétní úkol, vyberte jeden nebo více úkolů a poté vyberte možnost **Zrušit přidružení řádků nabídek**.</span><span class="sxs-lookup"><span data-stu-id="8a867-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="8a867-152">Na zobrazené stránce dialogu vyberte řádek nabídky.</span><span class="sxs-lookup"><span data-stu-id="8a867-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="8a867-153">Zaškrtnutím políčka určíte, zda má být přidružení odebráno také u podřízených úkolů vybraných úkolů.</span><span class="sxs-lookup"><span data-stu-id="8a867-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="8a867-154">Zaškrtnutí políčka zruší také přidružení podřízených úkolů vybraných úkolů k řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="8a867-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="8a867-155">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a867-155">Select **OK**.</span></span> <span data-ttu-id="8a867-156">Varovná zpráva vás informuje, že pokud toto přidružení odeberete, všechny skutečné údaje dříve zaznamenané v úkolu lze stornovat.</span><span class="sxs-lookup"><span data-stu-id="8a867-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="8a867-157">Výběrem možnosti **OK** pokračujte a odeberte přidružení mezi úkolem a řádkem nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="8a867-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="8a867-158">Ze stránky řádku nabídky</span><span class="sxs-lookup"><span data-stu-id="8a867-158">From the Quote line page</span></span>

<span data-ttu-id="8a867-159">Přidružení projektových úkolů k řádkům nabídky lze zrušit také na kartě **Účtovatelné úkoly** umístěné ve stránce **Řádek nabídky**.</span><span class="sxs-lookup"><span data-stu-id="8a867-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="8a867-160">Na kartě **Účtovatelné úkoly** vyberte možnost **Odstranit úkol řádku nabídky**.</span><span class="sxs-lookup"><span data-stu-id="8a867-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="8a867-161">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a867-161">Select **OK**.</span></span> <span data-ttu-id="8a867-162">Varovná zpráva vás informuje, že pokud toto přidružení odeberete, všechny skutečné údaje dříve zaznamenané v úkolu lze stornovat.</span><span class="sxs-lookup"><span data-stu-id="8a867-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="8a867-163">Výběrem možnosti **OK** pokračujte a odeberte přidružení mezi úkolem a řádkem nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="8a867-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="8a867-164">Tento postup neodstraní úkol z projektu.</span><span class="sxs-lookup"><span data-stu-id="8a867-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="8a867-165">Odstraní pouze přidružení úkolu k řádku nabídky založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="8a867-165">It only removes the task association from the project-based quote line.</span></span>
