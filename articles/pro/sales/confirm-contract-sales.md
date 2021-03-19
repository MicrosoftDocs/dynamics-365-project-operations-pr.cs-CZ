---
title: Potvrzení projektové smlouvy
description: Toto téma poskytuje informace o potvrzení smlouvy v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d807d3631f40a93ec7dbd918b64c287fd4875c79
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273820"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="61cee-103">Potvrzení projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="61cee-103">Confirm a project contract</span></span>

<span data-ttu-id="61cee-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="61cee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="61cee-105">Smlouva o projektu v Dynamics 365 Project Operations může být aktivní z důvodu **Potvrzeno**, nebo uzavřena z důvodu **Ztracená**.</span><span class="sxs-lookup"><span data-stu-id="61cee-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="61cee-106">Když potvrdíte smlouvu o projektu, stav se aktualizuje z **Návrh** na **Aktivní** a důvod stavu je **Potvrzeno**.</span><span class="sxs-lookup"><span data-stu-id="61cee-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="61cee-107">Aktivní nebo uzavřenou smlouvu nelze upravit ani znovu otevřít.</span><span class="sxs-lookup"><span data-stu-id="61cee-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="61cee-108">Finanční dopad potvrzení smlouvy o projektu</span><span class="sxs-lookup"><span data-stu-id="61cee-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="61cee-109">Po potvrzení smlouvy projektu aplikace přepočítá náklady obrácením starších údajů o nákladech a opětovným vytvořením nových údajů o nákladech.</span><span class="sxs-lookup"><span data-stu-id="61cee-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="61cee-110">Nové náklady jsou poté zpracovány na základě metody fakturace příslušného řádku smlouvy projektu.</span><span class="sxs-lookup"><span data-stu-id="61cee-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="61cee-111">Pokud skutečné náklady odkazují na řádek smlouvy o čase a materiálu, aplikace automaticky znovu vytvoří odpovídající nevyfakturované skutečné prodejní údaje.</span><span class="sxs-lookup"><span data-stu-id="61cee-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="61cee-112">Pokud skutečné náklady odkazují na řádek smlouvy s pevnou cenou, aplikace zastaví přepracování skutečných nákladů.</span><span class="sxs-lookup"><span data-stu-id="61cee-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="61cee-113">Nepřekročitelné limity, nastavení poplatků a ceny a nákladování na skutečných údajích jsou vyhodnocovány a poté aktualizovány jako součást procesu potvrzení.</span><span class="sxs-lookup"><span data-stu-id="61cee-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="61cee-114">Uzavření smlouvy projektu jako ztracené</span><span class="sxs-lookup"><span data-stu-id="61cee-114">Close a project contract as lost</span></span>

<span data-ttu-id="61cee-115">Když uzavřete smlouvu projektu jako ztracenou, stav smlouvy se aktualizuje na **Uzavřeno** a důvod stavu je **Ztraceno**.</span><span class="sxs-lookup"><span data-stu-id="61cee-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="61cee-116">Smlouva o projektu se stane jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="61cee-116">The project contract becomes read-only.</span></span> <span data-ttu-id="61cee-117">Před dokončením změn je k dispozici potvrzovací dialog, protože nemůžete znovu otevřít uzavřenou smlouvu o projektu.</span><span class="sxs-lookup"><span data-stu-id="61cee-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="61cee-118">Pokud smlouva projektu, která je uzavřena jako ztracená, odkazuje na projekt na svých řádcích, je tento projekt také označen jako uzavřený.</span><span class="sxs-lookup"><span data-stu-id="61cee-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="61cee-119">Veškeré rezervace zdrojů od daného dne budou zrušeny.</span><span class="sxs-lookup"><span data-stu-id="61cee-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="61cee-120">Jakékoli nevyfakturované prodejní údaje o projektové smlouvě, které ještě nejsou na faktuře, budou stornovány.</span><span class="sxs-lookup"><span data-stu-id="61cee-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="61cee-121">V Dynamics 365 Project Operations uzavření smlouvy o projektu jako ztracené nebude mít vliv na tento stav přidružené příležitosti.</span><span class="sxs-lookup"><span data-stu-id="61cee-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="61cee-122">Příležitost zůstane otevřená a musí být ručně uzavřena.</span><span class="sxs-lookup"><span data-stu-id="61cee-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]