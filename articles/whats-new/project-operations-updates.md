---
title: Aktualizace Project Operations
description: Toto téma poskytuje informace o uvolněných verzích Dynamics 365 Project Operations.
author: sigitac
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7b398bae07956f4c3de15ec53a860fca15422dd9f2a977086669ebf2fcdb240
ms.sourcegitcommit: 17353ff3f4aeb42a64bac5e1db000ac6def91d07
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/09/2021
ms.locfileid: "7024775"
---
# <a name="project-operations-updates"></a>Aktualizace Project Operations

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení – od obchodu po proforma fakturaci a Project Operations pro scénáře založené na skladovém materiálu / výrobě_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a>Součásti Project Operations

Dynamics 365 Project Operations se skládá ze dvou komponent:

- Project Operations v prostředí Dataverse pokrývá funkce od příležitosti po proforma fakturaci. Dataverse se používá při omezeném nasazení Project Operations a nasazení Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě.
- Řízení projektů a účetnictví v prostředí Dynamics 365 Finance pokrývá funkce správy výdajů, účtování projektů a uznání výnosů. Prostředí aplikace Finance and Operations je použito v Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě, a pro scénáře založené na skladovém materiálu / výrobě.

## <a name="project-operations-release-notes"></a>Poznámky k verzi Project Operations
- Nejnovější poznámky k verzi Project Operations z prosince 2020 pro scénář [zdroje / položky, které nejsou na skladě](whats-new-july-2021-resource-based.md).
- Nejnovější poznámky k verzi Project Operations z prosince 2020 pro scénář [nasazení Lite](../pro/whats-new/whats-new-july-2021-lite.md).
- Nejnovější poznámky k verzi Project Operations z prosince 2020 pro scénář [skladové materiály/výroba](../prod-pma/whats-new/whats-new-jul-2021-stocked.md).

## <a name="project-operations-latest-version"></a>Nejnovější verze Project Operations

| Project Operations v prostředí Dataverse | Řízení projektů a účetnictví v prostředí aplikací Finance and Operations | 
| --- | --- |
| 4.13.0.152 | 10.0.20 |

U scénářů Project Operations se zdroji bez skladových materiálů doporučujeme použít orchestraci duálního zápisu ve verzi 2.2.2.83 nebo vyšší.

## <a name="release-schedule-for-project-operations-on-dataverse-environment"></a>Plán vydání pro Project Operations v prostředí Dataverse

Aktualizace Project Operations v prostředí Dataverse jsou k dispozici měsíčně. 

| Stanice | Oblast | Aktuální číslo verze | Automatické aktualizace pro omezené nasazení | Automatické aktualizace pro nasazení prostředků / bez zásob | Číslo příští verze | Další obecně dostupná verze |
|-----------|-----------------------|-----------------|--------------------|---------------------|---------------------|---------------------|
| Stanice 1 |   &nbsp;              |    &nbsp;       | &nbsp;             |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | První vydání         |  4.13.0.152     | Dokončit           | 13. srpna 2021     | TBD                 | 27. srpna 2021     |
| Stanice 2 |   &nbsp;              |    &nbsp;       | &nbsp;             |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Jižní Amerika         |  4.13.0.152     | 13. srpna 2021    | 20. srpna 2021     | TBD                 | 27. srpna 2021     |
|    &nbsp; | Kanada                |  4.13.0.152     | 13. srpna 2021    | 20. srpna 2021     | TBD                 | 27. srpna 2021     |
|   &nbsp;  | Indie                 |  4.13.0.152     | 13. srpna 2021    | 20. srpna 2021     | TBD                 | 27. srpna 2021     |
|   &nbsp;  | Francie                |  4.13.0.152     | 13. srpna 2021    | 20. srpna 2021     | TBD                 | 27. srpna 2021     |
|   &nbsp;  | Spojené arabské emiráty  |  4.13.0.152     | 13. srpna 2021    | 20. srpna 2021     | TBD                 | 27. srpna 2021     |
|   &nbsp;  | Jižní Afrika          |  4.13.0.152     | 13. srpna 2021    | 20. srpna 2021     | TBD                 | 27. srpna 2021     |
| Stanice 3 |      &nbsp;           |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Japonsko                 |  4.12.0.152     | Dokončit*          | Dokončit            | 4.13.0.152          | 13. srpna 2021     |
|   &nbsp;  | Asie a Tichomoří          |  4.12.0.152     | Dokončit*          | Dokončit            | 4.13.0.152          | 13. srpna 2021     |
|   &nbsp;  | Velká Británie         |  4.12.0.152     | Dokončit*          | Dokončit            | 4.13.0.152          | 13. srpna 2021     |
|   &nbsp;  | Oceánie               |  4.12.0.152     | Dokončit*          | Dokončit            | 4.13.0.152          | 13. srpna 2021     |
| Stanice 4 |     &nbsp;            |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Evropě                |  4.12.0.152     | Dokončit           | Dokončit            | 4.13.0.152          | 20. srpna 2021     |
| Stanice 5 |     &nbsp;            |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Severní Amerika         |  4.12.0.152     | 13. srpna 2021    | 20. srpna 2021     | 4.13.0.152          | 27. srpna 2021     |


> [!NOTE]
> Automatické nasazení je dokončeno pro verzi 4.12.0.148. Pro aktualizovanou verzi vydání z července 2021 se neplánuje žádné automatické nasazení.

## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a>Plán vydávání pro správu projektů a účetnictví v prostředí aplikace Finance and Operations

Aktualizace pro správu projektů a účetnictví jsou vydávány osmkrát ročně.

|          Podporovaná verze          | Dostupnost Preview (PEAP) | Obecně dostupné (ruční aktualizace) | Počáteční datum vytvoření časového plánu automatické aktualizace (prostřednictvím nastavení aktualizace LCS) |   Ukončení služby   |
|:-------------------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|          10.0.20          |         28. května 2021        |           16. července 2021           |                             30. července 2021                             |  22. října 2021  |
|          10.0.19          |        23. dubna 2021       |            18. června 2021           |                             2. července 2021                             | 17. září 2021 |



Cílová data vydání se mohou změnit. Další informace naleznete v části [Dostupnost aktualizace služby](/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=%2fdynamics365%2ffinance%2ftoc.json).

|          Cílová verze          | Dostupnost Preview (PEAP) | Obecně dostupné (ruční aktualizace) | Počáteční datum vytvoření časového plánu automatické aktualizace (prostřednictvím nastavení aktualizace LCS) |   Ukončení služby   |
|:-------------------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|          10.0.21          |         02. srpna 2021     |           17. září 2021      |                             1. října 2021                           |  10. prosince 2021  |
|          10.0.22          |      3. září 2021      |          22. října 2021         |                           5. listopadu 2021                           |  14. ledna 2022  |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
