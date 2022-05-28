---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 25, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 25, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 2d24403b1bf6a06cc138de3f0158f675f6d3b6ec
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581506"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 25, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí funkce a opravy, které jsou nové nebo změněné pro Project Service Automation V3, vydání aktualizace 25. Tato verze má číslo sestavení V 3.10.43.76 a je obecně dostupná prostřednictvím ruční aktualizace v říjnu 2020.

## <a name="update-release-25"></a>Aktualizace verze 25

### <a name="bug-fixes"></a>Opravy chyb

**Čas a výdaje**

Následující problém byl opraven:

- Graf časových záznamů zobrazující dodatečná data na základě příliš velkého načteného intervalu.

**Správa zdrojů**

Následující problém byl opraven:

- Přidán kód Package Deployer pro přeskočení importu opravy Universal Resource Scheduling, pokud již existuje vyšší verze opravy.

**Správa projektů**

Byly vyřešeny následující problémy:

- Opravené nesrovnalosti zaokrouhlování a směnného kurzu vedoucí k nesprávným plánovaným nákladům v mřížce sledování projektu.
- Podpora zobrazení dvou nebo více reakčních mřížek ve formuláři **Projekt**.
- Poskytnuto ověření, které řeší možnost přiřadzení úkolu po datu ukončení kalendáře, což má za následek neúspěšné přiřazení prostředků.
- Vylepšené zpracování chyb pro řešení výjimky odkazu s hodnotou null generované z následujících:

    - Modul plugin **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate**, když je projektový úkol vytvořen bez přidruženého projektu
    - Modul plugin **PreProjectTeamMemberCreate**
    - Modul plugin **PostProjectTeamMemberDelete**
    - Modul plugin **PreValidateProjectTaskDelete**

**Sales**

Byly vyřešeny následující problémy:

- Vylepšené zpracování chyb při řešení výjimek odkazu s hodnotou null generovaných z **Kopírování projektu: správa odhadů HelperResource**.
- **Nepřipraveno k fakturaci** v **Nedokončená fakturace času a materiálu** nevymaže stav fakturace.
- Opraveno nesprávně označená tlačítka **Ceny** na kartách **Cena role** a **Položky katalogu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
