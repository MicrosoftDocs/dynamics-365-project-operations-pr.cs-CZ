---
title: Práce s osobními výdaji ve výkazu výdajů
description: Tento téma poskytuje informace o tom, jak pracovat s osobními výdaji vzniklým zaměstnancům při cestování za obchodními účely.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025676"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="82643-103">Práce s osobními výdaji ve výkazu výdajů</span><span class="sxs-lookup"><span data-stu-id="82643-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="82643-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="82643-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="82643-105">Během služebních cest může zaměstnanec platit osobní výdaje ze své podnikové kreditní karty.</span><span class="sxs-lookup"><span data-stu-id="82643-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="82643-106">Pokud nebyl definován proces pro zpracování osobních výdajů, může být proces schválení sestavy výdajů narušen, když zaměstnanec odešle svou podrobnou sestavu výdajů.</span><span class="sxs-lookup"><span data-stu-id="82643-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="82643-107">Existují dvě metody, které můžete použít k práci s osobními výdaji zaměstnance:</span><span class="sxs-lookup"><span data-stu-id="82643-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="82643-108">**Placeno zaměstnancem**: Vaše organizace neplatí osobní výdaje, které jsou uvedeny na účtu firemní kreditní karty.</span><span class="sxs-lookup"><span data-stu-id="82643-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="82643-109">Zaměstnanec místo toho zaplatí dodavateli kreditní karty náklady přímo.</span><span class="sxs-lookup"><span data-stu-id="82643-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="82643-110">**Placeno společností**: Vaše organizace zaplatí celý účet za firemní kreditní kartu a poté strhne z účtu pracovníka osobní náklady.</span><span class="sxs-lookup"><span data-stu-id="82643-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="82643-111">Způsob, který vaše organizace používá, se vybírá na stránce **Parametry řízení výdajů**.</span><span class="sxs-lookup"><span data-stu-id="82643-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="82643-112">Povolit funkci rozdělení výdajů, pokud má pole osobní částky definovanou hodnotu</span><span class="sxs-lookup"><span data-stu-id="82643-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="82643-113">Funkce **Povolit funkci rozdělení výdajů, pokud má pole osobní částky definovanou hodnotu** platí pouze pro sestavy výdajů, které jsou schváleny pomocí pracovního postupu na úrovni řádků.</span><span class="sxs-lookup"><span data-stu-id="82643-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="82643-114">Sestavy jsou schváleny přechodem na **Zpracovat sestavy výdajů** > **Sestavy výdajů, které mi byly přiřazeny** > **Otevřít sestavu výdajů**.</span><span class="sxs-lookup"><span data-stu-id="82643-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="82643-115">Chcete-li tuto funkci povolit, přejděte na **Pracovní prostory** > **Správa funkcí**, vyberte **Povolit funkci rozdělení výdajů, pokud má pole osobní částky definovanou hodnotu** a potom vyberte **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="82643-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="82643-116">Když je funkce povolena, řádky výdajů, které používají tuto funkci, vygenerují při odeslání sestavy dva řádky.</span><span class="sxs-lookup"><span data-stu-id="82643-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="82643-117">Jsou generovány dva řádky, aby schvalovatel mohl schválit každý řádek zvlášť.</span><span class="sxs-lookup"><span data-stu-id="82643-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
