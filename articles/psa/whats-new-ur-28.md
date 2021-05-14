---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 28, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 28, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 079679302b2d8dac3074732b2392a7b811ac9711
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280210"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí funkce a opravy, které jsou nové nebo změněné pro Project Service Automation V3, vydání aktualizace 28. Tato verze má číslo sestavení V 3.10.46.32 a je obecně dostupná prostřednictvím ruční aktualizace v lednu 2021.

## <a name="update-release-28"></a>Aktualizace verze 28

### <a name="bug-fixes"></a>Opravy chyb

**Čas a výdaje**

Byly vyřešeny následující problémy:

- Uživatelé mohou použít **Hromadné úpravy** k aktualizaci položek času, které byly schváleny a odeslány.

**Správa projektů**

Byly vyřešeny následující problémy:

- V případech, kdy je identifikátor GUID úlohy interpretován jako číslo, nelze úkoly otevřít pro úpravy pomocí **Upravit úkol** ve pásu nástrojů na stránce **Strukturovaný rozpis prací**.

**Sales**

Byly vyřešeny následující problémy:

- Výjimka nulové reference je generována, když je vyvolán modul plug-in **GetEstimatesForProject**.
- **Označit jako připraveno k fakturaci** na mřížce milníku aktualizuje atributy pouze částečně, s výjimkou atributu **Stav faktury**, který je aktualizován.



[!INCLUDE[footer-include](../includes/footer-banner.md)]