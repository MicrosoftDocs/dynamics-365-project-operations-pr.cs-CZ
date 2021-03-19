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
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286060"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="4895b-103">Proč nemohu odstranit záznamy z entity Skutečné hodnoty?</span><span class="sxs-lookup"><span data-stu-id="4895b-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4895b-104">Project Service Automation (PSA) neumožňuje odstranit skutečné hodnoty, protože slouží jako zdroj pravdy pro transakce, které mají finanční dopad na následné systémy, jako je například hlavní kniha.</span><span class="sxs-lookup"><span data-stu-id="4895b-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="4895b-105">Pokud by bylo možné skutečné hodnoty odstranit, bylo by možné zpochybnit integritu transakcí finančních výkazů.</span><span class="sxs-lookup"><span data-stu-id="4895b-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="4895b-106">Aby mohli zákazníci vytvořit revizní záznam, měli by k vytvoření zušlechtěných transakcí použít deníky.</span><span class="sxs-lookup"><span data-stu-id="4895b-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]