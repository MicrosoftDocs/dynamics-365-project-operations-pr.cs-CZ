---
title: Řádky faktury dodavatele pro kategorie výdajů
description: Tento článek vysvětluje, jak zaznamenat řádky faktury dodavatele pro kategorie výdajů.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ffad20b53344221ead9b6850ecdc1efd48d5b13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925860"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Řádky faktury dodavatele pro kategorie výdajů

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Faktura dodavatele v Microsoft Dynamics 365 Project Operations může mít řádky faktury dodavatele pro kategorie výdajů. Projektoví manažeři mohou použít řádky faktury dodavatele pro kategorie výdajů k zaznamenání nákladů na služby, které jsou pořizovány jako kategorie nákladů.

Řádky faktury dodavatele pro kategorie výdajů mohou nebo nemusí odkazovat na řádek subdodávky pro kategorie výdajů. Pokud řádek faktury dodavatele pro kategorie výdajů odkazuje na subdodávku, projektoví manažeři budou moci porovnat a ověřit výdaje, které je fakturován řádkem faktury dodavatele, s výdaji, který jsou zaznamenány v těchto kategoriích a schváleny projektovými manažery na projektu.

Následující tabulka obsahuje informace o polích na řádcích faktur dodavatele pro kategorie výdajů.

| Pole | Description | Funkční dopad |
| --- | --- | --- |
| Name | Název řádku faktury dodavatele pro jeho identifikaci. | Tento název se zobrazí jako první sloupec ve všech vyhledáváních podle řádků faktur dodavatele. |
| Description | Stručný popis služeb a produktů, které jsou fakturovány dodavatelem na řádku faktury dodavatele. | Žádná |
| Subdodávka | Subdodávka, na kterou byly služby původně objednány. | Když je pro fakturu dodavatele vybrána subdodávka, všechny řádky na faktuře dodavatele zdědí tento výběr. Faktura dodavatele nemůže obsahovat řádky faktury dodavatele, které odkazují na různé subdodávky. |
| Řádek subdodávky | Řádek subdodávky, na kterou byly služby objednány. Seznam řádků subdodávky, které lze vybrat, je omezen na řádky na vybrané subdodávce. | Když je na řádku faktury dodavatele pro kategorie výdajů vybrán řádek subdodávky, výchozí hodnoty pro pole **Projekt**, **Úkol** a **Kategorie transakcí** se zadávají z odpovídajících polí na řádku subdodávky. Pokud má vybraný řádek subdodávky hodnoty v polích **Projekt**, **Projektový úkol** a **Kategorie transakcí**, hodnoty odpovídajících polí na řádku faktury dodavatele se nemohou lišit od těchto hodnot. |
| Datum transakce | Datum, kdy budou v projektu zaznamenány skutečné náklady řádku dodavatelské faktury. |Žádná |
| Třída transakce | Vyberte **Výdaj** k zaznamenání faktury dodavatele pro kategorii výdajů. | Hodnota **Výdaj** označuje, že řádek faktury dodavatele se používá k zaznamenání fakturované částky za služby, které byly pořízeny jako kategorie nákladů. |
| Project | Název projektu, na kterém byly použity fakturované služby. | Je to povinné pole a nemůže být prázdné. |
| Úloha | Název projektového úkolu, na kterém byly použity fakturované služby. Toto pole je dostupné pouze v případě, že je vybrán projekt. Výběr projektového úkolu je volitelný. | Pokud toto pole zůstane prázdné, může projektový manažer porovnat řádek faktury dodavatele s výdaji, které jsou zaznamenány u libovolného úkolu projektu. Pokud řádek faktury dodavatele neodkazuje na řádek subdodávky a toto pole zůstane prázdné, skutečné náklady vytvořené řádkem faktury dodavatele nebudou propojeny s žádnými nevyfakturovanými skutečnými hodnotami prodeje. V tomto případě, pokud je nastavena fakturace na základě úkolů, nemusí být možné náklady fakturovat koncovému zákazníkovi. |
| Kategorie transakce | Kategorie transakce, která je fakturována. Pro vybranou kategorii transakce musí být vytvořena odpovídající kategorie výdajů. | Kombinace hodnot **Kategorie transakcí** a **Jednotka** bude použita jako výchozí nebo vypočítaná hodnota pro pole **Jednotková cena** na řádku faktury dodavatele. |
| Množství | Do řádku faktury zadejte množství, které je fakturováno dodavatelem. |Žádná|
| Skupina jednotek | Výchozí hodnota je zadána na základě skupiny jednotek vybrané kategorie transakcí. | Žádná |
| Jednotka | Výchozí hodnota je základní jednotka skupiny jednotek, která je vybrána. Tuto hodnotu můžete změnit a koupit jakoukoli jednotku skupiny jednotek. | Kombinace hodnot **Kategorie transakcí** a **Jednotka** bude použita jako výchozí nebo vypočítaná hodnota pro pole **Jednotková cena** na řádku faktury dodavatele. |
| Jednotková cena | Výchozí cenová jednotka používá kombinaci hodnot **Kategorie transakcí** a **Jednotka** z ceníku projektu, který platí pro datum transakce na řádku faktury dodavatele. | Pokud je cena pro příslušný ceník projektu nastavena v jednotce, která se liší od jednotky na řádku faktury dodavatele, systém použije k výpočtu jednotkové ceny převod jednotek. |
| Dílčí součet | Toto pole je pouze pro čtení a počítá se jako *Množství* &times; *Jednotková cena*, pokud jsou zadány hodnoty do polí **Množství** a **Jednotková cena**. Pokud je jedno nebo obě pole prázdná, můžete do tohoto pole zadat hodnotu.| Žádná |
| Prodejní daň | Zadejte částku prodejní daně. | Žádná |
| Celková částka | Celková částka řádku faktury dodavatele, včetně daní. Toto pole se počítá jako *Mezisoučet* + *DPH*. | Žádná |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
