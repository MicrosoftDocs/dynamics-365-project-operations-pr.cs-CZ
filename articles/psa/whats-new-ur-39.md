---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 39, V3
description: Toto téma obsahuje funkce a opravy, které jsou k dispozici ve Microsoft Dynamics 365 Project Service Automation vydání aktualizace 39, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: 1d198f9ad9144f5cc2f533fa9603e1f1a181c8b6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588728"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 39, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Je kompatibilní s Dynamics 365 9.x. Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 39 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.60.170 a je obvykle k dispozici prostřednictvím automatické aktualizace v lednu 2022.

## <a name="update-release-39"></a>Aktualizace verze 39

### <a name="bug-fixes"></a>Opravy chyb

Byly vyřešeny následující problémy.

**Všeobecné**

- V mapě webu pro překlad do arabštiny bylo provedeno několik vylepšení.

**Správa projektů**

- Když změníte projektového manažera v projektu na uživatele, který je již členem týmu v projektu, dojde k chybě.

**Prodej**

- Vlastník **Ceníku projektové smlouvy** je nesprávný, když se ceník vytváří automaticky. 
- Při aplikaci ceníku na parametr projektu není dodržena platnost data ceníku.
- Při úpravě dvou samostatných nabídek nemusí mít smluvní jednotka správnou výchozí hodnotu.
