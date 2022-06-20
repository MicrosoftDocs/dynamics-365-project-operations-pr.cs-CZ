---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 14, V3
description: Tento článek obsahuje informace o novinkách a změnách ve vydání Update 14, V3 aplikace Project Service Automation.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e8e5132f970e3ec5742842175c118faf98a7b079
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926538"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation, vydání aktualizace 14, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Dynamics 365 Project Service Automation (PSA). Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 a na stránce řešení nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tento článek uvádí funkce a opravy, které jsou nové nebo se změnily v PSA V3, vydání Update 14. Tato verze má číslo sestavení V3.10.4.21 a je k dispozici v následujícím plánu:

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
