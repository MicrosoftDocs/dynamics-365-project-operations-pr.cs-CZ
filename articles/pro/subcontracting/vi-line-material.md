---
title: Řádky faktury dodavatele pro produkty
description: Tento článek vysvětluje, jak zaznamenat řádky faktury dodavatele pro produkty a jak používat různá pole k zaznamenání nákupů produktů od dodavatelů.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261550"
---
# <a name="vendor-invoice-lines-for-products"></a>Řádky faktury dodavatele pro produkty

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Faktura dodavatele v Microsoft Dynamics 365 Project Operations může mít řádky dodavatelské faktury pro produkty (také označované jako materiály). Projektoví manažeři mohou používat řádky faktur dodavatele pro produkty k zaznamenávání nákladů produktů, které byly zakoupeny v projektech.

Řádky faktury dodavatele pro produkty mohou nebo nemusí odkazovat na řádek subdodávky pro materiály. Pokud řádek faktury dodavatele pro produkty odkazuje na subdodávku, projektoví manažeři budou moci porovnat a ověřit produkty, které jsou fakturovány řádkem faktury dodavatele, s použitím zakoupených produktů, které jsou zaznamenány subdodavateli a schváleny projektovými manažery.

Následující tabulka obsahuje informace o polích na řádcích faktur dodavatele pro produkty.

| Pole | Description | Funkční dopad |
| --- | --- | --- |
| Name | Název řádku faktury dodavatele pro jeho identifikaci. | Tento název se zobrazí jako první sloupec ve všech vyhledáváních podle řádků faktur dodavatele. |
| Description | Stručný popis služeb a produktů, které jsou fakturovány dodavatelem na řádku faktury dodavatele. | Žádná |
| Subdodávka | Subdodávka, na kterou byly produkty původně objednány. | Když je pro fakturu dodavatele vybrána subdodávka, všechny řádky na faktuře dodavatele zdědí tento výběr. Faktura dodavatele nemůže obsahovat řádky faktury dodavatele, které odkazují na různé subdodávky. |
| Řádek subdodávky | Řádek subdodávky, na kterou byly produkty objednány. Seznam řádků subdodávky, které lze vybrat, je omezen na řádky na vybrané subdodávce. | Když je na řádku faktury dodavatele pro produkty vybrán řádek subdodávky, výchozí hodnoty pro pole **Projekt**, **Úkol** a **Produkt** se zadávají z odpovídajících polí na řádku subdodávky. Pokud má vybraný řádek subdodávky hodnoty v polích **Projekt**, **Úkol** a **Produkt**, hodnoty odpovídajících polí na řádku faktury dodavatele se nemohou lišit od těchto hodnot. |
| Datum transakce | Datum, kdy budou v projektu zaznamenány skutečné náklady řádku dodavatelské faktury. | Žádná|
| Třída transakce | Když jsou produkty fakturovány, toto pole by mělo být nastaveno na **Materiál**. | Hodnota **Materiál** označuje, že řádek faktury dodavatele se používá k zaznamenání fakturované částky za materiály, které byly zakoupeny. |
| Project | Název projektu, na kterém byly použity fakturované produkty. | Je to povinné pole a nemůže být prázdné. |
| Úloha | Název projektového úkolu, na kterém byly použity fakturované produkty. Toto pole je dostupné pouze v případě, že je vybrán projekt. Výběr projektového úkolu je volitelný. | Pokud toto pole zůstane prázdné, může projektový manažer porovnat řádek faktury dodavatele se zakoupeným produktem, který se používá u libovolného úkolu projektu. Pokud řádek faktury dodavatele neodkazuje na řádek subdodávky a toto pole zůstane prázdné, skutečné náklady vytvořené řádkem faktury dodavatele nebudou propojeny s žádnými nevyfakturovanými skutečnými hodnotami prodeje. V tomto případě, pokud je nastavena fakturace na základě úkolů, nebude možné náklady fakturovat koncovému zákazníkovi. |
| Vybrat produkt | Vyberte, jestli fakturovaný produkt existuje v katalogu nebo není zahrnutý v katalogu. | Výchozí hodnota se zadává z řádku subdodávky, když je vybrán řádek subdodávky. |
| Produkt | Vybrat produkt z katalogu. Pokud produkt není zahrnutý v katalogu, zadejte název produktu. | Toto pole se používá k zadání výchozích nákupních cen pro stávající produkty. |
| Množství | Do tohoto řádku faktury zadejte množství mateiálu, které je fakturováno dodavatelem. | Žádná |
| Skupina jednotek | Vyberte skupinu jednotek jednotky, ve které je vyjádřeno fakturované množství. | Žádná |
| Jednotka | Výchozí hodnota je základní jednotka skupiny jednotek, která je vybrána. Tuto hodnotu můžete změnit a vyplatit jakoukoli jednotku vybrané skupiny jednotek. | Kombinace hodnot **Produkt** a **Jednotka** bude použita jako výchozí nebo vypočítaná hodnota pro pole **Jednotková cena** na řádku faktury dodavatele. |
| Jednotková cena | Výchozí cenová jednotka používá kombinaci hodnot **Produkt** a **Jednotka** z ceníku projektu, který platí pro datum transakce na řádku faktury dodavatele. | Žádná |
| Dílčí součet | Toto pole je pouze pro čtení a počítá se jako *Množství* &times; *Jednotková cena*, pokud jsou zadány hodnoty do polí **Množství** a **Jednotková cena**. Pokud je jedno nebo obě pole prázdná, můžete do tohoto pole zadat hodnotu. | Žádná |
| Prodejní daň | Zadejte částku prodejní daně. | Žádná |
| Celková částka | Celková částka řádku faktury dodavatele, včetně daní. Toto pole se počítá jako *Mezisoučet* + *DPH*. | Žádná |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
