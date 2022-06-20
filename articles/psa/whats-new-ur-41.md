---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 41, V3
description: Tento článek uvádí funkce a opravy, které jsou k dispozici v Microsoft Dynamics 365 Project Service Automation, vydání Update 41, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930540"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 41, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Je kompatibilní s Dynamics 365 9.x. Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tento článek uvádí funkce a opravy, které jsou nové nebo se změnily v Project Service Automation, vydání Update 41, V3. Tato verze má číslo sestavení V3.10.62.162 a je obecně k dispozici prostřednictvím automatické aktualizace v březnu 2022.

## <a name="update-release-41"></a>Aktualizace verze 41

### <a name="bug-fixes"></a>Opravy chyb

Byly vyřešeny následující problémy.

**Správa projektů**
- Když se pokusíte vytvořit projekt ze šablony, která je založena na projektu vytvořeném z desktopového doplňku, zobrazí se následující chyba: „Ověření pole plánované práce přiřazení zdrojů: Koncové datum každého časového úseku přiřazení zdrojů nesmí být dřívější než jeho počáteční datum".

**Čas a výdaje**
- Když se pokusíte odstranit položku času, zobrazí se následující chybová zpráva: "Z kódu ISV došlo k neočekávané chybě".

**Prodej**
- Když vytvoříte fakturu za milník s pevnou cenou, pole **Popis** a **Externí popis** nejsou vyplněna. 
