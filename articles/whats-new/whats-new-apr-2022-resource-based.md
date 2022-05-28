---
title: Co je nového, duben 2022 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Toto téma poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Microsoft Dynamics 365 Project Operations z dubna 2022 pro scénáře založené na zdrojích / neskladových položkách.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc713e7a0dd6993e38ce3e3b2ba19f796a6f4773
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613244"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Co je nového, duben 2022 - Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Toto téma se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.41.0.45
- Řízení projektů a účetnictví v Dynamics 365 Finance, verze prostředí 10.0.26

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

Kategorie zásobování lze použít v projektových nákupních objednávkách a nevyřízených fakturách dodavatele. Další informace viz [Používání kategorií zásobování s projektovými nákupními objednávkami a nevyřízenými fakturami dodavatele](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizace map duálního zápisu Project Operations

Následující tabulka ukazuje mapy duálního zápisu, které byly upraveny nebo přidány ve verzi Project Operations z března 2022.

| Mapování entity | Aktualizovaná verze | Komentáře |
| -------------- | ------------------- | ------------|
| Entita exportu řádku faktury dodavatele projektu integrace Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.4 | Tato mapa podporuje používání kategorií zásobování s nákupními objednávkami a nevyřízenými fakturami dodavatele. |

Vždy spusťte nejnovější verzi mapy ve vašem prostředí a povolte všechny související mapové tabulky při aktualizaci verze řešení Project Operations Dataverse a řešení Finance. Některé funkce a možnosti nemusí fungovat správně, pokud není aktivována nejnovější verze mapy. Aktivní verzi mapy můžete zobrazit ve sloupci **Verze** na stránce **Duální zápis**. Novou verzi mapy můžete aktivovat výběrem **Verze mapy tabulky** výběrem nejnovější verze a poté uložením vybrané verze. Pokud jste upravili integrovanou mapu tabulky, použijte změny znovu. Další informace: [Správa životního cyklu aplikace](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Pokud při spuštění mapy narazíte na problém, postupujte podle pokynů v části [Problém s chybějícími sloupci tabulky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) průvodce řešením problémů s duálním zápisem.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v Dataverse

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| ------------ | ---------------- | -------------- |
| Čas a výdaje | 2573900 | Funce **Moderní schválení** musí být ve výchozím nastavení povolena. |
| Fakturace a ceny | 2603313 | Opravena chyba duplicitního záznamu, která bránila přidání řádků cenových nabídek a smluv, které obsahují produkt. |
| Nasazení a konfigurace | 2611368 | Zákazníci musí mít možnost přidat do řešení až pět vlastních entit pomocí moderního návrháře aplikací. |
| Čas a výdaje | 2628285 | Opraven problém, který ovlivnil možnost nastavit správnou kategorii zdrojů během importu časového záznamu. |
| Správa příležitostí| 2628815 | Aktualizujte limit počtu znaků v popisu podrobností řádku citace tak, aby odpovídal limitu znaků předmětu úkolu, aby byl import úspěšný u úkolů, jejichž předmět je delší než 100 znaků. |
| Čas a výdaje| 2629547 | Pole **Odeslal** schválení projektu musí ukazovat na uživatele, který záznam odeslal. |
| Čas a výdaje| 2629865 | Pole **Kopírovat kategorii** na úkolech při kopírování projektů. |
| Čas a výdaje| 2636463 | Opraveny filtry na schválení v moderních formulářích schválení. |
| Plánování a sledování projektu | 2648300 | Opraven problém, který bránil změně vlastníka projektu. |
| Fakturace a ceny | 2563000 | Řádky deníku pro nevyfakturovaný prodej, kde se měna liší od měny kontraktu, nesmí být povoleny. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Řízení projektů a účetnictví v Dynamics 365 Finance

Sháníte-li informace o opravách chyb zahrnutých v této aktualizaci, přihlaste se ke službám Microsoft Dynamics Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
