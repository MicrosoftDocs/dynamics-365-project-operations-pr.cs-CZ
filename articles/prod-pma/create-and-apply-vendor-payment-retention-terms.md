---
title: Vytvoření a použití podmínek zadržení plateb dodavatele
description: Tento téma poskytuje informace o tom, jak nastavit a udržovat podmínky zadržení pro platby dodavatele.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 09bb30f55ee8e1f24634e9d8b7dea95bd3dbd24f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006310"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="50234-103">Vytvoření a použití podmínek zadržení plateb dodavatele</span><span class="sxs-lookup"><span data-stu-id="50234-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="50234-104">Nastavení podmínek zadržení plateb dodavatele pro projekt je užitečné, když chce vaše organizace zadržet část plateb provedených prodejci.</span><span class="sxs-lookup"><span data-stu-id="50234-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="50234-105">Například když chcete pozdržet platbu prodejci, dokud dodané produkty nesplní vaše očekávání.</span><span class="sxs-lookup"><span data-stu-id="50234-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="50234-106">Podmínky pro zadržení plateb dodavatele lze určit při sjednávání smlouvy s dodavatelem.</span><span class="sxs-lookup"><span data-stu-id="50234-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="50234-107">Vytvoření podmínek zadržení plateb dodavatele</span><span class="sxs-lookup"><span data-stu-id="50234-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="50234-108">Můžete zadat procento platby dodavatele za zadržení a procento dříve zadržených částek, které mají být uvolněny.</span><span class="sxs-lookup"><span data-stu-id="50234-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="50234-109">Částky jsou automaticky zadržovány na fakturách dodavatelů, dokud smlouva nedosáhne zadaného stavu dokončení.</span><span class="sxs-lookup"><span data-stu-id="50234-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="50234-110">Jakmile nastavíte podmínky zadržení, můžete je použít na jakýkoli projekt pro daného dodavatele.</span><span class="sxs-lookup"><span data-stu-id="50234-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="50234-111">Pomocí následujících kroků můžete nastavit a udržovat podmínky zadržení plateb dodavatele.</span><span class="sxs-lookup"><span data-stu-id="50234-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="50234-112">Přejděte do **Řízení projektů a účetnictví** > **Zadržení** > **Podmínky zadržení plateb dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="50234-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="50234-113">Vyberte možnost **Nový** a přidejte novou podmínku zadržení pro dodavatele.</span><span class="sxs-lookup"><span data-stu-id="50234-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="50234-114">Hodnota **ID pravidla** pro novou podmínku je automaticky zadána.</span><span class="sxs-lookup"><span data-stu-id="50234-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="50234-115">Zadejte krátký popis do pole **Popis** pole a na rychlé kartě **Podmínky** vyberte **Přidat řádek** pro zadání hodnot podmínek pro následující:</span><span class="sxs-lookup"><span data-stu-id="50234-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="50234-116">**Procento dodaných jednotek**: Zadejte procento dokončení pro danou podmínku.</span><span class="sxs-lookup"><span data-stu-id="50234-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="50234-117">Částky jsou automaticky zadržovány na fakturách dodavatelů, dokud fáze dokončení projektu neodpovídá zadanému procentu.</span><span class="sxs-lookup"><span data-stu-id="50234-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="50234-118">Například pokud zadáte 50,00, částky budou zadrženy, dokud nebude projekt dokončen na 50 procent.</span><span class="sxs-lookup"><span data-stu-id="50234-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="50234-119">**Procento k zadržení**: Zadejte procento z částky faktury dodavatele, která se má zadržet.</span><span class="sxs-lookup"><span data-stu-id="50234-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="50234-120">Například pokud zadáte 10,00, pak se 10 procent částky na faktuře dodavatele zadrží, dokud projekt nedosáhne procenta dokončení stanoveného v poli **Procento dodaných jednotek**.</span><span class="sxs-lookup"><span data-stu-id="50234-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="50234-121">**Procento k uvolnění**: Vyberte **Přidat řádek** k zadání procenta všech dříve zadržených částek, které mají být uvolněny pro vybranou úroveň dokončení projektu.</span><span class="sxs-lookup"><span data-stu-id="50234-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="50234-122">Pokud máte více než jeden milník pro různé úrovně dokončení projektu, zadejte pro každé pravidlo zadržení samostatný řádek podmínek zadržení pro dodavatele.</span><span class="sxs-lookup"><span data-stu-id="50234-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="50234-123">Každý řádek může specifikovat jiné procento zadržení a jiné procento uvolnění pro každou určenou úroveň dokončení projektu.</span><span class="sxs-lookup"><span data-stu-id="50234-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="50234-124">Jakmile vytvoříte podmínky zadržení pro dodavatele, můžete je použít na projekt.</span><span class="sxs-lookup"><span data-stu-id="50234-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="50234-125">Použití podmínek zadržení pro dodavatele na projekt</span><span class="sxs-lookup"><span data-stu-id="50234-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="50234-126">Přejděte do nabídky **Řízení projektů a účetnictví** > **Projekty** > **Všechny projekty** a otevřete projekt na stránce seznamu projektů.</span><span class="sxs-lookup"><span data-stu-id="50234-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="50234-127">Na pevné záložce **Smlouvy s dodavatelem** vyberte položku **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="50234-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="50234-128">V poli **Kód účtu** vyberte jednu z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="50234-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="50234-129">**Tabulka**: Podmínky zadržení pro dodavatele platí pro jednoho dodavatele.</span><span class="sxs-lookup"><span data-stu-id="50234-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="50234-130">**Skupina**: Podmínky zadržení pro dodavatele platí pro všechny dodavatele ve skupině dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="50234-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="50234-131">**Vše**: Podmínky zadržení pro dodavatele platí pro všechny dodavatele.</span><span class="sxs-lookup"><span data-stu-id="50234-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="50234-132">V poli **Dodavatel / skupina dodavatelů** vyberte dodavatele nebo skupinu dodavatelů, na které se vztahují podmínky zadržení pro dodavatele.</span><span class="sxs-lookup"><span data-stu-id="50234-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="50234-133">Pokud jste vybrali **Všechno** v předchozím kroku, toto pole není k dispozici.</span><span class="sxs-lookup"><span data-stu-id="50234-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="50234-134">V poli **Podmínky zadržení pro dodavatele** vyberte podmínky zadržení, které jste vytvořili v předchozím postupu.</span><span class="sxs-lookup"><span data-stu-id="50234-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="50234-135">Pokud má projekt pro dodavatele nastaveny také podmínky zaplacení po uhrazení (PWP), zadejte prahovou hodnotu pro projekt do pole **Procento prahové hodnoty PWP**.</span><span class="sxs-lookup"><span data-stu-id="50234-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="50234-136">Podmínky zadržení pro dodavatele se také zobrazují na nákupních objednávkách, které pro dodavatele vytvoříte.</span><span class="sxs-lookup"><span data-stu-id="50234-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]