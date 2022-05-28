---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 33, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 063290526c25e7073137fc88408be6a61d2d20ac
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601470"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 33, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Je kompatibilní s Dynamics 365 9.x. Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 33 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.54.98 a je obecně dostupná prostřednictvím vlastní aktualizace v červenci 2021.

## <a name="update-release-33"></a>Aktualizace verze 33

### <a name="bug-fixes"></a>Opravy chyb

**Čas a výdaje**

Byly vyřešeny následující problémy:

- Dvě zamčená pole, **msdyn_description** a **msdyn_externaldescription** jsou upravitelné po odeslání.
- Chybová zpráva se objeví, pokud je vytvořen výdaj, který nesouvisí s projektem.
- Když je vytvořen časový záznam, výchozí role zdroje je neaktivní role.
- Řádky deníku spojené s odvolaným a odstraněným výdajem nebudou odstraněny.
- Ve **Formuláři pro rychlé vytvoření časového záznamu** aktualizujte zobrazení **Seznam úkolů projektu** pro změnu data zobrazeného vy výchozím nastavení na datum zahájení úkolu.
- Když vytvoříte časový záznam z karty **Související** rezervovatelného zdroje, pro přihlášeného uživatele je nesprávně vytvořen časový údaj místo nadřazeného rezervovatelného prostředku.
- Do dialogového okna **Hromadné schválení MDD** jsou přidána nová pole.

**Plánování projektu**

Byly vyřešeny následující problémy:
- Pomalý výkon při vytváření projektu, když jsou šablony pracovních hodin projektu použity s komplexními kalendáři.
- Když je počáteční datum větší než koncové datum, zobrazí se na šabloně projektu kopírování chyba z důvodu rozdílů v časové složce každého pole.

**Řízení zdrojů**

Byly vyřešeny následující problémy:
- V dotazu na využití prostředků se používá nesprávný parametr a XML vede k nesprávným výsledkům filtrů v mřížce **Využití zdrojů**.
- Potvrzení **Rozšířit rezervace** zobrazí nesprávné datum ukončení rezervace.

**Prodej**

Byly vyřešeny následující problémy:
- Pokud je cena kategorie vytvořena s chybějícími hodnotami, objeví se chybová zpráva.
- Objeví se chybová zpráva, pokud je milník řádku smlouvy vytvořen bez řádku objednávky.
