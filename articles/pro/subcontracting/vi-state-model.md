---
title: Přechody stavu na faktuře dodavatele
description: Tento článek vysvětluje přechody stavů na faktuře dodavatele v aplikaci Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261008"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Přechody stavu na faktuře dodavatele

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Tento článek vysvětluje přechody stavů na faktuře dodavatele v aplikaci Microsoft Dynamics 365 Project Operations. Používají se následující stavy: **Návrh**, **Probíhá kontrola**, **Potvrzeno**, **Pozastaveno** a **Zrušeno**.

Následující obrázek znázorňuje přechod stavu.

![Model přechodů stavu subdodávky.](../media/VI_State_Model.jpg)

Následující tabulka vysvětluje, co jednotlivé stavy představují v životním cyklu faktury dodavatele v Project Operations.

| State | Description | Povolené přechody |
| --- | --- | --- |
| Koncepty | Tento stav je počátečním stavem faktury dodavatele. Řady a ceny podléhají změnám. Fakturu dodavatele v tomto stavu nelze upravit a smazat. | Rozpracované |
| Kontroluje se | Tento stav představuje stavem zpraccování faktury dodavatele. Alespoň jeden řádek faktury dodavatele má stav ověření **Probíhá**. | Potvrzeno, pozastaveno |
| Potvrzený | Tento stav představuje fázi faktury dodavatele, kde aplikace vytvořila skutečné náklady pro každý řádek faktury dodavatele. Veškeré propojené skutečné náklady, které byly přiřazeny k řádkům faktury dodavatele, byly stornovány a nahrazeny skutečnými náklady z těchto řádků faktury dodavatele. Fakturu dodavatele v tomto stavu nelze upravit nebo smazat. Můžete použít tlačítko **Zrušit** pro zrušení potvrzené faktury dodavatele. Akce Zrušit zruší dopad akce Potvrdit. | Zrušeno |
| Pozastaveno | <p>Tento stav představuje fázi faktury dodavatele, kde se faktura dodavatele nemůže posunout kvůli problému s fakturou nebo stavu dodavatele. Fakturu dodavatele v tomto stavu nelze potvrdit, zrušit, upravit nebo smazat.</p><p>Pomocí akce Znovu otevřít můžete fakturu dodavatele přesunout do stavů **Návrh** nebo **Probíhá kontrola**. Pokud má alespoň jeden řádek na faktuře dodavatele stav ověření **Probíhá** nebo **Kompletní**, faktura dodavatele bude znovu otevřena ve stavu **Probíhá kontrola**. Pokud mají všechny řádky na faktuře dodavatele stav ověření **Nezahájeno**, faktura dodavatele bude znovu otevřena ve stavu **Koncept**.</p> | Koncept, probíhá kontrola |
| Zrušeno | Tento stav představuje fázi subdodávky, kdy skutečná dodávka materiálů a/nebo práce ze subdodavatelských zdrojů již není vyžadována. Subdodávku v tomto stavu nelze použít k odhadu a personálnímu zajištění požadavků na zdroje a materiály, ani nelze odkazovat na čas, náklady a spotřebu materiálu v projektu. Subdodávku v tomto stavu nelze upravovat ani odstranit. | Žádná |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]