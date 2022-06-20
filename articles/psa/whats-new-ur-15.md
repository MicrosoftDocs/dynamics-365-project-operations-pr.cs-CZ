---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 15, V3
description: Tento článek obsahuje informace o novinkách a změnách ve vydání Update 15, V3 aplikace Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: b87cae2cd8913457c2931d1661a57509d1398d29
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915636"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation, vydání aktualizace 15, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Dynamics 365 Project Service Automation (PSA). Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 a na stránce řešení nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tento článek uvádí funkce a opravy, které jsou nové nebo se změnily v PSA V3, vydání Update 15. Tato verze má číslo sestavení V3.10.5.28 a je obvykle k dispozici prostřednictvím automatické aktualizace v lednu 2020.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
