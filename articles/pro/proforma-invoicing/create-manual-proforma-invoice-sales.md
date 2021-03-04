---
title: Vytvoření manuální proforma faktury – omezené
description: Toto téma poskytuje informace o o vytváření manuálních proforma faktur v aplikaci Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764495"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="dd557-103">Vytvoření manuální proforma faktury – omezené</span><span class="sxs-lookup"><span data-stu-id="dd557-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="dd557-104">_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="dd557-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dd557-105">V Dynamics 365 Project Operations lze proforma faktury podle potřeby vytvářet ručně.</span><span class="sxs-lookup"><span data-stu-id="dd557-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="dd557-106">Proforma fakturu můžete ručně vytvořit na stránce seznamu **Projektové smlouvy** ze seznamu nebo ze stránky s podrobnostmi **Projektová smlouva**.</span><span class="sxs-lookup"><span data-stu-id="dd557-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="dd557-107">Stránka se seznamem Projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="dd557-107">Project Contracts list page</span></span>

<span data-ttu-id="dd557-108">Na stránce se seznamem **Projektové smlouvy** vyberte jednu nebo více projektových smluv a vytvořte faktury pro všechny vybrané záznamy.</span><span class="sxs-lookup"><span data-stu-id="dd557-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="dd557-109">Systém zkontroluje, která z vybraných projektových smluv má nevyřízené položky **Připraveno k fakturaci** datované před dnešním datem.</span><span class="sxs-lookup"><span data-stu-id="dd557-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="dd557-110">Z těchto smluv systém vytvoří koncepty proforma faktur.</span><span class="sxs-lookup"><span data-stu-id="dd557-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="dd557-111">Pokud má projektová smlouva více zákazníků, může být vytvořena jedna faktura na zákazníka a více faktur na projektovou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="dd557-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="dd557-112">Všechny vytvořené faktury projektu jsou k dispozici na stránce **Faktura** v části **Fakturace** oblasti **Prodej**.</span><span class="sxs-lookup"><span data-stu-id="dd557-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="dd557-113">Stránka s podrobnostmi projektových smluv</span><span class="sxs-lookup"><span data-stu-id="dd557-113">Project Contract details page</span></span>

<span data-ttu-id="dd557-114">Pro forma fakturu lze také vytvořit na stránce s podrobnostmi **Smlouva o projektu**.</span><span class="sxs-lookup"><span data-stu-id="dd557-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="dd557-115">Systém ověří, že projektová smlouva má nevyřízené položky **Připraveno k fakturaci** datované před dnešním datem.</span><span class="sxs-lookup"><span data-stu-id="dd557-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="dd557-116">Z těchto smluv systém vytváří návrhy proforma faktur na základě počtu zákazníků na každém řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="dd557-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="dd557-117">Když je vytvořena jedna proforma faktura, otevře se stránka **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="dd557-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="dd557-118">Pokud je pro danou projektovou smlouvu vytvořeno více faktur, otevře se stránka seznamu **Faktury** se seznamem, kde se zobrazí všechny vytvořené faktury.</span><span class="sxs-lookup"><span data-stu-id="dd557-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>
