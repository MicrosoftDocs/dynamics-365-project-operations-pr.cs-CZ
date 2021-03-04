---
title: Uzavření nabídky – omezené
description: Toto téma poskytuje informace o uzavření nabídky v aplikaci Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764856"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="74645-103">Uzavření nabídky – omezené</span><span class="sxs-lookup"><span data-stu-id="74645-103">Close a quote - lite</span></span>

<span data-ttu-id="74645-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="74645-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="74645-105">Nabídku projektu lze uzavřít jako Získanou nebo Ztracenou.</span><span class="sxs-lookup"><span data-stu-id="74645-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="74645-106">Koncept nabídky lze uzavřít, protože operace Aktivace a Revize nabídek nejsou v Microsoft Dynamics 365 Project Operations podporovány.</span><span class="sxs-lookup"><span data-stu-id="74645-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="74645-107">Uzavření nabídky jako získané</span><span class="sxs-lookup"><span data-stu-id="74645-107">Close a quote as Won</span></span>

<span data-ttu-id="74645-108">Když zavřete nabídku projektu jako vyhraná, stav je nastaven na uzavřeno a důvod stavu je vyhraná.</span><span class="sxs-lookup"><span data-stu-id="74645-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="74645-109">Uzavřením se nabídka projektu nastaví jako jen pro čtení a vytvoří se návrh smlouvy o projektu, který obsahuje informace o nabídce.</span><span class="sxs-lookup"><span data-stu-id="74645-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="74645-110">Protože uzavřenou nabídku nelze znovu otevřít, potvrzovací dialog potvrdí vaše změny.</span><span class="sxs-lookup"><span data-stu-id="74645-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="74645-111">Pokud je nabídka připojena k příležitosti, jakékoli jiné projektové nabídky příležitosti budou automaticky uzavřeny jako Ztraceno.</span><span class="sxs-lookup"><span data-stu-id="74645-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="74645-112">Finanční dopad uzavření nabídky jako získané</span><span class="sxs-lookup"><span data-stu-id="74645-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="74645-113">Pokud jsou na projektu nějaké skutečné údaje, zatímco je stále připojen ke konceptu nabídky, zaznamenají se pouze náklady na čas nebo výdaj.</span><span class="sxs-lookup"><span data-stu-id="74645-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="74645-114">Po uzavření nabídky jako získané aplikace refaktoruje náklady obrácením starších údajů o nákladech a opětovným vytvořením nových údajů o nákladech.</span><span class="sxs-lookup"><span data-stu-id="74645-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="74645-115">Aplikace zpracuje tyto údaje o nákladech na základě metody fakturace příslušného řádku smlouvy projektu.</span><span class="sxs-lookup"><span data-stu-id="74645-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="74645-116">Pokud skutečná cena odkazuje na řádek smlouvy času a materiálu, vytvoří se odpovídající nevyfakturované prodejní skutečné hodnoty, když je nabídka uzavřena a je vytvořena smlouva o projektu.</span><span class="sxs-lookup"><span data-stu-id="74645-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="74645-117">Pokud skutečné náklady odkazují na řádek smlouvy s pevnou cenou, aplikace přestane přepracovávat skutečné náklady, které jsou založeny na pravidlech rozdělené fakturace pro zákazníky smlouvy o projektu.</span><span class="sxs-lookup"><span data-stu-id="74645-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="74645-118">Uzavření nabídky jako ztracené:</span><span class="sxs-lookup"><span data-stu-id="74645-118">Closing a quote as lost:</span></span>

<span data-ttu-id="74645-119">Když zavřete nabídku projektu jako prohraná, stav je nastaven na uzavřeno a důvod stavu je prohraná.</span><span class="sxs-lookup"><span data-stu-id="74645-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="74645-120">Uzavřením se nabídka projektu nastaví jako jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="74645-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="74645-121">Protože uzavřenou nabídku nelze znovu otevřít, před uzavřením nabídky jsou změny potvrzeny v potvrzovacím dialogu.</span><span class="sxs-lookup"><span data-stu-id="74645-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="74645-122">Pokud nabídka projektu, která je uzavřena jako Prohraná, odkazuje na projekt na kterémkoli z jejích řádků, je tento projekt také označen jako Uzavřený.</span><span class="sxs-lookup"><span data-stu-id="74645-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="74645-123">Veškeré rezervace zdrojů od daného dne budou zrušeny.</span><span class="sxs-lookup"><span data-stu-id="74645-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="74645-124">V Project Operations nebude mít uzavření nabídky jako získané nebo ztracené vliv na tento stav příležitosti, která zůstane otevřená, dokud nebude ručně uzavřena.</span><span class="sxs-lookup"><span data-stu-id="74645-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
