---
title: Mezipodnikové výdaje
description: Pracovník, který je zaměstnán u jedné právnické osoby v organizaci, může vykonávat práci pro jinou právnickou osobu ve stejné organizaci. V této situaci můžete pomocí funkce mezipodnikových výdajů přiřadit výdaje pracovníka právnické osobě, pro kterou byla práce provedena.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073931"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="5b9fb-104">Mezipodnikové výdaje</span><span class="sxs-lookup"><span data-stu-id="5b9fb-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b9fb-105">Pracovník, který je zaměstnán u jedné právnické osoby v organizaci, může vykonávat práci pro jinou právnickou osobu ve stejné organizaci.</span><span class="sxs-lookup"><span data-stu-id="5b9fb-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="5b9fb-106">V této situaci můžete pomocí funkce mezipodnikových výdajů přiřadit výdaje pracovníka právnické osobě, pro kterou byla práce provedena.</span><span class="sxs-lookup"><span data-stu-id="5b9fb-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="5b9fb-107">Právnická osoba, která zaměstnává pracovníka, se nazývá půjčující právnická osoba.</span><span class="sxs-lookup"><span data-stu-id="5b9fb-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="5b9fb-108">Právní osoba, za kterou vznikají náklady na pracovníka, se nazývá vypůjčující právnická osoba.</span><span class="sxs-lookup"><span data-stu-id="5b9fb-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="5b9fb-109">Než může pracovník vytvořit a odeslat výdaje za práci, která je prováděna pro jinou právnickou osobu, v půjčující právnické osobě na stránce **Parametry řízení výdajů** vyberte možnost **Povolit mezipodnikové výdajové řádky**.</span><span class="sxs-lookup"><span data-stu-id="5b9fb-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="5b9fb-110">Daňové účtování mezipodnikových nákladů</span><span class="sxs-lookup"><span data-stu-id="5b9fb-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b9fb-111">Pokud chcete ve své zprávě o výdajích použít daňové skupiny, které jsou přidruženy k půjčující právnické osobě (zdrojové) místo právnické osoby vypůjčující (cílové), budete to muset nakonfigurovat v nastavení daně z obratu hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="5b9fb-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="5b9fb-112">Když je parametr hlavní knihy **Právní subjekt pro účtování mezipodnikových daní** je nastaven na **Zdrojový** a možnost **Použít pravidla pro zdanění daně z obratu** je nastavena na **Ne** , použije se daňová kombinace pro půjčující právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="5b9fb-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="5b9fb-113">Když je stejný parametr nastaven na **Cílová** , použije se daňová kombinace pro vypůjčující právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="5b9fb-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="5b9fb-114">U právnických osob ve Spojených státech, když je parametr nastaven na **Zdrojová** , pole **Pohledávka z prodejní dáně** musí být také nakonfigurováno na nové stránce **Skupiny účtování hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="5b9fb-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="5b9fb-115">Účetní nástroj použije informace z tohoto pole pro daňový účetní záznam.</span><span class="sxs-lookup"><span data-stu-id="5b9fb-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="5b9fb-116">Chování je konzistentní pro výdajové řádky zaúčtované s projektem nebo bez něj.</span><span class="sxs-lookup"><span data-stu-id="5b9fb-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
