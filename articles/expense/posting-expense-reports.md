---
title: Zaúčtování sestav výdajů
description: Toto téma vysvětluje, jak zaúčtovat sestavy výdajů.
author: suvaidya
manager: AnnBe
ms.date: 09/09/2020
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
ms.openlocfilehash: ec897373cd74f7d7f63cd9ca4c46f4245336eb7f
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907400"
---
# <a name="post-expense-reports"></a><span data-ttu-id="af21e-103">Zaúčtování sestav výdajů</span><span class="sxs-lookup"><span data-stu-id="af21e-103">Post expense reports</span></span>

<span data-ttu-id="af21e-104">Jakmile bude sestava výdajů schválena a přenesena do finančního deníku, může být zaúčtována.</span><span class="sxs-lookup"><span data-stu-id="af21e-104">After an expense report has been approved and transferred to the general journal, it can be posted.</span></span> <span data-ttu-id="af21e-105">Když zaúčtujete sestavu výdajů, budou identifikovány výdaje, které jsou způsobilé k vrácení daně z přidané hodnoty (DPH).</span><span class="sxs-lookup"><span data-stu-id="af21e-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="af21e-106">Úkol ověřovat a vymáhat platby DPH je přidělen zaměstnanci, který je odpovědný za ověření sestavy výdajů.</span><span class="sxs-lookup"><span data-stu-id="af21e-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="af21e-107">Pokud jsou výdaje na sestavě výdajů účtovány jiné společnosti než společnosti, která zaměstnává tohoto zaměstnance, musíte ověřit jak společnost, které tyto výdaje patří, tak společnosti, která je dluží.</span><span class="sxs-lookup"><span data-stu-id="af21e-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify both the company that those expenses are owed to and the company that they are owed from.</span></span> <span data-ttu-id="af21e-108">Příklad: zaměstnanec, který odeslal sestavu o výdajích, pracuje pro společnost DAT, ale účtoval výdaj společnosti DIR.</span><span class="sxs-lookup"><span data-stu-id="af21e-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="af21e-109">V tomto případě je DAT společnost, které tyto výdaje patří, a DIR je společnost, která je dluží.</span><span class="sxs-lookup"><span data-stu-id="af21e-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="af21e-110">Po ověření těchto řádků deníku můžete zaúčtovat řádky výdajů do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="af21e-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="af21e-111">Chcete-li zaúčtovat sestavu výdajů, vyberte na stránce **Schválené sestavy výdajů** sestavu výdajů a poté v podokně akcí vyberte příkaz **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="af21e-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="af21e-112">Je také možné zaúčtovat všechny sestavy výdajů v seznamu současně.</span><span class="sxs-lookup"><span data-stu-id="af21e-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="af21e-113">Vyberte všechny sestavy výdajů a poté vyberte příkaz **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="af21e-113">Select all the expense reports, and then select **Post**.</span></span>
