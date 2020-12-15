---
title: Nastavení zásad výdajů
description: Můžete nastavit zásady výdajů, které musí vaši pracovníci dodržovat při zadávání a odesílání výkazů výdajů a cestovních žádanek v aplikaci Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6240a7be175800ce6f3b066de9e935ab370629ef
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650086"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="3e657-103">Nastavení zásad výdajů</span><span class="sxs-lookup"><span data-stu-id="3e657-103">Set up expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e657-104">Můžete definovat zásady, které musí vaši pracovníci dodržovat při zadávání a odesílání výkazů výdajů a cestovních žádanek.</span><span class="sxs-lookup"><span data-stu-id="3e657-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="3e657-105">Implementace zásad výdajů vám pomůže efektivně spravovat výdaje.</span><span class="sxs-lookup"><span data-stu-id="3e657-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="3e657-106">Můžete například nastavit zásadu pro hotelové výdaje v New Yorku, kde se uvádí, že výdaje za noc nesmí překročit 250 USD.</span><span class="sxs-lookup"><span data-stu-id="3e657-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="3e657-107">Pokud pracovník předloží výkaz výdajů nebo cestovní žádanku, ve kterých sazba za pokoj překročí tuto částku, systém oznámí</span><span class="sxs-lookup"><span data-stu-id="3e657-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="3e657-108">pracovníkovi, že byla překročena částka zásady pro výdaj.</span><span class="sxs-lookup"><span data-stu-id="3e657-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="3e657-109">Můžete nakonfigurovat zprávu, kterou pracovník obdrží, když vy</span><span class="sxs-lookup"><span data-stu-id="3e657-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="3e657-110">definujete zásadu.</span><span class="sxs-lookup"><span data-stu-id="3e657-110">define the policy.</span></span>      
        
<span data-ttu-id="3e657-111">Můžete definovat tři typy zásad:</span><span class="sxs-lookup"><span data-stu-id="3e657-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="3e657-112">Upozornění – Umožňuje pracovníkovi odeslat výkaz výdajů nebo cestovní žádanku, ale výdaj bude označen pro všechny schvalovatele a</span><span class="sxs-lookup"><span data-stu-id="3e657-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="3e657-113">a pro pozdější vykázání.</span><span class="sxs-lookup"><span data-stu-id="3e657-113">for later reporting.</span></span>        

- <span data-ttu-id="3e657-114">Chyba – Vyžaduje, aby pracovník před odesláním výkazu výdajů nebo cestovní žádanky revidoval výdaj ohledně splnění zásady.</span><span class="sxs-lookup"><span data-stu-id="3e657-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="3e657-115">Odůvodnění – Vyžaduje, aby pracovník nebo manažer před odesláním výkazu výdajů nebo cestovní žádanky zadal odůvodnění překročení částky zásady.</span><span class="sxs-lookup"><span data-stu-id="3e657-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="3e657-116">Tipy pro zásady</span><span class="sxs-lookup"><span data-stu-id="3e657-116">Policy tips</span></span>
<span data-ttu-id="3e657-117">Zde je několik návrhů, které vám mohou pomoci při vytváření nových zásad pro správu výdajů.</span><span class="sxs-lookup"><span data-stu-id="3e657-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="3e657-118">Zásady jsou účinné od data a nezačnou platit, pokud bude zásada vytvořena s datem po datu, kdy došlo k výdaji.</span><span class="sxs-lookup"><span data-stu-id="3e657-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="3e657-119">Například pokud dnes vytváříte novou zásadu pro vynucení maximálních výdajů na jídlo ve výši 50 USD, nebudou všechny existující výdaje zadané do včerejška kontrolovány proti této zásadě.</span><span class="sxs-lookup"><span data-stu-id="3e657-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="3e657-120">Při vytváření zásady pro kategorii výdajů, kterou lze rozčlenit na položky, zvažte přidání podmínky pro typ řádku výdajů.</span><span class="sxs-lookup"><span data-stu-id="3e657-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="3e657-121">Některé zásady, jako je požadavek na odevzdání stvrzenky, nemusí mít smysl u rozepsaných řádků a měly by být použity pouze na řádek záhlaví nebo nerozepsaný řádek.</span><span class="sxs-lookup"><span data-stu-id="3e657-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="3e657-122">Ve výchozím nastavení se zásady správy výdajů vyhodnocují oproti zdrojové entitě.</span><span class="sxs-lookup"><span data-stu-id="3e657-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="3e657-123">Pro mezipodnikové scénáře můžete místo toho nastavit zásadu, která se má vyhodnotit podle cílové entity (výpůjční entita).</span><span class="sxs-lookup"><span data-stu-id="3e657-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="3e657-124">Chcete-li spustit zásady proti cílové entitě, zapněte funkci „Vyhodnotit zásadu výdajů proti vypůjčující právnické osobě“ v pracovním prostoru **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="3e657-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="3e657-125">Kdy vyhodnotit zásady</span><span class="sxs-lookup"><span data-stu-id="3e657-125">When to evaluate policies</span></span>

<span data-ttu-id="3e657-126">V parametrech správy výdajů existuje volba, zda chcete vyhodnotit zásady správy výdajů při uložení řádku nebo při odeslání výkazu výdajů.</span><span class="sxs-lookup"><span data-stu-id="3e657-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="3e657-127">Pokud se rozhodnete vyhodnotit při uložení řádku, zajistíte, že uživatelé budou mít dříve přehled o tom, co potřebují k dokončení svého výkazu najednou.</span><span class="sxs-lookup"><span data-stu-id="3e657-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="3e657-128">Jinak můžete zpozdit vyhodnocení zásad a ušetřit čas,, když k ověření dojde až na konci, během odesílání do pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="3e657-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
