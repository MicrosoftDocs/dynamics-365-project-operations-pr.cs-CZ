---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 18, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 18, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: d6e0bb669513185ca266858ea9b8a89ed6dd4408
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147195"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation, vydání aktualizace 18, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 18 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.8.12 a je obvykle k dispozici prostřednictvím automatické aktualizace v dubnu 2020.

## <a name="update-release-18"></a>Aktualizace verze 18

### <a name="bug-fixes"></a>Opravy chyb

**Čas a výdaje**

- Opraveno: Toky **Odvolat**, **Požádat** a **Zrušit schválení** vyvolávají výjimky s nejasnými chybovými zprávami.
- Opraveno: Když možnost **Zrušit schválení** selže u nákladů, není vyvolána relevantní výjimka.
- Opraveno: Mřížka časového záznamu nesprávně zpracovává nepracovní dny v Austrálii po přepnutí letního času (DST) v říjnu.
- Opraveno: Nesprávná výchozí logika zabraňuje odesílání výdajů.
- Opraveno: Pokud selže schválení časového záznamu, zůstává schválení ve stavu **Čekající**.
- Opraveno: Chyby SQL při hromadném schvalování (zablokování / časový limit).
- Opraveno: Významné problémy s výkonem v uživatelském rozhraní způsobené aktualizací členů týmu při schvalování časových záznamů.

**Správa projektů**

- Opraveno: Oznámení o časovém pásmu bylo přesunuto ze zobrazení **Vyrovnání** do hlavního formuláře **Projekt**.
- Opraveno: Šablona kalendáře není správně nastavena, když se otevře nový formulář projektu.
- Oprava: V prohlížečích založených na Chromiu nemohou uživatelé snadno vybrat předchozí úkoly, které mají být odstraněny.
- Opraveno: Vytvoření nebo kopírování **Projektu z prázdné šablony** načítá nesouvisející úkoly.
- Opraveno: V konkrétních mezních případech má vytvoření nového přiřazení z mřížky úkolu za následek vytvoření duplicitních záznamů.
- Opraveno: V ručním režimu nemohou uživatelé aktualizovat počáteční data úlohy na pozdější než aktuální uložené datum.

**Správa zdrojů**

- Opraveno: Řádek mezisoučtu zobrazení **Vyrovnání** nesprávně vypočítá variantu rezervací po prodloužení rezervace.
- Opraveno: Zobrazení **Vyrovnání** nesprávně zobrazuje přiřazení zdrojů, pokud rezervovatelný zdroj obsahuje kalendář, který neodpovídá kalendáři projektu.

**Sales**

- Opraveno: Při opětovném schválení časových záznamů (**Schválit > Zrušit>** a znovu schválit), se vytvoří duplicitní neúčtovatelná skutečná hodnota.
