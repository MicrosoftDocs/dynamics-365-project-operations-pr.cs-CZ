---
title: Řádky faktury dodavatele pro milníky
description: Toto téma vysvětluje, jak vytvořit řádky faktury dodavatele pro milníky v subdodávce.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590614"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Řádky faktury dodavatele pro milníky

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Faktura dodavatele v Microsoft Dynamics 365 Project Operations může mít řádky faktury dodavatele pro milníky, které jsou definovány na řádku subdodávky. Projektoví manažeři mohou používat řádky dodavatelské faktury pro milníky k zaznamenávání nákladů na služby, které jsou pořizovány jako náklady založené na milníku, které jsou vynaloženy na služby nebo produkty, které jsou pořizovány pro projekt.

Řádky faktury dodavatele pro milníky musí vždy odkazovat na řádek subdodávky, který má metodu účtování s pevnou cenou. Pokud řádek faktury dodavatele pro milník odkazuje na řádek subdodávky, projektoví manažeři budou moci porovnat a ověřit zdrojové náklady na čas, výdaje nebo materiály, které odkazují na řádek subdodávky s milníkem, který je fakturován dodavatelem.

Následující tabulka obsahuje informace o polích na řádcích faktur dodavatele pro milníky.

| Pole | Description | Funkční dopad |
| --- | --- | --- |
| Name | Název řádku faktury dodavatele pro jeho identifikaci. | Tento název se zobrazí jako první sloupec ve všech vyhledáváních podle řádků faktur dodavatele. |
| Description | Stručný popis služeb a produktů, které jsou fakturovány dodavatelem na řádku faktury dodavatele. | Žádná |
| Subdodávka | Subdodávka, na kterou byly služby původně objednány. | Když je pro fakturu dodavatele vybrána subdodávka, všechny řádky na faktuře dodavatele zdědí tento výběr. Faktura dodavatele nemůže obsahovat řádky faktury dodavatele, které odkazují na různé subdodávky. |
| Řádek subdodávky | Řádek subdodávky, na kterou byly služby objednány. Seznam řádků subdodávky, které lze vybrat, je omezen na řádky na vybrané subdodávce. | Když je vybrán řádek subdodávky na řádku faktury dodavatele pro milníky, pole **Role** a **Kategorie transakcí** a pole související s produktem jsou irelevantní a nejsou k dispozici. Pole **Množství**, **Jednotka** a **Skupina jednotek** také nejsou relevantní pro řádky faktur dodavatele založené na milníku. |
| Datum transakce | Datum, kdy budou v projektu zaznamenány skutečné náklady řádku dodavatelské faktury. | Žádná |
| Třída transakce | Vyberte **Milník**, chcete-li zaznamenat fakturu dodavatele za dokončený milník, který byl definován na řádku subdodávek. | Žádná |
| Milník | Vyberte milník, který je definován na souvisejícím řádku subdodávky, který je označen jako **Připraveno k fakturaci**. | Milníky řádku subdodávky, které mají stav **Připraveno k fakturaci**, lze vybrat na řádku faktury dodavatele. |
| Project | Název projektu, na kterém byly použity fakturované služby. | Je to povinné pole a nemůže být prázdné. |
| Úloha | Název projektového úkolu, na kterém byly použity fakturované služby. Toto pole je dostupné pouze v případě, že je vybrán projekt. Výběr projektového úkolu je volitelný. | Pokud toto pole zůstane prázdné, může projektový manažer porovnat řádek faktury dodavatele s třídou transakce na souvisejícím řádku subdodávky, který je zaznamenán u libovolného úkolu projektu. Pokud řádek faktury dodavatele neodkazuje na řádek subdodávky a toto pole zůstane prázdné, skutečné náklady vytvořené řádkem faktury dodavatele nebudou propojeny s žádnými nevyfakturovanými skutečnými hodnotami prodeje. V tomto případě, pokud je nastavena fakturace na základě úkolů, nemusí být možné náklady fakturovat koncovému zákazníkovi. |
| Částka milníku | Vložte hodnotu milníku, který je definován na řádku subdodávky, který je připraven k fakturaci. | Žádná |
| Prodejní daň | Zadejte částku prodejní daně. | Žádná |
| Celková částka | Celková částka řádku faktury dodavatele, včetně daní. Toto pole se počítá jako *Částka milníku* + *DPH*. | Žádná |

> [!NOTE]
> Když je vytvořen řádek faktury dodavatele, který odkazuje na milník řádku subdodávky, stav milníku subdodávky se aktualizuje na **Faktura dodavatele byla vytvořena**. Poté, co je faktura dodavatele potvrzena, stav milníku řádku subdodávky se aktualizuje na **Faktura dodavatele potvrzena**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
