---
title: Proč nemohu odstranit záznamy z entity Skutečné hodnoty?
description: Toto téma poskytuje informace o důvodech, proč nelze odstranit záznamy z entity Skutečné hodnoty.
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073906"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="cf0ec-103">Proč nemohu odstranit záznamy z entity Skutečné hodnoty?</span><span class="sxs-lookup"><span data-stu-id="cf0ec-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cf0ec-104">Project Service Automation (PSA) neumožňuje odstranit skutečné hodnoty, protože slouží jako zdroj pravdy pro transakce, které mají finanční dopad na následné systémy, jako je například hlavní kniha.</span><span class="sxs-lookup"><span data-stu-id="cf0ec-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="cf0ec-105">Pokud by bylo možné skutečné hodnoty odstranit, bylo by možné zpochybnit integritu transakcí finančních výkazů.</span><span class="sxs-lookup"><span data-stu-id="cf0ec-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="cf0ec-106">Aby mohli zákazníci vytvořit revizní záznam, měli by k vytvoření zušlechtěných transakcí použít deníky.</span><span class="sxs-lookup"><span data-stu-id="cf0ec-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

