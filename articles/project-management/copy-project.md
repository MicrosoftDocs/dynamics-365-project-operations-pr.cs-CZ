---
title: Kopírování projektu
description: Toto téma poskytuje informace o kopírování projektů v Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907989"
---
# <a name="copy-a-project"></a>Kopírování projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

S Dynamics 365 Project Operations můžete rychle vytvářet nové projekty pomocí akce **Kopírovat projekt** ve formuláři **Projekty**. Chcete-li zkopírovat projekt, vyberte projekt a poté vyberte **Kopírovat**. Akce zkopíruje:

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