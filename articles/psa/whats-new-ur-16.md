---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 16, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 16, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: f277d23e3fb0517f072e51f6f80f855479ab8189
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073739"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation, vydání aktualizace 16, V3

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.  Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace preferovaného řešení](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).
Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 16 pro aplikaci PSA V3. Tato verze má číslo sestavení V3.10.6.34 a je obvykle k dispozici prostřednictvím automatické aktualizace v lednu 2020.


## <a name="update-release-16"></a>Aktualizace verze 16

### <a name="bug-fixes"></a>Opravy chyb

-   Čas a výdaje

    -   Oprava: Uživatelé, kteří se pokusí odeslat odstraněné údaje o času a výdajích ke schválení, nyní obdrží příslušné chybové zprávy.

-   Správa projektů

    -   Oprava: Jednotky zdroje definované pro členy týmu v šablonách jsou respektovány se šablonami, které jsou použity na nový projekt.

    -   Oprava: Vylepšené zpracování opětovného přiřazení vlastnictví záznamu.

    -   Oprava: Projekty, které se právě kopírují, nebudou zkopírovány, dokud nebudou dokončeny všechny operace kopírování.

-   Správa zdrojů

    -   Oprava: Rozšířené rezervace nyní zpracovávají krátké doby správně a již nevytvářejí nulové hodiny pro rozšířené rezervace.

    -   Oprava: Zobrazení odsouhlasení se nyní vykreslí, když je časové pásmo projektu +5:30 GMT a čas uživatele je jiný.

-   Sales

    -   Oprava: Když je odstraněn projekt mapovaný na řádek smlouvy a je namapován nový projekt, skutečné záznamy o novém projektu nebyly znovu vyhodnoceny na základě fakturačních a cenových pravidel definovaných na řádku smlouvy. To bylo v této verzi opraveno. Ceny a skutečné záznamy o nově mapovaném projektu budou stornovány a znovu vytvořeny správně na základě cenových a fakturačních pravidel řádku smlouvy. Skutečné záznamy nemapovaného projektu se v důsledku toho také přehodnotí a znovu vytvoří.

    -   Oprava: K poli **Částka** řádku odhadu bylo přidáno další ověření, aby se zajistilo, že nezůstanou zachovány hodnoty null.

    -   Oprava: Po aktualizaci skutečných hodnot projektu bylo do hlavního formuláře projektu přidáno tlačítko Obnovit, aby uživatelé mohli znovu synchronizovat skutečné hodnoty.

    -   Oprava: Když uživatelé upgradují z 2.X na 3.X, budou povoleny projekty s hodnotou NULL pro název projektu.

