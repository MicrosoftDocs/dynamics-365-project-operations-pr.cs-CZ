---
title: Projekty odhadu výnosů pevné ceny
description: Toto téma obsahuje informace o výnosech s fixní cenou v projektech.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531390"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="7d558-103">Projekty odhadu výnosů pevné ceny</span><span class="sxs-lookup"><span data-stu-id="7d558-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="7d558-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="7d558-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7d558-105">Když vytvoříte řádek smlouvy projektu s následujícími atributy v Dynamics 365 Project Operations v Microsoft Dataverse, systém automaticky vytvoří projekt odhadu výnosů s fixní cenou.</span><span class="sxs-lookup"><span data-stu-id="7d558-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="7d558-106">Informace v tomto projektu jsou založeny na následujícím:</span><span class="sxs-lookup"><span data-stu-id="7d558-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="7d558-107">Metoda fakturace za pevnou cenu.</span><span class="sxs-lookup"><span data-stu-id="7d558-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="7d558-108">Přidružený projekt</span><span class="sxs-lookup"><span data-stu-id="7d558-108">An associated project.</span></span>
  - <span data-ttu-id="7d558-109">Alespoň jeden milník definovaný na kartě **Harmonogram faktur** na stránce **Řádek projektové smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="7d558-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="7d558-110">Kontrola projektů odhadu výnosů s fixní cenou</span><span class="sxs-lookup"><span data-stu-id="7d558-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="7d558-111">Chcete-li zkontrolovat projekty odhadů výnosů s pevnou cenou, proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="7d558-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="7d558-112">V prostředí Dynamics 365 Finance přejděte na **Řízení projektů a účetnictví** > **Projekty** > **Projekty odhadu výnosů s fixní cenou**.</span><span class="sxs-lookup"><span data-stu-id="7d558-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="7d558-113">Vyberte projekt, který chcete zobrazit, a dvakrát klikněte na ikonu **ID projektu odhadu**, chcete-li otevřít záznam a zkontrolovat podrobnosti projektu.</span><span class="sxs-lookup"><span data-stu-id="7d558-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="7d558-114">Rozbalte kartu **Projekt**. Jeden projekt uvidíte v mřížce **Vybrané projekty**.</span><span class="sxs-lookup"><span data-stu-id="7d558-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="7d558-115">Systém toto používá jako výchozí projekt, protože se jedná o projekt přidružený k řádku smlouvy projektu.</span><span class="sxs-lookup"><span data-stu-id="7d558-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="7d558-116">Chcete-li změnit přidružení, vyberte další projekty a přidejte je do mřížky **Vybrané projekty**.</span><span class="sxs-lookup"><span data-stu-id="7d558-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="7d558-117">Pokud je v této mřížce vybráno více projektů, vypočítá se procento dokončení projektu a odhady výnosů společně pro všechny vybrané projekty.</span><span class="sxs-lookup"><span data-stu-id="7d558-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="7d558-118">Náklady na projekt, profil výnosů, šablonu nákladů a kód období lze nastavit ručně.</span><span class="sxs-lookup"><span data-stu-id="7d558-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="7d558-119">Pokud nejsou nastaveny ručně, výchozí hodnoty jsou během prvního výpočtu odhadu pro projekt pomocí pravidel nakonfigurovaných pro profily nákladů a výnosů projektu.</span><span class="sxs-lookup"><span data-stu-id="7d558-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>
