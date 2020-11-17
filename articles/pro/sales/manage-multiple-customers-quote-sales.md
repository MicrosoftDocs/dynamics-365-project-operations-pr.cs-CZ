---
title: Správa více zákazníků v projektových nabídkách
description: Toto téma poskytuje informace o práci na nabídkách s více zákazníky, kteří budou financovat projekt. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 656418ab99db46455195f70c38b6f5fa13c30755
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073680"
---
# <a name="managing-multiple-customers-on-project-quotes-sales"></a><span data-ttu-id="13fa8-104">Správa více zákazníků v projektových nabídkách (Sales)</span><span class="sxs-lookup"><span data-stu-id="13fa8-104">Managing multiple customers on project quotes (Sales)</span></span>

<span data-ttu-id="13fa8-105">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="13fa8-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="13fa8-106">Projektové nabídky podporují scénář, kdy návrh zahrnuje více zákazníků, kteří budou obchod financovat.</span><span class="sxs-lookup"><span data-stu-id="13fa8-106">Project quotes support the scenario where the proposal involves multiple customers who will fund the deal.</span></span> <span data-ttu-id="13fa8-107">Karta **Souhrn** nabídky obsahuje pole **Potencionální zákazník** , které identifikuje primárního zákazníka obchodu.</span><span class="sxs-lookup"><span data-stu-id="13fa8-107">The **Summary** tab of the Quote has the **Potential customer** field that identifies the primary customer of the deal.</span></span> <span data-ttu-id="13fa8-108">Další zákazníky pro obchod lze nastavit na kartě **Zákazníci** projektové nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-108">Other customers for the deal can be set up on the **Customers** tab of the project quote.</span></span>

<span data-ttu-id="13fa8-109">Všichni zákazníci nabídky na kartě **Zákazníci** projektové nabídky jsou uvedeni jako výchozí zákazníci řádku nabídky na všech **nových** řádcích nabídek založených na projektu vytvořených pro nabídku.</span><span class="sxs-lookup"><span data-stu-id="13fa8-109">All quote customers on the **Customers** tab of the project quote default as quote line customers on any **new** project-based quote lines created for the quote.</span></span> <span data-ttu-id="13fa8-110">Žádné stávající řádky nabídek založených na projektu nezdědí nové záznamy zákazníků nabídky vytvořené po nich.</span><span class="sxs-lookup"><span data-stu-id="13fa8-110">Any existing project-based quote lines will not inherit new quote customer records created after them.</span></span>

<span data-ttu-id="13fa8-111">Řádky nabídky založené na projektu jsou automaticky přidruženy k primárnímu zákazníkovi, který je také zákazníkem v poli **Potencionální zákazník** na kartě **Souhrn** nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-111">Product-based quote lines are automatically associated to the primary customer who is also the customer in the **Potential Customer** field on the **Summary** tab of the quote.</span></span>

<span data-ttu-id="13fa8-112">Zákazníky nabídky a zákazníky řádku nabídky lze přidávat, aktualizovat nebo odstraňovat kdykoli před získáním nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-112">Quote customers and quote line customers can be added, updated, or deleted at any time before the quote is won.</span></span>

## <a name="concept-of-a-primary-customer"></a><span data-ttu-id="13fa8-113">Koncept primárního zákazníka</span><span class="sxs-lookup"><span data-stu-id="13fa8-113">Concept of a primary customer</span></span>

<span data-ttu-id="13fa8-114">Zákazník uvedený na kartě Souhrn projektové nabídky jako potenciální zákazník je primárním zákazníkem nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-114">The customer who is on the summary tab of the project quote as the potential customer is the primary customer of the quote.</span></span> <span data-ttu-id="13fa8-115">Když se pokusíte odstranit primárního zákazníka ze seznamu zákazníků v nabídce, zobrazí se chyba se zprávou, že záznam primárního zákazníka v nabídce nelze odstranit.</span><span class="sxs-lookup"><span data-stu-id="13fa8-115">When you try to delete the primary customer from customers list on quote, you will see an error that a primary customer record on a quote cannot be deleted.</span></span>

<span data-ttu-id="13fa8-116">Primární zákazník by neměl být aktualizován ze seznamu zákazníků v nabídce.</span><span class="sxs-lookup"><span data-stu-id="13fa8-116">The primary customer shouldn't be updated from the customer list on the quote.</span></span> <span data-ttu-id="13fa8-117">Primárního zákazníka však můžete ovlivnit změnou potenciálního zákazníka na kartě **Souhrn** nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-117">However, you can influence the primary customer by changing the potential customer on the **Summary** tab of the quote.</span></span> <span data-ttu-id="13fa8-118">Když je toto pole aktualizováno na kartě **Souhrn nabídky** , nově vybraný potenciální zákazník je přidán jako nový zákazník nabídky s nastaveným příznakem **Primární**.</span><span class="sxs-lookup"><span data-stu-id="13fa8-118">When this field is updated on the **Quote Summary** , the newly selected potential customer is added as a new quote customer with the **Primary** flag set.</span></span> <span data-ttu-id="13fa8-119">Starý potenciální zákazník bude i nadále zákazníkem v nabídce.</span><span class="sxs-lookup"><span data-stu-id="13fa8-119">The old potential customer will still be a customer on the quote.</span></span>

## <a name="create-update-or-delete-a-quote-customer-record"></a><span data-ttu-id="13fa8-120">Vytvoření, aktualizace nebo odstranění záznamu zákazníka nabídky</span><span class="sxs-lookup"><span data-stu-id="13fa8-120">Create, Update, or Delete a quote customer record</span></span>

<span data-ttu-id="13fa8-121">Zákazník nabídky může být vytvořen, aktualizován nebo odstraněn na kartě **Zákazníci nabídky** na stránce **Nabídka**.</span><span class="sxs-lookup"><span data-stu-id="13fa8-121">A quote customer can be created, updated, or deleted from the **Quote customers** tab on the **Quote** page.</span></span> <span data-ttu-id="13fa8-122">Pole uvedená v následující tabulce se nacházejí v záznamu zákazníka nabídky patřícího do projektové nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-122">The fields listed in the following table are on the quote customer record of a project quote.</span></span>

| <span data-ttu-id="13fa8-123">**Pole**</span><span class="sxs-lookup"><span data-stu-id="13fa8-123">**Field**</span></span> | <span data-ttu-id="13fa8-124">**Umístění**</span><span class="sxs-lookup"><span data-stu-id="13fa8-124">**Location**</span></span> | <span data-ttu-id="13fa8-125">**Relevance, účel a vedení**</span><span class="sxs-lookup"><span data-stu-id="13fa8-125">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="13fa8-126">**Dopad na následné složky**</span><span class="sxs-lookup"><span data-stu-id="13fa8-126">**Downstream impact**</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="13fa8-127">Účet</span><span class="sxs-lookup"><span data-stu-id="13fa8-127">Account</span></span> | <span data-ttu-id="13fa8-128">Upravitelná mřížka na kartě **Zákazníci nabídky** a formuláře **Hlavní** a **Vytvořit** pro zákazníka nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-128">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="13fa8-129">Vypíše seznam všech aktivních účtů.</span><span class="sxs-lookup"><span data-stu-id="13fa8-129">Lists all the active accounts.</span></span> <span data-ttu-id="13fa8-130">Po vytvoření záznamu je toto pole uzamčeno.</span><span class="sxs-lookup"><span data-stu-id="13fa8-130">This field is locked after the record is created.</span></span> <span data-ttu-id="13fa8-131">Chcete-li jej aktualizovat, odstraňte záznam a znovu jej vytvořte.</span><span class="sxs-lookup"><span data-stu-id="13fa8-131">If you want to update it, delete the record, and re-create it.</span></span> <span data-ttu-id="13fa8-132">Pokud jste zaznamenali nějaké skutečnosti nebo pokud je záznam zákazníka nabídky primárním zákazníkem, budete moci záznam odstranit.</span><span class="sxs-lookup"><span data-stu-id="13fa8-132">If you have recorded any actuals, or if the quote customer record is a primary customer, you will be allowed to delete the record.</span></span> | <span data-ttu-id="13fa8-133">Po vytvoření řádku nabídky se zákazníci nabídky zkopírují k zákazníkům řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-133">Quote customers are copied over as quote line customers when a quote line is created.</span></span> <span data-ttu-id="13fa8-134">Po získání nabídky se také zákazníci nabídky zkopírují k zákazníkům projektové smlouvy.</span><span class="sxs-lookup"><span data-stu-id="13fa8-134">Quote customers are also copied over to the project contract customers when a quote is won.</span></span> |
| <span data-ttu-id="13fa8-135">Procento rozdělení fakturace</span><span class="sxs-lookup"><span data-stu-id="13fa8-135">Billing split percent</span></span> | <span data-ttu-id="13fa8-136">Upravitelná mřížka na kartě **Zákazníci nabídky** a formuláře **Hlavní** a **Vytvořit** pro zákazníka nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-136">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="13fa8-137">Představuje procento z každé nevyfakturované prodejní transakce, která bude připsána tomuto zákazníkovi nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-137">Represent the percentage of each unbilled sales transaction that will be attributed to this quote customer.</span></span> | <span data-ttu-id="13fa8-138">Zkopírováno do nových řádků nabídek a do zákazníků projektové smlouvy.</span><span class="sxs-lookup"><span data-stu-id="13fa8-138">Copied over to new quote lines and to project contract customers.</span></span> |
| <span data-ttu-id="13fa8-139">Fakturační adresa – jméno kontaktu</span><span class="sxs-lookup"><span data-stu-id="13fa8-139">Bill to Contact Name</span></span> | <span data-ttu-id="13fa8-140">Upravitelná mřížka na kartě **Zákazníci nabídky** a formuláře **Hlavní** a **Vytvořit** pro zákazníka nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-140">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="13fa8-141">Toto je textové pole a mělo by se použít k identifikaci kontaktní osoby faktury pro tohoto zákazníka.</span><span class="sxs-lookup"><span data-stu-id="13fa8-141">This is a text field and should be used to identify the Invoice contact person for this customer.</span></span> <span data-ttu-id="13fa8-142">Výchozí hodnoty jsou brány ze záznamu souvisejícího účtu</span><span class="sxs-lookup"><span data-stu-id="13fa8-142">These are defaulted from the related account record</span></span> | <span data-ttu-id="13fa8-143">Zkopírováno do zákazníků projektové smlouvy po získání nabídky, a následně do pole Fakturační adresa – jméno kontaktu na faktuře, která je generována pro tohoto zákazníka.</span><span class="sxs-lookup"><span data-stu-id="13fa8-143">Copied over to project contract customers when a Quote is won and in turn to the Bill to Contract name field on the Invoice that is generated for this customer.</span></span> |
| <span data-ttu-id="13fa8-144">Fakturační adresa – jméno</span><span class="sxs-lookup"><span data-stu-id="13fa8-144">Bill to Name</span></span> | <span data-ttu-id="13fa8-145">Upravitelná mřížka na kartě **Zákazníci nabídky** a formuláře **Hlavní** a **Vytvořit** pro zákazníka nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-145">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="13fa8-146">Toto textové pole by se mělo použít k identifikaci kontaktní osoby faktury pro tohoto zákazníka.</span><span class="sxs-lookup"><span data-stu-id="13fa8-146">This text field should be used to identify the invoice contact person for this customer.</span></span> | <span data-ttu-id="13fa8-147">Zkopírováno do zákazníků projektové smlouvy po získání nabídky, a následně do pole **Fakturační adresa – jméno kontaktu** na faktuře, která je generována pro tohoto zákazníka.</span><span class="sxs-lookup"><span data-stu-id="13fa8-147">Copied to the project contract customers when a quote is won and in turn to the **Bill to Contract Name** field on the invoice that is generated for this customer.</span></span> |
| <span data-ttu-id="13fa8-148">Platební podmínky</span><span class="sxs-lookup"><span data-stu-id="13fa8-148">Payment Terms</span></span> | <span data-ttu-id="13fa8-149">Upravitelná mřížka na kartě **Zákazníci nabídky** a formuláře **Hlavní** a **Vytvořit** pro zákazníka nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-149">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="13fa8-150">Toto je sada možností s hodnotami, které jsou implicitně načteny ze záznamu souvisejícího účtu.</span><span class="sxs-lookup"><span data-stu-id="13fa8-150">This is an option set with values that default from the related account record.</span></span> | <span data-ttu-id="13fa8-151">Zkopírováno do zákazníků projektové smlouvy po získání nabídky, a následně do pole **Fakturační adresa – jméno kontaktu** na faktuře, která je generována pro tohoto zákazníka,</span><span class="sxs-lookup"><span data-stu-id="13fa8-151">Copied to the project contract customers when a quote is won and in turn, to the **Bill to Contract Name** field on the invoice that is generated for this customer,</span></span> |
| <span data-ttu-id="13fa8-152">Je zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="13fa8-152">Is Rounding</span></span> | <span data-ttu-id="13fa8-153">Upravitelná mřížka na kartě **Zákazníci nabídky** a formuláře **Hlavní** a **Vytvořit** pro zákazníka nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-153">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="13fa8-154">Označuje, zda je tento zákazník výchozím zaokrouhlovacím zákazníkem pro tento obchod.</span><span class="sxs-lookup"><span data-stu-id="13fa8-154">Indicates if this customer is a default rounding customer for this deal.</span></span> | <span data-ttu-id="13fa8-155">Zkopírováno do zákazníků projektové smlouvy při získání nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-155">Copied to the project contract customers when a quote is won.</span></span> |
| <span data-ttu-id="13fa8-156">Nepřekročitelný limit</span><span class="sxs-lookup"><span data-stu-id="13fa8-156">Not-to-exceed limit</span></span> | <span data-ttu-id="13fa8-157">Upravitelná mřížka na kartě **Zákazníci nabídky** a formuláře **Hlavní** a **Vytvořit** pro zákazníka nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-157">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="13fa8-158">Určuje, zda existuje sjednaný limit nebo strop celkové částky, která bude fakturována tomuto zákazníkovi za tuto zakázku</span><span class="sxs-lookup"><span data-stu-id="13fa8-158">Indicates if there is a negotiated limit or cap to the overall amount that will be invoiced to this customer for this engagement</span></span> | <span data-ttu-id="13fa8-159">Zkopírováno do zákazníků projektové smlouvy při získání nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-159">Copied to the project contract customers when a quote is won.</span></span> |

## <a name="editing-billing-split-percentages"></a><span data-ttu-id="13fa8-160">Úprava procentuálních rozdělení fakturace</span><span class="sxs-lookup"><span data-stu-id="13fa8-160">Editing billing split percentages</span></span>

<span data-ttu-id="13fa8-161">Procenta rozdělení fakturace se dají upravit v prostředí in-line úprav v mřížce.</span><span class="sxs-lookup"><span data-stu-id="13fa8-161">You can edit the billing split percentages by using the in-line grid edit experience.</span></span> <span data-ttu-id="13fa8-162">Pokud součet procent rozdělení fakturace není 100%, dojde k chybě.</span><span class="sxs-lookup"><span data-stu-id="13fa8-162">When the billing split percentages don't total 100%, an error will occur.</span></span> <span data-ttu-id="13fa8-163">Po aktualizaci procent rozdělení fakturace chybu odstraníte aktualizací stránky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-163">After you update the billing split percentages, refresh the page to remove the error.</span></span>

<span data-ttu-id="13fa8-164">Můžete také zkusit vybrat možnost **Rovnoměrně distribuovat** v podřízené mřížce zákazníků nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-164">You can also try selecting **Evenly Distribute** on the quote customers' sub-grid.</span></span> <span data-ttu-id="13fa8-165">Tato akce přiděluje rozdělení fakturace všem zákazníkům nabídky.</span><span class="sxs-lookup"><span data-stu-id="13fa8-165">This action allocates billing splits to all quote customers.</span></span> <span data-ttu-id="13fa8-166">Pokud existuje zaokrouhlovací faktor, bude přidán k zaokrouhlovacímu zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="13fa8-166">If there is any rounding factor, that will be added to the rounding customer.</span></span> <span data-ttu-id="13fa8-167">Jeden ze zákazníků nabídky je vždy označen jako zaokrouhlující zákazník.</span><span class="sxs-lookup"><span data-stu-id="13fa8-167">One of the quote customers is always tagged as the rounding customer.</span></span> <span data-ttu-id="13fa8-168">To znamená, že záznam zákazníka nabídky má příznak **Zaokrouhlování** nastaven na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="13fa8-168">this means that the quote customer record has the **Rounding** flag set to **Yes**.</span></span> <span data-ttu-id="13fa8-169">Obvykle se jedná o primárního zákazníka nabídky, ale lze to změnit.</span><span class="sxs-lookup"><span data-stu-id="13fa8-169">Typically this is the primary customer of the quote, but that can be changed.</span></span>