---
title: Proč nemohu odstranit záznamy z entity Skutečné hodnoty?
description: Toto téma poskytuje informace o důvodech, proč nelze odstranit záznamy z entity Skutečné hodnoty.
author: JPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 36cd241c7c7a2ff6ae018c94d691bc95d1f0c912
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148950"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="0a6c9-103">Proč nemohu odstranit záznamy z entity Skutečné hodnoty?</span><span class="sxs-lookup"><span data-stu-id="0a6c9-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0a6c9-104">Project Service Automation (PSA) neumožňuje odstranit skutečné hodnoty, protože slouží jako zdroj pravdy pro transakce, které mají finanční dopad na následné systémy, jako je například hlavní kniha.</span><span class="sxs-lookup"><span data-stu-id="0a6c9-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="0a6c9-105">Pokud by bylo možné skutečné hodnoty odstranit, bylo by možné zpochybnit integritu transakcí finančních výkazů.</span><span class="sxs-lookup"><span data-stu-id="0a6c9-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="0a6c9-106">Aby mohli zákazníci vytvořit revizní záznam, měli by k vytvoření zušlechtěných transakcí použít deníky.</span><span class="sxs-lookup"><span data-stu-id="0a6c9-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

