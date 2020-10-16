---
title: Přehled schválení
description: Toto téma poskytuje informace o práci se schváleními ve službě Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961158"
---
# <a name="approvals-overview"></a><span data-ttu-id="fd5ad-103">Přehled schválení</span><span class="sxs-lookup"><span data-stu-id="fd5ad-103">Approvals overview</span></span>

<span data-ttu-id="fd5ad-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="fd5ad-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fd5ad-105">Odeslání času a výdajů prochází schvalovacím pracovním postupem.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="fd5ad-106">Po schválení položek jsou transakce zaznamenány ve skutečných hodnotách nebo je čas zaúčtován v rozvrhu.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="fd5ad-107">Pracovní postup schválení</span><span class="sxs-lookup"><span data-stu-id="fd5ad-107">Approvals workflow</span></span>
<span data-ttu-id="fd5ad-108">Když vytvoříte a odešlete položku času nebo výdajů, vytvoří se položka schválení.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="fd5ad-109">Schvalovatel projektu nebo váš nadřízený váš vstup zkontroluje a schválí.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="fd5ad-110">Pokud položka souvisí s projektem, po schválení budou vytvořeny skutečné údaje.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="fd5ad-111">To umožňuje sledování nákladů a fakturace.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="fd5ad-112">Schválit záznam</span><span class="sxs-lookup"><span data-stu-id="fd5ad-112">Approve an entry</span></span>
<span data-ttu-id="fd5ad-113">Formulář **Schválení** umožňuje přepínat mezi různými pohledy, takže můžete prohlížet různé typy schválení.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="fd5ad-114">Přejděte na formulář **Schválení** a vyberte **Výdaje**, **Čas** nebo **Odvolání**.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="fd5ad-115">Zkontrolujte každé schválení a vyberte ty, které chcete schválit.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="fd5ad-116">Vyberte **Schvalovat**, chcete-li schválit vybrané položky.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="fd5ad-117">Systém tyto záznamy zpracuje a vytvoří skutečné hodnoty nebo rezervaci.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="fd5ad-118">Odmítnout záznam</span><span class="sxs-lookup"><span data-stu-id="fd5ad-118">Reject an entry</span></span>
<span data-ttu-id="fd5ad-119">Jako schvalovatel projektu možná budete muset zaslat záznam zpět uživateli k opravě.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="fd5ad-120">Přejděte na formulář **Schválení** a vyberte záznam, který chcete odmítnout.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="fd5ad-121">Vyberte **Odmítnout**.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-121">Select **Reject**.</span></span>
3. <span data-ttu-id="fd5ad-122">Volitelné - Přidejte komentář do dialogového okna **Komentáře k odmítnutí** informující uživatele, proč je záznam odmítnut.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="fd5ad-123">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-123">Select **OK**.</span></span> <span data-ttu-id="fd5ad-124">Záznam bude vrácen uživateli.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="fd5ad-125">Odvolání záznamů</span><span class="sxs-lookup"><span data-stu-id="fd5ad-125">Recall entries</span></span>
<span data-ttu-id="fd5ad-126">V určitém okamžiku možná budete muset odeslaný záznam odvolat.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="fd5ad-127">Pokud záznam nebyl schválen, bude okamžitě vrácen.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="fd5ad-128">Schválená položka však může mít podstatný dopad.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="fd5ad-129">Schvalovatel projektu je povinen schválit odvolání, aby se transakce dále nepromítala do skutečných hodnot.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="fd5ad-130">Zadejte schvalovatele projektu</span><span class="sxs-lookup"><span data-stu-id="fd5ad-130">Specify Project approvers</span></span>
<span data-ttu-id="fd5ad-131">Každý projekt má několik členů projektového týmu.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-131">Each project has a number of project team members.</span></span> <span data-ttu-id="fd5ad-132">Můžete určit, kteří členové týmu jsou také schvalovateli projektu.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="fd5ad-133">Přejděte na formulář **Projekty** a otevřete projekt ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="fd5ad-134">Na kartě **Tým** vyberte člena týmu, který bude schvalovatelem projektu, a poté vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="fd5ad-135">Nastavte pole **Schvalovatel projektu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="fd5ad-136">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-136">Select **Save**.</span></span>
5. <span data-ttu-id="fd5ad-137">Opakováním kroků 2 a 4 přidejte další schvalovatele projektu.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="fd5ad-138">Nakonfigurujte správce uživatele</span><span class="sxs-lookup"><span data-stu-id="fd5ad-138">Configure the user's manager</span></span>

1. <span data-ttu-id="fd5ad-139">Přejděte na **Nastavení** > **Zabezpečení** > **Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="fd5ad-140">Vyberte uživatele, kterému přiřazujete manažera, a v oblasti **Informace o organizaci** vyberte správce ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="fd5ad-141">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="fd5ad-141">Select **Save**.</span></span>


