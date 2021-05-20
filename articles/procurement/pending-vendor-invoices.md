---
title: Zakoupení neskladovaných materiálů pomocí nevyřízené faktury dodavatele
description: Tento téma vysvětluje, jak zaznamenat nevyřízené faktury dodavatele.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880630"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="ca8ce-103">Zakoupení neskladovaných materiálů pomocí nevyřízené faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="ca8ce-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="ca8ce-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="ca8ce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ca8ce-105">Když společnost pro projekt pořizuje neskladované materiály, lze náklady okamžitě zaznamenat oproti projektu.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="ca8ce-106">Například Contoso Robotics USA provádí projekt obnovy zařízení a potřebuje softwarové licence.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="ca8ce-107">Tyto licence jsou zakoupeny od dodavatele třetí strany.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="ca8ce-108">Pomocí Dynamics 365 Finance účetní odpovědný za účty zaznamená dokument nevyřízené faktury dodavatele a přiřadí náklady na licenci přímo proti projektu obnovy zařízení.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="ca8ce-109">Než použijete funkce popsané v tomto tématu, zkontrolujte a použijte požadované konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="ca8ce-110">Další informace viz [Povolené neskladovaných materiálů a nevyřízených faktury dodavatele](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="ca8ce-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="ca8ce-111">Zaúčtování nevyřízené faktury dodavatele související s projektem</span><span class="sxs-lookup"><span data-stu-id="ca8ce-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="ca8ce-112">Nevyřízené faktury dodavatele lze zaznamenat na stránce **Nevyřízené faktury dodavatele** (**Závazky** > **Faktury** > **Nevyřízené faktury dodavatele**).</span><span class="sxs-lookup"><span data-stu-id="ca8ce-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="ca8ce-113">Chcete-li zaúčtovat nevyřízenou fakturu dodavatele související s projektem, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="ca8ce-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="ca8ce-114">Přejděte na **Závazky** > **Faktury** a vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="ca8ce-115">V poli **Účet faktury** vyberte dodavatele a v poli **Číslo** zadejte identifikaci faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="ca8ce-116">Přidejte řádek na fakturu dodavatele a do pole **Číslo položky** vyberte skladovou položku zakoupenou od dodavatele.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="ca8ce-117">Řádky faktury dodavatele založené na kategorii nákupu nelze proti projektu zaznamenat.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="ca8ce-118">Přidejte zakoupené množství.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-118">Add the quantity purchased.</span></span> <span data-ttu-id="ca8ce-119">Systém naplní jednotkovou cenu na základě konfigurace ceny zboží, které není skladem.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="ca8ce-120">Ověřte celkovou částku a další požadované podrobnosti na řádku.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="ca8ce-121">Na řádku podrobnosti na kartě **Projekt** vyberte ID projektu, do kterého bude tato položka zaznamenána.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="ca8ce-122">Volitelně vyberte číslo aktivity a aktualizujte kategorii projektu a vlastnost řádku.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="ca8ce-123">Zaúčtujte nevyřízenou fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-123">Post pending vendor invoice.</span></span> <span data-ttu-id="ca8ce-124">Když je faktura zaúčtována, systém zaznamená:</span><span class="sxs-lookup"><span data-stu-id="ca8ce-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="ca8ce-125">Částka zůstatku dodavatele.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="ca8ce-126">Částka DPH.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-126">The sales tax amount.</span></span>
    - <span data-ttu-id="ca8ce-127">Náklady na projekt se zaznamenají na účet integrace nákupu.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="ca8ce-128">Skutečná transakce projektu v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="ca8ce-129">Tato transakce je dále zpracovávána pomocí [deníku integrace Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="ca8ce-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="ca8ce-130">Zaúčtováním tohoto deníku se částka přesune z účtu integrace nákupu do účtu nákladů projektu.</span><span class="sxs-lookup"><span data-stu-id="ca8ce-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
