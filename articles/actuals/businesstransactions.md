---
title: Obchodní transakce v Project Operations
description: Toto téma poskytuje přehled konceptu obchodních transakcí v aplikaci Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582196"
---
# <a name="business-transactions-in-project-operations"></a>Obchodní transakce v Project Operations

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

V Microsoft Dynamics 365 Project Operations je *obchodní transakce* abstraktním konceptem, který není reprezentován žádnou entitou. Některá společná pole a procesy v entitách jsou však navrženy tak, aby používaly koncept obchodních transakcí. Následující entity používají tuto abstrakci:

- Podrobnosti řádku nabídky
- Podrobnosti řádku smlouvy
- Řádky odhadu
- Řádky deníku
- Skutečnost

Z těchto entit jsou na *fázi odhadu* v životním cyklu projektu mapovány Podrobnosti řádku nabídky, Podrobnosti řádku smlouvy a Řádky odhadu. Entity Řádky deníku a Skutečné hodnoty jsou mapovány na *fázi spuštění* v životním cyklu projektu.

Project Operations zachází se záznamy v těchto pěti entitách jako s obchodními transakcemi. Jediným rozdílem je, že záznamy v entitách, které jsou mapovány na fázi odhadu (Podrobnosti řádku nabídky, Podrobnosti řádku smlouvy a Řádky odhadu), jsou považovány za *finanční prognózy*, zatímco záznamy v entitách, které jsou mapovány na fázi spuštění (Řádky deníku a Skutečné hodnoty), jsou považovány za *finanční fakty*, které již nastaly.

Další informace viz [Odhady](../project-management/estimating-projects-overview.md) a [Skutečné hodnoty](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepty, které jsou jedinečné pro obchodní transakce

Následující koncepty jsou jedinečné pro koncept obchodních transakcí:

- Typ transakce
- Třída transakce
- Původ transakce
- Propojení transakce

### <a name="transaction-type"></a>Typ transakce

Typ transakce představuje načasování a kontext finančního dopadu na projekt. Je definován sadou možností, která má v Project Operations následující podporované hodnoty:

- Náklady
- Projektová smlouva
- Nefakturovaný prodej
- Fakturovaný prodej
- Vnitropodnikový prodej
- Jednotkové náklady zdroje

### <a name="transaction-class"></a>Třída transakce

Třída transakce představuje různé typy nákladů vynaložených na projekty. Je definován sadou možností, která má v Project Operations následující podporované hodnoty:

- Čas
- Výdaje
- Materiál
- Poplatek
- Milník
- Daň

> [!NOTE]
> Hodnotu **Milníku** obvykle používá obchodní logika v Project Operations u fakturací s pevnou cenou.

### <a name="transaction-origin"></a>Původ transakce

Původ transakce je entita, která ukládá původ každé obchodní transakce, aby pomohla s vykazováním a sledovatelností. Na začátku provádění projektu vytvoří každá obchodní transakce další obchodní transakci, která zase vytvoří další obchodní transakci a tak dále.

### <a name="transaction-connection"></a>Propojení transakce

Propojení transakce je entita, která uchovává vztah mezi dvěma podobnými obchodními transakcemi, jako jsou např. náklady a související skutečné hodnoty prodeje nebo storna transakcí, které jsou spouštěny fakturačními aktivitami, jako je např. potvrzení faktury nebo opravy faktury.

Entity Původ transakce a Propojení transakce vám společně pomáhají sledovat vztahy mezi obchodními transakcemi a akcemi, které způsobily vytvoření specifické obchodní transakce.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
