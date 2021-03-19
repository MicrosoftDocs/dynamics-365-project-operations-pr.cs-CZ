---
title: Řešení potíží s prací v mřížce úloh
description: Tento téma poskytuje potřebné informace o odstraňování potíží při práci v mřížce úloh.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286555"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="a1e97-103">Řešení potíží s prací v mřížce úloh</span><span class="sxs-lookup"><span data-stu-id="a1e97-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="a1e97-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="a1e97-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a1e97-105">Tento téma popisuje, jak opravit problémy, se kterými se můžete setkat při práci se správou nákladů.</span><span class="sxs-lookup"><span data-stu-id="a1e97-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="a1e97-106">Povolení souborů cookie</span><span class="sxs-lookup"><span data-stu-id="a1e97-106">Enable cookies</span></span>

<span data-ttu-id="a1e97-107">Aby bylo možné vykreslit strukturu rozpisu práce, vyžaduje Project Operations povolení souborů cookie třetích stran.</span><span class="sxs-lookup"><span data-stu-id="a1e97-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="a1e97-108">Pokud nejsou povoleny soubory cookie třetích stran, místo zobrazení úkolů se zobrazí prázdná stránka po výběru karty **Úkoly** na stránce **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="a1e97-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Prázdná karta, pokud nejsou povoleny soubory cookie třetích stran](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="a1e97-110">Zástupné řešení</span><span class="sxs-lookup"><span data-stu-id="a1e97-110">Workaround</span></span>
<span data-ttu-id="a1e97-111">U prohlížečů Microsoft Edge a Google Chrome následující postupy popisují, jak aktualizovat nastavení prohlížeče tak, aby povolil soubory cookie třetích stran.</span><span class="sxs-lookup"><span data-stu-id="a1e97-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="a1e97-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a1e97-112">Microsoft Edge</span></span>

1. <span data-ttu-id="a1e97-113">Spusťte prohlížeč Edge.</span><span class="sxs-lookup"><span data-stu-id="a1e97-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="a1e97-114">V pravém horním rohu vyberte **tři tečky** (…). Potom vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="a1e97-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="a1e97-115">V části **Soubory cookie a oprávnění stránek** vyberte **Cookies a data stránek**.</span><span class="sxs-lookup"><span data-stu-id="a1e97-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="a1e97-116">Vypněte **Blokovat soubory cookie třetích stran**.</span><span class="sxs-lookup"><span data-stu-id="a1e97-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="a1e97-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="a1e97-117">Google Chrome</span></span>

1. <span data-ttu-id="a1e97-118">Spusťte prohlížeč Chrome.</span><span class="sxs-lookup"><span data-stu-id="a1e97-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="a1e97-119">V pravém horním rohu vyberte tři svislé tečky a potom **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="a1e97-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="a1e97-120">V části **Ochrana osobních údajů a zabezpečení** vyberte **Cookies a další data stránek**.</span><span class="sxs-lookup"><span data-stu-id="a1e97-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="a1e97-121">Vyberte **Povolit všechny soubory cookie**.</span><span class="sxs-lookup"><span data-stu-id="a1e97-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1e97-122">Pokud zablokujete soubory cookie třetích stran, budou blokovány všechny soubory cookie a data webů z jiných webů, i když je web povolen ve vašem seznamu výjimek.</span><span class="sxs-lookup"><span data-stu-id="a1e97-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="a1e97-123">Koncový bod PEX</span><span class="sxs-lookup"><span data-stu-id="a1e97-123">PEX Endpoint</span></span>

<span data-ttu-id="a1e97-124">Project Operations vyžaduje, aby parametr projektu odkazoval na PEX koncový bod.</span><span class="sxs-lookup"><span data-stu-id="a1e97-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="a1e97-125">Tento koncový bod je vyžadován pro komunikaci se službou používanou k vykreslování strukturovaného rozpisu prací.</span><span class="sxs-lookup"><span data-stu-id="a1e97-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="a1e97-126">Pokud parametr není povolen, zobrazí se chyba „Parametr projektu není platný“.</span><span class="sxs-lookup"><span data-stu-id="a1e97-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="a1e97-127">Zástupné řešení</span><span class="sxs-lookup"><span data-stu-id="a1e97-127">Workaround</span></span>
 ![Pole PEX koncového bodu v parametru projektu](media/projectparameter.png)

1. <span data-ttu-id="a1e97-129">Přidejte pole **Koncový bod PEX** na stránku **Parametry projektu**.</span><span class="sxs-lookup"><span data-stu-id="a1e97-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="a1e97-130">Aktualizujte pole následující hodnotou: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="a1e97-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="a1e97-131">Odeberte pole ze stránky **Parametry projektu**.</span><span class="sxs-lookup"><span data-stu-id="a1e97-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="a1e97-132">Oprávnění pro Projekt pro web</span><span class="sxs-lookup"><span data-stu-id="a1e97-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="a1e97-133">Project Operations spoléhá na externí plánovací službu.</span><span class="sxs-lookup"><span data-stu-id="a1e97-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="a1e97-134">Služba vyžaduje, aby měl uživatel několik rolí přiřazených ke čtení a zápisu do entit souvisejících se strukturou rozpisu práce.</span><span class="sxs-lookup"><span data-stu-id="a1e97-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="a1e97-135">Mezi tyto entity patří projektové úkoly, přiřazení prostředků a závislosti úkolů.</span><span class="sxs-lookup"><span data-stu-id="a1e97-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="a1e97-136">Pokud uživatel nemůže vykreslit strukturu rozpisu práce, když přejde na kartu **Úkoly**, je to pravděpodobně proto, že projekt pro Project Operations nebyl povolen.</span><span class="sxs-lookup"><span data-stu-id="a1e97-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="a1e97-137">Uživatel může obdržet buď chybu role zabezpečení, nebo chybu související s odepřením přístupu.</span><span class="sxs-lookup"><span data-stu-id="a1e97-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="a1e97-138">Zástupné řešení</span><span class="sxs-lookup"><span data-stu-id="a1e97-138">Workaround</span></span>

1. <span data-ttu-id="a1e97-139">Přejděte na **Nastavení > Zabezpečení > >Uživatelé aplikace**.</span><span class="sxs-lookup"><span data-stu-id="a1e97-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Čtečka aplikace](media/applicationuser.jpg)
   
2. <span data-ttu-id="a1e97-141">Dvojitým kliknutím na záznam uživatele aplikace ověřte následující:</span><span class="sxs-lookup"><span data-stu-id="a1e97-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="a1e97-142">Uživatel má přístup k projektu.</span><span class="sxs-lookup"><span data-stu-id="a1e97-142">The user has access to the project.</span></span> <span data-ttu-id="a1e97-143">Toto ověření se obvykle provádí zajištěním, že uživatel má roli zabezpečení **Projektový manažer**.</span><span class="sxs-lookup"><span data-stu-id="a1e97-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="a1e97-144">Uživatel aplikace Microsoft Project existuje a je správně nakonfigurován.</span><span class="sxs-lookup"><span data-stu-id="a1e97-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="a1e97-145">Pokud tento uživatel neexistuje, můžete vytvořit nový záznam uživatele.</span><span class="sxs-lookup"><span data-stu-id="a1e97-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="a1e97-146">Vyberte možnost **Noví uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="a1e97-146">Select **New Users**.</span></span> <span data-ttu-id="a1e97-147">Změňte formulář zadání na **Uživatel aplikace** a poté přidejte **ID aplikace**.</span><span class="sxs-lookup"><span data-stu-id="a1e97-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Uživatelské údaje aplikace](media/applicationuserdetails.jpg)

4. <span data-ttu-id="a1e97-149">Ověřte, že uživateli byla přiřazena správná licence a že je služba povolena v podrobnostech servisních plánů licence.</span><span class="sxs-lookup"><span data-stu-id="a1e97-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="a1e97-150">Ověřte, že uživatel může otevřít project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a1e97-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="a1e97-151">Prostřednictvím parametrů projektu ověřte, že systém ukazuje na správný koncový bod projektu.</span><span class="sxs-lookup"><span data-stu-id="a1e97-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="a1e97-152">Ověřte, že je vytvořen uživatel aplikace projektu.</span><span class="sxs-lookup"><span data-stu-id="a1e97-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="a1e97-153">Aplikujte na uživatele následující role zabezpečení:</span><span class="sxs-lookup"><span data-stu-id="a1e97-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="a1e97-154">Uživatel služby Dataverse</span><span class="sxs-lookup"><span data-stu-id="a1e97-154">Dataverse User</span></span>
  - <span data-ttu-id="a1e97-155">Systém Project Operations</span><span class="sxs-lookup"><span data-stu-id="a1e97-155">Project Operations System</span></span>
  - <span data-ttu-id="a1e97-156">Systém projektu</span><span class="sxs-lookup"><span data-stu-id="a1e97-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="a1e97-157">Chyba při aktualizaci strukturovaného rozpisu práce</span><span class="sxs-lookup"><span data-stu-id="a1e97-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="a1e97-158">Když se provede jedna nebo více aktualizací struktury rozpisu práce, změny nakonec selžou a neuloží se.</span><span class="sxs-lookup"><span data-stu-id="a1e97-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="a1e97-159">V mřížce plánu se vyskytla chyba s informací, že „poslední provedenou změnu nelze uložit“.</span><span class="sxs-lookup"><span data-stu-id="a1e97-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="a1e97-160">Zástupné řešení</span><span class="sxs-lookup"><span data-stu-id="a1e97-160">Workaround</span></span>

1. <span data-ttu-id="a1e97-161">Ověřte, že uživateli byla přiřazena správná licence a že je služba povolena v podrobnostech servisních plánů licence.</span><span class="sxs-lookup"><span data-stu-id="a1e97-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="a1e97-162">Ověřte, že uživatel může otevřít project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a1e97-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="a1e97-163">Ověřte, že systém ukazuje na správný koncový bod projektu.</span><span class="sxs-lookup"><span data-stu-id="a1e97-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="a1e97-164">Ověřte, že uživatel aplikace projektu byl vytvořen.</span><span class="sxs-lookup"><span data-stu-id="a1e97-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="a1e97-165">Aplikujte na uživatele následující role zabezpečení:</span><span class="sxs-lookup"><span data-stu-id="a1e97-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="a1e97-166">Uživatel Dataverse nebo základní uživatel</span><span class="sxs-lookup"><span data-stu-id="a1e97-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="a1e97-167">Systém Project Operations</span><span class="sxs-lookup"><span data-stu-id="a1e97-167">Project Operations System</span></span>
  - <span data-ttu-id="a1e97-168">Systém projektu</span><span class="sxs-lookup"><span data-stu-id="a1e97-168">Project System</span></span>
  - <span data-ttu-id="a1e97-169">Systém duálního zápisu Project Operations (Tato role je vyžadována, pokud nasazujete scénář Project Operations, který není založen na zdroji / není skladem.)</span><span class="sxs-lookup"><span data-stu-id="a1e97-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]