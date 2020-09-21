---
title: Co je nového v aktualizaci verze 15 pro aplikaci Project Service Automation V3
description: Tohle téma poskytuje informace o tom, co je nového v aktualizaci verze 15 pro aplikaci Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750332"
---
# <a name="project-service-automation-v3-update-release-15"></a>Project Service Automation V3, aktualizace verze 15

S potěšením oznamujeme nejnovější aktualizaci aplikace Dynamics 365 Project Service Automation (PSA). Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 a na stránce řešení nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 15 pro aplikaci PSA V3. Tato verze má číslo sestavení V3.10.5.28 a je obvykle k dispozici prostřednictvím automatické aktualizace v lednu 2020.

## <a name="update-release-15"></a>Aktualizace verze 15 

### <a name="enhancements"></a>Vylepšení

- Správa projektů

### <a name="bug-fixes"></a>Opravy chyb

- Čas a výdaje

  - Opraveno: Přidáno zpracování chyb při načítání v zobrazení odsouhlasení.
  - Opraveno: Centrum projektových zdrojů: Přejmenováno **Množství** pro omezení nejednoznačnosti.
  - Opraveno: Upraveno zobrazení **Zkopírovat sloupce časového záznamu**, aby zahrnovalo typ.
  - Opraveno: Úprava doby trvání časového záznamu v zobrazení mřížky pomocí desetinných čísel způsobila u některých čísel neznámou chybu.

- Správa projektů

  - Opraveno: Rozevírací nabídka pro **Použít v zobrazení sledování** se nyní rozevírá podle šířky možností.
  - Opraveno: Při správě projektů v časovém pásmu +13 mohou výpočty úkolů zobrazovat nepřesné výsledky.
  - Opraveno: **Čas ukončení člena týmu** byl opraven při použití 24hodinového kalendáře.
  - Opraveno: Znovu aktivován **BPF** v hlavním formuláři **msdyn_project**.
  - Opraveno: Výpočet přiřazení již neignoruje jeden den.
  - Opraveno: Do formuláře projektu byl přidán nový oznamovací pruh, když se časové pásmo liší mezi uživatelem a projektem.

- Sales

  - Opraveno: Vyhledávání kategorie odhadu nákladů lze použít k filtrování duplikátů.
  - Opraveno: Kód v **PluginDomain.ExecuteIn tryCatchBlock(..)** již neskrývá původ výjimky.
  - Opraveno: Již se nezobrazí chybová zpráva ve **Vyhledávání projektu** ve formuláři **Řádek nabídky**, pokud existuje více než 1000 projektů.
  - Opraveno: Mřížka **Odhady** pro odhady práce a nákladů nyní zobrazuje správný symbol měny.
  - Opraveno: Poté, co organizace aktualizuje PSA z aktualizace verze 14 na verzi 15, karta **Plán** se již na formuláři **Projekt** nezobrazuje jako prázdná.
