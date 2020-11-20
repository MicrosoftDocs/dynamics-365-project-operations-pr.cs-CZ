---
title: Potvrzení proforma faktury
description: Tento téma poskytuje informace o potvrzení proforma faktury.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128095"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="931a2-103">Potvrzení proforma faktury</span><span class="sxs-lookup"><span data-stu-id="931a2-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="931a2-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="931a2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="931a2-105">Po potvrzení proforma faktury se stav projektové faktury aktualizuje na **Potvrzeno**.</span><span class="sxs-lookup"><span data-stu-id="931a2-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="931a2-106">Když je faktura potvrzena, stane se pouze pro čtení.</span><span class="sxs-lookup"><span data-stu-id="931a2-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="931a2-107">Do budoucna bude možné fakturu opravit, pouze pokud dojde k opravám nebo kreditům zahájeným zákazníkem nebo pokud je označena jako zaplacená.</span><span class="sxs-lookup"><span data-stu-id="931a2-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="931a2-108">V následující tabulce jsou uvedeny skutečné hodnoty vytvořené systémem.</span><span class="sxs-lookup"><span data-stu-id="931a2-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="931a2-109">Tyto skutečné hodnoty se vytvoří, když se na faktuře konceptu projektu provedou určité operace, než se potvrdí.</span><span class="sxs-lookup"><span data-stu-id="931a2-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="931a2-110">
                    <strong>Scénář</strong>
                </span><span class="sxs-lookup"><span data-stu-id="931a2-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="931a2-111">
                    <strong>Skutečné hodnoty vytvořené při potvrzení</strong>
                </span><span class="sxs-lookup"><span data-stu-id="931a2-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="931a2-112">Fakturace časové transakce bez jakýchkoli úprav konceptu faktury.</span><span class="sxs-lookup"><span data-stu-id="931a2-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-113">Nevyfakturované storno prodeje pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="931a2-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-114">Fakturovaný skutečný prodej pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="931a2-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="931a2-115">Fakturace časové transakce, která byla upravena, aby se snížilo množství.</span><span class="sxs-lookup"><span data-stu-id="931a2-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-116">Nevyfakturované storno prodeje pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="931a2-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-117">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za hodiny a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="931a2-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-118">Nový nevyfakturovaný skutečný prodej, který je neúčtovatelný za zbývající hodiny a částku po odečtení korigovaných čísel na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="931a2-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="931a2-119">Fakturace časové transakce, která byla upravena, aby se zvýšilo množství.</span><span class="sxs-lookup"><span data-stu-id="931a2-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-120">Nevyfakturované storno prodeje pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="931a2-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-121">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za hodiny a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="931a2-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="931a2-122">Fakturace transakce výdaje bez jakýchkoli úprav konceptu faktury.</span><span class="sxs-lookup"><span data-stu-id="931a2-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-123">Nevyfakturované storno prodeje pro množství a částku při původním schválení výdaje.</span><span class="sxs-lookup"><span data-stu-id="931a2-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-124">Fakturovaný skutečný prodej pro množství a částku při původním schválení výdaje.</span><span class="sxs-lookup"><span data-stu-id="931a2-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="931a2-125">Fakturace transakce výdaje, která byla upravena, aby se snížilo množství.</span><span class="sxs-lookup"><span data-stu-id="931a2-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-126">Nevyfakturované storno prodeje pro množství a částku při původním schválení výdaje.</span><span class="sxs-lookup"><span data-stu-id="931a2-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-127">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="931a2-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-128">Nový nevyfakturovaný skutečný prodej, který je neúčtovatelný za zbývající množství a částku po odečtení korigovaných čísel na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="931a2-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="931a2-129">Fakturace transakce výdaje, která byla upravena, aby se zvýšilo množství.</span><span class="sxs-lookup"><span data-stu-id="931a2-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-130">Nevyfakturované storno prodeje pro množství a částku při původním schválení výdaje.</span><span class="sxs-lookup"><span data-stu-id="931a2-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-131">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="931a2-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="931a2-132">Fakturace poplatku.</span><span class="sxs-lookup"><span data-stu-id="931a2-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-133">Nevyfakturované storno prodeje pro částku poplatku na původním řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="931a2-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-134">Fakturovaný skutečný prodej pro množství a částku na původním řádku deníku poplatku.</span><span class="sxs-lookup"><span data-stu-id="931a2-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="931a2-135">Fakturace milníku.</span><span class="sxs-lookup"><span data-stu-id="931a2-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="931a2-136">Skutečně fakturovaný prodej pro část milníku v původním milníku na řádku smlouvy o projektu.</span><span class="sxs-lookup"><span data-stu-id="931a2-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
