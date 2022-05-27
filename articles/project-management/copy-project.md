---
title: Kopírování projektu
description: Toto téma obsahuje informace o kopírování projektů v Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574422"
---
# <a name="copy-a-project"></a>Kopírování projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

V Dynamics 365 Project Operations můžete rychle vytvářet nové projekty výběrem volby **Kopírovat projekt** ve formuláři **Projekty**. Chcete-li zkopírovat projekt, otevřete projekt, který chcete zkopírovat, a poté vyberte **Kopírovat projekt**. Akce zkopíruje následující:

- Vlastnosti projektu 
- Strukturovaný rozpis prací
- Členové projektových týmů
- Odhady projektů
- Odhady projektových výdajů
- Odhady materiálu projektu
- Kontrolní seznamy projektu
- Kbelíky projektů

## <a name="project-properties"></a>Vlastnosti projektu

Při kopírování projektu se zkopírují hodnoty v následujících polích.

| Pole | Project Operations pro neskladové materiály | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Name | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| zákazníku | :heavy_check_mark: | :heavy_check_mark: | |
| Šablona kalendáře | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Měna | :heavy_check_mark: | :heavy_check_mark: | |
| Smluvní jednotka | :heavy_check_mark: | :heavy_check_mark: | |
| Vlastnící společnost | :heavy_check_mark: | | |
| Projektový manažer | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Celkový stav projektu | :heavy_check_mark: | :heavy_check_mark: | |
| Komentáře | :heavy_check_mark: | :heavy_check_mark: | |
| Odhady | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Odhadované počáteční datum</p><p><strong>Poznámka:</strong> Toto pole určuje datum, kdy je projekt vytvořen z kopie. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Odhadované datum dokončení</p><p><strong>Poznámka:</strong> Datum v tomto poli je upraveno na základě data zahájení nového projektu, který byl vytvořen z kopie.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Úsilí (hodiny) | :heavy_check_mark: | :heavy_check_mark: | |
| Odhadované pracovní náklady | :heavy_check_mark: | :heavy_check_mark: | |
| Odhadované výdajové náklady | :heavy_check_mark: | :heavy_check_mark: | |
| Odhadované náklady na materiál | | :heavy_check_mark: | |

> [!NOTE]
> Projekt kopírování je dlouhá operace. Kopírují se také záznamy projektu, jejich příslušné atributy a mnoho souvisejících entit. Z důvodu dlouhodobé povahy operace je po spuštění kopírování cílová stránka projektu uzamčena pro úpravy, dokud není operace kopírování dokončena.

## <a name="work-breakdown-structure"></a>Strukturovaný rozpis prací

Když je projekt zkopírován, zkopíruje se celý strukturovaný rozpis prací načtený ze zdrojů. Pojmenované zdroje jsou nahrazeny obecnými zdroji. Pokud pojmenované zdroje nemají stejnou pracovní dobu jako obecný zdroj, plán se přepočítá a doba trvání úkolů se může změnit.

## <a name="project-team-members"></a>Členové projektových týmů

Když se projektový tým zkopíruje ze zdrojového projektu, zkopírují se obecné zdroje. Přiřazení obecných zdrojů jsou rovněž zachována tak, jako byla ve zdrojovém projektu. Pojmenované zdroje budou převedeny na obecné členy týmu.

> [!NOTE]
> Členové týmu a přiřazení se do Project for the Web nekopírují.

## <a name="estimates"></a>Odhady

Při kopírování projektu se zkopírují řádky odhadu zdrojů, výdajů a materiálu ze zdrojového projektu. 

Informace o tom, jak programátorsky přistupovat ke kopírování projektu, najdete v části [Vývoj projektových šablon pomocí nástroje kopírovat projekt](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Nabídky a smlouvy

Nabídky a smlouvy nejsou propojeny s cílovým projektem.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
