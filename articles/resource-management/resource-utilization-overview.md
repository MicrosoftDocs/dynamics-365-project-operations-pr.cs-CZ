---
title: Přehled využití zdroje
description: Tohle téma obsahuje informace o využití zdrojů v Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000788"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="f106b-103">Přehled využití zdroje</span><span class="sxs-lookup"><span data-stu-id="f106b-103">Resource utilization overview</span></span>

<span data-ttu-id="f106b-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="f106b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f106b-105">Zdroje mohou mít cílové fakturovatelné využití.</span><span class="sxs-lookup"><span data-stu-id="f106b-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="f106b-106">Toto cílové využití je definováno jako atribut výchozí role zdroje, nebo je nastaveno v záznamu konkrétního rezervovatelného zdroje.</span><span class="sxs-lookup"><span data-stu-id="f106b-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="f106b-107">Výpočty využití vycházejí ze skutečných hodin, které zdroje vykázaly pomocí schválených časových záznamů.</span><span class="sxs-lookup"><span data-stu-id="f106b-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="f106b-108">K výpočtu využití se používají následující vzorce:</span><span class="sxs-lookup"><span data-stu-id="f106b-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="f106b-109">Fakturovatelné využití = skutečné fakturovatelné hodiny ÷ kapacita zdroje</span><span class="sxs-lookup"><span data-stu-id="f106b-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="f106b-110">Nefakturovatelné využití = skutečný čas s ID typu fakturace = neúčtovatelné, komplementární nebo nedostupné ÷ kapacita zdroje</span><span class="sxs-lookup"><span data-stu-id="f106b-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="f106b-111">Interní = skutečný čas bez prodejní smlouvy ÷ kapacita zdroje</span><span class="sxs-lookup"><span data-stu-id="f106b-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="f106b-112">Kapacita zdroje = pracovní doba zdroje – mimo kancelář – nepracovní dny</span><span class="sxs-lookup"><span data-stu-id="f106b-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="f106b-113">Zobrazení **Využití zdroje** naleznete v podokně **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="f106b-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="f106b-114">Každá buňka v tabulce představuje procentuální hodnotu fakturovatelného využití zdroje v určitém období, například den, týden nebo měsíc.</span><span class="sxs-lookup"><span data-stu-id="f106b-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="f106b-115">K obarvení buněk se používají následující vzorce:</span><span class="sxs-lookup"><span data-stu-id="f106b-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="f106b-116">**Zelená**: Fakturovatelné využití > = Cílové využití zdroje</span><span class="sxs-lookup"><span data-stu-id="f106b-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="f106b-117">**Žlutá**: Cílové využití – 20 < = Fakturovatelné využití < Cílové využití</span><span class="sxs-lookup"><span data-stu-id="f106b-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="f106b-118">**Červená**: Fakturovatelné využití < Cílové využití – 20.</span><span class="sxs-lookup"><span data-stu-id="f106b-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="f106b-119">Vzhledem k tomu, že je zobrazení **Využití zdroje** založeno na Plánovací vývěsce, můžete k filtrování výsledků využít funkce filtrování Plánovací vývěsky.</span><span class="sxs-lookup"><span data-stu-id="f106b-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="f106b-120">Mřížka vyžaduje, abyste nastavili cílové využití buď u role, nebo u konkrétního zdroje.</span><span class="sxs-lookup"><span data-stu-id="f106b-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="f106b-121">Pro toto nastavení přejděte na **Zdroje** > **Role zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="f106b-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="f106b-122">Navíc musí být ke každému rezervovatelnému zdroji přiřazena výchozí role.</span><span class="sxs-lookup"><span data-stu-id="f106b-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="f106b-123">Přejděte na **Zdroje** > **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="f106b-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="f106b-124">Na kartě **Project Service** ověřte, zda je definována role zdroje a zda pole **Je výchozí** je nastaveno na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="f106b-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="f106b-125">Můžete přidat další role, kde **Je výchozí** = **Ne**.</span><span class="sxs-lookup"><span data-stu-id="f106b-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="f106b-126">Role, ve které **Je výchozí** = **Ano**, slouží k vyhodnocení využití prostředku vůči cíli pro danou roli.</span><span class="sxs-lookup"><span data-stu-id="f106b-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="f106b-127">Na kartě **Project Service** můžete také nastavit individuální cílové využití zdroje.</span><span class="sxs-lookup"><span data-stu-id="f106b-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="f106b-128">Výpočet využití pak používá toto cílové využití k vyhodnocení cíle zdroje namísto cíle výchozí role zdroje.</span><span class="sxs-lookup"><span data-stu-id="f106b-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="f106b-129">Využití je pro zdroj zobrazeno pouze v případě, že tento zdroj má schválenou fakturovatelnou dobu během období zobrazeného v mřížce.</span><span class="sxs-lookup"><span data-stu-id="f106b-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]