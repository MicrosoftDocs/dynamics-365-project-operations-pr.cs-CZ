---
title: Oprava účtování návrhů konceptů faktur projektu
description: Tento téma vysvětluje, jak upravit informace související s účetnictvím u návrhu konceptu faktury.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251192"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a><span data-ttu-id="81ef7-103">Oprava účtování návrhů konceptů faktur projektu</span><span class="sxs-lookup"><span data-stu-id="81ef7-103">Correct the accounting on draft project invoice proposals</span></span>

<span data-ttu-id="81ef7-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="81ef7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="81ef7-105">*Provozní podrobnosti* pro projektové faktury vede projektový manažer na proforma faktuře.</span><span class="sxs-lookup"><span data-stu-id="81ef7-105">*Operational details* for project invoices are maintained by the project manager on a pro forma invoice.</span></span> <span data-ttu-id="81ef7-106">Mezi tyto podrobnosti patří rozhodnutí o hodinách, výdajích, materiálech nebo milnících, které musí být fakturovány, sazbách a použití záloh a zadržených částek.</span><span class="sxs-lookup"><span data-stu-id="81ef7-106">These details include the decision about the hours, expenses, materials, or milestones that must be invoiced, the rates, and the application of advance and retainer amounts.</span></span> <span data-ttu-id="81ef7-107">Po potvrzení původní proforma faktury můžete upravit provozní podrobnosti vytvořením a potvrzením [opravné proforma faktury](../proforma-invoicing/corrective-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="81ef7-107">After you confirm the original pro forma invoice, you can adjust the operational details by creating and confirming a [corrective pro forma invoice](../proforma-invoicing/corrective-invoices.md).</span></span>

<span data-ttu-id="81ef7-108">*Účetní údaje* pro projektové faktury jsou uchovávány v dokumentu faktury orientované na zákazníka.</span><span class="sxs-lookup"><span data-stu-id="81ef7-108">*Accounting details* for project invoices are maintained in a customer-facing invoice document.</span></span> <span data-ttu-id="81ef7-109">Mezi tyto podrobnosti patří výpočet DPH a finanční dimenze použité na faktuře.</span><span class="sxs-lookup"><span data-stu-id="81ef7-109">These details include the sales tax calculation and the financial dimensions that are applied to the invoice.</span></span> <span data-ttu-id="81ef7-110">Tento téma poskytuje podrobnosti o tom, jak lze tyto účetní podrobnosti upravit v návrhu faktury konceptu projektu.</span><span class="sxs-lookup"><span data-stu-id="81ef7-110">This topic provides details about how these accounting details can be adjusted on a draft project invoice proposal.</span></span>

## <a name="adjust-sales-tax"></a><span data-ttu-id="81ef7-111">Úprava DPH</span><span class="sxs-lookup"><span data-stu-id="81ef7-111">Adjust sales tax</span></span>

<span data-ttu-id="81ef7-112">Výchozí fakturační skupiny DPH a položkové skupiny DPH lze upravit přímo v dokumentu návrhu faktury.</span><span class="sxs-lookup"><span data-stu-id="81ef7-112">Default billing sales tax groups and item sales tax groups can be adjusted directly on the invoice proposal document.</span></span> <span data-ttu-id="81ef7-113">Chcete-li tyto skupiny upravit, vyberte **Upravit** a poté na každém řádku návrhu faktury projektu zadejte novou hodnotu do pole **Skupina DPH** nebo **Skupina DPH položek**.</span><span class="sxs-lookup"><span data-stu-id="81ef7-113">To adjust these groups, select **Edit**, and then, on each project invoice proposal line, enter a new value in the **Sales tax group** or **Item sales tax group** field.</span></span>

## <a name="adjust-financial-dimensions"></a><span data-ttu-id="81ef7-114">Úprava finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="81ef7-114">Adjust financial dimensions</span></span>

<span data-ttu-id="81ef7-115">Finanční dimenze nelze upravit přímo na řádku návrhu faktury projektu.</span><span class="sxs-lookup"><span data-stu-id="81ef7-115">Financial dimensions can't be edited directly on a project invoice proposal line.</span></span> <span data-ttu-id="81ef7-116">Místo toho postupujte podle těchto kroků a upravte finanční dimenze v návrhu faktury projektu.</span><span class="sxs-lookup"><span data-stu-id="81ef7-116">Instead, follow these steps to adjust financial dimensions on a project invoice proposal.</span></span>

1. <span data-ttu-id="81ef7-117">Na návrhu faktury projektu vyberte **Smazat všechny**, chcete-li odebrat řádky návrhu faktury projektu.</span><span class="sxs-lookup"><span data-stu-id="81ef7-117">On the project invoice proposal, select **Delete all** to remove the project invoice proposal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="81ef7-118">Tlačítko **Smazat všechny** je k dispozici pouze poté, co správce systému povolí funkci **Odstranit řádky návrhu faktury při použití Project Operations pro scénáře se zdroji bez skladových materiálů** v pracovním prostoru **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="81ef7-118">The **Delete all** button is available only after the system administrator enables the **Delete invoice proposal lines when using Project Operations for resource based/ non-stocked scenarios** feature in the **Feature management** workspace.</span></span>

2. <span data-ttu-id="81ef7-119">Úprava finančních dimenzí:</span><span class="sxs-lookup"><span data-stu-id="81ef7-119">Adjust the financial dimensions:</span></span>

    - <span data-ttu-id="81ef7-120">**Transakce na účet (milníky fakturace):** přejděte na **Všechny projekty** \> **Spravovat** \> **Transakce na účet** a vyberte milník, který vyžaduje úpravu.</span><span class="sxs-lookup"><span data-stu-id="81ef7-120">**On-account transactions (billing milestones):** Go to **All projects** \> **Manage** \> **On-account transactions**, and select the milestone that requires adjustment.</span></span> <span data-ttu-id="81ef7-121">Pak na kartě **Finanční dimenze** aktualizujte hodnoty podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="81ef7-121">Then, on the **Financial dimensions** tab, update the values as required.</span></span>
    - <span data-ttu-id="81ef7-122">**Časové, výdajové a materiální transakce:** Na stránce **Zaúčtované transakce projektu** vyberte **Upravte účetnictví**, chcete-li aktualizovat finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="81ef7-122">**Time, expense, and material transactions:** On the **Posted project transactions** page, select **Adjust accounting** to update the financial dimensions.</span></span>

3. <span data-ttu-id="81ef7-123">Po dokončení úpravy hodnot finanční dimenze přejděte na **Řízení projektů a účetnictví** \> **Periodické** \> **Integrace Project Operations** a vyberte **Import z pracovní tabulky**, chcete-li spustit periodický proces.</span><span class="sxs-lookup"><span data-stu-id="81ef7-123">After you've finished adjusting the financial dimension values, go to **Project management and accounting** \> **Periodic** \> **Project Operations integration**, and select **Import from staging table** to run the periodic process.</span></span> <span data-ttu-id="81ef7-124">Tento proces používá aktualizované hodnoty finančních dimenzí k opětovnému vytvoření řádků návrhu faktury projektu.</span><span class="sxs-lookup"><span data-stu-id="81ef7-124">That process uses the updated financial dimension values to re-create the project invoice proposal lines.</span></span> <span data-ttu-id="81ef7-125">Aktualizované hodnoty se poté použijí v podřízené účetní knize projektu a hlavní knize při zaúčtování faktury projektu.</span><span class="sxs-lookup"><span data-stu-id="81ef7-125">The updated values are then used in the project subledger and general ledger when the project invoice is posted.</span></span>
