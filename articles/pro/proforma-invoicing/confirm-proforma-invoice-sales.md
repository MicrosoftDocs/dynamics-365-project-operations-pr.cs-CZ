---
title: Potvrzení proforma faktury – omezené
description: Toto téma poskytuje informace o tom, jak potvrzovat proforma faktury v aplikaci Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176513"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="431da-103">Potvrzení proforma faktury – omezené</span><span class="sxs-lookup"><span data-stu-id="431da-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="431da-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="431da-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="431da-105">Po potvrzení proforma faktury se stav projektové faktury aktualizuje na **Potvrzeno**.</span><span class="sxs-lookup"><span data-stu-id="431da-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="431da-106">Když je faktura potvrzena, stane se pouze pro čtení.</span><span class="sxs-lookup"><span data-stu-id="431da-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="431da-107">Do budoucna bude možné fakturu opravit, pouze pokud dojde k opravám nebo kreditům zahájeným zákazníkem nebo pokud je faktura označena jako zaplacená.</span><span class="sxs-lookup"><span data-stu-id="431da-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="431da-108">V následující tabulce jsou uvedeny skutečné hodnoty vytvořené systémem.</span><span class="sxs-lookup"><span data-stu-id="431da-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="431da-109">Tyto skutečné hodnoty se vytvoří, když se na faktuře konceptu projektu provedou určité operace, než se potvrdí.</span><span class="sxs-lookup"><span data-stu-id="431da-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="431da-110">
                    <strong>Scénář</strong>
                </span><span class="sxs-lookup"><span data-stu-id="431da-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="431da-111">
                    <strong>Skutečné hodnoty vytvořené při potvrzení</strong>
                </span><span class="sxs-lookup"><span data-stu-id="431da-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="431da-112">Fakturace záloh</span><span class="sxs-lookup"><span data-stu-id="431da-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-113">Fakturovaný skutečný prodej typu <strong>Záloha</strong> je vytvořen pro částku v záloze.</span><span class="sxs-lookup"><span data-stu-id="431da-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-114">Nevyfakturovaný skutečný prodej se zápornou částkou zálohy, která má být použita k odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="431da-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="431da-115">Po úplném odsouhlasení zálohy na fakturu.</span><span class="sxs-lookup"><span data-stu-id="431da-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-116">Nevyfakturované prodejní storno zálohy, která byla vytvořena pro odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="431da-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="431da-117">Tato částka je kladná, protože má zrušit zápornou hodnotu, která byla vytvořen při fakturaci zálohy.</span><span class="sxs-lookup"><span data-stu-id="431da-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-118">Fakturovaný skutečný prodej na částku na této faktuře.</span><span class="sxs-lookup"><span data-stu-id="431da-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="431da-119">Po částečném odsouhlasení zálohy na fakturu.</span><span class="sxs-lookup"><span data-stu-id="431da-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-120">Nevyfakturované prodejní storno zálohy, která byla vytvořena pro odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="431da-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="431da-121">Tato částka je kladná, protože má zrušit zápornou hodnotu, která byla vytvořen při fakturaci zálohy.</span><span class="sxs-lookup"><span data-stu-id="431da-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-122">Fakturovaný skutečný prodej na částku na této faktuře.</span><span class="sxs-lookup"><span data-stu-id="431da-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-123">Záporný nevyfakturovaný skutečný prodej zbývající zálohy, která má být použita k odsouhlasení na budoucích fakturách.</span><span class="sxs-lookup"><span data-stu-id="431da-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="431da-124">Fakturace časové transakce bez jakýchkoli úprav konceptu faktury.</span><span class="sxs-lookup"><span data-stu-id="431da-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-125">Nevyfakturované storno prodeje pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="431da-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-126">Fakturovaný skutečný prodej pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="431da-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="431da-127">Fakturace časové transakce, která byla upravena, aby se snížilo množství.</span><span class="sxs-lookup"><span data-stu-id="431da-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-128">Nevyfakturované storno prodeje pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="431da-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-129">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za hodiny a částku na upraveném detailu řádku faktury, zrušení skutečného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="431da-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-130">Nový nevyfakturovaný skutečný prodej, který je neúčtovatelný za zbývající hodiny a částku po odečtení korigovaných čísel na upraveném detailu řádku faktury, zrušení skutečného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="431da-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="431da-131">Fakturace časové transakce, která byla upravena, aby se zvýšilo množství.</span><span class="sxs-lookup"><span data-stu-id="431da-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-132">Nevyfakturované storno prodeje pro hodiny a částku při původním schválení času.</span><span class="sxs-lookup"><span data-stu-id="431da-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-133">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za hodiny a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="431da-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="431da-134">Fakturace transakce výdaje bez jakýchkoli úprav konceptu faktury.</span><span class="sxs-lookup"><span data-stu-id="431da-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-135">Nevyfakturované storno prodeje pro množství a částku při původním schválení výdaje.</span><span class="sxs-lookup"><span data-stu-id="431da-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-136">Fakturovaný skutečný prodej pro množství a částku při původním schválení výdaje</span><span class="sxs-lookup"><span data-stu-id="431da-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="431da-137">Fakturace transakce výdaje, která byla upravena, aby se snížilo množství.</span><span class="sxs-lookup"><span data-stu-id="431da-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-138">Nevyfakturované storno prodeje pro množství a částku při původním schválení výdaje.</span><span class="sxs-lookup"><span data-stu-id="431da-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-139">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="431da-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-140">Nový nevyfakturovaný skutečný prodej, který je neúčtovatelný za zbývající množství a částku po odečtení korigovaných čísel na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="431da-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="431da-141">Fakturace transakce výdaje, která byla upravena, aby se zvýšilo množství.</span><span class="sxs-lookup"><span data-stu-id="431da-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-142">Nevyfakturované storno prodeje pro množství a částku při původním schválení výdaje.</span><span class="sxs-lookup"><span data-stu-id="431da-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-143">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="431da-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="431da-144">Fakturace poplatku.</span><span class="sxs-lookup"><span data-stu-id="431da-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-145">Nevyfakturované storno prodeje pro částku poplatku na původním řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="431da-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-146">Fakturovaný skutečný prodej pro množství a částku na původním řádku deníku poplatku.</span><span class="sxs-lookup"><span data-stu-id="431da-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="431da-147">Fakturace milníku.</span><span class="sxs-lookup"><span data-stu-id="431da-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-148">Skutečně fakturovaný prodej pro část milníku v původním milníku na řádku smlouvy o projektu.</span><span class="sxs-lookup"><span data-stu-id="431da-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="431da-149">Fakturace řádku smlouvy založené na produktu.</span><span class="sxs-lookup"><span data-stu-id="431da-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="431da-150">Fakturovaný skutečný prodej na řádek produktu s množstvím a částkou pocházejícím z řádku smlouvy na základě produktu.</span><span class="sxs-lookup"><span data-stu-id="431da-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
