---
title: Nastavení integrace kreditní karty
description: Toto téma vysvětluje, jak importovat a udržovat transakce kreditních karet související s výdaji.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 483775e1334a281026dbfaf214d06d235255f13e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896813"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="60458-103">Nastavení integrace kreditní karty</span><span class="sxs-lookup"><span data-stu-id="60458-103">Set up credit card integration</span></span>

<span data-ttu-id="60458-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="60458-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="60458-105">Transakce kreditních karet související s výdaji lze nastavit tak, aby se automaticky importovaly podle opakujícího se plánu.</span><span class="sxs-lookup"><span data-stu-id="60458-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="60458-106">Alternativně lze transakce podle potřeby importovat ručně.</span><span class="sxs-lookup"><span data-stu-id="60458-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="60458-107">Transakce kreditní kartou se importují prostřednictvím datové entity transakce kreditní kartou.</span><span class="sxs-lookup"><span data-stu-id="60458-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="60458-108">Import transakcí kreditní kartou</span><span class="sxs-lookup"><span data-stu-id="60458-108">Import credit card transactions</span></span>

1. <span data-ttu-id="60458-109">Na stránce **Transakce kreditní kartou** vyberte **Importovat transakce**.</span><span class="sxs-lookup"><span data-stu-id="60458-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="60458-110">Pokud otevíráte správu dat poprvé, musí systém aktualizovat seznam datových entit, než budete moci pokračovat.</span><span class="sxs-lookup"><span data-stu-id="60458-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="60458-111">Do pole **Název** zadejte jedinečný popis úlohy importu.</span><span class="sxs-lookup"><span data-stu-id="60458-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="60458-112">V poli **Formát zdrojových dat** vyberte formát souboru k importu, který obsahuje transakce kreditní kartou.</span><span class="sxs-lookup"><span data-stu-id="60458-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="60458-113">Vyberte **Odeslat** a poté vyhledejte a vyberte soubor, který chcete importovat.</span><span class="sxs-lookup"><span data-stu-id="60458-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="60458-114">Po odeslání souboru ověřte mapování souboru transakcí kreditní karty a sloupců datové entity transakce kreditní karty výběrem odkazu na dlaždici **Zobrazit mapu**.</span><span class="sxs-lookup"><span data-stu-id="60458-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="60458-115">Pokud existují chyby mapování nebo pokud musíte změnit mapování, proveďte změny mapování buď z karty **Vizualizace mapování** nebo **Podrobnosti mapování**.</span><span class="sxs-lookup"><span data-stu-id="60458-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="60458-116">Chcete-li automatizovat transakce kreditní kartou, vyberte **Vytvořit opakující se datovou úlohu**.</span><span class="sxs-lookup"><span data-stu-id="60458-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="60458-117">Poté můžete nastavit opakování, které definuje, jak často se mají transakce kreditní kartou importovat.</span><span class="sxs-lookup"><span data-stu-id="60458-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="60458-118">Jakmile budete hotovi, zvolte **OK**.</span><span class="sxs-lookup"><span data-stu-id="60458-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="60458-119">Chcete-li nyní importovat vybraný soubor, vyberte **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="60458-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="60458-120">Pokud se během importu vyskytnou chyby, můžete si prohlédnout protokol provádění nebo pracovní data a zobrazit chyby, které musíte opravit, abyste mohli zaručit úspěšný import.</span><span class="sxs-lookup"><span data-stu-id="60458-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="60458-121">Pokud musíte importovat více než jeden formát souboru, musíte vytvořit samostatné úlohy importu pro každý typ formátu.</span><span class="sxs-lookup"><span data-stu-id="60458-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="60458-122">Změna přiřazení transakcí kreditní kartou pro ukončené zaměstnance</span><span class="sxs-lookup"><span data-stu-id="60458-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="60458-123">Po ukončení záznamu zaměstnance je účet zaměstnance služby Active Directory Domain Services (AD DS) deaktivován.</span><span class="sxs-lookup"><span data-stu-id="60458-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="60458-124">Mohou však existovat aktivní transakce kreditních karet, které je třeba stále proplatit a uhradit.</span><span class="sxs-lookup"><span data-stu-id="60458-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="60458-125">Ze stránky **Transakce kreditní kartou** můžete zaměstnanci znovu přiřadit jakékoli transakce kreditní kartou, kde byl přidružený zaměstnanec ukončen.</span><span class="sxs-lookup"><span data-stu-id="60458-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="60458-126">Vyberte jednu nebo více transakcí kreditní kartou a poté vyberte **Znovu přiřadit transakce**.</span><span class="sxs-lookup"><span data-stu-id="60458-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="60458-127">Poté můžete vybrat dalšího zaměstnance, kterému chcete přiřadit transakce kreditní kartou.</span><span class="sxs-lookup"><span data-stu-id="60458-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="60458-128">Poté, co byly transakce s kreditními kartami znovu přiřazeny, mohou být vybrány pro výkazy výdajů a zaplaceny obvyklým postupem pro refundaci výkazu výdajů.</span><span class="sxs-lookup"><span data-stu-id="60458-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
