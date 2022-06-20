---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 19, V3
description: Tento článek uvádí funkce a opravy, které jsou k dispozici v Project Service Automation, vydání Update 19, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: a17275220eec726107e8ce5f82bdf5cdd403033e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915498"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation, vydání aktualizace 19, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tento článek uvádí funkce a opravy, které jsou nové nebo se změnily v PSA V3, vydání Update 19. Tato verze má číslo sestavení V3.10.30.41 a je obvykle k dispozici prostřednictvím automatické aktualizace v květnu 2020.

## <a name="update-release-19"></a>Aktualizace verze 19

### <a name="bug-fixes"></a>Opravy chyb

**Čas a výdaje**

Byly vyřešeny následující problémy: 

- Chyby odvozené z importu časových vstupů nejsou správně zviditelněny.
- Mřížka pro zadání času nepodporuje chování v terénu **Pouze datum**.
- Zdroje projektu nemohou vytvořit náklady s projektem.

**Správa projektů**

Byly vyřešeny následující problémy: 

-  Úloha na nižším stupni podřízenosti způsobuje nesprávný odhad úsilí během výpočtu dokončení (EAC).

**Sales**

Byly vyřešeny následující problémy: 

- Akce **Přepočítat** nefunguje s podrobnostmi o nákladech na smlouvu nebo s podrobnostmi o nabídce.
- V odhadech nákladů chybí **aktualizované ceny**.
-  Zákazníci si nemohou vybrat vlastní důvody stavu smlouvy ze stránky **Projektová smlouva**.
- Při vytváření vlastního ceníku z nabídky dochází u zákazníků k poklesu výkonu.
- Zákazníci narážejí na nekonzistenci s výchozími hodnotami **jednotka** na stránkách **Podrobnosti řádku nabídky** a **Podrobnosti řádku smlouvy**.
- Přidání položek z kategorie nefakturovatelné transakce do fakturovatelného řádku smlouvy nebude respektovat typ fakturace **Nefakturovatelné** v kategorii transakce.
- Zákazníci nemohou používat nově přidané role a kategorie u dříve vytvořených smluv.
- Zákazníci zažívají snížený výkon Zbytečné načítání v souboru PreValidateProjectTeamMemberUpdate.cs
- Role nastavené jako nefakturovatelné v seznamu **Kategorie zdrojů** by měly být přidány na kartu **Fakturovatelné role** jako **Nefakturovatelné** na řádku smlouvy pro projekt.
- Zákazníci se mohou při vytváření projektu setkat se sníženým výkonem, protože **GetBookableResourceIdFromUser** načte všechny sloupce rezervovatelných zdrojů namísto pouze primárního ID.
- Entita **Typ transakce** postrádá plug-in aktualizace před ověřením, aby uživatelům zabránila v zadání vlastností **Units** a **UnitGroups**, které nejsou platné pro typy transakcí.
- Krok **Odebrat** krok nefunguje při importu zadání času.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
