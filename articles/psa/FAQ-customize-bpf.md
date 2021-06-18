---
title: Jak přizpůsobit tok obchodního procesu týkající se fází projektu?
description: Přehled přizpůsobení toku obchodního procesu týkajícího se fází projektu.
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2e6c60fe67aea908013077bde40c2faeabc2f39e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993138"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="5782f-103">Jak přizpůsobit tok obchodního procesu týkající se fází projektu?</span><span class="sxs-lookup"><span data-stu-id="5782f-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="5782f-104">Existuje známé omezení v dřívějších verzích aplikace Project Service spočívající v tom, že názvy fází v toku obchodního procesu týkajícího se fází projektu musí přesně odpovídat očekávaným anglickým názvům (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="5782f-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="5782f-105">V opačném případě obchodní logika, která závisí na anglických názvech fází, nefunguje podle očekávání.</span><span class="sxs-lookup"><span data-stu-id="5782f-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="5782f-106">Proto nevidíte známé akce, jako je **Přepnout proces** nebo **Upravit proces** dostupné ve formuláři projektu, a přizpůsobení toku obchodního procesu není doporučeno.</span><span class="sxs-lookup"><span data-stu-id="5782f-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="5782f-107">Toto omezení bylo adresováno ve verzi 2.4.5.48 a vyšší.</span><span class="sxs-lookup"><span data-stu-id="5782f-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="5782f-108">Tento článek obsahuje zástupná řešení, pokud potřebujete přizpůsobit výchozí tok obchodního procesu pro starší verze.</span><span class="sxs-lookup"><span data-stu-id="5782f-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="5782f-109">Obchodní logika vyžaduje přesnou shodu s anglickými názvy fází</span><span class="sxs-lookup"><span data-stu-id="5782f-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="5782f-110">Tok obchodního procesu týkající se fází projektu zahrnuje obchodní logiku, která řídí následující chování v aplikaci:</span><span class="sxs-lookup"><span data-stu-id="5782f-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="5782f-111">Když je přiřazen projekt k nabídce, kód nastaví tok obchodního procesu do fáze **Quote**.</span><span class="sxs-lookup"><span data-stu-id="5782f-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="5782f-112">Když je přiřazen projekt ke smlouvě, kód nastaví tok obchodního procesu do fáze **Plan**.</span><span class="sxs-lookup"><span data-stu-id="5782f-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="5782f-113">Když se tok obchodního procesu posune do fáze **Close**, záznam projektu je deaktivovaný.</span><span class="sxs-lookup"><span data-stu-id="5782f-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="5782f-114">Když je projekt deaktivován, formulář projektu a strukturovaný rozpis prací jsou nastaveny pouze na čtení, rezervace pojmenovaných zdrojů se uvolní a všechny přidružené ceníky se deaktivují.</span><span class="sxs-lookup"><span data-stu-id="5782f-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="5782f-115">Tato obchodní logika spoléhá na anglické názvy fází projektu.</span><span class="sxs-lookup"><span data-stu-id="5782f-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="5782f-116">Tato závislost na anglických názvech fází je hlavním důvodem, proč není doporučeno přizpůsobení toku obchodního procesu týkajícího se fází projektu, stejně jako příčinou, proč nevidíte běžné akce toku obchodního procesu, jako je **Přepnout proces** nebo **Upravit proces** na entitě projektu.</span><span class="sxs-lookup"><span data-stu-id="5782f-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="5782f-117">Co se stane, pokud se neshodují názvy fáze s anglickými názvy?</span><span class="sxs-lookup"><span data-stu-id="5782f-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="5782f-118">V aplikaci Project Service verze 1.x na platformě 8.2, když názvy fáze v procesu obchodního toku neodpovídají přesně anglickým názvům fází, obchodní logika, která nastavuje správnou fázi pro nabídky nebo smlouvy, nebo která uzavírá projekt, bude vynechána.</span><span class="sxs-lookup"><span data-stu-id="5782f-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="5782f-119">Nejsou zobrazeny žádné chybové zprávy.</span><span class="sxs-lookup"><span data-stu-id="5782f-119">No error messages are displayed.</span></span> <span data-ttu-id="5782f-120">Proto se zobrazí, že jste schopni přizpůsobit tok obchodního procesu týkajícího se fází projektu.</span><span class="sxs-lookup"><span data-stu-id="5782f-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="5782f-121">Neuvidíte ale žádné automatické procesy fungující pro nabídky, smlouvy a uzavření projektu.</span><span class="sxs-lookup"><span data-stu-id="5782f-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="5782f-122">V aplikaci Project Service verze 2.4.4.30 nebo dřívější na platformě 9.0 došlo k významné změně architektury toků obchodních procesů, což vyžaduje přepsání obchodní logiky toku obchodního procesu.</span><span class="sxs-lookup"><span data-stu-id="5782f-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="5782f-123">Důsledkem je, že pokud se názvy fází procesu neshodují s očekávanými anglickými názvy, zobrazí se chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="5782f-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="5782f-124">Proto, pokud chcete přizpůsobit tok obchodního procesu týkajícího se fází projektu pro entitu projektu, můžete přidat pouze zcela nové fáze k výchozímu toku obchodního procesu pro entitu projektu, zatímco fáze **Quote**, **Plan** a **Close** zůstanou beze změny.</span><span class="sxs-lookup"><span data-stu-id="5782f-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="5782f-125">Toto omezení zajišťuje, že neobdržíte chyby z obchodní logiky, která očekává anglické názvy fází v toku obchodního procesu.</span><span class="sxs-lookup"><span data-stu-id="5782f-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="5782f-126">Ve verzi 2.4.5.48 nebo novější byla obchodní logika popsaná v tomto článku odebrána z výchozího toku obchodního procesu pro entitu projektu.</span><span class="sxs-lookup"><span data-stu-id="5782f-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="5782f-127">Upgrade na tuto verzi nebo novější vám umožní přizpůsobit nebo nahradit výchozí tok obchodního procesu jedním ze svých vlastních.</span><span class="sxs-lookup"><span data-stu-id="5782f-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="5782f-128">Zástupná řešení pro starší verze</span><span class="sxs-lookup"><span data-stu-id="5782f-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="5782f-129">Pokud upgrade není možností, můžete přizpůsobit tok obchodního procesu týkajícího se fází projektu pro entitu projektu pomocí jednoho z těchto dvou způsobů:</span><span class="sxs-lookup"><span data-stu-id="5782f-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="5782f-130">Přidejte další fáze k výchozí konfiguraci při současném zachování anglických názvů fází pro možnosti **Quote**, **Plan** a **Close**.</span><span class="sxs-lookup"><span data-stu-id="5782f-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Snímek obrazovky přidání fází k výchozí konfiguraci](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="5782f-132">Vytvořte svůj vlastní tok obchodního procesu a učiňte ho primárním tokem obchodního procesu pro entitu projektu, který umožňuje mít názvy fáze, které chcete.</span><span class="sxs-lookup"><span data-stu-id="5782f-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="5782f-133">Pokud však chcete použít stejné standardní fáze projektu **Quote**, **Plan** a **Close**, je nutné provést některá přizpůsobení, která jsou vyvozena z vašich vlastních názvů fází.</span><span class="sxs-lookup"><span data-stu-id="5782f-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="5782f-134">Složitější logika je v uzavření projektu, kterou můžete stále spustit pouze deaktivací záznamu projektu.</span><span class="sxs-lookup"><span data-stu-id="5782f-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Vlastní nastavení BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="5782f-136">Další skutečnosti ke zvážení pro aplikaci Project Service verze 2.4.4.30 nebo starší na platformě 9.0</span><span class="sxs-lookup"><span data-stu-id="5782f-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="5782f-137">V aplikaci Project Service verze 2.4.4.30 nebo starší na platformě 9.0 s vlastním tokem obchodního procesu, se pole **Název fáze** na entitě projektu použité v grafu **Projektu podle fáze** a zobrazeních seznamů projektu nebude aktualizovat, protože je kombinované s výchozím tokem obchodního procesu týkajícího se fází projektu.</span><span class="sxs-lookup"><span data-stu-id="5782f-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="5782f-138">Můžete vyřešit tento problém pomocí následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="5782f-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="5782f-139">Přidejte vlastní pole pro zachycení aktuální fáze toku obchodního procesu, která se aktualizuje, jakmile uživatel přejde přes vlastní tok obchodního procesu.</span><span class="sxs-lookup"><span data-stu-id="5782f-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="5782f-140">Upravte graf **Projekt podle fáze** tak, aby pracoval s vaším vlastním polem, namísto s výchozí konfigurací.</span><span class="sxs-lookup"><span data-stu-id="5782f-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="5782f-141">Kroky k vytvoření vlastního toku obchodního procesu pro entitu projektu</span><span class="sxs-lookup"><span data-stu-id="5782f-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="5782f-142">K vytvoření vlastního toku obchodního procesu pro entitu projektu proveďte následující:</span><span class="sxs-lookup"><span data-stu-id="5782f-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="5782f-143">Přejděte na **Nastavení** > **Centrum zpracování**.</span><span class="sxs-lookup"><span data-stu-id="5782f-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="5782f-144">Nekopírujte tok obchodního procesu týkajícího se fází projektu, protože ten rovněž kopíruje obchodní logiku aplikace Project Service.</span><span class="sxs-lookup"><span data-stu-id="5782f-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Vytvořit proces](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="5782f-146">Pomocí návrháře procesu vytvořte názvy fází, které chcete.</span><span class="sxs-lookup"><span data-stu-id="5782f-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="5782f-147">Chcete-li stejnou funkci jako výchozí fáze pro **Quote**, **Plan** a **Close**, budete ji muset vytvořit na základě vlastních názvů fází toku obchodního procesu.</span><span class="sxs-lookup"><span data-stu-id="5782f-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Snímek obrazovky návrháře procesu použitého k přizpůsobení BPF](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="5782f-149">V návrháři procesu klikněte na **Seřadit tok procesu** a učiňte vlastní tok obchodního procesu primárním tokem obchodního procesu pro entitu projektu přesunutím nad tok obchodního procesu týkajícího se fází projektu do horní části seznamu.</span><span class="sxs-lookup"><span data-stu-id="5782f-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="5782f-150">Snímek obrazovky použití možnosti Seřadit tok procesu</span><span class="sxs-lookup"><span data-stu-id="5782f-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="5782f-151">Následující kroky platí pro aplikaci Project Service verze 2.4.4.30 nebo starší na platformě 9.0</span><span class="sxs-lookup"><span data-stu-id="5782f-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="5782f-152">Přidejte nové vlastní pole k entitě projektu pro zachycení vlastních fází ve svém vlastním toku obchodního procesu.</span><span class="sxs-lookup"><span data-stu-id="5782f-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="5782f-153">Budete muset přidat obchodní logiku (modul plug-in/workflow) pro aktualizaci tohoto, když je fáze na vlastním toku obchodního procesu aktualizována.</span><span class="sxs-lookup"><span data-stu-id="5782f-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Snímek obrazovky přizpůsobení entity projektu](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="5782f-155">Upravte graf **Projekt podle fáze** pro použití vašeho nového vlastního pole pro fáze.</span><span class="sxs-lookup"><span data-stu-id="5782f-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Snímek obrazovky použití grafu Projekt podle fáze](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="5782f-157">Upravte jakékoliv zobrazení pro entitu projektu, aby zahrnovalo vaše nové vlastní pole pro fáze.</span><span class="sxs-lookup"><span data-stu-id="5782f-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Snímek obrazovky úprav zobrazení na entitě projektu](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]