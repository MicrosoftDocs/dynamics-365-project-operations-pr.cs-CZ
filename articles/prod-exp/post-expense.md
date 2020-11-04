---
title: Zaúčtování sestavy výdajů
description: Toto téma vysvětluje, jak zaúčtovat sestavu výdajů do hlavní knihy.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d008ef8dd55550431fbb9e329cd7d9428a08831
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073926"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="b68c4-103">Zaúčtování sestavy výdajů</span><span class="sxs-lookup"><span data-stu-id="b68c4-103">Post an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b68c4-104">Jakmile bude sestava výdajů schválena a přenesena do finančního deníku, může být zaúčtována do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="b68c4-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="b68c4-105">Když zaúčtujete sestavu výdajů, budou identifikovány výdaje, které jsou způsobilé k vrácení daně z přidané hodnoty (DPH).</span><span class="sxs-lookup"><span data-stu-id="b68c4-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="b68c4-106">Úkol ověřovat a vymáhat platby DPH je přidělen zaměstnanci, který je odpovědný za ověření sestavy výdajů.</span><span class="sxs-lookup"><span data-stu-id="b68c4-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="b68c4-107">Pokud jsou výdaje na sestavě výdajů účtovány jiné společnosti než společnosti, která zaměstnává tohoto zaměstnance, musíte ověřit společnost, které tyto výdaje patří, a společnost, která výdaje dluží.</span><span class="sxs-lookup"><span data-stu-id="b68c4-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="b68c4-108">Příklad: zaměstnanec, který odeslal sestavu o výdajích, pracuje pro společnost DAT, ale účtoval výdaj společnosti DIR.</span><span class="sxs-lookup"><span data-stu-id="b68c4-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="b68c4-109">V tomto případě je DAT společnost, které tyto výdaje patří, a DIR je společnost, která je dluží.</span><span class="sxs-lookup"><span data-stu-id="b68c4-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="b68c4-110">Po ověření těchto řádků deníku můžete zaúčtovat řádky výdajů do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="b68c4-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="b68c4-111">Chcete-li zaúčtovat sestavu výdajů, vyberte na stránce **Schválené sestavy výdajů** sestavu výdajů a poté v podokně akcí vyberte příkaz **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="b68c4-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="b68c4-112">Je také možné zaúčtovat všechny sestavy výdajů v seznamu současně.</span><span class="sxs-lookup"><span data-stu-id="b68c4-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="b68c4-113">Vyberte všechny sestavy výdajů a poté vyberte příkaz **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="b68c4-113">Select all the expense reports, and then select **Post**.</span></span>
