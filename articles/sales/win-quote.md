---
title: Uzavření nabídky
description: Toto téma poskytuje informace o uzavření nabídek v aplikaci Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f46bf61bc3e492a648d65e86750a25609d5ab7a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995928"
---
# <a name="close-a-quote"></a><span data-ttu-id="e29d2-103">Uzavření nabídky</span><span class="sxs-lookup"><span data-stu-id="e29d2-103">Close a quote</span></span>

<span data-ttu-id="e29d2-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="e29d2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e29d2-105">Nabídku projektu lze uzavřít jako Získanou nebo Ztracenou.</span><span class="sxs-lookup"><span data-stu-id="e29d2-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="e29d2-106">Koncept nabídky lze uzavřít, protože funkce Aktivace a Revize nabídek nejsou v Microsoft Dynamics 365 Project Operations podporovány.</span><span class="sxs-lookup"><span data-stu-id="e29d2-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="e29d2-107">Uzavření nabídky jako získané</span><span class="sxs-lookup"><span data-stu-id="e29d2-107">Close a quote as Won</span></span>

<span data-ttu-id="e29d2-108">Uzavření nabídky projektu jako získané nastaví stav nabídky na **Uzavřená** a důvod stavu na **Získaná**.</span><span class="sxs-lookup"><span data-stu-id="e29d2-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="e29d2-109">Uzavřením se nabídky projektu nastaví jako jen pro čtení a vytvoří se návrh smlouvy o projektu, který obsahuje všechny informace o nabídce.</span><span class="sxs-lookup"><span data-stu-id="e29d2-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="e29d2-110">Protože uzavřenou nabídku nelze znovu otevřít, před uzavřením nabídky jsou změny potvrzeny v potvrzovacím dialogu.</span><span class="sxs-lookup"><span data-stu-id="e29d2-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="e29d2-111">Smlouva o projektu vytvořená z nabídky projektu je také k dispozici v části Řízení projektů a účetnictví modulu Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e29d2-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="e29d2-112">Pokud smlouva o projektu není namapována na projekt na žádném z jeho řádků, je tato smlouva o projektu zpřístupněna jako neaktivní smlouva o projektu a stane se aktivní, jakmile je projekt namapován na alespoň jednu ze svých řádků smlouvy.</span><span class="sxs-lookup"><span data-stu-id="e29d2-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="e29d2-113">Pokud je nabídka připojena k příležitosti, jakékoli jiné projektové nabídky příležitosti budou automaticky uzavřeny jako Ztraceno.</span><span class="sxs-lookup"><span data-stu-id="e29d2-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="e29d2-114">Finanční dopad uzavření nabídky jako získané</span><span class="sxs-lookup"><span data-stu-id="e29d2-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="e29d2-115">Pokud na projektu byly zaznamenané nějaké skutečné hodnoty v době, kdy je ještě připojený ke konceptu nabídky, zaznamenají se pouze náklady na čas nebo výdaje.</span><span class="sxs-lookup"><span data-stu-id="e29d2-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="e29d2-116">Po uzavření nabídky jako získané aplikace refaktoruje náklady obrácením starších údajů o nákladech a opětovným vytvořením nových údajů o nákladech.</span><span class="sxs-lookup"><span data-stu-id="e29d2-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="e29d2-117">Aplikace zpracuje tyto údaje o nákladech na základě metody fakturace příslušného řádku smlouvy projektu.</span><span class="sxs-lookup"><span data-stu-id="e29d2-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="e29d2-118">Pokud skutečná cena odkazuje na řádek smlouvy o čase a materiálu, systém automaticky vytvoří odpovídající nevyfakturované prodejní skutečné hodnoty, když je nabídka uzavřena a je vytvořena smlouva o projektu.</span><span class="sxs-lookup"><span data-stu-id="e29d2-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="e29d2-119">Pokud skutečné náklady odkazují na řádek smlouvy s pevnou cenou, aplikace přestane přepracovávat skutečné náklady na základě pravidel rozdělené fakturace pro zákazníky smlouvy o projektu.</span><span class="sxs-lookup"><span data-stu-id="e29d2-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="e29d2-120">Všechny přepracované skutečné hodnoty jsou k dispozici v modulu Řízení projektu a účetnictví pro účetního, který je může zkontrolovat, aktualizovat a zaúčtovat do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="e29d2-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="e29d2-121">Uzavření nabídky jako ztracené</span><span class="sxs-lookup"><span data-stu-id="e29d2-121">Close a quote as Lost</span></span>

<span data-ttu-id="e29d2-122">Uzavřením nabídky projektu jako ztracené nastavíte stav na **Zavřeno** a důvod stavu na **Ztraceno**.</span><span class="sxs-lookup"><span data-stu-id="e29d2-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="e29d2-123">Uzavřením se nabídka nastaví jako jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="e29d2-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="e29d2-124">Protože uzavřenou nabídku nelze znovu otevřít, před uzavřením nabídky jsou změny potvrzeny v potvrzovacím dialogu.</span><span class="sxs-lookup"><span data-stu-id="e29d2-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="e29d2-125">Pokud má projektová nabídka, která je uzavřená jako ztracená, obsahuje na některé z řádků odkazovaný projekt, je tento projekt také označený jako uzavřený a veškeré rezervace zdrojů od daného dne dále jsou zrušeny.</span><span class="sxs-lookup"><span data-stu-id="e29d2-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="e29d2-126">V Project Operations nebude mít uzavření nabídky jako získané nebo ztracené vliv na tento stav příležitosti, která zůstane otevřená, dokud nebude ručně uzavřena.</span><span class="sxs-lookup"><span data-stu-id="e29d2-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]