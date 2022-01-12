---
title: Aktualizace Project Operations
description: Toto téma poskytuje informace o uvolněných verzích Dynamics 365 Project Operations.
author: sigitac
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5e37bc90a74e6bc9f1bf3d3820a34c3f4c3496d
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942831"
---
# <a name="project-operations-updates"></a>Aktualizace Project Operations

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení – od obchodu po proforma fakturaci a Project Operations pro scénáře založené na skladovém materiálu / výrobě_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a>Součásti Project Operations

Dynamics 365 Project Operations se skládá ze dvou komponent:

- Project Operations v prostředí Dataverse pokrývá funkce od příležitosti po proforma fakturaci. Dataverse se používá při omezeném nasazení Project Operations a nasazení Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě.
- Řízení projektů a účetnictví v prostředí Dynamics 365 Finance pokrývá funkce správy výdajů, účtování projektů a uznání výnosů. Prostředí aplikace Finance and Operations je použito v Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě, a pro scénáře založené na skladovém materiálu / výrobě.

## <a name="project-operations-release-notes"></a>Poznámky k verzi Project Operations
- Nejnovější poznámky k verzi Project Operations z prosince 2020 pro scénář [zdroje / položky, které nejsou na skladě](whats-new-dec-2021-resource-based.md).
- Nejnovější poznámky k verzi Project Operations z prosince 2020 pro scénář [nasazení Lite](../pro/whats-new/whats-new-dec-2021-lite.md).
- Nejnovější poznámky k verzi Project Operations z prosince 2020 pro scénář [skladové materiály/výroba](../prod-pma/whats-new/whats-new-oct-2021-stocked.md).

## <a name="project-operations-latest-version"></a>Nejnovější verze Project Operations

| Project Operations v prostředí Dataverse | Řízení projektů a účetnictví v prostředí aplikací Finance and Operations | 
| --- | --- |
| 4.27.0.242 | 10.0.23 |

U scénářů Project Operations se zdroji bez skladových materiálů doporučujeme použít orchestraci duálního zápisu ve verzi 2.3.1.15 nebo vyšší.

## <a name="release-schedule-for-project-operations-on-dataverse-environment"></a>Plán vydání pro Project Operations v prostředí Dataverse

Aktualizace Project Operations v prostředí Dataverse jsou k dispozici měsíčně. 

| Stanice | Oblast | Aktuální číslo verze | Automatické aktualizace pro omezené nasazení | Automatické aktualizace pro nasazení prostředků / bez zásob | Číslo příští verze | Další obecně dostupná verze |
|-----------|-----------------------|-----------------|--------------------|---------------------|---------------------|---------------------|
| Stanice 1 |   &nbsp;              |    &nbsp;       | &nbsp;             |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | První vydání         |  4.27.0.242     | Dokončit*          | Dokončit*           | TBD                 | 14. ledna 2022    |
| Stanice 2 |   &nbsp;              |    &nbsp;       | &nbsp;             |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Jižní Amerika         |  4.27.0.242     | Dokončit           | 07. ledna 2022    | TBD                 | 14. ledna 2022    |
|   &nbsp;  | Kanada                |  4.27.0.242     | Dokončit           | 07. ledna 2022    | TBD                 | 14. ledna 2022    |
|   &nbsp;  | Indie                 |  4.27.0.242     | Dokončit           | 07. ledna 2022    | TBD                 | 14. ledna 2022    |
|   &nbsp;  | Francie                |  4.27.0.242     | Dokončit           | 07. ledna 2022    | TBD                 | 14. ledna 2022    |
|   &nbsp;  | Jižní Afrika          |  4.27.0.242     | Dokončit           | 07. ledna 2022    | TBD                 | 14. ledna 2022    |
| Stanice 3 |      &nbsp;           |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Japonsko                 |  4.27.0.242     | Dokončit           | 07. ledna 2022    | TBD                 | 21. ledna 2022    |
|   &nbsp;  | Asie a Tichomoří          |  4.27.0.242     | Dokončit           | 07. ledna 2022    | TBD                 | 21. ledna 2022    |
|   &nbsp;  | Velká Británie         |  4.27.0.242     | Dokončit           | 07. ledna 2022    | TBD                 | 21. ledna 2022    |
|   &nbsp;  | Oceánie               |  4.27.0.242     | Dokončit           | 07. ledna 2022    | TBD                 | 21. ledna 2022    |
|   &nbsp;  | Spojené arabské emiráty  |  4.27.0.242     | Dokončit           | 07. ledna 2022    | TBD                 | 21. ledna 2022    |
| Stanice 4 |     &nbsp;            |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Evropě                |  4.26.0.155     | Dokončit           | 07. ledna 2022    | 4.27.0.242          | 10. ledna 2022    |
| Stanice 5 |     &nbsp;            |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Severní Amerika         |  4.26.0.155     | 07. ledna 2022   | 14. ledna 2022    | 4.27.0.242          | 17. ledna 2022    |

>[!Note]
> - Dokončeno* – Automatické aktualizace dokončeny ve verzi 4.27.0.195.


## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a>Plán vydávání pro správu projektů a účetnictví v prostředí aplikace Finance and Operations

Aktualizace pro správu projektů a účetnictví jsou vydávány osmkrát ročně.

|Podporovaná verze| Dostupnost Preview (PEAP) | Obecně dostupné (ruční aktualizace) | Počáteční datum vytvoření časového plánu automatické aktualizace (prostřednictvím nastavení aktualizace LCS) |   Ukončení služby   |
|:---------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|     10.0.23     |      15. října 2021       |        10. prosince 2021          |                          31. prosince 2021                           | 18. března 2022     |
|     10.0.22     |      3. září 2021      |        22. října 2021           |                          5. listopadu 2021                            | 14. ledna 2022   |


Cílová data vydání se mohou změnit. Další informace naleznete v části [Dostupnost aktualizace služby](/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=%2fdynamics365%2ffinance%2ftoc.json).

|Cílová verze | Dostupnost Preview (PEAP) | Obecně dostupné (ruční aktualizace) | Počáteční datum vytvoření časového plánu automatické aktualizace (prostřednictvím nastavení aktualizace LCS) |   Ukončení služby   |
|:---------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|     10.0.24     |      3. prosince 2021       |        14. ledna 2022           |                          4. února 2022                            | 15. dubna 2022     |
|     10.0.25     |      31. ledna 2022       |        18. března 2022             |                          1. dubna 2022                               | 10. června 2022      |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
