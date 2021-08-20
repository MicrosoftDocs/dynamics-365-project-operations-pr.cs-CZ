---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 32, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 023e51e834060a35d2d7e3469d34297192e38ba11c12a2c4f57424213aba44ba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994853"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 32, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Je kompatibilní s Dynamics 365 9.x. Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 32 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.53.108 a je obecně dostupná prostřednictvím samostatné aktualizace v červnu 2021.

## <a name="update-release-32"></a>Aktualizace verze 32

### <a name="bug-fixes"></a>Opravy chyb

#### <a name="general"></a>Obecná

- Když hlavní upgrade selže, je třeba zablokovat pouze hlavní vstupní body aplikace, aby bylo zajištěno, že sdílené entity jsou stále přístupné.

#### <a name="time-and-expense"></a>Čas a výdaje

Byly vyřešeny následující problémy:

- **TimeEntriesImportFromResourceAssignment** neudržuje počáteční a koncový čas obrysového řezu přiřazení prostředků.
- Když vyberete **Otevřít vstup** na mřížce **Zadání času** mřížce, může vám to bránit ve výběru jiných formulářů.
- Při importu přiřazení k časovým položkám může dotaz na kód klienta vygenerovat dlouhou adresu URL, ve které se dotaz nezdaří.
- V mřížce **Zadání času** poté, co je hodnota odstraněna z buňky, zaměření nezůstane v mřížce.
- Tlačítko **Odmítnout** bylo odstraněno z pohledu **Zpracování schválení** u moderního schvalování.
- Stabilita a výkon hromadného schválení časového vstupu jsou ovlivněny zablokováním a selháním vhodného zpracování přizpůsobení, které souvisí s entitou **Zadání času**.

#### <a name="project-planning"></a>Plánování projektu

- Při aktualizaci projektu, který má v poli **Smluvní jednotka** hodnotu null, se vygeneruje výjimka nulového odkazu.
- **Obnovit součty projektu** nesprávně vypočítá zbývající náklady a zbývající prodeje projektu.
- Výpočty redundantních cen ovlivňují výkon, který souvisí s aktualizacemi kontur přiřazení prostředků.

#### <a name="resource-management"></a>Správa zdrojů

Následující problém byl opraven:

- Když je kapacita kalendáře rezervovatelného zdroje větší než 1, Project Service Automation nesprávně rozpozná kapacitu jako 0 (nula). Proto v zobrazení plánu dojde k nekonečné smyčce.

#### <a name="sales"></a>Prodej

Byly vyřešeny následující problémy:

- Když je vytvořen řádek deníku, který má vlastní typ transakce, dojde k následující výjimce nulového odkazu: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Role a kategorie, které jsou deaktivovány před zkopírováním nabídky, nesmíte do fakturovatelných rolí a kategorií nově zkopírované nabídky.
- Datum dokumentu a datum účetnictví nejsou v souladu s počátečním datem uvedeným v detailu řádku faktury, který je vytvořen přímo v konceptu faktury.
- Výjimky s nulovým odkazem se generují ve scénářích, které souvisejí s inaktivací rolí a kategorií před zkopírováním nabídky.
- Akce **Aktualizovat ceny** na stránce **Projekty** neaktualizuje odhady výdajů a odhady materiálu.
