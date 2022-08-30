---
title: Řádky faktury dodavatele pro čas
description: Tento článek vysvětluje, jak zaznamenat řádky faktur dodavatele pro časové náklady, které vložili subdodavatelé.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262004"
---
# <a name="vendor-invoice-lines-for-time"></a>Řádky faktury dodavatele pro čas

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Faktura dodavatele v Microsoft Dynamics 365 Project Operations může mít řádky faktury dodavatele pro čas. Projektoví manažeři mohou používat řádky faktur dodavatele pro čas k zaznamenávání nákladů na čas subdodavatelů na projektech.

Řádky faktury dodavatele pro čas mohou nebo nemusí odkazovat na řádek subdodávky pro čas. Pokud řádek faktury dodavatele pro čas odkazuje na subdodávku, projektoví manažeři budou moci porovnat a ověřit čas, který je fakturován řádkem faktury dodavatele, s časem, který je zaznamenán subdodavateli a schválen projektovými manažery na projektu.

Následující tabulka obsahuje informace o polích na řádcích faktur dodavatele pro čas.

| Pole | Description | Funkční dopad |
| --- | --- | --- |
| Name | Název řádku faktury dodavatele pro jeho identifikaci. | Tento název se zobrazí jako první sloupec ve všech vyhledáváních podle řádků faktur dodavatele. |
| Description | Stručný popis služeb a produktů, které jsou fakturovány dodavatelem na řádku faktury dodavatele. | Žádná |
| Subdodávka | Subdodávka, na kterou byly služby původně objednány. | Když je pro fakturu dodavatele vybrána subdodávka, všechny řádky na faktuře dodavatele zdědí tento výběr. Faktura dodavatele nemůže obsahovat řádky faktury dodavatele, které odkazují na různé subdodávky. |
| Řádek subdodávky | Řádek subdodávky, na kterou byly služby objednány. Seznam řádků subdodávky, které lze vybrat, je omezen na řádky na vybrané subdodávce. | Když je na řádku faktury dodavatele pro čas vybrán řádek subdodávky, výchozí hodnoty pro pole **Projekt**, **Role** a **Rezervovatelný zdroj** se zadávají z odpovídajících polí na řádku subdodávky. Pokud má vybraný řádek subdodávky hodnoty v polích **Projekt**, **Role** a **Rezervovatelné**, hodnoty odpovídajících polí na řádku faktury dodavatele se nemohou lišit od těchto hodnot. |
| Datum transakce | Datum, kdy budou v projektu zaznamenány skutečné náklady řádku dodavatelské faktury. | Žádná |
| Třída transakce | Výchozí hodnotou je **Čas**. | Hodnota **Čas** označuje, že řádek faktury dodavatele se používá k zaznamenání fakturované částky času subdodavatele. |
| Project | Název projektu, na kterém byly použity fakturované služby. | Je to povinné pole a nemůže být prázdné. |
| Úloha | Název projektového úkolu, na kterém byly použity fakturované služby. Toto pole je dostupné pouze v případě, že je vybrán projekt. Výběr projektového úkolu je volitelný. | Pokud toto pole zůstane prázdné, může projektový manažer porovnat řádek faktury dodavatele s časem, který je zaznamenán zdroji subdodavatele u libovolného úkolu projektu. Pokud řádek faktury dodavatele neodkazuje na řádek subdodávky a toto pole zůstane prázdné, skutečné náklady vytvořené řádkem faktury dodavatele nebudou propojeny s žádnými nevyfakturovanými skutečnými hodnotami prodeje. V tomto případě, pokud je nastavena fakturace na základě úkolů, nemusí být možné náklady fakturovat koncovému zákazníkovi. |
| Role | Role zdrojů subdodávky, jejichž čas se fakturuje. | Toto pole určuje roli, kterou plní subdodavatelské zdroje, jejichž čas je fakturován na faktuře dodavatele. |
| Rezervovatelný zdroj | Název subdodavatele, jehož čas se fakturuje. Výběr rezervovatelného zdroje je volitelný. | Pokud toto pole zůstane prázdné, může projektový manažer porovnat řádek faktury dodavatele s časem, který je zaznamenán libovolným zdrojem, který patří dodavateli na řádku faktury dodavatele. |
| Množství | Do řádku faktury zadejte počet hodin času, které jsou fakturovány dodavatelem. |Žádná |
| Skupina jednotek | Výchozí hodnota je **Skupina časových jednotek** a nelze ji změnit. | Žádná |
| Jednotka | Výchozí hodnota je základní jednotka hodin ze skupiny časových jednotek. Tuto hodnotu můžete změnit a koupit jakoukoli jednotku času skupiny časových jednotek, například den nebo týden. | Kombinace hodnot **Role** a **Jednotka** bude použita jako výchozí nebo vypočítaná hodnota pro pole **Jednotková cena** na řádku faktury dodavatele. |
| Jednotková cena | Výchozí cenová jednotka používá kombinaci hodnot **Role** a **Jednotka** z ceníku projektu, který platí pro datum transakce na řádku faktury dodavatele. | Pokud je cena pro příslušný ceník projektu nastavena v jednotce, která se liší od jednotky na řádku faktury dodavatele, systém použije k výpočtu jednotkové ceny převod jednotek. |
| Dílčí součet | Toto pole je pouze pro čtení a počítá se jako *Množství* &times; *Jednotková cena*, pokud jsou zadány hodnoty do polí **Množství** a **Jednotková cena**. Pokud je jedno nebo obě pole prázdná, můžete do tohoto pole zadat hodnotu. | Žádná |
| Prodejní daň | Zadejte částku prodejní daně. | Žádná |
| Celková částka | Celková částka řádku faktury dodavatele, včetně daní. Toto pole se počítá jako *Mezisoučet* + *DPH*. | Žádná |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
