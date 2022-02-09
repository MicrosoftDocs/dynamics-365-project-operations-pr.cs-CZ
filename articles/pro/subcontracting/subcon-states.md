---
title: Přechody stavů u subdodávky
description: Toto téma vysvětluje přechody stavů u subdodávky v Microsoft Dynamics 365 Project Operations při vytvoření, realizaci a uzavření subdodávky.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d67f4a3cd834c25462304c2d75c824427fcbd034
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903365"
---
# <a name="state-transitions-on-a-subcontract"></a>Přechody stavů u subdodávky 

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Toto téma vysvětluje přechody stavů u subdodávky v aplikaci Microsoft Dynamics 365 Project Operations. Každý stav je reprezentován buď jako koncept, potvrzeno, uzavřeno nebo zrušeno. Následující obrázek znázorňuje přechody stavů.

![Model stavu subdodávky](../media/SubconStates.png)  

Následující tabulka obsahuje popis toho, co jednotlivé stavy představují v životním cyklu subdodávky v Project Operations.

| State | Description | Povolené přechody |
| --- | --- | --- |
| Koncept | Představuje počáteční stav subdodávky. Probíhají jednání s dodavatelem. Řady a ceny podléhají změnám. Subdodávka v tomto stavu může být použita k odhadu a personálnímu zajištění požadavků na zdroje a materiály. Může také odkazovat na čas, náklady a spotřebu materiálu na projektu. Subdodávku v tomto stavu lze upravovat a odstranit. | Potvrzeno |
| Potvrzeno | Představuje fázi subdodávky po dokončení jednání s dodavatelem o cenách a nakupovaných řádkových položkách. Skutečná dodávka materiálů a/nebo práce ze subdodavatelských zdrojů však stále probíhá. Subdodávka v tomto stavu může být použita k odhadu a personálnímu zajištění požadavků na zdroje a materiály. Může také odkazovat na čas, náklady a spotřebu materiálu na projektu. Subdodávku v tomto stavu nelze upravovat ani odstranit. Tlačítko **Zrušit** umožňuje zrušit potvrzenou subdodávku. Tlačítko **Znovu otevřít** umožňuje znovu otevřít subdodávku a vrátit ji zpět do stavu **Koncept**. Tlačítkem **Zavřít** uzavřete potvrzenou subdodávku. | Zavřeno <br> Zrušeno <br> Koncept |
| Zavřeno | Představuje fázi subdodávky, kdy je dokončena skutečná dodávka materiálů a/nebo práce ze subdodavatelských zdrojů. Subdodávka v tomto stavu již nemůže být použita k odhadu a personálnímu zajištění požadavků na zdroje a materiály. Nemůže také odkazovat na čas, náklady a spotřebu materiálu na projektu. Subdodávku v tomto stavu nelze upravovat ani odstranit. | None |
| Zrušeno | Představuje fázi subdodávky, kdy skutečná dodávka materiálů a/nebo práce ze subdodavatelských zdrojů již není potřebná. Subdodávku v tomto stavu nelze použít k odhadu a personálnímu zajištění požadavků na zdroje a materiály, ani nelze odkazovat na čas, náklady a spotřebu materiálu v projektu. Subdodávku v tomto stavu nelze upravovat ani odstranit. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]