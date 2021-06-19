---
title: Aktualizace atributů modulů plug-in tak, aby zahrnovaly nové cenové dimenze
description: Toto téma obsahuje informace o aktualizaci atributů modulů plug-in pro cenové dimenze.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b0d50733340f277453f4ef5b52bdd3ee089449cd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012803"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="24ce4-103">Aktualizace atributů modulů plug-in tak, aby zahrnovaly nové cenové dimenze</span><span class="sxs-lookup"><span data-stu-id="24ce4-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="24ce4-104">Pokud nepoužíváte funkce Vypracování nabídky a Uzavírání smluv služby Project Service Automation (PSA), můžete toto téma přeskočit.</span><span class="sxs-lookup"><span data-stu-id="24ce4-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="24ce4-105">Toto téma předpokládá, že jste dokončili postupy v tématech [Vytvoření vlastních polí a entit](create-custom-fields-entities.md), [Přidání vlastních polí do nastavení ceny a transakčních entit](field-references.md) a [Nastavení vlastních polí jako cenových dimenzí](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="24ce4-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="24ce4-106">Pokud jste tyto postupy nedokončili, vraťte se zpět, dokončete je a vraťte se k tomuto tématu.</span><span class="sxs-lookup"><span data-stu-id="24ce4-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="24ce4-107">Při vytvoření detailu řádku nabídky na stránce **Řádek nabídky** pro řádek nabídky projektu systém vytvoří dva řádky odhadu na pozadí – jeden řádek pro nákladovou stranu odhadu a jeden pro prodejní stranu.</span><span class="sxs-lookup"><span data-stu-id="24ce4-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="24ce4-108">To je stejné pro řádky projektové smlouvy.</span><span class="sxs-lookup"><span data-stu-id="24ce4-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="24ce4-109">Pokud změníte množství nebo pole na straně nákladů, bude tato změna rozšířena na stranu prodeje.</span><span class="sxs-lookup"><span data-stu-id="24ce4-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="24ce4-110">To je možné kvůli tomu, že následující moduly plug-in je nutné po změně cenových dimenzí znovu zaregistrovat.</span><span class="sxs-lookup"><span data-stu-id="24ce4-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="24ce4-111">PreOperationContractLineDetailUpdate – Aktualizuje **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="24ce4-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="24ce4-112">PreOperationQuoteLineDetailUpdate – Aktualizuje **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="24ce4-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="24ce4-113">Následující postup vysvětluje proces registrace modulů plug-in.</span><span class="sxs-lookup"><span data-stu-id="24ce4-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="24ce4-114">Otevřete **PluginRegistrationTool** a připojte se k online instanci.</span><span class="sxs-lookup"><span data-stu-id="24ce4-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="24ce4-115">Klikněte na tlačítko **Hledat** a vyhledejte modul plug-in, který chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="24ce4-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Snímek obrazovky vyhledávacího stromu](media/PRT-1.png)

3. <span data-ttu-id="24ce4-117">Po nalezení modulu plug-in jej vyberte a klikněte na tlačítko **Vybrat v hlavním formuláři**.</span><span class="sxs-lookup"><span data-stu-id="24ce4-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="24ce4-118">Vyberte krok modulu plug-in, který chcete aktualizovat, klikněte pravým tlačítkem myši a vyberte položku **Aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="24ce4-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Snímek obrazovky modulu plug-in, který má být aktualizován](media/PRT-2.png)
 
5. <span data-ttu-id="24ce4-120">V okně aktualizace klikněte na tři tečky (**...**) v atributech filtrování.</span><span class="sxs-lookup"><span data-stu-id="24ce4-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Snímek obrazovky aktualizace existujících informací kroku konfigurace](media/PRT-3.png)
 
6. <span data-ttu-id="24ce4-122">Zaškrtněte políčka atributu ceny.</span><span class="sxs-lookup"><span data-stu-id="24ce4-122">Select the pricing attribute check boxes.</span></span>

 ![Snímek obrazovky zaškrtnutí políčka pro atributy ceny](media/PRT-4.png)

7. <span data-ttu-id="24ce4-124">Kliknutím na tlačítko **OK** zavřete stránku a pak vyberte možnost **Aktualizovat krok**.</span><span class="sxs-lookup"><span data-stu-id="24ce4-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Snímek obrazovky s tlačítkem „Aktualizovat krok“](media/PRT-5.png)
 
8. <span data-ttu-id="24ce4-126">Tento postup zopakujte pro druhý modul plug-in **PreOperationQuoteLineDetail – Aktualizace msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="24ce4-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="24ce4-127">Zavřete nástroj Plug-in Registration Tool.</span><span class="sxs-lookup"><span data-stu-id="24ce4-127">Close the plug-in registration tool.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]