---
title: Přehled mezipodnikové fakturace
description: Toto téma poskytuje informace a příklady o mezipodnikové fakturaci projektů.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c1dcf642f79ce64cb83285ac6dc6d7eaf815145c
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369368"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="4e6ca-103">Přehled mezipodnikové fakturace</span><span class="sxs-lookup"><span data-stu-id="4e6ca-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="4e6ca-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="4e6ca-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4e6ca-105">Vaše organizace může mít více divizí, dceřiných společností a dalších právnických subjektů, které si navzájem přenášejí produkty a služby pro účely projektů.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="4e6ca-106">Právnická osoba, která poskytuje službu nebo produkt, se nazývá *půjčující právnická osoba*.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="4e6ca-107">Právnická osoba, která získává službu nebo produkt, se nazývá *vypůjčující právnická osoba*.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="4e6ca-108">Následující obrázek ukazuje typický scénář, kdy dva právní subjekty, Contoso Robotics USA (právnická osoba, která si půjčuje) a Contoso Robotics UK (půjčující právnická osoba) sdílí zdroje na realizaci projektu pro zákazníka, Adventure works.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="4e6ca-109">Pro tento scénář Contoso Robotics USA uzavřela smlouvu na dodání díla společnosti Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Mezipodniková fakturace](./media/IntercompanyScenario.png) 

<span data-ttu-id="4e6ca-111">Dynamics 365 Project Operations používá následující tok ke zpracování mezipodnikových transakcí:</span><span class="sxs-lookup"><span data-stu-id="4e6ca-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="4e6ca-112">Zdroje z půjčující právnické osoby zaznamenávají mezipodnikové transakce času nebo výdajů tím, že rezervují čas a výdaje oproti projektům ve vypůjčující právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="4e6ca-113">Časové a výdajové náklady se zaznamenávají v půjčující společnosti pomocí ceníku jednotkových nákladů vypůjčující společnosti.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="4e6ca-114">Mezipodnikové nefakturované prodejní transakce se zaznamenávají v půjčující společnosti pomocí ceníku jednotkových nákladů vypůjčující společnosti.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="4e6ca-115">Nevyfakturované výnosy se ve vypůjčující společnosti zaznamenávají pomocí ceníku smluvních prodejů.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="4e6ca-116">Zákazníkovi lze vystavit fakturu, když je zaznamenán nevyfakturovaný příjem.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="4e6ca-117">Zákazník nemusí čekat na dokončení zpracování mezipodnikové faktury.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="4e6ca-118">Mezipodnikové faktury zákazníků se v půjčující společnosti vytvářejí pravidelně.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="4e6ca-119">Faktury jsou vytvářeny ručně nebo pomocí periodického automatizovaného procesu.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="4e6ca-120">Pro každou vypůjčující právnickou osobu lze vytvořit jednu fakturu nebo lze podle projektu vytvořit samostatné faktury.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="4e6ca-121">Když je zaúčtována příslušná mezipodniková faktura zákazníka v půjčující právnické osobě, ve vypůjčující právnické osobě je vytvořena příslušná čekající faktura dodavatele.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="4e6ca-122">Po zaúčtování faktury budou náklady na čekající faktuře dodavatele zaznamenány do podřízené účetní knihy projektu.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="4e6ca-123">Následující diagram ilustruje mezipodnikovou fakturaci, protože se týká účetních událostí a očekávaných zaúčtování do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="4e6ca-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Mezipodnikový tok](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="4e6ca-125">Další materiály</span><span class="sxs-lookup"><span data-stu-id="4e6ca-125">Additional resources</span></span>

- [<span data-ttu-id="4e6ca-126">Konfigurace mezipodnikové fakturace</span><span class="sxs-lookup"><span data-stu-id="4e6ca-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="4e6ca-127">Zaznamenávání mezipodnikových transakcí</span><span class="sxs-lookup"><span data-stu-id="4e6ca-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="4e6ca-128">Vytváření mezipodnikových faktur zákazníků a dodavatelů</span><span class="sxs-lookup"><span data-stu-id="4e6ca-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]