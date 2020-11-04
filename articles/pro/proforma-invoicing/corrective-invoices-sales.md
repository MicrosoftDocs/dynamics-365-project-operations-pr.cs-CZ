---
title: Kredity a opravené faktury
description: Toto téma poskytuje informace o opravených fakturách v aplikaci Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2187627439d42b37222dce0a491c62dafc358d5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073891"
---
# <a name="credits-and-corrected-invoices"></a><span data-ttu-id="0d7dc-103">Kredity a opravené faktury</span><span class="sxs-lookup"><span data-stu-id="0d7dc-103">Credits and corrected invoices</span></span>

<span data-ttu-id="0d7dc-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="0d7dc-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0d7dc-105">Potvrzenou fakturu za projekt lze opravit ke zpracování změn nebo kreditů podle dohody se zákazníkem a projektovým manažerem.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="0d7dc-106">Chcete-li provést úpravy potvrzené faktury, otevřete potvrzenou fakturu a vyberte **Opravit tuto fakturu**.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="0d7dc-107">Tento výběr není k dispozici, dokud nebude potvrzena faktura projektu.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="0d7dc-108">Z potvrzené faktury se vytvoří nový koncept faktury.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="0d7dc-109">Všechny podrobnosti řádku faktury z dříve potvrzené faktury se zkopírují do nového konceptu.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="0d7dc-110">Následuje několik klíčových bodů, které je třeba pochopit o podrobnostech řádku v nové opravené faktuře:</span><span class="sxs-lookup"><span data-stu-id="0d7dc-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="0d7dc-111">Všechna množství se aktualizují na nulu.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-111">All quantities are updated to zero.</span></span> <span data-ttu-id="0d7dc-112">Aplikace předpokládá, že všechny fakturované položky jsou plně připsány.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="0d7dc-113">V případě potřeby můžete tato množství ručně aktualizovat, aby odrážela množství, které je fakturováno, a nikoli množství, které je připsáno.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="0d7dc-114">Na základě zadaného množství aplikace vypočítá připsané množství.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="0d7dc-115">Tato částka se promítne do skutečných hodnot, které se vytvářejí při potvrzení opravené faktury.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="0d7dc-116">Pokud provádíte změny v částce daně, musíte zadat správnou částku daně, nikoli částku daně, která je připisována.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="0d7dc-117">Dříve potvrzené řádky smlouvy na základě produktu se nekopírují.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="0d7dc-118">Zpracování oprav na projektové faktuře založené na produktu není podporováno.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="0d7dc-119">Opravy milníků jsou vždy zpracovány jako plné kredity.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="0d7dc-120">Částky záloh lze opravit, pokud byla zákazníkovi fakturována nesprávná částka.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="0d7dc-121">Odsouhlasení záloh lze opravit, pokud byla použita nesprávná částka k vyrovnání proti poplatkům na dříve potvrzené faktuře.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d7dc-122">Podrobnosti řádku faktury, které jsou opravami dalších již fakturovaných poplatků, mají pole **Oprava** nastavený na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="0d7dc-123">Faktury, které opravují podrobnosti řádku faktury, mají pole s názvem **Má opravy** , které je také nastaveno na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="0d7dc-124">Skutečné hodnoty vytvořené při potvrzení opravné faktury:</span><span class="sxs-lookup"><span data-stu-id="0d7dc-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="0d7dc-125">Níže jsou uvedeny skutečné hodnoty vytvořené aplikací při potvrzení opravy na základě operací provedených na konceptu opravné faktury před potvrzením.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="0d7dc-126">
                    <strong>Scénář</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d7dc-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="0d7dc-127">
                    <strong>Skutečné hodnoty vytvořené při potvrzení</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d7dc-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="0d7dc-128">Potvrďte opravu fakturované zálohy.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d7dc-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-129">Nevyfakturované prodejní storno zálohy, která byla vytvořena pro odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="0d7dc-130">Tato částka je kladná, protože má zrušit zápornou hodnotu, která byla vytvořen při fakturaci zálohy.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-131">Skutečná hodnota storna fakturovaného prodeje je vytvořena pro částku v záloze, aby se stornoval původní fakturovaný prodej.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-132">Nový fakturovaný skutečný prodej je vytvořen pro částku opraveného řádku faktury na základě zálohy.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-133">Nevyfakturovaný skutečný prodej se zápornou částkou opraveného řádku faktury na základě zálohy, který bude použit k odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="0d7dc-134">Potvrzení opravy dříve odsouhlasené zálohy.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-135">Nevyfakturované prodejní storno zálohy, která byla vytvořena pro odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="0d7dc-136">Tato částka je kladná a má zrušit zápornou hodnotu, která byla vytvořena při předchozím odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-137">Skutečné storno fakturovaného prodeje na částku na předchozí faktuře.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-138">Nový fakturovaný skutečný prodej pro částku opravené zálohy, který je použit na opravenou fakturu.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-139">Nevyfakturovaný skutečný prodej se zápornou částkou z opraveného zbytku zálohy, který bude použit k odsouhlasení na pozdějších fakturách.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0d7dc-140">Fakturace celého kreditu dříve fakturované časové transakce.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-141">Vyfakturované storno prodeje pro hodiny a částku na původním detailu řádku faktury pro čas.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-142">Nový skutečný nevyfakturovaný prodej pro hodiny a částku na původním detailu řádku faktury pro čas.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0d7dc-143">Fakturace částečného kreditu u časové transakce.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-144">Vyfakturované storno prodeje pro hodiny a fakturovanou částku na původním detailu řádku faktury pro čas.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-145">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za hodiny a částku na upraveném detailu řádku faktury, jeho storno a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-146">Skutečný nový nevyfakturovaný prodej, který je účtovatelný za zbývající hodiny a částku po odečtení opravených údajů v detailu řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0d7dc-147">Fakturace celého kreditu dříve fakturované transakce výdaje.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-148">Vyfakturované storno prodeje pro množství a částku na původním detailu řádku faktury pro výdaj.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-149">Nový nevyfakturovaný skutečný prodej pro množství a částku na původním detailu řádku faktury pro výdaj.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0d7dc-150">Fakturace částečného kreditu dříve fakturované transakce výdaje.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-151">Vyfakturované storno prodeje pro množství a fakturovanou částku na původním detailu řádku faktury pro výdaj.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-152">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na opraveném detailu řádku faktury, jeho storno a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-153">Skutečný nový nevyfakturovaný prodej, který je účtovatelný za zbývající množství a částku po odečtení opravených údajů v detailu řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0d7dc-154">Fakturace celého kreditu dříve fakturované transakce poplatku.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-155">Vyfakturované storno prodeje pro množství a částku na původním detailu řádku faktury pro poplatek.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-156">Nový nevyfakturovaný skutečný prodej pro množství a částku na původním detailu řádku faktury pro poplatek.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0d7dc-157">Fakturace částečného kreditu dříve fakturované transakce poplatku.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-158">Vyfakturované storno prodeje pro množství a fakturovanou částku na původním detailu řádku faktury pro poplatek.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-159">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném opraveném detailu řádku faktury, jeho storno a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0d7dc-160">Fakturace celého kreditu dříve fakturovaného milníku.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-161">Vyfakturované storno prodeje pro částku na původním detailu řádku faktury pro milník.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="0d7dc-162">Milník faktura nebo stav fakturace na řádku smlouvy projektu je aktualizován na **Připraveno k fakturaci**.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0d7dc-163">Fakturace částečného kreditu dříve fakturovaného milníku.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-164">Nepodporováno</span><span class="sxs-lookup"><span data-stu-id="0d7dc-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0d7dc-165">Kredity a opravy dříve fakturovaného řádku smlouvy na základě produktu.</span><span class="sxs-lookup"><span data-stu-id="0d7dc-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0d7dc-166">Nepodporováno</span><span class="sxs-lookup"><span data-stu-id="0d7dc-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>
