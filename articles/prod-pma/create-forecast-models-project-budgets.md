---
title: Vytvoření modelů prognóz pro rozpočty projektů
description: Tento téma popisuje, jak vytvořit model prognózy pro zbývající rozpočty.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073916"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="559f0-103">Vytvoření modelů prognóz pro rozpočty projektů</span><span class="sxs-lookup"><span data-stu-id="559f0-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="559f0-104">Tento téma popisuje, jak vytvořit model prognózy pro zbývající rozpočty.</span><span class="sxs-lookup"><span data-stu-id="559f0-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="559f0-105">Projekt, který podléhá kontrole rozpočtu, používá dva typy rozpočtů: původní a zbývající.</span><span class="sxs-lookup"><span data-stu-id="559f0-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="559f0-106">Když vytváříte rozpočet projektu, musíte určit původní a zbývající modely prognózy rozpočtu, které byly vytvořeny na stránce **Předpovědní modely**.</span><span class="sxs-lookup"><span data-stu-id="559f0-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="559f0-107">Rozpočty projektu založené na zadaných modelech se vytvářejí při potvrzení rozpočtu projektu.</span><span class="sxs-lookup"><span data-stu-id="559f0-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="559f0-108">Model předpovědi, který se používá pro kontrolu rozpočtu, nemůže mít podmodel ani jej nelze použít jako podmodel.</span><span class="sxs-lookup"><span data-stu-id="559f0-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="559f0-109">Vyberte možnost **Řízení projektů a účetnictví** > **Nastavení** > **Prognózy**  > **Předpovědní modely**.</span><span class="sxs-lookup"><span data-stu-id="559f0-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="559f0-110">Vybráním možnosti **Nový** vytvořte nový model předpovědi a poté zadejte identifikační číslo modelu a název nového modelu.</span><span class="sxs-lookup"><span data-stu-id="559f0-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="559f0-111">Nastavte možnost **Zastaveno** na **Ano** , abyste zabránili jakýmkoli změnám v řádcích prognózy pro předpovědní model.</span><span class="sxs-lookup"><span data-stu-id="559f0-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="559f0-112">Pokud by řádky prognózy, ke kterým je model přidružen, měly generovat prognózy peněžních toků v hlavní knize, nastavte možnost **Zahrnout do prognóz peněžních toků** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="559f0-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="559f0-113">Chcete-li jako datum faktury použít datum projektu, nastavte **Datum faktury předpovědi** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="559f0-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="559f0-114">V poli **Typ rozpočtu** vyberte jeden z následujících typů modelů:</span><span class="sxs-lookup"><span data-stu-id="559f0-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="559f0-115">**Původní rozpočet** : Použijte původní částky rozpočtu, které jsou přiděleny, když je vytvořen a schválen původní rozpočet.</span><span class="sxs-lookup"><span data-stu-id="559f0-115">**Original budget** : Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="559f0-116">**Zbývající rozpočet** : Použijte zbývající částky rozpočtu během doby trvání projektu.</span><span class="sxs-lookup"><span data-stu-id="559f0-116">**Remaining budget** : Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="559f0-117">Zůstatky v tomto modelu prognózy se snižují o skutečné transakce a zvyšují nebo snižují revize rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="559f0-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="559f0-118">**Převádět** : Použijte částky převedeného rozpočtu pro projekt.</span><span class="sxs-lookup"><span data-stu-id="559f0-118">**Carry-forward** : Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="559f0-119">Převedení je volitelný proces, který lze spustit a převést nevyužité částky rozpočtu z jednoho fiskálního roku do druhého.</span><span class="sxs-lookup"><span data-stu-id="559f0-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="559f0-120">Nastavte následující možnosti podle potřeby:</span><span class="sxs-lookup"><span data-stu-id="559f0-120">Set the following options as required:</span></span>

   - <span data-ttu-id="559f0-121">Chcete-li jako datum faktury použít datum projektu, zapněte **Datum faktury předpovědi**.</span><span class="sxs-lookup"><span data-stu-id="559f0-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="559f0-122">Zapněte možnost **Předpověď s WIP** , chcete-li předpovídat na základě nedokončené výroby (WIP) a poté vyberte typ WIP.</span><span class="sxs-lookup"><span data-stu-id="559f0-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="559f0-123">Můžete ponechat výchozí **Typ rozpočtu** jako **Žádný** nebo zadat nový typ.</span><span class="sxs-lookup"><span data-stu-id="559f0-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="559f0-124">Po změně záznamu nelze typ rozpočtu změnit.</span><span class="sxs-lookup"><span data-stu-id="559f0-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="559f0-125">Pokud změníte výchozí typ rozpočtu, nebudou pro aktualizace k dispozici všechny ostatní možnosti a nebudete moci tento předpovědní model znovu použít.</span><span class="sxs-lookup"><span data-stu-id="559f0-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

