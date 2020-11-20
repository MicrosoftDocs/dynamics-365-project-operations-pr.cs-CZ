---
title: Vytvoření ad hoc zálohy na smlouvě – omezené
description: Tohle téma poskytuje informace o vytvoření zálohy na smlouvě podle potřeby.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181354"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a><span data-ttu-id="d88ca-103">Vytvoření ad hoc zálohy na smlouvě – omezené</span><span class="sxs-lookup"><span data-stu-id="d88ca-103">Creating an ad hoc advance on a contract - lite</span></span>

<span data-ttu-id="d88ca-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="d88ca-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d88ca-105">Microsoft Dynamics 365 Project Operations podporuje scénáře fakturace, které zahrnují platby předem a zálohy.</span><span class="sxs-lookup"><span data-stu-id="d88ca-105">Microsoft Dynamics 365 Project Operations supports invoicing scenarios that involve pre-payments and advances.</span></span> <span data-ttu-id="d88ca-106">Proces používání **Záloh** v **Project Operations** je podobný smlouvám **Záloha**.</span><span class="sxs-lookup"><span data-stu-id="d88ca-106">The process for using **Advances** in **Project Operations** is similar to **Retainer** contracts.</span></span> 

<span data-ttu-id="d88ca-107">Chcete-li zákazníkovi fakturovat zálohu, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="d88ca-107">Complete the following steps to invoice the customer for an advance.</span></span>

1. <span data-ttu-id="d88ca-108">Přejděte na stránku **Projektová smlouva** a poté vyberte kartu **Zálohy**.</span><span class="sxs-lookup"><span data-stu-id="d88ca-108">Go to the **Project Contract** page, and then select the **Advances and Retainers** tab.</span></span>
2. <span data-ttu-id="d88ca-109">V podmřížce, která obsahuje seznam všech dříve zaznamenaných záloh, vyberte **+ Nová záloha projektové smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="d88ca-109">In the subgrid that lists all the previously recorded advances and prepayments, select **+ New Project contract retainer**.</span></span> 

    <span data-ttu-id="d88ca-110">Otevře se formulář **Rychlé vytvoření** pro zaznamenání zálohy.</span><span class="sxs-lookup"><span data-stu-id="d88ca-110">The **Quick Create** form opens for recording a prepayment or advance.</span></span>
    
3. <span data-ttu-id="d88ca-111">V tabulce níže jsou uvedena pole záznamu zálohy, které je třeba mít na paměti při vytváření nových:</span><span class="sxs-lookup"><span data-stu-id="d88ca-111">The table below lists the fields for recording an advance and the considerations to keep in mind as you create new ones:</span></span>

    | <span data-ttu-id="d88ca-112">Pole</span><span class="sxs-lookup"><span data-stu-id="d88ca-112">Field</span></span> | <span data-ttu-id="d88ca-113">Popis</span><span class="sxs-lookup"><span data-stu-id="d88ca-113">Description</span></span> | <span data-ttu-id="d88ca-114">Dopad na následné složky</span><span class="sxs-lookup"><span data-stu-id="d88ca-114">Downstream impact</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="d88ca-115">**Zákazník projektové smlouvy**</span><span class="sxs-lookup"><span data-stu-id="d88ca-115">**Project Contract Customer**</span></span> | <span data-ttu-id="d88ca-116">Toto pole označuje, kterému zákazníkovi na smlouvě bude tato záloha fakturována.</span><span class="sxs-lookup"><span data-stu-id="d88ca-116">This field indicates which customer on the contract will be invoiced for this advance.</span></span> | <span data-ttu-id="d88ca-117">Pokud máte na smlouvě více zákazníků a chcete každému z nich fakturovat konkrétní zálohu nebo částku zálohy, vytvořte zálohu pro každého zákazníka zvlášť.</span><span class="sxs-lookup"><span data-stu-id="d88ca-117">If you have multiple customers on the contract and want to invoice each of them for a specific retainer or advance amount, create an advance for each customer individually.</span></span> |
    | <span data-ttu-id="d88ca-118">**Popis**</span><span class="sxs-lookup"><span data-stu-id="d88ca-118">**Description**</span></span> | <span data-ttu-id="d88ca-119">Popis účelu nebo načasování zálohy, který pomůže tuto zálohu identifikovat.</span><span class="sxs-lookup"><span data-stu-id="d88ca-119">The description of the purpose or timing of the advance to help identify this advance.</span></span> | <span data-ttu-id="d88ca-120">Tento popis se zobrazuje na řádku faktury pro tuto zálohu.</span><span class="sxs-lookup"><span data-stu-id="d88ca-120">This description is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="d88ca-121">**Částka**</span><span class="sxs-lookup"><span data-stu-id="d88ca-121">**Amount**</span></span> | <span data-ttu-id="d88ca-122">Částka zálohy.</span><span class="sxs-lookup"><span data-stu-id="d88ca-122">The amount for the pre-payment or advance.</span></span> | <span data-ttu-id="d88ca-123">Tato částka se zobrazuje na řádku faktury pro tuto zálohu.</span><span class="sxs-lookup"><span data-stu-id="d88ca-123">This amount is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="d88ca-124">**Datum faktury**</span><span class="sxs-lookup"><span data-stu-id="d88ca-124">**Invoice Date**</span></span> | <span data-ttu-id="d88ca-125">Datum, kdy je tato záloha fakturována zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="d88ca-125">The date on which this advance is invoiced to the customer.</span></span> | <span data-ttu-id="d88ca-126">Toto je datum, kdy má proces automatického vytváření faktur vytvořit řádek faktury pro tuto zálohu.</span><span class="sxs-lookup"><span data-stu-id="d88ca-126">This is the date for the automated invoice creation process to create an invoice line for this advance.</span></span> |
    | <span data-ttu-id="d88ca-127">**Stav faktury**</span><span class="sxs-lookup"><span data-stu-id="d88ca-127">**Invoice Status**</span></span> | <span data-ttu-id="d88ca-128">Toto je nastavení možnosti, které označuje, zda je tato záloha přidána do konceptu faktury pro tohoto zákazníka.</span><span class="sxs-lookup"><span data-stu-id="d88ca-128">This is an option setting that indicates whether this advance is added to a draft invoice for this customer.</span></span> <span data-ttu-id="d88ca-129">Možné hodnoty jsou:</span><span class="sxs-lookup"><span data-stu-id="d88ca-129">The possible values are:</span></span></br><span data-ttu-id="d88ca-130">- **Nepřipraveno k fakturaci**</span><span class="sxs-lookup"><span data-stu-id="d88ca-130">- **Not ready to invoice**</span></span></br><span data-ttu-id="d88ca-131">- **Připraveno k fakturaci**</span><span class="sxs-lookup"><span data-stu-id="d88ca-131">- **Ready to invoice**</span></span> | <span data-ttu-id="d88ca-132">Když je záloha označena jako **Připraveno k fakturaci**, je přidána jako čas na řádku v konceptu faktury.</span><span class="sxs-lookup"><span data-stu-id="d88ca-132">When an advance or pre-payment is marked as **Ready to invoice**, it is added as a line time on a draft invoice.</span></span> <span data-ttu-id="d88ca-133">K vyrovnání vůči nákladům projektu na další fakturační období lze použít pouze plně fakturovanou zálohu.</span><span class="sxs-lookup"><span data-stu-id="d88ca-133">Only a fully invoiced advance can be used to reconcile against project costs for the next invoice period.</span></span> |

4. <span data-ttu-id="d88ca-134">Vyberte **Uložit a zavřít** v dialogovém okně pro rychlé vytvoření, čímž zálohu zaznamenáte.</span><span class="sxs-lookup"><span data-stu-id="d88ca-134">Select **Save and close** on the quick create dialog to record the advance or the pre-payment.</span></span>
