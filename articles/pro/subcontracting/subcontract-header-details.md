---
title: Podrobnosti záhlaví pro subdodávky
description: Tento článek vysvětluje funkce poskytované v záhlaví subdodávky v Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 00b7c08235654d4bed0bcb4053d2044a3d092b54
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522552"
---
# <a name="header-details-for-subcontracts"></a>Podrobnosti záhlaví pro subdodávky

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Tento článek vysvětluje funkce poskytované v záhlaví subdodávky v Dynamics 365 Project Operations.

Když projektový manažer plánuje a provádí projekty, může zaměstnávat subdodavatele a nakupovat produkty a služby od prodejců. Když správce projektu potřebuje zakoupit produkty nebo služby, může vytvořit subdodávku v Project Operations.

Chcete-li vytvořit subdodávku postupujte podle následujících kroků.

1. V navigačním podokně vyberte **Subdodávky**, a na stránce **Subdodávka** vyberte **Nový**.
2. Zadejte požadované informace a zvolte **Uložit**.

    Následující tabulka obsahuje informace o polích na stránce **Záhlaví subdodávky**.

    | Pole | Popis |Funkční dopad |
    |---|------|---| 
    | Jméno | Název subdodávky | Ve všech rozevíracích seznamech subdodávek je název subdodávky uveden v prvním sloupci, což vám pomůže s identifikací subdodávky. | 
    | Popis | Stručný popis služeb a produktů, které jsou nakupovány na základě subdodávky. | Nic |
    | Dodavatel | Název společnosti, od které jsou produkty a služby nakupovány. Tento účet dodavatele má typ vztahu **Prodejce** nebo **Dodavatel**. | Na základě vybraného dodavatele se automaticky zadají výchozí hodnoty pro následující pole:<br/> **• Měna** </br> **• Ceníky** </br> **• Platební podmínky**</br> **• Adresa platby**</br> **• Fakturační adresa**</br> **• Fakturační adresa – jméno** </br>**• Manažer účtu dodavatele**|
    | Datum subdodávky | Datum vytvoření subdodávky. | Datum subdodávky se používá k výběru správného nákupního ceníku buď z ceníků, které jsou připojeny k příslušnému dodavateli, nebo z parametrů projektu. |
    | Důvod stavu | Stav řádku subdodávky | Stav určuje, kde se subdodávka v obchodním procesu nachází a zda ji lze upravit. <br/>Mezi tyto hodnoty patří:<br>• **Koncept**: Subdodávku lze upravit. Upravovat můžete pouze subdodávky ve stavu **Koncept**.<br/>• **Potvrzeno**: Jednání s dodavatelemje dokončeno a subdodávka je schválena k dodání. <br/>• **Uzavřeno**: Dodávka na subdodávce je dokončena.<br/>• **Zrušeno**: Subdodávka byla zrušena a není plánována žádná dodávka.  | 
    | Měna | Měna, ve které jsou produkty a služby zakoupeny. Výchozí hodnota je automaticky zadávána z účtu dodavatele, ale lze ji změnit. | Měna subdodávky se používá k výběru nákupního ceníku buď z ceníků, které jsou připojeny k příslušnému dodavateli, nebo z parametrů projektu. K subdodávce nelze přidružit ceníky v jiné měně. Náklady na čas, výdaje a materiály, které zdroje dodavatelů dodají z této subdodávky, jsou v projektu zaznamenány v této měně. Po uložení záznamu o subdodávce nelze na subdodávky změnit.|
    | Smluvní jednotka | Divize společnosti, která uzavírá kupní smlouvu nebo subdodávku s prodejcem. | Nic |
    | Platební podmínky | Platební podmínky pro faktury dodavatele vystavené na základě této subdodávky. Výchozí hodnota je automaticky zadávána ze záznamu účtu dodavatele. | Platební podmínky ze subdodávky jsou zkopírovány do všech faktur dodavatele, které souvisejí s touto subdodávkou. Platební podmínky lze aktualizovat, pokud má subdodávka stav **Koncept**. | 
    | Adresa platby | Adresa dodavatele, kterému musí být zaslány platby. Výchozí hodnota je automaticky zadávána ze záznamu účtu dodavatele. | Platební adresa ze subdodávky je zkopírována jako platební adresa do všech faktur dodavatele, které jsou pro tuto subdodávku vytvořeny. Platební adresu lze aktualizovat, pokud má subdodávka stav **Koncept**.|
    | Fakturační adresa – jméno | Jméno osoby nebo divize ve společnosti dodavatele, která bude zasílat fakturu. Výchozí hodnota je automaticky zadávána ze záznamu účtu dodavatele. | Hodnota **Fakturační adresa – jméno** ze subdodávky je zkopírována do všech faktur dodavatele, které souvisejí s touto subdodávkou. Toto pole lze aktualizovat, pokud má subdodávka stav **Koncept**.|
    | Fakturační adresa | Adresa, která je použita na fakturách dodavatele. Výchozí hodnota je automaticky zadávána ze záznamu účtu dodavatele. | Tato adresa je adresa „Faktura od“ na fakturách dodavatele, které jsou vytvořeny pro tuto subdodávku. |
    | Dílčí součet | Pokud subdodávka neobsahuje řádky, zadejte mezisoučet objednávky před zdaněním. Pokud má subdodávka řádky, je toto pole pouze pro čtení. Částka, která je zobrazena, je mezisoučtem částky ze všech řádků na subdodávce. | Nic |
    | Celková daň | Pokud subdodávka neobsahuje řádky, zadejte celkové daně na této subdodávce. Pokud má subdodávka řádky, je toto pole pouze pro čtení. Částka, která je zobrazena, je součtem částky daně ze všech řádků na subdodávce. | Nic |
    | Celková částka | Tato počítané pole ukazuje celkovou částku subdodávky po zahrnutí daní. | Nic |
    | Datum potvrzení | Datum, kdy byla subdodávka potvrzena. | Nic |
    | Vyžádal/a | Ve výchozím nastavení je toto pole nastaveno na jméno uživatele, který vytváří subdodávku. Tvůrce subdodávky však může změnit hodnotu označující osobu, jejímž jménem subdodávku vytváří. | Nic |
    | Manažer účtu dodavatele | Název primárního kontaktu účtu dodavatele. Výchozí hodnota je automaticky zadávána ze záznamu účtu dodavatele. Jako správce účtu dodavatele subdodávky můžete vybrat jiný kontakt. | Můžete nastavit e-mailové výstrahy upozorňující kontakt na změny subdodávky v důsledku vyjednávání o ceně. |
