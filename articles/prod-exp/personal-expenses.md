---
title: Osobní výdaje ve výkazu výdajů
description: Toto téma vysvětluje dva způsoby zpracování osobních výdajů pracovníka v Microsoft Dynamics 365 Finance.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073929"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="cec39-103">Osobní výdaje ve výkazu výdajů</span><span class="sxs-lookup"><span data-stu-id="cec39-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cec39-104">Během služebních cest mohou pracovníci někdy účtovat osobní výdaje na vrub svých podnikových kreditních karet.</span><span class="sxs-lookup"><span data-stu-id="cec39-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="cec39-105">Pokud nedefinujete proces zpracování osobních výdajů, může dojít k narušení procesu schvalování výkazů výdajů, když pracovníci předloží své rozepsané výkazy výdajů.</span><span class="sxs-lookup"><span data-stu-id="cec39-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="cec39-106">Existují dva způsoby, jak účtovat osobní výdaje pracovníka:</span><span class="sxs-lookup"><span data-stu-id="cec39-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="cec39-107">**Placeno zaměstnancem** – Vaše organizace neplatí osobní výdaje, které jsou uvedeny na účtu firemní kreditní karty.</span><span class="sxs-lookup"><span data-stu-id="cec39-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="cec39-108">Namísto toho vytvoří zprávu, která zobrazuje osobní výdaje spolu s firemními výdaji, které byly účtovány na vrub podnikové kreditní karty.</span><span class="sxs-lookup"><span data-stu-id="cec39-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="cec39-109">**Placeno společností** – Vaše organizace zaplatí celý účet firemní kreditní karty a poté strhne z účtu pracovníka osobní náklady.</span><span class="sxs-lookup"><span data-stu-id="cec39-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="cec39-110">Způsob, který vaše organizace používá, se vybírá na stránce **Parametry řízení výdajů**.</span><span class="sxs-lookup"><span data-stu-id="cec39-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
