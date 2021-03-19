---
title: Definice zásad výdajů
description: Můžete definovat zásady výdajů, které musí vaši pracovníci dodržovat při zadávání a odesílání výkazů výdajů a cestovních žádanek.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 863d1e44dad9fa0d2174cf77582a1d820988e92d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276070"
---
# <a name="define-expense-policies"></a><span data-ttu-id="f1b06-103">Definice zásad výdajů</span><span class="sxs-lookup"><span data-stu-id="f1b06-103">Define expense policies</span></span>

<span data-ttu-id="f1b06-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="f1b06-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f1b06-105">Můžete definovat zásady, které musí vaši pracovníci dodržovat při zadávání a odesílání výkazů výdajů a cestovních žádanek.</span><span class="sxs-lookup"><span data-stu-id="f1b06-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="f1b06-106">Implementace zásad výdajů vám pomůže efektivně spravovat výdaje.</span><span class="sxs-lookup"><span data-stu-id="f1b06-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="f1b06-107">Můžete například nastavit zásadu pro hotelové výdaje v New Yorku, kde se uvádí, že výdaje za noc nesmí překročit 250 USD.</span><span class="sxs-lookup"><span data-stu-id="f1b06-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="f1b06-108">Pokud pracovník předloží výkaz výdajů nebo cestovní žádanku, kde sazba za pokoj překročí tuto částku, systém oznámí</span><span class="sxs-lookup"><span data-stu-id="f1b06-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="f1b06-109">pracovníkovi, že byla překročena částka zásady pro výdaj.</span><span class="sxs-lookup"><span data-stu-id="f1b06-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="f1b06-110">Můžete nakonfigurovat zprávu, kterou pracovník obdrží, když vy</span><span class="sxs-lookup"><span data-stu-id="f1b06-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="f1b06-111">definujete zásadu.</span><span class="sxs-lookup"><span data-stu-id="f1b06-111">define the policy.</span></span>      
        
<span data-ttu-id="f1b06-112">Můžete definovat tři typy zásad:</span><span class="sxs-lookup"><span data-stu-id="f1b06-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="f1b06-113">**Upozornění**: Umožňuje pracovníkovi odeslat výkaz výdajů nebo cestovní žádanku, ale výdaj bude označen pro všechny schvalovatele a</span><span class="sxs-lookup"><span data-stu-id="f1b06-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="f1b06-114">a pro pozdější vykázání.</span><span class="sxs-lookup"><span data-stu-id="f1b06-114">for later reporting.</span></span>        

- <span data-ttu-id="f1b06-115">**Chyba**: Vyžaduje, aby pracovník před odesláním výkazu výdajů nebo cestovní žádanky revidoval výdaj ohledně splnění zásady.</span><span class="sxs-lookup"><span data-stu-id="f1b06-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="f1b06-116">**Odůvodnění**: Vyžaduje, aby pracovník nebo manažer před odesláním výkazu výdajů nebo cestovní žádanky zadal odůvodnění překročení částky zásady.</span><span class="sxs-lookup"><span data-stu-id="f1b06-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="f1b06-117">Tipy pro zásady</span><span class="sxs-lookup"><span data-stu-id="f1b06-117">Policy tips</span></span>
<span data-ttu-id="f1b06-118">Zde je několik návrhů, které vám mohou pomoci při vytváření nových zásad pro správu výdajů:</span><span class="sxs-lookup"><span data-stu-id="f1b06-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="f1b06-119">Zásady jsou účinné od data, což znamená, že zásada nebude platit, pokud bude vytvořena s datem po datu, kdy došlo k výdaji.</span><span class="sxs-lookup"><span data-stu-id="f1b06-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="f1b06-120">Například dnes vytvoříte novou zásadu k vynucení maximálních výdajů na jídlo ve výši 50 USD.</span><span class="sxs-lookup"><span data-stu-id="f1b06-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="f1b06-121">Veškeré stávající výdaje zadané od včerejška nebudou porovnány s touto zásadou.</span><span class="sxs-lookup"><span data-stu-id="f1b06-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="f1b06-122">Při vytváření zásady pro kategorii výdajů, kterou lze rozčlenit na položky, zvažte přidání podmínky pro typ řádku výdajů.</span><span class="sxs-lookup"><span data-stu-id="f1b06-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="f1b06-123">Některé zásady, například požadavek účtenky, nemusí mít pro rozepsané řádky smysl.</span><span class="sxs-lookup"><span data-stu-id="f1b06-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="f1b06-124">V této situaci se zásada použije pouze na řádek záhlaví nebo na nerozepsaný řádek.</span><span class="sxs-lookup"><span data-stu-id="f1b06-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="f1b06-125">Ve výchozím nastavení se zásady správy výdajů vyhodnocují oproti zdrojové entitě.</span><span class="sxs-lookup"><span data-stu-id="f1b06-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="f1b06-126">Pro mezipodnikové scénáře můžete místo toho nastavit zásadu, která se má vyhodnotit podle cílové entity (výpůjční entita).</span><span class="sxs-lookup"><span data-stu-id="f1b06-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="f1b06-127">Chcete-li spustit zásady proti cílové entitě, zapněte funkci **Vyhodnotit zásadu výdajů proti vypůjčující právnické osobě** v pracovním prostoru **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="f1b06-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="f1b06-128">Kdy vyhodnotit zásady</span><span class="sxs-lookup"><span data-stu-id="f1b06-128">When to evaluate policies</span></span>

<span data-ttu-id="f1b06-129">V parametrech správy výdajů můžete vybrat, zda chcete vyhodnotit zásady správy výdajů při uložení řádku nebo při odeslání výkazu výdajů.</span><span class="sxs-lookup"><span data-stu-id="f1b06-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="f1b06-130">Pokud se rozhodnete vyhodnotit při uložení řádku, uživatelé budou mít dříve přehled o tom, co potřebují k dokončení svého výkazu najednou.</span><span class="sxs-lookup"><span data-stu-id="f1b06-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="f1b06-131">Jinak můžete zpozdit vyhodnocení zásad a ušetřit čas ověřením na konci, během odesílání do pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="f1b06-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]