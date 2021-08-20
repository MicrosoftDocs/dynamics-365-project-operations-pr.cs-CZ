---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 27, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 27, V3.
author: ruhercul
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
ms.openlocfilehash: ee7bbe888a982e3554ba524c67442437c9be9183a5ee0940ccc3261b4a4992e7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985043"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 27, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 27 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.45.98 a je obvykle k dispozici prostřednictvím automatické aktualizace v lednu 2021.

## <a name="update-release-27"></a>Aktualizace verze 27

### <a name="bug-fixes"></a>Opravy chyb

**Obecné**

Byly vyřešeny následující problémy:

- Protokoly generované moduly plug-in v Project Service Automation nebyly nastaveny na automatické mazání.
- Automatický upgrade se nezdaří, protože řešení Project Service Automation obsahuje starší nulovou hodnotu NavBarArea a název.

**Čas a výdaje**

Byly vyřešeny následující problémy:

- Mřížka **Zadání času** zobrazuje nesprávná data pro chování data **Nezávislé na časové zóně**.
- Mřížka **Zadání času** vytvoří nesprávný čas pro chování data **Nezávislé na časové zóně**.
- Vyhledávání úkolů není omezeno na vybraný projekt na stránce **Upravit zadání času**.
- Schválení času pro neprojektové časové údaje je blokováno, protože systém hledá schvalovatele projektu.
- Správné zadání ve skutečných hodnotách zobrazí nesprávnou chybovou zprávu.
- Když úkol obsahuje hodnotu null pro skutečné náklady a aktualizují se součty projektu, dojde k následující chybě „Daný klíč není ve slovníku přítomen“.
- V konkrétních případech filtry **Seskupit podle** na kartě **Odhad projektu** nezobrazují odhady výdajů.
- Interval **Letní čas** není správný pro časové údaje.

**Správa projektů**

Byly vyřešeny následující problémy:

- Vylepšení ukládání do mezipaměti, které zvyšuje výkon související s načítáním stránky **Projekt**.
- Zastaralé obchodní pravidlo zabraňující dokončení projektových úkolů.
- Kontury doplňku Microsoft Project nedodržují kalendář doplňku, což má za následek nesprávné požadavky na zdroje.
- Vytváření projektů ze šablon nesprávně nastavuje data přiřazení a brání možnosti generovat požadavky na zdroje.
- Uživatelé nemají přístup k možnostem **Kategorie**, **Popis**, **Stav** pomocí klávesnice.
- Skutečné hodnoty prodeje projektu nezahrnují hodnoty prodeje poplatků a materiálů.
- Agregace skutečných prodejů a skutečných nákladů se při různých směnných kurzech děje nesprávně.
- Popis v **Výchozí šablona pracovní doby** je zavádějící.
- Odsazení úlohy neodstraní **Kategorii** v uživatelském rozhraní, dokud se neobnoví.
- Chybějící ověření k zajištění přesunutí projektu nad jeho datum ukončení není povoleno.

**Sales**

Byly vyřešeny následující problémy:

- Na řádku nabídky projektu je vygenerována výjimka nulového odkazu, protože **Import z odhadu projektu** je viditelný, pokud nebyl vybrán projekt.
- Při zavírání nabídky jako **Vyhráno** dojde k následující chybě „Odkaz na objekt není nastaven na instanci objektu“.
- Stav vyrovnání není nastaven během skutečného zrušení při odpojení projektu od řádku smlouvy.
- Když je nainstalováno Dynamics 365 Field Service i Project Service Automation, možnosti **Uzamčení ceny** a **Použít aktuální ceny** se nezobrazují současně na stránce **Faktura**.
- Pro japonský jazyk existuje nekonzistentní překlad s jinými stránkami založenými na kalendáři.
- **Aktivovat** a **Deaktivovat** byly odebrány z entit **Přiřazení ceníků** v Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]