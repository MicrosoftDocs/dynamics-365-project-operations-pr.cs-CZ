---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 36, V3
description: Toto téma obsahuje funkce a opravy, které jsou k dispozici ve Microsoft Dynamics 365 Project Service Automation vydání aktualizace 36, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 108c75598dc7dd3dd0cdb9ce68e30423d051a4cf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586658"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Je kompatibilní s Dynamics 365 9.x. Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 36 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.57.152 a je obvykle k dispozici prostřednictvím automatické aktualizace v říjnu 2021.

## <a name="update-release-36"></a>Aktualizace verze 36

### <a name="bug-fixes"></a>Opravy chyb

Byly vyřešeny následující problémy.

**Obecná**
- Název pole **Výchozí šablona pracovní doby** je nesprávně přeložen na stránce **Parametry projektu**.
- Asynchronní moduly plug-in nesprávně zpracovávají výjimky související s **SharedVariableService**.

**Čas a výdaje**
- Pokud chybí řádky deníku nebo uživatel nemá správná oprávnění ke čtení řádků deníku, při zrušení schválení projektu dojde k nesprávné chybě.
- Uživatelé nemohou zrušit schválení, pokud má záznam výdaje nebo času více než jedno přidružené schválení projektu.
- **Absence** a **Dovolená** jsou nesprávně přeloženy do čínštiny při vyhledávání na stránce pro rychlé vytvoření **Časový záznam**.

**Řízení zdrojů**
- Uživatel nemůže hledat zdroje v **Pomocníku plánování**, když je režim zobrazení nastaven na **Den**, **Týden** nebo **Měsíc**.
- Pro obecné zdroje jsou nesprávně povoleny prázdné názvy pozic. 
- Uzavření smlouvy jako ztracené nezruší budoucí rezervace.

**Prodej**
- Když má prostředí velký objem produktů, sníží se výkon v mřížce **Odhad materiálů**.
- Při vytváření projektu ze šablony se měna projektu nenastaví na výchozí pro příslušnou smluvní jednotku projektového manažera.
- Skutečné částky ne vždy odpovídají tomu, co se děje v projektu, nebo se částky stanou zápornými v některých scénářích odvolání.
- Při přidružení projektu vytvořeného ze šablony projektu k řádku smlouvy dojde k chybě.
- Uživatelé mohou odstranit řádek smlouvy s milníky **Připraveno k fakturaci** a **Faktura vytvořena**. To by nemělo být dovoleno.
- Když jsou odhady importovány z projektu, je nesprávně nastaveno účtování detailu řádku nabídky, když je pro řádek nabídky povolena fakturace na základě úkolu.
- Když přidáte milník fakturace s pevnou cenou, mílník se neprojeví v jeho podmřížce, dokud se stránka neobnoví.
- Při vytváření smlouvy projektu s názvem nabídky, který je null, je generována výjimka odkazu null.
- Úkoly ručního režimu, kde je měna projektu odlišná od měny zdroje, mají za následek nesprávné odhady cen.
- Uživatelé nemohou odvolat transakci, která byla úspěšně opravena opravnou fakturou.
- Deaktivované kategorie transakcí se zobrazí v mřížce **Odhady výdajů**.



