---
title: Co je nového v červenci 2021 - Project Operations omezené
description: Toto téma poskytuje informace o aktualizacích kvality dostupných ve verzi omezeného nasazení Project Operations z července 2021.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6992498df5beb97d4e7197e301f093320dc28a23
ms.sourcegitcommit: 3abf1e67938d91bd826b025ae3187cd313f556b9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433645"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Co je nového v červenci 2021 - Project Operations omezené

_Platí pro: Omezené nasazení – od obchodu po pro forma fakturaci_

Toto téma se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

  - Project Operations v prostředí Dataverse verze 4.12.0.148.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality
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
