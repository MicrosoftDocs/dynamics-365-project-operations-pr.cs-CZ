---
title: Přechody stavů u subdodávky
description: Tento článek vysvětluje přechody stavů u subdodávky v Microsoft Dynamics 365 Project Operations při vytvoření, realizaci a uzavření subdodávky.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 02553099a6728c19c219659dff431ff9a5cf10fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261181"
---
# <a name="state-transitions-on-a-subcontract"></a>Přechody stavů u subdodávky 

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Tento článek vysvětluje přechody stavů u subdodávky v aplikaci Microsoft Dynamics 365 Project Operations. Každý stav je reprezentován buď jako koncept, potvrzeno, uzavřeno nebo zrušeno. Následující obrázek znázorňuje přechody stavů.

![Model stavu subdodávky](../media/SubconStates.png)  

Následující tabulka obsahuje popis toho, co jednotlivé stavy představují v životním cyklu subdodávky v Project Operations.

| State | Description | Povolené přechody |
| --- | --- | --- |
| Koncepty | Představuje počáteční stav subdodávky. Probíhají jednání s dodavatelem. Řady a ceny podléhají změnám. Subdodávka v tomto stavu může být použita k odhadu a personálnímu zajištění požadavků na zdroje a materiály. Může také odkazovat na čas, náklady a spotřebu materiálu na projektu. Subdodávku v tomto stavu lze upravovat a odstranit. | Potvrzený |
| Potvrzený | Představuje fázi subdodávky po dokončení jednání s dodavatelem o cenách a nakupovaných řádkových položkách. Skutečná dodávka materiálů a/nebo práce ze subdodavatelských zdrojů však stále probíhá. Subdodávka v tomto stavu může být použita k odhadu a personálnímu zajištění požadavků na zdroje a materiály. Může také odkazovat na čas, náklady a spotřebu materiálu na projektu. Subdodávku v tomto stavu nelze upravovat ani odstranit. Tlačítko **Zrušit** umožňuje zrušit potvrzenou subdodávku. Tlačítko **Znovu otevřít** umožňuje znovu otevřít subdodávku a vrátit ji zpět do stavu **Koncept**. Tlačítkem **Zavřít** uzavřete potvrzenou subdodávku. | Zavřeno <br> Zrušeno <br> Koncepty |
| Zavřeno | Představuje fázi subdodávky, kdy je dokončena skutečná dodávka materiálů a/nebo práce ze subdodavatelských zdrojů. Subdodávka v tomto stavu již nemůže být použita k odhadu a personálnímu zajištění požadavků na zdroje a materiály. Nemůže také odkazovat na čas, náklady a spotřebu materiálu na projektu. Subdodávku v tomto stavu nelze upravovat ani odstranit. | None |
| Zrušeno | Představuje fázi subdodávky, kdy skutečná dodávka materiálů a/nebo práce ze subdodavatelských zdrojů již není potřebná. Subdodávku v tomto stavu nelze použít k odhadu a personálnímu zajištění požadavků na zdroje a materiály, ani nelze odkazovat na čas, náklady a spotřebu materiálu v projektu. Subdodávku v tomto stavu nelze upravovat ani odstranit. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
