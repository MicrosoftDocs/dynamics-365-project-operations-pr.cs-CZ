---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 45, V3
description: Tento článek uvádí funkce a opravy, které jsou k dispozici v Microsoft Dynamics 365 Project Service Automation, vydání Update 45, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169150"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 45, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Je kompatibilní s Dynamics 365 9.x. Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tento článek uvádí funkce a opravy, které jsou nové nebo se změnily v Project Service Automation, vydání Update 45, V3. Tato verze má číslo sestavení V3.10.76.168 a je obecně dostupná prostřednictvím vlastní aktualizace v červenci 2022.

## <a name="update-release-45"></a>Aktualizace verze 45

### <a name="bug-fixes"></a>Opravy chyb

Byly vyřešeny následující problémy.

**Prodej**

- Uživatelé nemohou úspěšně vytvářet faktury poté, co se pokusili vytvořit fakturu bez jakýchkoli nevyfakturovaných prodejů, pokud si také prohlížejí stejnou instanci stránky a neaktualizují ji.

**Čas a výdaje**

- Když je povoleno Moderní schválení a je schváleno odvolané schválení projektu, je fáze záznamu nesprávně aktualizována na **Žádost o odvolání byla schválena**.
- Když je povoleno Moderní schválení a Cloudové toky jsou neaktivní, proces schvalování není úspěšný a odesílající nebo schvalující uživatelé nejsou informováni.
