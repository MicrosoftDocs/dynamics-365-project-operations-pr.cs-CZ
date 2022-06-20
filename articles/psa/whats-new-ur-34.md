---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 34, V3
description: Tento článek uvádí funkce a opravy, které jsou k dispozici v Project Service Automation, vydání Update 34, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e47a5442f285952c165a2d30e337a362a6b065dd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928654"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Je kompatibilní s Dynamics 365 9.x. Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tento článek uvádí funkce a opravy, které jsou nové nebo se změnily v Project Service Automation V3, vydání Update 34. Tato verze má číslo sestavení V3.10.55.38 a je obecně dostupná prostřednictvím vlastní aktualizace v červenci 2021.

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
