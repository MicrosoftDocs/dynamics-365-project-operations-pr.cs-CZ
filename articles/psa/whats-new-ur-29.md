---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 29, V3
description: Tento článek uvádí funkce a opravy, které jsou k dispozici v Project Service Automation, vydání Update 29, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 733bbad53933b2de62222e78e3c5c919543c59e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915361"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tento článek uvádí funkce a opravy, které jsou nové nebo se změnily v Project Service Automation V3, vydání Update 29. Tato verze má číslo sestavení V3.10.47.7 a je obecně dostupná prostřednictvím vlastní aktualizace v únoru 2021.

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
