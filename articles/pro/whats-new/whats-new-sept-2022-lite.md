---
title: Co je nového, září 2022 – omezené nasazení Project Operations
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Microsoft Dynamics 365 Project Operations ze září 2022 pro omezené nasazení.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621226"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Co je nového, září 2022 – omezené nasazení Project Operations

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Tento článek se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.46.0.60

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

| Oblast funkcí | Název funkce | Více informací |
| --- | --- | --- |
| Správa příležitostí | **Revize a aktivace nabídek**<br>Project Operations přináší plnou podporu prodejního procesu. Nabídky projektu lze aktivovat, aby představovaly stav, kdy je nabídka pouze pro čtení a prochází kontrolou. Aktivované nabídky lze revidovat a vytvářet nové nabídky, které mají zvýšené číslo revize. Aktivované nabídky projektu a revize nabídky lze uzavírat jako získané nebo ztracené. | [Aktivace a úprava nabídky projektu](/dynamics365/project-operations/sales/activation-and-revision) |
| Fakturace a ceny | **Výchozí cena bez ohledu na časové pásmo**<br>Project Operations zavedly koncept nezávislosti data časového pásma u všech skutečných událostí projektu. Nové pole, **Datum transakce**, je nyní k dispozici na řádcích deníku a skutečných hodnotách a bude sloužit k uložení data, kdy k transakci došlo, ale bez převodu tohoto data na koordinovaný univerzální čas. Toto datum bude použito pro následné procesy, jako je prodlení s cenou a vytvoření faktury. | <p>[Určení nákladových sazeb pro odhady a skutečné hodnoty projektu](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Určení prodejních cen pro odhady projektu a skutečné hodnoty](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Fakturace a ceny | **Přepisy ceny platné k datu v Project Operations**<br>Přepisy cen platné k datu poskytují způsob, jak přepsat nebo změnit konkrétní ceny v ceníku. | [Přepsání cen s datem platnosti](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Čas a výdaje | **Globální schvalovatel**<br>Tato funkce umožňuje nezávislého dodavatele softwaru (ISV) a centralizované schvalování bez ohledu na stav projektu nebo člena týmu v projektu. | [Zabezpečení a schválení](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Fakturace a ceny | 2754422 | Odhady materiálu a nákladů neplynou do Dynamics 365 Finance, když jsou projekty zkopírovány do Dataverse. |
| Čas a výdaje | 2787409 | Neplatný schvalovatel může schválit neprojektovou časovou položku. |
| Správa příležitostí | 2788907 | Aktualizovaná chybová zpráva při ověřování jedinečnosti pro řádky objednávky, které obsahují příznaky. |
| Čas a výdaje | 2842253 | Zpracování výjimky null pro schválení času. |
| Fakturace a ceny | 2844181 | Nezískání ID korelace blokuje vytvoření faktury. |
| Fakturace a ceny | 2876628 | QLD, CLD – Rozlišení odhadovaného ceníku by mělo používat starší pole rozsahu dat ceníku. |
| Subdodávka | 2893222 | Pokud není pro řádek dílčí smlouvy zadána žádná role, mělo by být možné vybrat tento řádek u člena týmu pro jakoukoli roli. |
