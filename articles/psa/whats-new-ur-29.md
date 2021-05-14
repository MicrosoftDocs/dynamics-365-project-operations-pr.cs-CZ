---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 29, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 0e1ff0db42adb8b991b26dca1585bd603b2e2276
ms.sourcegitcommit: f57408d6637f670b920d7ce95f8ace8eb1963093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664635"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 29 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.47.7 a je obecně dostupná prostřednictvím vlastní aktualizace v únoru 2021.

## <a name="update-release-29"></a>Aktualizace verze 29

### <a name="bug-fixes"></a>Opravy chyb

**Čas a výdaje**

Byly vyřešeny následující problémy:

- Uživatelé nemohou zobrazit pracovní dobu zaprotokolovanou v nepracovní dny v mřížce pro zadávání času.
- Schválené položky výdajů lze upravovat v mřížce.

**Správa projektů**

Byly vyřešeny následující problémy:

- Chybějící logika ověření, aby se zajistilo, že hodiny úsilí o přiřazení zdrojů nebudou záporné.
- Vlastní akce, **AssignResourcesForTask** aktualizuje všechna pole namísto pouze změněných polí.
- Při kopírování projektu v prostředí s doplňky nebo pracovními postupy , které jsou registrovány v události **CreateProject**, není atribut **msdyn_bulkgenerationstatus** aktualizován, pokud **CopyWBSToProject** selže.
- Když rozbalíte kalendář projektu, pracovní dny nebudou seřazeny vzestupně, což způsobí selhání některých aktualizací úkolů projektu.
- Změna manažera projektu v existujícím projektu aktivuje výchozí logiku organizační jednotky.

**Prodej**

Byly vyřešeny následující problémy:

- Karta **Plnění smlouvy** na stránce **Smlouva** během instalace bezobslužně selže, pokud nejsou k dispozici žádné řádky smlouvy.