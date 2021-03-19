---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 14, V3
description: Tohle téma poskytuje informace o tom, co je nového v aktualizaci verze 14 pro aplikaci Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: e19c8ffe7d92ab7ec9eb46aff8f944c62b0bb4bc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280975"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation, vydání aktualizace 14, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Dynamics 365 Project Service Automation (PSA). Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 a na stránce řešení nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 14 pro aplikaci PSA V3. Tato verze má číslo sestavení V3.10.4.21 a je k dispozici v následujícím plánu:

- **Obecná dostupnost (automatická aktualizace):** Leden 2020
- **Automatická aktualizace:** Únor 2020

## <a name="update-release-14"></a>Aktualizace verze 14

### <a name="enhancements"></a>Vylepšení

- Sales

     - Vlastní hodnoty pole **Podrobnosti řádku nabídky** jsou zkopírovány do pole **Podrobnosti řádků projektových smluv** při aktualizaci nabídky na **Uzavřeno jako získané**.
     - Potvrzené projekty mohou být ve stavu **Uzavřeno jako ztracené**.

- Správa zdrojů

     - Při rozšiřování rezervace budou se uživatelům zobrazí potvrzovací dialogové okno obsahující shrnutí výsledků rezervace a odkaz Zachovat rezervace.


### <a name="bug-fixes"></a>Opravy chyb

- Čas a výdaje

     - Opraveno: Vylepšeno uživatelské prostředí, když uživatel nevybral žádné položky, které mají být opraveny.

- Správa zdrojů

     - Opraveno: Vícenásobná rezervace zdroje přeteče název rezervovatelného zdroje.

- Sales

     - Opraveno: Celková prodejní cena se nevypočítává, dokud uživatel také nevloží nákladovou cenu pro odhad nákladů na projekt.
     - Opraveno: Uzavření nabídky jako **Získáno** selže, pokud přidružená projektová smlouva není ve stavu **Koncept**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]