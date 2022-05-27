---
title: Podrobnosti záhlaví pro faktury dodavatele
description: Toto téma vysvětluje funkce poskytované v záhlaví faktury dodavatele v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 17be106d5486358ff0bbf011af3da26a4c85a274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575572"
---
# <a name="header-details-for-vendor-invoices"></a>Podrobnosti záhlaví pro faktury dodavatele

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Toto téma vysvětluje funkce poskytované v záhlaví faktury dodavatele v Microsoft Dynamics 365 Project Operations.

Když projektoví manažeři plánují a realizují projekty, mohou zaměstnávat subdodavatele a nakupovat produkty a služby od prodejců. Během realizace projektu vznikají náklady na služby, materiály a kategorie nákladů, které jsou pořizovány na základě subdodávek s dodavateli. Dodavatelé fakturují tyto náklady projektům vytvořením dodavatelských faktur.

Následující tabulka poskytuje informace o polích v záhlaví faktur dodavatele v Project Operations.

| Pole | Description | Funkční dopad |
| --- | --- | --- |
| Name | Název faktury dodavatele. | Ve všech rozevíracích seznamech faktur dodavetele je název faktury dodavatele uveden v prvním sloupci, což vám pomůže s identifikací faktury dodavatele. Ve výchozím nastavení, když je faktura dodavatele vytvořena ze subdodávky, pole **Název** faktury dodavatele je nastaveno na hodnotu, která se skládá z názvu subdodávky a aktuálního data. |
| Description | Stručný popis služeb a produktů, které jsou fakturovány na faktuře dodavatele. | Žádná |
| Dodavatel | Název společnosti, která fakturuje produkty a služby. Tato společnost by měla být záznamem účtu, který má typ vztahu **Prodejce** nebo **Dodavatel**. | <p>Na základě vybraného dodavatele se automaticky zadají výchozí hodnoty v následujících polích:</p><ul><li>Měna</li><li>Ceníky</li><li>Platební podmínky</li><li>Adresa platby</li></ul> |
| Subdodávka | Odkaz na subdodávku pro fakturu dodavatele. | <p>Na základě vybrané subdodávky se automaticky zadají výchozí hodnoty v následujících polích:</p><ul><li>Měna</li><li>Ceníky</li><li>Platební podmínky</li><li>Adresa platby</li></ul><p>Subdodávka, která je vybrána v hlavičce faktury dodavatele, je standardně zadána do řádků faktury dodavatele a nelze ji tam změnit.</p> |
| Datum vystavení faktury | Datum pro skutečné náklady, které bude vytvořeno po potvrzení faktury dodavatele. | Datum faktury se také používá k výběru správného nákupního ceníku buď z ceníků, které jsou připojeny k příslušnému dodavateli, nebo z parametrů projektu. |
| Důvod stavu | Stav faktury dodavatele | <p>Stav určuje, kde se faktura dodavatele v obchodním procesu nachází a zda ji lze upravit. Zde jsou některé z dostupných hodnot:</p><ul><li>**Koncept** - fakturu dodavatele lze upravit.</li><li>**Potvrzeno** – Faktura dodavatele byla ověřena a potvrzena. Faktury dodavatele v tomto stavu nelze upravit nebo smazat.</li><li>**V procesu** – Probíhá kontrola faktury dodavatele. Faktury dodavatele v tomto stavu lze upravit, ale nelze je smazat.</li><li>**Zrušeno** – Faktura dodavatele byla stornována. Faktury dodavatele v tomto stavu nelze upravit nebo smazat.</li></ul> |
| Měna | Měna, kterou dodavatel fakturuje za produkty a služby na faktuře dodavatele. | Na faktuře dodavatele, která odkazuje na subdodávku, je měna subdodávky standardně zadána jako měna faktury dodavatele. Na faktuře dodavatele, která neodkazuje na subdodávku, je výchozí hodnota zadána ze záznamu účtu dodavatele a lze ji změnit. Po uložení faktury dodavatele již nelze měnu upravovat. |
| Smluvní jednotka | Divize společnosti, která je zodpovědná za příjem služeb a/nebo produktů od prodejce. | Žádná |
| Platební podmínky | Platební podmínky pro faktury dodavatele, které jsou vystavené. Výchozí hodnota je automaticky zadávána ze záznamu účtu dodavatele. | Platební podmínky ze subdodávky jsou zkopírovány do všech faktur dodavatele, které souvisejí s touto subdodávkou. Platební podmínky lze aktualizovat, pokud má faktura dodavatele stav **Koncept**. |
| Adresa platby | Adresa dodavatele, kterému musí být zaslány platby. Výchozí hodnota je automaticky zadávána ze záznamu účtu dodavatele. | Platební adresa ze subdodávky je zkopírována jako platební adresa do všech faktur dodavatele, které jsou pro tuto subdodávku vytvořeny. Platební adresu lze aktualizovat, pokud má faktura dodavatele stav **Koncept**. |
| Dílčí součet | Pokud faktura dodavatele neobsahuje řádky, zadejte mezisoučet faktury před zdaněním. Pokud má faktura dodavatele řádky, je toto pole pouze pro čtení. V takové připadě je částka, která je zobrazena, mezisoučtem částky ze všech řádků na faktuře dodavatele. | Žádná |
| Celková daň | Pokud faktura dodavatele neobsahuje řádky, zadejte celkovou daň v subdodávce. Pokud má faktura dodavatele řádky, je toto pole pouze pro čtení. V takové připadě je částka, která je zobrazena, součtem částek daně ze všech řádků na faktuře dodavatele. | Žádná |
| Celková částka | Toto počítané pole ukazuje celkovou částku faktury dodavatele po zahrnutí daní. | Žádná |

> [!NOTE]
> Následující pole na faktuře dodavatele nelze po uložení faktury dodavatele změnit: **Prodejce**, **Subdodávka**, **Měna**, **Smluvní jednotka** a **Platební podmínky**. Pokud jsou vyžadovány nějaké změny v těchto polích na faktuře dodavatele, musíte fakturu dodavatele odstranit a vytvořit novou fakturu dodavatele.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
