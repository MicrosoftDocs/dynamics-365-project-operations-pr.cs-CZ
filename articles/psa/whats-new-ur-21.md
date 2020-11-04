---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 21, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 21, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: e8a15d5f723da528640c62c1892bac0d801c2bee
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073731"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation, vydání aktualizace 21, V3

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 21 pro aplikaci Project Service Automation V3. Tato verze má číslo sestaveníV 3.10.32.50 a je obvykle k dispozici prostřednictvím automatické aktualizace v červnu 2020.

## <a name="update-release-21"></a>Aktualizace verze 21

### <a name="bug-fixes"></a>Opravy chyb

**Čas a výdaje**

Byly vyřešeny následující problémy:

- Při hostování **ovládacího prvku mřížky pro zadání času** v řídicích panelech mřížka nevyužívá celou šířku kontejneru mřížky řídicího panelu.
- Pro konkrétní časová pásma ovládací prvek mřížky **Zadání času** nezobrazuje záznamy.
- Časové záznamy, které jsou po 21:00, se zobrazují ve špatný den.
- Uživatelé nemohou odesílat výdaje, pokud kategorie výdajů **Je vyžadován příjem výdajů** nemá žádnou hodnotu.

**Správa zdrojů**

Byly vyřešeny následující problémy:

- Neaktivní rezervace jsou zobrazeny v zobrazení **Párování**.
- Při plnění obecných prostředků chybělo ověření, aby bylo zajištěno, že existuje platný stav rezervace.

**Správa projektů**

Byly vyřešeny následující problémy:

- Mřížky formuláře **Projekt** (zobrazení **Přiřazení zdroje** , **Úkol** , **Párování** , **Odhady výdajů** ) zůstávají upravitelné, i když projekt není aktivní.
- Duplicitní zákazníky nelze sloučit se zákazníky, kteří jsou spojeni s potvrzenými smlouvami o projektu.
- Když je přidán prostředek, který nemá platný kalendář, systém nevrací uživatelsky přehlednou chybovou zprávu.
- Tlačítko **Přidat úkol** v mřížce úlohy je povoleno, když je projekt propojen s **doplňkem aplikace Microsoft Project**.
- Úsilí nekontrolovatelně roste, když je úkol s kategorií přiřazen ke zdroji s rolí, pro niž je definována nákladová cena.

**Sales**

Byla provedena následující vylepšení:

- **Frekvence faktury** a **začátek fakturace** byly přesunuty na kartu **Plán faktur**.

Byly vyřešeny následující problémy:

- **Celková prodejní cena** je nula (0) pro **Kategorii** , přestože **Role** má celkovou prodejní cenu, která není nula.
- Zákazníci nemohou změnit hodnotu pole **Stav faktury** na **Připraveno k fakturaci** , když jiný přizpůsobený proces aktualizuje další pole.
- Tlačítko **Aktualizovat řádky faktury** může vytvořit více duplikovaných řádků, pokud je opakovaně vybráno.
- Tlačítko **Aktualizace cen** nefunguje v podmřížce **Ceny role** ve formuláři **Rychlé zobrazení**.
- Logika **Řešení seznamu prodejních cen** nesprávně zpracovává časová pásma, což má za následek nesprávný výběr ceníků.
- **Celkové skutečné náklady** na projekt mohou být po schválení jednoho časového záznamu posunuty o zlomkovou hodnotu.
- Logika **Rozlišení cen** neposkytuje uživatelsky přehlednou chybovou zprávu, pokud **Načtená RolePrice** nemá hodnoty v polích **'Primární jednotka'** a **'Cena v primární jednotce'**.
