---
title: Kopírování projektu
description: Toto téma poskytuje informace o kopírování projektů v Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cf80f2a1cd27aae33d123e45dee70d94ea4d01a9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073721"
---
# <a name="copy-a-project"></a>Kopírování projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

S Dynamics 365 Project Operations můžete rychle vytvářet nové projekty výběrem **Kopírovat projekt** ve formuláři **Projekty**. Chcete-li zkopírovat projekt, otevřete projekt, který chcete zkopírovat, a poté vyberte **Kopírovat projekt**. Akce zkopíruje:

- Vlastnosti projektu
- Strukturovaný rozpis prací
- Členové projektových týmů
- Odhady projektů
- Odhady projektových výdajů

## <a name="project-properties"></a>Vlastnosti projektu

Při kopírování projektu se zkopírují hodnoty v následujících polích:

- Jméno
- Popis
- Zákazník
- Šablona kalendáře
- Měna
- Smluvní jednotka
- Projektový manažer
- Stav
- Celkový stav projektu
- Komentáře
- Odhady
- Odhadované počáteční datum
- Datum ukončení
- Úsilí (hodiny)
- Odhadované pracovní náklady
- Odhadované výdajové náklady

## <a name="work-breakdown-structure"></a>Strukturovaný rozpis prací

Když je projekt zkopírován, zkopíruje se celý strukturovaný rozpis prací načtený ze zdrojů. Pojmenované zdroje jsou nahrazeny obecnými zdroji. Pokud pojmenované zdroje nemají stejnou pracovní dobu jako obecný zdroj, plán se přepočítá a doba trvání úkolu se může změnit.

## <a name="project-team-members"></a>Členové projektových týmů

Když se projektový tým zkopíruje ze zdrojového projektu, zkopírují se obecné zdroje. Přiřazení obecných zdrojů jsou rovněž zachována tak, jako byla ve zdrojovém projektu. Pojmenované zdroje budou převedeny na obecné členy týmu.

## <a name="estimates"></a>Odhady

Při kopírování projektu se zkopírují řádky odhadu zdrojů a výdajů ze zdrojového projektu. 

Informace o tom, jak programátorsky přistupovat ke kopírování projektu, najdete v části [Vývoj projektových šablon pomocí nástroje kopírovat projekt](dev-copy-project.md).
