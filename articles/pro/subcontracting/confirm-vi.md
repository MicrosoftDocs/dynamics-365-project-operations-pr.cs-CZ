---
title: Potvrzení projektové faktury dodavatele
description: Tento článek vysvětluje, jak potvrdit fakturu dodavatele projektu v Microsoft Dynamics 365 Project Operations a finanční dopad potvrzení faktury dodavatele projektu.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261503"
---
# <a name="confirm-a-project-vendor-invoice"></a>Potvrzení projektové faktury dodavatele

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Po ověření všech řádků na faktuře dodavatele v Microsoft Dynamics 365 Project Operations můžete použít akci Potvrdit k potvrzení faktury dodavatele.

Když vyberete **Potvrdit** na faktuře dodavatele, dojde k následujícím akcím:

1. Stav faktury dodavatele je aktualizován na **Potvrzeno**.
2. Potvrzená faktura dodavatele a související záznamy jsou nadále pouze ke čtení a nelze je upravovat ani odstranit.
3. Pokud některé skutečné náklady odkazují na řádek faktury dodavatele jako součást procesu párování, všechny skutečné náklady, které jsou přidruženy k řádku faktury dodavatele odkazu, jsou stornovány.
4. Nové skutečné náklady se vytvářejí pomocí informací na řádku faktury dodavatele.
5. Po potvrzení faktury dodavatele již nemůžete vytvářet deníky oprav, zpracovávat odvolání časových záznamů nebo zrušit schválení původních skutečných časů, výdajů nebo materiálu, které byly stornovány.

> [!NOTE]
> Pokud má některý řádek na faktuře dodavatele stav ověření jiný než **Dokončeno**, fakturu dodavatele nelze potvrdit.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
