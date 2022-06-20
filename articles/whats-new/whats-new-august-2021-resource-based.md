---
title: Co je nového v srpnu 2021 - Project Operations pro scénáře založené na zdrojích/položkách, které nejsou na skladě
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations ze srpna 2021 pro scénáře založené na zdrojích / neskladových položkách.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bd91f7f6b3a6f78161f8900aa06c810a58609b53
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912278"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového v srpnu 2021 - Project Operations pro scénáře založené na zdrojích/položkách, které nejsou na skladě

*Platí pro: Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě*

Tento článek se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

   - Project Operations v prostředí Microsoft Dataverse verze 4.13.0.152.
   - Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.20.

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

V této vydané verzi jsou zahrnuty následující funkce:

- **Sady schválení**: Sady schválení nastavují čas skupiny, výdaje nebo schválení použití materiálu do menších podsad operací. Toto seskupení umožňuje zpracování schválení podle projektu v konkrétním pořadí a umožňuje opakování a sekvenování. Seskupení žádostí o schválení zvyšuje spolehlivost a sledovatelnost zpracování schválení pro velké objemy schvalování. Další informace viz [Sady schválení](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

V této verzi nejsou k dispozici žádné aktualizace map duálního zápisu Project Operations.

Aktuální seznam a verze map duálního zápisu Project Operations najdete v části [Verze map duálního zápisu Project Operations](../environment/resource-dual-write-maps.md).

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a řešení Finance. Pokud není aktivována nejnovější verze mapy, některé funkce a možnosti nemusí fungovat správně. Aktivní verzi mapy můžete vidět na stránce **Duální zápis** ve sloupci **Verze**. Aktivujte novou verzi mapy výběrem **Verze mapy tabulky** a výberte nejnovější verzi a uložte vybranou verzi. Pokud jste přizpůsobili připravenou mapu tabulky, změny znovu použijte. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud narazíte na problém se spuštěním mapy, postupujte podle pokynů v [Problém chybějících sloupců tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v příručce pro řešení potíží s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| **Oblast funkcí** | **Referenční číslo** | **Aktualizace pro zvýšení kvality** |
| --- | --- | --- |
| Fakturace a ceny | 2295625 | Název milníku musí být zkopírován z plánu faktur do detailu řádku faktury. |
| Fakturace a ceny | 2316323 | V Project Operations by nemělo být možné upravovat slevy na proforma faktuře pro scénáře založené na zdrojích. |
|   Správa příležitostí | 2338619 | Obchodní pravidla pro **příležitost** a **nabídku** musejí být vyvolána pouze na stránkách. |
| Správa zdrojů | 2316523 | Použití **Poslat žádost** z požadavku na zdroj, ke kterému je připojena role, by se nemělo zobrazovat chyba. |
| Správa zdrojů | 2326885 | Při vytváření požadavku na zdroj prostřednictvím projektu by se neměla zobrazit chyba. |
| Čas a výdaje | 2335584 | Odmítnuté toky úkolů v zadávání času. |
| Čas a výdaje | 2336884 | Tlačítko **Kopírovat týden** pro zadání času musí fungovat nejen pro aktuálního uživatele. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Řízení projektů a účetnictví v Dynamics 365 Finance

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Cestování a výdaje | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Nesprávné transakce dodavatele a částky transakcí daně z prodeje jsou zaúčtovány, když je z transakce kreditní kartou vytvořen výdaj. |
| Cestování a výdaje | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Chybné vypořádání jsou řádky vytvořené při generování deníku plateb. |
| Cestování a výdaje | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Nesprávné částky transakcí daně z prodeje jsou zaúčtovány, když je z transakce kreditní kartou vytvořen výdaj. |
| Cestování a výdaje | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Odstranění řádku výdajů může trvat dlouho. |
| Účetnictví projektu | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Systém nepodporuje nastavení nepřetržitého sekvenčního číslování, zaúčtujete-li odhad po využití 4619395 kB. |
| Účetnictví projektu | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Účtování faktury dodavatele může selhat s chybovou zprávou „Transakce na poukázce nejsou v souladu k datu 17. 5. 2021. (účetní měna: 0,00 - měna vykazování: 0,01)“ |
