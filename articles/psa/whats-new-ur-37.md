---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 37, V3
description: Toto téma obsahuje funkce a opravy, které jsou k dispozici ve Microsoft Dynamics 365 Project Service Automation vydání aktualizace 37, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: e8696d84aaca019c2e12d852e669df71146484b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593466"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Je kompatibilní s Dynamics 365 9.x. Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 37 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.58.120 a je obecně dostupná prostřednictvím automatické aktualizace od listopadu 2021.

## <a name="update-release-37"></a>Aktualizace verze 37

### <a name="bug-fixes"></a>Opravy chyb

Byly vyřešeny následující problémy.

**Čas a výdaje**
- Uživatelé nemohou odstranit časový záznam vymazáním buňky.
- Zobrazení **Moje neúspěšná schválení** obsahuje pouze schválení projektů se stavem **Odesláno**.

**Správa projektů**
- Pokud je název pozice člena týmu projektu prázdný, zobrazí se uživatelům chyba výjimky odkazu null při otevírání projektu v desktopovém doplňku Microsoftu.
- Ve stránce **Projektový úkol** není žádné tlačítko **Uložit**, takže uživatelé nemohou ukládat změny záznamů úkolů.
- Uživatelé nemohou odstranit projekt, který má úkol přidružený k nabídce se stavem **Získáno**.

**Prodej**
- Pole **Měna** na stránce **Projekt** se aktualizuje tak, aby odpovídalo měně použité šablony.
- Náklady se počítají nesprávně u úkolů, které mají více měn.
