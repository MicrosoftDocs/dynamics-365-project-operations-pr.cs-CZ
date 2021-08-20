---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 20, V3
description: Toto téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 20, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 9939e2f354b69dcbc304f4f6e2ac41a00f251fed69f37978059f4053335ee651
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993593"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation, vydání aktualizace 20, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 20 pro aplikaci Project Service Automation V3. Tato verze má číslo sestaveníV 3.10.31.37 a je obvykle k dispozici prostřednictvím automatické aktualizace v červnu 2020.

## <a name="update-release-20"></a>Aktualizace verze 20

### <a name="bug-fixes"></a>Opravy chyb

**Správa projektů**

Byly vyřešeny následující problémy:

- Import členů projektového týmu s metodou alokace, která vyžaduje hodiny, vede k nejasné chybové zprávě, když jsou zadané hodiny nula.
- Uživatelům se zobrazí nesprávná chyba při zadání maximálního počtu znaků do pole **Popis** pro projektovou úlohu.
- Stránka **Stažení doplňku Microsoft Dynamics 365 Project Service Automation** je přesměrována na stránku ke stažení v angličtině, když je jazykové nastavení uživatele nastaveno na japonštinu.
- Pokud nastane chyba serveru, popisek synchronizace na kartě **Plán** formuláře **Projekty** někdy zůstává.
- Při změně úlohy jsou na server odesílány redundantní aktualizace úkolů.

**Sales**

Byly vyřešeny následující problémy:

- Ve formuláři **Smlouva** dojde při dvojím kliknutí na **Vytvořit fakturu** k vytvoření dvou faktur pro jeden záznam skutečných hodnot.
- V aplikaci Internet Explorer 11 nemohou uživatelé vytvářet položky výdajů.
- Stornování nákladů a nefakturovaných prodejních skutečných hodnot není propojené.
- Tlačítko **Aktualizovat skutečné hodnoty** ve formuláři **Projekt** neaktualizuje **Skutečné hodiny úkolu**.
- Modul plug-in **PreValidateProjectTeamMemberCreate** může vytvářet duplicitní obecné rezervovatelné zdroje, když je atribut **msdyn_isgenericresourceprojectscoped** nastaven na **False**.
- Hodnota **Přepočítat** vymaže fakturovatelné náklady položek řádku založených na produktu a podrobnosti řádku smlouvy.
- V konkrétních scénářích zobrazuje modul plug-in **PostEstimateLineUpdate** chybu výjimky nulového odkazu.
- Trvání časové fáze v **Grafu analýzy ziskovosti** neodpovídá době trvání nákladů v podrobnostech pevné cenové nabídky v nabídce.
- Hodnoty jednotek a skupin jednotek nejsou správně nastaveny pro kategorie výdajů ve formulářích **Detaily řádku smlouvy** a **Detaily řádku nabídky**.
- Seznamy **Nákladová cena organizační jednotky** umožňují překrývání účinnosti data.
- Uživatelé nemají dovoleno měnit hodnotu **OrgUnit**, když typ objednávky není založený na práci, protože to povede k chybě výjimky nulového odkazu.
- Když se uživatel pokusí přejít z formuláře **Detaily řádku nabídky** zpět na kartu **Nabídka** formulář se aktualizuje a zobrazí kartu **Souhrn**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]