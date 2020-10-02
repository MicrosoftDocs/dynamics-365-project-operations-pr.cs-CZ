---
title: Konfigurace automatického vytváření faktur
description: Toto téma poskytuje informace o tom, jak nakonfigurovat systém pro automatické generování faktur.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898118"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="64eb4-103">Konfigurace automatického vytváření faktur</span><span class="sxs-lookup"><span data-stu-id="64eb4-103">Configure automated invoice creation</span></span>

<span data-ttu-id="64eb4-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="64eb4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="64eb4-105">Chcete-li nakonfigurovat automatické spuštění faktury v Project Operations, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="64eb4-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="64eb4-106">Přejděte na **Nastavení** \> **Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="64eb4-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="64eb4-107">Vytvořte dávkovou úlohu a pojmenujte ji **Vytvořit faktury v Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="64eb4-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="64eb4-108">Název dávkové úlohy musí obsahovat termín „Vytvořit faktury”.</span><span class="sxs-lookup"><span data-stu-id="64eb4-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="64eb4-109">V poli **Typ úlohy** vyberte **Žádný**.</span><span class="sxs-lookup"><span data-stu-id="64eb4-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="64eb4-110">Ve výchozím nastavení jsou možnosti **Frekvence denně** a **Je aktivní** nastaveny na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="64eb4-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="64eb4-111">Vyberte **Spustit pracovní postup**.</span><span class="sxs-lookup"><span data-stu-id="64eb4-111">Select **Run Workflow**.</span></span> <span data-ttu-id="64eb4-112">V dialogovém okně **Vyhledat záznam** se zobrazí tři pracovní postupy:</span><span class="sxs-lookup"><span data-stu-id="64eb4-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="64eb4-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="64eb4-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="64eb4-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="64eb4-114">ProcessRunner</span></span>
    - <span data-ttu-id="64eb4-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="64eb4-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="64eb4-116">Vyberte **ProcessRunCaller** a potom vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="64eb4-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="64eb4-117">V dalším dialogovém okně vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="64eb4-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="64eb4-118">Po pracovním postupu **Spánek** následuje pracovní postup **Zpracovat**.</span><span class="sxs-lookup"><span data-stu-id="64eb4-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="64eb4-119">Pracovní postup **ProcessRunner** můžete také vybrat v kroku 5.</span><span class="sxs-lookup"><span data-stu-id="64eb4-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="64eb4-120">Když potom vyberete **OK**, bude pracovní postup **Zpracovat** následován pracovním postupem **Spánek**.</span><span class="sxs-lookup"><span data-stu-id="64eb4-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="64eb4-121">Pracovní postupy **ProcessRunCaller** a **ProcessRunner** vytvářejí faktury.</span><span class="sxs-lookup"><span data-stu-id="64eb4-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="64eb4-122">**ProcessRunCaller** volá **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="64eb4-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="64eb4-123">**ProcessRunner** je pracovní postup, který skutečně vytváří faktury.</span><span class="sxs-lookup"><span data-stu-id="64eb4-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="64eb4-124">Prochází všemi řádky smluv, pro které musí být vytvořeny faktury, a vytváří faktury pro tyto řádky.</span><span class="sxs-lookup"><span data-stu-id="64eb4-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="64eb4-125">Aby určil řádky smluv, pro které musí být vytvořeny faktury, vyhledává úloha data spuštění faktury pro řádky smluv.</span><span class="sxs-lookup"><span data-stu-id="64eb4-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="64eb4-126">Jestliže řádky smluv, které patří k jedné smlouvě, mají stejné datum spuštění faktury, budou transakce sloučeny do jedné faktury, která má dva řádky faktury.</span><span class="sxs-lookup"><span data-stu-id="64eb4-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="64eb4-127">Pokud neexistují žádné transakce pro vytvoření faktur, úloha přeskočí vytvoření faktury.</span><span class="sxs-lookup"><span data-stu-id="64eb4-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="64eb4-128">Proces **ProcessRunner** po svém dokončení volá proces **ProcessRunCaller**, poskytne čas ukončení a je zavřen.</span><span class="sxs-lookup"><span data-stu-id="64eb4-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="64eb4-129">Proces **ProcessRunCaller** poté spustí časovač, který běží po dobu 24 hodin od zadaného času ukončení.</span><span class="sxs-lookup"><span data-stu-id="64eb4-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="64eb4-130">Po doběhnutí časovače je **ProcessRunCaller** uzavřen.</span><span class="sxs-lookup"><span data-stu-id="64eb4-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="64eb4-131">Úloha dávkového zpracování pro vytváření faktur je opakující se úloha.</span><span class="sxs-lookup"><span data-stu-id="64eb4-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="64eb4-132">Pokud je tento dávkový proces spuštěn vícekrát, vytvoří se více instancí této úlohy a způsobí chyby.</span><span class="sxs-lookup"><span data-stu-id="64eb4-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="64eb4-133">Proto byste tento dávkový proces měli spustit pouze jednou a restartovat ho, pouze pokud přestane běžet.</span><span class="sxs-lookup"><span data-stu-id="64eb4-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="64eb4-134">Dávková fakturace běží pouze pro řádky projektové smlouvy, které jsou konfigurovány podle plánů faktur.</span><span class="sxs-lookup"><span data-stu-id="64eb4-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="64eb4-135">Řáeke smlouvy s metodou fakturace s pevnou cenou musí mít nakonfigurované milníky.</span><span class="sxs-lookup"><span data-stu-id="64eb4-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="64eb4-136">Řádek smlouvy o projektu s metodou fakturace času a materiálu bude vyžadovat sestavení časového rozvrhu faktur.</span><span class="sxs-lookup"><span data-stu-id="64eb4-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="64eb4-137">Totéž platí pro řádek smlouvy založené na projektu.</span><span class="sxs-lookup"><span data-stu-id="64eb4-137">The same applies to a project-based contract line.</span></span>     
