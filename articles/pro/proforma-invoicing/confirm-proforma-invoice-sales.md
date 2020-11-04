---
title: Potvrzení proforma faktury
description: Toto téma poskytuje informace o tom, jak potvrzovat proforma faktury v aplikaci Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b67ee6848efdcb85cf732c1eaa3e40cdc51a2e2
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073688"
---
# <a name="confirming-a-proforma-invoice"></a><span data-ttu-id="df1a2-103">Potvrzení proforma faktury</span><span class="sxs-lookup"><span data-stu-id="df1a2-103">Confirming a proforma invoice</span></span>

<span data-ttu-id="df1a2-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="df1a2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="df1a2-105">Po potvrzení proforma faktury se stav projektové faktury aktualizuje na **Potvrzeno**.</span><span class="sxs-lookup"><span data-stu-id="df1a2-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="df1a2-106">Když je faktura potvrzena, stane se pouze pro čtení.</span><span class="sxs-lookup"><span data-stu-id="df1a2-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="df1a2-107">Do budoucna bude možné fakturu opravit, pouze pokud dojde k opravám nebo kreditům zahájeným zákazníkem nebo pokud je faktura označena jako zaplacená.</span><span class="sxs-lookup"><span data-stu-id="df1a2-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="df1a2-108">V následující tabulce jsou uvedeny skutečné hodnoty vytvořené systémem.</span><span class="sxs-lookup"><span data-stu-id="df1a2-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="df1a2-109">Tyto skutečné hodnoty se vytvoří, když se na faktuře konceptu projektu provedou určité operace, než se potvrdí.</span><span class="sxs-lookup"><span data-stu-id="df1a2-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="df1a2-110">
                    <strong>Scénář</strong>
                </span><span class="sxs-lookup"><span data-stu-id="df1a2-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="df1a2-111">
                    <strong>Skutečné hodnoty vytvořené při potvrzení</strong>
                </span><span class="sxs-lookup"><span data-stu-id="df1a2-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="df1a2-112">Fakturace záloh</span><span class="sxs-lookup"><span data-stu-id="df1a2-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-113">Fakturovaný skutečný prodej typu <strong>Záloha</strong> je vytvořen pro částku v záloze.</span><span class="sxs-lookup"><span data-stu-id="df1a2-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-114">Nevyfakturovaný skutečný prodej se zápornou částkou zálohy, která má být použita k odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="df1a2-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="df1a2-115">Po úplném odsouhlasení zálohy na fakturu.</span><span class="sxs-lookup"><span data-stu-id="df1a2-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-116">Nevyfakturované prodejní storno zálohy, která byla vytvořena pro odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="df1a2-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="df1a2-117">Tato částka je kladná, protože má zrušit zápornou hodnotu, která byla vytvořen při fakturaci zálohy.</span><span class="sxs-lookup"><span data-stu-id="df1a2-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-118">Fakturovaný skutečný prodej na částku na této faktuře.</span><span class="sxs-lookup"><span data-stu-id="df1a2-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="df1a2-119">Po částečném odsouhlasení zálohy na fakturu.</span><span class="sxs-lookup"><span data-stu-id="df1a2-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-120">Nevyfakturované prodejní storno zálohy, která byla vytvořena pro odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="df1a2-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="df1a2-121">Tato částka je kladná, protože má zrušit zápornou hodnotu, která byla vytvořen při fakturaci zálohy.</span><span class="sxs-lookup"><span data-stu-id="df1a2-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-122">Fakturovaný skutečný prodej na částku na této faktuře.</span><span class="sxs-lookup"><span data-stu-id="df1a2-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-123">Záporný nevyfakturovaný skutečný prodej zbývající zálohy, která má být použita k odsouhlasení na budoucích fakturách.</span><span class="sxs-lookup"><span data-stu-id="df1a2-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="df1a2-124">Fakturace časové transakce bez jakýchkoli úprav konceptu faktury.</span><span class="sxs-lookup"><span data-stu-id="df1a2-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-125">Nevyfakturované storno prodeje pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="df1a2-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-126">Fakturovaný skutečný prodej pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="df1a2-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="df1a2-127">Fakturace časové transakce, která byla upravena, aby se snížilo množství.</span><span class="sxs-lookup"><span data-stu-id="df1a2-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-128">Nevyfakturované storno prodeje pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="df1a2-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-129">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za hodiny a částku na upraveném detailu řádku faktury, zrušení skutečného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="df1a2-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-130">Nový nevyfakturovaný skutečný prodej, který je neúčtovatelný za zbývající hodiny a částku po odečtení korigovaných čísel na upraveném detailu řádku faktury, zrušení skutečného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="df1a2-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="df1a2-131">Fakturace časové transakce, která byla upravena, aby se zvýšilo množství.</span><span class="sxs-lookup"><span data-stu-id="df1a2-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-132">Nevyfakturované storno prodeje pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="df1a2-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-133">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za hodiny a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="df1a2-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="df1a2-134">Fakturace transakce výdaje bez jakýchkoli úprav konceptu faktury.</span><span class="sxs-lookup"><span data-stu-id="df1a2-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-135">Nevyfakturované storno prodeje pro množství a částku při původním schválení výdaje.</span><span class="sxs-lookup"><span data-stu-id="df1a2-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-136">Fakturovaný skutečný prodej pro množství a částku při původním schválení výdaje</span><span class="sxs-lookup"><span data-stu-id="df1a2-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="df1a2-137">Fakturace transakce výdaje, která byla upravena, aby se snížilo množství.</span><span class="sxs-lookup"><span data-stu-id="df1a2-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-138">Nevyfakturované storno prodeje pro množství a částku při původním schválení výdaje.</span><span class="sxs-lookup"><span data-stu-id="df1a2-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-139">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="df1a2-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-140">Nový nevyfakturovaný skutečný prodej, který je neúčtovatelný za zbývající množství a částku po odečtení korigovaných čísel na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="df1a2-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="df1a2-141">Fakturace transakce výdaje, která byla upravena, aby se zvýšilo množství.</span><span class="sxs-lookup"><span data-stu-id="df1a2-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-142">Nevyfakturované storno prodeje pro množství a částku při původním schválení výdaje.</span><span class="sxs-lookup"><span data-stu-id="df1a2-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-143">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="df1a2-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="df1a2-144">Fakturace poplatku.</span><span class="sxs-lookup"><span data-stu-id="df1a2-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-145">Nevyfakturované storno prodeje pro částku poplatku na původním řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="df1a2-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-146">Fakturovaný skutečný prodej pro množství a částku na původním řádku deníku poplatku.</span><span class="sxs-lookup"><span data-stu-id="df1a2-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="df1a2-147">Fakturace milníku.</span><span class="sxs-lookup"><span data-stu-id="df1a2-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-148">Skutečně fakturovaný prodej pro část milníku v původním milníku na řádku smlouvy o projektu.</span><span class="sxs-lookup"><span data-stu-id="df1a2-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="df1a2-149">Fakturace řádku smlouvy založené na produktu.</span><span class="sxs-lookup"><span data-stu-id="df1a2-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="df1a2-150">Fakturovaný skutečný prodej na řádek produktu s množstvím a částkou pocházejícím z řádku smlouvy na základě produktu.</span><span class="sxs-lookup"><span data-stu-id="df1a2-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
