---
title: Evidence času, výdajů a spotřeby materiálu pro součásti subdodávky
description: Tento článek vysvětluje, jak společnost Microsoft sleduje čas, výdaje a využití materiálu zaznamenané u projektů ze součástí subdodávky v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522505"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Evidence času, výdajů a spotřeby materiálu u projektů u součástí subdodávky

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Tento článek vysvětluje, jak společnost Microsoft sleduje čas, výdaje a využití materiálu zaznamenané u projektů ze součástí subdodávky v Microsoft Dynamics 365 Project Operations.

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
