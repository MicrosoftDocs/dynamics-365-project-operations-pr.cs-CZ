---
title: Co je nového, září 2021 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Toto téma poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations ze září 2021 pro scénáře založené na zdrojích / neskladových položkách.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 842ea95892fa4f7a29a778cfd2c33a66e84f676c
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547146"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového, září 2021 – Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

*Platí pro: Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě*

Toto téma se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

   - Project Operations v prostředí Microsoft Dataverse verze 4.14.0.99.
   - Řízení projektů a účetnictví v prostředí Dynamics 365 Finance verze 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

V této verzi nejsou k dispozici žádné aktualizace map duálního zápisu Project Operations. Aktuální seznam a verze map duálního zápisu Project Operations najdete v části [Verze map duálního zápisu Project Operations](../environment/resource-dual-write-maps.md).

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a řešení Finance. Pokud není aktivována nejnovější verze mapy, některé funkce a možnosti nemusí fungovat správně. Aktivní verzi mapy můžete vidět na stránce **Duální zápis** ve sloupci **Verze**. Novou verzi mapy můžete aktivovat výběrem **Verze mapy tabulky** výběrem nejnovější verze a poté uložením vybrané verze. Pokud jste přizpůsobili připravenou mapu tabulky, změny znovu použijte. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud při spuštění mapy narazíte na problém, postupujte podle pokynů v části [Problém s chybějícími sloupci tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) průvodce řešením problémů s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| **Oblast funkcí** | **Referenční číslo** | **Aktualizace pro zvýšení kvality** |
| --- | --- | --- |
| Čas a výdaje | 1811407 | Upravena role zabezpečení schvalovatele projektu pro schválení položky vstupu výdajů. |
| Čas a výdaje | 1811438 | Upravena role zabezpečení schvalovatele projektu pro zrušení schválení časového záznamu. |
| Čas a výdaje | 2370126 | Aktualizovány ikony **Úkol projektu** a **Role** v entitě **Časový záznam**. |
| Čas a výdaje | 2379879 | Opravena funkce **Kopírovat týden** v časovém záznamu při použití aplikace Dynamics 365 pro telefony. |
| Fakturace a ceny | 2371906 | Celková částka proforma faktury nesmí být nastavitelná v Project Operations pro nasazení na základě zdrojů. |
| Fakturace a ceny | 2385802 | Opravena chyba, ke které dochází při záporných skutečných hodinách při aktualizaci součtů projektu. |
| Fakturace a ceny | 2389675 | Vylepšené chování při potvrzování proforma faktury. Entita dlouhotrvajících úloh musí vzít v úvahu aktivitu požadovanou pro zápis výsledků potvrzení pro účetnictví. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Přehled řízení projektů a účetnictví v Dynamics 365 Finance

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Cestování a výdaje | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Částky transakcí dodavatele a transakcí DPH, které jsou zaúčtovány z výdajů, které byly vytvořeny z transakce paltební kartou, jsou nesprávné. |
| Cestování a výdaje | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Při generování deníku plateb se vytvoří nesprávné řádky vyrovnání. |
| Cestování a výdaje | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Částky transakcí DPH, které jsou zaúčtovány z výdajů, které byly vytvořeny z transakce paltební kartou, jsou nesprávné. |
| Cestování a výdaje | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Odstranění řádku výdajů může trvat dlouho. |
| Účetnictví projektu | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Po použití KB 4619395 není podporována změna číselné řady na **Průběžně**, a když zaúčtujete odhad, dojde k chybě „Systém nepodporuje nastavení „Průběžně“ číselné řady Proj_X.“ |
| Účetnictví projektu | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Zaúčtování faktury dodavatele může selhat s chybovou zprávou „Transakce na dokladu nevyrovnává k datu 17. 5. 2021. (účetní měna: 0,00 – měna vykazování: 0,01).“ |
