---
title: Porozumění stavu projektu
description: Tento téma poskytuje informace o stavu přiřazeném projektům v Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ad8c012b93bc65595dca33df1770562916c557e0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993408"
---
# <a name="understand-project-status"></a><span data-ttu-id="4d925-103">Porozumění stavu projektu</span><span class="sxs-lookup"><span data-stu-id="4d925-103">Understand project status</span></span>

<span data-ttu-id="4d925-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="4d925-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="4d925-105">Sekce **Stav** na stránce **Entita projektu** poskytuje přehled stavu projektu na základě nákladů a úsilí.</span><span class="sxs-lookup"><span data-stu-id="4d925-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="4d925-106">Souhrnná pole stavu</span><span class="sxs-lookup"><span data-stu-id="4d925-106">Status summary fields</span></span>

- <span data-ttu-id="4d925-107">Pole **Celkový stav projektu** je upravitelné pole, které zobrazuje celkový stav projektu.</span><span class="sxs-lookup"><span data-stu-id="4d925-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="4d925-108">Toto pole k označení zvyšujících se rizik používá barevné označení, například zelené, žluté a červené.</span><span class="sxs-lookup"><span data-stu-id="4d925-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="4d925-109">Pole **Komentáře** umožňuje projektovému manažerovi zadat konkrétní komentáře o stavu.</span><span class="sxs-lookup"><span data-stu-id="4d925-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="4d925-110">Pole **Datum aktualizace stavu** nelze upravovat.</span><span class="sxs-lookup"><span data-stu-id="4d925-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="4d925-111">Hodnota v tomto poli je časové razítko, které označuje, kdy byl stav naposledy aktualizován.</span><span class="sxs-lookup"><span data-stu-id="4d925-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="4d925-112">Pole **Plnění plánu** a **Plnění nákladů** jsou nastavena z mřížky sledování.</span><span class="sxs-lookup"><span data-stu-id="4d925-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="4d925-113">Pokud jsou odchylky plánu a nákladů kořenového uzlu v zobrazení **Sledování úsilí** kladné, tato pole jsou aktualizována na **V předstihu**.</span><span class="sxs-lookup"><span data-stu-id="4d925-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="4d925-114">Pokud jsou odchylky plánu a nákladů kořenového uzlu záporné, tato pole se nastaví na **Ve skluzu**.</span><span class="sxs-lookup"><span data-stu-id="4d925-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]