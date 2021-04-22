---
title: Vytvoření opravných faktur založených na projektu
description: Tento téma poskytuje informace o opravných fakturách v Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788842"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="27937-103">Vytvoření opravných faktur založených na projektu</span><span class="sxs-lookup"><span data-stu-id="27937-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="27937-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="27937-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="27937-105">Potvrzenou fakturu za projekt lze opravit ke zpracování změn nebo kreditů podle dohody se zákazníkem a projektovým manažerem.</span><span class="sxs-lookup"><span data-stu-id="27937-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="27937-106">Chcete-li provést úpravy potvrzené faktury, otevřete potvrzenou fakturu a vyberte **Opravit tuto fakturu**.</span><span class="sxs-lookup"><span data-stu-id="27937-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="27937-107">Tento výběr není k dispozici, dokud nebude potvrzena faktura projektu.</span><span class="sxs-lookup"><span data-stu-id="27937-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="27937-108">Z potvrzené faktury se vytvoří nový koncept faktury.</span><span class="sxs-lookup"><span data-stu-id="27937-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="27937-109">Všechny podrobnosti řádku faktury z dříve potvrzené faktury se zkopírují do nového konceptu.</span><span class="sxs-lookup"><span data-stu-id="27937-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="27937-110">Následuje několik klíčových bodů, které vám pomohou pochopit více údajů řádku v nové opravené faktuře:</span><span class="sxs-lookup"><span data-stu-id="27937-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="27937-111">Všechna množství se aktualizují na nulu.</span><span class="sxs-lookup"><span data-stu-id="27937-111">All quantities are updated to zero.</span></span> <span data-ttu-id="27937-112">Předpokládá to, že všechny fakturované položky jsou plně připsány.</span><span class="sxs-lookup"><span data-stu-id="27937-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="27937-113">V případě potřeby můžete tato množství ručně aktualizovat, aby odrážela množství, které je fakturováno, a nikoli množství, které je připsáno.</span><span class="sxs-lookup"><span data-stu-id="27937-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="27937-114">Na základě zadaného množství aplikace vypočítá připsané množství.</span><span class="sxs-lookup"><span data-stu-id="27937-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="27937-115">Tato částka se promítne do skutečných hodnot, které se vytvářejí při potvrzení opravené faktury.</span><span class="sxs-lookup"><span data-stu-id="27937-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="27937-116">Pokud provádíte změny v částce daně, musíte zadat správnou částku daně, nikoli částku daně, která je připisována.</span><span class="sxs-lookup"><span data-stu-id="27937-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="27937-117">Opravy milníků jsou vždy zpracovány jako plné kredity.</span><span class="sxs-lookup"><span data-stu-id="27937-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="27937-118">Částky záloh lze opravit, pokud byla zákazníkovi fakturována nesprávná částka.</span><span class="sxs-lookup"><span data-stu-id="27937-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="27937-119">Odsouhlasení záloh lze opravit, pokud byla použita nesprávná částka k vyrovnání proti poplatkům na dříve potvrzené faktuře.</span><span class="sxs-lookup"><span data-stu-id="27937-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="27937-120">Údaje řádku faktury, které jsou opravami dalších již fakturovaných poplatků, mají pole **Oprava** nastaveno na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="27937-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="27937-121">Faktury, které opravují podrobnosti řádku faktury, mají pole s názvem **Má opravy**, které je také nastaveno na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="27937-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="27937-122">Skutečné hodnoty vytvořené při potvrzení opravné faktury</span><span class="sxs-lookup"><span data-stu-id="27937-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="27937-123">V následující tabulce jsou uvedeny skutečné hodnoty, které jsou vytvořeny při potvrzení opravné faktury.</span><span class="sxs-lookup"><span data-stu-id="27937-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="27937-124">
                    <strong>Scénář</strong>
                </span><span class="sxs-lookup"><span data-stu-id="27937-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="27937-125">
                    <strong>Skutečné hodnoty vytvořené při potvrzení</strong>
                </span><span class="sxs-lookup"><span data-stu-id="27937-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="27937-126">Potvrďte opravu fakturované zálohy.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="27937-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-127">Nevyfakturované prodejní storno zálohy, která byla vytvořena pro odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="27937-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="27937-128">Tato částka je kladná, protože má zrušit zápornou hodnotu, která byla vytvořen při fakturaci zálohy.</span><span class="sxs-lookup"><span data-stu-id="27937-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-129">Skutečná hodnota storna fakturovaného prodeje je vytvořena pro částku v záloze, aby se stornoval původní fakturovaný prodej.</span><span class="sxs-lookup"><span data-stu-id="27937-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-130">Nový fakturovaný skutečný prodej je vytvořen pro částku opraveného řádku faktury na základě zálohy.</span><span class="sxs-lookup"><span data-stu-id="27937-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-131">Nevyfakturovaný skutečný prodej se zápornou částkou opraveného řádku faktury na základě zálohy, který bude použit k odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="27937-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="27937-132">Potvrzení opravy dříve odsouhlasené zálohy.</span><span class="sxs-lookup"><span data-stu-id="27937-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-133">Nevyfakturované prodejní storno zálohy, která byla vytvořena pro odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="27937-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="27937-134">Tato částka je kladná a má zrušit zápornou hodnotu, která byla vytvořena při předchozím odsouhlasení.</span><span class="sxs-lookup"><span data-stu-id="27937-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-135">Skutečné storno fakturovaného prodeje na částku na předchozí faktuře.</span><span class="sxs-lookup"><span data-stu-id="27937-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-136">Nový fakturovaný skutečný prodej pro částku opravené zálohy, který je použit na opravenou fakturu.</span><span class="sxs-lookup"><span data-stu-id="27937-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-137">Nevyfakturovaný skutečný prodej se zápornou částkou z opraveného zbytku zálohy, který bude použit k odsouhlasení na pozdějších fakturách.</span><span class="sxs-lookup"><span data-stu-id="27937-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="27937-138">Fakturace celého kreditu dříve fakturované časové transakce.</span><span class="sxs-lookup"><span data-stu-id="27937-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-139">Vyfakturované storno prodeje pro hodiny a částku na původním detailu řádku faktury pro čas.</span><span class="sxs-lookup"><span data-stu-id="27937-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-140">Nový skutečný nevyfakturovaný prodej pro hodiny a částku na původním detailu řádku faktury pro čas.</span><span class="sxs-lookup"><span data-stu-id="27937-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="27937-141">Fakturace částečného kreditu u časové transakce.</span><span class="sxs-lookup"><span data-stu-id="27937-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-142">Vyfakturované storno prodeje pro hodiny a fakturovanou částku na původním detailu řádku faktury pro čas.</span><span class="sxs-lookup"><span data-stu-id="27937-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-143">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za hodiny a částku na upraveném detailu řádku faktury, jeho storno a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="27937-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-144">Skutečný nový nevyfakturovaný prodej, který je účtovatelný za zbývající hodiny a částku po odečtení opravených údajů v detailu řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="27937-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="27937-145">Fakturace celého kreditu dříve fakturované transakce výdaje.</span><span class="sxs-lookup"><span data-stu-id="27937-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-146">Vyfakturované storno prodeje pro množství a částku na původním detailu řádku faktury pro výdaj.</span><span class="sxs-lookup"><span data-stu-id="27937-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-147">Nový nevyfakturovaný skutečný prodej pro množství a částku na původním detailu řádku faktury pro výdaj.</span><span class="sxs-lookup"><span data-stu-id="27937-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="27937-148">Fakturace částečného kreditu dříve fakturované transakce výdaje.</span><span class="sxs-lookup"><span data-stu-id="27937-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-149">Vyfakturované storno prodeje pro množství a fakturovanou částku na původním detailu řádku faktury pro výdaj.</span><span class="sxs-lookup"><span data-stu-id="27937-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-150">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na opraveném detailu řádku faktury, jeho storno a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="27937-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-151">Skutečný nový nevyfakturovaný prodej, který je účtovatelný za zbývající množství a částku po odečtení opravených údajů v detailu řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="27937-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="27937-152">Fakturace celého kreditu dříve fakturované transakce poplatku.</span><span class="sxs-lookup"><span data-stu-id="27937-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-153">Vyfakturované storno prodeje pro množství a částku na původním detailu řádku faktury pro poplatek.</span><span class="sxs-lookup"><span data-stu-id="27937-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-154">Nový nevyfakturovaný skutečný prodej pro množství a částku na původním detailu řádku faktury pro poplatek.</span><span class="sxs-lookup"><span data-stu-id="27937-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="27937-155">Fakturace částečného kreditu dříve fakturované transakce poplatku.</span><span class="sxs-lookup"><span data-stu-id="27937-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-156">Vyfakturované storno prodeje pro množství a fakturovanou částku na původním detailu řádku faktury pro poplatek.</span><span class="sxs-lookup"><span data-stu-id="27937-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-157">Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném opraveném detailu řádku faktury, jeho storno a ekvivalentní fakturovaný skutečný prodej.</span><span class="sxs-lookup"><span data-stu-id="27937-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="27937-158">Fakturace celého kreditu dříve fakturovaného milníku.</span><span class="sxs-lookup"><span data-stu-id="27937-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-159">Vyfakturované storno prodeje pro částku na původním detailu řádku faktury pro milník.</span><span class="sxs-lookup"><span data-stu-id="27937-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="27937-160">Stav faktury milníku je aktualizován z <b>Zákaznická faktura zaúčtována</b> na <b>Připraveno k fakturaci</b>.</span><span class="sxs-lookup"><span data-stu-id="27937-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="27937-161">Fakturace částečného kreditu dříve fakturovaného milníku.</span><span class="sxs-lookup"><span data-stu-id="27937-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="27937-162">Nepodporováno</span><span class="sxs-lookup"><span data-stu-id="27937-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
