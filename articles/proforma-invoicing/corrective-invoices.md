---
title: Opravné faktury založené na projektu
description: Tento téma poskytuje informace o tom, jak vytvořit a potvrdit opravné faktury založené na projektu v Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012263"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="30a27-103">Opravné faktury založené na projektu</span><span class="sxs-lookup"><span data-stu-id="30a27-103">Corrective project-based invoices</span></span>

<span data-ttu-id="30a27-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="30a27-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="30a27-105">Potvrzenou fakturu za projekt lze opravit ke zpracování změn nebo kreditů podle dohody se zákazníkem a projektovým manažerem.</span><span class="sxs-lookup"><span data-stu-id="30a27-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="30a27-106">Chcete-li provést úpravy potvrzené faktury, otevřete potvrzenou fakturu a vyberte **Opravit tuto fakturu**.</span><span class="sxs-lookup"><span data-stu-id="30a27-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="30a27-107">Tento výběr není k dispozici, dokud není potvrzena faktura projektu nebo faktura založená na projektu obsahuje zálohy nebo zadržovací prostředky nebo odsouhlasení záloh nebo zadržovacích prostředků.</span><span class="sxs-lookup"><span data-stu-id="30a27-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="30a27-108">Z potvrzené faktury se vytvoří nový koncept faktury.</span><span class="sxs-lookup"><span data-stu-id="30a27-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="30a27-109">Všechny podrobnosti řádku faktury z dříve potvrzené faktury se zkopírují do nového konceptu.</span><span class="sxs-lookup"><span data-stu-id="30a27-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="30a27-110">Následuje několik klíčových bodů, které je třeba pochopit o podrobnostech řádku v nové opravené faktuře:</span><span class="sxs-lookup"><span data-stu-id="30a27-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="30a27-111">Všechna množství se aktualizují na nulu.</span><span class="sxs-lookup"><span data-stu-id="30a27-111">All quantities are updated to zero.</span></span> <span data-ttu-id="30a27-112">Dynamics 365 Project Operations předpokládá, že všechny fakturované položky jsou plně připsány.</span><span class="sxs-lookup"><span data-stu-id="30a27-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="30a27-113">V případě potřeby můžete tato množství ručně aktualizovat, aby odrážela množství, které je fakturováno, a nikoli množství, které je připsáno.</span><span class="sxs-lookup"><span data-stu-id="30a27-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="30a27-114">Na základě zadaného množství aplikace vypočítá připsané množství.</span><span class="sxs-lookup"><span data-stu-id="30a27-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="30a27-115">Tato částka se promítne do skutečných hodnot, které se vytvářejí při potvrzení opravené faktury.</span><span class="sxs-lookup"><span data-stu-id="30a27-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="30a27-116">Pokud provádíte změny v částce daně, musíte zadat správnou částku daně, nikoli částku daně, která je připisována.</span><span class="sxs-lookup"><span data-stu-id="30a27-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="30a27-117">Opravy milníků jsou vždy zpracovány jako plné kredity.</span><span class="sxs-lookup"><span data-stu-id="30a27-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="30a27-118">Údaje řádku faktury, které jsou opravami dalších již fakturovaných poplatků, mají pole **Oprava** nastaveno na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="30a27-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="30a27-119">Faktury, které mají opravené údaje řádku faktury, mají pole **Má opravy** nastaveno na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="30a27-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="30a27-120">Skutečné hodnoty vytvořené při potvrzení opravné faktury</span><span class="sxs-lookup"><span data-stu-id="30a27-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="30a27-121">V následující tabulce jsou uvedeny skutečné hodnoty, které jsou vytvořeny při potvrzení opravné faktury.</span><span class="sxs-lookup"><span data-stu-id="30a27-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="30a27-122">
                    <strong>Scénář</strong>
                </span><span class="sxs-lookup"><span data-stu-id="30a27-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="30a27-123">
                    <strong>Skutečné hodnoty vytvořené při potvrzení</strong>
                </span><span class="sxs-lookup"><span data-stu-id="30a27-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="30a27-124">Fakturace celého kreditu dříve fakturované časové transakce.</span><span class="sxs-lookup"><span data-stu-id="30a27-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-125">Vyfakturované storno prodeje pro hodiny a částku na původním detailu řádku faktury pro čas.</span><span class="sxs-lookup"><span data-stu-id="30a27-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-126">Nový skutečný nevyfakturovaný prodej pro hodiny a částku na původním detailu řádku faktury pro čas.</span><span class="sxs-lookup"><span data-stu-id="30a27-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="30a27-127">Fakturace částečného kreditu u časové transakce.</span><span class="sxs-lookup"><span data-stu-id="30a27-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-128">Vyfakturované storno prodeje pro hodiny a fakturovanou částku na původním detailu řádku faktury pro čas.</span><span class="sxs-lookup"><span data-stu-id="30a27-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-129">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za hodiny a částku na upraveném detailu řádku faktury, jeho storno a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="30a27-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-130">Skutečný nový nevyfakturovaný prodej, který je účtovatelný za zbývající hodiny a částku po odečtení opravených údajů v detailu řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="30a27-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="30a27-131">Fakturace celého kreditu dříve fakturované transakce výdaje.</span><span class="sxs-lookup"><span data-stu-id="30a27-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-132">Vyfakturované storno prodeje pro množství a částku na původním detailu řádku faktury pro výdaj.</span><span class="sxs-lookup"><span data-stu-id="30a27-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-133">Nový nevyfakturovaný skutečný prodej pro množství a částku na původním detailu řádku faktury pro výdaj.</span><span class="sxs-lookup"><span data-stu-id="30a27-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="30a27-134">Fakturace částečného kreditu dříve fakturované transakce výdaje.</span><span class="sxs-lookup"><span data-stu-id="30a27-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-135">Vyfakturované storno prodeje pro množství a fakturovanou částku na původním detailu řádku faktury pro výdaj.</span><span class="sxs-lookup"><span data-stu-id="30a27-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-136">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na opraveném detailu řádku faktury, jeho storno a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="30a27-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-137">Skutečný nový nevyfakturovaný prodej, který je účtovatelný za zbývající množství a částku po odečtení opravených údajů v detailu řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="30a27-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="30a27-138">Fakturace celého kreditu dříve fakturované transakce materiálu.</span><span class="sxs-lookup"><span data-stu-id="30a27-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-139">Vyfakturované vrácení prodeje a množství a částky údajích původního řádku faktury pro materiál.</span><span class="sxs-lookup"><span data-stu-id="30a27-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-140">Nová neyfakturovaná skutečná hodnota prodeje a množství a částky údajích původního řádku faktury pro materiál.</span><span class="sxs-lookup"><span data-stu-id="30a27-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="30a27-141">Fakturace částečného kreditu u materiálové transakce.</span><span class="sxs-lookup"><span data-stu-id="30a27-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-142">Vyfakturované vrácení prodeje a množství a fakturované částky údajích původního řádku faktury pro materiál.</span><span class="sxs-lookup"><span data-stu-id="30a27-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-143">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku v údaji upraveného řádku faktury, jeho zrušení a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="30a27-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-144">Skutečný nový nevyfakturovaný prodej, který je účtovatelný za zbývající množství a částku po odečtení opravených údajů v detailu řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="30a27-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="30a27-145">Fakturace celého kreditu dříve fakturované transakce poplatku.</span><span class="sxs-lookup"><span data-stu-id="30a27-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-146">Vyfakturované storno prodeje pro množství a částku na původním detailu řádku faktury pro poplatek.</span><span class="sxs-lookup"><span data-stu-id="30a27-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-147">Nový nevyfakturovaný skutečný prodej pro množství a částku na původním detailu řádku faktury pro poplatek.</span><span class="sxs-lookup"><span data-stu-id="30a27-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="30a27-148">Fakturace částečného kreditu dříve fakturované transakce poplatku.</span><span class="sxs-lookup"><span data-stu-id="30a27-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-149">Vyfakturované storno prodeje pro množství a fakturovanou částku na původním detailu řádku faktury pro poplatek.</span><span class="sxs-lookup"><span data-stu-id="30a27-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-150">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném opraveném detailu řádku faktury, jeho storno a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="30a27-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="30a27-151">Fakturace celého kreditu dříve fakturovaného milníku.</span><span class="sxs-lookup"><span data-stu-id="30a27-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-152">Vyfakturované storno prodeje pro částku na původním detailu řádku faktury pro milník.</span><span class="sxs-lookup"><span data-stu-id="30a27-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="30a27-153">Stav faktury milníku je aktualizován z <b>Zákaznická faktura zaúčtována</b> na <b>Připraveno k fakturaci</b>.</span><span class="sxs-lookup"><span data-stu-id="30a27-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="30a27-154">Fakturace částečného kreditu dříve fakturovaného milníku.</span><span class="sxs-lookup"><span data-stu-id="30a27-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="30a27-155">Tento scénář není podporován.</span><span class="sxs-lookup"><span data-stu-id="30a27-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
