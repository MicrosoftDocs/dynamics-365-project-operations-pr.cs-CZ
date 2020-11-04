---
title: Cestovní žádanky
description: Toto téma poskytuje informace o cestovních žádankách.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073649"
---
# <a name="travel-requisitions"></a><span data-ttu-id="0e20b-103">Cestovní žádanky</span><span class="sxs-lookup"><span data-stu-id="0e20b-103">Travel requisitions</span></span>

<span data-ttu-id="0e20b-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="0e20b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0e20b-105">Cestovní žádanka uvádí výdaje, které vzniknou za účelem cesty.</span><span class="sxs-lookup"><span data-stu-id="0e20b-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="0e20b-106">Cestovní žádanka je předložena ke kontrole a lze ji použít k autorizaci výdajů.</span><span class="sxs-lookup"><span data-stu-id="0e20b-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="0e20b-107">Předtím, než vám vzniknou jakékoli náklady, které jsou účtovány organizaci, může být nutné předložit cestovní žádanku.</span><span class="sxs-lookup"><span data-stu-id="0e20b-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="0e20b-108">Tento požadavek platí bez ohledu na to, zda účtujete výdaje na podnikovou kreditní kartu, utrácíte hotovost, kterou jste obdrželi z hotovostní zálohy, nebo vám vzniknou hotové výdaje, které vám organizace uhradí.</span><span class="sxs-lookup"><span data-stu-id="0e20b-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="0e20b-109">Cestovní žádanky a zásady lze použít ke správě výdajů organizace.</span><span class="sxs-lookup"><span data-stu-id="0e20b-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="0e20b-110">Například pokud vaše organizace pracuje na projektu s pevnou cenou, který vyžaduje cestování, musí cestovní náklady členů týmu projektu odpovídat rozpočtu projektu.</span><span class="sxs-lookup"><span data-stu-id="0e20b-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="0e20b-111">Vyžadováním schválení cestovních výdajů před jejich vznikem může organizace pomoci zajistit, aby projekt zůstal v rámci rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="0e20b-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="0e20b-112">Konfigurace</span><span class="sxs-lookup"><span data-stu-id="0e20b-112">Configuration</span></span> 

<span data-ttu-id="0e20b-113">Cestovní požadavky lze nakonfigurovat jako „povinné“ povolením parametru „Předběžná autorizace cesty je povinná“ v parametrech správy výdajů.</span><span class="sxs-lookup"><span data-stu-id="0e20b-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="0e20b-114">Vytvoření a odeslání cestovní žádanky</span><span class="sxs-lookup"><span data-stu-id="0e20b-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="0e20b-115">Přejděte na **Moje výdaje: Cestovní žádanka** a vyberte **Nová cestovní žádanka**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-115">Go to **My expenses: Travel Requisition** , and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="0e20b-116">Zadejte účel a cíl žádanky.</span><span class="sxs-lookup"><span data-stu-id="0e20b-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="0e20b-117">Do pole **Popis cesty** zadejte jakékoli další informace.</span><span class="sxs-lookup"><span data-stu-id="0e20b-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="0e20b-118">Pro každý z očekávaných výdajů, například za letenku, stravu nebo pronájem auta, vytvořte řádkovou položku výdajů.</span><span class="sxs-lookup"><span data-stu-id="0e20b-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="0e20b-119">Uveďte předpokládané datum, odhadovanou částku a měnu pro každý výdaj.</span><span class="sxs-lookup"><span data-stu-id="0e20b-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="0e20b-120">Po dokončení přidávání očekávaných výdajů vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="0e20b-121">Až budete připravení odeslat cestovní žádanku, vyberte **Pracovní postup** > **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="0e20b-122">Schválené cestovní žádanky si můžete prohlédnout v okně **Moje výdaje: Cestovní žádanka**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="0e20b-123">Zobrazení dostupných cestovních žádanek</span><span class="sxs-lookup"><span data-stu-id="0e20b-123">View available travel requisitions</span></span>

<span data-ttu-id="0e20b-124">Všechny své cestovní žádanky si můžete prohlédnout v okně **Moje výdaje: Cestovní žádanky**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="0e20b-125">Schválení cestovních žádanek</span><span class="sxs-lookup"><span data-stu-id="0e20b-125">Approve travel requisitions</span></span>

<span data-ttu-id="0e20b-126">Vyberte cestovní žádanku, kterou chcete schválit, a poté vyberte **Pracovní postup** > **Schválit**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="0e20b-127">Odeslání zprávy o výdajích pomocí schválené cestovní žádanky</span><span class="sxs-lookup"><span data-stu-id="0e20b-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="0e20b-128">Vytvořte nové vyúčtování výdajů a v záhlaví vyúčtování výdajů vyberte ze seznamu schválených cestovních žádanek **Mapa k cestovní žádance**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="0e20b-129">Pole **Částka na cestovní žádance** se automaticky aktualizuje v záhlaví vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="0e20b-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="0e20b-130">Přidejte jednotlivé výdaje vynaložené na cestu.</span><span class="sxs-lookup"><span data-stu-id="0e20b-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="0e20b-131">Pokud je povoleno pole **Schváleno předem** , bude aktualizována sesouhlasená částka a autorizovaná částka pro konkrétní kategorii výdajů.</span><span class="sxs-lookup"><span data-stu-id="0e20b-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="0e20b-132">Když mapujete vyúčtování výdajů na schválenou žádost o cestování, částka transakce nemůže být větší než autorizovaná částka.</span><span class="sxs-lookup"><span data-stu-id="0e20b-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
