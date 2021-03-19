---
title: Konfigurace integrace Project Operations podle právnické osoby
description: Toto téma poskytuje informace o tom, jak nastavit integraci podle právnické osoby v aplikaci Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ccdbdce6b7d006adc9be2b5f3573dd8e79dd2b8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276970"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="6cf9b-103">Konfigurace integrace Project Operations podle právnické osoby</span><span class="sxs-lookup"><span data-stu-id="6cf9b-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="6cf9b-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="6cf9b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6cf9b-105">Toto téma vás provede kroky potřebnými ke konfiguraci Dynamics 365 Project Operations pro právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="6cf9b-106">Povolení klíče oprávnění v Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="6cf9b-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="6cf9b-107">Chcete-li povolit požadované funkce, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="6cf9b-108">V aplikaci Dynamics 365 Finance přejděte do pracovního prostoru **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="6cf9b-109">V poli **Seznam funkcí** vyhledejte a povolte následující funkce:</span><span class="sxs-lookup"><span data-stu-id="6cf9b-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="6cf9b-110">**Povolit více řádků smlouvy pro projekt**</span><span class="sxs-lookup"><span data-stu-id="6cf9b-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="6cf9b-111">**Povolit Project Operations v Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="6cf9b-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="6cf9b-112">Pokud nevidíte uvedené **Klíče oprávnění**, ověřte, zda vaše verze Finance splňuje požadavek na minimální verzi (verze aplikace 10.0.13 se všemi použitými aktualizacemi kvality nebo vyšší).</span><span class="sxs-lookup"><span data-stu-id="6cf9b-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="6cf9b-113">Výběrem položky **Kontrola aktualizací** aktualizujte seznam funkcí.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="6cf9b-114">Definování scénáře nasazení Project Operations pro právnickou osobu</span><span class="sxs-lookup"><span data-stu-id="6cf9b-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="6cf9b-115">Aplikaci Project Operations můžete v Dynamics 365 Customer Engagement povolit na úrovni právnických osob.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="6cf9b-116">Můžete mít jednu právnickou osobu, která používá Project Operations v Dynamics 365 Customer Engagement pro scénáře založené na zdrojích / položkách, které nejsou na skladě.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="6cf9b-117">Ve stejném prostředí můžete mít jinou právnickou osobu, která používá Project Operations pro scénáře se skladovým materiálem a výrobními příkazy.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="6cf9b-118">V Dynamics 365 Finance přejděte do nabídky **Řízení projektů a účetnictví** > **Nastavení** > **Globální parametry modulu Řízení a účetnictví projektu**.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="6cf9b-119">V seznamu dostupných právnických osob vyberte entity, u kterých budou povoleny smlouvy s více řádky a Project Operations v Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="6cf9b-120">Nevybírejte právnické osoby, které budou používat Project Operations pro scénáře se skladovým materiálem a výrobními příkazy.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="6cf9b-121">Právnickou osobu lze vybrat, pouze pokud nemá žádné stávající projekty.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="6cf9b-122">Konfigurace parametrů modulu Řízení projektu a účetnictví</span><span class="sxs-lookup"><span data-stu-id="6cf9b-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="6cf9b-123">Každá právnická osoba využívající Project Operations v Dynamics 365 Customer Engagement potřebuje sadu výchozích parametrů.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="6cf9b-124">Tyto parametry se konfigurují na kartě **Project Operations** ve stránce **Parametry řízení projektu a účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="6cf9b-125">K dispozici jsou tyto parametry:</span><span class="sxs-lookup"><span data-stu-id="6cf9b-125">The parameters are:</span></span>

  - <span data-ttu-id="6cf9b-126">**Výchozí hodnoty typu účtování**: Project Operations používá pevnou sadu výchozích typů účtování, které musejí být mapovány na vlastnosti řádku ve Finance.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="6cf9b-127">Vytvořte záznam pro každý typ účtování: **Nezadáno**, **Účtovatelné**, **Neúčtovatelné**, **Doplňkové** a **Není dostupné**.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="6cf9b-128">**Výchozí nastavení kategorie projektu**: Vyberte výchozí kategorie projektu, které se mají použít pro každý typ transakce.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="6cf9b-129">Tyto výchozí hodnoty budou použity v **Deníku integrace Project Operations** a v odhadech, kde není pro skutečný projekt zadána žádná kategorie transakcí.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="6cf9b-130">**Prognózy** : Vyberte model prognózy, který se použije pro odhady času a výdajů.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]