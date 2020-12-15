---
title: Vývoj šablon projektů pomocí kopírování projektu
description: Tento téma poskytuje informace o tom, jak vytvořit šablony projektu pomocí vlastní akce Kopírovat projekt.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642400"
---
# <a name="develop-project-templates-with-copy-project"></a>Vývoj šablon projektů pomocí kopírování projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations podporuje schopnost kopírovat projekt a vrátit jakékoli přiřazení zpět k obecným prostředkům, které představují roli. Zákazníci mohou pomocí této funkce vytvářet základní šablony projektů.

Když vyberete **Kopírovat projekt**, je aktualizován stav cílového projektu. Použijte **Důvod stavu** k určení, kdy je akce kopírování dokončena. Výběr možnosti **Kopírovat projekt** také aktualizuje počáteční datum projektu na aktuální počáteční datum, pokud v entitě cílového projektu není zjištěno žádné cílové datum.

## <a name="copy-project-custom-action"></a>Vlastní akce Kopírovat projekt 

### <a name="name"></a>Jméno 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Vstupní parametry
Jsou tři vstupní parametry:

| Parametr          | Typ   | Hodnoty                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** nebo **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Odkaz na entitu | Zdrojový projekt |
| Cíl             | Odkaz na entitu | Cílový projekt |


- **{"clearTeamsAndAssignments":true}**: Výchozí chování pro Project for the Web a odstraní všechna přiřazení a členy týmu.
- **{"removeNamedResources":true}** Výchozí chování pro Project Operations a vrátí přiřazení na obecné prostředky.

Další informace o akcích naleznete v části [Použití akcí Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Zadejte pole ke kopírování 
Po zavolání se akce **Kopírovat projekt** podívá na pohled projektu **Kopírovat sloupce projektu** k určení, která pole se mají kopírovat při kopírování projektu.
