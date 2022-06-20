---
title: Zrušení faktury dodavatele projektu
description: Tento článek vysvětluje, jak zrušit fakturu dodavatele projektu v Microsoft Dynamics 365 Project Operations a finanční dopad zrušení faktury dodavatele projektu.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7ddaadc0f6e336a8ba67bb4ad8000f7e894f3eb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911542"
---
# <a name="cancel-a-project-vendor-invoice"></a>Zrušení faktury dodavatele projektu

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Fakturu dodavatele nelze po potvrzení upravit ani odstranit. Pokud se na faktuře dodavatele vyskytla chyba, která byla potvrzena, můžete pomocí akce Zrušit zvrátit dopad faktury dodavatele a vytvořit novou fakturu dodavatele.

Když vyberete **Zrušit** na faktuře dodavatele, dojde k následujícím akcím:

1. Stav faktury dodavatele je aktualizován na **Zrušeno**.
2. Zrušená faktura dodavatele a související záznamy jsou nadále pouze ke čtení a nelze je upravovat ani odstranit.
3. Veškeré skutečné náklady, které byly vytvořeny na základě řádků faktury dodavatele jako součást potvrzení faktury dodavatele, jsou stornovány.
4. Pokud byly nějaké skutečné náklady spojeny s řádky faktury dodavatele jako součást procesu párování, původní potvrzení faktury dodavatele je stornovalo. Během zrušení faktury dodavatele se tyto skutečné náklady znovu vytvoří. Původy ukazují na položky času, nákladů nebo použití materiálu.
5. Po zrušení faktury dodavatele můžete znovu vytvářet deníky oprav, zpracovávat odvolání časových záznamů a zrušit schválení původních skutečných časů, výdajů nebo materiálu.

> [!NOTE]
> Zrušit lze pouze potvrzené projektové faktury dodavatele. Faktury dodavatele v jiných stavech nelze zrušit.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
