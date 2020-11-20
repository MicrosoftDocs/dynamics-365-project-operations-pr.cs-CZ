---
title: Rezervace zdrojů a jejich souvislost s přiřazeními úkolů
description: Toto téma obsahuje informace o způsobu správy pojmenovaných zdrojů, rezervací zdrojů a přiřazení úkolů a jejich vzájemných souvislostech.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: c4b976b49bd643bc7a774a86b1ba89bd76d7c916
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124990"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Rezervace zdrojů a jejich souvislost s přiřazeními úkolů


Pojmenované zdroje lze rezervovat k projektovému týmu a přiřadit projektovým úkolům třemi způsoby:

- Zdroj lze přímo rezervovat na projekt a poté přiřadit k projektovým úkolům.
- Úkoly lze přiřadit k obecnému zdroji, který se pak používá k vyhledání a nahrazení obecného zdroje pojmenovaným zdrojem. 

V obou případech akce rezervace zdroje rezervuje kapacitu zdroje.

Projektový manažer plánující projekt je vlastníkem projektového plánu a plánu. Pomocí obecného zdroje pro přiřazení a následného generování požadavku na zdroj z tohoto zdroje může projektový manažer rezervovat zdroje na projekt s průběhovými křivkami uvedenými v projektovém plánu. Mohou si rezervovat zdroje na projekt a pak je přiřadit k úkolům, neexistuje však způsob, jak sladit průběhové křivky rezervací s průběhovými křivkami úkolů. Rezervace nemají vliv na plán projektu.

Zvažte komplexní projekt s více překrývajícími se úkoly, kde je nutné, aby více zdrojů stejného typu pracovalo souběžně. Je-li zdroji přidělena průběhová křivka, která se liší od té, která je agregací jejich přiřazení, je obtížné upravit úkoly tak, aby odpovídaly průběhovým křivkám rezervací na jejich jednotlivé úkoly a jejich původní průběhové křivky.

V následujícím příkladu je celkové úsilí vyžadované stejným zdrojem ze sady čtyř úkolů 62 hodin za období dvou týdnů a existuje konkrétní průběhová křivka. Pokud je zdroj Bob rezervován na 62 hodin během stejných dvou týdnů, ale s různou průběhovou křivkou, požadavek a rezervace jsou ve shodě.

| **Průběhová křivka úkolu**    | **Celkové hodiny** | Po 6/4 | Út 6/5 | St 6/6 | Čt 6/7 | Pá 6/8 | So 6/9 | Ne 6/10 | Po 6/11 | Út 6/12 | St 6/13 | Čt 6/14 | Pá 6/15 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Úkol 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Úkol 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Úkol 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Úkol 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Součty**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Dostupnost Roberta
| **Rezervace   zdroje** | **Celkové hodiny** | Po 6/4 | Út 6/5 | St 6/6 | Čt 6/7 | Pá 6/8 | So 6/9 | Ne 6/10 | Po 6/11 | Út 6/12 | St 6/13 | Čt 6/14 | Pá 6/15 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Robert                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Neexistuje však systematický způsob, jak přiřadit průběhovou křivku rezervovaných hodin k úkolům na denní bázi. Pokud je vedoucí projektu ochotný změnit plán projektu, aby vyhověl dostupnosti zdroje, pak se bude muset odebrat přiřazení a revidovat všechny úkoly tak, aby odpovídaly průběhové křivce rezervace.

V případě, že organizace zadala úkol projektového plánování jak projektovému manažerovi, tak manažerovi zdrojů, projektový manažer nastaví plán a to zahrnuje průběhovou křivku požadované práce. Manažer zdrojů by neměl být schopen ovlivnit rozvrh bez znalostí manažera projektu změnou průběhových křivek úsilí při rezervování skutečných zdrojů. Pokud manažer zdrojů naplňuje něco jiného, než požadoval projektový manažer, musí dospět k dohodě o tom, jaké změny jsou zapotřebí v plánu projektu.

Vzhledem k tomu, že rezervace a přiřazení nejsou úzce spojeny, je možné rezervovat průběhové křivky, které se liší od křivek úkolu, nebo změnit přiřazení, což vede k situacím, kdy nejsou rezervace a přiřazení ve shodě.

**Zobrazení vyrovnání** umožňuje projektovému manažerovi zobrazit rezervace a přiřazení jednotlivých členů projektového týmu. Zobrazení používá barvy a stínování, aby ukázalo, kde existuje nesoulad mezi rezervacemi členů týmu a přiřazeními. Na základě těchto informací může projektový manažer přijmout nápravná opatření buď k rozšíření rezervací zdrojů pro případy, kdy existují přiřazení a žádné rezervace, nebo ke zrušení rezervace, kde jsou rezervovány zdroje, ale nemají žádná přiřazení.

> [!NOTE]
> Pokud přesunete úkol, kterému jste sami dali průběhové křivky, tyto křivky nejsou zachovány. Průběhové křivky jsou regenerovány podle kalendáře projektu, aby byly zohledněny změny v pracovní době a svátcích. Toto je záměrné, protože systém nezná záměr původní průběhové křivky a nemůže určit, zda má smysl zachovat tuto průběhovou křivku v novém časovém období. Protože rezervace a přiřazení nejsou ve shodě, rezervace zachovají průběhové křivky původní rezervace. V takovém případě bude nutné zrušit a opětovně rezervovat na novou průběhovou křivku přiřazení.

