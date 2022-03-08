---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 31, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 31, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 2e5fce003c25f9c5911e5a01fb4ec3e19c06c078e00b054472699a522b9cd070
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002143"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 31 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.52.77 a je obvykle k dispozici prostřednictvím automatické aktualizace v květnu 2021.

## <a name="update-release-31"></a>Aktualizace verze 31

### <a name="bug-fixes"></a>Opravy chyb

**Čas a výdaje**

Byly vyřešeny následující problémy:

- Ovládací tlačítka pro zadávání času na stránce **Rezervovatelný zdroj** byla matoucí.
- Byla vygenerována výjimka nulové reference v **Project.SetTrackingFields** při schvalování zadání času.

**Správa zdrojů**

Byly vyřešeny následující problémy:

- **Vytvořit člena týmu** správně nezobrazuje nastavení metadat nastavení rezervace pro **Výchozí stav potvrzení rezervace**.
- Při upgradu z PSA 1.X na 3.X proces upgradu selže při **UpgradeResourceRequirements**.


**Prodej**

Byly vyřešeny následující problémy:

- Skutečný příjem převádí částky na měnu projektu v mřížce sledování.
- Výchozí měna je nejasná při vytváření řádků deníku, řádků nabídek a řádků kontraktů ve scénářích, kde se základní měna organizace liší od měny projektu.
- Dotaz **Ověření deníku čekajících na opravu** nefiltruje podle projektu.
- Zbývající tržby se u projektu počítají nesprávně.
- Nabídky založené na kontaktu selžou, když jsou vytvořeny bez ceníku.
- Po výběru **Potvrdit fakturu** se nezobrazí žádné kolečko zpracování.
- Po výběru **Vytvořit fakturu** se nezobrazí žádné kolečko zpracování.
- Uzavření nabídky jako ztracené nezruší rezervace.







