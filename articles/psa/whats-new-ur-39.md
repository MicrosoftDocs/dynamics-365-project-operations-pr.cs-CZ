---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 39, V3
description: Tento článek uvádí funkce a opravy, které jsou k dispozici v Microsoft Dynamics 365 Project Service Automation, vydání Update 39, V3.
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
ms.openlocfilehash: d5b5938762d98acaead9e26c47bce07e0059faf6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922444"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 39, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Je kompatibilní s Dynamics 365 9.x. Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tento článek uvádí funkce a opravy, které jsou nové nebo se změnily v Project Service Automation, vydání Update 39, V3. Tato verze má číslo sestavení V3.10.60.170 a je obvykle k dispozici prostřednictvím automatické aktualizace v lednu 2022.

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
