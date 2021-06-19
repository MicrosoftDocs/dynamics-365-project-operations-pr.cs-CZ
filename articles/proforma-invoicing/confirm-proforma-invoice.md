---
title: Potvrzení proforma faktury založené na projektu
description: Tento téma poskytuje informace o tom, jak potvrdit projektovou proforma fakturu.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e4591d97e9d895dade42b2bcce57f22208cba96
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012128"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="e5b40-103">Potvrzení proforma faktury založené na projektu</span><span class="sxs-lookup"><span data-stu-id="e5b40-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="e5b40-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="e5b40-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e5b40-105">Po potvrzení proforma faktury se stav projektové faktury aktualizuje na **Potvrzeno**.</span><span class="sxs-lookup"><span data-stu-id="e5b40-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="e5b40-106">Když je faktura potvrzena, stane se pouze pro čtení.</span><span class="sxs-lookup"><span data-stu-id="e5b40-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="e5b40-107">Do budoucna bude možné fakturu opravit pouze v případě, že dojde k opravám nebo kreditům zahájeným zákazníkem.</span><span class="sxs-lookup"><span data-stu-id="e5b40-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="e5b40-108">V následující tabulce jsou uvedeny skutečné hodnoty vytvořené systémem.</span><span class="sxs-lookup"><span data-stu-id="e5b40-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="e5b40-109">Tyto skutečné hodnoty se vytvoří, když se na faktuře konceptu projektu provedou určité operace, než se potvrdí.</span><span class="sxs-lookup"><span data-stu-id="e5b40-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="e5b40-110">
                    <strong>Scénář</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e5b40-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="e5b40-111">
                    <strong>Skutečné hodnoty vytvořené při potvrzení</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e5b40-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5b40-112">Fakturace záloh</span><span class="sxs-lookup"><span data-stu-id="e5b40-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-113">Fakturovaný skutečný prodej typu <strong>Záloha</strong> je vytvořen pro částku v záloze.</span><span class="sxs-lookup"><span data-stu-id="e5b40-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-114">Skutečný nevyfakturovaný prodej se zápornou částkou zálohy nebo platby předem, která má být použita k odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="e5b40-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5b40-115">Po úplném odsouhlasení zálohy na fakturu.</span><span class="sxs-lookup"><span data-stu-id="e5b40-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-116">Nevyfakturované prodejní storno zálohy, která byla vytvořena pro odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="e5b40-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="e5b40-117">Tato částka je kladná, protože má zrušit zápornou hodnotu, která byla vytvořen při fakturaci zálohy.</span><span class="sxs-lookup"><span data-stu-id="e5b40-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-118">Fakturovaný skutečný prodej na částku na této faktuře.</span><span class="sxs-lookup"><span data-stu-id="e5b40-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e5b40-119">Po částečném odsouhlasení zálohy na fakturu.</span><span class="sxs-lookup"><span data-stu-id="e5b40-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-120">Nevyfakturované prodejní storno zálohy, která byla vytvořena pro odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="e5b40-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="e5b40-121">Tato částka je kladná, protože má zrušit zápornou hodnotu, která byla vytvořen při fakturaci zálohy.</span><span class="sxs-lookup"><span data-stu-id="e5b40-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-122">Fakturovaný skutečný prodej na částku na této faktuře.</span><span class="sxs-lookup"><span data-stu-id="e5b40-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-123">Záporný nevyfakturovaný skutečný prodej zbývající zálohy, která má být použita k odsouhlasení na budoucích fakturách.</span><span class="sxs-lookup"><span data-stu-id="e5b40-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5b40-124">Fakturace časové transakce bez jakýchkoli úprav konceptu faktury.</span><span class="sxs-lookup"><span data-stu-id="e5b40-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-125">Nevyfakturované storno prodeje pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="e5b40-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-126">Fakturovaný skutečný prodej pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="e5b40-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e5b40-127">Fakturace časové transakce, která byla upravena, aby se snížilo množství.</span><span class="sxs-lookup"><span data-stu-id="e5b40-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-128">Nevyfakturované storno prodeje pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="e5b40-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-129">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za hodiny a částku na upraveném detailu řádku faktury, zrušení skutečného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="e5b40-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-130">Nový nevyfakturovaný skutečný prodej, který nelze účtovat za zbývající hodiny a částku po odečtení opravených údajů v údajích upraveného řádku faktury, zrušení skutečného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="e5b40-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5b40-131">Fakturace časové transakce, která byla upravena, aby se zvýšilo množství.</span><span class="sxs-lookup"><span data-stu-id="e5b40-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-132">Nevyfakturované storno prodeje pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="e5b40-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-133">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za hodiny a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="e5b40-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5b40-134">Fakturace transakce výdaje bez jakýchkoli úprav konceptu faktury.</span><span class="sxs-lookup"><span data-stu-id="e5b40-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-135">Nevyfakturované storno prodeje pro množství a částku při původním schválení výdaje.</span><span class="sxs-lookup"><span data-stu-id="e5b40-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-136">Fakturovaný skutečný prodej pro množství a částku při původním schválení výdaje.</span><span class="sxs-lookup"><span data-stu-id="e5b40-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e5b40-137">Fakturace transakce výdaje, která byla upravena, aby se snížilo množství.</span><span class="sxs-lookup"><span data-stu-id="e5b40-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-138">Nevyfakturované storno prodeje pro množství a částku při původním schválení výdaje.</span><span class="sxs-lookup"><span data-stu-id="e5b40-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-139">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="e5b40-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-140">Nový nevyfakturovaný skutečný prodej, který je neúčtovatelný za zbývající množství a částku po odečtení korigovaných čísel na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="e5b40-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5b40-141">Fakturace transakce výdaje, která byla upravena, aby se zvýšilo množství.</span><span class="sxs-lookup"><span data-stu-id="e5b40-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-142">Nevyfakturované storno prodeje pro množství a částku při původním schválení výdaje.</span><span class="sxs-lookup"><span data-stu-id="e5b40-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-143">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="e5b40-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5b40-144">Fakturace významné transakce bez jakýchkoli úprav konceptu faktury.</span><span class="sxs-lookup"><span data-stu-id="e5b40-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-145">Nevyfakturované vrácení prodeje a množství a částky na původním schválení použití materiálu.</span><span class="sxs-lookup"><span data-stu-id="e5b40-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-146">Vyfakturovaný skutečný prodej a množství a částky na původním schválení použití materiálu.</span><span class="sxs-lookup"><span data-stu-id="e5b40-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e5b40-147">Fakturace materiálové transakce, která byla upravena, aby se snížilo množství.</span><span class="sxs-lookup"><span data-stu-id="e5b40-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-148">Nevyfakturované vrácení prodeje a množství a částky na původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="e5b40-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-149">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="e5b40-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-150">Nový nevyfakturovaný skutečný prodej, který je neúčtovatelný za zbývající množství a částku po odečtení korigovaných čísel na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="e5b40-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5b40-151">Fakturace materiálové transakce, která byla upravena, aby se zvýšilo množství.</span><span class="sxs-lookup"><span data-stu-id="e5b40-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-152">Nevyfakturované vrácení prodeje a množství a částky na původním schválení použití materiálu.</span><span class="sxs-lookup"><span data-stu-id="e5b40-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-153">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="e5b40-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5b40-154">Fakturace poplatku.</span><span class="sxs-lookup"><span data-stu-id="e5b40-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-155">Nevyfakturované storno prodeje pro částku poplatku na původním řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="e5b40-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-156">Fakturovaný skutečný prodej pro množství a částku na původním řádku deníku poplatku.</span><span class="sxs-lookup"><span data-stu-id="e5b40-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="e5b40-157">Fakturace milníku.</span><span class="sxs-lookup"><span data-stu-id="e5b40-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e5b40-158">Skutečně fakturovaný prodej pro část milníku v původním milníku na řádku smlouvy o projektu.</span><span class="sxs-lookup"><span data-stu-id="e5b40-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
