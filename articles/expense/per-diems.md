---
title: Denní diety
description: Tento téma poskytuje informace o pravidlech pro denní diety, které se používají ve správě výdajů.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b1476bfc0386412762c30e5a00acaff65bfbe3c7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995253"
---
# <a name="per-diems"></a><span data-ttu-id="bb6d8-103">Denní diety</span><span class="sxs-lookup"><span data-stu-id="bb6d8-103">Per diems</span></span>

<span data-ttu-id="bb6d8-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="bb6d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="bb6d8-105">Denní dieta je příspěvek vyplácený pracovníkovi, který cestuje za prací.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="bb6d8-106">Ve správě výdajů můžete vytvořit pravidla pro denní diety určené pro různé cestovní situace.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="bb6d8-107">Sazby denních diet mohou být založeny na ročním období, místě cesty nebo na obou kritériích.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="bb6d8-108">Když vytvoříte pravidlo denní diety, můžete určit, že určité procento sazby diety bude zadrženo, pokud pracovník obdrží bezplatné jídlo nebo služby.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="bb6d8-109">Můžete také nastavit minimální a maximální počet hodin, které musí cesta pracovníka trvat, aby byla sazba denní diety použita.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="bb6d8-110">Konfigurace</span><span class="sxs-lookup"><span data-stu-id="bb6d8-110">Configuration</span></span> 

1. <span data-ttu-id="bb6d8-111">Chcete-li přidat místa vyplácení denních diet, přejděte na nabídku **Nastavit** > **Výpočty a kódy** > **Umístění denních diet**.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="bb6d8-112">Pro každé z výše přidaných umístění vyberte sazbu denní diety a měnu, která je platná mezi konkrétním počátečním a konečným datem pro hotel, stravování a další výdaje.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="bb6d8-113">Sazby a měny diet se konfigurují v nabídce **Nastavit** > **Výpočty a kódy** > **Denní diety**.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="bb6d8-114">Na stránce **Umístění denních diet** konfigurujte úrovně sazeb denních diet.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="bb6d8-115">Úrovně sazeb denních diet vám umožňují definovat procentuální rozdělení denního příspěvku na hotel, stravu a další výdaje.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="bb6d8-116">Chcete-li určit procentuální snížení sazby pro snídani, oběd nebo večeři, aktualizujte pole na stránce **Parametry správy výdajů** na kartě **Denní diety**.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="bb6d8-117">Odesílání výdajů na denní diety</span><span class="sxs-lookup"><span data-stu-id="bb6d8-117">Submit expenses using per diem</span></span>
<span data-ttu-id="bb6d8-118">Chcete-li odeslat výdaje s využitím denních diet, použijte při vytváření sestavy výdajů kategorie výdajů **Denní diety**.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="bb6d8-119">Zadejte hodnoty **Denní diety od data**, **Denní diety do data** a **Umístění denních diet**.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="bb6d8-120">Částka bude vypočítána na základě sazeb denních diet pro vybrané místo a redukce diety za jídlo bude vypočítána na základě úrovní sazeb denních diet.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]