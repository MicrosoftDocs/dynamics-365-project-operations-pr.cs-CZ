---
title: Mezipodnikové výdaje
description: Tento téma poskytuje informace o tom, jak pomocí mezipodnikových výdajů přiřadit výdaje pracovníka entitě, pro kterou byla práce provedena.
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
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271525"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="079b2-103">Mezipodnikové výdaje</span><span class="sxs-lookup"><span data-stu-id="079b2-103">Intercompany expenses</span></span>

<span data-ttu-id="079b2-104">Pracovník, který je zaměstnán u jedné právnické osoby v organizaci, může vykonávat práci pro jinou právnickou osobu ve stejné organizaci.</span><span class="sxs-lookup"><span data-stu-id="079b2-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="079b2-105">Pomocí mezipodnikových výdajů můžete přiřadit výdaje pracovníka entitě, pro kterou byla práce provedena.</span><span class="sxs-lookup"><span data-stu-id="079b2-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="079b2-106">Právnická osoba, která zaměstnává pracovníka, se nazývá půjčující právnická osoba.</span><span class="sxs-lookup"><span data-stu-id="079b2-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="079b2-107">Právní osoba, za kterou vznikají náklady na pracovníka, se nazývá vypůjčující právnická osoba.</span><span class="sxs-lookup"><span data-stu-id="079b2-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="079b2-108">Než bude pracovník moci vytvářet a odesílat mezipodnikové výdaje, musíte povolit mezipodnikové výdajové řádky.</span><span class="sxs-lookup"><span data-stu-id="079b2-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="079b2-109">V půjčující entitě na stránce **Parametry řízení výdajů** vyberte **Povolit mezipodnikové výdajové řádky**.</span><span class="sxs-lookup"><span data-stu-id="079b2-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="079b2-110">Daňové účtování mezipodnikových nákladů</span><span class="sxs-lookup"><span data-stu-id="079b2-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="079b2-111">Než budete moci v sestavě výdajů použít daňové skupiny, které jsou přidruženy k zapůjčující (zdroj) entitě místo půjčující si (cílové) entity, musíte povolit funkci v nastavení daně z prodeje hlavního registru.</span><span class="sxs-lookup"><span data-stu-id="079b2-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="079b2-112">Když je parametr **Právní entita pro účtování mezipodnikových daní** nastaven na **Zdroj** a **Použít pravidla pro zdanění daně z prodeje** je nastaveno na **Ne**, je použita daňová kombinace pro zapůjčující právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="079b2-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="079b2-113">Když je stejný parametr nastaven na **Cílová**, použije se daňová kombinace pro vypůjčující právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="079b2-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="079b2-114">U právnických osob ve Spojených státech, když je parametr nastaven na **Zdrojová**, pole **Pohledávka z prodejní dáně** musí být také nakonfigurováno na nové stránce **Skupiny účtování hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="079b2-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="079b2-115">Účetní nástroj použije informace z tohoto pole pro daňový účetní záznam.</span><span class="sxs-lookup"><span data-stu-id="079b2-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="079b2-116">Chování je konzistentní pro výdajové řádky zaúčtované s projektem nebo bez něj.</span><span class="sxs-lookup"><span data-stu-id="079b2-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]