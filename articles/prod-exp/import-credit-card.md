---
title: Import a údržba transakcí kreditní kartou
description: Toto téma vysvětluje, jak importovat a udržovat transakce kreditních karet související s výdaji. Tyto transakce lze nastavit tak, aby se automaticky importovaly podle opakujícího se plánu, nebo je lze podle potřeby ručně importovat.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: edeab157aa2fa6cf518ad086b4c1f22c5b45fa04
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005153"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="b1d5c-104">Import a údržba transakcí kreditní kartou</span><span class="sxs-lookup"><span data-stu-id="b1d5c-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="b1d5c-105">Transakce kreditních karet související s výdaji lze nastavit tak, aby se automaticky importovaly podle opakujícího se plánu.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="b1d5c-106">Alternativně lze transakce podle potřeby importovat ručně.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="b1d5c-107">Transakce kreditní kartou se importují prostřednictvím datové entity transakce kreditní kartou.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="b1d5c-108">Další informace o datových entitách najdete v tématu [Datové entity ](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="b1d5c-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="b1d5c-109">Import transakcí kreditní kartou</span><span class="sxs-lookup"><span data-stu-id="b1d5c-109">Import credit card transactions</span></span>

1. <span data-ttu-id="b1d5c-110">Na stránce **Transakce kreditní kartou** vyberte **Importovat transakce**.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="b1d5c-111">Pokud otevíráte správu dat poprvé, musí systém aktualizovat seznam datových entit, než budete moci pokračovat.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="b1d5c-112">Do pole **Název** zadejte jedinečný popis úlohy importu.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="b1d5c-113">V poli **Formát zdrojových dat** vyberte formát souboru k importu, který obsahuje transakce kreditní kartou.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="b1d5c-114">Vyberte **Odeslat** a poté vyhledejte a vyberte soubor, který chcete importovat.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="b1d5c-115">Po odeslání souboru ověřte mapování souboru transakcí kreditní karty a sloupců datové entity transakce kreditní karty výběrem odkazu na dlaždici **Zobrazit mapu**.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="b1d5c-116">Pokud existují chyby mapování nebo pokud musíte změnit mapování, proveďte změny mapování buď z karty **Vizualizace mapování** nebo **Podrobnosti mapování**.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="b1d5c-117">Chcete-li automatizovat transakce kreditní kartou, vyberte **Vytvořit opakující se datovou úlohu**.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="b1d5c-118">Poté můžete nastavit opakování, které definuje, jak často se mají transakce kreditní kartou importovat.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="b1d5c-119">Jakmile budete hotovi, zvolte **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="b1d5c-120">Chcete-li nyní importovat vybraný soubor, vyberte **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="b1d5c-121">Pokud se během importu vyskytnou chyby, můžete si prohlédnout protokol provádění nebo pracovní data a zobrazit chyby, které musíte opravit, abyste mohli zaručit úspěšný import.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="b1d5c-122">Pokud musíte importovat více než jeden formát souboru, musíte vytvořit samostatné úlohy importu pro každý typ formátu.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="b1d5c-123">Změna přiřazení transakcí kreditní kartou pro ukončené zaměstnance</span><span class="sxs-lookup"><span data-stu-id="b1d5c-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="b1d5c-124">Po ukončení záznamu zaměstnance je účet zaměstnance služby Active Directory Domain Services (AD DS) deaktivován.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="b1d5c-125">Mohou však existovat aktivní transakce kreditních karet, které je třeba stále proplatit a uhradit.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="b1d5c-126">Ze stránky **Transakce kreditní kartou** můžete zaměstnanci znovu přiřadit jakékoli transakce kreditní kartou, kde byl přidružený zaměstnanec ukončen.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="b1d5c-127">Vyberte jednu nebo více transakcí kreditní kartou a poté vyberte **Znovu přiřadit transakce**.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="b1d5c-128">Poté můžete vybrat dalšího zaměstnance, kterému chcete přiřadit transakce kreditní kartou.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="b1d5c-129">Poté, co byly transakce s kreditními kartami znovu přiřazeny, mohou být vybrány pro výkazy výdajů a zaplaceny obvyklým postupem pro refundaci výkazu výdajů.</span><span class="sxs-lookup"><span data-stu-id="b1d5c-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]