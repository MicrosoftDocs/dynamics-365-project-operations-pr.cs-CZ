---
title: Opravené faktury
description: Toto téma poskytuje informace o opravených fakturách.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287815"
---
# <a name="corrected-invoices"></a><span data-ttu-id="dc440-103">Opravené faktury</span><span class="sxs-lookup"><span data-stu-id="dc440-103">Corrected invoices</span></span>

<span data-ttu-id="dc440-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="dc440-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="dc440-105">Potvrzené faktury lze upravovat.</span><span class="sxs-lookup"><span data-stu-id="dc440-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="dc440-106">Když upravíte potvrzenou fakturu, vytvoří se koncept opravené faktury.</span><span class="sxs-lookup"><span data-stu-id="dc440-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="dc440-107">Protože se předpokládá, že chcete zrušit všechny transakce a množství z původní faktury, obsahuje tato opravená faktura všechny transakce z původní faktury a všechna množství na ní jsou nula (0).</span><span class="sxs-lookup"><span data-stu-id="dc440-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="dc440-108">Pokud transakce nevyžadují opravu, můžete je odebrat z konceptu opravné faktury.</span><span class="sxs-lookup"><span data-stu-id="dc440-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="dc440-109">Pokud chcete stornovat nebo vrátit pouze částečné množství, můžete upravit pole Množství v podrobnostech řádku.</span><span class="sxs-lookup"><span data-stu-id="dc440-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="dc440-110">Pokud otevřete podrobnosti řádku faktury, uvidíte původní množství faktury.</span><span class="sxs-lookup"><span data-stu-id="dc440-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="dc440-111">Potom můžete upravit aktuální množství faktury tak, aby bylo menší nebo větší než původní množství faktury.</span><span class="sxs-lookup"><span data-stu-id="dc440-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="dc440-112">Po potvrzení opravné faktury se původní skutečná hodnota fakturovaného prodeje stornuje a vytvoří se nová skutečná hodnota fakturovaného prodeje.</span><span class="sxs-lookup"><span data-stu-id="dc440-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="dc440-113">Pokud bylo množství sníženo, rozdíl způsobí, že bude vytvořena i nová skutečná hodnota nefakturovaného prodeje.</span><span class="sxs-lookup"><span data-stu-id="dc440-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="dc440-114">Pokud byl například původní fakturovaný prodej na 8 hodin a opravené podrobnosti řádku faktury obsahují snížené množství 6 hodin, stornují se původní vyfakturované prodejní řádky a vytvoří dvě nové skutečné hodnoty:</span><span class="sxs-lookup"><span data-stu-id="dc440-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="dc440-115">Fakturovaná skutečná hodnota prodeje pro 6 hodin.</span><span class="sxs-lookup"><span data-stu-id="dc440-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="dc440-116">Skutečná hodnota nefakturovaného prodeje pro zbývající dvě hodiny.</span><span class="sxs-lookup"><span data-stu-id="dc440-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="dc440-117">Tato transakce může být buď fakturována později, nebo označena jako neúčtovatelná, v závislosti na jednáních se zákazníkem.</span><span class="sxs-lookup"><span data-stu-id="dc440-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]