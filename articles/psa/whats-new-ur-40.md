---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 40, V3
description: Tento článek uvádí funkce a opravy, které jsou k dispozici v Microsoft Dynamics 365 Project Service Automation, vydání Update 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912784"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Je kompatibilní s Dynamics 365 9.x. Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tento článek uvádí funkce a opravy, které jsou nové nebo se změnily v Project Service Automation, vydání Update 40, V3. Tato verze má číslo sestavení V3.10.61.61 a je obecně dostupná prostřednictvím vlastní aktualizace v únoru 2022.

## <a name="update-release-40"></a>Aktualizace verze 40

### <a name="features"></a>Funkce
Fáze 1 upgradu z Project Service Automation na Project Operations - Lite bude uvolněna v únoru 2022 pro všechny zákazníky. Chcete-li zjistit, zda máte nárok, viz [Upgrade z Project Service Automation na Project Operations](upgrade-project-operations-non-stocked.md). Pokud se aplikace neobjeví ve vaší instanci v centru pro správu Power Platform, kontaktujte podporu a požádejte o povolení nasazení testovací verze pro vaše prostředí. Vaše žádost musí obsahovat seznam ID prostředí, kde je třeba nasazení testovací verze povolit.

### <a name="bug-fixes"></a>Opravy chyb

Byly vyřešeny následující problémy.

**Čas a výdaje**
- Při odmítnutí nebo zrušení záznamu času chybí záznam poznámky. 

**Prodej**

- Když aktualizujete odhady nákladů nebo prodeje pomocí předem připravených zásuvných modulů, máte nesprávné oprávnění odesílat datové části JSON, které nejsou platné mimo uživatelské rozhraní.
- Když aktualizujete řádky nabídek pomocí rychlého zobrazení, můžete aktivovat nabídky.