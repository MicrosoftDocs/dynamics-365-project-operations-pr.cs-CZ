---
title: Evidence času, výdajů a spotřeby materiálu pro součásti subdodávky
description: Toto téma vysvětluje, jak společnost Microsoft sleduje čas, výdaje a využití materiálu zaznamenané u projektů ze součástí subdodávky v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 04c78dd48367c3720b8f5ad5d924ed106da6a128
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903364"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Evidence času, výdajů a spotřeby materiálu u projektů u součástí subdodávky

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Toto téma vysvětluje, jak společnost Microsoft sleduje čas, výdaje a využití materiálu zaznamenané u projektů ze součástí subdodávky v Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Kalkulace času subdodavatele na projektech
V Project Operations mohou smluvní pracovníci zaznamenávat čas na projektech podobným způsobem jako zaměstnanci. Při zadávání času stráveného na projektech a/nebo projektových úkolech si smluvní pracovník může vybrat konkrétní subdodávku a řádek subdodávky.

Když je čas předložený smluvními pracovníky schválen, náklady na projekt se zaznamenají s použitím sazby jednotkových nákladů, která je nastavena pro daný zdroj smluvního pracovníka v sekci **Ceny rolí** nákupního ceníku na subdodávce.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Kalkulace výdajů subdodávky na projektech
Při zadávání výdajů vynaložených na projekty můžete u položky výdajů vybrat subdodávku a řádek subdodávky. 

Když je tato položka výdajů odeslána a schválena, částka výdajů se zaznamená do projektu na základě jednotkových nákladů, které jsou nastaveny pro tuto kategorii transakcí v sekci **Ceny kategorií** nákupního ceníku na subdodávce.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Kalkulace spotřeby materiálů subdodávky na projektech
Při zadávání spotřebovaných materiálů u projektů můžete vybrat subdodávku a řádek subdodávky v protokolu spotřeby materiálu. Když je protokol spotřeby materiálů odeslán a schválen, částka materiálů se zaznamená do projektu na základě jednotkových nákladů, které jsou nastaveny pro tento produkt v sekci **Položky ceníku** ceníku subdodávky.

Spotřebu materiálu lze v projektech také zaznamenat u produktů nezahrnutých do katalogu. Tento typ spotřeby materiálu lze také propojit se subdodávkou a řádkem subdodávky. Při zaznamenávání spotřeby materiálu u produktů nezahrnutých do katalogu musíte zadat cenu za jednotku nezahrnutého produktu. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
