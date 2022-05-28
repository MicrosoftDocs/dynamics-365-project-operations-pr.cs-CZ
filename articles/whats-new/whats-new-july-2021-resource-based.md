---
title: Co je nového, červenec 2021 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Toto téma poskytuje informace o aktualizacích kvality dostupných ve verzi Project Operations z července 2021 pro scénáře založené na zdrojích / položkách, které nejsou na skladě.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1c88f3b4747005bee0d68d0e8a4314c01ffdaf34
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600872"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového, červenec 2021 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

*Platí pro: Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě*

Toto téma se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

   - Project Operations v prostředí Microsoft Dataverse verze 4.12.0.148 nebo 4.12.0.152.
   - Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.20.

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

V této vydané verzi jsou zahrnuty následující funkce:

- Možnost pro správce zobrazit protokoly PSS a protokoly sady operací z nabídky nastavení. Protokoly jsou uloženy po dobu 90 dnů.

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

V této verzi nejsou k dispozici žádné aktualizace map duálního zápisu Project Operations.

Aktuální seznam a verze map duálního zápisu Project Operations najdete v části [Verze map duálního zápisu Project Operations](../environment/resource-dual-write-maps.md).

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a řešení Finance. Pokud není aktivována nejnovější verze mapy, některé funkce a možnosti nemusí fungovat správně. Aktivní verzi mapy můžete vidět na stránce **Duální zápis** ve sloupci **Verze**. Aktivujte novou verzi mapy výběrem **Verze mapy tabulky** a výberte nejnovější verzi a uložte vybranou verzi. Pokud jste přizpůsobili připravenou mapu tabulky, změny znovu použijte. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud narazíte na problém se spuštěním mapy, postupujte podle pokynů v [Problém chybějících sloupců tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v příručce pro řešení potíží s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| **Oblast funkcí**              | **Referenční číslo** | **Aktualizace pro zvýšení kvality**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fakturace a ceny           | 2224046              | Pole **Třída transakce** je upravitelné na kartě **Podrobnosti řádku nabídky** ale je uzamčeno, pokud pracujete na stránce **Podrobnosti řádku nabídky**.                                                                     |
| Fakturace a ceny           | 2224400              | Akce **Uzavřít nabídku, jako získanou** selže, pokud nabídka nemá žádné milníky dat.                                                                                                                                    |
| Fakturace a ceny           | 2234089              | Když ručně zadáte popis produktu, vymaže se po zadání množství pro odhad materiálu.                                                                                                                         |
| Fakturace a ceny           | 2234100              | Mřížka **Nastavení fakturace úkolů** nezahrnuje sloupec **Materiál** a jeho hodnotu na kartě **Fakturace úkolů** projektu.                                                                                                       |
| Fakturace a ceny           | 2277409              | ID produktu není k dispozici v detailu řádku smlouvy pro řádek typu materiálu.                                                                                                                                        |
| Fakturace a ceny           | 2281728              | Vytvoření řádku smlouvy zbytečně přehodnocuje skutečné hodnoty, což způsobuje výrazné zvýšení objemu dat, a to má dopad na výkon.                                                                                |
| Fakturace a ceny           | 2298668              | Řádky deníku spojené s odvolaným a odstraněným výdajem nebudou odstraněny.                                                                                                                                     |
| Fakturace a ceny           | 2300192              | Když více uživatelů upravuje fakturu, je možné na potvrzené faktuře vytvořit nový detail řádku faktury.                                                                                   |
| Fakturace a ceny           | 2301569              | Faktury nelze opravit, pokud byla použita záloha částky \$0.                                                                                                                                        |
| Fakturace a ceny           | 2307965              | Pokud je cena kategorie vytvořena s chybějícími hodnotami, dojde k chybě.                                                                                                                           |
| Fakturace a ceny           | 2326870              | Došlo k chybě v **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete**, je-li **producttypecode** null.                                                                            |
| Fakturace a ceny           | 2332732              | Dojde k chybě, pokud je milník řádku smlouvy vytvořen bez řádku objednávky.                                                                                                                |
| Plánování a sledování projektu | 2181094              | Rozhraní API pro plánování projektu nyní podporuje protokoly PSS a protokoly provozních sad, které jsou uloženy po dobu 90 dnů.                                                                                                                  |
| Plánování a sledování projektu | 2254201              | Popisek **Režim plánu** je aktualizován podrobnostmi, které popisují výchozí logiku.                                                                                                                                      |
| Plánování a sledování projektu | 2300252              | Mezipaměť odpovědi **openProject** je aktualizována a zahrnuje vlastníka tokenu v klíči mezipaměti, **základní adresu URL** a **Adresu URL segmentu**, aby **Adresa URL požadavku** šlo vždy znovu vytvořit, pokud se změní **základní adresa URL**. |
| Plánování a sledování projektu | 2301312              | **msdyn_membershipstatus** byl odebrán ze zobrazení **Člen projektového týmu**.                                                                                                                                        |
| Plánování a sledování projektu | 2302759              | Výrobky jsou zbytečně stahovány na karty **Přiřazení zdrojů**, **Odhady** a **Odhady výdajů**.                                                                                                        |
| Plánování a sledování projektu | 2308050              | **CopyProject** selže s chybou „Nepodařilo se získat token pro komunikaci se vzdálenou službou“.                                                                                                                           |
| Plánování a sledování projektu | 2322650              | Zobrazení **Seznam úkolů projektu** bylo aktualizováno tak, aby ve výchozím nastavení zobrazovalo datum úkolu.                                                                                                            |
| Plánování a sledování projektu | 2327266              | **CopyProject** při kopírování odhadů generuje chybu „Klíč nebyl nalezen ve slovníku“.                                                                                                      |
| Plánování a sledování projektu | 2328123              | **CopyProject** generuje chybu „Nepodařilo se získat token pro komunikaci se vzdálenou službou“.                                                                                                                          |
| Plánování a sledování projektu | 2336258              | **CopyProject** nesprávně kopíruje názvy pozic zdrojů.                                                                                                                                                 |
| Fakturace a ceny           | 2224476              | Pole **Rezervovatelný zdroj** není správně výchozí pro přihlášeného uživatele na stránce **Využití materiálu**.                                                                                                            |
| Správa zdrojů           | 2277249              | Při aktualizaci požadavku na jiný než projektový prostředek dojde k chybě.                                                                                                            |
| Správa zdrojů           | 2323869              | Využití zdrojů správně nerozpozná filtrované prostředky.                                                                                                                                             |
| Čas a výdaje              | 2176538              | Na ovládací prvek **Časový záznam** jsou použity nesprávné operátory filtrů.                                                                                                                                                   |
| Čas a výdaje              | 2177462              | Odstranění záznamu času v mřížce neaktualizuje stav tlačítka **Odeslat**, **Odvolání**, **Vymazat** a **Upravit záznam** podle očekávání.                                                                                        |
| Čas a výdaje              | 2299985              | **TimeEntriesImportFromResourceAssignment** neudržuje čas začátku / konce z průběhových křivek přiřazení.                                                                                                  |
| Čas a výdaje              | 2318426              | Po zadání času lze uzamčená pole stále upravovat.                                                                                                                                   |
| Čas a výdaje              | 2323749              | Dojde k chybě, když je vytvořen výdaj z karty **Související** rezervovatelného zdroje.                                                                                                      |
| Čas a výdaje              | 2327678              | Když vytvoříte časový záznam z karty **Související** rezervovatelného prostředku, nadřazený prostředek není předán ovládacímu prvku časový záznam.                                                                            |
| Obecná                       | 2296857              | Sledování pokroku pro dlouho běžící úlohy.                                                                                                                                                                        |
| Obecná                       | 2253682              | Řešení duálního zápisu Project Operations by se nemělo instalovat, když je jádro duálního zápisu nainstalováno v prostředí bez řešení orchestrace duálního zápisu.                                                |
| Obecná                       | 2316420              | Zřízení jádra projektové služby selže, pokud se změní obchodní jednotka uživatele aplikace.                                                                                                                     |
| Obecná                       | 2376405              | Opravený problém s aktualizací řízenou vydavatelem (aktualizace kvality je k dispozici ve verzi 4.12.0.152)                                                                                                                     |
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Řízení projektů a účetnictví v Dynamics 365 Finance

| Oblast funkcí                      | Referenční číslo | Aktualizace pro zvýšení kvality                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Přehled řízení projektů a účetnictví | 4620267          | Nelze přizpůsobit formuláře pro přidání pole **Účel** na stránky **Transakce zaúčtovaná v projektu**, **Vytvoření návrhu faktury** a **Návrh faktury**.                                                                                                                                                                                         |
| Přehled řízení projektů a účetnictví | 4613449          | Když vyberete ID kontraktu projektu v Finance, integrované prostředí Project Operations otevře stránku a vytvoří nový záznam namísto stránky pro již vytvořené smlouvy projektu.                                                                                                                                           |
| Přehled řízení projektů a účetnictví | 4614445          | V nasazení integrovaného scénáře Project Operations nelze upravit pole **Skupina DPH zboží** v návrhu faktury, která je importováná z fázování. Skupinu DPH položek je možné upravit pro návrh otevřené faktury všech typů transakcí, včetně účtu, hodin, výdajů, poplatků a položek. |
| Přehled řízení projektů a účetnictví |                  | Nelze zaúčtovat návrh faktury, která je výsledkem záporné časové opravy transakce.                                                                                                                                                                                                                                              |
| Přehled řízení projektů a účetnictví |                  | Řádky návrhu faktury jsou duplikovány z důvodu více periodických procesů **Import z fázování** běžících současně.                                                                                                                                                                                                                |

