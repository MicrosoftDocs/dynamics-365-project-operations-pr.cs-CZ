---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 35, V3
description: Toto téma obsahuje funkce a opravy, které jsou k dispozici ve Microsoft Dynamics 365 Project Service Automation vydání aktualizace 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 53670e2c7f54f8fccf636b2855e190f5f85c6068
ms.sourcegitcommit: 5bb8ca5055deda57e2b1173a2e45c53b15f61d62
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473257"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 35, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Je kompatibilní s Dynamics 365 9.x. Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 35 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.56.110 a je obecně dostupná prostřednictvím vlastní aktualizace v září 2021.

## <a name="update-release-35"></a>Aktualizace verze 35

### <a name="bug-fixes"></a>Opravy chyb

Byly vyřešeny následující problémy.

**Čas a výdaje**

- Schvalovateli projektu se zobrazí chyba oprávnění ke čtení, když schválí položky výdajů s rolí **Schvalovatel projektu**.
- Schvalovateli projektu se zobrazí chyba oprávnění zápisu **msdyn_projectapproval**, když zruší schválený časový záznam pomocí role **Schvalovatel projektu**.
- Když vyberete **Kopírovat týden** v časové položce v modulu aplikace Dynamics 365 pro telefon - Centrum projektových zdrojů dojde k následující chybě: „...\OfficeProductivity_RibbonRules.js.map: chyba HTTP: stavový kód 404, net:: ERR_HTTP_RESPONSE_CODE_FAILURE.“
- Zásada **Zkusit znovu** automaticky schvaluje položky, které byly dříve odmítnuty.
- Dílčí mřížka **Schvalovací sady** zobrazuje nepoužitelné akce pásu karet.
- Ikony chybí pro **Úkol projektu** a **Role zdroje** v entitě **Časový záznam**.
- Když importujete přiřazení zdrojů, importované časové záznamy nemají správnou dobu trvání pro přiřazení, která byla vytvořena pomocí úkolů ručního režimu.
- **Odstranit** na stránce **Rozšířené hledání časových záznamů** chybí.
- **Uložit** na stránce **Informace o zadání času** chybí. Tento problém brání uložení změn při zavření stránky.

**Plánování projektu**

- Mřížky **Přiřazení zdrojů** a **Odsouhlasení zdrojů** neřadí seskupené atributy podle abecedy.
- Úkoly nelze vytvářet, pokud je přizpůsobeno chování podle data **Pouze datum**.

**Řízení zdrojů**

- Pokud jsou nainstalovány Dynamics 365 Field Service a Project Service Automation problémy s překrytím nastanou, když **Zobrazení spojené s požadavkem na zdroje** je spojeno s hlavní stránkou.
- Poklepáním na **Uložit** v dialogovém okně **Rychlé vytvoření člena týmu** zabraňuje vytvoření požadavku na zdroje.

**Prodej**

- Výjimka je vyvolána, pokud odstraníte úkol, který je spojen s nabídkou, která má stav **Vyhrála**.
