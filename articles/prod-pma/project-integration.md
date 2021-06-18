---
title: Integrace aplikace Microsoft Project Client
description: Plánování a údržba projektového harmonogramu mohou být složité, a proto projektoví manažeři musí používat nástroje, které jim pomohou tento úkol zvládnout. Integrace s klientem Microsoft Project Client poskytuje podporu pro otevření a správu strukturovaného rozpisu prací na projektu.
author: Yowelle
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 032d726bb6206c563b573f30d13fe2697a13c949
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999438"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="84613-104">Integrace aplikace Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="84613-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84613-105">Plánování a údržba projektového harmonogramu mohou být složité, a proto projektoví manažeři musí používat nástroje, které jim pomohou tento úkol zvládnout.</span><span class="sxs-lookup"><span data-stu-id="84613-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="84613-106">Integrace s klientem Microsoft Project Client poskytuje podporu pro otevření a správu strukturovaného rozpisu prací na projektu.</span><span class="sxs-lookup"><span data-stu-id="84613-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="84613-107">Manažer projektu může publikovat jakékoli změny zpět do strukturovaného rozpisu prací na projektu v Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="84613-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="84613-108">Pokud používáte červencovou aktualizaci (verze 10.0.4), musíte nainstalovat aktualizace KB 4054797 a 4055884.</span><span class="sxs-lookup"><span data-stu-id="84613-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="84613-109">Konfigurace doplňku Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="84613-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="84613-110">Chcete-li povolit integraci s doplňkem Microsoft Project Client, je nutné nainstalovat doplněk Microsoft Dynamics 365 do aplikace Microsoft Project klienta uživatele.</span><span class="sxs-lookup"><span data-stu-id="84613-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="84613-111">To se provádí otevřením **pracovního prostoru pro správu projektů**.</span><span class="sxs-lookup"><span data-stu-id="84613-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="84613-112">•   Klikněte na příkaz **Konfigurace doplňku klienta projektu** v části **Odkazy** > **Nastavení** pracovního prostoru.</span><span class="sxs-lookup"><span data-stu-id="84613-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="84613-113">•   Klikněte na položku **Otevřít** a po výzvě klikněte na možnost **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="84613-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="84613-114">Otevření a úprava stávajícího konceptu strukturovaného rozpisu prací v doplňku Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="84613-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="84613-115">Pokud má projekt v Dynamics 365 Finance již vytvořený strukturovaný rozpis prací, lze strukturovaný rozpis prací otevřít v aplikaci Microsoft Project Client, pokud je ve stavu konceptu.</span><span class="sxs-lookup"><span data-stu-id="84613-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="84613-116">Chcete-li otevření provést ze stránky **Projekt**, klikněte na odkaz **Otevřít v Microsoft Project** na kartě **Plán**. Tuto stránku lze otevřít také z aplikace Microsoft Project Client kliknutím na možnost **Otevřít** na kartě **Microsoft Dynamics 365**. V seznamu vyberte **Právnická osoba** a **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="84613-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="84613-117">Pokud jako prohlížeč používáte Internet Explorer, budete muset kliknout na **Uložit** a ručně otevřít soubor z umístění, do kterého je stažen.</span><span class="sxs-lookup"><span data-stu-id="84613-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="84613-118">Nebo klikněte **Uložit a otevřít** a otevřete soubor v aplikaci Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="84613-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="84613-119">Při ukládání neměňte název souboru.</span><span class="sxs-lookup"><span data-stu-id="84613-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="84613-120">Před provedením jakýchkoli úprav souboru pomocí aplikace Microsoft Project Client je nutné jej rezervovat. Klikněte na příkaz **Rezervovat** na kartě **Microsoft Dynamics 365**. Rezervace nedovolí ostatním uživatelům upravovat současně strukturovaný rozpis prací v rámci aplikace Finance.</span><span class="sxs-lookup"><span data-stu-id="84613-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="84613-121">Chcete-li po dokončení všech úprav strukturovaný rozpis prací publikovat, klikněte na **Vrátit se změnami** na kartě **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="84613-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="84613-122">Pokud již byl projektový tým přidán do projektu v aplikaci Finance, seznam zdrojů se naplní členy týmu.</span><span class="sxs-lookup"><span data-stu-id="84613-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="84613-123">Pokud projektový tým ještě nebyl do projektu přidán, můžete vybrat zdroje a vytvořit tým uvnitř aplikace Microsoft Project Client kliknutím na tlačítko **Zdroje** na kartě **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="84613-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="84613-124">Následující data budou synchronizována zpět do Finance jako součást procesu vrácení se změnami:</span><span class="sxs-lookup"><span data-stu-id="84613-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="84613-125">•   Název úkolu</span><span class="sxs-lookup"><span data-stu-id="84613-125">•   Task name</span></span>

<span data-ttu-id="84613-126">•   Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="84613-126">•   Start date</span></span>

<span data-ttu-id="84613-127">•   Datum dokončení</span><span class="sxs-lookup"><span data-stu-id="84613-127">•   Finish date</span></span>

<span data-ttu-id="84613-128">•   Předchůdci</span><span class="sxs-lookup"><span data-stu-id="84613-128">•   Predecessors</span></span>

<span data-ttu-id="84613-129">•   Názvy zdrojů</span><span class="sxs-lookup"><span data-stu-id="84613-129">•   Resource names</span></span>

<span data-ttu-id="84613-130">•   Kategorie</span><span class="sxs-lookup"><span data-stu-id="84613-130">•   Category</span></span>

<span data-ttu-id="84613-131">•   Kategorie zdroje</span><span class="sxs-lookup"><span data-stu-id="84613-131">•   Resource category</span></span>

<span data-ttu-id="84613-132">•   Pracovní doba</span><span class="sxs-lookup"><span data-stu-id="84613-132">•   Work hours</span></span>

<span data-ttu-id="84613-133">•   Poznámky</span><span class="sxs-lookup"><span data-stu-id="84613-133">•   Notes</span></span>

<span data-ttu-id="84613-134">•   Priorita</span><span class="sxs-lookup"><span data-stu-id="84613-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="84613-135">Pokud do souboru aplikace Microsoft Project Client přidáte jakékoli další sloupce, nebudou do souboru uloženy a po opětovném otevření souboru se nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="84613-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="84613-136">Vytvoření strukturovaného rozpisu prací pro existující projekt v aplikaci Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="84613-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="84613-137">Chcete-li vytvořit nový strukturovaný rozpis prací v aplikaci Microsoft Project Client, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="84613-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="84613-138">Otevřete aplikaci Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="84613-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="84613-139">Na kartě **Microsoft Dynamics 365** klikněte na položku **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="84613-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="84613-140">Vyberte hodnotu **Právnická osoba** pro projekt.</span><span class="sxs-lookup"><span data-stu-id="84613-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="84613-141">Vyberte **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="84613-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="84613-142">Klikněte na příkaz **Rezervovat** na kartě **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="84613-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="84613-143">Až budete připraveni publikovat do aplikace Finance, klikněte na **Vrátit se změnami** na kartě **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="84613-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="84613-144">Nahrazení stávajícího strukturovaného rozpisu prací pro existující projekt v aplikaci Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="84613-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="84613-145">Chcete-li vytvořit nový strukturovaný rozpis prací pomocí aplikace Microsoft Project Client a nahradit stávající strukturovaný rozpis prací pro existující projekt, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="84613-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="84613-146">Otevřete aplikaci Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="84613-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="84613-147">Vytvořte plán v aplikaci Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="84613-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="84613-148">Na kartě **Microsoft Dynamics 365** klikněte na příkaz **Uložit změny** > **Nahradit stávající projekt**.</span><span class="sxs-lookup"><span data-stu-id="84613-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="84613-149">Vyberte hodnotu **Právnická osoba** pro projekt.</span><span class="sxs-lookup"><span data-stu-id="84613-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="84613-150">Vyberte **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="84613-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="84613-151">Klikněte na **OK**.</span><span class="sxs-lookup"><span data-stu-id="84613-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="84613-152">Vytvoření nového projektu v aplikaci Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="84613-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="84613-153">Otevřete aplikaci Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="84613-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="84613-154">Vytvořte plán v aplikaci Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="84613-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="84613-155">Na kartě **Microsoft Dynamics 365** klikněte na příkaz **Uložit změny** > **Uložit do nového projektu**.</span><span class="sxs-lookup"><span data-stu-id="84613-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="84613-156">Vyberte hodnotu **Právnická osoba** pro projekt.</span><span class="sxs-lookup"><span data-stu-id="84613-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="84613-157">Zadejte **ID projektu**, pokud je třeba.</span><span class="sxs-lookup"><span data-stu-id="84613-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="84613-158">Zadejte **Název projektu**.</span><span class="sxs-lookup"><span data-stu-id="84613-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="84613-159">Zvolte hodnoty **Typ projektu**, **Projektová skupina** a **ID smlouvy o projektu**.</span><span class="sxs-lookup"><span data-stu-id="84613-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="84613-160">Alternativně můžete vytvořit novou projektovou smlouvu kliknutím na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="84613-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="84613-161">Vyberte **Kalendář**, který bude použit pro zajišťování zdrojů.</span><span class="sxs-lookup"><span data-stu-id="84613-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="84613-162">Klikněte na **OK**.</span><span class="sxs-lookup"><span data-stu-id="84613-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]