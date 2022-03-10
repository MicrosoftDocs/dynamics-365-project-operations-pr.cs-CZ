---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 34, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 34, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 528d4f8d108720cb9c912cea1c0d5f37e3716eec
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323273"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Je kompatibilní s Dynamics 365 9.x. Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 34 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.55.38 a je obecně dostupná prostřednictvím vlastní aktualizace v červenci 2021.

## <a name="update-release-34"></a>Aktualizace verze 34

### <a name="bug-fixes"></a>Opravy chyb
Byly vyřešeny následující problémy.

**Obecná**

- Aktualizace řízené vydavatelem neaktivují nový moderní pracovní postup schvalování.
- Atributy **Stav cíle** a **Typ akce** chybí na hlavní stránce **Schvalovací sada**.

**Čas a výdaje**

- Nelze schválit žádost o odvolání pomocí moderního postupu schválení.
- Kopírování týdenních časových záznamů nefunguje při kopírování záznamů, které nesouvisejí s přihlášeným uživatelem.

**Plánování projektu**

- Při importu z desktopového doplňku aplikace Microsoft Project jsou poškozeny obrysy přiřazení zdrojů.

**Řízení zdrojů**

- Když publikujete projekt z doplňku desktopového klienta Microsoft Project, změní se datum ukončení stávajících požadavků.
- Desetinná přesnost přesahuje dvě desetinná místa v dialogu pro potvrzení rozšířených rezervací.

**Prodej**

- Když do projektové smlouvy přidáte produktovou řadu s existujícím produktem, zobrazí se výjimka **klíč nebyl nalezen ve slovníku**.
- Zájemce nelze kvalifikovat, pokud je typ objednávky mapován ze zájemce na příležitost.
