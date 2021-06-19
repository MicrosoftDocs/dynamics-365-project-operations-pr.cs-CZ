---
title: Nastavení integrace kreditní karty
description: Tento téma vysvětluje, jak pracovat s transakcemi kreditních karet, které souvisejí s výdaji.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001800"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="39f87-103">Nastavení integrace kreditní karty</span><span class="sxs-lookup"><span data-stu-id="39f87-103">Set up credit card integration</span></span>

<span data-ttu-id="39f87-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="39f87-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="39f87-105">Transakce kreditních karet související s výdaji lze nastavit tak, aby se automaticky importovaly podle opakujícího se plánu.</span><span class="sxs-lookup"><span data-stu-id="39f87-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="39f87-106">Alternativně lze transakce podle potřeby importovat ručně.</span><span class="sxs-lookup"><span data-stu-id="39f87-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="39f87-107">Transakce kreditní kartou se importují prostřednictvím datové entity transakcí kreditní kartou.</span><span class="sxs-lookup"><span data-stu-id="39f87-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="39f87-108">Import transakcí kreditní kartou</span><span class="sxs-lookup"><span data-stu-id="39f87-108">Import credit card transactions</span></span>

<span data-ttu-id="39f87-109">Chcete-li importovat transakce kreditní kartou, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="39f87-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="39f87-110">Na stránce **Transakce kreditní kartou** vyberte **Importovat transakce**.</span><span class="sxs-lookup"><span data-stu-id="39f87-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="39f87-111">Pokud otevíráte správu dat poprvé, musí systém aktualizovat seznam datových entit, než budete moci pokračovat.</span><span class="sxs-lookup"><span data-stu-id="39f87-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="39f87-112">V poli **Název** zadejte jedinečný popis úlohy importu.</span><span class="sxs-lookup"><span data-stu-id="39f87-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="39f87-113">V poli **Formát zdrojových dat** vyberte formát souboru k importu, který obsahuje transakce kreditní kartou.</span><span class="sxs-lookup"><span data-stu-id="39f87-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="39f87-114">Vyberte **Odeslat** a poté vyhledejte a vyberte soubor, který chcete importovat.</span><span class="sxs-lookup"><span data-stu-id="39f87-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="39f87-115">Po odeslání souboru ověřte mapování souboru transakcí kreditní karty a sloupců datové entity transakce kreditní karty výběrem odkazu na dlaždici **Zobrazit mapu**.</span><span class="sxs-lookup"><span data-stu-id="39f87-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="39f87-116">Pokud existují chyby mapování nebo pokud musíte změnit mapování, proveďte změny mapování buď z karty **Vizualizace mapování** nebo **Podrobnosti mapování**.</span><span class="sxs-lookup"><span data-stu-id="39f87-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="39f87-117">Chcete-li automatizovat transakce kreditní kartou, vyberte **Vytvořit opakující se datovou úlohu**.</span><span class="sxs-lookup"><span data-stu-id="39f87-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="39f87-118">Poté můžete nastavit opakování, které definuje, jak často se mají transakce kreditní kartou importovat.</span><span class="sxs-lookup"><span data-stu-id="39f87-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="39f87-119">Jakmile budete hotovi, zvolte **OK**.</span><span class="sxs-lookup"><span data-stu-id="39f87-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="39f87-120">Chcete-li nyní importovat vybraný soubor, vyberte **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="39f87-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="39f87-121">Pokud se během importu vyskytnou chyby, můžete si prohlédnout protokol provádění nebo pracovní data, ve kterých najdete chyby, které musíte opravit, abyste zajistili úspěšný import.</span><span class="sxs-lookup"><span data-stu-id="39f87-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="39f87-122">Pokud potřebujete importovat více než jeden formát souboru, musíte pro každý typ formátu vytvořit samostatné úlohy importu.</span><span class="sxs-lookup"><span data-stu-id="39f87-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="39f87-123">Změna přiřazení transakcí kreditní kartou pro ukončené zaměstnance</span><span class="sxs-lookup"><span data-stu-id="39f87-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="39f87-124">Po ukončení záznamu zaměstnance je účet zaměstnance služby Active Directory Domain Services (AD DS) deaktivován.</span><span class="sxs-lookup"><span data-stu-id="39f87-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="39f87-125">Mohou však existovat aktivní transakce kreditních karet, které je třeba stále proplatit a uhradit.</span><span class="sxs-lookup"><span data-stu-id="39f87-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="39f87-126">Na stránce **Transakce kreditní kartou** můžete znovu přiřadit zaměstnance u jakékoli transakce kreditní kartou, kde byl přidružený zaměstnanec ukončen.</span><span class="sxs-lookup"><span data-stu-id="39f87-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="39f87-127">Vyberte jednu nebo více transakcí kreditní kartou a poté vyberte **Znovu přiřadit transakce**.</span><span class="sxs-lookup"><span data-stu-id="39f87-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="39f87-128">Poté můžete vybrat dalšího zaměstnance, kterému chcete přiřadit transakce kreditní kartou.</span><span class="sxs-lookup"><span data-stu-id="39f87-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="39f87-129">Poté, co byly transakce s kreditními kartami znovu přiřazeny, mohou být vybrány pro výkazy výdajů a zaplaceny obvyklým postupem pro refundaci výkazu výdajů.</span><span class="sxs-lookup"><span data-stu-id="39f87-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="39f87-130">Odstranění transakcí kreditní kartou</span><span class="sxs-lookup"><span data-stu-id="39f87-130">Delete credit card transactions</span></span> 

<span data-ttu-id="39f87-131">Někdy po importu transakcí kreditní kartou může být nutné některé transakce odstranit.</span><span class="sxs-lookup"><span data-stu-id="39f87-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="39f87-132">Důvodem může být například fakt, že transakce jsou duplikáty, nebo protože jejich data nejsou přesná.</span><span class="sxs-lookup"><span data-stu-id="39f87-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="39f87-133">Správci mohou použít funkci **„Odstranění transakcí kreditní kartou“** k výběru a odstranění transakcí kreditní karty, které **nejsou připojeny** k sestavě výdajů.</span><span class="sxs-lookup"><span data-stu-id="39f87-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="39f87-134">Přejděte do nabídky **Pravidelné úkoly** > **Odstranit transakce kreditní kartou**.</span><span class="sxs-lookup"><span data-stu-id="39f87-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="39f87-135">Vyberte **Filtr** a zadejte informace identifikující záznamy, které mají být odstraněny.</span><span class="sxs-lookup"><span data-stu-id="39f87-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="39f87-136">Výběrem tlačítka **OK** záznamy odstraníte.</span><span class="sxs-lookup"><span data-stu-id="39f87-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
