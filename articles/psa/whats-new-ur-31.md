---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 31, V3
description: Tento článek uvádí funkce a opravy, které jsou k dispozici v Project Service Automation, vydání Update 31, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8d62b12a5363637e46b29c2e9edf4e1f17da729f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925020"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tento článek uvádí funkce a opravy, které jsou nové nebo se změnily v Project Service Automation V3, vydání Update 31. Tato verze má číslo sestavení V3.10.52.77 a je obvykle k dispozici prostřednictvím automatické aktualizace v květnu 2021.

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







