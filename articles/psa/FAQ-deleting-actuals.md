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
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Proč nemohu odstranit záznamy z entity Skutečné hodnoty?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) neumožňuje odstranit skutečné hodnoty, protože slouží jako zdroj pravdy pro transakce, které mají finanční dopad na následné systémy, jako je například hlavní kniha. Pokud by bylo možné skutečné hodnoty odstranit, bylo by možné zpochybnit integritu transakcí finančních výkazů. Aby mohli zákazníci vytvořit revizní záznam, měli by k vytvoření zušlechtěných transakcí použít deníky.

