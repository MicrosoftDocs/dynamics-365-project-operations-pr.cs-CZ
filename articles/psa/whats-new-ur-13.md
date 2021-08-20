---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 13, V3
description: Tohle téma poskytuje informace o tom, co je nového v aktualizaci verze 13 pro aplikaci Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 3a20cf32e578bc818f3ef6ed916784c32b559c3342162bcb7857f5e9cc520d9c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006675"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation, vydání aktualizace 13, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Dynamics 365 Project Service Automation (PSA). Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 a na stránce řešení nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 13 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.3.18 a je k dispozici v následujícím plánu:

- **Obecná dostupnost (automatická aktualizace):** Listopad 2019
- **Automatická aktualizace:** Prosinec 2019


## <a name="update-release-13"></a>Aktualizace verze 13 

### <a name="bug-fixes"></a>Opravy chyb

- Čas a výdaje

     - Opraveno: Funkce vyhledávání na stránce **Schválení výdajů** nefunguje při vyhledávání podle účelu výdajů.

- Správa zdrojů

     - Opraveno: Čísla odsouhlasení byla aktualizována, aby byla správně odůvodněna.
     - Opraveno: Pojmenované zdroje nelze k úkolům přiřadit pomocí karty **Plán**.

- Správa projektů

     - Opraveno: Nulová referenční výjimka při přiřazování člena týmu, když pro **Typ transakce** chybí informace o nastavení pro **Jednotka** a **Výchozí skupina**.

- Sales

     - Opraveno: Duplicitní záznamy typu transakce vrátí chybu při vytváření záznamů cen rolí.
     - Opraveno: Dodatečná tlačítka pro **Nová příležitost**, **Nabídka**, **Řádek objednávky** a **Přidat produkt** jsou viditelné v příkazech pro Příležitosti, Nabídky, Produkty v objednávkách a podmřížku Řádky na základě projektu.




[!INCLUDE[footer-include](../includes/footer-banner.md)]