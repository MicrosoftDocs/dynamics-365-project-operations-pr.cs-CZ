---
title: Vytvoření manuální proforma faktury
description: Toto téma poskytuje informace o o vytváření manuálních proforma faktur v aplikaci Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/20/2020
ms.locfileid: "4074009"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="050a5-103">Vytvoření manuální proforma faktury</span><span class="sxs-lookup"><span data-stu-id="050a5-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="050a5-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="050a5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="050a5-105">V Dynamics 365 Project Operations lze proforma faktury vytvářet ručně podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="050a5-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="050a5-106">Proforma fakturu můžete ručně vytvořit na stránce seznamu **Projektové smlouvy** ze seznamu nebo ze stránky s podrobnostmi **Projektová smlouva**.</span><span class="sxs-lookup"><span data-stu-id="050a5-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="050a5-107">Stránka se seznamem Projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="050a5-107">Project Contracts list page</span></span>

<span data-ttu-id="050a5-108">Na stránce se seznamem **Projektové smlouvy** vyberte jednu nebo více projektových smluv a vytvořte faktury pro všechny vybrané záznamy.</span><span class="sxs-lookup"><span data-stu-id="050a5-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="050a5-109">Systém zkontroluje, která z vybraných projektových smluv má nevyřízené položky **Připraveno k fakturaci** datované před dnešním datem.</span><span class="sxs-lookup"><span data-stu-id="050a5-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="050a5-110">Z těchto smluv systém vytvoří koncepty proforma faktur.</span><span class="sxs-lookup"><span data-stu-id="050a5-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="050a5-111">Pokud má projektová smlouva více zákazníků, může být vytvořena jedna faktura na zákazníka a více faktur na projektovou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="050a5-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="050a5-112">Všechny vytvořené faktury projektu jsou k dispozici na stránce **Faktura** v části **Fakturace** oblasti **Prodej**.</span><span class="sxs-lookup"><span data-stu-id="050a5-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="050a5-113">Stránka s podrobnostmi projektových smluv</span><span class="sxs-lookup"><span data-stu-id="050a5-113">Project Contract details page</span></span>

<span data-ttu-id="050a5-114">Proforma fakturu lze také vytvořit na stránce s podrobnostmi **Smlouva o projektu** , kde se vytváří faktura za konkrétní smlouvu o projektu.</span><span class="sxs-lookup"><span data-stu-id="050a5-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="050a5-115">Systém zkontroluje, že projektová smlouva má nevyřízené položky **Připraveno k fakturaci** datované před dnešním datem.</span><span class="sxs-lookup"><span data-stu-id="050a5-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="050a5-116">Z těchto smluv systém vytváří návrhy proforma faktur na základě počtu zákazníků na každém řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="050a5-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="050a5-117">Když je vytvořena jedna proforma faktura, otevře se stránka **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="050a5-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="050a5-118">Pokud je pro danou projektovou smlouvu vytvořeno více faktur, se otevře stránka se seznamem **Faktury** , kde se zobrazí všechny vytvořené faktury.</span><span class="sxs-lookup"><span data-stu-id="050a5-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
