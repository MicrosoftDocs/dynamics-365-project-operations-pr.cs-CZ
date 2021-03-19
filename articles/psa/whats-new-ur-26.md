---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 26, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 135f017533705e165230ac994d217ad7c58bab10
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280390"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation, vydání aktualizace 26, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 26 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.44.59 a je obecně dostupná prostřednictvím vlastní aktualizace v prosinci 2020.

## <a name="update-release-26"></a>Aktualizace verze 26

### <a name="bug-fixes"></a>Opravy chyb

**Čas a výdaje**

Byly vyřešeny následující problémy:

- Uživatelé jsou schopni změnit úkol u časového záznamu, který byl schválen / odeslán.
- Chyba „Odkaz na objekt není nastaven“ při ukládání časového záznamu.
- Import časového záznamu z přiřazení prostředků vytváří časové záznamy s nesprávnými hodnotami DateTime.
- Když jsou nainstalovány aplikace Project Service Automation i Field Service, tlačítko **Nový** se zobrazuje dvakrát na panelu příkazů pro časové údaje v aplikaci Field Service.
- Aktualizace buněk **Povolit jednotku** a **Skupina jednotek** nyní funguje v mřížce **Odhady výdajů**.
- Formulář **Aktualizovat úpravu časového údaje** obsahuje **Časovou osu**.
- Schválení času pro neprojektové časové údaje blokuje systém při hledání role schvalovatele projektu.

**Správa zdrojů**

Byly vyřešeny následující problémy:

- Přidáno ověření v modulu plug-in **PostProjectCreate**, který před vytvořením zkontroluje primární požadavek.
- Rychlé vytvoření formuláře **Člen projektového týmu** vyvolá výjimku s nulovým odkazem, pokud jsou pole z formuláře odstraněna.
- Generování požadavků na 12 hodin po dobu 1 roku nefunguje.
- Vylepšená chybová zpráva výjimky s bulovým odkazem během vytváření požadavku na zdroj.

**Správa projektů**

Byly vyřešeny následující problémy:

- Vylepšené ověřování pro řešení výjimky s nulovým odkazem generované v modulu plug-in **PreProjectUpdate**.
- Projekty publikované doplňkem Microsoft Project pro stolní počítače odstraňují nepřiřazená přiřazení.
- Přidáno nové ověření, když je odkaz na projekt úkolu neplatný kvůli výjimce nulového odkazu v modulu plug-in **PreValidateProjectTaskUpdate**.
- Mřížka členů týmu nezobrazuje odlišná přiřazení v záznamu člena týmu.
- Přidáno nové ověření a chybové zprávy kvůli výjimce nulové reference v modulu plug-in **PreProjectTaskDelete**.

**Sales**

Byly vyřešeny následující problémy:

- Při výběru řádku založeného na projektu v nabídce nebo smlouvě by tlačítko **Návrh** mělo být viditelné pouze při výběru řádku založeného na projektu spojené s existujícím produktem.
- Rozdělit oprávnění **Create_Product** z oprávnění **Create_ProjectContract**.
- Odstranění řádku faktury způsobí selhání nulové reference v **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]