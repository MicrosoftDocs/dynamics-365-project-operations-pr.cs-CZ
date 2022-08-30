---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 42, V3
description: Tento článek uvádí funkce a opravy, které jsou k dispozici v Microsoft Dynamics 365 Project Service Automation, vydání Update 42, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912707"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 42, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Je kompatibilní s Dynamics 365 9.x. Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tento článek uvádí funkce a opravy, které jsou nové nebo se změnily v Project Service Automation, vydání Update 42, V3. Tato verze má číslo sestavení V3.10.73.61 a je obvykle k dispozici prostřednictvím automatické aktualizace v dubnu 2022.

## <a name="update-release-42"></a>Aktualizace verze 42

### <a name="bug-fixes"></a>Opravy chyb

Byly vyřešeny následující problémy.

**Čas a výdaje**

- Když je časový výkaz odmítnut, uživatel, který jej odmítl, je nesprávně identifikován jako **Systém**.
- Když jsou importovány časové záznamy, hodnota **Kategorie zdroje** chybí.
- Schvalovatelé projektů mohou schvalovat předložené projekty, pokud jejich oprávnění nejsou konkrétně nastavena na **Může schválit**.

**Prodej**

- Když jsou skutečné hodnoty zaprotokolovány u úloh, které nejsou na úrovni kořenu, jsou skutečné náklady nesprávně agregovány.