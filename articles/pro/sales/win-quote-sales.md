---
title: Uzavření nabídky – omezené
description: Toto téma poskytuje informace o uzavření nabídky v aplikaci Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175703"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="611e9-103">Uzavření nabídky – omezené</span><span class="sxs-lookup"><span data-stu-id="611e9-103">Close a quote - lite</span></span>

<span data-ttu-id="611e9-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="611e9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="611e9-105">Nabídku projektu lze uzavřít jako Získanou nebo Ztracenou.</span><span class="sxs-lookup"><span data-stu-id="611e9-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="611e9-106">Operace Aktivovat and Revidovat v nabídkách nejsou v Microsoft Dynamics 365 Project Operations podporovány, takže lze koncept nabídky uzavřít.</span><span class="sxs-lookup"><span data-stu-id="611e9-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="611e9-107">Uzavření nabídky jako získané</span><span class="sxs-lookup"><span data-stu-id="611e9-107">Close a quote as Won</span></span>

<span data-ttu-id="611e9-108">Uzavření nabídky projektu jako získané zavře nabídku se stavem nastaveným na Uzavřeno a důvodem stavu nastaveným na Získáno.</span><span class="sxs-lookup"><span data-stu-id="611e9-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="611e9-109">Uzavřením se nabídka projektu nastaví jako jen pro čtení a vytvoří se návrh smlouvy o projektu, který obsahuje informace o nabídce.</span><span class="sxs-lookup"><span data-stu-id="611e9-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="611e9-110">Protože uzavřenou nabídku nelze znovu otevřít, zobrazí se potvrzovací dialog Před provedením změn existuje potvrzovací dialog, protože uzavřenou nabídku nelze znovu otevřít a změny jsou nevratné.</span><span class="sxs-lookup"><span data-stu-id="611e9-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="611e9-111">Pokud je nabídka připojena k příležitosti, jakékoli jiné projektové nabídky příležitosti budou automaticky uzavřeny jako Ztraceno.</span><span class="sxs-lookup"><span data-stu-id="611e9-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="611e9-112">Finanční dopad uzavření nabídky jako získané</span><span class="sxs-lookup"><span data-stu-id="611e9-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="611e9-113">Pokud na projektu byly zaznamenané nějaké skutečné hodnoty v době, kdy je ještě připojený ke konceptu nabídky, zaznamenají se pouze náklady na čas nebo výdaje.</span><span class="sxs-lookup"><span data-stu-id="611e9-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="611e9-114">Po uzavření nabídky jako získané aplikace refaktoruje náklady obrácením starších údajů o nákladech a opětovným vytvořením nových údajů o nákladech.</span><span class="sxs-lookup"><span data-stu-id="611e9-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="611e9-115">Aplikace zpracuje tyto údaje o nákladech na základě metody fakturace příslušného řádku smlouvy projektu.</span><span class="sxs-lookup"><span data-stu-id="611e9-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="611e9-116">Pokud skutečná cena odkazuje na řádek smlouvy o čase a materiálu, systém automaticky vytvoří odpovídající nevyfakturované prodejní skutečné hodnoty, když je nabídka uzavřena a je vytvořena smlouva o projektu.</span><span class="sxs-lookup"><span data-stu-id="611e9-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="611e9-117">Pokud skutečné náklady odkazují na řádek smlouvy s pevnou cenou, aplikace přestane přepracovávat skutečné náklady na základě pravidel rozdělené fakturace pro zákazníky smlouvy o projektu.</span><span class="sxs-lookup"><span data-stu-id="611e9-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="611e9-118">Uzavření nabídky jako ztracené:</span><span class="sxs-lookup"><span data-stu-id="611e9-118">Closing a quote as lost:</span></span>

<span data-ttu-id="611e9-119">Uzavřením nabídky projektu jako ztracené nastavíte stav na Zavřeno a důvod stavu na Ztraceno.</span><span class="sxs-lookup"><span data-stu-id="611e9-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="611e9-120">Uzavřením se nabídka projektu nastaví jako jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="611e9-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="611e9-121">Protože uzavřenou nabídku nelze znovu otevřít, před uzavřením nabídky jsou změny potvrzeny v potvrzovacím dialogu.</span><span class="sxs-lookup"><span data-stu-id="611e9-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="611e9-122">Pokud má projektová nabídka, která je uzavřená jako ztracená, obsahuje na některé z řádků odkazovaný projekt, je tento projekt také označený jako uzavřený a veškeré rezervace zdrojů od daného dne dále jsou zrušeny.</span><span class="sxs-lookup"><span data-stu-id="611e9-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="611e9-123">V Project Operations nebude mít uzavření nabídky jako získané nebo ztracené vliv na tento stav příležitosti, která zůstane otevřená, dokud nebude ručně uzavřena.</span><span class="sxs-lookup"><span data-stu-id="611e9-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
